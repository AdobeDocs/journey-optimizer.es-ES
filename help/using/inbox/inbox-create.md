---
title: Crear bandeja de entrada
description: Obtenga información sobre cómo crear y configurar una bandeja de entrada en Adobe Journey Optimizer para enviar mensajes persistentes y no intrusivos a los usuarios.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 4%

---

# Crear una bandeja de entrada {#inbox-create}

Antes de crear una bandeja de entrada, complete los pasos de [Configuración de la bandeja de entrada](inbox-configuration.md). La configuración de canal identifica la aplicación o sitio web de destino, la página o regla y la ubicación en la que se representa la bandeja de entrada.

Para crear una bandeja de entrada de mensaje a través de una campaña, siga estos pasos:

1. Cree una campaña. [Más información](../campaigns/create-campaign.md)

1. Seleccione el tipo de campaña que desea ejecutar:

   * **[!UICONTROL Programado - Marketing]**: ejecute la campaña inmediatamente o en una fecha especificada. Las campañas programadas están destinadas a enviar **marketing** mensajes. Se configuran y ejecutan desde la interfaz de usuario de.

   * **[!UICONTROL Activado por API - Marketing/Transaccional]**: ejecute la campaña mediante una llamada de API. Las campañas activadas por API están destinadas a enviar **marketing** o **mensajes transaccionales**, es decir, mensajes enviados después de una acción realizada por un individuo: restablecimiento de contraseña, compra en el carro de compras, etc. [Aprenda a almacenar en déclencheur una campaña mediante API](../campaigns/api-triggered-campaigns.md)

1. En la ficha **[!UICONTROL Propiedades]**, especifique un nombre y una descripción para la campaña.

1. En la ficha **[!UICONTROL Acción]**, seleccione la acción **[!UICONTROL Bandeja de entrada]**.

   ![](assets/inbox-create-1.png)

1. Seleccione o cree una nueva [configuración de la bandeja de entrada](inbox-configuration.md).

   ![](assets/inbox-create-2.png)

1. Acceda a la pestaña Contenido para diseñar el mensaje con el diseñador de contenido. [Más información](inbox-design.md)

1. En la ficha **[!UICONTROL Audiencia]**, haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para mostrar la lista de audiencias de Adobe Experience Platform disponibles. [Más información sobre los públicos](../audience/about-audiences.md)

1. En el campo **[!UICONTROL Área de nombres de identidad]**, elija el área de nombres que desea utilizar para identificar a los individuos del segmento seleccionado. [Más información sobre áreas de nombres](../event/about-creating.md#select-the-namespace)

1. Puede programar la campaña para una fecha específica o configurarla para que se repita a intervalos regulares. [Más información](../campaigns/create-campaign.md#schedule)

1. Revise y active la campaña para enviar mensajes a la bandeja de entrada.

Ahora puede elegir esta Bandeja de entrada al crear su [campaña de tarjeta de contenido](../content-card/create-content-card.md).
