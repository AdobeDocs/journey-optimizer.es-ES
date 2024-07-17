---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor Infobip
description: Aprenda a configurar su entorno para enviar mensajes de texto y MMS con Journey Optimizer con Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 794ac45177e467be4bd5b8f7288e07c85e4d806a
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 5%

---

# Configuración del proveedor Infobip {#sms-configuration-infobip}

Para configurar Infobip con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API como se detalla a continuación.

   * **[!UICONTROL Proveedor de SMS]**: Infobip.

   * **[!UICONTROL Nombre]**: elige un nombre para tu credencial de API.

   * **[!UICONTROL URL base de API]** y **[!UICONTROL clave de API]**: accede a la página de inicio de la interfaz web o a la página de administración de claves de API para encontrar tus credenciales. Obtenga más información en [Documentación de Infobip](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL Palabras clave de inclusión]**: escriba las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su **[!UICONTROL mensaje de inclusión]**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de inclusión]**: escriba la respuesta personalizada que se enviará automáticamente como **[!UICONTROL Mensaje de inclusión]**.

   * **[!UICONTROL Palabras clave de exclusión]**: escriba las palabras clave predeterminadas o las palabras clave que almacenarán en déclencheur automáticamente su **[!UICONTROL mensaje de exclusión]**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de exclusión]**: escriba la respuesta personalizada que se enviará automáticamente como **[!UICONTROL Mensaje de exclusión]**.

   * **[!UICONTROL Palabras clave de ayuda]**: escribe las palabras clave predeterminadas o personalizadas que almacenarán automáticamente en déclencheur tu **mensaje de ayuda**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de ayuda]**: escriba la respuesta personalizada que se enviará automáticamente como **Mensaje de ayuda**.

   * **[!UICONTROL Palabras clave de inclusión doble]**: escriba las palabras clave que almacenan en déclencheur el proceso de inclusión doble. Si no existe ningún perfil de usuario, se crea tras una confirmación correcta. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de inclusión doble]**: escriba la respuesta personalizada que se enviará automáticamente en respuesta a la confirmación de inclusión doble.

   * **[!UICONTROL ID de entidad principal]**: escriba el ID de entidad principal DLT asignado.

   * **[!UICONTROL ID de plantilla de contenido]**: escriba su ID de plantilla de contenido DLT registrado.

   * **[!UICONTROL Período de validez]**: introduzca el período de validez del mensaje en horas. En caso de que los mensajes no se puedan enviar dentro de este periodo de tiempo, el sistema intentará reenviarlos de nuevo. El periodo de validez predeterminado es de 48 horas.

   * **[!UICONTROL Datos de devolución de llamada]**: escriba los datos de cliente adicionales que se enviarán en la dirección URL de notificación.

   * **[!UICONTROL Número de entrada]**: agrega tu número de entrada único. Esto le permite utilizar las mismas credenciales de API en diferentes zonas protegidas, cada una con su propio número de entrada.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes SMS y MMS. [Más información](sms-configuration-surface.md)
