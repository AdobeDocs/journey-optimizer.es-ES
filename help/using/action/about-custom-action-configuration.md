---
solution: Journey Optimizer
product: journey optimizer
title: Configurar una acción personalizada
description: Obtenga información sobre cómo configurar una acción personalizada
feature: Actions
topic: Administration
role: Admin
level: Experienced
keywords: acción, terceros, personalizado, recorrido, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 15%

---

# Configurar una acción personalizada {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Acciones personalizadas"
>abstract="Si utiliza un sistema de terceros para enviar mensajes o si desea que los recorridos envíen llamadas de API a un sistema de terceros, utilice acciones personalizadas para configurar la conexión a su recorrido. Por ejemplo, puede conectarse a los siguientes sistemas con las acciones personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase, etc."

Si utiliza un sistema de terceros para enviar mensajes o si desea que los recorridos envíen llamadas de API a un sistema de terceros, utilice acciones personalizadas para configurar la conexión a su recorrido. Por ejemplo, puede conectarse a los siguientes sistemas con acciones personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, etc.

Las acciones personalizadas son acciones adicionales definidas por usuarios técnicos y que se ponen a disposición de los expertos en marketing. Una vez configuradas, aparecen en la paleta izquierda del recorrido, en la **[!UICONTROL Acción]** categoría. Obtenga más información en [esta página](../building-journeys/about-journey-activities.md#action-activities).

## Limitaciones{#custom-actions-limitations}

Las acciones personalizadas incluyen algunas limitaciones enumeradas en [esta página](../start/guardrails.md).

En los parámetros de acción personalizados, puede pasar una colección simple, así como una colección de objetos. Obtenga más información acerca de las limitaciones de recopilación en [esta página](../building-journeys/collections.md#limitations).

Tenga en cuenta también que los parámetros de acciones personalizadas tienen un formato esperado (por ejemplo: cadena, decimal, etc.). Debe tener cuidado de respetar estos formatos esperados. Obtenga más información en esta [caso de uso](../building-journeys/collections.md).

## Consentimiento y control de datos {#privacy}

En Journey Optimizer, puede aplicar políticas de gobernanza de datos y consentimiento a sus acciones personalizadas para evitar que campos específicos se exporten a sistemas de terceros o excluyan a los clientes que no hayan aceptado recibir comunicaciones por correo electrónico, push o SMS. Para obtener más información, consulte las siguientes páginas:

* [Gobernanza de datos](../action/action.md).
* [Consentimiento](../action/action.md).


## Pasos de configuración {#configuration-steps}

Estos son los pasos principales necesarios para configurar una acción personalizada:

1. En la sección del menú ADMINISTRACIÓN, seleccione **[!UICONTROL Configuraciones]**. En el  **[!UICONTROL Acciones]** , haga clic en **[!UICONTROL Administrar]**. Clic **[!UICONTROL Crear acción]** para crear una acción nueva. El panel de configuración de acción se abre en el lado derecho de la pantalla.

   ![](assets/custom2.png)

1. Escriba un nombre para la acción.

   >[!NOTE]
   >
   >No utilice espacios ni caracteres especiales. No utilice más de 30 caracteres.

1. Añada una descripción a la acción. Este paso es opcional.
1. El número de recorridos que utilizan esta acción se muestra en la variable **[!UICONTROL Utilizado en]** field. Puede hacer clic en **[!UICONTROL Ver recorridos]** para mostrar la lista de recorridos con esta acción.
1. Defina los diferentes **[!UICONTROL Configuración de URL]** parámetros. Consulte [esta página](../action/about-custom-action-configuration.md#url-configuration).
1. Configure las variables **[!UICONTROL Autenticación]** sección. Esta configuración es la misma que para las fuentes de datos.  Consulte [esta sección](../datasource/external-data-sources.md#custom-authentication-mode).
1. Defina el **[!UICONTROL Parámetros de acción]**. Consulte [esta página](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Haga clic en **[!UICONTROL Guardar]**.

   La acción personalizada ahora está configurada y lista para utilizarse en sus recorridos. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Cuando se utiliza una acción personalizada en un recorrido, la mayoría de los parámetros son de solo lectura. Solo puede modificar la variable **[!UICONTROL Nombre]**, **[!UICONTROL Descripción]**, **[!UICONTROL URL]** y el **[!UICONTROL Autenticación]** sección.

## Configuración de URL {#url-configuration}

Al configurar una acción personalizada, debe definir lo siguiente **[!UICONTROL Configuración de URL]** parámetros:

![](assets/journeyurlconfiguration.png)

1. En el **[!UICONTROL URL]** , especifique la URL del servicio externo:

   * Si la dirección URL es estática, introduzca la dirección URL en este campo.

   * Si la dirección URL incluye una ruta dinámica, introduzca solo la parte estática de la dirección URL, es decir, el esquema, el host, el puerto y, opcionalmente, una parte estática de la ruta.

      Ejemplo: `https://xxx.yyy.com/somethingstatic/`

      Especifique la ruta dinámica de la URL al agregar la acción personalizada a un recorrido. [Más información](../building-journeys/using-custom-actions.md).
   >[!NOTE]
   >
   >Por motivos de seguridad, le recomendamos encarecidamente que utilice el esquema HTTPS para la dirección URL. No permitimos el uso de direcciones de Adobe que no sean públicas ni de direcciones IP.
   >
   >Solo se permiten los puertos predeterminados al definir una acción personalizada: 80 para http y 443 para https.

1. Seleccione la llamada **[!UICONTROL Método]**: puede ser cualquiera de las siguientes **[!UICONTROL POST]** o **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > El **DELETE** no se admite el método. Si necesita actualizar un recurso existente, seleccione la **PUT** método.

1. Defina los encabezados y los parámetros de consulta:

   * En el **[!UICONTROL Encabezados]** , haga clic en **[!UICONTROL Añadir un campo de encabezado]** para definir los encabezados HTTP del mensaje de solicitud que se va a enviar al servicio externo. El **[!UICONTROL Content-Type]** y **[!UICONTROL Charset]** los campos de encabezado están configurados de forma predeterminada. Estos campos no se pueden modificar ni eliminar.

   * En el **[!UICONTROL Parámetros de consulta]** , haga clic en **[!UICONTROL Agregar un campo de parámetro de consulta]** para definir los parámetros que desea añadir en la dirección URL.

   ![](assets/journeyurlconfiguration2bis.png)

1. Introduzca la etiqueta o el nombre del campo.

1. Seleccione el tipo: **[!UICONTROL Constante]** o **[!UICONTROL Variable]**. Si ha seleccionado **[!UICONTROL Constante]**, luego introduzca el valor constante en **[!UICONTROL Valor]** field. Si ha seleccionado **[!UICONTROL Variable]**, entonces especificará esta variable al agregar la acción personalizada a un recorrido. [Más información](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Después de agregar la acción personalizada a un recorrido, aún puede agregarle campos de encabezado o de parámetros de consulta si el recorrido está en estado de borrador. Si no desea que los cambios de configuración afecten al recorrido, duplique la acción personalizada y agregue los campos a la nueva acción personalizada.
   >
   >Los encabezados se validan según las reglas de análisis de campos. Obtenga más información en [esta documentación](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Defina los parámetros de acción {#define-the-message-parameters}

En el **[!UICONTROL Parámetros de acción]** , pegue un ejemplo de la carga útil JSON para enviar al servicio externo.

![](assets/messageparameterssection.png)

>[!NOTE]
>
>El ejemplo de carga útil no puede contener valores nulos. Los nombres de campo en la carga no pueden contener un &quot;&quot;. carácter. No pueden comenzar con el carácter &quot;$&quot;.

Podrá definir el tipo de parámetro (por ejemplo, cadena, entero, etc.).

También puede elegir entre especificar si un parámetro es una constante o una variable:

* **Constante** significa que el valor del parámetro lo define una persona técnica en el panel de configuración de acciones. El valor siempre será el mismo en todos los recorridos. No variará y el experto en marketing no lo verá al utilizar la acción personalizada en el recorrido. Podría ser, por ejemplo, un ID que espere el sistema de terceros. En ese caso, el campo a la derecha de la constante/variable de alternancia es el valor pasado.
* **Variable** significa que el valor del parámetro variará. Los especialistas en marketing que utilicen esta acción personalizada en un recorrido podrán transferir el valor que deseen o especificar dónde recuperar el valor de este parámetro (por ejemplo, desde el evento, desde Adobe Experience Platform, etc.). En ese caso, el campo a la derecha de la constante/variable de alternancia es el que los especialistas en marketing verán en el recorrido para asignar un nombre a este parámetro.

![](assets/customactionpayloadmessage2.png)
