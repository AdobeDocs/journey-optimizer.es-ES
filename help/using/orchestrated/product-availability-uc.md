---
solution: Journey Optimizer
product: journey optimizer
title: Notificar a los usuarios sobre la disponibilidad del producto
description: Notificar a los usuarios sobre la disponibilidad del producto
version: Campaign Orchestration
source-git-commit: 51c8c9282cb6eb9cdbd310d8f263d7973f28bbf0
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 3%

---

# Notificar a los usuarios sobre la disponibilidad del producto {#product-availability-uc}

>[!BEGINSHADEBOX]

Este caso de uso muestra la entrega a varios niveles: generar un correo electrónico distinto para cada elemento de la lista de deseos utilizando la dirección de correo electrónico almacenada con el elemento individual en lugar de con el registro de destinatario. Esto permite a los clientes recibir notificaciones independientes para cada producto de su lista de deseos aunque utilicen direcciones de correo electrónico diferentes para cada artículo.

>[!ENDSHADEBOX]

![](assets/notify-6.png){zoomable="yes"}

Diseñe una notificación de disponibilidad para informar a los clientes cuando los artículos de su lista de deseos vuelvan a estar disponibles. Este mensaje ayuda a volver a atraer a los clientes interesados y les anima a completar su compra mientras se repone el inventario.

1. Comience por configurar una nueva campaña específica para la renovación de la participación en la lista de deseos. Esto garantiza que su mensaje se centre en los clientes que ya han mostrado intención de compra al guardar productos en su lista de deseos.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Complete **[!UICONTROL Configuración de campaña]**, como el nombre de la campaña, la descripción, las fechas de inicio y finalización y las etiquetas relevantes.

1. Agregue una actividad **[!UICONTROL Generar audiencia]** con Lista de deseos como **[!UICONTROL Dimensión de segmentación]**.

   ![](assets/notify-1.png){zoomable="yes"}

1. Añada la condición para incluir solo las listas de deseos creadas en los últimos 36 meses.

   ![](assets/notify-2.png){zoomable="yes"}

1. Agregue una actividad **[!UICONTROL Change dimension]** para pasar de las listas de deseos al respectivo conjunto de clientes para la segmentación.

   ![](assets/notify-3.png){zoomable="yes"}

1. Después de iniciar el modo de borrador, previsualice la audiencia con detalles de la lista de deseos. Para obtener información más detallada, haga clic en un resultado de salida y seleccione **[!UICONTROL Previsualizar resultados]**.

   En este caso, los datos muestran tanto los destinatarios como sus elementos de la lista de deseos. Algunos clientes tienen varios artículos en la lista de deseos y, mediante el envío a varios niveles, reciben un correo electrónico independiente para cada artículo. En algunos casos, los clientes utilizan direcciones de correo electrónico diferentes para solicitudes de reserva independientes.

   ![](assets/notify-4.png){zoomable="yes"}

1. Para poder enviar un correo electrónico independiente para cada elemento, asegúrese de que [su configuración de correo electrónico](../orchestrated/target-dimension.md) está establecida con `Recipients - email` como **[!UICONTROL Dimension de destino de perfil]** y `Wishlistitems` como **[!UICONTROL dimensión secundaria]**.

   A continuación, en el menú **[!UICONTROL Dirección de ejecución]**, seleccione `wishlist.email` como **[!UICONTROL dimensión secundaria]**. Cada elemento de la Lista de deseos déclencheur un correo electrónico independiente, utilizando la dirección de correo electrónico almacenada en los datos de la Lista de deseos como dimensión secundaria.

   ![](assets/notify-5.png){zoomable="yes"}

1. Agregue una actividad **[!UICONTROL Correo electrónico]** para crear un mensaje de disponibilidad del producto. Haz clic en **[!UICONTROL Editar contenido]** para empezar a diseñar tu contenido.

   ➡️ [Más información sobre la personalización de correo electrónico](../email/content-from-scratch.md)

   ![](assets/notify-7.png){zoomable="yes"}

1. Una vez que la campaña se haya probado y esté lista, haga clic en **[!UICONTROL Publicar]** para activarla.

Con esta campaña orquestada, el cliente recibe un correo electrónico independiente para cada uno de sus elementos de la lista de deseos. Cada mensaje se envía a la dirección de correo electrónico específica asociada con esa lista de deseos, con contenido personalizado extraído de los detalles de ese elemento de la lista de deseos en particular.

