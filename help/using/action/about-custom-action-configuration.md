---
solution: Journey Orchestration
title: Configurar una acción personalizada
description: Obtenga información sobre cómo configurar una acción personalizada
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: d9f7c64358be3c3355337ba0db12e5b8c17bba4c
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 6%

---

# Configurar una acción personalizada {#configure-an-action}

Si utiliza un sistema de terceros para enviar mensajes o si desea que los recorridos envíen llamadas de API a un sistema de terceros, utilice acciones personalizadas para configurar su conexión con el recorrido. Por ejemplo, puede conectarse a los siguientes sistemas con acciones personalizadas: Epsilon, Slack, Adobe.io, Firebase, etc.

Las acciones personalizadas son acciones adicionales definidas por usuarios técnicos y que se ponen a disposición de los especialistas en marketing. Una vez configurados, aparecen en la paleta izquierda del recorrido, en la **[!UICONTROL Action]** categoría. Obtenga más información en [esta página](../building-journeys/about-journey-activities.md#action-activities).

## Limitaciones{#custom-actions-limitations}

Las acciones personalizadas incluyen algunas limitaciones enumeradas en [esta página](../start/limitations.md).

En los parámetros de acción personalizados, puede pasar una colección simple, así como una colección de objetos. Obtenga más información sobre las limitaciones de recopilación en [esta página](../building-journeys/collections.md#limitations).

Tenga en cuenta también que los parámetros de acciones personalizadas tienen un formato esperado (por ejemplo: string, decimal, etc.). Debe tener cuidado de respetar estos formatos esperados. Obtenga más información en esta [caso de uso](../building-journeys/collections.md).


## Pasos de configuración {#configuration-steps}

Estos son los pasos principales necesarios para configurar una acción personalizada:

1. En la sección del menú ADMINISTRACIÓN , seleccione **[!UICONTROL Configurations]**. En el  **[!UICONTROL Actions]** , haga clic en **[!UICONTROL Manage]**. Haga clic en **[!UICONTROL Create Action]** para crear una nueva acción. El panel de configuración de acciones se abre en el lado derecho de la pantalla.

   ![](assets/custom2.png)

1. Escriba un nombre para la acción.

   >[!NOTE]
   >
   >No utilice espacios ni caracteres especiales. No utilice más de 30 caracteres.

1. Añada una descripción a la acción. Este paso es opcional.
1. El número de recorridos que utilizan esta acción se muestra en la **[!UICONTROL Used in]** campo . Puede hacer clic en el botón **[!UICONTROL View journeys]** para mostrar la lista de recorridos que utilizan esta acción.
1. Defina los diferentes **[!UICONTROL URL Configuration]** parámetros. Consulte [esta página](../action/about-custom-action-configuration.md#url-configuration).
1. Configure las variables **[!UICONTROL Authentication]** para obtener más información. Esta configuración es la misma que para las fuentes de datos.  Consulte [esta sección](../datasource/external-data-sources.md#custom-authentication-mode).
1. Defina el **[!UICONTROL Action parameters]**. Consulte [esta página](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Haga clic en **[!UICONTROL Save]**.

   La acción personalizada ahora está configurada y lista para utilizarse en sus recorridos. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Cuando se utiliza una acción personalizada en un recorrido, la mayoría de los parámetros son de solo lectura. Solo puede modificar el **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** y **[!UICONTROL Authentication]** para obtener más información.

## Configuración de URL {#url-configuration}

Al configurar una acción personalizada, debe definir lo siguiente **[!UICONTROL URL Configuration]** parámetros:

![](assets/journeyurlconfiguration.png)

1. En el **[!UICONTROL URL]** especifique la URL del servicio externo:

   * Si la dirección URL es estática, introduzca la dirección URL en este campo.

   * Si la dirección URL incluye una ruta dinámica, introduzca únicamente la parte estática de la dirección URL, es decir, el esquema, el host, el puerto y, opcionalmente, una parte estática de la ruta.

      Ejemplo: `https://xxx.yyy.com/somethingstatic/`

      Al agregar la acción personalizada a un recorrido, especificará la ruta dinámica de la dirección URL. [Más información](../building-journeys/using-custom-actions.md).
   >[!NOTE]
   >
   >Por motivos de seguridad, recomendamos encarecidamente que utilice el esquema HTTPS para la dirección URL. No permitimos el uso de direcciones de Adobe que no sean públicas ni de direcciones IP.
   >
   >Solo se permiten los puertos predeterminados al definir una acción personalizada: 80 para http y 443 para https.

1. Seleccione la llamada **[!UICONTROL Method]**: puede ser **[!UICONTROL POST]** o **[!UICONTROL PUT]**.
1. En el **[!UICONTROL Headers]** , defina los encabezados HTTP del mensaje de solicitud que se enviarán al servicio externo:
   1. Para añadir un campo de encabezado, haga clic en **[!UICONTROL Add a header field]**.
   1. Introduzca la clave del campo de encabezado.
   1. Para establecer un valor dinámico para el par clave-valor, seleccione **[!UICONTROL Variable]**. De lo contrario, seleccione **[!UICONTROL Constant]**.

      Por ejemplo, para una marca de tiempo, puede establecer un valor dinámico.

   1. Si ha seleccionado **[!UICONTROL Constant]** y, a continuación, introduzca el valor constante.

      Si ha seleccionado **[!UICONTROL Variable]**, especificará esta variable al agregar la acción personalizada a un recorrido. [Más información](../building-journeys/using-custom-actions.md).

      ![](assets/journeyurlconfiguration2.png)

   1. Para eliminar un campo de encabezado, elija el campo de encabezado y haga clic en el botón **[!UICONTROL Delete]** icono.
   La variable **[!UICONTROL Content-Type]** y **[!UICONTROL Charset]** los campos de encabezado se establecen de forma predeterminada. Estos campos no se pueden modificar ni eliminar.

   Después de agregar la acción personalizada a un recorrido, puede agregarle campos de encabezado si el recorrido está en estado de borrador. Si no desea que el recorrido se vea afectado por los cambios de configuración, duplique la acción personalizada y añada los campos del encabezado a la nueva acción personalizada.

   >[!NOTE]
   >
   >Los encabezados se validan según las reglas de análisis de campos. [Más información](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## Definir los parámetros de acción {#define-the-message-parameters}

![](assets/messageparameterssection.png)

En el **[!UICONTROL Action parameters]** , pegue un ejemplo de la carga útil JSON para enviarla al servicio externo.

![](assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Los nombres de campo de la carga útil no pueden contener &quot;.&quot; carácter. No pueden empezar con un carácter &quot;$&quot;.

Puede definir el tipo de parámetro (p. ej.: string, integer, etc.).

También tendrá la opción de especificar si un parámetro es una constante o una variable:

* Constante significa que el valor del parámetro se define en el panel de configuración de acciones mediante un perfil técnico. El valor siempre será el mismo en todos los recorridos. No variará y el especialista en marketing no lo verá al utilizar la acción personalizada en el recorrido. Podría ser, por ejemplo, un ID que el sistema de terceros espera. En ese caso, el campo a la derecha de la constante o variable de alternancia es el valor pasado.
* Variable significa que el valor del parámetro variará. Los especialistas en marketing que utilicen esta acción personalizada en un recorrido podrán pasar el valor que deseen o especificar dónde recuperar el valor de este parámetro (por ejemplo, desde el evento, desde Adobe Experience Platform, etc.). En ese caso, el campo a la derecha de la constante o variable de alternancia es la etiqueta que los especialistas en marketing verán en el recorrido para asignar un nombre a este parámetro.

![](assets/customactionpayloadmessage2.png)
