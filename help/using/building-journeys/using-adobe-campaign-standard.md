---
solution: Journey Optimizer
product: journey optimizer
title: Acciones de Adobe Campaign Standard
description: Más información sobre las acciones de Adobe Campaign Standard
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: recorrido, integración, estándar, campaña, ACS
exl-id: 50565cd9-7415-4c6a-9651-24fefeded3f5
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/spxxZT-JH5yzziL8-oSkJdBcKEppm-4ZzeLC2-laCaM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 953
ht-degree: 8%

---

# Acciones estándar de [!DNL Adobe Campaign] {#using_campaign_action}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar las actividades de acción integradas de correo electrónico, push y SMS de Adobe Campaign Standard en sus recorridos basándose en las plantillas de mensajería transaccional de Campaign Standard.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acs"
>title="Acciones personalizadas"
>abstract="Una integración está disponible si tiene [!DNL Adobe Campaign] estándar. Permite enviar correos electrónicos, notificaciones push y SMS mediante las funcionalidades de mensajería transaccional de [!DNL Adobe Campaign]."

Si tiene [!DNL Adobe Campaign] Standard, están disponibles las siguientes actividades de acción integradas: **[!UICONTROL Correo electrónico]**, **[!UICONTROL Push]** y **[!UICONTROL SMS]**.

>[!NOTE]
>
>Para ello, debe configurar la acción integrada. Consulte [esta página](../action/acs-action.md).

Para cada uno de estos canales, selecciona una [!DNL Adobe Campaign] plantilla **de mensaje transaccional estándar**. Para los canales integrados de correo electrónico, SMS y push, dependemos de la mensajería transaccional para ejecutar el envío de mensajes. Significa que si desea utilizar una determinada plantilla de mensaje en los recorridos, debe publicarla en [!DNL Adobe Campaign] Standard. Consulte [esta página](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=es) para aprender a utilizar esta función.

>[!NOTE]
>
>El mensaje transaccional de Campaign Standard y su evento asociado deben publicarse para poder utilizarse en Journey Optimizer. Si el evento se publica pero el mensaje no, no será visible en la interfaz de Journey Optimizer. Si el mensaje se publica pero su evento asociado no, estará visible en la interfaz de Journey Optimizer, pero no se podrá utilizar.

![[!DNL Adobe Campaign] Configuración de acción estándar en el recorrido ](assets/journey59.png)

Puede utilizar un evento (también conocido como tiempo real) o una plantilla de mensajería transaccional de perfil.

>[!NOTE]
>
>Cuando enviamos mensajes transaccionales en tiempo real (rtEvent) o cuando enrutamos mensajes con un sistema de terceros gracias a una acción personalizada, se requiere una configuración específica para la administración de la fatiga, la lista de bloqueados o la baja. Por ejemplo, si un atributo &quot;unsubscribe&quot; está almacenado en [!DNL Adobe Experience Platform] o en un sistema de terceros, se tendrá que agregar una condición antes del envío del mensaje para comprobar esta condición.

Al seleccionar una plantilla, todos los campos esperados en la carga útil del mensaje se muestran en el panel de configuración de actividad en **[!UICONTROL Dirección]** y **[!UICONTROL Datos de Personalization]**. Debe asignar cada uno de estos campos con el campo que desea utilizar, ya sea desde el evento o desde el origen de datos. También puede utilizar el editor de expresiones avanzadas para pasar un valor manualmente, realizar la manipulación de datos en la información recuperada (por ejemplo, convertir una cadena a mayúsculas) o utilizar funciones como &quot;if, then, else&quot;. Consulte [esta página](expression/expressionadvanced.md).

![Interfaz de selección de plantillas de mensajes Campaign Standard](assets/journey60.png)

## Correo electrónico y SMS {#section_asc_51g_nhb}

Para **[!UICONTROL correo electrónico]** y **[!UICONTROL SMS]**, los parámetros son idénticos.

>[!NOTE]
>
>Al utilizar la plantilla transaccional de un perfil para el correo electrónico, [!DNL Adobe Campaign] Standard gestiona automáticamente el mecanismo de baja.
>Incluir un bloque de contenido de **[!UICONTROL vínculo de baja]** en [la plantilla de correo electrónico transaccional](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=es).
>Si utiliza una plantilla basada en eventos (rtEvent), incorpore un vínculo en el mensaje que pase el correo electrónico del destinatario como parámetro de URL y lo dirija a una página de aterrizaje de baja.
>Cree la página de aterrizaje y asegúrese de que la decisión de cancelar la suscripción del destinatario se transmita a Adobe.

En primer lugar, debe elegir una plantilla de mensajería transaccional.

Hay dos categorías disponibles: **[!UICONTROL Dirección]** y **[!UICONTROL Datos de Personalization]**.

Puede definir fácilmente dónde recuperar la **[!UICONTROL dirección]** o los **[!UICONTROL datos de Personalization]** mediante la interfaz. Puede examinar los eventos y los campos de la fuente de datos disponible. También puede utilizar el editor de expresiones avanzadas para casos de uso más avanzados, como el uso de una fuente de datos que requiera el paso de parámetros o la realización de manipulaciones. Consulte [esta página](expression/expressionadvanced.md).

**[!UICONTROL Dirección]**

>[!NOTE]
>
>Esta categoría solo está visible si selecciona un mensaje transaccional de &quot;evento&quot;. Para los mensajes de &quot;perfil&quot;, el sistema recupera automáticamente el campo **[!UICONTROL Address]** de [!DNL Adobe Campaign] Standard.

Estos son los campos que el sistema necesita para saber dónde enviar el mensaje. Para una plantilla de correo electrónico, es la dirección de correo electrónico. Para un SMS, es el número de teléfono móvil.

![Configuración del parámetro del mensaje para la integración con Campaign Standard](assets/journey61.png)

**[!UICONTROL Datos de Personalization]**

>[!NOTE]
>
>No se puede pasar una colección en datos de personalización. Si el correo electrónico o SMS transaccional espera colecciones, no funcionará. Tenga en cuenta también que los datos de personalización tienen un formato esperado (por ejemplo: cadena, decimal, etc.). Debe tener cuidado de respetar estos formatos esperados.

Estos son los campos esperados por el mensaje estándar [!DNL Adobe Campaign]. Estos campos se pueden utilizar para personalizar el mensaje, aplicar formato condicional o elegir una variante de mensaje específica.

![Asignación de campos entre Journey Optimizer y Campaign Standard](assets/journey62.png)

## Push {#section_im3_hvf_nhb}

Antes de utilizar la actividad push, la aplicación móvil debe configurarse junto con Campaign Standard para enviar notificaciones push. Use este [artículo](https://helpx.adobe.com/es/campaign/kb/integrate-mobile-sdk.html) para tomar los pasos de implementación necesarios para dispositivos móviles.

En primer lugar, debe elegir una aplicación móvil de la lista desplegable y un mensaje transaccional.

![Editor de expresiones avanzadas para la asignación de parámetros de Campaign Standard](assets/journey62bis.png)

Hay dos categorías disponibles: **[!UICONTROL Target]** y **[!UICONTROL Personalization Data]**.

**[!UICONTROL Target]**

>[!NOTE]
>
>Esta categoría solo está visible si selecciona un mensaje de evento. Para los mensajes de perfil, el sistema recupera automáticamente los campos **[!UICONTROL Target]** mediante la reconciliación realizada por [!DNL Adobe Campaign] Standard.

En esta sección, debe definir la **[!UICONTROL plataforma push]**. La lista desplegable le permite seleccionar **[!UICONTROL Apple Push Notification Server]** (iOS) o **[!UICONTROL Firebase Cloud Messaging]** (Android). También puede seleccionar un campo específico de un evento o una fuente de datos, o definir una expresión avanzada.

También necesita definir el **[!UICONTROL Token de registro]**. La expresión depende de cómo se defina el token en la carga útil de evento o en otra información de [!DNL Journey Optimizer]. Puede ser un campo simple o una expresión más compleja en el caso de que el token se defina en una colección, por ejemplo:

```
@event{Event_push._experience.campaign.message.profileSnapshot.pushNotificationTokens.first().token}
```

**[!UICONTROL Datos de Personalization]**

>[!NOTE]
>
>No se puede pasar una colección en datos de personalización. Si la inserción transaccional espera colecciones, no funcionará. Tenga en cuenta también que los datos de personalización tienen un formato esperado (por ejemplo: cadena, decimal, etc.). Debe tener cuidado de respetar estos formatos esperados.

Estos son los campos esperados por la plantilla transaccional utilizada en su mensaje estándar de [!DNL Adobe Campaign]. Estos campos se pueden utilizar para personalizar el mensaje, aplicar formato condicional o elegir una variante de mensaje específica.
