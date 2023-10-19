---
solution: Journey Optimizer
product: journey optimizer
title: Comprobación y prueba del mensaje SMS
description: Obtenga información sobre cómo comprobar y enviar su mensaje SMS en Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 6%

---

# Compruebe y envíe su mensaje SMS {#send-sms}

## Previsualización de SMS {#preview-sms}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizar su contenido. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje con los datos del perfil de prueba.

Para ello, haga clic en **[!UICONTROL Simular contenido]** a continuación, añada un perfil de prueba para comprobar el mensaje con los datos del perfil de prueba.

![](assets/sms_preview_2.png)

Encontrará información detallada sobre cómo seleccionar perfiles de prueba y previsualizar el contenido en el [Gestión de contenido](../content-management/preview-test.md) sección.

## Validar el SMS{#sms-validate}

Debe comprobar las alertas en la sección superior del editor. Algunas son simples advertencias, pero otras pueden impedir que envíe el mensaje. Pueden producirse dos tipos de alertas: advertencias y errores.

* **Advertencias** consulte recomendaciones y prácticas recomendadas. Por ejemplo, se muestra un mensaje de advertencia si el mensaje SMS está vacío.

* **Errores** evite probar o activar el recorrido, o publicar la campaña, siempre que no se resuelvan. Por ejemplo, un mensaje de error le advierte cuando falta la línea de asunto.

![](assets/sms-alert-button.png)

>[!NOTE]
>
> Para mejorar la capacidad de envío, utilice los números de teléfono en los formatos admitidos por el proveedor. Por ejemplo, Twilio y Sinch solo admiten números de teléfono en formato E.164.

## Envío de SMS{#sms-send}

Cuando el mensaje SMS esté listo, complete la configuración de su [recorrido](../building-journeys/journey-gs.md) o [campaña](../campaigns/create-campaign.md) para enviarlo.

**Temas relacionados**

* [Configuración del canal de SMS](sms-configuration.md)
* [Informe SMS](../reports/journey-global-report.md#sms-global)
* [Creación de un mensaje SMS](create-sms.md)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
