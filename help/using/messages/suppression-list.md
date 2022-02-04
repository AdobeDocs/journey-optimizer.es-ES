---
title: Lista de supresión
description: Aprenda qué es la lista de supresión, su propósito y qué se incluye en ella.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 06a7abc2ada930356cbaf45ce01eed5e3156f2e3
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# Lista de supresión {#suppression-list}

Una lista de supresión consiste en direcciones de correo electrónico que desea excluir de los envíos, ya que el envío a estos contactos podría dañar la reputación del envío y las tasas de envío.

La variable [!DNL Journey Optimizer] la lista de supresión se administra en su propio nivel de entorno.

Recopila direcciones de correo electrónico y dominios que se suprimen en todos los correos en un único entorno de cliente, lo que significa que son específicos de un ID de organización de IMS asociado a un ID de simulador de pruebas.

## ¿Por qué una lista de supresión? {#why-suppression-list}

Para controlar los mensajes de correo electrónico que reciben los propietarios de las bandejas de entrada y asegurarse de que solo reciben los que desean, los proveedores de servicios de Internet (ISP) y los filtros de correo no deseado comerciales tienen sus algoritmos propietarios para realizar un seguimiento de la reputación general de los remitentes de correo electrónico en función de las direcciones IP y los dominios de envío que utilizan.

Si no recibe sus comentarios (como quejas por correo no deseado, devoluciones, etc.) teniendo en cuenta, valorarán su reputación por debajo. La lista de supresión le ayuda a cumplir con los comentarios de los ISP.

Los destinatarios cuyas direcciones de correo electrónico se supriman se excluyen automáticamente de la entrega de mensajes. Esto acelera las entregas, ya que la tasa de error afecta significativamente a la velocidad de entrega.

## ¿Qué hay en la lista de supresión? {#what-s-on-suppression-list}

Las direcciones de correo electrónico se añaden a la lista de supresión de la siguiente manera:

* Todo **rechazos graves** y **quejas por correo no deseado** envíe automáticamente las direcciones de correo electrónico correspondientes a la lista de supresión después de una sola incidencia.

* **Rechazos leves** no envíe inmediatamente una dirección de correo electrónico a la lista de supresión, sino que se sumará a un contador de errores. Varios [reintentos](../configuration/retries.md) a continuación, se realizan y, cuando el contador de errores alcanza el umbral, la dirección se agrega a la lista de supresión.

* También puede [**manualmente** añadir una dirección o un dominio](../configuration/manage-suppression-list.md#add-addresses-and-domains) a la lista de supresión.

Obtenga más información sobre los rechazos graves y los rechazos leves en [esta sección](#delivery-failures).

>[!NOTE]
>
>Las direcciones de los usuarios que han dejado de suscribirse no se pueden enviar a la lista de supresión, ya que no reciben correos electrónicos de [!DNL Journey Optimizer]. Su elección se gestiona a nivel de Experience Platform. Más información sobre [exclusión](consent.md).

Para cada dirección, el motivo básico de la supresión y la categoría de supresión (suave, dura, etc.) se muestran en la lista de supresión. Obtenga más información sobre el acceso y la administración de la lista de supresión en [esta sección](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Los perfiles con **[!UICONTROL Suppressed]** se excluyen durante el proceso de envío de mensajes. Por lo tanto, mientras que la variable **Informes de recorrido** mostrará estos perfiles como si se hubieran movido a través del recorrido ([Leer segmento](../building-journeys/read-segment.md) y [Mensaje](../building-journeys/journeys-message.md) actividades), **Informes de correo electrónico** no los incluirá en la variable **[!UICONTROL Sent]** las métricas tal y como están filtradas antes del envío por correo electrónico.
>
>Obtenga más información sobre [Informe Activo](../reports/live-report.md) y [Informe global](../reports/global-report.md). Para averiguar el motivo de todos los casos de exclusión, puede usar la variable [Servicio de consultas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.

### Errores de entrega {#delivery-failures}

Existen dos tipos de errores cuando falla una entrega:

* **Rechazo grave**. Un rechazo grave indica una dirección de correo electrónico no válida (es decir, una dirección de correo electrónico que no existe). Esto implica un mensaje de rechazo del servidor de correo electrónico receptor que indica explícitamente que la dirección no es válida.
* **Rechazo suave**. Se trata de una devolución temporal de correo electrónico que se produjo para una dirección de correo electrónico válida.

A **devolución fuerte** agrega automáticamente la dirección de correo electrónico a la lista de supresión.

A **devolución suave** <!--or an **ignored** error--> que ocurre demasiadas veces también envía la dirección de correo electrónico a la lista de supresión después de varios reintentos. [Más información sobre los reintentos](../configuration/retries.md)

Si continúa enviando direcciones a estas, puede afectar a las tasas de envío, ya que indica a los ISP que puede que no siga las prácticas recomendadas de mantenimiento de la lista de direcciones de correo electrónico y, por lo tanto, puede que no sea un remitente fiable.

### Reclamaciones por correo no deseado {#spam-complaints}

La lista de supresión recopila direcciones de correo electrónico que marcan el mensaje como correo no deseado. Por ejemplo, si alguien escribe a un servicio de atención al cliente pidiéndole que nunca vuelva a recibir correo, la dirección de correo electrónico de esa persona se suprime en toda la instancia y ya no podrá enviarlo a esa dirección.

El envío a los destinatarios después de que envíen una queja por correo no deseado puede tener un gran impacto en su reputación de envío, ya que informa a los ISP de que puede enviar correos electrónicos no deseados y no escuchar a sus destinatarios.

Esto podría hacer que su dirección IP o dominio de envío se bloquearan, lo que se puede evitar con estas direcciones en la lista de supresión.
