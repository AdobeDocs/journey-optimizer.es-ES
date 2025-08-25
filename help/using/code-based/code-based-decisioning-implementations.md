---
title: Deduplicación de elementos de decisión en implementaciones basadas en código
description: Esta página muestra cómo aplicar la anulación de duplicación a las solicitudes de toma de decisiones en la implementación basada en código de Journey Optimizer.
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: f9477611-b792-4b28-8ec2-6bbea2fa3328
source-git-commit: 57686b9684f9233c81bd46b67d12ec5f1e3544c5
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---

# Decisiones en las implementaciones de experiencias basadas en código

Cuando utilice Decisioning en experiencias basadas en código, considere la posibilidad de agregar los siguientes indicadores a la implementación de su cliente en los casos que se describen a continuación.

## Prueba de experiencias basadas en código mediante decisiones {#code-based-test-decisions}

<!--Currently you cannot simulate content from the user interface in a [code-based experience](create-code-based.md) campaign or journey using decisions.-->

Al probar la [experiencia basada en código](create-code-based.md) con toma de decisiones, el indicador `dryRun` se puede usar para suprimir eventos de comentarios tanto para los contadores de informes como de límite.

Después de publicar la campaña, agregue el indicador `dryRun` al bloque de evento XDM `data` en la implementación del cliente:

    &quot;
    &lbrace;
    &quot;data&quot;: &lbrace;
    &quot;__adobe&quot;: &lbrace;
    &quot;ajo&quot;: &lbrace;
    &quot;dryRun&quot;: true
    &rbrace;
    &rbrace;
    
    
    &quot;

<!--
>[!CAUTION]
>
>Adding the `dryRun` flag to your request will prevent feedback to be captured for reporting and frequency counters from being added to.-->

## Deduplicación de elementos de decisión en implementaciones basadas en código {#code-based-decisioning-deduplication}

Al usar [políticas de decisión](../experience-decisioning/create-decision.md) en sus experiencias basadas en código, puede aplicar la anulación de duplicación a sus solicitudes de toma de decisiones en su implementación de cliente.

Las solicitudes de decisión (a través de Konductor) aceptan el indicador de deduplicación, que administra la exclusividad de los elementos de decisión en una sola solicitud compuesta de varias políticas de decisión o ubicaciones.

### Lógica de deduplicación {#deduplication-logic}

Para cualquier solicitud de toma de decisiones, puede tener una o más políticas/ubicaciones de decisión basadas en la configuración.

* Para una directiva de decisión **single** y ubicación en una solicitud, todos los elementos de la respuesta son únicos (de forma predeterminada). Dos elementos de decisión no pueden ser iguales en una sola solicitud.

* Para **varias** directivas o ubicaciones de decisión en una solicitud:

   * Si `allowDuplicateDecisionItems` se establece en `false`: todos los elementos de la respuesta son únicos (independientemente de para qué directiva de mensaje/decisión/ubicación se encuentre el elemento).

   * Si `allowDuplicateDecisionItems` se establece en `true` (predeterminado): los elementos de la respuesta se pueden duplicar (si varios mensajes/directivas de decisión/ubicaciones cumplen los requisitos para el mismo elemento de decisión para esa solicitud).

### Aplicación de la deduplicación en una solicitud {#deduplication-in-request}

De manera predeterminada, el indicador de deduplicación está establecido en `true`.

En una solicitud de Konductor, puede pasar el indicador de deduplicación si desea elementos únicos en la respuesta. En ese caso, establézcalo en `false`.

```
{
    "data": {
        "__adobe": {
            "ajo": {
                "allowDuplicateDecisionItems": false
            }
        }
    }
}
```

+++Solicitud de muestra de Decisioning

```
curl --location 'https://edge-int.adobedc.net/ee/v1/interact?configId=2f21d344-b69f-4a4f-98e8-000282fc9552' \
--header 'Content-Type: application/json' \
--data-raw '{
    "events": [
        {
            "query": {
                "personalization": {
                    "schemas": [
                        "https://ns.adobe.com/personalization/html-content-item"
                    ],
                    "surfaces": [
                        "https://www.adobe.com/san/placement/header",
                        "https://www.adobe.com/san/placement/footer"
                    ]
                }
            },
            "xdm": {
                "identityMap": {
                    "Email": [
                        {
                            "id": "cmk-exd-user01-deleted@adobe.com",
                            "primary": true
                        }
                    ]
                }
            },
            "data": {
                "__adobe":{
                    "ajo":{
                        "allowDuplicateDecisionItems": false
                    }
                }       
            }
        }
    ]
}'
```

+++

### Respuesta de deduplicación {#deduplication-response}

Supongamos que tiene la misma política de decisión con la colocación del encabezado y el pie de página en una sola solicitud.

* Decisioning devuelve dos propuestas.

* Si `itemId-X` es el único elemento de decisión que cumple los requisitos tanto para la política de decisión como para la combinación de ubicación:

   * Si `allowDuplicateDecisionItems` es `true` (predeterminado): `itemId-X` se devuelve para ambas propuestas en una sola respuesta.

   * Si `allowDuplicateDecisionItems` es `false`:

      * `itemId-X` se devolvió para la primera propuesta.

      * El elemento de decisión de reserva (también único) o un elemento de decisión vacío se pasan para la segunda propuesta.

+++Respuesta de muestra de toma de decisiones (`allowDuplicateDecisionItems` = `true`)

```
{
    "requestId": "b40170e9-7d31-4242-adcc-18063d6b1d9e",
    "handle": [
        {
            "payload": [
                {
                    "id": "d97f102c-bdae-4ed7-aff6-622d73e3db3d",
                    "scope": "https://www.adobe.com/san/placement/header",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiYmQxMDEzNGMtNjBkMS00NjZiLWEwYWMtOWQ0MzdmNmY5YTczIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI4ZmMzMDBjYy1iMTg5LTQ2MTUtYmY0OC03NjIwMjZkMjlmMWYiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvaGVhZGVyIl19fSwiaXRlbXMiOlt7ImlkIjoiZHBzOmM3MjI1YzNmYWMxNGUzMDBjYTNkZTlmY2I2ZDk4NTI0YjM5NTQ4YzFmYzFlYmQ2OToxOThkM2I5NDczZDRjYzQ3IiwiZXRhZyI6IjciLCJuYW1lIjoidGVzdFNhbi1tYW51YWxGYWxsYmFjay1vZmZlcjAxIiwic2NvcmUiOjExLjAsIml0ZW1TZWxlY3Rpb24iOnsic2VsZWN0aW9uRGV0YWlsIjp7InN0cmF0ZWd5SUQiOiJkcHM6c2VsZWN0aW9uLXN0cmF0ZWd5OjFhMGUzOTY4NzJlOWZiMWUiLCJzdHJhdGVneU5hbWUiOiJ0ZXN0U2FuLW1hbnVhbEZhbGxiYWNrLXN0cmF0ZWd5MTAwIiwic2VsZWN0aW9uVHlwZSI6InNlbGVjdGlvblN0cmF0ZWd5IiwidmVyc2lvbiI6Ijc0NUYzN0MzNUU0Qjc3NkUwQTQ5NDIxQkBBZG9iZU9yZzo2MzM5NzRmNC1lNTRlLTQyZjMtYjk3NC1mNGU1NGVjMmYzYmU6NThlNjE0MTItZTExOS00Mjg4LWJiZGEtYmQ1NGQ1MDgxNjVmIn0sInJhbmtpbmdEZXRhaWwiOnsic3RlcCI6InByaW9yaXR5In19LCJ0b2tlbiI6IitsckV1NWtHdnkrRXVYRFZ1K0VMWHcifV19XQ=="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/header"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                },
                {
                    "id": "e1de0998-44d6-435d-8974-1d5175a845ea",
                    "scope": "https://www.adobe.com/san/placement/footer",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiMGI4NTYxMzAtNDZiNy00OTQ1LTgwYTAtZjM2MGUzMjhlMjllIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI1NzViZDY3My0yMTQ1LTQ2MzAtYjQ1Yy1iNDAwMGUxMzI1NmMiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvZm9vdGVyIl19fSwiaXRlbXMiOltdfV0="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/footer"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                }
            ],
            "type": "personalization:decisions",
            "eventIndex": 0
        }
    ]
}
```

+++

+++Respuesta de muestra de toma de decisiones (`allowDuplicateDecisionItems` = `false`)

```
{
    "requestId": "b40170e9-7d31-4242-adcc-18063d6b1d9e",
    "handle": [
        {
            "payload": [
                {
                    "id": "d97f102c-bdae-4ed7-aff6-622d73e3db3d",
                    "scope": "https://www.adobe.com/san/placement/header",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiYmQxMDEzNGMtNjBkMS00NjZiLWEwYWMtOWQ0MzdmNmY5YTczIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI4ZmMzMDBjYy1iMTg5LTQ2MTUtYmY0OC03NjIwMjZkMjlmMWYiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvaGVhZGVyIl19fSwiaXRlbXMiOlt7ImlkIjoiZHBzOmM3MjI1YzNmYWMxNGUzMDBjYTNkZTlmY2I2ZDk4NTI0YjM5NTQ4YzFmYzFlYmQ2OToxOThkM2I5NDczZDRjYzQ3IiwiZXRhZyI6IjciLCJuYW1lIjoidGVzdFNhbi1tYW51YWxGYWxsYmFjay1vZmZlcjAxIiwic2NvcmUiOjExLjAsIml0ZW1TZWxlY3Rpb24iOnsic2VsZWN0aW9uRGV0YWlsIjp7InN0cmF0ZWd5SUQiOiJkcHM6c2VsZWN0aW9uLXN0cmF0ZWd5OjFhMGUzOTY4NzJlOWZiMWUiLCJzdHJhdGVneU5hbWUiOiJ0ZXN0U2FuLW1hbnVhbEZhbGxiYWNrLXN0cmF0ZWd5MTAwIiwic2VsZWN0aW9uVHlwZSI6InNlbGVjdGlvblN0cmF0ZWd5IiwidmVyc2lvbiI6Ijc0NUYzN0MzNUU0Qjc3NkUwQTQ5NDIxQkBBZG9iZU9yZzo2MzM5NzRmNC1lNTRlLTQyZjMtYjk3NC1mNGU1NGVjMmYzYmU6NThlNjE0MTItZTExOS00Mjg4LWJiZGEtYmQ1NGQ1MDgxNjVmIn0sInJhbmtpbmdEZXRhaWwiOnsic3RlcCI6InByaW9yaXR5In19LCJ0b2tlbiI6IitsckV1NWtHdnkrRXVYRFZ1K0VMWHcifV19XQ=="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/header"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                },
                {
                    "id": "e1de0998-44d6-435d-8974-1d5175a845ea",
                    "scope": "https://www.adobe.com/san/placement/footer",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiMGI4NTYxMzAtNDZiNy00OTQ1LTgwYTAtZjM2MGUzMjhlMjllIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI1NzViZDY3My0yMTQ1LTQ2MzAtYjQ1Yy1iNDAwMGUxMzI1NmMiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvZm9vdGVyIl19fSwiaXRlbXMiOltdfV0="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/footer"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "3913a28e-d33b-475b-9737-9f6de3940799",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": ""
                            }
                        }
                    ]
                }
            ],
            "type": "personalization:decisions",
            "eventIndex": 0
        }       
    ]
}
```

+++
