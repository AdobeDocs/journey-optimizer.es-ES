---
solution: Journey Optimizer
product: journey optimizer
title: Previsualización de mensajes y envío de pruebas
description: Obtenga información sobre cómo previsualizar y probar el correo electrónico
feature: Preview, Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: vista previa, contenido, correo electrónico, prueba, prueba, perfil
exl-id: f2c2a360-a4b2-4416-bbd0-e27dd014e4ac
source-git-commit: 45f19563c79d298eeec6cb757636a9ce47e54adf
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 10%

---

# Previsualizar y probar el correo electrónico {#preview-and-proof}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Previsualizar y probar sus mensajes"
>abstract="Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo."

Una vez definido el contenido del correo electrónico, puede utilizar perfiles de prueba para previsualizarlo y probarlo. Si ha insertado [contenido personalizado](../personalization/personalize.md), puede comprobar cómo se muestra este contenido en el mensaje mediante los datos de perfil de prueba.

Para detectar posibles errores en el contenido del correo electrónico o la configuración de personalización, envíe pruebas a los perfiles de prueba. Se debe enviar una prueba cada vez que se realiza un cambio para validar el contenido más reciente.

>[!CAUTION]
>
>Debe tener perfiles de prueba disponibles para poder previsualizar los mensajes y enviar pruebas.
>
>Aprenda a crear perfiles de prueba en [esta página](../audience/creating-test-profiles.md).

Para probar el contenido del correo electrónico, debe:

* [Seleccionar perfiles de prueba](#select-test-profiles)
* [Compruebe la previsualización del mensaje](#preview-your-messages)

Entonces, podrá hacer lo siguiente [envío de pruebas](#send-proofs) a sus perfiles de prueba.

Además, aproveche la cuenta **Litmus** en [!DNL Journey Optimizer] para previsualizar instantáneamente su **procesamiento de correo electrónico** en clientes de correo electrónico populares. A continuación, puede asegurarse de que el contenido del correo electrónico tenga buen aspecto y funcione correctamente en cada bandeja de entrada. Obtenga información sobre cómo desbloquear vistas previas de correo electrónico de Litmus en [esta sección](#email-rendering).

>[!CAUTION]
>
>Al obtener una vista previa de un mensaje o enviar pruebas, solo se muestran los datos de personalización del perfil. La personalización basada en datos de contexto, como la información de evento, solo se puede probar en el contexto de un recorrido. Obtenga información sobre cómo probar la personalización en [este caso de uso](../personalization/personalization-use-case.md).

➡️ [Obtenga información sobre cómo previsualizar y probar el correo electrónico en este vídeo](#video-preview)

## Seleccionar perfiles de prueba {#select-test-profiles}

Uso [Perfiles de prueba](../audience/creating-test-profiles.md) para dirigirse a destinatarios adicionales que no coincidan con los criterios de objetivo definidos.

Para seleccionar perfiles de prueba, siga los pasos a continuación:

1. En el [Editar contenido](create-email.md#define-email-content) o en el Diseñador de correo electrónico, haga clic en **[!UICONTROL Simular contenido]** para acceder a la selección del perfil de prueba.

   ![](assets/email-preview-button.png)

1. Seleccionar **[!UICONTROL Administración de perfiles de prueba]**.

   ![](assets/email-preview_manage-test-profiles.png)

1. Seleccione el área de nombres que se utilizará para identificar los perfiles de prueba haciendo clic en **[!UICONTROL Área de nombres de identidad]** icono de selección.

   ![](assets/previewselect-namespace.png)

   Más información sobre las Áreas de nombres de identidad de Adobe Experience Platform [en esta sección](../audience/get-started-identity.md).

   En el ejemplo siguiente, utilizaremos la variable **Correo electrónico** namespace.

1. Utilice el campo de búsqueda para encontrar el área de nombres, selecciónela y haga clic en **[!UICONTROL Seleccionar]**

   ![](assets/preview-email-namespace.png)

1. En el **[!UICONTROL Valor de identidad]** , introduzca el valor (aquí la dirección de correo electrónico) para identificar el perfil de prueba y haga clic en **[!UICONTROL Añadir perfil]**.

   <!--![](assets/preview-identity-value.png)-->

1. Si ha añadido personalización al mensaje, agregue otros perfiles para poder probar distintas variantes del mensaje según los datos del perfil. Una vez añadidos, los perfiles se enumeran en los campos seleccionados.

   ![](assets/preview-profile-list.png)

   En función de los elementos de personalización de mensajes, esta lista muestra los datos de cada perfil de prueba en las columnas relacionadas.

### Previsualización de correo electrónico {#preview-email}

Una [perfiles de prueba](#select-test-profiles) están seleccionados, puede previsualizar el contenido del correo electrónico. Complete los siguientes pasos:

1. En el [Editar contenido](create-email.md#define-email-content) o en el Diseñador de correo electrónico, haga clic en **[!UICONTROL Simular contenido]** botón.

1. Seleccione un perfil de prueba. Puede comprobar los valores disponibles en las columnas. Utilice las flechas derecha e izquierda para examinar los datos.

   ![](assets/preview-select-profile.png)

   >[!NOTE]
   >
   >Para añadir más perfiles de prueba, seleccione **[!UICONTROL Administración de perfiles de prueba]**. [Más información](#select-test-profiles)

1. Haga clic en **[!UICONTROL Seleccionar datos]** sobre la lista para añadir o quitar columnas.

   ![](assets/preview-select-data.png)

   Al final de la lista se pueden ver campos de personalización específicos del mensaje actual. En este ejemplo, el perfil de ciudad, nombre y apellidos. Seleccione esos campos y asegúrese de que estos valores se rellenen en los perfiles de prueba.

1. En la vista previa del mensaje, los elementos personalizados se sustituyen por los datos del perfil de prueba seleccionado.

   Por ejemplo, para este mensaje, tanto el contenido del correo electrónico como el asunto del correo electrónico están personalizados:

   ![](assets/preview-test-profile.png)

1. Seleccione otros perfiles de prueba para previsualizar el procesamiento de correo electrónico para cada variante del mensaje.

## Envío de pruebas {#send-proofs}

Una prueba es un mensaje específico que le permite probar un mensaje antes de enviarlo a la audiencia principal. Los destinatarios de la prueba se encargan de aprobar el mensaje: procesamiento, contenido, configuración y configuración.

Una [perfiles de prueba](#select-test-profiles) están seleccionados, puede enviar pruebas.

1. En el **[!UICONTROL Simular]** , haga clic en **[!UICONTROL Enviar prueba]** botón.

   ![](assets/send-proof-button.png)

1. Desde el **[!UICONTROL Enviar prueba]** , escriba el correo electrónico del destinatario y haga clic en **[!UICONTROL Añadir]** para enviarse la prueba a sí mismo o a los miembros de sus organizaciones.

   Tenga en cuenta que puede añadir hasta diez destinatarios para la entrega de prueba.

   ![](assets/send-proof-add.png)

1. A continuación, seleccione la **Perfiles de prueba** que se utiliza para personalizar el contenido del mensaje.

   Cada destinatario de la prueba recibirá tantos mensajes como el número de perfiles de prueba seleccionados. Por ejemplo, si ha añadido cinco correos electrónicos de destinatario y ha seleccionado diez perfiles de prueba, enviará cincuenta mensajes de prueba y cada destinatario recibirá diez de ellos.

1. Si es necesario, puede añadir un prefijo a la línea de asunto de la prueba. Solo caracteres alfanuméricos y caracteres especiales como . - _ ( ) [ ] se permiten como prefijo en la línea de asunto.

1. Clic **[!UICONTROL Enviar prueba]**.

   ![](assets/send-proof-select.png)

1. De nuevo en  **[!UICONTROL Simular]** , haga clic en  **[!UICONTROL Ver pruebas]** para comprobar el estado.

   ![](assets/send-proof-view.png)

Se recomienda enviar pruebas después de cada modificación al contenido del mensaje.

>[!NOTE]
>
>En la prueba enviada, el vínculo a la página espejo no está activo. Solo se activa en los mensajes finales.

## Usar procesamiento de correo electrónico {#email-rendering}

Puede aprovechar sus **Litmus** cuenta en [!DNL Journey Optimizer] para previsualizar instantáneamente su **procesamiento de correo electrónico** en clientes de correo electrónico populares.

Para acceder a las funciones de procesamiento de correo electrónico, debe:

* Tener una cuenta de Litmus
* [Seleccionar perfiles de prueba](#select-test-profiles)

A continuación, siga los pasos a continuación:

1. En el [Editar contenido](create-email.md#define-email-content) o en el Diseñador de correo electrónico, haga clic en **[!UICONTROL Simular contenido]** botón.

1. Seleccione el **[!UICONTROL Procesar correo electrónico]** botón.

   ![](assets/email-rendering-button.png)

1. Clic **Conecte su cuenta de Litmus** en la sección superior derecha.

   ![](assets/email-rendering-litmus.png)

1. Introduzca sus credenciales de e inicie sesión.

   ![](assets/email-rendering-credentials.png)

1. Haga clic en **Ejecutar prueba** para generar previsualizaciones de correo electrónico.

1. Compruebe el contenido de su correo electrónico en clientes populares de escritorio, móviles y web.

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>Al conectar su **Litmus** cuenta con [!DNL Journey Optimizer]Por lo tanto, acepta que los mensajes de prueba se envíen a Litmus: una vez enviados, estos correos electrónicos ya no se administran mediante el Adobe. Como consecuencia, la política de correo electrónico de retención de datos de Litmus se aplica a estos correos electrónicos, incluidos los datos de personalización que pueden incluirse en estos mensajes de prueba.

## Vídeo explicativo {#video-preview}

Obtenga información sobre cómo probar el procesamiento de correos electrónicos en varias bandejas de entrada, previsualizar los correos electrónicos personalizados con perfiles de prueba y enviar pruebas.

>[!VIDEO](https://video.tv.adobe.com/v/334239?quality=12)
