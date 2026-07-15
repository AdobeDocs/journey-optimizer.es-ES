---
title: Ejemplos de Personalization de plantilla
description: Ejemplos de Journey Optimizer Personalization
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
TQID: https://experienceleague.adobe.com/fZtkkz9pvdZ3G7ojmHlNhasxawVbXmBHX-uznq6hseY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 1%

---

# Correo electrónico de prescripciones del plan de salud {#plan-prescription}

>[!BEGINSHADEBOX]

**En esta página:** Siga un caso de uso de personalización que se repite en matrices de perfiles anidadas con reglas condicionales para crear una lista de correo electrónico de plan de mantenimiento con recetas listas para ser recogidas o recuperadas.

>[!ENDSHADEBOX]

Un perfil contiene planes de salud y cada plan incluye recetas. Las recetas tienen varios estados, como &quot;listo&quot;, &quot;recordado&quot; o &quot;recogido&quot;.

En este caso de uso, queremos enviar un solo correo electrónico a cada perfil, incluidas todas las prescripciones que estén listas para ser recogidas o retiradas. Haga clic en cada pestaña a continuación para obtener más información sobre la sintaxis que se debe utilizar para implementar este caso de uso.

>[!BEGINTABS]

>[!TAB Mensaje procesado]

<p>Hola John Doe,</p>
<p>Estas son las recetas que están listas para ser recogidas o que han sido retiradas:</p>

**Plan de salud A**

<ul>

<li>
      <strong>Id. de prescripción:</strong> pres1<br>
      <strong>Nombre:</strong> Medicamento A<br>
      <strong>Estado:</strong> listo
   </li>

<li>
      <strong>Id. de prescripción:</strong> pres2<br>
      <strong>Nombre:</strong> Medicamento B<br>
      Recuperación de <strong>estado:</strong>
   </li>

</ul>

**Plan de salud B**

<ul>

<li>
      <strong>Id. de prescripción:</strong> pres4<br>
      <strong>Nombre:</strong> ID de medicamento<br>
      <strong>Estado:</strong> listo
   </li>

</ul>

>[!TAB Plantilla de HTML]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB Datos de perfil]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]

## Referencia rápida {#quick-reference}

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

>[!BEGINTABS]

>[!TAB Información general]

**TL;DR**

Esta página muestra un caso de uso de personalización completo: iteración en matrices de perfiles anidadas (planes de mantenimiento que contienen recetas) con filtrado condicional para mostrar solo las recetas en estados &quot;listas&quot; o &quot;recuperadas&quot; en un mensaje de correo electrónico.

**Intenciones**

* Ver un ejemplo de salida procesado de un correo electrónico personalizado del plan de mantenimiento
* Comprenda la plantilla de HTML utilizando bloques anidados `{{#each}}` y `{%#if%}` para la iteración de matriz condicional
* Comprenda la estructura de datos de perfil necesaria: una matriz `plans` en la que cada plan contiene una matriz `prescriptions` con `state` campos

>[!TAB Glosario]

* **Iteración anidada**: se usan bucles `{{#each}}` dentro de otros bucles `{{#each}}` para atravesar estructuras de matrices de varios niveles en datos de perfil (por ejemplo, planes → prescripciones).
* **Estado de prescripción**: un campo en cada objeto de prescripción que indica su estado de ciclo de vida en este caso de uso; los valores utilizados son &quot;listo&quot;, &quot;recuperado&quot; y &quot;recogido&quot;. *(específico de caso de uso)*
* **`{%#if%}`/`{%/if%}`**: sintaxis de bloque condicional utilizada dentro de las plantillas de mensajes para filtrar los elementos de la matriz durante la iteración (distinta de la sintaxis de Handlebars de doble curvatura `{{#if}}`).

>[!TAB Terminología]

* **Nombre canónico:** iteración de matriz anidada — variantes: bucles anidados, cada uno anidado, iteración de varios niveles
* **No confunda:** `{{#each}}` / `{{/each}}` (sintaxis de iteración de Handlebars, llaves dobles) ≠ `{%#if%}` / `{%/if%}` (sintaxis condicional, llaves de porcentaje): ambos se utilizan juntos en esta plantilla
* **No confunda:** &quot;listo&quot; (receta disponible para recoger) ≠ &quot;recuperar&quot; (receta recuperada) ≠ &quot;recogido&quot; (receta ya recopilada; excluido de la salida por el filtro condicional)

>[!TAB Preguntas más frecuentes]

**Q: ¿Qué estados de prescripción se incluyen en la salida de correo electrónico?**

Solo se muestran las recetas con el estado &quot;listo&quot; o &quot;retirado&quot;. Las recetas con el estado &quot;recogidas&quot; se excluyen mediante el filtro condicional `{%#if prescription.state = "ready" or prescription.state = "recall"%}`.

**Q: ¿Qué estructura de datos de perfil se requiere para este caso de uso?**

Un perfil con una matriz `plans`, donde cada objeto de plan contiene una matriz `prescriptions`. Cada objeto de prescripción debe tener los campos `prescription_id`, `name` y `state`.

**Q: ¿Cómo se iteran los planes y las recetas en la plantilla?**

El bucle `{{#each profile.plans as |plan|}}` externo se repite en cada plan de mantenimiento. Dentro de él, `{{#each plan.prescriptions as |prescription|}}` se repite en las prescripciones de cada plan, y un bloque condicional se filtra únicamente a los estados &quot;listo&quot; o &quot;revocar&quot;.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 4b68d597 -->
