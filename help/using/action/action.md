---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las acciones
description: Aprenda a trabajar con acciones
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Experienced
keywords: acciones, recorrido, mensajes, envío, conexiones
exl-id: 7f0cda1d-daf0-4d4c-9978-ddef81473813
TQID: https://experienceleague.adobe.com/u-fLClLKK9cC7D2BwO5vxdW11tywPDRWzOMBtYUj5Ts
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 62bc5f833b5612570ba50c98519a2f9c07d0bd5e
workflow-type: tm+mt
source-wordcount: 397
ht-degree: 35%

---

# Introducción a las acciones personalizadas {#about_actions}

>[!BEGINSHADEBOX]

**En esta página:** Comprenda cómo las acciones y las acciones personalizadas le permiten ofrecer experiencias personalizadas y conectar sistemas de terceros a través de llamadas a la API de REST, de modo que pueda extender los recorridos más allá de la mensajería integrada.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_list"
>title="Acciones personalizadas"
>abstract="Las acciones son conexiones a través de las cuales se ofrecen experiencias personalizadas en tiempo real a clientes, como notificaciones push, correo electrónico, SMS u otro medio de participación digital de su negocio."

Las acciones son conexiones a través de las cuales se ofrecen experiencias personalizadas en tiempo real a clientes, como notificaciones push, correo electrónico, SMS u otro medio de participación digital de su negocio.

➡️ [Descubra esta funcionalidad en vídeo](#video)

[!DNL Journey Optimizer] viene con capacidad de envío de mensajes integrada. Las acciones personalizadas permiten configurar la conexión de un sistema de terceros para enviar mensajes o llamadas API. Se puede configurar una acción con cualquier servicio de cualquier proveedor al que se pueda llamar mediante una API REST con carga útil en formato JSON.

* Si utiliza las versiones 7 u 8 de Adobe Campaign, hay una integración disponible bajo petición. Consulte [esta página](../action/acc-action.md).

* Si utiliza un sistema de terceros para enviar mensajes como Epsilon, Facebook, Adobe Developer, Firebase, etc., debe crear y configurar una acción personalizada. Consulte [esta página](../action/about-custom-action-configuration.md).

>[!CAUTION]
>
>La configuración de las acciones personalizadas debe realizarla un **usuario técnico**.

Las acciones personalizadas son acciones adicionales definidas por usuarios técnicos y que se ponen a disposición de los especialistas en marketing: una vez configuradas, aparecen en la paleta izquierda del recorrido, en la categoría **[!UICONTROL Acción]**. Obtenga más información en [esta página](../building-journeys/about-journey-activities.md#action-activities).

Para ver la lista de acciones o configurar una nueva acción, seleccione **[!UICONTROL Configuraciones]** en la sección del menú ADMINISTRACIÓN. En la sección **[!UICONTROL Acciones]**, haga clic en **[!UICONTROL Administrar]**. Se muestra la lista de acciones. Consulte [esta página](../start/user-interface.md) para obtener más información sobre la interfaz.

![](assets/custom1.png)

Aprenda a solucionar problemas de una acción personalizada [en esta página dedicada](../action/troubleshoot-custom-action.md).

## Vídeo práctico {#video}

Obtenga información sobre cómo configurar acciones personalizadas.

>[!VIDEO](https://video.tv.adobe.com/v/3428396?quality=12)

## Recursos adicionales

Examine las secciones siguientes para obtener más información sobre la configuración y el uso de las acciones personalizadas:

* [Configurar las acciones personalizadas](../action/about-custom-action-configuration.md): aprenda a crear y configurar una acción personalizada
* [Usar acciones personalizadas](../building-journeys/using-custom-actions.md): aprenda a usar acciones personalizadas en sus recorridos
* [Pasar colecciones a parámetros de acción personalizados](../building-journeys/collections.md): aprenda a pasar una colección en parámetros de acción personalizados que se rellenan dinámicamente durante la ejecución
* [Solución de problemas con acciones personalizadas](../action/troubleshoot-custom-action.md) - Aprenda a solucionar problemas de una acción personalizada

