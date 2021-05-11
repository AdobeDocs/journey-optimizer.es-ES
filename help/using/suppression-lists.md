---
title: Supervisión de la ejecución de los mensajes
description: Conozca las directrices de monitorización y envío
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 3%

---

# Administrar listas de supresión {#manage-suppression-lists}

![](assets/do-not-localize/badge.png)

Una lista de supresión consiste en direcciones de correo electrónico que desea excluir de los envíos, ya que el envío a estos contactos podría dañar la reputación del envío y las tasas de envío.

La **lista de supresión** de Journey Optimizer se administra en su propio nivel de entorno. Recopila quejas por correo no deseado, rechazos graves y rechazos leves que se producen de manera consistente.

## ¿Por qué las listas de supresión? {#why-suppression-lists}

Para controlar los mensajes de correo electrónico que reciben los propietarios de las bandejas de entrada y asegurarse de que solo reciben los que desean, los proveedores de servicios de Internet (ISP) y los filtros de correo no deseado comerciales tienen sus algoritmos propietarios para realizar un seguimiento de la reputación general de los remitentes de correo electrónico en función de las direcciones IP y los dominios de envío que utilizan.

Si no recibe sus comentarios (como quejas por correo no deseado, devoluciones, etc.) teniendo en cuenta, valorarán su reputación por debajo. La lista de supresión le ayuda a cumplir con los comentarios de los ISP.

Los destinatarios cuyas direcciones de correo electrónico se supriman se excluyen automáticamente de la entrega de mensajes. Esto acelera las entregas, ya que la tasa de error afecta significativamente a la velocidad de entrega.

### Reclamaciones por correo no deseado {#spam-complaints}

La lista de supresión recopila direcciones de correo electrónico que marcan el mensaje como correo no deseado. El envío a los destinatarios después de que envíen una queja por correo no deseado puede tener un gran impacto en su reputación de envío, ya que informa a los ISP de que puede enviar correos electrónicos no deseados y no escuchar a sus destinatarios.

Esto podría hacer que su dirección IP o dominio de envío se bloquearan, lo que se puede evitar con estas direcciones en la lista de supresión.

### Devoluciones {#bounces}

Además, la lista de supresión contiene direcciones de correo electrónico que se devuelven de forma rígida o que devuelven de forma suave demasiadas veces. Si continúa enviando direcciones a estas, puede afectar a las tasas de envío, ya que indica a los ISP que puede que no siga las prácticas recomendadas de mantenimiento de la lista de direcciones de correo electrónico y, por lo tanto, puede que no sea un remitente fiable.

## Administración de listas de supresión {#suppression-list-management}

La lista de supresión de Journey Optimizer recopila direcciones de correo electrónico y dominios que se suprimen en todos los correos **en un único entorno de cliente**, lo que significa específico de un ID de organización de IMS asociado a un ID de simulador de pruebas.

La lista de supresión le permite recopilar automáticamente:
* Las direcciones de correo electrónico que no son válidas o que devuelven mensajes de forma flexible de forma consistente podrían afectar negativamente a la reputación del correo electrónico si continúa incluyéndolas en los envíos.
* Destinatarios que emiten una queja de correo no deseado de algún tipo contra uno de sus mensajes de correo electrónico.

Por ejemplo, si alguien escribe a un servicio de atención al cliente pidiéndole que nunca vuelva a recibir correo, la dirección de correo electrónico de esa persona se suprime en toda la instancia y ya no podrá enviarlo a esa dirección.

<!--For each address, the basic reason for suppression (soft bounces, a hard bounce or a spam complaint) will be shown in the Suppression list.-->

### Errores de envío {#delivery-failures}

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

Existen tres tipos de errores cuando falla una entrega:

* **Rechazo** duro. Un rechazo grave indica una dirección de correo electrónico no válida (es decir, una dirección de correo electrónico que no existe). Esto implica un mensaje de rechazo del servidor de correo electrónico receptor que indica explícitamente que la dirección no es válida, como &quot;usuario desconocido&quot;.
* **Rechazo suave**. Se trata de una devolución temporal de correo electrónico que se produjo para una dirección de correo electrónico válida.
* **Ignorado**. Se trata de una devolución de correo electrónico que se produjo para una dirección de correo electrónico válida pero que se conoce como temporal, como un intento de conexión fallido, un problema temporal relacionado con el correo no deseado (reputación de correo electrónico) o un problema técnico temporal.

Los rechazos graves y los rechazos leves pueden ser un motivo para que una dirección de correo electrónico se añada automáticamente a la lista de supresión.

### ¿Qué hay en la lista de supresión? {#what-s-on-suppression-list}

Las direcciones de correo electrónico se añaden a la lista de supresión de la siguiente manera:

* Todas las **rechazos graves** y **quejas por correo no deseado** envían automáticamente las direcciones de correo electrónico correspondientes a la lista de supresión tras una sola incidencia.

* **Los** rechazos leves no envían inmediatamente una dirección de correo electrónico a la lista de supresión, sino que se suman a un contador de errores. Cuando el contador de errores alcanza el umbral, la dirección se agrega a la lista de supresión.

   El umbral se establece en tres errores:
   * Para la misma entrega, en el tercer intento, se suprime la dirección .
   * Si hay diferentes entregas y dos errores se producen al menos con una diferencia de 24 horas, el contador de errores se incrementa con cada error y la dirección también se suprime en el tercer intento.

   Cuando una entrega se realiza correctamente después de un reintento, el contador de errores de la dirección se reinicia.

### Reintentos {#retries}

Si un mensaje falla debido a un rechazo temporal del tipo **Ignored** , los reintentos se realizarán durante **3,5 días** desde el momento en que el mensaje se agregó a la cola de correo electrónico.

El retardo mínimo entre reintentos y el número máximo de reintentos que se van a realizar es <!--managed by the Enhanced MTA,--> en función del rendimiento histórico y actual de una IP en un dominio determinado.

Después de 3,5 días, cualquier mensaje de la cola de reintentos se eliminará de la cola y se enviará de nuevo como una devolución.
