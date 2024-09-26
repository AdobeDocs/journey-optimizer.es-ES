---
solution: Journey Optimizer
product: journey optimizer
title: Comprobación y prueba de los mensajes de texto
description: Obtenga información sobre cómo comprobar y enviar mensajes de texto en Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: dd4173698d7034173b7ae9f44afec397d62a6f78
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 3%

---

# Compruebe y envíe su mensaje de texto (SMS/MMS){#send-sms}

## Previsualización del mensaje de texto {#preview-sms}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizar su contenido. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje con los datos del perfil de prueba.

Para ello, haga clic en **[!UICONTROL Simular contenido]** y añada un perfil de prueba para comprobar el mensaje con los datos del perfil de prueba.

![](assets/sms_preview_2.png)

Encontrará información detallada sobre cómo seleccionar perfiles de prueba y obtener una vista previa del contenido en la sección [Administración de contenido](../content-management/preview-test.md).

## Validación del contenido {#sms-validate}

Debe comprobar las alertas en la sección superior del editor. Algunas son simples advertencias, pero otras pueden impedir que envíe el mensaje. Pueden producirse dos tipos de alertas: advertencias y errores.

![](assets/sms-alert-button.png)

* **Advertencias** se refieren a recomendaciones y prácticas recomendadas. Por ejemplo, se muestra un mensaje de advertencia si el mensaje de texto está vacío.

* **Los errores** le impiden probar o activar la recorrido o publicar la campaña, siempre y cuando no se resuelvan. Por ejemplo, un mensaje de error le advierte cuando falta la línea de asunto.


>[!NOTE]
>
> Para mejorar la capacidad de envío, utilice los números de teléfono en los formatos admitidos por el proveedor. Por ejemplo, Twilio y Sinch solo admiten números de teléfono en formato E.164.

## Envíe sus mensajes de texto {#sms-send}

>[!IMPORTANT]
>
>A partir de la versión de septiembre, una nueva experiencia de activación de recorrido y campaña le permite administrar todo el proceso de aprobación, lo que garantiza que las campañas y los recorridos sean revisados y aprobados a fondo por las partes interesadas adecuadas antes de lanzarse. Esta función está disponible con disponibilidad limitada. [Más información](../test-approve/gs-approval.md)

Cuando el mensaje de texto esté listo, completa la configuración de tu [recorrido](../building-journeys/journey-gs.md) o [campaña](../campaigns/create-campaign.md) para enviarlo.

**Temas relacionados**

* [Configuración del canal de SMS](sms-configuration.md)
* [Informes de SMS/MMS](../reports/journey-global-report.md#sms-global)
* [Creación de un mensaje de texto](create-sms.md)
* [Añadir un mensaje en un recorrido](../building-journeys/journeys-message.md)
