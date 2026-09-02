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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1024
ht-degree: 8%

---

# Uso de acciones personalizadas {#use-custom-actions}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar acciones personalizadas para conectar un recorrido a un sistema de terceros a través de una llamada de API de REST con una carga útil JSON, mientras aplica políticas de gobernanza de datos y consentimiento.

>[!ENDSHADEBOX]

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

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo agregar y configurar una actividad de acción personalizada en un recorrido para llamar a una API de REST de terceros con una carga útil JSON, incluida la configuración de URL, la asignación de parámetros de encabezado/consulta, la asignación de parámetros de acción y la aplicación de directivas de gobernanza y consentimiento de datos.

**Intenciones:**

* Añada una actividad de acción personalizada a un recorrido para enviar datos a un sistema de terceros mediante la API de REST
* Configure una ruta de URL dinámica concatenando campos y texto estático en el editor de expresiones
* Asignar valores de encabezado dinámico y parámetros de consulta desde eventos de recorrido o fuentes de datos
* Asignar parámetros de acción (definidos como variables) a campos de evento, campos de fuente de datos o valores estáticos
* Aplique políticas de gobernanza de datos y consentimiento para controlar qué datos se exportan mediante acciones personalizadas

**Glosario:**

* **Acción personalizada**: una actividad de acción de recorrido que llama a un extremo externo de API REST con una carga en formato JSON para integrar sistemas de terceros *(específicos del producto)*
* **Ruta dinámica**: La parte variable de la URL de acción personalizada que se define por ejecución usando campos del contexto de recorrido *(específico del producto)*
* **Parámetros de acción**: los campos de carga útil del mensaje definidos como &quot;Variable&quot; en la configuración de acción personalizada, asignados a los datos de recorrido en el nivel de recorrido *(específico del producto)*

**Protecciones:**

* La parte estática de la dirección URL no se puede modificar en la recorrido; debe establecerse en la configuración de acción personalizada global.
* Los campos de encabezado dinámico y parámetro de consulta se definen como variables en la pantalla de configuración de acciones, no en el recorrido.
* Las políticas de gobernanza de datos y consentimiento se pueden aplicar para evitar que se exporten campos específicos o para excluir a los clientes no consentidos.

**Terminología:**

* Nombre canónico: Acción personalizada — Acrónimo: none — variantes: acciones personalizadas, acción de terceros
* Sinónimos: &quot;parámetros de acción&quot; = &quot;parámetros de mensaje definidos como variables&quot;
* No confunda: &quot;parte de URL estática&quot; (establecida en la configuración de acción global, no editable en el recorrido) ≠ &quot;ruta dinámica&quot; (establecida en el recorrido por ejecución)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Puedo cambiar la dirección URL base de una acción personalizada dentro del recorrido?** — No, solo se puede establecer la parte de ruta dinámica en la recorrido; la parte estática de la dirección URL se configura en la configuración de acción personalizada global.
* **Q: ¿Cómo creo una ruta de URL dinámica que incluya un identificador de perfil?** — Utilice el campo Ruta con el editor de expresiones avanzadas para concatenar el campo Id. con cadenas estáticas, por ejemplo: `_id + '/messages'`.
* **Q: ¿Cómo se aplican las reglas de consentimiento a una acción personalizada?** — Configure políticas de consentimiento en la acción personalizada para excluir a los clientes que no hayan aceptado recibir la comunicación relevante; consulte la página Consentimiento para obtener más detalles.
* **Q: ¿Dónde se asignan los valores para los encabezados dinámicos?** — En la sección Configuración de URL del panel de actividad, haga clic dentro del campo de encabezado dinámico o utilice el icono de lápiz para seleccionar el campo deseado entre eventos o fuentes de datos.
* **Q: ¿Qué tipos de valores puedo asignar a parámetros de acción?** — Puede asignar parámetros a campos de evento, campos de fuente de datos, pasar valores manualmente o utilizar el editor de expresiones avanzadas para la manipulación de datos.

+++
