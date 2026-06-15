---
solution: Journey Optimizer
product: journey optimizer
title: Exportación de mensajes en Journey Optimizer
description: Obtenga información sobre cómo exportar mensajes
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: exportación, mensajes, HIPAA, correos electrónicos, SMS, configuración
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
TQID: https://experienceleague.adobe.com/4i6dFByqNizhrMeQrr32twEPVrg4Jz8J-rgA-sR70Ho
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 1431
ht-degree: 6%

---

# Exportar contenido del mensaje {#message-export}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a habilitar la exportación de mensajes en las configuraciones de canal de correo electrónico y SMS para escribir contenido de mensajes enviados en un conjunto de datos de Adobe Experience Platform y transferirlo a su propio almacenamiento.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Conservar y exportar el contenido enviado"
>abstract="Si selecciona esta opción, puede escribir el contenido del correo electrónico o los mensajes SMS enviados mediante esta configuración en un conjunto de datos de [!DNL Experience Platform]. Los registros se conservan durante 7 días naturales a partir de la ingesta, durante los cuales puede exportarlos a su propio almacenamiento."

>[!AVAILABILITY]
>
>Esta funcionalidad solo está disponible para el canal de correo electrónico y SMS, para organizaciones que han adquirido la oferta de complemento de Exportación de mensajes. Para obtener más información, contacte con su representante de Adobe.

**Message Export** le permite transferir el contenido de mensajes SMS y de correo electrónico enviados desde [!DNL Journey Optimizer] a su propio almacenamiento a través de [[!DNL Adobe Experience Platform] destinos](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/home){target="_blank"}, lo que le permite enviar datos de [!DNL Experience Platform] a extremos externos.

Con esta función, el contenido de los mensajes de correo electrónico y SMS enviados a través de [!DNL Journey Optimizer] que se han marcado para la exportación se escribe en el [!DNL Experience Platform] [conjunto de datos de exportación de mensajes de AJO](message-export-schema.md).

A continuación, los registros se conservan en el conjunto de datos durante siete días naturales a partir de la ingesta, durante los cuales puede exportarlos al sistema externo de su elección.

➡️: para obtener preguntas y respuestas comunes, consulte las [Preguntas frecuentes sobre la exportación de mensajes](#message-export-faq).

## Mecanismos de protección

* Esta función solo admite los canales **Correo electrónico** y **SMS**.
* Los registros del conjunto de datos de exportación de mensajes de AJO se conservan **durante siete días naturales** a partir de la ingesta.
* El relleno no es compatible con los mensajes enviados antes de habilitar la exportación de mensajes como se describe a continuación.

## Habilitar exportación de mensajes {#enable-message-export}

El proceso de incorporación de la función Exportación de mensajes consta de dos pasos:

1. [Configurar el flujo de datos de exportación](#set-up-export-dataflow) en [!DNL Experience Platform];
1. [Habilitar exportación de mensajes](#config-message-export) en la configuración de canal de [!DNL Journey Optimizer].

>[!WARNING]
>
>Solo aparecen los registros nuevos después de habilitar las exportaciones y enviar mensajes. No se admiten rellenos para el contenido antes de configurar el proceso de exportación y habilitar la opción Exportar mensaje.

### Configuración del flujo de datos de exportación {#set-up-export-dataflow}

Antes de poder exportar los datos, configure el proceso de exportación definiendo el destino [!DNL Experience Platform] y el flujo de exportación del conjunto de datos.

Para ver los pasos detallados, los destinos de nube admitidos, los permisos requeridos y más información, consulte [esta sección](../data/export-datasets.md#export-datasets).

>[!NOTE]
>
>Esta configuración debe configurarse para cada zona protegida.

1. Elija un Experience Platform [tipo de destino](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/destination-types){target="_blank"}. Hay disponible una lista de plataformas de destino disponibles que están listas para recibir datos en [esta página](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. En [!DNL Experience Platform], configure el destino definiendo credenciales, contenedor/contenedor, prefijo de ruta y opciones de seguridad. [Descubra cómo](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Cree un flujo de exportación de conjunto de datos con los siguientes datos:

   * Conjunto de datos Source: seleccione **Conjunto de datos de exportación de mensajes AJO**.
   * Formato del archivo: seleccione JSON o Parquet (elija uno basado en las herramientas de flujo descendente).
   * Programación: asegúrese de que se ejecuta dentro del período de retención de 7 días.

### Habilitar la exportación de mensajes en la configuración de canal {#config-message-export}

Para aplicar Message Export a sus campañas y recorridos, debe habilitar la opción específica en el nivel de configuración del canal. Siga los pasos a continuación.

1. En [!DNL Journey Optimizer], edite o cree el correo electrónico o SMS [configuración de canal](channel-surfaces.md#create-channel-surface) deseado.

1. Seleccione la opción **[!UICONTROL Habilitar exportación de mensajes]**.

   ![](assets/config-message-export.png)

1. Guarde los cambios y envíe la configuración de canal.

Una vez que haya enviado mensajes a través de campañas o recorridos usando esta configuración de canal, los mensajes de correo electrónico y SMS se escriben en el **conjunto de datos de exportación de mensajes de AJO**. A continuación, puede [acceder a los registros](#access-exported-data) del conjunto de datos y exportarlos al destino de almacenamiento seleccionado en función del flujo de datos de exportación que haya definido.

>[!NOTE]
>
>Al deshabilitar la opción **[!UICONTROL Habilitar exportación de mensajes]**, se detienen los nuevos registros para que esta configuración de canal no se ingrese en el conjunto de datos. Los registros existentes se conservarán hasta que caduque la retención.

## Acceso a datos de mensajes exportados {#access-exported-data}

Una vez enviados los mensajes mediante una configuración de canal con la opción Message Export habilitada, podrá obtener acceso a los datos exportados y revisarlos en el **conjunto de datos de exportación de mensajes de AJO**.

Para ver los datos de mensajes exportados:

1. En [!DNL Journey Optimizer], vaya a **[!UICONTROL Administración de datos]** > **[!UICONTROL Conjuntos de datos]** en el panel de navegación izquierdo. [Más información sobre los conjuntos de datos](../data/get-started-datasets.md)

1. Asegúrese de mostrar los conjuntos de datos generados por el sistema.

1. Seleccione el **conjunto de datos de exportación de mensajes de AJO** de la lista.

   ![](assets/datasets-list.png)

1. En la página de detalles del conjunto de datos, haga clic en **[!UICONTROL Vista previa del conjunto de datos]** para ver los registros más recientes.

   ![](assets/ajo-message-export-dataset.png)

El conjunto de datos contiene información completa para cada mensaje enviado a través de la configuración de canal con Exportación de mensajes habilitada, que incluye: línea de asunto, cuerpo del mensaje, dirección de correo electrónico del destinatario o número de teléfono, dirección del remitente o número de teléfono, fecha y hora de envío, datos de personalización, etc.

➡️ Para obtener una vista completa de la estructura del conjunto de datos y de todos los campos disponibles, consulte el [esquema de exportación de mensajes de AJO](message-export-schema.md).

Todos los registros del conjunto de datos se conservarán durante **siete días naturales** a partir de la ingesta. Durante este período de retención, puede acceder a los datos para realizar auditorías de conformidad o consultas legales, o exportarlos a su propio sistema de almacenamiento a través del destino configurado de Experience Platform.

## Ejemplo de JSON exportado {#sample-exported-json}

Los ejemplos siguientes muestran la forma general de los registros escritos en el conjunto de datos de exportación de mensajes de AJO para SMS y correo electrónico. Los valores como identificadores, referencias de esquema, marcas de tiempo y contenido son ilustrativos; las exportaciones reflejan su zona protegida, esquema y mensajes enviados.

Expanda cada sección para ver la muestra completa de JSON.

+++ Ejemplo de exportación de SMS

```json
{
  "header": {
    "msgId": "f06d2a6d-65c3-472b-9ca7-cc4224af2df4",
    "xactionId": "9ccd6e76-9ee5-4a12-bff3-fea240228121",
    "msgType": "xdmEntityCreate",
    "imsOrgId": "906E3A095DC834230A495FD6@AdobeOrg",
    "sandboxId": "db3adc95-dcf6-49c3-badc-95dcf639c345",
    "sandboxName": "ajo-e2e",
    "createdAt": 1773591102107,
    "datasetId": "689653509dd3432b92f6323f",
    "schemaRef": {
      "id": "https://ns.adobe.com/aemonacpprodcampaign/schemas/64cb5d9d26c2aae6b08bdc9b7882deb90202439ec53836e7",
      "contentType": "application/vnd.adobe.xed-full+json;version=1"
    },
    "source": {
      "name": "message-execution-service"
    },
    "originalTimestamp": 1773591102107,
    "tags": [
      "ups:segmentation=false"
    ]
  },
  "body": {
    "xdmEntity": {
      "_experience": {
        "customerJourneyManagement": {
          "messageExecution": {
            "messageExecutionID": "CSM-09561055",
            "messageID": "15fe77c8-ab73-49e4-abbb-c25b859162ff-0",
            "messageType": "marketing",
            "campaignID": "5638ce57-5264-4a96-995f-5ae34eddafd7",
            "campaignVersionID": "f9019155-3d6a-44a1-9b6f-5f9cd49e7cf5",
            "campaignActionID": "dfa7f59f-477c-42ec-9db2-831d294b5779",
            "batchInstanceID": "5e23a286fb72411f1cdf1443a81ad2eb",
            "messagePublicationID": "15fe77c8-ab73-49e4-abbb-c25b859162ff",
            "audience": {
              "id": "4c339f63-b66e-4e72-8d56-db624b5277f2",
              "type": "targeted"
            }
          },
          "messageProfile": {
            "channel": {
              "_id": "https://ns.adobe.com/xdm/channels/sms",
              "_type": "https://ns.adobe.com/xdm/channel-types/sms"
            },
            "messageProfileID": "7ff5aefb-7583-38c4-8c32-b63cced94aa7",
            "variant": "5c1092da-5ba2-4bcc-b591-713ee7999f7d"
          },
          "messageRenderedContent": {
            "smsContent": {
              "message": "AJO Campaigns - Prod - E2E Test Text VA7"
            }
          },
          "messageDeliveryMetadata": {
            "smsMetadata": {
              "recipient": {
                "number": "+19256260201"
              },
              "sender": {
                "numbers": [
                  "12345678"
                ]
              }
            }
          }
        }
      },
      "identityMap": {
        "email": [
          {
            "id": "rlyajoqa+messageExport1@adobe.com",
            "primary": true
          }
        ]
      },
      "_id": "b0001846-cafa-379a-be96-1d8ee973e047",
      "timestamp": "2026-03-15T16:11:42.184Z"
    }
  }
}
```

+++

+++ Ejemplo de exportación de correo electrónico

```json
{
  "header": {
    "msgId": "1e64d2c4-7887-4f80-8b28-5c20d3da8baf",
    "xactionId": "5yfSV2Gs7VJM5TKo1uEkbiDd4iuakgzQ",
    "msgType": "xdmEntityCreate",
    "imsOrgId": "745F37C35E4B776E0A49421B@AdobeOrg",
    "sandboxId": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "sandboxName": "prod",
    "createdAt": 1754489661211,
    "datasetId": "68912b8881572a2b267380c1",
    "schemaRef": {
      "id": "https://ns.adobe.com/cjmstage/schemas/1684477c0160376b8bb6975a80b5e5bd384696329faa1c42",
      "contentType": "application/vnd.adobe.xed-full+json;version=1"
    },
    "source": {
      "name": "message-execution-service"
    },
    "originalTimestamp": 1754489659000,
    "tags": [
      "ups:segmentation=false"
    ]
  },
  "body": {
    "xdmEntity": {
      "_experience": {
        "customerJourneyManagement": {
          "messageExecution": {
            "messageExecutionID": "HUMA-62208933",
            "messageID": "d0d02f68-afea-42fc-b898-6819cee643e6-0",
            "messageType": "transactional",
            "campaignID": "ce2331c2-c259-47ff-a1dd-f6d1eae08801",
            "campaignVersionID": "4272bb9f-e154-44e9-89f1-6548c77d1455",
            "batchInstanceID": "03587190-72cf-11f0-938b-31e7c9f96d89",
            "messagePublicationID": "d0d02f68-afea-42fc-b898-6819cee643e6",
            "audience": {
              "type": "all"
            }
          },
          "messageProfile": {
            "channel": {
              "_id": "https://ns.adobe.com/xdm/channels/email",
              "_type": "https://ns.adobe.com/xdm/channel-types/email"
            },
            "messageProfileID": "5yfSV2Gs7VJM5TKo1uEkbiDd4iuakgzQ",
            "variant": "11cc5796-8017-4738-aa66-ca5db967dfcc"
          },
          "messageRenderedContent": {
            "emailContent": {
              "subject": "test",
              "html": "xxx"
            }
          },
          "messageDeliveryMetadata": {
            "emailMetadata": {
              "recipient": {
                "email": "himanshig@adobe.com"
              },
              "sender": {
                "email": "cjm-team@e2e-personalisation.test.cjmadobe.com",
                "name": "CJM team",
                "replyToEmail": "replyto@marketing.adobecjm.com",
                "replyToName": "replyto",
                "errorEmail": "replyto@e2e-personalisation.test.cjmadobe.com"
              }
            }
          }
        }
      },
      "identityMap": {
        "email": [
          {
            "id": "chijain@adobe.com",
            "primary": true
          }
        ]
      },
      "_id": "ea48ce1b-80c9-3c6a-b05f-d1c998989e02",
      "timestamp": "2025-08-06T14:14:22.814Z"
    }
  }
}
```

+++

## Preguntas frecuentes sobre exportación de mensajes {#message-export-faq}

+++ ¿Qué es la exportación de mensajes?

La exportación de mensajes permite a los clientes exportar mensajes completamente procesados (correo electrónico y SMS) enviados a los usuarios finales. Los datos exportados se pueden enviar a destinos externos utilizando las funciones de exportación estándar de [!DNL Adobe Experience Platform] (AEP) y se pueden utilizar para fines como archivado, revisión de conformidad, análisis o integraciones posteriores.

+++

+++ ¿Qué canales son compatibles?

La exportación de mensajes admite:

* Correo electrónico
* SMS

+++

+++ ¿Qué datos genera la exportación de mensajes?

Message Export crea un conjunto de datos generado por el sistema en [!DNL Adobe Experience Platform] que contiene una instantánea del mensaje en el momento del envío. Este conjunto de datos se puede exportar a destinos admitidos (por ejemplo, almacenamiento en la nube o sistemas de terceros).

Message Export está diseñado como un mecanismo de habilitación para que los clientes muevan los datos de los mensajes fuera de los sistemas de Adobe; los clientes son responsables de transformar, almacenar y administrar los datos en sus propias soluciones de archivado o cumplimiento normativo.

+++

+++ ¿Message Export captura mensajes totalmente personalizados?

Sí. Message Export captura el mensaje completamente procesado que se envió a cada destinatario, incluida la personalización y el contenido dinámico tal y como se representa en el momento del envío.

+++

+++ ¿Es posible utilizar la exportación de mensajes para reproducir el mensaje original?

Sí. La HTML exportada se puede utilizar para reproducir el mensaje enviado original en un explorador.

Sin embargo, la reproducción depende de la disponibilidad de recursos alojados externamente (como imágenes). Message Export no incrusta los archivos multimedia directamente en la exportación.

+++

+++ ¿Se incluyen imágenes y medios en la exportación?

La exportación de mensajes incluye contenido de HTML con referencias (URL) a imágenes y otros medios. Los recursos de medios no están incrustados en la exportación.

Si la URL de una imagen o un recurso deja de ser válida, restringida o no se publica después del tiempo de envío, la exportación de mensajes no podrá recuperar ese recurso.

+++

+++ ¿Cómo se gestionan los vínculos en la exportación de mensajes?

Los mensajes exportados contienen vínculos rastreados cifrados, de acuerdo con la forma en que se gestionan los vínculos en el momento del envío. Estos vínculos cifrados se conservan en la exportación y se pueden resolver según lo diseñado por la plataforma.

+++

+++ ¿Cómo se gestionan los datos PII y de personalización?

Los datos se almacenan exactamente como aparecen en el mensaje procesado:

* Los valores de Personalization representados en el mensaje (por ejemplo, el nombre) aparecen como texto.
* Los elementos cifrados (como los vínculos rastreados) permanecen cifrados.
* Message Export no convierte automáticamente en anónimo ni redacta el contenido de los mensajes procesados.

+++

+++ ¿Cuál es el período de retención de datos de exportación de mensajes?

Los datos de exportación de mensajes siguen un período de retención de 7 días en [!DNL Adobe Experience Platform].

Los clientes deben exportar los datos dentro de este periodo y almacenarlos en sus propios sistemas si se requiere una retención más larga.

+++

+++ ¿Pueden los clientes probar Message Export antes de comprar?

No hay ninguna opción de prueba o &quot;try-before-you-buy&quot; para Message Export.

Los clientes pueden validar sus sistemas descendentes mediante archivos de exportación de ejemplo, ya que Message Export depende de la funcionalidad de destino y del conjunto de datos estándar de AEP.

+++

+++ ¿Está disponible el esquema de exportación de mensajes antes de la compra?

No. El conjunto de datos y el esquema de exportación de mensajes solo estarán disponibles en el producto una vez que se haya adquirido y habilitado el complemento Exportación de mensajes.

+++

+++ ¿Es la exportación de mensajes una solución completa de archivado o conformidad?

No. La exportación de mensajes es un activador, no un producto completo de archivado o conformidad.

Se espera que los clientes:

* Exportación de datos de mensajes desde Adobe
* Transforme o enriquezca según sea necesario
* Almacenar y administrar los datos en sus propios sistemas de archivado o cumplimiento normativo

+++

+++ ¿Cuáles son los casos de uso más comunes?

Los clientes suelen utilizar la exportación de mensajes para:

* Revisión regulatoria o de cumplimiento
* Archivado de mensajes
* Integración con sistemas de terceros
* Flujos de trabajo de soporte o auditoría interna
* Analytics más allá de las aplicaciones Adobe

+++

+++ Qué no hace la exportación de mensajes

La exportación de mensajes no:

* Incrustar imágenes externas o recursos de medios
* Proporcionar retención de datos ilimitada o a largo plazo en sistemas Adobe
* Ofrecer un entorno de prueba
* Archivar mensajes automáticamente fuera de Adobe

+++

