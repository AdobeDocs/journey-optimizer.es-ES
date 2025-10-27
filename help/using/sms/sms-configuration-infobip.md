---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor Infobip
description: Aprenda a configurar su entorno para enviar mensajes de texto y MMS con Journey Optimizer con Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 5b719ccfb38ea51d6f6c6a9204e235c022b01b4f
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 2%

---

# Configuración del proveedor Infobip {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

Si no se proporcionan las palabras clave de inclusión u exclusión, se utilizan mensajes de consentimiento estándar para respetar la privacidad del usuario. Añadir palabras clave personalizadas anula automáticamente los valores predeterminados.

**Palabras clave predeterminadas:**

* **Inclusión**: SUSCRIBIRSE, SÍ, NO DETENER, INICIAR, CONTINUAR, REANUDAR, INICIAR
* **Exclusión**: DETENER, SALIR, CANCELAR, FINALIZAR, CANCELAR SUSCRIPCIÓN, NO
* **Ayuda**: AYUDA

>[!ENDSHADEBOX]

## Configuración de credenciales de API para SMS

Para configurar Infobip con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   +++ Lista de credenciales de SMS para la configuración

   | Campos de configuración | Descripción |
   |---|---|    
   | Proveedor de SMS | Infobip |
   | Nombre | Elija un nombre para su credencial de API. |
   | URL base de API y clave de API | Acceda a la página de inicio de la interfaz web o a la página de administración de claves de API para encontrar sus credenciales. Obtenga más información en [Documentación de Infobip](https://www.infobip.com/docs/api){target="_blank"} |
   | Palabras clave de inclusión | Introduzca las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su mensaje de inclusión. Para varias palabras clave, utilice valores separados por comas. |
   | Mensaje de inclusión | Introduzca la respuesta personalizada que se envía automáticamente como mensaje de inclusión. |
   | Palabras clave de exclusión | Introduzca las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente el mensaje de exclusión. Para varias palabras clave, utilice valores separados por comas. |
   | Mensaje de exclusión | Introduzca la respuesta personalizada que se enviará automáticamente como mensaje de exclusión. |
   | Palabras clave de ayuda | Escriba las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su **mensaje de ayuda**. Para varias palabras clave, utilice valores separados por comas. |
   | Mensaje de ayuda | Escriba la respuesta personalizada que se enviará automáticamente como **mensaje de ayuda**. |
   | Palabras clave de inclusión doble | Introduzca las palabras clave que almacenan en déclencheur el proceso de inclusión doble. Si no existe ningún perfil de usuario, se crea tras una confirmación correcta. Para varias palabras clave, utilice valores separados por comas. [Más información sobre la inclusión doble de SMS](https://video.tv.adobe.com/v/3440278/?captions=spa&learn=on). |
   | Mensaje de inclusión doble | Introduzca la respuesta personalizada que se envía automáticamente en respuesta a la confirmación de doble inclusión. |
   | ID de entidad principal | Introduzca el ID de entidad principal de DLT asignado. |
   | ID de plantilla de contenido | Introduzca su ID de plantilla de contenido DLT registrado. |
   | Período de validez | Introduzca el periodo de validez del mensaje en horas. En caso de que los mensajes no se puedan enviar dentro de este periodo de tiempo, el sistema intentará reenviarlos de nuevo. El periodo de validez predeterminado es de 48 horas. |
   | Datos de llamada de retorno | Introduzca los datos de cliente adicionales que se enviarán en la dirección URL de notificación. |
   | Número entrante | Añada su número de entrada único. Esto le permite utilizar las mismas credenciales de API en diferentes zonas protegidas, cada una con su propio número de entrada. |
   | Palabras clave de entrada personalizadas | Defina palabras clave únicas no relacionadas con el consentimiento para las acciones basadas en lotes, por ejemplo, DESCUENTO, OFERTAS, INSCRIBIRSE. Estas palabras clave se capturan y almacenan como atributos en el perfil, lo que le permite almacenar en déclencheur una calificación de segmentos por lotes dentro del recorrido y enviar una respuesta o acción personalizada. |
   | Mensaje de respuesta entrante predeterminado | Introduzca la respuesta predeterminada que se envía cuando un usuario final envía un SMS entrante que no coincide con ninguna de las palabras clave definidas. |

   +++

1. Habilite la opción **[!UICONTROL exclusión aproximada]** para detectar mensajes que se parezcan a palabras clave de exclusión (por ejemplo, &quot;CANCIL&quot;) y personalizar la respuesta de confirmación en el campo **[!UICONTROL Respuesta automática aproximada]**.

   **[!UICONTROL Exclusión parcial]** identifica los mensajes SMS que indican que un usuario desea cancelar la suscripción, aunque el mensaje no coincida exactamente con una palabra clave de exclusión definida. Puede detectar frases de exclusión comunes y ciertos términos ofensivos, lo que ayuda a garantizar que las campañas respeten las preferencias del usuario y sigan cumpliendo las normas.

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

La mensajería RCS se admite en Adobe Journey Optimizer a través de Infobip mediante la característica [Proveedor de SMS personalizado](sms-configuration-custom.md). Esto permite enviar mensajes interactivos enriquecidos a través de perfiles comerciales verificados, incorporando elementos como carruseles, botones y contenido multimedia.

➡️ [Descubra cómo Infobip admite RCS en la documentación de Infobip](https://www.infobip.com/docs/api/channels/rcs)

Para habilitar la mensajería RCS con Infobip, se deben configurar nuevas credenciales de API mediante un proveedor de SMS personalizado. Las credenciales existentes de Infobip SMS no son compatibles, ya que RCS requiere un formato de carga útil distinto.

Para configurar RCS con Infobip:

1. **Registre su empresa para RCS a través de Infobip**

   Comience por completar el proceso de incorporación y registro de RCS en la plataforma Infobip. Esto implica configurar el perfil del remitente de RCS y asegurarse de que la cuenta esté habilitada para RCS. Obtenga más información en [Documentación de Infobip](https://www.infobip.com/docs/rcs/get-started)

1. **Crear un webhook de SMS**

   [Configurar un webhook de SMS personalizado](sms-configuration-custom.md#webhook) en Journey Optimizer. Este webhook será responsable de gestionar las confirmaciones de entrega, los mensajes RCS entrantes y las actualizaciones de estado desde la plataforma de Infobip.

1. **Crear credencial de API usando Personalizado como proveedor de SMS**

   [Cree una nueva credencial de API](sms-configuration-custom.md#api-credential) en Journey Optimizer, seleccionando &quot;Personalizado&quot; como proveedor de SMS. Utilice el método de autenticación de extremo RCS adecuado, la dirección URL base y los encabezados.

Después de crear y configurar las credenciales de la API, debe crear una configuración de canal para los mensajes RCS. [Más información](sms-configuration-surface.md)
