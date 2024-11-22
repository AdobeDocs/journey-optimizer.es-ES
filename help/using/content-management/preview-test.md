---
title: Previsualización y prueba del contenido
description: Obtenga información sobre cómo previsualizar y probar el contenido.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: a5eacd7a746b2f17804062b23aee3146db0434c9
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 26%

---

# Previsualización y prueba del contenido {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Compruebe cómo se representa el contenido"
>abstract="Una vez definido el contenido, puede utilizar perfiles de prueba para previsualizarlo y comprobar si la representación es correcta según el canal que utilice."

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="Compruebe cómo se representa el contenido"
>abstract="Una vez definido el contenido, puede previsualizarlo y comprobar si la renderización es correcta según el canal que utilice."

## Acerca de la vista previa y las pruebas {#about}

Una vez definido el contenido, puede obtener una previsualización de este antes de enviar el mensaje. Este es un paso crucial para garantizar que sea precisa, pero también que esté libre de errores, tanto en la configuración del contenido como de la personalización.

También puede enviar envíos de prueba de sus mensajes de correo electrónico a destinatarios o suscriptores específicos para realizar pruebas y validarlos, y comprobar su renderización en clientes populares de escritorio, móviles y basados en web.

>[!CAUTION]
>
>Al obtener una vista previa de un mensaje o enviar pruebas, solo se muestran los datos de personalización del perfil. Personalization basado en datos de contexto, como información de evento, solo se puede probar en el contexto de un recorrido. Aprenda a probar la personalización en [este caso de uso](../personalization/personalization-use-case.md).

Todas estas acciones se pueden realizar con el botón **[!UICONTROL Simular contenido]**, al que se puede acceder desde la pantalla de edición de contenido del mensaje, o desde el correo electrónico y los diseñadores web de los canales web y de correo electrónico.

![](../email/assets/email-preview-button.png)

Tenga en cuenta que necesita tener el permiso **[!DNL Manage Simulate Content]** incluido en el perfil de producto **[!DNL Content Library Manager]**. [Más información](../administration/ootb-product-profiles.md#content-library-manager).

## Pruebas con perfiles de prueba o datos de entrada de muestra {#methods}

Puede obtener una vista previa y probar el contenido mediante lo siguiente:

* **Perfiles de prueba**

  Utilice perfiles de prueba para previsualizar el contenido, enviar pruebas de correo electrónico y comprobar el procesamiento de correo electrónico. Si ha añadido campos personalizados, puede comprobar cómo se muestran utilizando datos de perfil de prueba. Para obtener más información, consulte estas secciones:

  ➡️ [Seleccionar perfiles de prueba](test-profiles.md)

  ➡️ [Vista previa del contenido mediante perfiles de prueba](preview.md)

  ➡️ [Enviar pruebas de correo electrónico](proofs.md)

  ➡️ [Comprobar procesamiento de correo electrónico](rendering.md)

  ➡️ [Vista previa y revisión del correo electrónico (vídeo)](#video-preview)

* **Datos de entrada de muestra**

  [!DNL Journey optimizer] le permite probar diferentes variantes del contenido previsualizándolo y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV / JSON, o añadidos manualmente.

  El sistema detecta automáticamente todos los atributos de perfiles utilizados en el contenido para la personalización y los puede utilizar en las pruebas para crear varias variantes.

  ➡️ [Aprenda a probar el contenido con datos de entrada de ejemplo](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >Actualmente, esta función está disponible para todos los clientes como una versión beta pública solo para los canales de correo electrónico, SMS y notificaciones push.

## Vídeo explicativo {#video-preview}

Aprenda a utilizar perfiles de prueba para probar el procesamiento de correos electrónicos en varias bandejas de entrada, previsualizar los correos electrónicos personalizados con perfiles de prueba y enviar pruebas.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
