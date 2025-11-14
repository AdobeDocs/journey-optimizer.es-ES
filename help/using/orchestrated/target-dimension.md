---
solution: Journey Optimizer
product: journey optimizer
title: Cree su dimensión de segmentación
description: Obtenga información sobre cómo asignar un esquema relacional al perfil del cliente
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: f842142a985481004192c88af2973787912c85b3
workflow-type: tm+mt
source-wordcount: '438'
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
  > Las campañas organizadas permiten segmentar cualquier esquema que tenga una relación directa o relacionada con el esquema **Profile**. Aunque su uso está dirigido principalmente a relaciones 1:1, también admite relaciones 1:N, como los destinatarios de la cuenta `>`, siempre que la ruta de la relación esté modelada correctamente en el modelo de datos. Esto permite el direccionamiento basado en los datos de nivel de cuenta, pero sin dejar de resolver la identidad de perfil correcta para la entrega de mensajes.

* **Vínculo de perfil**

  El sistema debe comprender cómo se asigna el esquema de destino al esquema `Profile`. Esto se logra a través de un campo de identidad compartido, que existe tanto en el esquema de destino como en el esquema `Profile` y que está configurado como un área de nombres de identidad.

➡️ [Obtenga más información acerca de esquemas relacionales en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#how-relational-schemas-differ-from-standard-xdm-schemas)

## Cree su dimensión de segmentación {#targeting-dimension}

Comience por configurar la orquestación de campañas asignando un esquema relacional al perfil del cliente.

1. Desde **[!UICONTROL Administration]**, acceda al menú **[!UICONTROL Configurations]** y seleccione **[!UICONTROL Campaign Target Dimension]**.

   ![](assets/target-dimension-1.png)

1. Haga clic en **[!UICONTROL Crear]** para empezar a crear su **[!UICONTROL dimensión de segmentación]**.

1. Elija su [esquema](gs-schemas.md) configurado previamente &#x200B;de la lista desplegable.

   Aunque se muestran todos los esquemas relacionales, solo se pueden seleccionar los que tengan una relación de identidad directa con **Perfil**. Evite elegir esquemas que no sean personas, como compras, y seleccione un esquema asociado directamente a un perfil.

1. Seleccione el **[!UICONTROL valor de identidad]** que representa la entidad a la que desea destinar.

   En este ejemplo, el perfil del cliente está vinculado a varias suscripciones, cada una representada por un único `crmID` en el esquema `Recipient`. Al configurar **[!UICONTROL Target Dimension]** para que use el esquema `Recipient` y su identidad `crmID`, puede enviar mensajes en el nivel de suscripción, en lugar de al perfil de cliente principal, asegurándose de que cada contrato o línea reciba su propio mensaje personalizado.

   [Más información en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition#identity).

   ![](assets/target-dimension-2.png)

1. Haga clic en **[!UICONTROL Guardar]** para completar la configuración. Tenga en cuenta que una vez creada, una **[!UICONTROL dimensión de destino]** no se puede eliminar ni editar.

Después de configurar **[!UICONTROL Target Dimension]**, proceda a crear y configurar su **[!UICONTROL configuración de canal]** y defina los **[!UICONTROL detalles de ejecución]** correspondientes.