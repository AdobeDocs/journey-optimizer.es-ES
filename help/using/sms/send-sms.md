---
solution: Journey Optimizer
product: journey optimizer
title: Previsualizar y probar el mensaje SMS
description: Obtenga información sobre cómo previsualizar y probar el mensaje SMS en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 12%

---

# Previsualizar y probar el mensaje SMS {#send-sms}

## Previsualización de SMS {#preview-sms}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este contenido en el mensaje mediante los datos de perfil de prueba.

1. Haga clic en **[!UICONTROL Simular contenido]**.

1. Haga clic en **[!UICONTROL Administrar perfiles de prueba]** para agregar un perfil de prueba.

1. Busque el perfil de prueba con la variable **[!UICONTROL Área de nombres de identidad]** y **[!UICONTROL Valor de identidad]** campos. A continuación, haga clic en **[!UICONTROL Añadir perfil]**.

   ![](assets/sms_preview_3.png)

1. Una vez que haya seleccionado el perfil de prueba, puede cerrar el **[!UICONTROL Añadir perfil de prueba]** ventana.

1. En el **Vista previa y prueba** , los datos del perfil de prueba se añaden al contenido del mensaje.

   ![](assets/sms_preview_2.png)


## Validar el SMS{#sms-validate}

Debe comprobar las alertas en la sección superior del editor. Algunas son simples advertencias, pero otras pueden impedir que envíe el mensaje. Pueden producirse dos tipos de alertas: advertencias y errores.

* **Advertencias** consulte recomendaciones y prácticas recomendadas. Por ejemplo, se muestra un mensaje de advertencia si el mensaje SMS está vacío.

* **Errores** evite probar o activar el recorrido, o publicar la campaña, siempre que no se resuelvan. Por ejemplo, un mensaje de error le advierte cuando falta la línea de asunto.

![](assets/sms-alert-button.png)

>[!NOTE]
>
> Para mejorar la capacidad de envío, utilice los números de teléfono en los formatos admitidos por el proveedor. Por ejemplo, Twilio y Sinch solo admiten números de teléfono en formato E.164.

## Envíe su SMS{#sms-send}

Cuando el mensaje SMS esté listo, complete la configuración de su [recorrido](../building-journeys/journey-gs.md) o [campaign](../campaigns/create-campaign.md) para enviarlo.

**Temas relacionados**

* [Configuración del canal de SMS](sms-configuration.md)
* [Informe SMS](../reports/journey-global-report.md#sms-global)
* [Creación de un mensaje SMS](create-sms.md)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
