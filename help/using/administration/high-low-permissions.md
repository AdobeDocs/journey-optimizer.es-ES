---
solution: Journey Optimizer
product: journey optimizer
title: Niveles de permisos
description: Obtenga información acerca de los permisos de alto y bajo nivel que permiten a los usuarios acceder a las distintas funciones.
topic: Administration
feature: Access Management
role: Admin, Architect, Developer
level: Experienced
keywords: permiso, alto nivel, bajo nivel, perfil, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 2a5db6950ac82fd18deb2e4009c9a43247444d6a
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Niveles de permisos {#high-low-permissions}


Cada función está compuesta por permisos que permiten a los usuarios acceder a las distintas funciones.

Se pueden dividir en dos tipos:

* **Permiso de alto nivel**: representa los diferentes permisos que se pueden asignar a **[!UICONTROL Rol]**, como **[!DNL Publish journeys]** y **[!DNL Manage subdomains delegation]**. Los permisos de alto nivel abarcan permisos de bajo nivel. Los permisos de alto nivel se detallan en [esta página](ootb-permissions.md).

* **Permiso de bajo nivel**: representa los diferentes permisos que provienen del permiso de alto nivel.

Por ejemplo, el rol **[!DNL Journey administrator]** tiene asignado el permiso **[!DNL Manage journeys]**. De este permiso se obtienen los permisos de bajo nivel que permitirán al administrador del Recorrido escribir, leer y eliminar recorridos.

![](assets/do-not-localize/permissions.png){width="70%"}


## recurso de recorrido {#journey-capability}

* El permiso de alto nivel **[!DNL Manage journeys]** permite a los usuarios crear Recorridos nuevos y editar/eliminar/detener/pausar los existentes, así como el acceso a los objetos que se utilizan en el lienzo de recorrido para generar el flujo de recorrido.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

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

  +++

* El permiso de alto nivel **[!DNL Publish journeys]** permite a los usuarios publicar recorridos.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  
   * Específico de Journey Optimizer:
      * journeys.publish
      * journeys.read

  +++

* El permiso de alto nivel **[!DNL View journeys]** permite a los usuarios examinar y ver recorridos.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:
      * journeys.read

   * Específico de Adobe Experience Platform:
      * segments.read
      * profiles.read

  +++

* El permiso de alto nivel **[!DNL Manage journeys events, data sources and actions]** permite a los usuarios configurar configuraciones de datos y eventos.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

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

  +++

* El permiso de alto nivel **[!DNL View journeys events, data sources and actions]** permite a los usuarios utilizar eventos y datos en el flujo de recorrido.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:
      * recorrido_events.read
      * recorrido_data_sources.read
      * recorrido_actions.read

   * Específico de Adobe Experience Platform:
      * schemas.read
      * datasets.read
      * identity_namespace.read

  +++

* El permiso de alto nivel **[!DNL View journeys report]** permite a los usuarios generar un informe de recorrido de solo lectura.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:
      * recorrido_report.read
      * messages_report.read

   * Específico de Adobe Experience Platform:
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

  +++

## recurso de reglas de Journey Optimizer {#journey-rules-capability}

* El permiso de alto nivel **[!DNL Manage frequency rules]** permite a los usuarios leer, crear, editar, eliminar y activar o desactivar reglas de frecuencia.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

  +++

* El permiso de alto nivel **[!DNL View frequency rules]** permite a los usuarios ver reglas de frecuencia.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:
      * frequency_rules.read

  +++

## Recurso de campaña {#campaign-capability}

* El permiso de alto nivel **[!DNL Export suppression list]** permite a los usuarios descargar la lista de supresión como archivo CSV.

  +++ Este permiso incluye los siguientes permisos de bajo nivel: 

   * Específico de Journey Optimizer:
      * suppression_list.export

   * Específico de Adobe Experience Platform:
      * profiles.read
      * datasets.read

  +++

* El permiso de alto nivel **[!DNL Manage campaigns]** permite a los usuarios crear nuevas campañas y editarlas o eliminarlas

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

  +++

* El permiso de alto nivel **[!DNL Publish campaigns]** permite a los usuarios publicar campañas.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:

      * campaign-read
      * campaign-publish
        <!--* experiments.activate-->

  +++

* El permiso de alto nivel **[!DNL View campaigns report]** permite a los usuarios leer y editar el informe de campañas.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

  +++

## Recurso de gestión de decisiones {#decisions-permissions}

* El permiso de alto nivel **[!DNL Manage decisions]** permite a los usuarios crear, editar o eliminar **[!DNL Activity entities]** nuevos y administrar los objetos que se usan en esas actividades para tomar las decisiones.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

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

  +++

* El permiso de alto nivel **[!DNL View decisions]** permite a los usuarios utilizar una actividad existente y objetos empresariales relacionados para tomar las decisiones.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico para la gestión de decisiones:
      * activities.read
      * offers.read
      * placements.read
      * ranking_strategy.read

   * Específico de Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read

  +++

* El permiso de alto nivel **[!DNL Manage offers]** permite a los usuarios crear, editar y eliminar todas las ofertas, componentes, decisiones de lectura y colecciones.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico para la gestión de decisiones:
      * offers_activity.read
      * offers.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * ranking_strategy.read

   * Específico de Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

  +++

* El permiso de alto nivel **[!DNL Manage ranking strategies]** permite a los usuarios leer, crear, editar y eliminar estrategias de clasificación.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico para la gestión de decisiones:
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

  +++

## Recurso de configuraciones de canal {#administration-permissions}

<!--
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Decisioning entities.

  +++ This permission includes the following low-level permissions:  

  * Experience decisions specific:
    * ranking_strategy.read
    * offeritem.read
    * offeritem.write
    * offeritem.delete
    * itemCollection.read
    * itemCollection.write
    * itemCollection.delete
    * SelectionStrategy.read
    * SelectionStrategy.write
    * SelectionStrategy.delete
    * Decisionpolicy.read
    * Decisionpolicy.write
    * Decisionpolicy.delete
  +++
-->

* El permiso de alto nivel **[!DNL Manage file routing]** permite a los usuarios crear, editar y eliminar configuraciones de enrutamiento de archivos.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  
   * Específico de Journey Optimizer:

      * file_routing.read
      * file_routing.write
      * file_routing.delete

  +++

* El permiso de alto nivel **[!DNL Manage IP pools]** permite a los usuarios crear, editar y eliminar la definición de afinidad.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  
   * Específico de Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

  +++

* El permiso de alto nivel **[!DNL Manage landing page settings]** permite a los usuarios leer, crear y editar subdominios de páginas de aterrizaje y ajustes preestablecidos.

  +++ Este permiso incluye los siguientes permisos de bajo nivel: 

   * Específico de Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

  +++

* El permiso de alto nivel **[!DNL Manage messages general settings]** permite a los usuarios crear, editar y eliminar la configuración global en el nivel de zona protegida.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Específico de Adobe Experience Platform:
      * schemas.read

  +++

* El permiso de alto nivel **[!DNL Manage messages presets]** permite a los usuarios leer, crear, editar y eliminar configuraciones de canal en varios canales en el nivel de zona protegida.

  +++ Este permiso incluye los siguientes permisos de bajo nivel: 

   * Específico de Journey Optimizer:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * Específico de la recopilación de datos:
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

  +++

* El permiso de alto nivel **[!DNL Manage PTR records]** permite a los usuarios leer y editar registros PTR que se hayan configurado en función del subdominio.

  +++ Este permiso incluye los siguientes permisos de bajo nivel: 

   * Específico de Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

  +++

* El permiso de alto nivel **[!DNL Manage Seedlist]** permite a los usuarios leer, crear, editar y eliminar Seedlist.

  +++ Este permiso incluye los siguientes permisos de bajo nivel: 

   * Específico de Journey Optimizer:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

  +++

* El permiso de alto nivel **[!DNL Manage SMS subdomains]** permite a los usuarios leer, crear, editar y eliminar subdominios de SMS.

  +++ Este permiso incluye los siguientes permisos de bajo nivel: 

   * Específico de Journey Optimizer:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

  +++

* El permiso de alto nivel **[!DNL Manage subdomains delegations]** permite a los usuarios crear, editar y eliminar delegaciones de subdominios (incluido el grupo de IP).

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  
   * Específico de Journey Optimizer:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

  +++

* El permiso de alto nivel **[!DNL Manage suppression]** permite a los usuarios definir el número de rechazos antes de que se agregue una dirección de correo electrónico a la lista de supresión, así como agregar y eliminar entradas en la lista de supresión.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  
   * Específico de Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

  +++

* El permiso de alto nivel **[!DNL View file routing]** permite a los usuarios ver las configuraciones de enrutamiento de archivos.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  
   * Específico de Journey Optimizer:

      * file_routing.read

  +++

* El permiso de alto nivel **[!DNL View messages general settings]** permite a los usuarios ver los mensajes en la configuración general, como la dirección de ejecución.

  +++ Este permiso incluye los siguientes permisos de bajo nivel: 

   * Específico de Journey Optimizer:
      * messages_general_settings.read

   * Específico de Adobe Experience Platform:
      * schemas.read

  +++

* El permiso de alto nivel **[!DNL View messages presets]** permite a los usuarios ver los ajustes preestablecidos de los mensajes.

  +++ Este permiso incluye los siguientes permisos de bajo nivel: 

   * Específico de Journey Optimizer:
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * Específico de la recopilación de datos:
      * Mobile_setting.read

  +++

* El permiso de alto nivel **[!DNL View PTR records]** permite a los usuarios ver los registros PTR que se han configurado en función del subdominio.

  +++ Este permiso incluye los siguientes permisos de bajo nivel: 
   * Específico de Journey Optimizer:

      * PTR_records.read
      * subdomains_delegation.read

  +++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ This permission includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* El permiso de alto nivel **[!DNL View suppression list]** permite a los usuarios ver el contenido y la configuración de la lista de supresión.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:
      * suppression_list.view

   * Específico de Adobe Experience Platform:
      * profiles.read
      * datasets.read

  +++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ This permission includes the following low-level permissions: 
-->

## recurso de asistencia de IA {#ai-permissions}

* El permiso de alto nivel **[!DNL Generate content]** permite a los usuarios acceder al Asistente para IA en Journey Optimizer.

  +++ Incluye el siguiente permiso de bajo nivel:  

   * Específico de Journey Optimizer:
      * ai-assistant-generated-content.generate

  +++

## Recurso de campaña organizado {#ai-orchestrated-campaign}

* El permiso de alto nivel **[!DNL Manage orchestrated campaigns]** permite a los usuarios crear nuevas campañas orquestadas, editarlas o eliminarlas.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:

      * orchestrated_campaigns.read
      * orchestrated_campaigns.write
      * orchestrated_campaigns.delete
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.write
      * cjm-message.delete
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * cjm-message-preview-test.write
      * experiment.read
      * experiment.write
      * experiment.delete

   * Específico de Adobe Experience Platform:

      * identity-graph.read
      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read
      * sandboxes.view

  +++

* El permiso de alto nivel **[!DNL Manage orchestrated campaigns admin]** permite a los usuarios crear vínculos nuevos y editar/eliminar, así como conciliaciones entre perfiles de Adobe Experience Platform y entidades de almacén relacional.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:

      * cjm-orchestrated-campaign-admin.read
      * cjm-orchestrated-campaign-admin.write
      * cjm-orchestrated-campaign-admin.delete

  +++

* El permiso de alto nivel **[!DNL Publish orchestrated campaigns]** permite a los usuarios publicar campañas orquestadas.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:

      * cjm-orchestrated-campaign.read
      * cjm-orchestrated-campaign.publish
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.publish
      * cjm-library-item.read

   * Específico de Adobe Experience Platform:

      * sandboxes.view

  +++

* El permiso de alto nivel **[!DNL View orchestrated campaigns]** permite a los usuarios ver la campaña organizada y su contenido.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:

      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * experiment.read

   * Específico de Adobe Experience Platform:

      * sandboxes.view
      * segments.read
      * profiles.read

  +++

* El permiso de alto nivel **[!DNL View orchestrated campaigns admin]** permite a los usuarios ver la configuración de administración, pero no puede editarla.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:

      * cjm-orchestrated-campaign-admin.read

  +++

* El permiso de alto nivel **[!DNL View orchestrated campaigns report]** permite a los usuarios ver el rendimiento de las campañas orquestadas en los informes en vivo y empresariales.

  +++ Este permiso incluye los siguientes permisos de bajo nivel:  

   * Específico de Journey Optimizer:

      * cjm-orchestrated-campaign-reports.read
      * cjm-message-report.read
      * cjm-channel-report.read
      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * experiment.read
      * experiment-report.read

   * Específico de Adobe Experience Platform:

      * sandboxes.view
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

  +++
