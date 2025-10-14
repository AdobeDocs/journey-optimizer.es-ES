---
solution: Journey Optimizer
product: journey optimizer
title: Configure su configuración de canal
description: Obtenga información sobre cómo configurar el canal
version: Campaign Orchestration
source-git-commit: 0b92d0e806c47b0d87ba53b7c7f1d56ee4453abb
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Configure su configuración de canal {#channel-configuration}

Después de configurar su [Dimension de destino](target-dimension.md), debe configurar su **[!UICONTROL configuración de canal]** y definir los **[!UICONTROL detalles de ejecución]** adecuados. Esto le permite definir:

* **El nivel de entrega de mensajes**: por ejemplo, enviar un mensaje por destinatario, como un solo correo electrónico por individuo.

* **La dirección de ejecución**: el campo de contacto específico que se va a utilizar para el envío, como una dirección de correo electrónico o un número de teléfono.

Para configurar la configuración de canal:

1. Comience creando y configurando su **[!UICONTROL configuración de canal]**.

   También puede actualizar una **[!UICONTROL configuración de canal]** existente.

   ➡️ [Siga los pasos detallados en esta página](../email/surface-personalization.md)

1. Desde la sección **[!UICONTROL Detalles de ejecución]** de tu **[!UICONTROL configuración de canal]**, accede a la pestaña **[!UICONTROL Campañas orquestadas]**.

   ![](assets/target-dimension-3.png)

1. Haga clic en **[!UICONTROL Habilitado]** para que sea compatible con campañas orquestadas.

1. Elija el método de entrega:

   * **[!UICONTROL Target Dimension]**: enviar a la entidad principal; por ejemplo, destinatario.

   * **[!UICONTROL Target + Dimension secundario]**: envíe utilizando entidades primarias y secundarias; por ejemplo, destinatario + contrato.

1. Seleccione en la lista desplegable su [Dimension de Target creado anteriormente](#targeting-dimension).

   ![](assets/target-dimension-4.png)

1. Si seleccionó **[!UICONTROL Target + Dimension secundario]** como método de entrega, elija un **[!UICONTROL Dimension secundario]** para definir el contexto para la entrega de mensajes.

1. En la sección **[!UICONTROL Dirección de ejecución]**, elija qué **[!UICONTROL Source]** se debe usar para obtener la dirección de entrega, como la dirección de correo electrónico o el número de teléfono:

   * **[!UICONTROL Perfil]**: seleccione esta opción si la dirección de envío, por ejemplo: correo electrónico, se almacena directamente en el perfil principal del cliente.

     Resulta útil al enviar mensajes al cliente principal, no a una entidad asociada específica.

   * **[!UICONTROL Target Dimension]**: elija esta opción si la dirección de envío está almacenada en la entidad principal; por ejemplo, un destinatario.

     Resulta útil cuando cada destinatario tiene su propia dirección de envío, como un correo electrónico o un número de teléfono diferentes.

   * **[!UICONTROL Dimension secundario]**: Cuando use **[!UICONTROL Target + Dimension secundario]** como método de envío, seleccione el **[!UICONTROL Dimension secundario]** relevante que configuró anteriormente.

     Por ejemplo, si la dimensión secundaria representa una reserva o una suscripción, la dirección de ejecución, como un correo electrónico, se puede tomar de ese nivel. Esto resulta útil en casos en los que los perfiles utilizan un detalle de contacto diferente al reservar o suscribirse a un servicio.

1. En el campo **[!UICONTROL Dirección de entrega]**, haga clic en ![icono de edición](assets/do-not-localize/edit.svg) para elegir el campo específico que se usará para la entrega de mensajes.

   ![](assets/target-dimension-4.png)

1. Una vez configurada, haga clic en **[!UICONTROL Enviar]**.

El canal está listo para usarse con **Campañas orquestadas**, y los mensajes se enviarán de acuerdo con la dimensión de destino seleccionada.
