---
title: Vista previa y prueba del contenido
description: Obtenga información sobre cómo previsualizar y probar el contenido.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 97%

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

## Acerca de la vista previa y la prueba {#about}

Una vez definido el contenido, puede obtener una vista previa del mismo antes de enviar el mensaje. Es un paso crucial para garantizar que sea preciso, pero también que no haya errores, tanto en la configuración del contenido como de la personalización.

También puede realizar envíos de prueba de sus mensajes de correo electrónico a destinatarios o suscriptores específicos para realizar pruebas y validarlos, y comprobar cómo se representan en los clientes de escritorio, móviles y basados en web más conocidos.

>[!CAUTION]
>
>Al obtener una vista previa de un mensaje o enviar pruebas, solo se muestran los datos de personalización del perfil. La personalización basada en datos de contexto, como la información del evento, solo se puede probar en el contexto de un recorrido. Obtenga información sobre cómo probar la personalización en [este caso de uso](../personalization/personalization-use-case.md).

Todas estas acciones se pueden realizar con el botón **[!UICONTROL Simular contenido]**, al que se puede acceder desde la pantalla de edición de contenido del mensaje, o desde el correo electrónico y los diseñadores web de los canales web y de correo electrónico.

![](../email/assets/email-preview-button.png)

Tenga en cuenta que necesita tener el permiso **[!DNL Manage Simulate Content]** incluido en el perfil de producto **[!DNL Content Library Manager]**. [Más información](../administration/ootb-product-profiles.md#content-library-manager).

## Pruebas con perfiles de prueba o datos de entrada de muestra {#methods}

Puede obtener una vista previa y probar el contenido mediante lo siguiente:

* **Perfiles de prueba**

  Utilice perfiles de prueba para previsualizar el contenido, enviar pruebas de correo electrónico y comprobar la representación de correo electrónico. Si ha añadido campos personalizados, puede comprobar cómo se muestran utilizando datos de perfil de prueba. Para obtener más información, consulte estas secciones:

  ➡️ [Seleccionar perfiles de prueba](test-profiles.md)

  ➡️ [Vista previa del contenido mediante perfiles de prueba](preview.md)

  ➡️ [Envío de pruebas de correo electrónico](proofs.md)

  ➡️ [Comprobar representación de correo electrónico](rendering.md)

  ➡️ [Vista previa y revisión del correo electrónico (vídeo)](#video-preview)

* **Datos de entrada de muestra**

  [!DNL Journey optimizer] ahora le permite probar diferentes variantes del contenido del correo electrónico previsualizándolo y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV o JSON o añadidos manualmente. 

  El sistema detecta automáticamente todos los atributos de perfiles utilizados en el contenido para la personalización y los puede utilizar en las pruebas para crear varias variantes.

  ➡️ [Obtenga información sobre cómo probar el contenido con datos de entrada de muestra](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >Actualmente, todos los clientes tienen esta posibilidad disponible como una versión Beta pública, para los canales de correo electrónico, SMS y notificaciones push solamente.

## Vídeo práctico {#video-preview}

Aprenda a utilizar perfiles de prueba para probar el renderizado de correos electrónicos en varias bandejas de entrada, previsualizar los correos electrónicos personalizados con perfiles de prueba y enviar pruebas.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
