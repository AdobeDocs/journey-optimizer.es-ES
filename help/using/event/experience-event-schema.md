---
solution: Journey Optimizer
product: journey optimizer
title: Esquemas de ExperienceEvent para eventos de recorrido
description: Obtenga información sobre los esquemas de ExperienceEvent para eventos de recorrido
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: esquemas, XDM, plataforma, flujo, ingesta, recorrido
exl-id: f19749c4-d683-4db6-bede-9360b9610eef
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 1%

---

# Esquemas de ExperienceEvent para [!DNL Journey Optimizer] Eventos {#about-experienceevent-schemas}

[!DNL Journey Optimizer] Los eventos son eventos de experiencia XDM que se envían a Adobe Experience Platform mediante la ingesta de flujos.

Como tal, un requisito previo importante para configurar eventos para [!DNL Journey Optimizer] Esto le indica que está familiarizado con el modelo de datos de Experience de Adobe Experience Platform (o XDM) y con cómo componer esquemas de evento de Experience XDM, así como con cómo transmitir datos con formato XDM a Adobe Experience Platform.

## Requisitos de esquema para [!DNL Journey Optimizer] Eventos  {#schema-requirements}

El primer paso para configurar un evento de [!DNL Journey Optimizer] es garantizar que tiene un esquema XDM definido para representar el evento y un conjunto de datos creado para registrar instancias del evento en Adobe Experience Platform. Tener un conjunto de datos para los eventos no es estrictamente necesario, pero enviar los eventos a un conjunto de datos específico le permitirá mantener el historial de eventos de los usuarios para referencias y análisis futuros, por lo que siempre es una buena idea. Si aún no tiene un esquema y un conjunto de datos adecuados para su evento, ambas tareas se pueden realizar en la interfaz web de Adobe Experience Platform.

![](assets/schema1.png)

Cualquier esquema XDM que se vaya a utilizar para [!DNL Journey Optimizer] Los eventos de deben cumplir los siguientes requisitos:

* El esquema debe ser de la clase XDM ExperienceEvent.

  ![](assets/schema2.png)

* Para los eventos generados por el sistema, el esquema debe incluir el grupo de campos eventID de orquestación. [!DNL Journey Optimizer] utiliza este campo para identificar eventos utilizados en recorridos.

  ![](assets/schema3.png)

* Declare un campo de identidad para identificar perfiles individuales en el evento. Si no se especifica ninguna identidad, se puede utilizar un mapa de identidad. Este proceso no es recomendable.

  ![](assets/schema4.png)

* Si desea que estos datos estén disponibles para la búsqueda más adelante en un Recorrido, marque el esquema y el conjunto de datos para el perfil.

  ![](assets/schema5.png)

  ![](assets/schema6.png)

* No dude en incluir campos de datos para capturar cualquier otro dato de contexto que desee incluir en el evento, como información sobre el usuario, el dispositivo desde el que se generó el evento, la ubicación o cualquier otra circunstancia significativa relacionada con el evento.

  ![](assets/schema7.png)

  ![](assets/schema8.png)

## Aprovechamiento de las relaciones de esquema{#leverage_schema_relationships}

Adobe Experience Platform permite definir relaciones entre esquemas para utilizar un conjunto de datos como una tabla de búsqueda para otro.

Supongamos que el modelo de datos de marca tiene un esquema que captura las compras. También tiene un esquema para el catálogo de productos. Puede capturar el ID de producto en el esquema de compra y utilizar una relación para buscar detalles de producto más completos en el catálogo de productos. Esto le permite crear una audiencia para todos los clientes que compraron un portátil, por ejemplo, sin tener que enumerar explícitamente todos los ID de portátil ni capturar todos los detalles del producto en sistemas transaccionales.

Para definir una relación, debe tener un campo dedicado en el esquema de origen, en este caso el campo ID de producto en el esquema de compra. Este campo debe hacer referencia al campo de ID de producto en el esquema de destino. Las tablas de origen y destino deben estar habilitadas para los perfiles y el esquema de destino debe tener ese campo común definido como su identidad principal.

Este es el esquema del catálogo de productos habilitado para el perfil con el ID de producto definido como identidad principal.

![](assets/schema9.png)

Este es el esquema de compra con la relación definida en el campo ID de producto.

![](assets/schema10.png)

>[!NOTE]
>
>Obtenga más información sobre las relaciones de esquema en la [Documentación del Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/configure-relationships-between-schemas.html?lang=es).

En Journey Optimizer, puede aprovechar todos los campos de las tablas vinculadas:

* al configurar un evento empresarial o unitario, [Más información](../event/experience-event-schema.md#unitary_event_configuration)
* cuando se utilizan condiciones en un recorrido, [Más información](../event/experience-event-schema.md#journey_conditions_using_event_context)
* en la personalización de mensajes, [Más información](../event/experience-event-schema.md#message_personalization)
* en la personalización de acciones personalizadas, [Más información](../event/experience-event-schema.md#custom_action_personalization_with_journey_event_context)

### Matrices{#relationships_limitations}

Puede definir una relación de esquema en una matriz de cadenas como, por ejemplo, una lista de ID de productos.

![](assets/schema15.png)

Sin embargo, no se puede definir una relación de esquema con un atributo dentro de una matriz de objetos; por ejemplo, una lista de información de compra (ID de producto, nombre de producto, precio, descuento). Los valores de búsqueda no estarán disponibles en recorridos (condiciones, acciones personalizadas, etc.) y personalización de mensajes.

![](assets/schema16.png)

### Configuración de eventos{#unitary_event_configuration}

Los campos de esquema vinculados están disponibles en la configuración de eventos unitarios y empresariales:

* al navegar por los campos de esquema de evento en la pantalla de configuración de evento.
* al definir una condición para eventos generados por el sistema.

![](assets/schema11.png)

Los campos vinculados no están disponibles:

* en la fórmula de clave de evento
* en la condición de id de evento (eventos basados en reglas)

Para aprender a configurar un evento unitario, consulte [página](../event/about-creating.md).

### Condiciones de recorrido que utilizan el contexto de evento{#journey_conditions_using_event_context}

Puede utilizar datos de una tabla de búsqueda vinculada a un evento utilizado en un recorrido para la creación de condiciones (editor de expresiones).

Añada una condición en un recorrido, edite la expresión y despliegue el nodo de evento en el editor de expresiones.

![](assets/schema12.png)

Para aprender a definir las condiciones de recorrido, consulte esta sección [página](../building-journeys/condition-activity.md).

### Personalización de mensajes{#message_personalization}

Los campos vinculados están disponibles al personalizar un mensaje. Los campos relacionados se muestran en el contexto que se pasa del recorrido al mensaje.

![](assets/schema14.png)

Para aprender a personalizar un mensaje con información de recorrido contextual, consulte esta sección [página](../personalization/personalization-use-case.md).

### Personalización de acciones personalizadas con contexto de evento de recorrido{#custom_action_personalization_with_journey_event_context}

Los campos vinculados están disponibles al configurar los parámetros de acción de una actividad de acción personalizada de recorrido.

![](assets/schema13.png)

Para aprender a utilizar acciones personalizadas, consulte esta sección [página](../building-journeys/using-custom-actions.md).
