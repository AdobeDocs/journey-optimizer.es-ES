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
source-git-commit: 49a607e8e4b4cce7bcf41d92abe6b9fa54dfb411
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 7%

---

# Funciones integradas {#ootb-product-profiles}

Las funciones integradas son un conjunto de derechos unitarios que permiten a los usuarios acceder a determinadas funcionalidades u objetos de la interfaz. Consulte [esta página](ootb-permissions.md) para ver la lista de permisos disponibles para crear su función.

## [!DNL Campaign Administrator] {#campaign-administrator}

El rol **[!DNL Campaign Administrator]** permite los menús de administración con la posibilidad de administrar y publicar campañas y administración de decisiones.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li> **[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL Publish campaigns]**: publicar campañas.</li><li>**[!DNL View campaigns report]**: leer y editar el informe de campañas.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL Manage subdomains delegation]**: leer, crear, editar y eliminar la delegación de subdominios.</li><li>**[!DNL Manage IP pools]**: leer, crear, editar y eliminar grupo de ip.</li><li>**[!DNL Manage PTR records]**: leer y editar registros PTR.</li><li>**[!DNL View PTR records]**: acceso de solo lectura a registros PTR.</li><li> **[!DNL Manage messages general settings]**: leer, crear, editar y eliminar la configuración general del mensaje.</li><li>**[!DNL Manage messages presets]**: leer, crear, editar y eliminar contenido de personalización de marca.</li><li>**[!DNL Manage suppression rules]**: acceder, leer, crear, editar y eliminar reglas de supresión.</li><li>**[!DNL Export suppression list]**: acceso a la lista de supresión de exportación como archivo CSV.</li><li>**[!DNL View suppression list]**: leer y exportar la lista de supresión local.</li><li>**[!DNL Manage alerts]**: habilitar/deshabilitar alertas para campañas, mensajes y autorizaciones.</li><li>**[!DNL Manage landing page settings]**: leer, crear, editar y eliminar la configuración de la página de aterrizaje.</li><li>**[!DNL Manage SMS settings]**: leer, crear, editar y eliminar la configuración de SMS.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar estrategias de clasificación.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: conceder acceso a zonas protegidas.</li><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Read Identity namespace]**: acceso de solo lectura al área de nombres de identidad.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

La función **[!DNL Campaign Approver]** permite a los usuarios aprobar envíos y publicarlos. Posteriormente, puede comprobar el éxito de sus envíos con los informes **[!DNL Campaigns]**.

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li>**[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL Publish campaigns]**: publicar campañas.</li><li>**[!DNL View Campaigns report]**: leer, editar informes de recorrido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar mensajes personalizados informes y utilizar funciones de acción.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View messages presets]**: acceso de solo lectura a los ajustes preestablecidos de mensajes.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

El rol **[!DNL Campaign Manager]** permite a los usuarios crear y editar **[!UICONTROL Campañas]** y todas las capacidades vinculadas a **[!UICONTROL Campañas]**, pero no podrá publicarlas.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li>**[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL View campaigns report]**: leer, editar informe de recorrido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar mensajes personalizados informes y utilizar funciones de acción.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li></ul> |
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
| Recorridos | <ul><li> **[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL Publish journeys]**: publicar recorridos.</li><li>**[!DNL Manage journeys events, data sources and actions]**: leer, crear, editar y eliminar eventos, orígenes o acciones.</li><li>**[!DNL View journeys report]**: leer y editar informe de recorridos.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL Manage subdomains delegation]**: leer, crear, editar y eliminar la delegación de subdominios.</li><li>**[!DNL Manage IP pools]**: leer, crear, editar y eliminar grupo de ip.</li><li>**[!DNL Manage PTR records]**: leer y editar registros PTR.</li><li>**[!DNL View PTR records]**: acceso de solo lectura a registros PTR.</li><li>**[!DNL Manage messages presets]**: leer, crear, editar y eliminar contenido de personalización de marca.</li><li>**[!DNL Manage Landing page settings]**: crear, editar y eliminar subdominios de página de aterrizaje y ajustes preestablecidos de página de aterrizaje.</li><li> **[!DNL Manage messages general settings]**: leer, crear, editar y eliminar la configuración general del mensaje.</li><li>**[!DNL Manage SMS settings]**: cree, edite y elimine las credenciales de la API y las configuraciones del canal SMS necesarias para habilitar el canal SMS.</li><li>**[!DNL Manage suppression rules]**: acceder, leer, crear, editar y eliminar reglas de supresión.</li><li>**[!DNL View suppression list]**: leer y exportar la lista de supresión local.</li><li>**[!DNL Manage alerts]**: habilitar/deshabilitar alertas para recorridos y derechos.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar estrategias de clasificación.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: conceder acceso a zonas protegidas.</li><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Read Identity namespace]**: acceso de solo lectura al área de nombres de identidad.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li></ul> |
| Biblioteca de Journey Optimizer | <ul><li>**[!DNL Manage Library Items]**: agregar y eliminar expresiones guardadas en la biblioteca [!DNL Journey Optimizer].</li></ul> |
| Gobernanza de datos | <ul><li>**[!DNL Manage usage label]**: leer, crear y eliminar etiquetas de uso.</li><li>**[!DNL Manage data usage policies]**: leer, crear, editar y eliminar directivas de uso de datos.</li><li>**[!DNL View data usage policies]**: acceso de solo lectura a las directivas de uso de datos.</li><li>**[!DNL View user activity log]**: leer y exportar registros de auditoría.</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

La función **[!DNL Journey Approver]** permite a los usuarios aprobar envíos y publicarlos. Posteriormente, puede comprobar el éxito de sus envíos con los informes **[!DNL Journey]**.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li>**[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL Publish journey]**: publicar recorridos.</li><li>**[!DNL View journeys events, data sources and actions]**: acceso de solo lectura a eventos de recorrido, acciones personalizadas de recorrido y orígenes de datos de recorrido.</li><li>**[!DNL View journeys report]**: leer, editar informes de recorrido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y usar características de acción.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View channel configurations]**: acceso de solo lectura a las configuraciones de canal.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

El rol **[!DNL Journey Manager]** permite a los usuarios crear y editar **[!UICONTROL Recorridos]** y todas las capacidades vinculadas a **[!UICONTROL Recorridos]**, pero no podrán publicarlos.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li>**[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL View journeys events]**: acceso de solo lectura a eventos de recorrido, acciones personalizadas de recorrido y orígenes de datos de recorrido.</li><li>**[!DNL View journeys report]**: leer, editar informe de recorrido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y usar características de acción.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View channel configurations]**: acceso de solo lectura a las configuraciones de canal.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

El rol **[!DNL Journey viewer]** permite el acceso de solo lectura a las capacidades de **[!UICONTROL Recorridos]** y **[!UICONTROL Administración de decisiones]**.

Los usuarios asignados a esta función no podrán editar ni publicar.

Este permiso incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li>**[!DNL View journeys]**: acceso de solo lectura a recorridos.</li><li>**[!DNL View journeys event, data sources, actions]**: acceso de solo lectura a eventos de recorrido y orígenes de datos.</li><li>**[!DNL View journeys report]**: acceso de solo lectura a los informes de recorrido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de decisiones.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

El rol **[!DNL Decisioning manager]** solo permite el acceso al menú **[!UICONTROL Administración de decisiones]**. Los usuarios asignados a esta función solo podrán administrar, ver y publicar decisiones.

Este permiso incluye los siguientes permisos:

| Capacidad | Permisos |
|-|-|
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y usar características de acción.</li><li>**[!DNL Publish decisions]**: activar o desactivar actividades de toma de decisiones.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

El rol **[!DNL Content Library Manager]** solo permite el acceso al menú **[!UICONTROL Plantillas de contenido]**. Los usuarios asignados a esta función solo podrán acceder a la biblioteca de plantillas para crear contenido sin acceder a los recorridos o campañas.

Este permiso incluye los siguientes permisos:

| Capacidad | Permisos |
|-|-|
| Biblioteca de Journey Optimizer | <ul><li>**[!DNL Manage library items]**: leer, crear, editar y eliminar elementos de la biblioteca Journey Optimizer, incluidas plantillas de contenido y fragmentos.</li><li>**[!DNL Manage simulate content]**: acceso a la opción **[!UICONTROL Simular contenido]** para vista previa y revisión.</li><li>**[!DNL Publish Fragment]**: publicar fragmentos de contenido.</li></ul> |
| Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y usar características de acción.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmento.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar directivas de combinación.</li></ul> |