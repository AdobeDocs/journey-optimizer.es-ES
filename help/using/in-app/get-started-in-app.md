---
title: Introducción a la mensajería en la aplicación
description: Obtenga información sobre cómo enviar notificaciones en la aplicación con Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, creación, inicio
exl-id: 51562843-7b50-4eb5-bf79-5ce03f7549cb
TQID: https://experienceleague.adobe.com/b139LQsPe3HwKe1O5cyBx4Nj4jpW3GXCFIVIWTAIlbg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: cc5c44e2-54a1-4927-b794-442cd87d8f74
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 601
ht-degree: 43%

---

# Introducción al canal en la aplicación {#gs-in-app}

>[!BEGINSHADEBOX]

**En esta página:** empiece a usar el canal de mensajería en la aplicación en Adobe Journey Optimizer para atraer a los usuarios de la aplicación con notificaciones que promocionen funciones, ofertas e incorporación.

>[!ENDSHADEBOX]

Los mensajes en la aplicación son notificaciones que se pueden enviar a los usuarios dentro de la aplicación y les guía a puntos de interés específicos. Estas notificaciones se pueden utilizar para distintos fines, como la promoción de nuevas funciones, la presentación de ofertas especiales o la facilitación de la incorporación del usuario. Al aprovechar los mensajes en la aplicación, puede interactuar con su público y dirigirlos hacia aspectos importantes de su aplicación.

Utilice Journey Optimizer para crear notificaciones en la aplicación y configurar las opciones de experiencia, incluidas las opciones de diseño y visualización de mensajes, texto y botones.

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="inapp-configuration.md">
<img alt="Validación" src="../assets/do-not-localize/inapp-config.jpg">
</a>
<div>
<a href="inapp-configuration.md"><strong>Configurar el canal en la aplicación</strong></a>
</div>
<p>
</td>
<td>
<a href="create-in-app.md">
<img alt="Posible cliente" src="../assets/do-not-localize/inapp-create.jpeg">
</a>
<div><a href="create-in-app.md"><strong>Creación de un mensaje en la aplicación</strong>
</div>
<p>
</td>
<td>
<a href="design-in-app.md">
<img alt="Poco frecuente" src="../assets/do-not-localize/inapp-design.jpg">
</a>
<div>
<a href="design-in-app.md"><strong>Diseño del contenido en la aplicación</strong></a>
</div>
<p></td>
<td>
<a href="../reports/campaign-global-report-cja-inapp.md">
<img alt="Validación" src="../assets/do-not-localize/inapp-report.jpg">
</a>
<div>
<a href="../reports/campaign-global-report-cja-inapp.md"><strong>Acceso a informes en la aplicación</strong></a>
</div>
<p>
</td>
</tr></table>

## Casos de uso

Los mensajes en la aplicación funcionan mejor cuando desea guiar o influir en los usuarios mientras estos ya están comprometidos con la aplicación, aprovechando ese momento de atención activa.

| Ventaja | Por qué | Casos de uso de ejemplo |
| --- | --- | --- |
| Alta participación del usuario | Llega a los usuarios mientras están activos en una sesión de la aplicación | Anuncios de funciones, sugerencias de incorporación |
| Déclencheur relevantes para el contexto | Se puede activar según el comportamiento o la ubicación dentro de la aplicación | Resaltar una función justo después de que un usuario visite una pantalla relacionada |
| Entrega en tiempo real | Sin dependencia de tokens push ni servicios de envío externos | Mensajes con distinción de tiempo que se muestran durante la sesión actual |
| Sin dependencia de canales externos | Funciona completamente dentro de la aplicación, independientemente del estado de inclusión de otros canales | Llegar a los usuarios que han excluido las notificaciones push |
| Mejor potencial de conversión | Entregado en un momento de atención activa, aumentando las tasas de respuesta | Ofertas de ampliación de venta o de venta cruzada, indicadores de encuestas |
| Personalización y segmentación | El diseño, el texto y los botones se pueden adaptar a audiencias específicas | Flujos de incorporación personalizados para diferentes segmentos de usuario |
| Diseño no intrusivo | Se puede diseñar para complementar la experiencia del usuario en lugar de interrumpirla | Titulares o modelos que se alinean con la interfaz de usuario de la aplicación |

## Cuándo no utilizar

Los mensajes en la aplicación dependen de una sesión activa, por lo que no son adecuados para todos los escenarios. Considere otro canal en las siguientes situaciones:

* El usuario no está utilizando la aplicación de forma activa, ya que el mensaje nunca se mostrará
* El mensaje es un problema crítico o sensible al tiempo que requiere llegar a los usuarios fuera de la aplicación, como una interrupción o una alerta de seguridad
* La comunicación es reglamentaria o legal y requiere una confirmación de lectura que los mensajes en la aplicación no pueden proporcionar
* El objetivo es la reactivación de cuentas o una campaña de recuperación para los usuarios inactivos que es poco probable que abran la aplicación
* El mensaje es una actualización transaccional de gran volumen, como una confirmación de pedido, más adecuada para correos electrónicos o SMS
* El uso excesivo puede provocar ceguera en los banners, donde los usuarios comienzan a ignorar los mensajes que aparecen con demasiada frecuencia
* Los usuarios pueden estar sin conexión o sin conectividad de la aplicación cuando el mensaje está pensado para enviarse



## Recursos adicionales

* **[Cree mensajes en la aplicación](create-in-app.md)**: aprenda a crear y configurar mensajes en la aplicación para aplicaciones móviles.
* **[Configure un canal en la aplicación](inapp-configuration.md)**: configure su canal de mensajería en la aplicación con las configuraciones adecuadas de la aplicación móvil.
* **[Diseñe contenido en la aplicación](design-in-app.md)**: personalice diseños de mensajes, estilos, botones y elementos interactivos en la aplicación.
* **[En la aplicación para la web](create-in-app-web.md)**: descubra cómo crear y enviar mensajes en la aplicación para aplicaciones web.
* **[Tutoriales de canal en la aplicación](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/channels/in-app-channel/in-app-messages-overview){target="_blank"}**: explore tutoriales de vídeo paso a paso sobre las funciones y prácticas recomendadas de la mensajería en la aplicación.

