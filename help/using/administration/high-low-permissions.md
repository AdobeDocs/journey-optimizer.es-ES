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
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Grupos de control
topic: Administración
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 0%

---

# Niveles de permisos {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Cada perfil de producto está compuesto por permisos que permiten a los usuarios acceder a las diferentes funciones.
Se pueden dividir en dos tipos:

* **Permiso** de alto nivel: representa los diferentes permisos que se pueden asignar a  **[!UICONTROL Product profile]** en  [!DNL Admin console], como  **[!UICONTROL Publish journeys]** y  **[!UICONTROL Manage subdomains delegation]**. Los permisos de alto nivel comprenden permisos de bajo nivel.

* **Permiso** de bajo nivel: representa los diferentes permisos que provienen del permiso de alto nivel.

Por ejemplo, al perfil de producto **[!UICONTROL Journey administrator]** se le asigna el permiso **[!UICONTROL Manage journeys]**. A partir de este permiso, se obtienen los permisos de bajo nivel que permiten al administrador de Recorrido escribir, leer y eliminar recorridos.

## Recorrido {#journey-capability}

### Permiso Administrar recorridos {#manage-journeys}

El permiso **[!UICONTROL Manage journeys]** de alto nivel permite a los usuarios crear Recorridos nuevos y editar o eliminar, así como acceder a los objetos que se utilizan en el lienzo de recorrido para crear el flujo de recorrido.

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

El permiso **[!UICONTROL Publish journeys]** de alto nivel permite a los usuarios publicar recorridos.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * journeys.publish
   * journeys.read

### Ver permiso de recorridos {#view-journeys}

El permiso **[!UICONTROL View journeys]** de alto nivel permite a los usuarios examinar y ver los recorridos.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * journeys.read

* Específico de Adobe Experience Platform:
   * segments.read
   * profiles.read

### Administrar eventos de recorrido, fuentes de datos y permisos de acciones {#manage-journeys-events}

El permiso **[!UICONTROL Manage journeys events, data sources and actions]** de alto nivel permite a los usuarios configurar configuraciones de datos y eventos.

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

El permiso **[!UICONTROL View journeys events, data sources and actions]** de alto nivel permite a los usuarios utilizar eventos y datos en el flujo de recorrido.

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

El permiso **[!UICONTROL View journeys report]** de alto nivel permite a los usuarios crear informes de recorrido de solo lectura.

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

El permiso **[!UICONTROL Manage messages]** de alto nivel permite a los usuarios crear, editar o eliminar mensajes.

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

El permiso **[!UICONTROL Manage messages preview and test]** de alto nivel permite a los usuarios previsualizar mensajes personalizados.

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

El permiso **[!UICONTROL Publish messages]** de alto nivel permite a los usuarios publicar mensajes.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages.publish

* Específico de Adobe Experience Platform:
   * profiles.read
   * schemas.read
   * datasets.read

### Ver permisos de mensajes {#view-messages}

El permiso **[!UICONTROL View messages]** de alto nivel permite a los usuarios leer solo mensajes.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages.read
   * messages_presets.read

* Específico de Adobe Experience Platform:
   * schemas.read
   * segments.read

### Ver permisos del informe de mensajes {#view-message-reports}

El permiso **[!UICONTROL View messages report]** de alto nivel permite a los usuarios enviar correos electrónicos de solo lectura e informes push.

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

El permiso **[!UICONTROL Manage decisions]** de alto nivel permite a los usuarios crear y editar y eliminar los **[!UICONTROL Activity entities]** existentes, así como administrar los objetos que se utilizan en esas actividades para tomar las decisiones.

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

El permiso **[!UICONTROL View decisions]** de alto nivel permite a los usuarios utilizar una actividad existente y objetos empresariales relacionados para tomar las decisiones.

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

El permiso **[!UICONTROL Publish offers decisioning]** de alto nivel permite a los usuarios acceder a las actividades de oferta de aprobación o desaprobación.

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

El permiso **[!UICONTROL Manage ranking strategies]** de alto nivel permite a los usuarios leer, crear, editar y eliminar informes de mensajes personalizados y utilizar funciones de acción.

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

El permiso **[!UICONTROL Manage subdomains delegation]** de alto nivel permite a los usuarios crear, editar y eliminar la delegación de subdominios (incluido el grupo de IP).

Incluye los siguientes permisos de bajo nivel:

* subdominios_delegation.read
* subdominios_delegación.write
* subdominios_delegación.delete

### Ver permiso de registros PTR {#view-ptr}

El permiso **[!UICONTROL View PTR records]** de alto nivel permite a los usuarios ver los registros PTR que se han configurado en función del subdominio e incluye los siguientes permisos de bajo nivel:

* PTR_records.read
* subdominios_delegation.read

### Permiso Administrar grupos de IP {#manage-ip-pools}

El permiso **[!UICONTROL Manage IP pools]** de alto nivel permite a los usuarios crear, editar y eliminar la definición de afinidad.

Incluye los siguientes permisos de bajo nivel:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### Administrar mensajes, permiso de configuración general {#manage-message-settings}

El permiso **[!UICONTROL Manage messages general settings]** de alto nivel permite a los usuarios crear, editar y eliminar la configuración global en el nivel de entorno limitado.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete

* Específico de Adobe Experience Platform:
   * schemas.read

### Ver mensajes, permiso de configuración general {#view-message-settings}

El permiso **[!UICONTROL View messages general settings]** de alto nivel permite a los usuarios ver los mensajes en la configuración general, como las reglas de supresión o la dirección de ejecución.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages_general_settings.read
* Específico de Adobe Experience Platform:
   * schemas.read

### Permiso Administrar ajustes preestablecidos de mensajes {#manage-message-presets}

El permiso **[!UICONTROL Manage messages presets]** de alto nivel permite a los usuarios crear, editar y eliminar ajustes preestablecidos de mensaje en todos los canales a nivel de entorno limitado.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdominios_delegation.read
   * IP_pools.read
   * mobile_setting.read (de Adobe Experience Platform Launch)

### Ver permisos preestablecidos de mensajes {#view-message-presets}

El permiso **[!UICONTROL View messages presets]** de alto nivel permite a los usuarios ver los ajustes preestablecidos de mensaje para saber qué mensajes utilizar al crear un mensaje.

Incluye los siguientes permisos de bajo nivel:

* messages_presets.read
* subdominios_delegation.read
* IP_pools.read
* mobile_setting.read (de Adobe Experience Platform Launch)

### Permiso Administrar reglas de supresión {#manage-suppression-rules}

El permiso de alto nivel **[!UICONTROL Manage suppression rules]** permite a los usuarios definir el número de devoluciones antes de que la dirección de correo electrónico del usuario se añada a la lista de supresión.

Incluye los siguientes permisos de bajo nivel:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete

### Ver permiso de la lista de supresión {#view-suppresion-list}

El permiso **[!UICONTROL View suppression list]** de alto nivel permite a los usuarios ver las configuraciones de los mensajes, incluidos los ajustes preestablecidos de mensajes y la configuración general de mensajes.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * suppression_list.view
* Específico de Adobe Experience Platform:
   * profiles.read
   * datasets.read

### Permiso de la lista de supresión de exportación {#export-suppression-list}

El permiso **[!UICONTROL Export suppression list]** de alto nivel permite a los usuarios configurar los mensajes, incluidos los ajustes preestablecidos de mensaje y la configuración general de mensajes.

Incluye los siguientes permisos de bajo nivel:

* Específico de Adobe Experience Platform:
   * profiles.read
   * datasets.read
