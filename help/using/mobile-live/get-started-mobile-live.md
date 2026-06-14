---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las actividades en directo
description: Obtenga información sobre cómo enviar actividades en directo en Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
TQID: https://experienceleague.adobe.com/IB00r0QSfCthvgvyqubGwsaUoiJKBL-E96duLn4R5i0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: ed2fba79-65cb-4680-96d2-2ad5d851714d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0977b7c36d8556d4aaed43f4b94abb4ccacd2305
workflow-type: tm+mt
source-wordcount: 449
ht-degree: 84%

---

# Introducción a las actividades en directo {#get-started-mobile-live}

>[!BEGINSHADEBOX]

**En esta página:** Descubra cómo las actividades de Live ofrecen actualizaciones persistentes y en tiempo real en la pantalla de bloqueo de iPhone y en Dynamic Island para que pueda mantener a los usuarios ocupados durante los eventos en curso y planificar la configuración y las campañas activadas por API necesarias para enviarlas con Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Las actividades en directo son elementos de interfaz de usuario persistentes y visibles que se muestran en la pantalla de bloqueo del dispositivo. Permiten que la aplicación presente información actualizada en tiempo real, lo que mantiene a los usuarios informados durante un evento en curso sin pedirles que abran la aplicación ni que reciban notificaciones push repetidas.

>[!AVAILABILITY]
>
>Las actividades en directo de Adobe Journey Optimizer solo son compatibles con Apple iOS.

A diferencia de las notificaciones push tradicionales, las actividades en directo representan una **participación basada en el estado**: en lugar de enviar alertas únicas, mantienen una presencia contextual continua que se actualiza dinámicamente a medida que evolucionan los eventos.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="Actividades en directo de iOS en Pantalla de bloqueo y Dynamic Island" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>Ventajas principales</strong></p>
<p>Las actividades en directo cambian la participación móvil de basada en notificaciones a basada en el estado, lo que permite a las marcas lo siguiente:</p>
<ul>
<li>Mantener una <strong>presencia continua</strong> en la pantalla de bloqueo durante los eventos de alto valor</li>
<li><strong>Actualizar información dinámicamente</strong> sin saturar a los usuarios con notificaciones repetidas</li>
<li>Entregar <strong>momentos móviles más completos y contextuales</strong> vinculados a eventos reales</li>
<li><strong>Aumentar la participación y la retención</strong> durante transacciones activas o experiencias en directo</li>
</ul>
</td>
</tr>
</table>

Con Adobe Journey Optimizer, puede **iniciar**, **actualizar** y **finalizar** actividades en directo de forma remota y mediante programación a través de campañas activadas por API, lo que admite casos de uso individuales y basados en públicos a escala.

Las actividades activas **solo** se pueden iniciar a través de **campañas activadas por API**, lo que le permite proporcionar cargas útiles personalizadas y realizar toda la personalización a través de su propia carga útil.
El tipo de campaña **activado por API** adecuado debe estar seleccionado según el caso de uso de actividad en directo deseado:

* Seleccione **Marketing activado por API** para casos de uso de difusión, es decir, actualizaciones basadas en públicos enviadas a escala:

   * Puntuaciones deportivas y cuenta atrás de eventos en directo
   * Actualizaciones del estado del vuelo para todos los pasajeros de una ruta
   * Experiencias compartidas en un segmento de usuario

* Seleccione **Transaccional activado por API** para casos de uso individuales — 1:1 actualizaciones en tiempo real por usuario:

   * Seguimiento del pedido y estado del envío
   * Actualizaciones del estado del servicio o del viaje
   * Confirmaciones de reservas y citas en tiempo real

## Guía de inicio rápido

Complete los pasos siguientes para configurar e implementar actividades en directo en su aplicación:

1. **[Configurar Adobe Journey Optimizer](mobile-live-configuration.md)**

   Configure su entorno creando una configuración móvil.

1. **[Integrar el SDK móvil de Adobe Experience Platform](mobile-live-configuration-sdk.md)**

   Intégrese con el SDK móvil de Adobe Experience Platform para habilitar actualizaciones dinámicas en tiempo real en la pantalla de bloqueo y Dynamic Island.

1. **[Crear una actividad en directo en Journey Optimizer](create-mobile-live.md)**

   Utilice campañas activadas por API en Journey Optimizer para iniciar su actividad en directo.

1. **[Seguir las campañas](../reports/campaign-global-report-cja-activity.md)**

   Empiece a medir el impacto de su actividad en directo con los informes integrados.

## Vídeo tutorial

Descubra cómo configurar las actividades en directo de iOS con Adobe Journey Optimizer para ofrecer actualizaciones enriquecidas en tiempo real en la pantalla de bloqueo de iPhone y Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
