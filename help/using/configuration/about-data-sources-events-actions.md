---
title: Administración y configuración
description: Conozca las directrices de administración y configuración
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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: b32306f9561946a6c289e5e9c7cc3243349141bc
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 49%

---

# Configurar recorridos

Para enviar mensajes con recorridos, debe configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** y **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

## Fuentes de datos

La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos. [Más información](../../using/datasource/about-data-sources.md)

## Eventos

Los eventos le permiten almacenar en déclencheur sus recorridos de forma unitaria para enviar mensajes, en tiempo real, al individuo que entra en el recorrido.

En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Adobe Experience (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). [Más información](../../using/event/about-events.md)

## Acciones

Las funcionalidades de mensajes de Journey Optimizer están incorporadas: solo necesita diseñar el contenido y publicar el mensaje. Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. [Más información](../../using/action/action.md)

## Navegación por los campos de Adobe Experience Platform {#friendly-names-display}

Al definir [carga útil de evento](../event/about-creating.md#define-the-payload-fields), [carga útil de grupo de campos](../datasource/configure-data-sources.md#define-field-groups) y seleccionar campos en el [editor de expresiones](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=es){target=&quot;_blank&quot;}, se muestra el nombre para mostrar además del nombre del campo. Esta información se recupera de la definición de esquema del modelo de datos de Experience.

Si se proporcionan descriptores como &quot;xdm:alternateDisplayInfo&quot; al configurar esquemas, los nombres descriptivos reemplazarán los nombres para mostrar. Resulta especialmente útil cuando se trabaja con eVars y campos genéricos. Puede configurar descriptores de nombres descriptivos mediante una llamada a API. Para obtener más información, consulte la [guía para desarrolladores del Registro de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=es){target=&quot;_blank&quot;}.

![](../assets/xdm-from-descriptors.png)

Si hay un nombre descriptivo disponible, el campo se mostrará como `<friendly-name>(<name>)`. Si no hay ningún nombre descriptivo disponible, aparecerá el nombre para mostrar, por ejemplo `<display-name>(<name>)`. Si no se define ninguno de ellos, solo se mostrará el nombre técnico del campo `<name>`.

>[!NOTE]
>
>Los nombres descriptivos no se recuperan al seleccionar campos de una unión de esquemas.