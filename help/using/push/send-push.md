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
source-git-commit: af40716070ab28001acb6f5c02f41a0ec3ad8258
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 6%

---

# Comprobación y envío de la notificación push {#send-push}

## Previsualización de la notificación push {#preview-push}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente para previsualizar su contenido. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje.

Para ello, haga clic en **[!UICONTROL Simular contenido]**. Puede seleccionar el tipo de dispositivo para obtener una vista previa del contenido: **[!UICONTROL iOS]** o **[!UICONTROL Android]**.

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
* [Informe de notificaciones push](../reports/journey-global-report-cja-push.md)
* [Crear una notificación push](create-push.md)
* [Añadir un mensaje en un recorrido](../building-journeys/journeys-message.md)
* [Añadir un mensaje en una campaña](../campaigns/create-campaign.md)

