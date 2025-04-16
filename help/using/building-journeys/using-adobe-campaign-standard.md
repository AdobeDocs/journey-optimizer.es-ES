---
solution: Journey Optimizer
product: journey optimizer
title: Acciones de Adobe Campaign Standard
description: Obtenga información sobre Adobe Campaign Standard acciones
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: viaje, integración, estándar, campaña, ACS
exl-id: 50565cd9-7415-4c6a-9651-24fefeded3f5
source-git-commit: e539d694e8fb91b6a8c7ba7ff5a2bb0905651f81
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 5%

---

# Acciones de Adobe Campaign Standard {#using_campaign_action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acs"
>title="Acciones personalizadas"
>abstract="Una integración está disponible si tiene Adobe Campaign Standard. Permite enviar correos electrónicos, notificaciones push y SMS mediante las funcionalidades de mensajería transaccional de Adobe Campaign."

Si tiene Adobe Campaign Standard, están disponibles las siguientes actividades de acción integradas: **[!UICONTROL correo electrónico]**, **[!UICONTROL push]** y **[!UICONTROL SMS]**.

>[!NOTE]
>
>Para ello, debe configurar la acción incorporada. Consulte [esta página](../action/acs-action.md).

Para cada uno de estos canales, seleccione un plantilla de mensajería **transaccional Adobe Campaign Standard**. Para los canales integrados de correo electrónico, SMS y push, confiamos en la mensajería transaccional para ejecutar el envío de mensajes. Significa que si desea utilizar un determinado mensaje plantilla en sus viajes, debe publicar en Adobe Campaign Standard. Consulte [este Página](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=es) para aprender a utilizar esta función.

>[!NOTE]
>
>El mensaje transaccional Campaign Standard y sus evento asociados deben publicarse para poder utilizarse en Journey Optimizer. Si el evento se publica pero el mensaje no, no será visible en la interfaz de Journey Optimizer. Si el mensaje se publica pero no su evento asociado, será visible en la interfaz de Journey Optimizer, pero no podrá utilizarse.

![](assets/journey59.png)

Puede utilizar un plantilla de mensajería evento (también conocido como tiempo real) o perfil transaccional.

>[!NOTE]
>
>Cuando enviamos mensajes transaccionales en tiempo real (rtEvent) o cuando enrutamos mensajes con un sistema terceros gracias a una acción personalizada, se requiere una configuración específica para la fatiga, el bloqueo lista o la gestión baja. Por ejemplo, si un atributo &quot;cancelar la suscripción&quot; se almacena en el Adobe Experience Platform o en un sistema terceros, se deberá agregar una condición antes del envío del mensaje para verificar esta condición.

Cuando selecciona un plantilla, todos los campos previstos en la carga útil del mensaje se muestran en el panel de configuración de actividad en **** Dirección y **[!UICONTROL datos]** de personalización. Debe asignar cada uno de estos campos al campo que desee utilizar, ya sea desde el evento o desde el fuente de datos. También puede usar el editor expresión avanzado para pasar un valor manualmente, realizar la manipulación de datos en la información recuperada (por ejemplo, convertir una cadena en mayúsculas) o usar funciones como &quot;si, entonces, más&quot;. Consulte [esta página](expression/expressionadvanced.md).

![](assets/journey60.png)

## Correo electrónico y SMS {#section_asc_51g_nhb}

Para **[!UICONTROL correo electrónico]** y **[!UICONTROL SMS]**, los parámetros son idénticos.

>[!NOTE]
>
>Cuando se utiliza el plantilla transaccional de un perfil para correo electrónico, el mecanismo de baja es manejado automáticamente por Adobe Campaign Standard. Para implementar esto, puede incluir fácilmente un **[!UICONTROL bloque de contenido vincular]** de cancelación de suscripción dentro [del plantilla de correo electrónico](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=es) transaccional. Sin embargo, si está utilizando un plantilla basado en evento (rtEvent), debe incorporar un vincular en el mensaje que pasa el correo electrónico del destinatario como un parámetro URL y los dirige a un página de aterrizaje baja. Es necesario crear este página de aterrizaje y garantizar que la decisión del destinatario de cancelar la suscripción se transmita efectivamente a Adobe Systems.

Primero, debe elegir un plantilla de mensajería transaccional.

Hay dos categorías disponibles: **[!UICONTROL Dirección]** y **[!UICONTROL Datos]** de personalización.

Puede definir fácilmente dónde recuperar la **[!UICONTROL dirección]** o los **[!UICONTROL datos]** de personalización mediante la interfaz. Puede navegar a través de eventos y campos de fuente de datos disponibles. También puede usar la editor de expresión avanzada para casos de uso más avanzados, como usar un fuente de datos que requiera pasar parámetros o realizar manipulaciones. Consulte [esta página](expression/expressionadvanced.md).

**[!UICONTROL Dirección]**

>[!NOTE]
>
>Este categoría sólo está visible si selecciona un mensaje transaccional &quot;evento&quot;. Para los mensajes de &quot;perfil&quot;, el sistema recupera automáticamente el **** campo Dirección de Adobe Campaign Standard.

Estos son los campos que el sistema necesita para saber dónde enviar el mensaje. Para un correo electrónico plantilla, es la dirección correo electrónico. Para un SMS, es el número de teléfono móvil.

![](assets/journey61.png)

**[!UICONTROL Datos de personalización]**

>[!NOTE]
>
>No es posible pasar un colección en personalización datos. Si el SMS o correo electrónico transaccional espera colecciones, no funcionará. Tenga en cuenta también que los datos del personalización tienen un formato esperado (por ejemplo: cadena, decimal, etc.). Debe tener cuidado de respetar estos formatos esperados.

Estos son los campos esperados por el mensaje de Adobe Campaign Standard. Estos campos se pueden utilizar para personalizar el mensaje, aplicar formato condicional o elegir una variante específica del mensaje.

![](assets/journey62.png)

## Push {#section_im3_hvf_nhb}

Antes de utilizar la actividad push, debe configurarse la aplicación móvil junto con Campaign Standard para enviar notificaciones push. Utilice este [artículo](https://helpx.adobe.com/es/campaign/kb/integrate-mobile-sdk.html) para tomar las medidas necesarias implementación para móviles.

Primero, debe elegir una aplicación móvil del lista desplegable y una mensaje transaccional.

![](assets/journey62bis.png)

Hay dos categorías disponibles: **[!UICONTROL Target]** y **[!UICONTROL Datos]** de personalización.

**[!UICONTROL Target]**

>[!NOTE]
>
>Este categoría solo está visible si selecciona un mensaje evento. Para perfil mensajes, el sistema recupera automáticamente los campos Target **** mediante la reconciliación realizada por Adobe Campaign Standard.

En esta sección, debe definir la **[!UICONTROL plataforma]** Push. La lista desplegable le permite seleccionar **[!UICONTROL Apple Push Notification Server]** (iOS) o **[!UICONTROL Firebase Cloud Messaging]** (Android). También puede seleccionar un campo específico de una evento o una fuente de datos, o definir una expresión avanzada.

También debe definir el token ]**de**[!UICONTROL  registro. El expresión depende de cómo se defina el token en la carga evento o en otra [!DNL Journey Optimizer] información. Puede ser un campo simple o un expresión más complejo en caso de que el token se defina en un colección para instancia:

```
@event{Event_push._experience.campaign.message.profileSnapshot.pushNotificationTokens.first().token}
```

**[!UICONTROL Datos de personalización]**

>[!NOTE]
>
>No es posible pasar un colección en personalización datos. Si la inserción transaccional espera colecciones, no funcionará. Tenga en cuenta también que los datos del personalización tienen un formato esperado (por ejemplo: cadena, decimal, etc.). Debe tener cuidado de respetar estos formatos esperados.

Estos son los campos esperados por el plantilla transaccional utilizado en su mensaje de Adobe Campaign Standard. Estos campos se pueden utilizar para personalizar el mensaje, aplicar formato condicional o elegir una variante específica del mensaje.
