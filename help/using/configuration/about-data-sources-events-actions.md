---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de recorridos
description: Obtenga información sobre cómo configurar fuentes de datos, eventos y acciones
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Configuración de recorridos {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="Acerca de la configuración del recorrido"
>abstract="Para enviar mensajes con recorridos, debe configurar Fuentes de datos, Eventos y Acciones. Las fuentes de datos permiten definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos, por ejemplo en las condiciones. Los eventos le permiten activar los recorridos cuando se recibe un evento. Las acciones personalizadas le permiten conectarse a un sistema de terceros para enviar sus mensajes. Si utiliza las funciones de mensaje integradas de Journey Optimizer, no es necesario configurar una acción."

Para enviar mensajes con recorridos, debe configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** y **[!UICONTROL Actions]**.

![](assets/admin-menu.png)

## Fuentes de datos {#data-sources}

La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos. [Más información](../../using/datasource/about-data-sources.md)

## Eventos {#events}

Los eventos le permiten activar los recorridos de forma unitaria para enviar mensajes, en tiempo real, al individuo que entra en el recorrido.

En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Adobe Experience (XDM). Los eventos proceden de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). [Más información](../../using/event/about-events.md)

## Acciones {#actions}

Las funcionalidades de mensaje de Journey Optimizer están incorporadas: solo necesita añadir una actividad de acción de canal al recorrido. Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. [Más información](../../using/action/action.md)

## Vaya a los campos de Adobe Experience Platform {#friendly-names-display}

Al definir [carga útil de evento](../event/about-creating.md#define-the-payload-fields), [carga útil de grupo de campos](../datasource/configure-data-sources.md#define-field-groups) y seleccionando campos en la variable [editor de expresiones](../building-journeys/expression/expressionadvanced.md), se muestra el nombre para mostrar además del nombre del campo. Esta información se recupera de la definición de esquema del modelo de datos de Experience.

Si se proporcionan descriptores como &quot;xdm:alternativeDisplayInfo&quot; al configurar esquemas, los nombres descriptivos reemplazarán a los nombres para mostrar. Resulta especialmente útil cuando se trabaja con &quot;eVars&quot; y campos genéricos. Puede configurar descriptores de nombres descriptivos mediante una llamada a la API. Para obtener más información, consulte la [Guía para desarrolladores de Schema Registry](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target=&quot;_blank&quot;}.

![](assets/xdm-from-descriptors.png)

Si hay un nombre descriptivo disponible, el campo se mostrará como `<friendly-name>(<name>)`. Si no hay ningún nombre descriptivo disponible, aparecerá el nombre para mostrar, por ejemplo `<display-name>(<name>)`. Si no se define ninguno de ellos, solo se mostrará el nombre técnico del campo `<name>`.

>[!NOTE]
>
>Los nombres descriptivos no se recuperan al seleccionar campos de una unión de esquemas.
