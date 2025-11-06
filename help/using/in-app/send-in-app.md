---
title: Comprobación y envío de la notificación en la aplicación
description: Obtenga información sobre cómo comprobar y enviar un mensaje en la aplicación en Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, creación, inicio
exl-id: 9e9c235a-b78c-4669-af82-822b6f1e6fca
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 12%

---

# Comprobación y envío de la notificación en la aplicación {#create-in-app}

## Previsualización en el dispositivo {#preview-device}

Si desea echar un vistazo a la notificación en la aplicación antes de que se active para todos los usuarios, puede previsualizarla en un dispositivo específico. Esta funcionalidad le permite asegurarse de que la notificación tenga el aspecto y el funcionamiento previstos en el dispositivo elegido, lo que proporciona una mejor experiencia de usuario para la audiencia.

Para ello, siga los pasos a continuación:

1. Haga clic en **[!UICONTROL Vista previa en el dispositivo]**.

   ![](assets/in_app_create_6.png)

1. En la ventana **[!UICONTROL Conectarse al dispositivo]**, haga clic en **[!UICONTROL Iniciar]**.

1. Escriba la **[!UICONTROL URL base]** de su aplicación y haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/in_app_create_7.png)

1. Escanee el código QR con su dispositivo e introduzca el código PIN mostrado.

El mensaje en la aplicación ahora se puede activar directamente en el dispositivo, lo que le permite previsualizar y revisar el mensaje en un dispositivo real.

## Vista previa con perfiles de prueba {#simulate}

Una vez definido el mensaje en la aplicación, puede utilizar perfiles de prueba para previsualizarlo. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje con los datos del perfil de prueba.

Para ello, haga clic en **[!UICONTROL Simular contenido]** y añada un perfil de prueba para comprobar el mensaje con los datos del perfil de prueba.

Encontrará información detallada sobre cómo seleccionar perfiles de prueba y obtener una vista previa del contenido en la sección [Administración de contenido](../content-management/preview-test.md).

## Revisión y activación de la notificación en la aplicación{#in-app-review}

>[!IMPORTANT]
>
> Si la campaña está sujeta a una directiva de aprobación, deberá solicitar la aprobación para poder enviar la notificación en la aplicación. [Más información](../test-approve/gs-approval.md)

Una vez creado el mensaje en la aplicación y definido y personalizado su contenido, puede revisarlo y activarlo.

Para ello, siga los pasos a continuación:

1. Use el botón **[!UICONTROL Revisar para activar]** para ver un resumen del mensaje.

   El resumen le permite modificar la campaña si es necesario y comprobar si algún parámetro es incorrecto o falta.

   ![](assets/in_app_create_5.png)

1. Compruebe que la campaña esté configurada correctamente y luego haga clic en **[!UICONTROL Activar]**.

La campaña está activada. La notificación en la aplicación configurada en la campaña se envía inmediatamente o en la fecha especificada.

Una vez enviado, puede medir el impacto de los mensajes en la aplicación dentro de los informes Campaña o Recorrido. Para obtener más información sobre la creación de informes, consulte [esta sección](../reports/campaign-global-report-cja-inapp.md).

**Temas relacionados:**

* [Creación de un mensaje en la aplicación ](create-in-app.md)
* [Diseño de un mensaje en la aplicación](design-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report-cja-inapp.md)
* [Configuración en la aplicación](inapp-configuration.md)
