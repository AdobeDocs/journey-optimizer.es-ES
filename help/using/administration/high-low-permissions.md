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
source-git-commit: 8db5ae5b3cbef245dfe7cd11a95355c072bc3ef8
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 0%

---

# Niveles de permisos {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Cada función está compuesta por permisos que permiten a los usuarios acceder a las distintas funciones.
Se pueden dividir en dos tipos:

* **Permiso de alto nivel**: representa los diferentes permisos que se pueden asignar a **[!UICONTROL Rol]**, como **[!DNL Publish journeys]** y **[!DNL Manage subdomains delegation]**. Los permisos de alto nivel abarcan permisos de bajo nivel. Los permisos de alto nivel se detallan en [esta página](ootb-permissions.md).

* **Permiso de bajo nivel**: representa los diferentes permisos que provienen del permiso de alto nivel.

Por ejemplo, la variable **[!DNL Journey administrator]** La función tiene asignada la función **[!DNL Manage journeys]** permiso. De este permiso se obtienen los permisos de bajo nivel que permitirán al administrador del Recorrido escribir, leer y eliminar recorridos.

## recurso de recorrido {#journey-capability}

* **[!DNL Manage journeys]** el permiso de alto nivel permite a los usuarios crear Recorridos nuevos y editar/eliminar los existentes, así como acceder a los objetos utilizados en el lienzo de recorrido para crear el flujo de recorrido.

+++ Incluye los siguientes permisos de bajo nivel:

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

* **[!DNL Publish journeys]** el permiso de alto nivel permite a los usuarios publicar recorridos.

+++ Incluye los siguientes permisos de bajo nivel:
   * Específico de Journey Optimizer:
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]** el permiso de alto nivel permite a los usuarios examinar y ver los recorridos.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * journeys.read

   * Específico de Adobe Experience Platform:
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]** el permiso de alto nivel permite a los usuarios configurar configuraciones de datos y eventos.

+++ Incluye los siguientes permisos de bajo nivel:

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

* **[!DNL View journeys events, data sources and actions]** el permiso de alto nivel permite a los usuarios utilizar eventos y datos en el flujo de recorrido.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * recorrido_events.read
      * recorrido_data_sources.read
      * recorrido_actions.read

   * Específico de Adobe Experience Platform:
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys report]** el permiso de alto nivel permite a los usuarios crear informes de recorrido de solo lectura.

+++ Incluye los siguientes permisos de bajo nivel:

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

* **[!DNL Manage frequency rules]** el permiso de alto nivel permite a los usuarios leer, crear, editar, eliminar y activar/desactivar reglas de frecuencia.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** el permiso de alto nivel permite a los usuarios ver las reglas de frecuencia.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * frequency_rules.read

+++

## Recurso de campaña {#campaign-capability}

* **[!DNL Export suppression list]** El permiso de alto nivel permite a los usuarios descargar la lista de supresión como archivo CSV.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * suppression_list.export

   * Específico de Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage campaigns]** El permiso de alto nivel permite a los usuarios crear nuevas campañas y editarlas o eliminarlas

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* **[!DNL Publish campaigns]** el permiso de alto nivel permite a los usuarios publicar campañas.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:

      * campaign-read
      * campaign-publish
        <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]** el permiso de alto nivel permite a los usuarios leer y editar el informe de campañas.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## Recurso de gestión de decisiones {#decisions-permissions}

* **[!DNL Manage decisions]** el permiso de alto nivel permite a los usuarios crear nuevos y editar/eliminar los existentes **[!DNL Activity entities]**, así como administrar los objetos que se utilizan en esas actividades para tomar las decisiones.

+++ Incluye los siguientes permisos de bajo nivel:

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

* **[!DNL View decisions]** El permiso de alto nivel permite a los usuarios utilizar una actividad existente y objetos empresariales relacionados para tomar las decisiones.

+++ Incluye los siguientes permisos de bajo nivel:

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

+++

* **[!DNL Manage offers]** el permiso de alto nivel permite a los usuarios crear, editar y eliminar todas las ofertas, componentes, decisiones de lectura y colecciones.

+++ Incluye los siguientes permisos de bajo nivel:

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

* **[!DNL Manage ranking strategies]** el permiso de alto nivel permite a los usuarios leer, crear, editar y eliminar estrategias de clasificación.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico para la gestión de decisiones:
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

+++

## Recurso de configuraciones de canal {#administration-permissions}

* **[!DNL Manage IP pools]** el permiso de alto nivel permite a los usuarios crear, editar y eliminar la definición de afinidad.

+++ Incluye los siguientes permisos de bajo nivel:
   * Específico de Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage landing page settings]** el permiso de alto nivel permite a los usuarios leer, crear y editar subdominios de páginas de aterrizaje y ajustes preestablecidos.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* **[!DNL Manage messages general settings]** el permiso de alto nivel permite a los usuarios crear, editar y eliminar la configuración global en el nivel de zona protegida.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Específico de Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL Manage messages presets]** el permiso de nivel superior permite a los usuarios leer, crear, editar y eliminar superficies de canal entre canales en el nivel de zona protegida.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * Específico de la recopilación de datos:
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

+++

* **[!DNL Manage PTR records]** El permiso de alto nivel permite a los usuarios leer y editar registros PTR configurados en función del subdominio.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL Manage Seedlist]** El permiso de alto nivel permite a los usuarios leer, crear, editar y eliminar Seedlist.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* **[!DNL Manage SMS subdomains]** El permiso de alto nivel permite a los usuarios leer, crear, editar y eliminar subdominios SMS.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

+++

* **[!DNL Manage subdomains delegations]** el permiso de alto nivel permite a los usuarios crear, editar y eliminar delegaciones de subdominios (incluido el grupo de IP).

+++ Incluye los siguientes permisos de bajo nivel:
   * Específico de Journey Optimizer:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage suppression]** el permiso de alto nivel permite a los usuarios definir el número de rechazos antes de añadir una dirección de correo electrónico a la lista de supresión, así como añadir y eliminar entradas en la lista de supresión.

+++ Incluye los siguientes permisos de bajo nivel:
   * Específico de Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View PTR records]** el permiso de alto nivel permite a los usuarios ver los registros PTR que se han configurado en función del subdominio.

+++ Incluye los siguientes permisos de bajo nivel:
   * Específico de Journey Optimizer:

      * PTR_records.read
      * subdomains_delegation.read

+++

* **[!DNL View messages general settings]** el permiso de alto nivel permite a los usuarios ver los mensajes en la configuración general, como la dirección de ejecución.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * messages_general_settings.read

   * Específico de Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL View messages presets]** el permiso de alto nivel permite a los usuarios ver los ajustes preestablecidos de mensajes.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * Específico de la recopilación de datos:
      * Mobile_setting.read

+++
<!--
### [!DNL View channel surface] permission {#view-channel-surface}

The **[!DNL View channel surface]** high-level permission allows users to view channel surfaces in order to know which channel surfaces to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* **[!DNL View suppression list]** el permiso de alto nivel permite a los usuarios ver el contenido y la configuración de la lista de supresión.

+++ Incluye los siguientes permisos de bajo nivel:

   * Específico de Journey Optimizer:
      * suppression_list.view

   * Específico de Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

