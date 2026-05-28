---
solution: Journey Optimizer
product: journey optimizer
title: Comprueba y prueba tus mensajes de WhatsApp
description: Aprenda a comprobar y enviar sus mensajes de WhatsApp en Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 31acb095-de90-495f-8e8c-43a78dedfa06
TQID: https://experienceleague.adobe.com/u2OevVu38fPdytpuTmHeSdEx3Wvpih7ifk-j88rhDFI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: b8df23d2-98a2-4406-86cc-2babe8728d36
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 2%

---

# Comprobación y envío de los mensajes de WhatsApp {#send-whatsapp}

## Previsualiza tu mensaje de WhatsApp {#preview-whatsapp}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente para previsualizar su contenido. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje.

Para ello, haga clic en **[!UICONTROL Simular contenido]** y compruebe su mensaje con los datos del perfil de prueba.

Encontrará información detallada sobre cómo obtener una vista previa y probar contenido en la sección [Administración de contenido](../content-management/preview-test.md).

## Validación del contenido {#whatsapp-validate}

Debe comprobar las alertas en la sección superior del editor. Algunas son simples advertencias, pero otras pueden impedir que envíe el mensaje. Pueden producirse dos tipos de alertas: advertencias y errores.

* **Advertencias** se refieren a recomendaciones y prácticas recomendadas. Por ejemplo, se muestra un mensaje de advertencia si el mensaje de texto está vacío.

* **Los errores** le impiden probar o activar la recorrido o publicar la campaña, siempre y cuando no se resuelvan. Por ejemplo, un mensaje de error le advierte cuando falta la línea de asunto.

## Enviar tus mensajes de WhatsApp {#whatsapp-send}

>[!IMPORTANT]
>
> Si la campaña está sujeta a una directiva de aprobación, debe solicitar la aprobación para poder enviar los mensajes de texto. [Más información](../test-approve/gs-approval.md)

Cuando el mensaje de WhatsApp esté listo, completa la configuración de tu [recorrido](../building-journeys/publish-journey.md) o [campaña](../campaigns/review-activate-campaign.md) para enviarlo.

## Analizar interacciones de WhatsApp {#whatsapp-channel-context}

Journey Optimizer captura datos de interacción adicionales devueltos por el canal WhatsApp y los almacena en el **Conjunto de datos de eventos de experiencia de seguimiento de correo electrónico - Informes** en el grupo de campos `whatsAppChannelContext`. Utilice estos campos para generar [audiencias](../audience/about-audiences.md), ejecutar [consultas](../data/get-started-queries.md) y analizar la participación de WhatsApp. [Más información sobre los conjuntos de datos del sistema](../data/get-started-datasets.md#system-datasets).

Se capturan los campos siguientes:

| Campo | Descripción |
|-|-|
| `messageType` | Tipo de mensaje de WhatsApp (por ejemplo, `templateBased`, `response`). |
| `inboundMessage` | Contenido de respuesta entrante (por ejemplo, `stop`, `start`, `subscribe`). |
| `inboundNumber` | ID del remitente donde se recibió el mensaje entrante. |
| `channelType` | Categoría de canal (`Utility`, `Marketing` o `Promotional`). |
| `profileNumber` | Número de teléfono desde el que se recibió el mensaje entrante. |
| `origTimestamp` | Marca de tiempo original de Meta/WhatsApp. |
| `status` | Estado de envío, incluidos los comentarios estandarizados del proveedor (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` o `unknown`) y el mensaje de estado del proveedor sin procesar. |
| `reactionEvent` | Contenido de la respuesta del usuario: emoji para reacciones o texto del mensaje para respuestas a un mensaje específico. |
| `reactionMessageID` | ID del mensaje original al que se responde. |
| `reactionActionName` | Tipo de acción de respuesta (`react`, `unreact` o `reply`). |
| `interactiveSelectedTitle` | Título seleccionado por el usuario de un mensaje interactivo de WhatsApp. |
| `interactiveType` | Tipo de mensaje interactivo (`list reply`, `button reply` o `button`). |
| `interactiveSelectedDescription` | Descripción de la opción interactiva de WhatsApp seleccionada. |
| `interactiveSelectedID` | ID de la opción seleccionada de WhatsApp. |

Para consultar este conjunto de datos, utilice la tabla `ajo_email_tracking_experience_event_dataset` en el servicio de consultas. Para ver patrones de consulta y casos de uso relacionados, vea [Ejemplos de consultas de conjuntos de datos](../data/datasets-query-examples.md).
