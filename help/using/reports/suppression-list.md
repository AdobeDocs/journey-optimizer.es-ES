---
solution: Journey Optimizer
product: journey optimizer
title: Lista de supresión
description: Aprenda a utilizar la lista de supresión
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 11%

---

# Lista de supresión {#suppression-list}

Una lista de supresión consiste en las direcciones y los dominios que desea excluir de las entregas, ya que el envío a estos contactos podría dañar su reputación y las tasas de entrega.

La lista de supresión [!DNL Journey Optimizer] se administra en su propio nivel de entorno, es decir, para una zona protegida determinada.

Recopila direcciones de correo electrónico y dominios que se suprimen en todos los correos en un solo entorno de cliente, lo que significa específico de un ID de organización asociado a un ID de zona protegida.

>[!NOTE]
>
>Adobe mantiene una lista actualizada de direcciones incorrectas conocidas que han demostrado ser perjudiciales para la participación y la reputación de correo electrónico, y garantiza que no se les envíen correos electrónicos. Esta lista se administra en una lista de supresión global que es común para todos los clientes de Adobe. Las direcciones y los nombres de dominio contenidos en la lista de supresión global están ocultos. En los informes de envío solo se indica el número de destinatarios excluidos.

Además, puede aprovechar la **API de REST de supresión** de Journey Optimizer para controlar los mensajes salientes mediante supresión y listas de permitidos. [Obtenga información sobre cómo trabajar con la API de REST de supresión](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## ¿Por qué una lista de supresión? {#why-suppression-list}

Para controlar los mensajes de correo electrónico que reciben los propietarios de la bandeja de entrada y asegurarse de que solo reciben los que desean, los proveedores de servicios de Internet (ISP) y los filtros comerciales de correo no deseado tienen sus algoritmos propietarios para rastrear la reputación general de los remitentes de correo electrónico en función de las direcciones IP y los dominios de envío que utilizan.

Si no tiene en cuenta sus comentarios (como quejas por correo no deseado, rechazos, etc.), valorarán su reputación de forma negativa. La lista de supresión le ayuda a cumplir los comentarios de los ISP.

Los destinatarios cuyas direcciones de correo electrónico están suprimidas se excluyen automáticamente de la entrega de mensajes. Esto acelera las entregas, ya que la tasa de error afecta significativamente a la velocidad de entrega.

## ¿Qué hay en la lista de supresión? {#what-s-on-suppression-list}

Las direcciones se agregan a la lista de supresión de la siguiente manera:

* Todas las **devoluciones graves** y **quejas por correo no deseado** envían automáticamente las direcciones correspondientes a la lista de supresión después de una sola incidencia. Obtenga más información acerca de quejas por correo no deseado en [esta sección](#spam-complaints).

* **Las devoluciones leves** no envían inmediatamente una dirección a la lista de supresión, sino que se suman a un contador de errores. A continuación, se realizan varios [reintentos](../configuration/retries.md) y, cuando el contador de errores alcanza el umbral, la dirección se agrega a la lista de supresión.

* También puede [**agregar manualmente** una dirección o un dominio](../configuration/manage-suppression-list.md#add-addresses-and-domains) a la lista de supresión.

Obtenga más información sobre devoluciones graves y leves en [esta sección](#delivery-failures).

>[!NOTE]
>
>Las direcciones de los usuarios que cancelaron su suscripción no se pueden enviar a la lista de supresión porque no reciben correos electrónicos de [!DNL Journey Optimizer]. Su elección se gestiona en el nivel de Experience Platform. Más información sobre la [exclusión](../privacy/opt-out.md).

Para cada dirección, el motivo básico de la supresión y la categoría de supresión (leve, grave, etc.) se muestran en la lista de supresión. Obtenga más información acerca de cómo obtener acceso y administrar la lista de supresión en [esta sección](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Los perfiles con estado **[!UICONTROL Suprimido]** se excluyen durante el proceso de envío de mensajes. Por lo tanto, aunque los **informes de Recorrido** mostrarán que estos perfiles se han movido a través del recorrido ([Leer audiencia](../building-journeys/read-audience.md) y [actividades de mensajes](../building-journeys/journeys-message.md)), los **informes de correo electrónico** no los incluirán en las métricas de **[!UICONTROL Enviados]**, ya que se filtran antes del envío de correo electrónico.
>
>Obtenga más información sobre [el informe en vivo](../reports/live-report.md) y [el informe de Customer Journey Analytics](../reports/report-gs-cja.md). Para averiguar el motivo de todos los casos de exclusión, puede usar [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}.

### Errores de envío {#delivery-failures}

Existen dos tipos de errores cuando falla una entrega:

* **Rechazo fuerte**. Las devoluciones graves indican que la dirección de correo electrónico no es válida (es decir, que no existe). Esto implica un mensaje de rechazo del servidor de correo electrónico receptor que indica explícitamente que la dirección no es válida.
* **Rebote suave**. Este es un rebote de correo electrónico temporal que se produjo para una dirección de correo electrónico válida.

Un **rechazo grave** agrega automáticamente la dirección de correo electrónico a la lista de supresión.

Un **rebote suave** <!--or an **ignored** error--> que se produce demasiadas veces también envía la dirección de correo electrónico a la lista de supresión después de varios reintentos. [Más información sobre los reintentos](../configuration/retries.md)

Si continúa enviando a estas direcciones, puede afectar a sus tasas de entrega, ya que indica a los ISP que es posible que no esté siguiendo las prácticas recomendadas de mantenimiento de la lista de direcciones de correo electrónico y, por lo tanto, que no sea un remitente de confianza.

### Quejas de spam {#spam-complaints}

La lista de supresión recopila direcciones de correo electrónico que marcan el mensaje como correo no deseado. Por ejemplo, si alguien escribe a un servicio de atención al cliente solicitando no volver a recibir correo de usted, la dirección de correo electrónico de esa persona se suprimirá en toda su instancia y ya no podrá volver a enviar a esa dirección.

Enviar a los destinatarios después de que envíen una queja de correo no deseado puede tener un gran impacto en su reputación de envío, ya que informa a los ISP de que puede enviar correos electrónicos no deseados y puede no escuchar a sus destinatarios.

Esto podría provocar que se bloqueara su dirección IP o dominio de envío, lo que se puede evitar con estas direcciones en la lista de supresión.

Algunos ISP ofrecen un bucle de comentarios (FBL) que permite notificar automáticamente al remitente del correo electrónico cuando el usuario que lo recibe decide marcarlo como correo no deseado. [Más información](deliverability.md#feedback-loops)
