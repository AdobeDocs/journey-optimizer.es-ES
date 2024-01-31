---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0c428b18469eb98392fe6c49d5892a4699477457
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 27%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras de las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Notas de la versión anteriores de enero de 2024 {#jan-2024}

**Fecha de lanzamiento**: 30-31 de enero de 2024

### Nuevas funciones{#jan24-features}

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
<p>Para obtener más información, consulte la <a href="../configuration/dmarc-record-update.md">documentación detallada</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
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
<p>Para obtener más información, consulte la <a href="../start/playbooks.md">documentación detallada</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Mejoras {#jan24-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Creación de informes**

* **Nuevos widgets de desglose basados en dominio** - Se han añadido nuevos widgets para mejorar los informes de Campaign y de Recorrido. El **Razones de rechazo por dominio**, **Enviados y entregados por dominios**, **Aperturas y clics por dominio** y **Rechazos y errores por dominio** los widgets proporcionan un desglose detallado a nivel de dominio para las métricas clave de envío y seguimiento de correo electrónico. [Más información](../reports/channel-report.md)

**Canal de SMS**

* **Inclusión doble** : el flujo de trabajo de inclusión doble para SMS garantiza que los usuarios se incluyan explícitamente en la recepción de mensajes cuando la solicitud se inicie desde su dispositivo. Los usuarios inician el proceso de consentimiento enviando un mensaje SMS entrante. Al confirmar su consentimiento, se envía un mensaje de seguimiento en el que se solicita la verificación final. Si no existe ningún perfil de usuario, se crea tras una confirmación correcta. [Más información](../sms/sms-configuration.md#create-api)

  Tenga en cuenta que esta capacidad está disponible con proveedores de SMS de Sinch e Infobip.

**Recorridos**

* **Duración de eventos de reacción** - La duración máxima que puede definir en la variable **Eventos de reacción** ahora es 29 días en lugar de 30. [Más información](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Leer audiencia**  - El **Leer audiencia** la actividad ahora depende del conjunto de datos de instantánea de perfil para segmentos de lote, que solo se genera una vez al día después de ejecutar el trabajo por lotes diario programado, por lo que los datos se actualizarán hasta ese último trabajo por lotes diario.

* **Grupos de campos** - Esta versión corrige un problema que bloqueaba que los grupos de campo se guardaran en ciertos casos.

**Reglas de frecuencia**

* **Límite de frecuencia semanal y diaria** : Ahora puede especificar el número máximo de mensajes enviados a un perfil de cliente en una semana o un día, además del mes. El límite de frecuencia se basa en el periodo de calendario seleccionado y se restablece al principio del lapso de tiempo correspondiente. [Más información](../configuration/frequency-rules.md#create-new-rule)

**Gestión de decisiones**

* **Límite de frecuencia en Edge** : El contador de límite de frecuencia ahora se actualiza y está disponible en una decisión de API de Edge Decisioning en menos de 3 segundos.