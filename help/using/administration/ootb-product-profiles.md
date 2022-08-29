---
title: Perfiles de producto integrados
description: Obtenga información sobre los perfiles de producto integrados
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 3afef10461ce29b811cb20a2c8c4e94f452daf1f
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 9%

---

# Perfiles de producto integrados {#ootb-product-profiles}


## Acerca de los permisos relacionados con los mensajes{#message-permissions}

Adobe Journey Optimizer ha lanzado nuevas funciones de creación en línea que le permiten crear y crear sus mensajes directamente desde un recorrido o una campaña. Para obtener más información sobre esta nueva función, [consulte esta página](../rn/inline-messages.md).

Esta función afecta a los permisos de la siguiente manera:

| Nombre del permiso | Se incluirá en |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**Después del 25 de julio**, permisos relacionados con **Mensajes** siguen estando disponibles, ya que se puede acceder a Mensajes para habilitar la transición y aún puede guardarlos como plantilla.

**A partir del 6 de septiembre**, permisos relacionados con **Mensajes** se eliminará y los mensajes ya no serán accesibles.

>[!WARNING]
>
>Si tiene usuarios asignados al **[!DNL Message Manager]** solo el perfil de producto, sin la variable **[!DNL Journey manager]** perfil de producto, debe asignar un nuevo perfil de producto para que puedan seguir editando contenido.


## [!DNL Campaign Administrator] {#campaign-administrator}

La variable **[!DNL Campaign Administrator]** perfil de producto permite que los menús de administración tengan la posibilidad de administrar y publicar campañas y administración de decisiones.

Este perfil de productos incluye los siguientes permisos:

| Capacidad | Permisos| |-|-| |Campañas| <ul><li> **[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL Publish campaigns]**: publicar campañas.</li><li>**[!DNL View campaigns report]**: leer y editar informes de campañas.</li></ul>|
|Administración|<ul><li>**[!DNL Manage subdomains delegation]**: leer, crear, editar y eliminar delegación de subdominios.</li><li>**[!DNL Manage IP pools]**: leer, crear, editar y eliminar el grupo ip.</li><li>**[!DNL Manage PTR records]**: leer y editar registros PTR.</li><li>**[!DNL View PTR records]**: acceso de solo lectura a registros PTR.</li><li> **[!DNL Manage messages general settings]**: leer, crear, editar y eliminar la configuración general del mensaje.</li><li>**[!DNL Manage messages presets]**: leer, crear, editar y eliminar la marca de contenido.</li><li>**[!DNL Manage suppression rules]**: acceda a las reglas de supresión: leer, crear, editar y eliminar.</li><li>**[!DNL Export suppression list]**: acceso para exportar la lista de supresión como archivo CSV.</li><li>**[!DNL View suppression list]**: leer y exportar la lista de supresión local.</li><li>**[!DNL Manage alerts]**: habilitar/deshabilitar alertas para campañas, mensajes y autorizaciones.</li><li>**[!DNL Manage landing page settings]**: leer, crear, editar y eliminar la configuración de la página de aterrizaje.</li><li>**[!DNL Manage SMS settings]**: leer, crear, editar y eliminar la configuración de SMS.</li></ul>|
|Administración de decisiones|<ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar estrategias de clasificación.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: conceda acceso a entornos limitados.</li><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Read Identity namespace]**: acceso de solo lectura al área de nombres de identidad.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

La variable **[!DNL Campaign Approver]** perfil de producto permite a los usuarios aprobar envíos y publicarlos. Posteriormente, pueden comprobar el éxito de sus envíos con la variable **[!DNL Campaigns]** informes.

| Capacidad | Permisos| |-|-| |Campañas| <ul><li>**[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL Publish campaigns]**: publicar campañas.</li><li>**[!DNL View Campaigns report]**: leer, editar informes de recorrido.</li></ul>|
|Administración de decisiones| <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de decisión.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes de mensajes personalizados y utilizar funciones de acción.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul>|
|Administración| <ul><li>**[!DNL View messages presets]**: acceso de solo lectura a los ajustes preestablecidos de mensajes.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

La variable **[!DNL Campaign Manager]** perfil de producto permite a los usuarios crear y editar **[!UICONTROL Campaigns]** y todas las capacidades vinculadas a **[!UICONTROL Campaigns]** pero no podrá publicarlas.

Este perfil de productos incluye los siguientes permisos:

| Capacidad | Permisos| |-|-| |Campañas| <ul><li>**[!DNL Manage campaigns]**: leer, crear, editar y eliminar campañas.</li><li>**[!DNL View campaigns report]**: leer, editar informe de recorrido.</li></ul>|
|Administración de decisiones| <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de decisión.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes de mensajes personalizados y utilizar funciones de acción.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul>|
|Administración| <ul><li>**[!DNL View messages presets]**: acceso de solo lectura a los ajustes preestablecidos de mensajes.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

La variable **[!DNL Campaign Viewer]** el perfil de producto permite el acceso de solo lectura al **[!UICONTROL Campaigns]** y **[!UICONTROL Decision management]** capacidades.

Los usuarios asignados a este perfil de producto no podrán editar ni publicar.

Este perfil de productos incluye los siguientes permisos:

| Capacidad | Permisos| |-|-| |Campañas| <ul><li>**[!DNL View campaigns]**: acceso de solo lectura a campañas.</li><li>**[!DNL View campaigns report]**: acceso de solo lectura a informes de campañas.</li></ul>|
|Administración de decisiones| <ul><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de decisiones.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

La variable **[!DNL Journey Administrator]** perfil de producto permite que los menús de administración puedan administrar y publicar Recorridos y la gestión de decisiones.

Este perfil de productos incluye los siguientes permisos:

| Capacidad | Permisos| |-|-| |Recorridos| <ul><li> **[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL Publish journeys]**: publicar recorridos.</li><li>**[!DNL Manage journeys events, data sources and actions]**: leer, crear, editar y eliminar eventos, fuentes o acciones.</li><li>**[!DNL View journeys report]**: leer y editar el informe recorridos .</li></ul>|
|Administración|<ul><li>**[!DNL Manage subdomains delegation]**: leer, crear, editar y eliminar delegación de subdominios.</li><li>**[!DNL Manage IP pools]**: leer, crear, editar y eliminar el grupo ip.</li><li>**[!DNL Manage PTR records]**: leer y editar registros PTR.</li><li>**[!DNL View PTR records]**: acceso de solo lectura a registros PTR.</li><li>**[!DNL Manage channel surfaces]**: leer, crear, editar y eliminar la marca de contenido.</li><li>**[!DNL Manage Landing page settings]**: cree, edite y elimine subdominios de la página de aterrizaje y ajustes preestablecidos de la página de aterrizaje.</li><li> **[!DNL Manage messages general settings]**: leer, crear, editar y eliminar la configuración general del mensaje.</li><li>**[!DNL Manage SMS settings]**: cree, edite y elimine las credenciales de API y las superficies de canal SMS necesarias para habilitar el canal SMS.</li><li>**[!DNL Manage suppression rules]**: acceda a las reglas de supresión: leer, crear, editar y eliminar.</li><li>**[!DNL View suppression list]**: leer y exportar la lista de supresión local.</li><li>**[!DNL Manage alerts]**: habilitar/deshabilitar alertas para recorridos y autorizaciones.</li></ul>|
|Administración de decisiones|<ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar decisiones.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar estrategias de clasificación.</li></ul>| |Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: conceda acceso a entornos limitados.</li><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Read Identity namespace]**: acceso de solo lectura al área de nombres de identidad.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul>| |Biblioteca de Journey Optimizer|<ul><li>**[!DNL Manage Library Items]**: agregar y eliminar expresiones guardadas en [!DNL Journey Optimizer] Biblioteca.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

La variable **[!DNL Journey Approver]** perfil de producto permite a los usuarios aprobar envíos y publicarlos. Posteriormente, pueden comprobar el éxito de sus envíos con la variable **[!DNL Journey]** informes.

Este perfil de productos incluye los siguientes permisos:

| Capacidad | Permisos| |-|-| |Recorridos| <ul><li>**[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL Publish journey]**: publicar recorridos.</li><li>**[!DNL View journeys events, data sources and actions]**: acceso de solo lectura a eventos de recorrido, acciones personalizadas de recorrido y fuentes de datos de recorrido.</li><li>**[!DNL View journeys report]**: leer, editar informes de recorrido.</li></ul>|
|Administración de decisiones| <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de decisión.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados, y usar funciones de acción.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: leer, crear, editar y eliminar segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul>|
|Administración| <ul><li>**[!DNL View channel surfaces]**: acceso de sólo lectura a las superficies del canal.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

La variable **[!DNL Journey Manager]** perfil de producto permite a los usuarios crear y editar **[!UICONTROL Journeys]** y todas las capacidades vinculadas a **[!UICONTROL Journeys]** pero no podrá publicarlas.

Este perfil de productos incluye los siguientes permisos:

| Capacidad | Permisos| |-|-| |Recorridos| <ul><li>**[!DNL Manage journeys]**: leer, crear, editar y eliminar recorridos.</li><li>**[!DNL View journeys events]**: acceso de solo lectura a eventos de recorrido, acciones personalizadas de recorrido y fuentes de datos de recorrido.</li><li>**[!DNL View journeys report]**: leer, editar informe de recorrido.</li></ul>|
|Administración de decisiones| <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de decisión.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados, y usar funciones de acción.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: leer, crear, editar y eliminar segmentos.</li><li>**[!DNL Manage profiles]**: leer, crear, editar y eliminar perfiles.</li><li>**[!DNL Read datasets]**: acceso de solo lectura a conjuntos de datos.</li><li>**[!DNL Read schemas]**: acceso de solo lectura a esquemas.</li><li>**[!DNL Manage merge policies]**: leer, crear, editar y eliminar políticas de combinación.</li></ul>|
|Administración| <ul><li>**[!DNL View channel surfaces]**: acceso de sólo lectura a las superficies del canal.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

La variable **[!DNL Journey viewer]** el perfil de producto permite el acceso de solo lectura al **[!UICONTROL Journeys]** y **[!UICONTROL Decision management]** capacidades.

Los usuarios asignados a este perfil de producto no podrán editar ni publicar.

Este perfil de productos incluye los siguientes permisos:

| Capacidad | Permisos| |-|-| |Recorridos| <ul><li>**[!DNL View journeys]**: acceso de solo lectura a recorrido.</li><li>**[!DNL View journeys event, data sources, actions]**: acceso de solo lectura a eventos de recorrido y fuentes de datos.</li><li>**[!DNL View journeys report]**: acceso de solo lectura a los informes de recorrido.</li></ul>|
|Administración de decisiones| <ul><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de decisiones.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

La variable **[!DNL Decisioning manager]** el perfil de producto solo permite que la variable **[!UICONTROL Decision management]** para abrir el Navegador. Los usuarios asignados a este perfil de producto solo podrán administrar, ver y publicar decisiones.

Este perfil de productos incluye los siguientes permisos:

| Capacidad | Permisos| |-|-| |Gestión de decisiones | <ul><li>**[!DNL Manage decisions]**: leer, crear, editar y eliminar entidades de decisión.</li><li>**[!DNL View decisions]**: acceso de solo lectura a entidades de decisión.</li><li>**[!DNL Manage ranking strategies]**: leer, crear, editar y eliminar informes personalizados, y usar funciones de acción.</li><li>**[!DNL Publish decisions]**: activar o desactivar actividades de decisiones.</li></ul>|
