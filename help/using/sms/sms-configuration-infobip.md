---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor Infobip
description: Aprenda a configurar su entorno para enviar mensajes de texto y MMS con Journey Optimizer con Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 8f045e1b709c0059ce21cda68c21e8732f58e51e
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 5%

---

# Configuración del proveedor Infobip {#sms-configuration-infobip}

Para configurar Infobip con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administration]** `>` **[!UICONTROL Canales]** y seleccione la **[!UICONTROL Credenciales de API]** menú. Haga clic en **[!UICONTROL Crear nuevas credenciales de API]** botón.

1. Configure las credenciales de la API como se detalla a continuación.

   * **[!UICONTROL Proveedor de SMS]**: Infobip.

   * **[!UICONTROL Nombre]**: elija un nombre para la credencial de la API.

   * **[!UICONTROL URL base de API]** y **[!UICONTROL Clave de API]**: acceda a la página de inicio de la interfaz web o a la página de administración de claves de API para encontrar sus credenciales. Obtenga más información en [Documentación de Infobip](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL Palabras clave de inclusión]**: introduzca las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su **[!UICONTROL Mensaje de inclusión]**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de inclusión]**: introduzca la respuesta personalizada que se envía automáticamente como **[!UICONTROL Mensaje de inclusión]**.

   * **[!UICONTROL Palabras clave de exclusión]**: introduzca las palabras clave predeterminadas o que almacenarán en déclencheur automáticamente su **[!UICONTROL Mensaje de exclusión]**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de exclusión]**: introduzca la respuesta personalizada que se envía automáticamente como **[!UICONTROL Mensaje de exclusión]**.

   * **[!UICONTROL Palabras clave de ayuda]**: introduzca las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su **Mensaje de ayuda**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de ayuda]**: introduzca la respuesta personalizada que se envía automáticamente como **Mensaje de ayuda**.

   * **[!UICONTROL Palabras clave de inclusión doble]**: introduzca las palabras clave que almacenan en déclencheur el proceso de inclusión doble. Si no existe ningún perfil de usuario, se crea tras una confirmación correcta. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de inclusión doble]**: introduzca la respuesta personalizada que se envía automáticamente en respuesta a la confirmación de inclusión doble.

   * **[!UICONTROL ID de entidad principal]**: introduzca el ID de entidad principal de DLT asignado.

   * **[!UICONTROL ID de plantilla de contenido]**: introduzca su ID de plantilla de contenido DLT registrado.

   * **[!UICONTROL Período de validez]**: introduzca el periodo de validez del mensaje en horas. En caso de que los mensajes no se puedan enviar dentro de este periodo de tiempo, el sistema intentará reenviarlos de nuevo. El periodo de validez predeterminado es de 48 horas.

   * **[!UICONTROL Datos de llamada de retorno]**: introduzca los datos de cliente adicionales que se enviarán en la dirección URL de notificación.

1. Clic **[!UICONTROL Enviar]** cuando haya terminado de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes SMS y MMS. [Más información](sms-configuration-surface.md)
