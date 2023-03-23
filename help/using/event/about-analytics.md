---
solution: Journey Optimizer
product: journey optimizer
title: Integración de Adobe Analytics
description: Aprenda a aprovechar los datos de Adobe Analytics en Journey Optimizer
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: analytics, integración, sdk web, plataforma
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 16752d94647b25b4a86c34b77bda0f72fcfaf169
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 7%

---

# Trabajo con datos de Adobe Analytics {#analytics-data}

Puede aprovechar todos los datos de eventos de comportamiento web que ya está capturando a través de Adobe Analytics o SDK web, y transmitirlos a Adobe Experience Platform, para almacenar en déclencheur los recorridos y automatizar las experiencias para sus clientes.

Para que esto funcione con Adobe Analytics, debe:

1. Active el grupo de informes que desee utilizar. [Más información](#leverage-analytics-data)
1. Habilite Journey Optimizer para que use la fuente de datos de Adobe Analytics. [Más información](#activate-analytics-data)
1. Añada un evento específico en el recorrido. [Más información](#event-analytic)

>[!NOTE]
>
>Esta sección solo se aplica para eventos basados en reglas y clientes que necesitan utilizar datos de Adobe Analytics o SDK web.
> 
>Si utiliza Adobe Customer Journey Analytics, consulte [esta página](../reports/cja-ajo.md).

## Configuración de datos de Adobe Analytics o SDK web {#leverage-analytics-data}

Los datos procedentes del SDK web de Adobe Analytics o Adobe Experience Platform deben estar activados para poder utilizarlos en sus recorridos.

Para realizar esto, siga los pasos a continuación:

1. Vaya a la **[!UICONTROL Fuentes]** para abrir el Navegador.

1. En la sección Adobe Analytics , seleccione **[!UICONTROL Añadir datos]**

   ![](assets/ajo-aa_1.png)

1. En la lista de grupos de informes de Adobe Analytics disponibles, seleccione la opción **[!UICONTROL Grupo de informes]** para habilitar. A continuación, haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/ajo-aa_2.png)

1. Elija si desea utilizar un esquema predeterminado o personalizado.

1. En el **[!UICONTROL Detalles de flujo de datos]** , elija un **[!UICONTROL Nombre de flujo de datos]**.

1. Una vez completada la configuración, haga clic en **[!UICONTROL Finalizar]**.

   ![](assets/ajo-aa_3.png)

Esto habilita el conector de origen de Analytics para ese grupo de informes. Cada vez que entran los datos, estos se transforman en un evento de Experience y se envían a Adobe Experience Platform.

![](assets/ajo-aa_4.png)

Obtenga más información sobre el conector de origen de Adobe Analytics en  [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=es){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=es){target="_blank"}.

## Activar esta configuración {#activate-analytics-data}

Una vez completada esta configuración, póngase en contacto con el Adobe para habilitar el entorno de Journey Optimizer para utilizar esta fuente de datos. Este paso solo es necesario para las fuentes de datos de Adobe Analytics. Para realizar esto:

1. Obtenga el ID de la fuente de datos. Esta información está disponible en la interfaz de usuario de : busque el origen de datos creado desde la **Flujos de datos** de la pestaña **Fuentes** para abrir el Navegador. La forma más sencilla de encontrarlo es filtrar las fuentes de Adobe Analytics.
1. Póngase en contacto con el Servicio de atención al cliente de Adobe con los siguientes detalles:

   * Asunto: Habilitar eventos de Adobe Analytics para recorridos

   * Contenido: Habilite mi entorno para utilizar eventos AA.

      * ID de organización: &quot;XXX@AdobeOrg&quot;

      * ID de fuente de datos: &quot;ID: xxxxx&quot;

1. Una vez que haya confirmado que su entorno está listo, puede utilizar los datos de Adobe Analytics en sus recorridos.

## Creación de un recorrido con un evento mediante datos de Adobe Analytics o SDK web {#event-analytics}

Ahora puede crear un evento basado en datos del SDK web de Adobe Analytics o Adobe Experience Platform para utilizarlo en un recorrido.

En el ejemplo siguiente, aprenda a dirigirse a los usuarios que agregaron un producto al carro de compras:

* Si se completa el pedido, los usuarios reciben un correo electrónico de seguimiento dos días después para solicitar comentarios.
* Si el pedido no se completa, los usuarios reciben un correo electrónico para recordarles que completen el pedido.

1. Desde Adobe Journey Optimizer, acceda a la **[!UICONTROL Configuración]** para abrir el Navegador.

1. A continuación, seleccione **[!UICONTROL Administrar]** de la variable **[!UICONTROL Eventos]** tarjeta.

   ![](assets/ajo-aa_5.png)

1. Haga clic en **[!UICONTROL Crear evento]**. El panel de configuración de evento se abre en el lado derecho de la pantalla.

1. Complete la variable **[!UICONTROL Evento]** parámetros:

   * **[!UICONTROL Nombre]**: Personalice el nombre de su **[!UICONTROL Evento]**.
   * **[!UICONTROL Tipo]**: Elija la **[!UICONTROL Unitario]** Escriba. [Más información](../event/about-events.md)
   * **[!UICONTROL Tipo de ID de evento]**: Elija la **[!UICONTROL Basado en reglas]** Tipo de ID de evento. [Más información](../event/about-events.md#event-id-type)
   * **[!UICONTROL Esquema]**: Seleccionar el esquema de Analytics o WebSDK [created before](#leverage-analytics-data).
   * **[!UICONTROL Campos]**: Seleccione los campos Carga útil . [Más información](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Condición de ID de evento]**: Defina la condición para identificar los eventos que van a almacenar en déclencheur el recorrido.

      En este caso, el evento se activa cuando los clientes añaden un artículo al carro de compras.
   * **[!UICONTROL Identificador de perfil]**: Elija un campo de los campos de carga útil o defina una fórmula para identificar la persona asociada al evento.

   ![](assets/ajo-aa_6.png)

1. Cuando esté configurado, seleccione **[!UICONTROL Guardar]**.

Ahora que el evento está listo, cree un recorrido para utilizarlo.

1. En el **[!UICONTROL Recorridos]** , abra o cree un recorrido. Para obtener más información, consulte [esta sección](../building-journeys/journey-gs.md).

1. Añada el evento de Analytics previamente configurado al recorrido.

   ![](assets/ajo-aa_8.png)

1. Añada un evento que se activará si se completa un pedido.

1. Desde su **[!UICONTROL Menú Evento]**, seleccione **[!UICONTROL Definir el tiempo de espera del evento]** y **[!UICONTROL Establecer una ruta de tiempo de espera]** opciones.

   ![](assets/ajo-aa_9.png)

1. Desde la ruta de tiempo de espera, agregue un **[!UICONTROL Correo electrónico]** acción. Esta ruta se utilizará para enviar un correo electrónico a los clientes que no hayan completado un pedido para recordarles que sus carros siguen disponibles.

1. Agregue un **[!UICONTROL Espera]** después de la ruta principal y configúrela en la duración necesaria.

   ![](assets/ajo-aa_10.png)

1. A continuación, agregue un **[!UICONTROL Acción de correo electrónico]**. En este correo electrónico, se pedirá a los clientes que proporcionen comentarios sobre el pedido realizado.

Ahora puede probar y publicar el recorrido. [Más información](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
