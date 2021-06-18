---
title: Vista previa de mensajes y envío de pruebas
description: Obtenga información sobre cómo previsualizar y probar los mensajes
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: f3421d6fcbf7400b8db344366be596e0bede762b
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 0%

---

# Previsualizar y probar los mensajes{#preview-and-proof}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo. Si ha insertado [contenido personalizado](personalization/personalize.md), podrá comprobar cómo se muestra este contenido en el mensaje, aprovechando los datos de perfil de prueba.

Para detectar posibles errores en el contenido del correo electrónico o en la configuración de personalización, envíe pruebas a los perfiles de prueba. Se debe enviar una prueba cada vez que se realiza un cambio para validar el contenido más reciente.

>[!CAUTION]
>
>Debe tener perfiles de prueba disponibles para poder previsualizar los mensajes y enviar pruebas.
>
>Aprenda a crear perfiles de prueba en [esta página](building-journeys/creating-test-profiles.md).


Para probar el contenido del mensaje, debe:

* [seleccionar perfiles de prueba](#select-test-profiles)
* [comprobar la vista previa del mensaje](#preview-your-messages)

A continuación, podrá [enviar pruebas](#send-proofs) a sus perfiles de prueba.

Además, aproveche su cuenta **Litmus** en [!DNL Journey Optimizer] para previsualizar instantáneamente su **procesamiento de correo electrónico** en clientes de correo electrónico populares. A continuación, puede asegurarse de que el contenido del correo electrónico tenga un aspecto bueno y funcione correctamente en cada bandeja de entrada. Aprenda a desbloquear las vistas previas de correo electrónico de Litmus en [esta sección](#email-rendering)

>[!CAUTION]
>
>Al obtener una vista previa de un mensaje o enviar pruebas, solo se muestran los datos de personalización del perfil. La personalización basada en datos de contexto, como la información de evento, solo se puede probar en el contexto de un recorrido. Aprenda a probar la personalización en [este caso de uso](personalization/personalization-use-case.md).


## Seleccionar perfiles de prueba{#select-test-profiles}

Utilice [Test profiles](building-journeys/creating-test-profiles.md) para dirigirse a destinatarios adicionales que no coincidan con los criterios de objetivo definidos.

Para seleccionar perfiles de prueba, siga los pasos a continuación:

1. En la interfaz de mensajes o en el diseñador de correo electrónico, haga clic en el botón **[!UICONTROL Show preview]** para acceder a la selección de perfil de prueba.

   ![](assets/email-preview-button.png)

1. Seleccione el espacio de nombres que se utilizará para identificar los perfiles de prueba haciendo clic en el icono de selección **[!UICONTROL Identity namespace]** .

   ![](assets/previewselect-namespace.png)

   Obtenga más información sobre los áreas de nombres de identidad [de Adobe Experience Platform en esta sección](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=en#getting-started).

   En el siguiente ejemplo, utilizaremos el espacio de nombres **Email**.

1. Utilice el campo de búsqueda para encontrar el área de nombres, selecciónela y haga clic en **[!UICONTROL Select]**

   ![](assets/preview-email-namespace.png)

1. Introduzca el valor para identificar el perfil de prueba y haga clic en **[!UICONTROL Find test profile]**.

   ![](assets/preview-identity-value.png)

1. Si ha añadido personalización en el mensaje, añada otros perfiles para poder probar distintas variantes del mensaje en función de los datos del perfil. Una vez añadidos, los perfiles se muestran en los campos de selección.

   ![](assets/preview-profile-list.png)

   En función de los elementos de personalización de mensajes, esta lista muestra los datos de cada perfil de prueba en las columnas relacionadas.

## Vista previa de mensajes{#preview-your-messages}

Una vez seleccionados los [perfiles de prueba](#select-test-profiles), puede obtener una vista previa de los mensajes y comprobar el contenido.

1. Haga clic en la pestaña **[!UICONTROL Preview]** para probar el mensaje.

1. Seleccione un perfil de prueba. Puede comprobar los valores disponibles en las columnas. Utilice las flechas derecha/izquierda para examinar los datos.

   ![](assets/preview-tab-select-profile.png)

1. Haga clic en el icono **[!UICONTROL Select data]** situado encima de la lista para añadir o quitar columnas.

   ![](assets/preview-select-data.png)

   Puede ver campos de personalización específicos del mensaje actual al final de la lista. En este ejemplo, la ciudad del perfil, el nombre y los apellidos. Seleccione esos campos y asegúrese de que estos valores se rellenen en los perfiles de prueba.

1. En la vista previa del mensaje, los elementos personalizados se sustituyen por los datos de perfil de prueba seleccionados.

   Por ejemplo, para este mensaje, el contenido del correo electrónico y el asunto del correo electrónico están personalizados:

   ![](assets/preview-test-profile.png)

1. Seleccione otros perfiles de prueba para previsualizar el procesamiento de correo electrónico para cada variante del mensaje.

Para una vista previa de notificaciones push:

1. Cambie al canal **[!UICONTROL Push]** desde la lista desplegable **[!UICONTROL Channels]** situada en la parte superior izquierda de la pantalla **[!UICONTROL Preview]**.

   ![](assets/preview-select-channel.png)

1. Siga los mismos pasos que se describen anteriormente para seleccionar un perfil de prueba y seleccione el tipo de dispositivo para obtener una vista previa del contenido: **[!UICONTROL iOS]** o **[!UICONTROL Android]**

   ![](assets/preview-iOS.png)

1. En la vista previa push, los datos de perfil de prueba se aprovechan en el contenido del mensaje.

   Por ejemplo, para esta notificación push, el título y el cuerpo están personalizados:

   ![](assets/preview-android.png)

## Envío de pruebas{#send-proofs}

Una prueba es un mensaje específico que le permite probar un mensaje antes de enviarlo a la audiencia principal. Los destinatarios de la prueba se encargan de aprobar el mensaje: renderización, contenido, configuración de personalización, configuración.

Una vez seleccionados los [perfiles de prueba](#select-test-profiles), puede enviar pruebas.

1. En la pantalla **[!UICONTROL Preview]**, haga clic en el botón **[!UICONTROL Send proof]**.

   ![](assets/send-proof-button.png)

1. Seleccione los perfiles de prueba que recibirán la prueba y haga clic en **[!UICONTROL Send proof]**. Puede añadir un prefijo a la línea de asunto de la prueba si es necesario.

   ![](assets/send-proof-select.png)

1. Vuelva a la pantalla **[!UICONTROL Preview]**, haga clic en el botón **[!UICONTROL View proofs]** para comprobar el estado.

   ![](assets/send-proof-view.png)

Debe enviar pruebas después de cualquier modificación en el contenido del mensaje.

>[!NOTE]
>
> En la prueba enviada a los perfiles de prueba, el vínculo a la página espejo no está activo. Solo se activa en los mensajes finales.

## Procesamiento de correo electrónico{#email-rendering}

Puede aprovechar su cuenta **Litmus** en [!DNL Journey Optimizer] para previsualizar instantáneamente su **procesamiento de correo electrónico** en los clientes de correo electrónico más populares.

Para acceder a las funciones de procesamiento de correo electrónico, debe:

* Tener una cuenta de Litmus
* [Seleccionar perfiles de prueba](#select-test-profiles)

A continuación, siga los pasos a continuación:

1. En el Diseñador de correo electrónico, haga clic en el botón **[!UICONTROL Preview]** y seleccione la pestaña **[!UICONTROL Email rendering]**.

1. Haga clic en **Conecte su cuenta de Litmus** en la sección superior derecha.

   ![](assets/email-rendering-litmus.png)

1. Introduzca sus credenciales e inicie sesión.

   ![](assets/email-rendering-credentials.png)

1. Haga clic en el botón **Run test** para generar vistas previas por correo electrónico.

1. Compruebe el contenido del correo electrónico en los clientes populares de escritorio, móviles y basados en la web.

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>Al conectar su cuenta **Litmus** con [!DNL Journey Optimizer], acepta que los mensajes de prueba se envíen a Litmus: una vez enviados, estos correos electrónicos ya no se administran mediante Adobe. Como consecuencia, la política de retención de datos de Litmus por correo electrónico se aplica a estos correos electrónicos, incluidos los datos de personalización que pueden incluirse en estos mensajes de prueba.

