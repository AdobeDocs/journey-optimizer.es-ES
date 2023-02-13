---
solution: Journey Optimizer
product: journey optimizer
title: Previsualizar y probar la notificación push
description: Obtenga información sobre cómo previsualizar y probar la notificación push en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 5%

---

# Previsualizar y probar la notificación push {#send-push}

## Vista previa de la notificación push {#preview-push}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este contenido en el mensaje mediante los datos de perfil de prueba.

1. Haga clic en **[!UICONTROL Simular contenido]**.

1. Haga clic en **[!UICONTROL Administrar perfiles de prueba]** para agregar un perfil de prueba.

1. Busque el perfil de prueba con la variable **[!UICONTROL Área de nombres de identidad]** y **[!UICONTROL Valor de identidad]** campos. A continuación, haga clic en **[!UICONTROL Añadir perfil]**.

   ![](assets/push_preview_1.png)

1. Una vez que haya seleccionado el perfil de prueba, puede cerrar el **[!UICONTROL Añadir perfil de prueba]** ventana.

1. En el **Vista previa y prueba** , los datos del perfil de prueba se añaden al contenido del mensaje.

   Seleccione el tipo de dispositivo para previsualizar el contenido: **[!UICONTROL iOS]** o **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## Validación de la notificación push {#push-validate}


Debe comprobar las alertas en la sección superior del editor. Algunas son simples advertencias, pero otras pueden impedir que envíe el mensaje. Pueden producirse dos tipos de alertas: advertencias y errores.

* **Advertencias** consulte recomendaciones y prácticas recomendadas.

* **Errores** evite probar o activar el recorrido siempre que no se resuelvan, como:

   * **[!UICONTROL La versión push del mensaje está vacía]**: este error se muestra cuando falta el cuerpo o el título de la notificación push. Aprenda a definir el contenido de las notificaciones push en [esta sección](create-push.md).

   * **[!UICONTROL La superficie no existe]**: no puede utilizar el mensaje si la superficie seleccionada se elimina después de la creación del mensaje. Si se produce este error, seleccione otra superficie en el mensaje **[!UICONTROL Propiedades]**. Obtenga más información sobre las superficies de canal en [esta sección](../configuration/channel-surfaces.md).

   * **[!UICONTROL La carga útil de iOS/Android push ha superado el límite de 4 KB]**: el tamaño de la notificación push no puede superar los 4 KB. Para respetar este límite, intente reducir el uso de imágenes o emojis. Aprenda a administrar el contenido de las notificaciones push en [esta sección](../push/create-push.md).

   ![](assets/push_alert.png)


>[!NOTE]
>
> Para mejorar la capacidad de envío, siempre debe utilizar los números de teléfono en los formatos admitidos por el proveedor. Por ejemplo, Twilio y Sinch solo admiten números de teléfono en formato E.164.

## Enviar la notificación push{#push-send}

Cuando el mensaje push esté listo, complete la configuración de su [recorrido](../building-journeys/journey-gs.md) o [campaign](../campaigns/create-campaign.md) para enviarlo.

**Temas relacionados**

* [Configurar el canal push](push-configuration.md)
* [Informe de notificaciones push](../reports/journey-global-report.md#push-global)
* [Crear una notificación push](create-push.md)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
* [Añadir un mensaje en una campaña](../campaigns/create-campaign.md)

