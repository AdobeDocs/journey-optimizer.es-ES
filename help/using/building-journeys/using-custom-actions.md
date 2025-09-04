---
solution: Journey Optimizer
product: journey optimizer
title: Uso de acciones personalizadas
description: Aprenda a utilizar acciones personalizadas
feature: Journeys, Actions, Custom Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: acción, personalizado, API, recorrido, configuración, servicio
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 21%

---

# Uso de acciones personalizadas {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Acciones personalizadas"
>abstract="Las acciones personalizadas permiten configurar la conexión de un sistema de terceros para enviar mensajes o llamadas API. Se puede configurar una acción con cualquier servicio de cualquier proveedor al que se pueda llamar mediante una API REST con carga útil en formato JSON."

Utilice acciones personalizadas para habilitar la conexión a un sistema de terceros para enviar mensajes o llamadas API. Se puede configurar una acción con cualquier servicio de cualquier proveedor al que se pueda llamar mediante una API REST con carga útil en formato JSON.

Obtenga más información acerca de las acciones personalizadas en [esta sección](../action/action.md).

Aprenda a crear y configurar una acción personalizada en [esta página](../action/about-custom-action-configuration.md).

## Consentimiento y control de datos {#privacy}

En Journey Optimizer, puede aplicar políticas de gobernanza de datos y consentimiento a sus acciones personalizadas para evitar que campos específicos se exporten a sistemas de terceros o excluyan a los clientes que no hayan aceptado recibir comunicaciones por correo electrónico, push o SMS. Para obtener más información, consulte las siguientes páginas:

* [Gobernanza de datos](../action/action-privacy.md).
* [Consentimiento](../action/consent.md).

## Configuración de URL

El panel de configuración de la actividad **Acción personalizada** muestra los parámetros de configuración de la URL y los parámetros de autenticación que están configurados para la acción personalizada. No se puede configurar la parte estática de la URL en la recorrido, sino en la configuración global de la acción personalizada. [Más información](../action/about-custom-action-configuration.md).

### Ruta dinámica

Si la dirección URL incluye una ruta dinámica, especifique la ruta en el campo **[!UICONTROL Ruta]**.

Para concatenar campos y cadenas de texto sin formato, utilice las funciones Cadena o el signo Más (+) en el editor de expresiones avanzadas. Escriba las cadenas de texto sin formato entre comillas simples (&#39;) o dobles (&quot;). [Más información](expression/expressionadvanced.md).

Esta tabla muestra un ejemplo de configuración:

| Campo | Valor |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Ruta | `The _id + '/messages'` |

La URL concatenada tiene este formulario:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;ID>`/messages`

![](assets/journey-custom-action-url.png)

### Encabezados y parámetros de consulta {#headers}

La sección **[!UICONTROL Configuración de URL]** muestra los campos de encabezado dinámico y parámetro de consulta, pero no los campos de constantes. Los campos de encabezado dinámico y parámetro de consulta se definen como variables en la pantalla de configuración de acciones. [Más información](../action/about-custom-action-configuration.md#url-configuration)

Para especificar el valor de los campos de encabezado dinámico y parámetro de consulta, haga clic dentro del campo o en el icono de lápiz y seleccione el campo deseado.

![](assets/journey-dynamicheaderfield.png)

## Parámetros de acción

En la sección **[!UICONTROL Parámetros de acción]**, verá los parámetros de mensaje definidos como _&quot;Variable&quot;_. Para estos parámetros, puede definir de dónde obtener esta información (por ejemplo: eventos, fuentes de datos), pasar valores manualmente o utilizar el editor de expresiones avanzadas para casos de uso avanzados. Los casos de uso avanzados pueden ser manipulación de datos y otro uso de funciones. Consulte [esta página](expression/expressionadvanced.md).

