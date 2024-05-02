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
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 6%

---

# Funciones integradas {#ootb-product-profiles}

Las funciones integradas son un conjunto de derechos unitarios que permiten a los usuarios acceder a determinadas funcionalidades u objetos de la interfaz. Consulte [esta página](ootb-permissions.md) para obtener la lista de permisos disponibles para crear la función.

## [!DNL Campaign Administrator] {#campaign-administrator}

El **[!DNL Campaign Administrator]** Esta función permite a los menús de administración la posibilidad de administrar y publicar campañas y la administración de decisiones.

Esta función incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li> **[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL Publish campaigns]**: publique campañas.</li><li>**[!DNL View campaigns report]**: lea y edite el informe de campañas.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL Manage subdomains delegation]**: lea, cree, edite y elimine la delegación de subdominios.</li><li>**[!DNL Manage IP pools]**: leer, crear, editar y eliminar el grupo de ip.</li><li>**[!DNL Manage PTR records]**: leer y editar registros PTR.</li><li>**[!DNL View PTR records]**: acceso de solo lectura a registros PTR.</li><li> **[!DNL Manage messages general settings]**: leer, crear, editar y eliminar la configuración general del mensaje.</li><li>**[!DNL Manage messages presets]**: leer, crear, editar y eliminar la personalización de marca del contenido.</li><li>**[!DNL Manage suppression rules]**: acceda a leer, crear, editar y eliminar reglas de supresión.</li><li>**[!DNL Export suppression list]**: acceso a la lista de supresión de exportación como archivo CSV.</li><li>**[!DNL View suppression list]**: lea y exporte la lista de supresión local.</li><li>**[!DNL Manage alerts]**: habilite/deshabilite alertas para campañas, mensajes y autorizaciones.</li><li>**[!DNL Manage landing page settings]**: lea, cree, edite y elimine la configuración de la página de aterrizaje.</li><li>**[!DNL Manage SMS settings]**: leer, crear, editar y eliminar la configuración de SMS.</li></ul> |
| Administración de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar decisiones.</li><li>**[!DNL Manage ranking strategies]**: lea, cree, edite y elimine estrategias de clasificación.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: conceda acceso a las zonas protegidas.</li><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Read Identity namespace]**: acceso de solo lectura al área de nombres de identidad.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

El **[!DNL Campaign Approver]** Esta función permite a los usuarios aprobar envíos y publicarlos. Posteriormente, puede comprobar el éxito de sus envíos con la variable **[!DNL Campaigns]** informes.

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li>**[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL Publish campaigns]**: publique campañas.</li><li>**[!DNL View Campaigns report]**: lea y edite los informes de recorrido.</li></ul> |
| Administración de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: lea, cree, edite y elimine informes de mensajes personalizados y utilice funciones de acción.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View messages presets]**: acceso de solo lectura a los ajustes preestablecidos de mensajes.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

El **[!DNL Campaign Manager]** función que permite a los usuarios crear y editar **[!UICONTROL Campañas]** y todas las capacidades vinculadas a **[!UICONTROL Campañas]** pero no será capaz de publicarlos.

Esta función incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li>**[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL View campaigns report]**: leer, editar informe de recorrido.</li></ul> |
| Administración de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: lea, cree, edite y elimine informes de mensajes personalizados y utilice funciones de acción.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View messages presets]**: acceso de solo lectura a los ajustes preestablecidos de mensajes.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

El **[!DNL Campaign Viewer]** permite el acceso de solo lectura a la función **[!UICONTROL Campañas]** y **[!UICONTROL Administración de decisiones]** funciones.

Los usuarios asignados a esta función no podrán editar ni publicar.

Esta función incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Campañas | <ul><li>**[!DNL View campaigns]**: acceso de solo lectura a las campañas.</li><li>**[!DNL View campaigns report]**: acceso de solo lectura a los informes de campañas.</li></ul> |
| Administración de decisiones | <ul><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de decisiones.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

El **[!DNL Journey Administrator]** Esta función permite que los menús de administración puedan administrar y publicar Recorridos y Administración de decisiones.

Esta función incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li> **[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL Publish journeys]**: publicar recorridos.</li><li>**[!DNL Manage journeys events, data sources and actions]**: leer, crear, editar y eliminar eventos, fuentes o acciones.</li><li>**[!DNL View journeys report]**: lea y edite el informe recorridos.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL Manage subdomains delegation]**: lea, cree, edite y elimine la delegación de subdominios.</li><li>**[!DNL Manage IP pools]**: leer, crear, editar y eliminar el grupo de ip.</li><li>**[!DNL Manage PTR records]**: leer y editar registros PTR.</li><li>**[!DNL View PTR records]**: acceso de solo lectura a registros PTR.</li><li>**[!DNL Manage messages presets]**: leer, crear, editar y eliminar la personalización de marca del contenido.</li><li>**[!DNL Manage Landing page settings]**: cree, edite y elimine subdominios de página de aterrizaje y ajustes preestablecidos de página de aterrizaje.</li><li> **[!DNL Manage messages general settings]**: leer, crear, editar y eliminar la configuración general del mensaje.</li><li>**[!DNL Manage SMS settings]**: cree, edite y elimine las credenciales de API y las superficies de canal SMS necesarias para habilitar el canal SMS.</li><li>**[!DNL Manage suppression rules]**: acceda a leer, crear, editar y eliminar reglas de supresión.</li><li>**[!DNL View suppression list]**: lea y exporte la lista de supresión local.</li><li>**[!DNL Manage alerts]**: activar/desactivar alertas para recorridos y derechos.</li></ul> |
| Administración de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar decisiones.</li><li>**[!DNL Manage ranking strategies]**: lea, cree, edite y elimine estrategias de clasificación.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: conceda acceso a las zonas protegidas.</li><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Read Identity namespace]**: acceso de solo lectura al área de nombres de identidad.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul> |
| Biblioteca de Journey Optimizer | <ul><li>**[!DNL Manage Library Items]**: agregue y elimine expresiones guardadas en [!DNL Journey Optimizer] Biblioteca.</li></ul> |
| Control de datos | <ul><li>**[!DNL Manage usage label]**: leer, crear y eliminar etiquetas de uso.</li><li>**[!DNL Manage data usage policies]**: leer, crear, editar y eliminar directivas de uso de datos.</li><li>**[!DNL View data usage policies]**: acceso de solo lectura a las políticas de uso de datos.</li><li>**[!DNL View user activity log]**: leer y exportar registros de auditoría.</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

El **[!DNL Journey Approver]** Esta función permite a los usuarios aprobar envíos y publicarlos. Posteriormente, puede comprobar el éxito de sus envíos con la variable **[!DNL Journey]** informes.

Esta función incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li>**[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL Publish journey]**: publicar recorridos.</li><li>**[!DNL View journeys events, data sources and actions]**: acceso de solo lectura a eventos de recorrido, acciones personalizadas de recorrido y fuentes de datos de recorrido.</li><li>**[!DNL View journeys report]**: lea y edite los informes de recorrido.</li></ul> |
| Administración de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y utilizar funciones de acción.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View channel surfaces]**: acceso de solo lectura a las superficies de canal.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

El **[!DNL Journey Manager]** función que permite a los usuarios crear y editar **[!UICONTROL Recorridos]** y todas las capacidades vinculadas a **[!UICONTROL Recorridos]** pero no será capaz de publicarlos.

Esta función incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li>**[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL View journeys events]**: acceso de solo lectura a eventos de recorrido, acciones personalizadas de recorrido y fuentes de datos de recorrido.</li><li>**[!DNL View journeys report]**: leer, editar informe de recorrido.</li></ul> |
| Administración de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y utilizar funciones de acción.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul> |
| Configuraciones de canal | <ul><li>**[!DNL View channel surfaces]**: acceso de solo lectura a las superficies de canal.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

El **[!DNL Journey viewer]** permite el acceso de solo lectura a la función **[!UICONTROL Recorridos]** y **[!UICONTROL Administración de decisiones]** funciones.

Los usuarios asignados a esta función no podrán editar ni publicar.

Esta función incluye los siguientes permisos:

| Recursos | Permisos |
|-|-|
| Recorridos | <ul><li>**[!DNL View journeys]**: acceso de solo lectura a recorrido.</li><li>**[!DNL View journeys event, data sources, actions]**: acceso de solo lectura a eventos de recorrido y fuentes de datos.</li><li>**[!DNL View journeys report]**: acceso de solo lectura a los informes de recorrido.</li></ul> |
| Administración de decisiones | <ul><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de decisiones.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

El **[!DNL Decisioning manager]** función solo permite acceder a **[!UICONTROL Administración de decisiones]** menú. Los usuarios asignados a esta función solo podrán administrar, ver y publicar decisiones.

Esta función incluye los siguientes permisos:

| Capacidad | Permisos |
|-|-|
| Administración de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y utilizar funciones de acción.</li><li>**[!DNL Publish decisions]**: activar o desactivar actividades de toma de decisiones.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Experience decisioning entities.</li--></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

El **[!DNL Content Library Manager]** función solo permite acceder a **[!UICONTROL Plantillas de contenido]** menú. Los usuarios asignados a esta función solo podrán acceder a la biblioteca de plantillas para crear contenido sin acceder a los recorridos o campañas.

Esta función incluye los siguientes permisos:

| Capacidad | Permisos |
|-|-|
| Biblioteca de Journey Optimizer | <ul><li>**[!DNL Manage library items]**: leer, crear, editar y eliminar elementos de la biblioteca de Journey Optimizer, incluidas plantillas de contenido y fragmentos.</li><li>**[!DNL Manage simulate content]**: acceso al **[!UICONTROL Simular contenido]** para vista previa y prueba.</li></ul> |
| Administración de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de toma de decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados y utilizar funciones de acción.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar definiciones de segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul> |