---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 570f50a86288378c26f967f4861f19b9da9f96cf
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 16%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la primera versión están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en la [notas de la versión](release-notes.md), en la fecha de lanzamiento.

## Notas de la versión anteriores de enero de 2024 {#e-2024}

**Fecha de lanzamiento**: 20-31 de enero de 2024

### Nuevas funciones{#e-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.


<table>
<thead>
<tr>
<th><strong>Actualizaciones de entrega</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora admite la tecnología de autenticación DMARC.</p>
<p>A partir del 1 de febrero de 2024, Google y Yahoo! requerirá que tenga un registro DMARC para cualquier dominio que utilice para enviarles correo electrónico. Asegúrese de tener configurado el registro DMARC para todos los subdominios que ha delegado o que está delegando al Adobe en Journey Optimizer.</p>
<!--img src="assets/channel-reports.png"/-->
<p>Para obtener más información, consulte la <a href="../configuration/dmarc-record.md">documentación detallada</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Manuales de casos de uso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveche un catálogo de libros de reproducción de casos de uso específicos del sector en Real-Time CDP y Journey Optimizer para abordar casos de uso comunes que puede realizar con Adobe Experience Platform y Adobe Recorrido Optimizer.</p><p>Una vez que haya elegido el libro de reproducción que mejor se adapte a sus necesidades, puede habilitarlo para generar los recursos necesarios para admitir su caso de uso, como recorridos, mensajes, esquemas o segmentos, y personalizarlos a su esquema para obtener un tiempo de valor más rápido.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
<!--<p>For more information, refer to the <a href="../start/playbooks.md">detailed documentation</a>.</p>-->
</tr>
</tbody>
</table>

### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Creación de informes**

* **Nuevos widgets de desglose basados en dominio** - Se han añadido nuevos widgets para mejorar los informes de Campaign y de Recorrido. El **Razones de rechazo por dominio**, **Enviados y entregados por dominios**, **Aperturas y clics por dominio** y **Rechazos y errores por dominio** los widgets proporcionan un desglose detallado a nivel de dominio para las métricas clave de envío y seguimiento de correo electrónico. [Más información](../reports/channel-report.md)

**Canal de SMS**

* **Inclusión doble** : el flujo de trabajo de inclusión doble para SMS garantiza que los usuarios se incluyan explícitamente en la recepción de mensajes cuando la solicitud se inicie desde su dispositivo. Los usuarios inician el proceso de consentimiento enviando un mensaje SMS entrante. Al confirmar su consentimiento, se envía un mensaje de seguimiento en el que se solicita la verificación final. Si no existe ningún perfil de usuario, se crea tras una confirmación correcta. [Más información](../sms/sms-configuration.md#create-api)

  Tenga en cuenta que esto solo se aplica a los proveedores de SMS de Sinch e Infobip.

**Recorridos**

* **Duración de eventos de reacción** - La duración máxima que puede definir en la variable **Eventos de reacción** ahora es 29 días en lugar de 30. [Más información](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Leer audiencia**  : la actividad Leer audiencia ahora se basa en el conjunto de datos de instantánea de perfil para segmentos por lotes, que solo se genera una vez al día después de ejecutar el trabajo por lotes diario programado, por lo que los datos se actualizarán hasta ese último trabajo por lotes diario.

* **Grupos de campos** - Se ha solucionado un problema que bloqueaba los grupos de campos para poder guardarlos en determinados casos.

**Reglas de frecuencia**

* **Límite de frecuencia semanal y diaria** : Ahora puede especificar el número máximo de mensajes enviados a un perfil de cliente en una semana o un día, además del mes. El límite de frecuencia se basa en el periodo de calendario seleccionado y se restablece al principio del lapso de tiempo correspondiente. [Más información](../configuration/frequency-rules.md#create-new-rule)

**Gestión de decisiones**

* **Límite de frecuencia en Edge** : El contador de límite de frecuencia ahora se actualiza y está disponible en una decisión de API de Edge Decisioning en menos de 3 segundos.