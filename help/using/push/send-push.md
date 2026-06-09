---
solution: Journey Optimizer
product: journey optimizer
title: Comprobación y envío de la notificación push
description: Obtenga información sobre cómo comprobar y enviar la notificación push en Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
TQID: https://experienceleague.adobe.com/QXJ9G3btsn7ZEwSB2Bm0uGt89gsh8D7SnNZ-Vw2muXM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 6%

---

# Comprobación y envío de la notificación push {#send-push}

## Previsualización de la notificación push {#preview-push}

Una vez definido el contenido del mensaje, puede previsualizar su contenido mediante cualquiera de los métodos de simulación:

* Haga clic en **[!UICONTROL Simular contenido]** para probar las variaciones de contenido con datos de entrada de muestra o generación automática de IA. [Aprenda a simular variaciones de contenido](../test-approve/simulate-sample-input.md)
* Haga clic en **[!UICONTROL Simular contenido]** y, a continuación, seleccione **[!UICONTROL Simular contenido (perfiles de AEP)]** en el menú desplegable para previsualizarlo con perfiles de prueba. Puede seleccionar el tipo de dispositivo para obtener una vista previa del contenido: **[!UICONTROL iOS]**, **[!UICONTROL Android]** o **[!UICONTROL Web]**.

![](assets/push_preview_3.png)

Encontrará información detallada sobre cómo obtener una vista previa y probar contenido en la sección [Administración de contenido](../content-management/preview-test.md).

## Validación de la notificación push {#push-validate}

Debe comprobar las alertas en la sección superior del editor. Algunas son simples advertencias, pero otras pueden impedir que envíe el mensaje. Pueden producirse dos tipos de alertas: advertencias y errores.

* **Advertencias** se refieren a recomendaciones y prácticas recomendadas.

* **Los errores** le impiden probar o activar la recorrido mientras no se resuelvan, como:

   * **[!UICONTROL La versión push del mensaje está vacía]**: este error se muestra cuando falta el cuerpo o el título de la notificación push. Aprenda a definir el contenido de las notificaciones push en [esta sección](create-push.md).

   * **[!UICONTROL la configuración no existe]**: no puede usar el mensaje si la configuración seleccionada se elimina después de la creación del mensaje. Si se produce este error, seleccione otra configuración en el mensaje **[!UICONTROL Propiedades]**. Obtenga más información acerca de las configuraciones de canal en [esta sección](../configuration/channel-surfaces.md).

   * **[!UICONTROL La carga de Push iOS/Android ha superado el límite de 4 KB]**: el tamaño de la notificación push no puede superar los 4 KB. Para respetar este límite, intente reducir el uso de imágenes o emojis. Aprenda a administrar el contenido de las notificaciones push en [esta sección](../push/create-push.md).

  ![](assets/push_alert.png)


>[!NOTE]
>
> Para mejorar la capacidad de envío, siempre debe utilizar los números de teléfono en los formatos admitidos por el proveedor. Por ejemplo, Twilio y Sinch solo admiten números de teléfono en formato E.164.

## Enviar la notificación push{#push-send}

>[!IMPORTANT]
>
> Si la campaña está sujeta a una directiva de aprobación, debe solicitar la aprobación para poder enviar la notificación push. [Más información](../test-approve/gs-approval.md)

Cuando el mensaje push esté listo, completa la configuración de tu [recorrido](../building-journeys/journey-gs.md) o [campaña](../campaigns/create-campaign.md) para enviarlo.

**Temas relacionados**

* [Configuración del canal push para dispositivos móviles](push-configuration.md)
* [Configuración del canal push para la web](push-configuration-web.md)
* [Informe de notificaciones push](../reports/journey-global-report-cja-push.md)
* [Crear una notificación push](create-push.md)
* [Añadir un mensaje en un recorrido](../building-journeys/journey-action.md)
* [Añadir un mensaje en una campaña](../campaigns/create-campaign.md)

