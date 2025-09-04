---
solution: Journey Optimizer
product: journey optimizer
title: Cree su dimensión de segmentación
description: Obtenga información sobre cómo asignar un esquema relacional al perfil del cliente
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---


# Configuración de una dimensión de segmentación {#configuration}

Con **[!UICONTROL Campañas orquestadas]**, puede diseñar y enviar comunicaciones segmentadas en el nivel de entidad, aprovechando las capacidades de esquema relacional de Adobe Experience Platform. Experience Platform utiliza esquemas para describir la estructura de los datos de una manera uniforme y reutilizable. Cuando se incorporan datos en Experience Platform, se estructuran según un esquema XDM.

Aunque la segmentación de **[!UICONTROL Campañas orquestadas]** funciona principalmente en esquemas relacionales, la entrega de mensajes real siempre se produce en el nivel **Perfil**.

Al configurar el direccionamiento, se definen dos aspectos clave:

* **Esquemas de destino**

  Especifique qué esquemas relacionales son aptos para la segmentación. De manera predeterminada, se usa el esquema denominado `Recipient`, pero puede configurar alternativas como `Visitors`, `Customers`, etc.

  >[!IMPORTANT]
  >
  > El esquema de destino debe tener una relación 1:1 con el esquema `Profile`. Por ejemplo, no puede usar `Purchases` como esquema de destino, ya que normalmente representa una relación uno a varios.

* **Vínculo de perfil**

  El sistema debe comprender cómo se asigna el esquema de destino al esquema `Profile`. Esto se logra a través de un campo de identidad compartido, que existe tanto en el esquema de destino como en el esquema `Profile` y que está configurado como un área de nombres de identidad.

## Cree su dimensión de segmentación {#targeting-dimension}

Comience por configurar la orquestación de campañas asignando un esquema relacional al perfil del cliente.

1. Desde **[!UICONTROL Administration]**, acceda al menú **[!UICONTROL Configurations]** y seleccione **[!UICONTROL Campaign Target Dimension]**.

   ![](assets/target-dimension-1.png)

1. Haga clic en **[!UICONTROL Crear]** para empezar a crear su **[!UICONTROL dimensión de segmentación]**.

1. Elija su [esquema](gs-schemas.md) configurado previamente &#x200B;de la lista desplegable.

   Aunque todos los esquemas relacionales son visibles, solo se pueden seleccionar los esquemas con una relación de identidad directa con el **perfil**.

1. Seleccione el **[!UICONTROL valor de identidad]** que representa la entidad a la que desea destinar.

   En este ejemplo, el perfil del cliente está vinculado a varias suscripciones, cada una representada por un único `crmID` en el esquema `Recipient`. Al configurar **[!UICONTROL Target Dimension]** para que use el esquema `Recipient` y su identidad `crmID`, puede enviar mensajes en el nivel de suscripción, en lugar de al perfil de cliente principal, asegurándose de que cada contrato o línea reciba su propio mensaje personalizado.

   [Más información en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/schema/composition#identity).

   ![](assets/target-dimension-2.png)

1. Haga clic en **[!UICONTROL Guardar]** para completar la configuración. Tenga en cuenta que una vez creada, una **[!UICONTROL dimensión de destino]** no se puede eliminar ni editar.

Después de configurar **[!UICONTROL Target Dimension]**, proceda a crear y configurar su **[!UICONTROL configuración de canal]** y defina los **[!UICONTROL detalles de ejecución]** correspondientes.

## Configure su configuración de canal {#channel-configuration}

Después de configurar tu **[!UICONTROL Dimension de Target]**, debes configurar tu correo electrónico o SMS **[!UICONTROL Configuración del canal]** y definir los **[!UICONTROL Detalles de ejecución]** adecuados. Esto le permite definir:

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
