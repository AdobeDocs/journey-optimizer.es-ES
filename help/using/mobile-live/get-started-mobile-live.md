---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las actividades en directo
description: Obtenga información sobre cómo enviar actividades en directo en Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: c6b36f31af29d21053cc455fd5dbba68ed5af63b
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 20%

---

# Introducción a las actividades en directo {#get-started-mobile-live}


Las actividades activas son elementos de interfaz de usuario persistentes y visibles que se muestran en la pantalla de bloqueo del dispositivo. Permiten que la aplicación presente información actualizada en tiempo real, lo que mantiene a los usuarios informados durante un evento en curso sin pedirles que abran la aplicación ni recibir notificaciones push repetidas.

>[!AVAILABILITY]
>
>Las actividades activas en Adobe Journey Optimizer solo son compatibles con Apple iOS.

A diferencia de las notificaciones push tradicionales, las actividades en directo representan **participación basada en el estado**: en lugar de enviar alertas únicas, mantienen una presencia contextual continua que se actualiza dinámicamente a medida que evolucionan los eventos.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="Actividades de iOS Live en Bloquear pantalla y Dynamic Island" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>Ventajas principales</strong></p>
<p>Las actividades activas cambian la participación móvil de basada en notificaciones a basada en el estado, lo que permite a las marcas lo siguiente:</p>
<ul>
<li>Mantener una <strong>presencia continua</strong> en la pantalla de bloqueo durante los eventos de alto valor</li>
<li><strong>Actualizar información dinámicamente</strong> sin saturar a los usuarios con notificaciones repetidas</li>
<li>Entregue <strong>momentos móviles más completos y contextuales</strong> vinculados a eventos reales</li>
<li><strong>Aumentar la participación y la retención</strong> durante transacciones activas o experiencias en directo</li>
</ul>
</td>
</tr>
</table>

Con Adobe Journey Optimizer, puede **iniciar**, **actualizar** y **finalizar** actividades en directo de forma remota mediante campañas activadas por API, lo que admite casos de uso individuales y basados en audiencias a escala.

Las actividades activas **solo** se pueden iniciar a través de **campañas activadas por API**, lo que le permite proporcionar cargas útiles personalizadas y realizar toda la personalización a través de su propia carga útil.
El tipo de campaña **activado por API** apropiado debe estar seleccionado según el caso de uso de actividad en directo deseado:

* Seleccione **Marketing activado por API** para casos de uso de difusión — actualizaciones basadas en audiencias enviadas a escala:

   * Puntuaciones deportivas y cuenta atrás de eventos en directo
   * Actualizaciones del estado del vuelo para todos los pasajeros de una ruta
   * Experiencias compartidas en un segmento de usuario

* Seleccione **Transaccional activado por API** para casos de uso individuales — 1:1 actualizaciones en tiempo real por usuario:

   * Seguimiento de pedidos y progreso de entrega
   * Actualizaciones del estado del servicio o del viaje
   * Confirmaciones de reservas y citas en tiempo real

## Guía de inicio rápido

Complete los pasos siguientes para configurar e implementar actividades en directo en su aplicación:

1. **[Configurar Adobe Journey Optimizer](mobile-live-configuration.md)**

   Configure su entorno creando una configuración móvil.

1. **[Integrar el SDK móvil de Adobe Experience Platform](mobile-live-configuration-sdk.md)**

   Intégrese con el SDK móvil de Adobe Experience Platform para habilitar actualizaciones dinámicas en tiempo real en la pantalla de bloqueo y Dynamic Island.

1. **[Crear una actividad en vivo en Journey Optimizer](create-mobile-live.md)**

   Utilice campañas activadas por API en Journey Optimizer para iniciar su actividad en directo.

1. **[Seguir las campañas](../reports/campaign-global-report-cja-activity.md)**

   Empiece a medir el impacto de su actividad en directo con los informes integrados.

## Vídeo práctico

Descubre cómo configurar las actividades de iOS Live con Adobe Journey Optimizer para ofrecer actualizaciones enriquecidas en tiempo real en la pantalla de bloqueo de iPhone y Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479867/?captions=spa&learn=on)
