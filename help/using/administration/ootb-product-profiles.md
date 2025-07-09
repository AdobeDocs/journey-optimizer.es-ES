---
solution: Journey Optimizer
product: journey optimizer
title: Funciones integradas de Journey Optimizer
description: Obtenga información sobre las funciones integradas
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: permisos, creación, mensajes
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: e20db7c39e751bf720cd0ae75b4e8f031de18eef
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 7%

---

# Funciones integradas {#ootb-product-profiles}

Las funciones integradas son un conjunto de derechos unitarios que permiten a los usuarios acceder a determinadas funcionalidades u objetos de la interfaz. Consulte [esta página](ootb-permissions.md) para ver la lista de permisos disponibles para crear su función.

## [!DNL Content Library Manager] {#content-library-manager}

El rol **[!DNL Content Library Manager]** solo permite el acceso al menú **[!UICONTROL Plantillas de contenido]**. Los usuarios asignados a esta función solo podrán acceder a la biblioteca de plantillas para crear contenido sin acceder a los recorridos o campañas.

Este permiso incluye los siguientes permisos:

| Capacidad | Permisos |
|-|-|
| Biblioteca de Journey Optimizer | <ul><li>**[!DNL Manage library items]**: leer, crear, editar y eliminar elementos de la biblioteca Journey Optimizer, incluidas plantillas de contenido y fragmentos.</li><li>**[!DNL Manage simulate content]**: acceso a la opción **[!UICONTROL Simular contenido]** para vista previa y revisión.</li><li>**[!DNL Publish Fragment]**: publicar fragmentos de contenido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y usar características de acción.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL View datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL View schemas]**: acceso de solo lectura a esquemas.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

El rol **[!DNL Decisioning manager]** solo permite el acceso al menú **[!UICONTROL Administración de decisiones]**. Los usuarios asignados a esta función solo podrán administrar, ver y publicar decisiones.

Este permiso incluye los siguientes permisos:

| Capacidad | Permisos |
|-|-|
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y usar características de acción.</li><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de toma de decisiones.</li><li>**[!DNL Publish decisions]**: activar o desactivar actividades de toma de decisiones.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Campaign Administrator] {#campaign-administrator}

El rol **[!DNL Campaign Administrator]** permite los menús de administración con la posibilidad de administrar y publicar campañas y administración de decisiones.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li> **[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL Publish campaigns]**: publicar campañas.</li><li>**[!DNL View campaigns report]**: leer y editar el informe de campañas.</li></ul> |
| Configuraciones de canal | <ul> <li>**[!DNL Export suppression list]**: acceso a la lista de supresión de exportación como archivo CSV.</li> <li>**[!DNL Manage alerts]**: habilitar/deshabilitar alertas para campañas, mensajes y autorizaciones.</li> <li>**[!DNL Manage IP pools]**: leer, crear, editar y eliminar grupo de ip.</li> <li>**[!DNL Manage landing page settings]**: leer, crear, editar y eliminar la configuración de la página de aterrizaje.</li> <li>**[!DNL Manage messages general settings]**: leer, crear, editar y eliminar la configuración general del mensaje.</li> <li>**[!DNL Manage messages presets]**: leer, crear, editar y eliminar contenido de personalización de marca.</li> <li>**[!DNL Manage PTR records]**: leer y editar registros PTR.</li> <li>**[!DNL Manage SMS settings]**: leer, crear, editar y eliminar la configuración de SMS.</li> <li>**[!DNL Manage subdomains delegation]**: leer, crear, editar y eliminar la delegación de subdominios.</li> <li>**[!DNL Manage suppression rules]**: acceder, leer, crear, editar y eliminar reglas de supresión.</li> <li>**[!DNL View PTR records]**: acceso de solo lectura a registros PTR.</li> <li>**[!DNL View suppression list]**: leer y exportar la lista de supresión local.</li> </ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar estrategias de clasificación.</li></ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li> <li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li> <li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li> <li>**[!DNL View datasets]**: acceso de solo lectura a conjuntos de datos.</li> <li>**[!DNL Read Identity namespace]**: acceso de solo lectura al área de nombres de identidad.</li> <li>**[!DNL View schemas]**: acceso de solo lectura a esquemas.</li> <li>**[!DNL Sandbox]**: conceder acceso a zonas protegidas.</li> </ul> |

## [!DNL Campaign Approver] {#campaign-approver}

La función **[!DNL Campaign Approver]** permite a los usuarios aprobar envíos y publicarlos. Posteriormente, puede comprobar el éxito de sus envíos con los informes **[!DNL Campaigns]**.

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li>**[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL Publish campaigns]**: publicar campañas.</li><li>**[!DNL View campaigns report]**: leer, editar informes de campaña.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar mensajes personalizados informes y utilizar funciones de acción.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL View datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL View schemas]**: acceso de solo lectura a esquemas.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View messages presets]**: acceso de solo lectura a los ajustes preestablecidos de mensajes.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

El rol **[!DNL Campaign Manager]** permite a los usuarios crear y editar **[!UICONTROL Campañas]** y todas las capacidades vinculadas a **[!UICONTROL Campañas]**, pero no podrá publicarlas.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li>**[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL View campaigns report]**: leer, editar informe de recorrido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar mensajes personalizados informes y utilizar funciones de acción.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL View datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL View schemas]**: acceso de solo lectura a esquemas.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View messages presets]**: acceso de solo lectura a los ajustes preestablecidos de mensajes.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

El rol **[!DNL Campaign Viewer]** permite acceso de solo lectura a las capacidades **[!UICONTROL Campaigns]** y **[!UICONTROL Decision management]**.

Los usuarios asignados a esta función no podrán editar ni publicar.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li>**[!DNL View campaigns]**: acceso de solo lectura a las campañas.</li><li>**[!DNL View campaigns report]**: acceso de solo lectura a los informes de campañas.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de decisiones.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

El rol **[!DNL Journey Administrator]** permite los menús de administración con la posibilidad de administrar y publicar Recorridos y Administración de decisiones.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul> <li>**[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li> <li>**[!DNL Manage journeys events, data sources and actions]**: leer, crear, editar y eliminar eventos, orígenes o acciones.</li> <li>**[!DNL Publish journeys]**: publicar recorridos.</li> <li>**[!DNL View journeys report]**: leer y editar informe de recorridos.</li> </ul> |
| Configuraciones de canal | <ul> <li>**[!DNL Manage alerts]**: habilitar/deshabilitar alertas para recorridos y derechos.</li> <li>**[!DNL Manage IP pools]**: leer, crear, editar y eliminar grupo de ip.</li> <li>**[!DNL Manage Landing page settings]**: crear, editar y eliminar subdominios de página de aterrizaje y ajustes preestablecidos de página de aterrizaje.</li> <li>**[!DNL Manage messages general settings]**: leer, crear, editar y eliminar la configuración general del mensaje.</li> <li>**[!DNL Manage messages presets]**: leer, crear, editar y eliminar contenido de personalización de marca.</li> <li>**[!DNL Manage PTR records]**: leer y editar registros PTR.</li> <li>**[!DNL Manage SMS settings]**: cree, edite y elimine las credenciales de la API y las configuraciones del canal SMS necesarias para habilitar el canal SMS.</li> <li>**[!DNL Manage subdomains delegation]**: leer, crear, editar y eliminar la delegación de subdominios.</li> <li>**[!DNL Manage suppression rules]**: acceder, leer, crear, editar y eliminar reglas de supresión.</li> <li>**[!DNL View PTR records]**: acceso de solo lectura a registros PTR.</li> <li>**[!DNL View suppression list]**: leer y exportar la lista de supresión local.</li> </ul> |
| Gestión de decisiones | <ul> <li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar decisiones.</li> <li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar estrategias de clasificación.</li> </ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li> <li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li> <li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li> <li>**[!DNL View datasets]**: acceso de solo lectura a conjuntos de datos.</li> <li>**[!DNL Read Identity namespace]**: acceso de solo lectura al área de nombres de identidad.</li> <li>**[!DNL View schemas]**: acceso de solo lectura a esquemas.</li> <li>**[!DNL Sandbox]**: conceder acceso a zonas protegidas.</li> </ul> |
| Biblioteca de Journey Optimizer | <ul> <li>**[!DNL Manage Library Items]**: agregar y eliminar expresiones guardadas en la biblioteca [!DNL Journey Optimizer].</li> </ul> |
| Gobernanza de datos | <ul> <li>**[!DNL Manage data usage policies]**: leer, crear, editar y eliminar directivas de uso de datos.</li> <li>**[!DNL Manage usage label]**: leer, crear y eliminar etiquetas de uso.</li> <li>**[!DNL View data usage policies]**: acceso de solo lectura a las directivas de uso de datos.</li> <li>**[!DNL View user activity log]**: leer y exportar registros de auditoría.</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

La función **[!DNL Journey Approver]** permite a los usuarios aprobar envíos y publicarlos. Posteriormente, puede comprobar el éxito de sus envíos con los informes **[!DNL Journey]**.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li>**[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL Publish journey]**: publicar recorridos.</li><li>**[!DNL View journeys events, data sources and actions]**: acceso de solo lectura a eventos de recorrido, acciones personalizadas de recorrido y orígenes de datos de recorrido.</li><li>**[!DNL View journeys report]**: leer, editar informes de recorrido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y usar características de acción.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL View datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL View schemas]**: acceso de solo lectura a esquemas.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View channel configurations]**: acceso de solo lectura a las configuraciones de canal.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

El rol **[!DNL Journey Manager]** permite a los usuarios crear y editar **[!UICONTROL Recorridos]** y todas las capacidades vinculadas a **[!UICONTROL Recorridos]**, pero no podrán publicarlos.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li>**[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL View journeys events]**: acceso de solo lectura a eventos de recorrido, acciones personalizadas de recorrido y orígenes de datos de recorrido.</li><li>**[!DNL View journeys report]**: leer, editar informe de recorrido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y usar características de acción.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL View datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL View schemas]**: acceso de solo lectura a esquemas.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View channel configurations]**: acceso de solo lectura a las configuraciones de canal.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

El rol **[!DNL Journey viewer]** permite el acceso de solo lectura a las capacidades de **[!UICONTROL Recorridos]** y **[!UICONTROL Administración de decisiones]**.

Los usuarios asignados a esta función no podrán editar ni publicar.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li>**[!DNL View journeys]**: acceso de solo lectura a recorridos.</li><li>**[!DNL View journeys event, data sources, actions]**: acceso de solo lectura a eventos de recorrido y orígenes de datos.</li><li>**[!DNL View journeys report]**: acceso de solo lectura a los informes de recorrido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de decisiones.</li></ul> |

<!--
## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

The **[!DNL Orchestrated Campaign Administrator]** role allows the administration menus with the possibility to manage and publish Campaigns and Decision management. 

This permission includes the following permissions:

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li> **[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete orchestrated campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish orchestrated campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read and edit orchestrated campaigns report.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Export suppression list]**: access to export suppression list as a CSV file.</li> <li>**[!DNL Manage alerts]**: enable/disable alerts for campaigns, messages and entitlements.</li> <li>**[!DNL Manage custom dashboards]**: XX.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li> <li>**[!DNL Manage landing page settings]**: read, create, edit, and delete landing page settings.</li> <li>**[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li> <li>**[!DNL Manage messages presets]**: read, create, edit, and delete content branding.</li> <li>**[!DNL Manage orchestrated campaign administrator]**: XX.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li> <li>**[!DNL Manage SMS settings]**: read, create, edit, and delete SMS settings.</li> <li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li> <li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li> <li>**[!DNL View PTR records]**: read-only access to PTR records.</li> <li>**[!DNL View suppression list]**: read and export local suppression list.</li> </ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL Read Identity namespace]**: read-only access to identity namespace.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Sandbox]**: grant access to sandboxes.</li> </ul>|

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

The **[!DNL Orchestrated Campaign Approver]** role allows users to approve deliveries and publish them. They can later check the success of their deliveries with the **[!DNL Campaigns]** reports. 

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read, edit orchestrated campaign reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations|<ul><li>**[!DNL View orchestrated campaigns admin]**: XX.</li> <li>**[!DNL View messages presets]**: read-only access to messages presets.</li> <li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li></ul>|

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

The **[!DNL Orchestrated Campaign Manager]** role allows users to create and edit **[!UICONTROL Campaigns]** and every capability linked to **[!UICONTROL Campaigns]** but will not be able to publish them.

This permission includes the following permissions:

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read, edit journey report.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li> **[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li><li>**[!DNL View datasets]**: read-only access to datasets.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: XX.</li><li>**[!DNL View schemas]**: read-only access to schemas.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View messages presets]**: read-only access to messages presets.</li></ul>|

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

The **[!DNL Campaign Viewer]** role allows read-only access to the **[!UICONTROL Campaigns]** and **[!UICONTROL Decision management]** capabilities. 

Users assigned to this role will not be able to edit or publish. 

This permission includes the following permissions:

| Resources | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL View orchestrated campaigns]**: read-only access to campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read-only access to campaigns reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: XX.</li></ul>|

-->