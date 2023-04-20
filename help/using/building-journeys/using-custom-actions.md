---
solution: Journey Optimizer
product: journey optimizer
title: Uso de acciones personalizadas
description: Aprenda a utilizar acciones personalizadas
feature: Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: acción, personalizado, API, recorrido, configuración, servicio
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 25%

---

# Uso de acciones personalizadas {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Acciones personalizadas"
>abstract="Las acciones personalizadas permiten configurar la conexión de un sistema de terceros para enviar mensajes o llamadas API. Se puede configurar una acción con cualquier servicio de cualquier proveedor al que se pueda llamar mediante una API REST con carga útil en formato JSON."

Las acciones personalizadas permiten configurar la conexión de un sistema de terceros para enviar mensajes o llamadas API. Se puede configurar una acción con cualquier servicio de cualquier proveedor al que se pueda llamar mediante una API REST con carga útil en formato JSON.

## Consentimiento y control de datos {#privacy}

En Journey Optimizer, puede aplicar políticas de control y consentimiento de datos a sus acciones personalizadas para evitar que campos específicos se exporten a sistemas de terceros o excluir a clientes que no hayan aceptado recibir comunicaciones por correo electrónico, push o SMS. Para obtener más información, consulte las páginas siguientes:

* [Administración de datos](../action/action-privacy.md).
* [Consentimiento](../action/consent.md).

## Configuración de URL

El panel de configuración del **Acción personalizada** actividad muestra los parámetros de configuración de URL y los parámetros de autenticación configurados para la acción personalizada. No se puede configurar la parte estática de la URL en el recorrido, sino en la configuración global de la acción personalizada. [Más información](../action/about-custom-action-configuration.md).

### Ruta dinámica

Si la dirección URL incluye una ruta dinámica, especifique la ruta en la **[!UICONTROL Ruta]** campo .

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

La variable **[!UICONTROL Configuración de URL]** muestra los campos del encabezado dinámico, pero no los campos del encabezado constante. Los campos de encabezado dinámico son campos de encabezado HTTP cuyo valor está configurado como variable. [Más información](../action/about-custom-action-configuration.md).

Si es necesario, especifique el valor de los campos del encabezado dinámico:

1. Seleccione la acción personalizada en el recorrido .
1. En el panel de configuración, haga clic en el icono de lápiz situado junto al campo de encabezado en la **[!UICONTROL Configuración de URL]** para obtener más información.

   ![](assets/journey-dynamicheaderfield.png)

1. Seleccione un campo y haga clic en **[!UICONTROL OK]**.

## Parámetros de acción

En el **[!UICONTROL Parámetros de acción]** , verá los parámetros de mensaje definidos como _&quot;Variable&quot;_. Para estos parámetros, puede definir dónde obtener esta información (por ejemplo: eventos, fuentes de datos), pase valores manualmente o utilice el editor de expresiones avanzadas para casos de uso avanzados. Los casos de uso avanzados pueden ser manipulación de datos y otro uso de funciones. Consulte [esta página](expression/expressionadvanced.md).

**Temas relacionados**

[Configuración de una acción](../action/about-custom-action-configuration.md)
