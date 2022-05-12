---
title: Uso de acciones personalizadas
description: Aprenda a utilizar acciones personalizadas
feature: Actions
topic: Content Management
role: User
level: Intermediate
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 94c2e889b38608aa173b62edb498eba7756e68e6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 29%

---

# Uso de acciones personalizadas {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Acciones personalizadas"
>abstract="Las acciones personalizadas le permiten configurar la conexión de un sistema de terceros para enviar mensajes o llamadas API. Se puede configurar una acción con cualquier servicio de cualquier proveedor al que se pueda llamar mediante una API REST con carga útil en formato JSON."

Las acciones personalizadas le permiten configurar la conexión de un sistema de terceros para enviar mensajes o llamadas API. Se puede configurar una acción con cualquier servicio de cualquier proveedor al que se pueda llamar mediante una API REST con carga útil en formato JSON.

## Configuración de URL

El panel de configuración del **Acción personalizada** actividad muestra los parámetros de configuración de URL y los parámetros de autenticación configurados para la acción personalizada. No se puede configurar la parte estática de la URL en el recorrido, sino en la configuración global de la acción personalizada. [Más información](../action/about-custom-action-configuration.md).

### Ruta dinámica

Si la dirección URL incluye una ruta dinámica, especifique la ruta en la **[!UICONTROL Path]** campo .

Para concatenar campos y cadenas de texto sin formato, utilice las funciones de cadena o el signo más (+) en el editor de expresiones avanzadas. Escriba cadenas de texto sin formato entre comillas simples (&#39;) o entre comillas dobles (&quot;). [Más información](expression/expressionadvanced.md).

Esta tabla muestra un ejemplo de configuración:

| Campo | Valor |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Ruta | `The id of marketingCampaign + '/messages'` |

La dirección URL concatenada tiene este formulario:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### Encabezados

La variable **[!UICONTROL URL Configuration]** muestra los campos del encabezado dinámico, pero no los campos del encabezado constante. Dynamic header fields are HTTP header fields whose value is configured as a variable. [Más información](../action/about-custom-action-configuration.md).

Si es necesario, especifique el valor de los campos del encabezado dinámico:

1. Select the custom action in the journey.
1. En el panel de configuración, haga clic en el icono de lápiz situado junto al campo de encabezado en la **[!UICONTROL URL Configuration]** para obtener más información.

   ![](assets/journey-dynamicheaderfield.png)

1. Select a field and click **[!UICONTROL OK]**.

## Action parameters

In the **[!UICONTROL Action parameters]** section, you&#39;ll see the message parameters defined as _&quot;Variable&quot;_. Para estos parámetros, puede definir dónde obtener esta información (por ejemplo: eventos, fuentes de datos), pase valores manualmente o utilice el editor de expresiones avanzadas para casos de uso avanzados. Los casos de uso avanzados pueden ser manipulación de datos y otro uso de funciones. Consulte [esta página](expression/expressionadvanced.md).
