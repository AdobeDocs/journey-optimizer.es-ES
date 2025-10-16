---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor Twilio
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer con Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 2%

---

# Configuración del proveedor Twilio {#sms-configuration-twilio}

## Configuración de las credenciales de API para SMS/MMS

Para configurar Twilio con Journey Optimizer, debe crear nuevas credenciales de API para Twilio:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** `>` **[!UICONTROL Configuración de SMS]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   * **[!UICONTROL Proveedor de SMS]**: Twilio.

   * **[!UICONTROL Nombre]**: elige un nombre para tu credencial de API.

   * **[!UICONTROL SID de cuenta]** y **[!UICONTROL token de autenticación]**: acceda al panel **Información de cuenta** de la página del panel de la consola de Twilio para encontrar sus credenciales.

   * **[!UICONTROL SID de mensaje]**: escriba el identificador único asignado a cada mensaje creado por la API de Twilio. Obtenga más información en [Documentación de Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Número de entrada]**: agrega tu número de entrada único. Esto le permite utilizar las mismas credenciales de API en diferentes zonas protegidas, cada una con su propio número de entrada.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

1. En el menú **[!UICONTROL Credenciales de API]**, haga clic en el icono bin para eliminar sus credenciales de API.

1. Para modificar las credenciales existentes, busque las credenciales de API que desee y haga clic en la opción **[!UICONTROL Editar]** para realizar los cambios necesarios.

1. Haga clic en **[!UICONTROL Verificar conexión de SMS]**, a partir de las credenciales de la API existente, para probar y comprobar las credenciales de la API de SMS enviando un mensaje de ejemplo a un dispositivo designado.

1. Rellene los campos **Número** y **Mensaje** y haga clic en **[!UICONTROL Verificar conexión]**.

   >[!IMPORTANT]
   >
   >El mensaje debe estar estructurado para alinearse con el formato de carga útil del proveedor.

   ![](assets/verify-connection.png)

Después de crear y configurar las credenciales de la API, debe crear una configuración de canal para los mensajes SMS y MMS. [Más información](sms-configuration-surface.md)

## Configurar las credenciales de API para RCS

La mensajería RCS se admite en Adobe Journey Optimizer a través de Twilio con la función [Proveedor de SMS personalizado](sms-configuration-custom.md). Esto permite enviar mensajes interactivos enriquecidos a través de perfiles comerciales verificados, incorporando elementos como carruseles, botones y contenido multimedia.

➡️ [Explore cómo Twilio admite RCS en la documentación de Twilio](https://www.twilio.com/docs/rcs)

Para habilitar la mensajería RCS con Twilio, las nuevas credenciales de la API deben configurarse mediante un proveedor de SMS personalizado. Las credenciales existentes de Twilio SMS no son compatibles, ya que RCS requiere un formato de carga útil distinto.

Para configurar RCS con Twilio:

1. **Regístrese para recibir mensajes RCS en Twilio**

   Comience por completar el proceso de registro RCS en la plataforma Twilio. Esto incluye configurar el perfil empresarial y habilitar las funcionalidades de RCS para la cuenta.

1. **Crear un webhook de SMS**

   [Configurar un webhook de SMS](sms-configuration-custom.md#webhook) que pueda recibir respuestas de mensajes RCS entrantes o actualizaciones de entrega. Este webhook debe estar correctamente vinculado a tu configuración de Twilio para la comunicación bidireccional.

1. **Crear credencial de API usando Personalizado como proveedor de SMS**

   En Journey Optimizer, [defina nuevas credenciales de API](sms-configuration-custom.md#api-credential) específicamente para RCS usando &quot;Personalizado&quot; como proveedor de SMS. Utilice el método de autenticación de extremo RCS adecuado, la dirección URL base y los encabezados.

Después de crear y configurar las credenciales de la API, debe crear una configuración de canal para los mensajes RCS. [Más información](sms-configuration-surface.md)







