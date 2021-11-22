---
title: Niveles de permisos
description: Obtenga información sobre permisos de alto y bajo nivel
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: da885bd5e29ff3454fef1c6b362f0e646fe8c39a
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# Niveles de permisos {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Cada perfil de producto está compuesto por permisos que permiten a los usuarios acceder a las diferentes funciones.
Se pueden dividir en dos tipos:

* **Permiso de alto nivel**: representa los diferentes permisos que se pueden asignar a **[!UICONTROL Product profile]** en el [!DNL Admin console], como **[!UICONTROL Publish journeys]** y **[!UICONTROL Manage subdomains delegation]**. Los permisos de alto nivel comprenden permisos de bajo nivel.

* **Permiso de bajo nivel**: representa los diferentes permisos que provienen del permiso de alto nivel.

Por ejemplo, la variable **[!UICONTROL Journey administrator]** al perfil de producto se le asigna la variable **[!UICONTROL Manage journeys]** permiso. A partir de este permiso, se obtienen los permisos de bajo nivel que permiten al administrador de Recorrido escribir, leer y eliminar recorridos.

## Recorrido {#journey-capability}

### Permiso Administrar recorridos {#manage-journeys}

La variable **[!UICONTROL Manage journeys]** los permisos de alto nivel permiten a los usuarios crear Recorridos nuevos, editar o eliminar los existentes, así como acceder a los objetos que se utilizan en el lienzo de recorrido para crear el flujo de recorrido.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Específico de Adobe Experience Platform:

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### Permiso Publicar recorridos {#publish-journeys}

La variable **[!UICONTROL Publish journeys]** permiso de alto nivel permite a los usuarios publicar recorridos.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * journeys.publish
   * journeys.read

### Ver permiso de recorridos {#view-journeys}

La variable **[!UICONTROL View journeys]** los permisos de alto nivel permiten a los usuarios examinar y ver recorridos.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * journeys.read

* Específico de Adobe Experience Platform:
   * segments.read
   * profiles.read

### Administrar eventos de recorrido, fuentes de datos y permisos de acciones {#manage-journeys-events}

La variable **[!UICONTROL Manage journeys events, data sources and actions]** los permisos de alto nivel permiten a los usuarios configurar configuraciones de datos y eventos.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * recorrido_events.read
   * recorrido_events.write
   * recorrido_events.delete
   * recorrido_data_sources.read
   * recorrido_data_sources.write
   * recorrido_data_sources.delete
   * recorrido_actions.read
   * recorrido_actions.write
   * recorrido_actions.delete
* Específico de Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Ver eventos de recorridos, fuentes de datos y permisos de acciones {#view-journeys-event}

La variable **[!UICONTROL View journeys events, data sources and actions]** permiso de alto nivel permite a los usuarios utilizar eventos y datos en el flujo de recorrido.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * recorrido_events.read
   * recorrido_data_sources.read
   * recorrido_actions.read

* Específico de Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Ver permiso del informe recorridos {#view-journeys-report}

La variable **[!UICONTROL View journeys report]** permiso de alto nivel permite a los usuarios crear informes de recorrido de solo lectura.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * recorrido_report.read
   * messages_report.read

* Específico de Adobe Experience Platform:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Capacidad del mensaje {#message-capability}

### Permiso Administrar mensajes {#manage-messages}

La variable **[!UICONTROL Manage messages]** permiso de alto nivel permite a los usuarios crear, editar o eliminar mensajes.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Específico de Adobe Experience Platform:
   * segments.read
   * schemas.read

### Administrar permisos de vista previa y prueba de mensajes {#mange-messages-preview}

La variable **[!UICONTROL Manage messages preview and test]** permiso de alto nivel permite a los usuarios previsualizar mensajes personalizados.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Específico de Adobe Experience Platform:
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policy.read

### Permiso de publicación de mensajes {#publish-messages}

La variable **[!UICONTROL Publish messages]** permiso de alto nivel permite a los usuarios publicar mensajes.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages.publish

* Específico de Adobe Experience Platform:
   * profiles.read
   * schemas.read
   * datasets.read

### Ver permisos de mensajes {#view-messages}

La variable **[!UICONTROL View messages]** permiso de alto nivel permite a los usuarios leer solo mensajes.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages.read
   * messages_presets.read

* Específico de Adobe Experience Platform:
   * schemas.read
   * segments.read

### Ver permisos del informe de mensajes {#view-message-reports}

La variable **[!UICONTROL View messages report]** permiso de alto nivel permite a los usuarios enviar informes push y de correo electrónico de solo lectura.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Capacidad de gestión de decisiones {#decisions-permissions}

### Permiso Administrar decisiones {#manage-decisioning}

La variable **[!UICONTROL Manage decisions]** el permiso de alto nivel permite a los usuarios crear nuevos y editar/eliminar **[!UICONTROL Activity entities]**, así como administrar los objetos que se utilizan en esas actividades para tomar las decisiones.

Incluye los siguientes permisos de bajo nivel:

* Específico de la gestión de decisiones:
   * activities.read
   * activities.write
   * activities.delete
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Específico de Adobe Experience Platform:
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### Ver permisos de decisiones {#view-decisions}

La variable **[!UICONTROL View decisions]** los permisos de alto nivel permiten a los usuarios utilizar una actividad existente y objetos empresariales relacionados para tomar las decisiones.

Incluye los siguientes permisos de bajo nivel:

* Específico de la gestión de decisiones:
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Específico de Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### Publicar ofertas, permiso de decisión {#publish-decisions}

La variable **[!UICONTROL Publish offers decisioning]** permiso de alto nivel permite a los usuarios acceder a para aprobar o desaprobar actividades de oferta.

Incluye los siguientes permisos de bajo nivel:

* Específico de la gestión de decisiones:
   * offer_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Específico de Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### Administrar permisos de estrategias de clasificación {#manage-decisions}

La variable **[!UICONTROL Manage ranking strategies]** los permisos de alto nivel permiten a los usuarios leer, crear, editar y eliminar informes de mensajes personalizados, así como utilizar funciones de acción.

Incluye los siguientes permisos de bajo nivel:

* Específico de la gestión de decisiones:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Capacidad de administración {#administration-permissions}

### Permiso de delegación de subdominios {#manage-subdomain}

La variable **[!UICONTROL Manage subdomains delegation]** los permisos de alto nivel permiten a los usuarios crear, editar y eliminar delegaciones de subdominios (incluido el grupo de IP).

Incluye los siguientes permisos de bajo nivel:

* subdominios_delegation.read
* subdominios_delegación.write
* subdominios_delegación.delete

### Ver permiso de registros PTR {#view-ptr}

La variable **[!UICONTROL View PTR records]** el permiso de alto nivel permite a los usuarios ver los registros PTR que se han configurado en función del subdominio.

Incluye los siguientes permisos de bajo nivel:

* PTR_records.read
* subdominios_delegation.read

### Permiso Administrar grupos de IP {#manage-ip-pools}

La variable **[!UICONTROL Manage IP pools]** el permiso de alto nivel permite a los usuarios crear, editar y eliminar la definición de afinidad.

Incluye los siguientes permisos de bajo nivel:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### Administrar mensajes, permiso de configuración general {#manage-message-settings}

La variable **[!UICONTROL Manage messages general settings]** los permisos de alto nivel permiten a los usuarios crear, editar y eliminar la configuración global en el nivel de entorno limitado.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Específico de Adobe Experience Platform:
   * schemas.read

### Ver mensajes, permiso de configuración general {#view-message-settings}

La variable **[!UICONTROL View messages general settings]** el permiso de alto nivel permite a los usuarios ver los mensajes en la configuración general, como la dirección de ejecución.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages_general_settings.read
* Específico de Adobe Experience Platform:
   * schemas.read

### Permiso Administrar ajustes preestablecidos de mensajes {#manage-message-presets}

La variable **[!UICONTROL Manage messages presets]** los permisos de alto nivel permiten a los usuarios crear, editar y eliminar ajustes preestablecidos de mensaje en todos los canales a nivel de entorno limitado.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdominios_delegation.read
   * IP_pools.read
   * mobile_setting.read (de Adobe Experience Platform Launch)

### Ver permisos preestablecidos de mensajes {#view-message-presets}

La variable **[!UICONTROL View messages presets]** los permisos de alto nivel permiten a los usuarios ver los ajustes preestablecidos de mensaje para saber qué mensajes utilizar al crear un mensaje.

Incluye los siguientes permisos de bajo nivel:

* messages_presets.read
* subdominios_delegation.read
* IP_pools.read
* mobile_setting.read (de Adobe Experience Platform Launch)

### Administrar permiso de supresión {#manage-suppression}

La variable **[!UICONTROL Manage suppression]** el permiso de alto nivel permite a los usuarios definir el número de devoluciones antes de agregar una dirección de correo electrónico a la lista de supresión, así como agregar y eliminar entradas a/desde la lista de supresión.

Incluye los siguientes permisos de bajo nivel:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### Ver permiso de la lista de supresión {#view-suppresion-list}

La variable **[!UICONTROL View suppression list]** permiso de alto nivel permite a los usuarios ver el contenido y la configuración de la lista de supresión.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * suppression_list.view
* Específico de Adobe Experience Platform:
   * profiles.read
   * datasets.read

### Permiso de la lista de supresión de exportación {#export-suppression-list}

La variable **[!UICONTROL Export suppression list]** permiso de alto nivel permite a los usuarios descargar la lista de supresión como archivo CSV.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * suppression_list.export
* Específico de Adobe Experience Platform:
   * profiles.read
   * datasets.read
