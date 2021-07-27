---
solution: Journey Orchestration
title: Acerca de la configuración de acciones personalizadas
description: Obtenga información sobre cómo configurar una acción personalizada
feature: Acciones
topic: Administración
role: Admin
level: Intermediate
source-git-commit: e6d8d8ee637008a886ca308b5b0d9d53d90b11ce
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 9%

---

# Configuración de una acción {#configure-an-action}

Si utiliza un sistema de terceros para enviar mensajes o si desea que los recorridos envíen llamadas de API a un sistema de terceros, aquí es donde puede configurar su conexión a recorrido. La acción personalizada definida por los usuarios técnicos estará disponible en la paleta izquierda del recorrido, en la categoría **[!UICONTROL Action]** (consulte [esta página](../building-journeys/about-journey-activities.md#action-activities)). A continuación se muestran algunos ejemplos de sistemas a los que puede conectarse con acciones personalizadas: Epsilon, Facebook, Adobe.io, Firebase, etc.
Las limitaciones se enumeran en [esta página](../building-journeys/limitations.md).

Estos son los pasos principales necesarios para configurar una acción personalizada:

1. En la sección del menú ADMINISTRACIÓN, seleccione **[!UICONTROL Configurations]**. En la sección **[!UICONTROL Actions]**, haga clic en **[!UICONTROL Manage]**. Haga clic en **[!UICONTROL Create Action]** para crear una nueva acción. El panel de configuración de acciones se abre en el lado derecho de la pantalla.

   ![](../assets/custom2.png)

1. Escriba un nombre para la acción.

   >[!NOTE]
   >
   >No utilice espacios ni caracteres especiales. No utilice más de 30 caracteres.

1. Añada una descripción a la acción. Este paso es opcional.
1. El número de recorridos que utilizan esta acción se muestra en el campo **[!UICONTROL Used in]**. Puede hacer clic en el botón **[!UICONTROL View journeys]** para mostrar la lista de recorridos que utilizan esta acción.
1. Defina los diferentes parámetros **[!UICONTROL URL Configuration]**. Consulte [esta página](../action/about-custom-action-configuration.md#url-configuration).
1. Configure la sección **[!UICONTROL Authentication]** . Esta configuración es la misma que para las fuentes de datos.  Consulte [esta sección](../datasource/external-data-sources.md#section_wjp_nl5_nhb).
1. Defina el **[!UICONTROL Action parameters]**. Consulte [esta página](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Haga clic en **[!UICONTROL Save]**.

   La acción personalizada ahora está configurada y lista para utilizarse en sus recorridos. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Cuando se utiliza una acción personalizada en un recorrido, la mayoría de los parámetros son de solo lectura. Solo puede modificar los campos **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** y la sección **[!UICONTROL Authentication]**.

## Configuración de URL {#url-configuration}

Al configurar una acción personalizada, debe definir los siguientes **[!UICONTROL URL Configuration]** parámetros:

![](../assets/journeyurlconfiguration.png)

1. Añada el **[!UICONTROL URL]** del servicio externo.

   >[!NOTE]
   >
   >Recomendamos encarecidamente utilizar HTTPS por motivos de seguridad. No permitimos el uso de direcciones de Adobe que no sean públicas ni de direcciones IP.

1. Seleccione la llamada **[!UICONTROL Method]**: puede ser **[!UICONTROL POST]** o **[!UICONTROL PUT]**.
1. En la sección **[!UICONTROL Headers]** , haga clic en **[!UICONTROL Add a header field]** para definir un nuevo par clave/valor. Corresponden a los encabezados HTTP de la solicitud realizada al servicio externo. Para eliminar pares de clave/valor, coloque el cursor en el campo del encabezado y haga clic en el icono **[!UICONTROL Delete]**.

   **[!UICONTROL Content-Type]** y  **[!UICONTROL Charset]** están configurados de forma predeterminada y no se pueden eliminar ni sobrescribir.

   >[!NOTE]
   >
   >Los encabezados se validan según las siguientes [reglas de análisis](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## Definir los parámetros de acción {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

En la sección **[!UICONTROL Action parameters]** , pegue un ejemplo de la carga útil JSON para enviarla al servicio externo.

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Los nombres de campo de la carga útil no pueden contener &quot;.&quot; carácter. No pueden empezar con un carácter &quot;$&quot;.

Puede definir el tipo de parámetro (p. ej.: string, integer, etc.).

También tendrá la opción de especificar si un parámetro es una constante o una variable:

* Constante significa que el valor del parámetro se define en el panel de configuración de acciones mediante un perfil técnico. El valor siempre será el mismo en todos los recorridos. No variará y el especialista en marketing no lo verá al utilizar la acción personalizada en el recorrido. Podría ser, por ejemplo, un ID que el sistema de terceros espera. En ese caso, el campo a la derecha de la constante o variable de alternancia es el valor pasado.
* Variable significa que el valor del parámetro variará. El especialista en marketing que utilice esta acción personalizada en un recorrido podrá pasar el valor que desee o especificar dónde recuperar el valor para este parámetro (por ejemplo, desde el evento, desde Adobe Experience Platform, etc.). En ese caso, el campo a la derecha de la constante o variable de alternancia es la etiqueta que el especialista en marketing verá en el recorrido para asignar un nombre a este parámetro.

![](../assets/customactionpayloadmessage2.png)
