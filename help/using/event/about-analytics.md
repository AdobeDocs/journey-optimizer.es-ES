---
solution: Journey Optimizer
product: journey optimizer
title: Integración de Adobe Analytics
description: Aprenda a aprovechar los datos de Adobe Analytics en Journey Optimizer
feature: Journeys, Events, Reporting, Integrations
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: analytics, integración, sdk web, plataforma
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 6%

---

# Trabajo con datos de Adobe Analytics {#analytics-data}

Puede aprovechar todos los datos de evento de comportamiento web que ya está capturando mediante Adobe Analytics o SDK web y la transmisión a Adobe Experience Platform para almacenar en déclencheur los recorridos y automatizar las experiencias para sus clientes.

Para que esto funcione con Adobe Analytics, debe:

1. Active el grupo de informes que desee utilizar. [Más información](#leverage-analytics-data)
1. Habilite Journey Optimizer para utilizar la fuente de datos de Adobe Analytics. [Más información](#activate-analytics-data)
1. Añada un evento específico en el recorrido. [Más información](#event-analytic)

>[!NOTE]
>
>Esta sección solo se aplica a los eventos basados en reglas y a los clientes que necesitan utilizar datos de Adobe Analytics o SDK web.
> 
>Si utiliza Adobe Customer Journey Analytics, consulte [esta página](../reports/cja-ajo.md).
>

## Configuración de datos de Adobe Analytics o SDK web {#leverage-analytics-data}

Los datos procedentes del SDK web de Adobe Analytics o Adobe Experience Platform deben habilitarse para que se utilicen en los recorridos.

Para realizar esto, siga los pasos a continuación:

1. Vaya a la **[!UICONTROL Fuentes]** menú.

1. En la sección Adobe Analytics, seleccione **[!UICONTROL Añadir datos]**

   ![](assets/ajo-aa_1.png)

1. En la lista de grupos de informes de Adobe Analytics disponibles, seleccione **[!UICONTROL Grupo de informes]** para habilitar. A continuación, haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/ajo-aa_2.png)

1. Elija si desea utilizar un esquema predeterminado o personalizado.

1. Desde el **[!UICONTROL Detalles del flujo de datos]** pantalla, elija una **[!UICONTROL Nombre de flujo de datos]**.

1. Una vez completada la configuración, haga clic en **[!UICONTROL Finalizar]**.

   ![](assets/ajo-aa_3.png)

Esto habilita el conector de origen de Analytics para ese grupo de informes. Cada vez que llegan los datos, se transforman en un evento de Experience y se envían a Adobe Experience Platform.

![](assets/ajo-aa_4.png)

Obtenga más información acerca del conector de origen de Adobe Analytics en  [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=es){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=es){target="_blank"}.

## Activar esta configuración {#activate-analytics-data}

Una vez completada esta configuración, póngase en contacto con el Adobe de para permitir que su entorno de Journey Optimizer utilice esta fuente de datos. Este paso solo es necesario para las fuentes de datos de Adobe Analytics. Para realizar esto:

1. Obtenga el ID de la fuente de datos. Esta información está disponible en la interfaz de usuario de: vaya a la fuente de datos creada desde el **Flujos de datos** de la pestaña **Fuentes** menú. La forma más sencilla de encontrarlo es filtrar por fuentes de Adobe Analytics.
1. Póngase en contacto con el Servicio de atención al cliente de Adobe con los siguientes detalles:

   * Asunto: Habilitar eventos de Adobe Analytics para recorridos

   * Contenido: habilite mi entorno para utilizar eventos AA.

      * ID de organización: &quot;XXX@AdobeOrg&quot;

      * ID de fuente de datos: &quot;ID: xxxxx&quot;

1. Una vez que tenga la confirmación de que su entorno está listo, puede utilizar los datos de Adobe Analytics en sus recorridos.

## Creación de un recorrido con un evento mediante datos de Adobe Analytics o SDK web {#event-analytics}

Ahora puede crear un evento basado en datos del SDK web de Adobe Analytics o Adobe Experience Platform para utilizarlo en un recorrido.

En el siguiente ejemplo, aprenda a segmentar usuarios que agregaron un producto a sus carros de compras:

* Si el pedido se completa, los usuarios reciben un correo electrónico de seguimiento dos días después para solicitar comentarios.
* Si el pedido no se ha completado, los usuarios recibirán un correo electrónico para recordarles que completen el pedido.

1. Desde Adobe Journey Optimizer, acceda a **[!UICONTROL Configuración]** menú.

1. A continuación, seleccione **[!UICONTROL Administrar]** desde el **[!UICONTROL Eventos]** Tarjeta de.

   ![](assets/ajo-aa_5.png)

1. Clic **[!UICONTROL Crear evento]**. El panel de configuración de evento se abre en el lado derecho de la pantalla.

1. Rellene el **[!UICONTROL Evento]** parámetros:

   * **[!UICONTROL Nombre]**: Personalice el nombre de su **[!UICONTROL Evento]**.
   * **[!UICONTROL Tipo]**: elija el **[!UICONTROL Unitario]** Escriba. [Más información](../event/about-events.md)
   * **[!UICONTROL Tipo de ID de evento]**: elija el **[!UICONTROL Basado en reglas]** Tipo de ID de evento. [Más información](../event/about-events.md#event-id-type)
   * **[!UICONTROL Esquema]**: seleccione el esquema de Analytics o WebSDK [creado antes de](#leverage-analytics-data).
   * **[!UICONTROL Campos]**: seleccione los campos Carga útil. [Más información](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Condición de ID de evento]**: Defina la condición para identificar los eventos que pondrán en déclencheur el recorrido.

     En este caso, el Evento se activa cuando los clientes agregan un artículo a sus carros de compras.
   * **[!UICONTROL Identificador de perfil]**: elija un campo de los campos de carga útil o defina una fórmula para identificar a la persona asociada al evento.

   ![](assets/ajo-aa_6.png)

1. Cuando esté configurado, seleccione **[!UICONTROL Guardar]**.

Ahora que el evento está listo, cree un recorrido para utilizarlo.

1. Desde el **[!UICONTROL Recorridos]** , abra o cree un recorrido. Para obtener más información, consulte [esta sección](../building-journeys/journey-gs.md).

1. Añada el evento de Analytics configurado anteriormente en el recorrido.

   ![](assets/ajo-aa_8.png)

1. Añada un evento que se activará si se completa una solicitud.

1. De su **[!UICONTROL Menú Evento]**, seleccione la **[!UICONTROL Definir el tiempo de espera del evento]** y **[!UICONTROL Establecer una ruta de tiempo de espera]** opciones.

   ![](assets/ajo-aa_9.png)

1. En la ruta de tiempo de espera, añada un **[!UICONTROL Correo electrónico]** acción. Esta ruta se utilizará para enviar un correo electrónico a los clientes que no hayan completado una solicitud para recordarles que sus carros de compras aún están disponibles.

1. Añadir un **[!UICONTROL Esperar]** actividad después de la ruta principal y configúrela en la duración necesaria.

   ![](assets/ajo-aa_10.png)

1. A continuación, añada una **[!UICONTROL Acción de correo electrónico]**. En este correo electrónico, se solicitará a los clientes que envíen comentarios sobre el pedido realizado.

Ahora puede probar y publicar el recorrido. [Más información](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
