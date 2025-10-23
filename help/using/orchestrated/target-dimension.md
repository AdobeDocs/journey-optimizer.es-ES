---
solution: Journey Optimizer
product: journey optimizer
title: Cree su dimensión de segmentación
description: Obtenga información sobre cómo asignar un esquema relacional al perfil del cliente
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: ac80d1cec351a3029c8b2bf862275ffe7fd5c86d
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

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

➡️ [Obtenga más información acerca de esquemas relacionales en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/schema/relational#how-relational-schemas-differ-from-standard-xdm-schemas)

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