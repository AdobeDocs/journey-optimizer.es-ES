---
title: Creación de una notificación en la aplicación
description: Obtenga información sobre cómo crear un mensaje en la aplicación en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Crear un mensaje en la aplicación {#create-in-app}

## Creación de una campaña y un mensaje en la aplicación{#create-in-app-in-a-campaign}

Para crear un mensaje en la aplicación, siga los pasos a continuación:

1. Acceda a la **[!UICONTROL Campaigns]** a continuación, haga clic en **[!UICONTROL Create campaign]**.

1. En el **[!UICONTROL Properties]** , especifique cuándo desea ejecutar la campaña.

1. En el **[!UICONTROL Actions]** , seleccione **[!UICONTROL In-app message]** y **[!UICONTROL App surface]** previamente configurado para el mensaje en la aplicación. A continuación, haga clic en **[!UICONTROL Create]**.

   [Obtenga más información sobre la configuración en la aplicación](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. En el **[!UICONTROL Properties]** , edite la **[!UICONTROL Title]** y **[!UICONTROL Description]**.

1. Para asignar etiquetas de uso de datos principales o personalizadas a la página de aterrizaje, seleccione **[!UICONTROL Manage access]**. [Más información](../administration/object-based-access.md).

1. Haga clic en el **[!UICONTROL Select audience]** para definir la audiencia a la que se dirigirá desde la lista de segmentos disponibles de Adobe Experience Platform. [Más información](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. En el **[!UICONTROL Identity namespace]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información](../event/about-creating.md#select-the-namespace).

1. Elija la frecuencia del activador cuando el mensaje en la aplicación esté activo:

   * **[!UICONTROL Show every time]**: Mostrar siempre el mensaje cuando los eventos seleccionados en la variable **[!UICONTROL Mobile app trigger]** se produce.
   * **[!UICONTROL Show once]**: Mostrar este mensaje solo la primera vez que se seleccionan los eventos en la variable **[!UICONTROL Mobile app trigger]** se produce.
   * **[!UICONTROL Show until click through]**: Mostrar este mensaje cuando los eventos seleccionados en la variable **[!UICONTROL Mobile app trigger]** se produce hasta que el SDK envía un evento de interacción con una acción de &quot;clic&quot;.

1. En el **[!UICONTROL Mobile app trigger]** , elija los eventos y criterios que activarán el mensaje:

   1. En el menú desplegable de la izquierda, seleccione el evento necesario para activar el mensaje.
   1. En la lista desplegable derecha, seleccione la validación requerida en el evento seleccionado.
   1. Haga clic en el **[!UICONTROL Add]** si desea que el activador considere varios eventos o criterios. A continuación, repita los pasos anteriores.
   1. Seleccione cómo están vinculados los eventos, por ejemplo, elija **[!UICONTROL And]** si desea **both** activa como true para que un mensaje se muestre o elija **[!UICONTROL Or]** si desea que se muestre el mensaje si **o** de los activadores son verdaderos.

   ![](assets/in_app_create_3.png)

1. Elija el evento que activa el mensaje desde la variable **[!UICONTROL Mobile app trigger]**
lista desplegable.

   Al elegir un activador, elige qué acción del usuario hace que se muestre el mensaje en la aplicación.

   ![](assets/in_app_create_3.png)

1. Las campañas están diseñadas para ejecutarse en una fecha específica o con una frecuencia recurrente. Obtenga información sobre cómo configurar la variable **[!UICONTROL Schedule]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Ahora puede empezar a diseñar el contenido con la variable **[!UICONTROL Edit content]** botón.

   ![](assets/in_app_create_4.png)

## Enviar mensajes en la aplicación{#in-app-send}

### Vista previa en el dispositivo {#preview-device}

Puede previsualizar la notificación en la aplicación en un dispositivo específico.

1. Haga clic en **[!UICONTROL Preview on device]**.

   ![](assets/in_app_create_6.png)

1. En el **[!UICONTROL Connect to device]** ventana, haga clic en **[!UICONTROL Start]**.

1. Escriba en la **[!UICONTROL Base URL]** de la aplicación y haga clic en **[!UICONTROL Next]**.

   ![](assets/in_app_create_7.png)

1. Analice el código QR con su dispositivo e introduzca el código PIN mostrado.

El mensaje en la aplicación ahora se puede activar directamente en el dispositivo, lo que le permite previsualizar y revisar el mensaje en un dispositivo real.

### Revise y active su notificación en la aplicación{#in-app-review}

Una vez creado el mensaje en la aplicación y definido y personalizado su contenido, puede revisarlo y activarlo.

Para ello, siga los pasos a continuación:

1. Utilice la variable **[!UICONTROL Review to activate]** para mostrar un resumen del mensaje.

   El resumen le permite modificar la campaña si es necesario y comprobar si algún parámetro es incorrecto o falta.

   ![](assets/in_app_create_5.png)

1. Compruebe que la campaña esté correctamente configurada y haga clic en **[!UICONTROL Activate]**.

La campaña ya está activada. La notificación en la aplicación configurada en la campaña se envía inmediatamente o en la fecha especificada.

Una vez enviados, puede medir el impacto de los mensajes en la aplicación dentro del informe de Campaign. Para obtener más información sobre los informes, consulte [esta sección](inapp-report.md).

**Temas relacionados:**

* [Diseño de mensajes en la aplicación](design-in-app.md)
* [Informe en la aplicación](inapp-report.md)
* [Configuración en la aplicación](inapp-configuration.md)
