---
solution: Journey Optimizer
product: journey optimizer
title: Niveles de permisos
description: Obtenga información acerca de los permisos de alto y bajo nivel que permiten a los usuarios acceder a las distintas funciones.
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: permiso, alto nivel, bajo nivel, perfil, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# Niveles de permisos {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Cada perfil de producto está compuesto por permisos que permiten a los usuarios acceder a las diferentes funciones.
Se pueden dividir en dos tipos:

* **Permiso de alto nivel**: representa los diferentes permisos que se pueden asignar a **[!UICONTROL Perfil del producto]** en el [!DNL Admin console], como **[!DNL Publish journeys]** y **[!DNL Manage subdomains delegation]**. Los permisos de alto nivel abarcan permisos de bajo nivel.

* **Permiso de bajo nivel**: representa los diferentes permisos que provienen del permiso de alto nivel.

Por ejemplo, la variable **[!DNL Journey administrator]** el perfil de producto tiene asignado el **[!DNL Manage journeys]** permiso. De este permiso se obtienen los permisos de bajo nivel que permitirán al administrador del Recorrido escribir, leer y eliminar recorridos.

## capacidad de recorrido {#journey-capability}

### [!DNL Manage journeys] permiso {#manage-journeys}

El **[!DNL Manage journeys]** el permiso de alto nivel permite a los usuarios crear Recorridos nuevos y editar/eliminar los existentes, así como acceder a los objetos utilizados en el lienzo de recorrido para crear el flujo de recorrido.

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

### [!DNL Publish journeys] permiso {#publish-journeys}

El **[!DNL Publish journeys]** el permiso de alto nivel permite a los usuarios publicar recorridos.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * journeys.publish
   * journeys.read

### [!DNL View journeys] permiso {#view-journeys}

El **[!DNL View journeys]** el permiso de alto nivel permite a los usuarios examinar y ver los recorridos.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * journeys.read

* Específico de Adobe Experience Platform:
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] permiso {#manage-journeys-events}

El **[!DNL Manage journeys events, data sources and actions]** el permiso de alto nivel permite a los usuarios configurar configuraciones de datos y eventos.

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

### [!DNL View journeys events, data sources and actions] permiso {#view-journeys-event}

El **[!DNL View journeys events, data sources and actions]** el permiso de alto nivel permite a los usuarios utilizar eventos y datos en el flujo de recorrido.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * recorrido_events.read
   * recorrido_data_sources.read
   * recorrido_actions.read

* Específico de Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] permiso {#view-journeys-report}

El **[!DNL View journeys report]** el permiso de alto nivel permite a los usuarios crear informes de recorrido de solo lectura.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * recorrido_report.read
   * messages_report.read

* Específico de Adobe Experience Platform:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Capacidad de administración de decisiones {#decisions-permissions}

### [!DNL Manage decisions] permiso {#manage-decisioning}

El **[!DNL Manage decisions]** el permiso de alto nivel permite a los usuarios crear nuevos y editar/eliminar los existentes **[!DNL Activity entities]**, así como administrar los objetos que se utilizan en esas actividades para tomar las decisiones.

Incluye los siguientes permisos de bajo nivel:

* Específico para la gestión de decisiones:
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

### [!DNL View decisions] permiso {#view-decisions}

El **[!DNL View decisions]** El permiso de alto nivel permite a los usuarios utilizar una actividad existente y objetos empresariales relacionados para tomar las decisiones.

Incluye los siguientes permisos de bajo nivel:

* Específico para la gestión de decisiones:
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

### [!DNL Publish offers decisioning] permiso {#publish-decisions}

El **[!DNL Publish offers decisioning]** el permiso de alto nivel permite a los usuarios acceder para aprobar o desaprobar actividades de oferta.

Incluye los siguientes permisos de bajo nivel:

* Específico para la gestión de decisiones:
   * offers_activity.read
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

### [!DNL Manage ranking strategies] permiso {#manage-ranking-strategies}

El **[!DNL Manage ranking strategies]** el permiso de alto nivel permite a los usuarios leer, crear, editar y eliminar estrategias de clasificación.

Incluye los siguientes permisos de bajo nivel:

* Específico para la gestión de decisiones:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Capacidad de administración {#administration-permissions}

### [!DNL Manage subdomains delegation] permiso {#manage-subdomain}

El **[!DNL Manage subdomains delegation]** el permiso de alto nivel permite a los usuarios crear, editar y eliminar delegaciones de subdominios (incluido el grupo de IP).

Incluye los siguientes permisos de bajo nivel:

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] permiso {#manage-ptr}

El **[!DNL Manage PTR records]** El permiso de alto nivel permite a los usuarios leer y editar registros PTR configurados en función del subdominio.

Incluye los siguientes permisos de bajo nivel:

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] permiso {#view-ptr}

El **[!DNL View PTR records]** el permiso de alto nivel permite a los usuarios ver los registros PTR que se han configurado en función del subdominio.

Incluye los siguientes permisos de bajo nivel:

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] permiso {#manage-ip-pools}

El **[!DNL Manage IP pools]** el permiso de alto nivel permite a los usuarios crear, editar y eliminar la definición de afinidad.

Incluye los siguientes permisos de bajo nivel:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

<!--
### [!DNL Manage messages general settings] permission {#manage-message-settings}

The **[!DNL Manage messages general settings]** high-level permission allows users to create, edit and delete global settings at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages_general_settings.read
  * messages_general_settings.write
  * messages_general_settings.delete
* Adobe Experience Platform specific:
  * schemas.read

### [!DNL View messages general settings] permission {#view-message-settings}

The **[!DNL View messages general settings]** high-level permission allows users to view messages general settings such as the execution address.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages_general_settings.read
* Adobe Experience Platform specific: 
  * schemas.read
-->

### [!DNL Manage channel surface] permiso {#manage-channel-surface}

El **[!DNL Manage channel surface]** el permiso de alto nivel permite a los usuarios crear, editar y eliminar superficies de canal entre canales en el nivel de zona protegida.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (de Adobe Experience Platform Launch)

### [!DNL View channel surface] permiso {#view-channel-surface}

El **[!DNL View channel surface]** el permiso de alto nivel permite a los usuarios ver las superficies de canal para saber qué superficies de canal utilizar.

Incluye los siguientes permisos de bajo nivel:

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (de la recopilación de datos de Adobe Experience Platform)

### [!DNL Manage suppression] permiso {#manage-suppression}

El **[!DNL Manage suppression]** el permiso de alto nivel permite a los usuarios definir el número de rechazos antes de añadir una dirección de correo electrónico a la lista de supresión, así como añadir y eliminar entradas en la lista de supresión.

Incluye los siguientes permisos de bajo nivel:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] permiso {#view-suppression-list}

El **[!DNL View suppression list]** el permiso de alto nivel permite a los usuarios ver el contenido y la configuración de la lista de supresión.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * suppression_list.view

* Específico de Adobe Experience Platform:
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] permiso {#export-suppression-list}

El **[!DNL Export suppression list]** El permiso de alto nivel permite a los usuarios descargar la lista de supresión como archivo CSV.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * suppression_list.export

* Específico de Adobe Experience Platform:
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] permiso {#manage-landing-page-settings}

El **[!DNL Manage landing page settings]** el permiso de alto nivel permite a los usuarios leer, crear y editar subdominios de páginas de aterrizaje y ajustes preestablecidos.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### [!DNL Manage frequency rules] permiso {#manage-frequency-rules}

El **[!DNL Manage frequency rules]** el permiso de alto nivel permite a los usuarios leer, crear, editar, eliminar y activar/desactivar reglas de frecuencia.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### [!DNL View frequency rules] permiso {#view-frequency-rules}

El **[!DNL View frequency rules]** el permiso de alto nivel permite a los usuarios ver las reglas de frecuencia.

Incluye los siguientes permisos de bajo nivel:

* Específico de Journey Optimizer:
   * frequency_rules.read
