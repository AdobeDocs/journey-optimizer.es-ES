---
solution: Journey Optimizer
product: journey optimizer
title: Publicar el recorrido
description: Obtenga información sobre cómo publicar un recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 5%

---

# Publicación del recorrido {#publishing-the-journey}

Debe publicar un recorrido para activarlo y hacer que esté disponible para que los nuevos perfiles lo introduzcan. Antes de publicar el recorrido, compruebe que sea válido y que no haya ningún error. No se puede publicar un recorrido con errores.

➡️ [Descubra esta función en vídeo](#video)

Los pasos para publicar un recorrido se detallan a continuación:

1. Antes de publicar el recorrido, compruebe que sea válido y que no haya ningún error. No podrá publicar un recorrido con errores.

   * Aprenda a probar su recorrido en [esta página](testing-the-journey.md).
   * Aprenda a solucionar los errores de recorrido en [esta sección](../building-journeys/troubleshooting.md#checking-for-errors-before-testing).

1. Para publicar el recorrido, haga clic en la opción **[!UICONTROL Publicar]**, que se encuentra en el menú desplegable superior derecho.

   >[!NOTE]
   >
   > Si el recorrido está sujeto a una directiva de aprobación, debe solicitar la aprobación para poder publicar el recorrido. [Más información](../test-approve/gs-approval.md)


   ![](assets/journeyuc1_18.png)

Cuando se publica el recorrido, está en modo **solo lectura**. Cuando un recorrido es de solo lectura, solo puede modificar las etiquetas y descripciones de la actividad, el nombre del recorrido y la descripción del recorrido. Si necesita hacer más modificaciones en un recorrido publicado, cree [una nueva versión](journey-ui.md#journey-versions) del recorrido.

Cuando se detiene un recorrido, se detiene permanentemente: todas las personas que fluyen en el recorrido se detienen permanentemente, y el recorrido deja de permitir nuevas entradas. Si necesita volver a ejecutar el recorrido, debe duplicarlo y publicar el nuevo recorrido.


>[!IMPORTANT]
>
>Si se realizan cambios en una decisión de oferta que se utiliza en el mensaje de un recorrido, se debe cancelar la publicación del recorrido y volver a publicarlo.  Esto garantizará que los cambios se incorporen al mensaje del recorrido y que el mensaje sea coherente con las últimas actualizaciones.

## Vídeo práctico {#video}

Obtenga información sobre cómo publicar un recorrido en este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)