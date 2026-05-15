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
TQID: https://experienceleague.adobe.com/Sw-hR0cfAG8Lk8YbhJKj53UqG-er2bC3-7Ijih0PF44
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 20%

---

# Uso de acciones personalizadas {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Acciones personalizadas"
>abstract="Las acciones personalizadas permiten configurar la conexión de un sistema de terceros para enviar mensajes o llamadas API. Se puede configurar una acción con cualquier servicio de cualquier proveedor al que se pueda llamar mediante una API REST con carga útil en formato JSON."

Utilice acciones personalizadas para habilitar la conexión a un sistema de terceros para enviar mensajes o llamadas API. Se puede configurar una acción con cualquier servicio de cualquier proveedor al que se pueda llamar mediante una API REST con carga útil en formato JSON.

Obtenga más información acerca de las acciones personalizadas en [esta sección](../action/action.md).

Aprenda a crear y configurar una acción personalizada en [esta página](../action/about-custom-action-configuration.md).

Aprenda a utilizar las respuestas de llamadas de API de acciones personalizadas para personalizar [esta página](../action/action-response.md).

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

![Configuración de URL de acción personalizada con asignación de parámetros dinámicos](assets/journey-custom-action-url.png)

### Encabezados y parámetros de consulta {#headers}

La sección **[!UICONTROL Configuración de URL]** muestra los campos de encabezado dinámico y parámetro de consulta, pero no los campos de constantes. Los campos de encabezado dinámico y parámetro de consulta se definen como variables en la pantalla de configuración de acciones. [Más información](../action/about-custom-action-configuration.md#url-configuration)

Para especificar el valor de los campos de encabezado dinámico y parámetro de consulta, haga clic dentro del campo o en el icono de lápiz y seleccione el campo deseado.

![Configuración del campo de encabezado dinámico en la acción personalizada](assets/journey-dynamicheaderfield.png)

## Parámetros de acción

En la sección **[!UICONTROL Parámetros de acción]**, verá los parámetros de mensaje definidos como _&quot;Variable&quot;_. Para estos parámetros, puede definir de dónde obtener esta información (por ejemplo: eventos, fuentes de datos), pasar valores manualmente o utilizar el editor de expresiones avanzadas para casos de uso avanzados. Los casos de uso avanzados pueden ser manipulación de datos y otro uso de funciones. Consulte [esta página](expression/expressionadvanced.md).

