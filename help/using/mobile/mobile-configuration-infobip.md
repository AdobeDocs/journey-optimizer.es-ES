---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor de Infobip
description: Aprenda a configurar su entorno para enviar mensajes de texto y MMS con Journey Optimizer con Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
TQID: https://experienceleague.adobe.com/hkloRlDuOO-lNSezWvOcD3dtsHrhDqCJGo3cHq5pWog
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7b5244e8bdbbe7458f283ac883cfaf1d695b332e
workflow-type: tm+mt
source-wordcount: 769
ht-degree: 1%

---

# Configuración del proveedor de Infobip {#sms-configuration-infobip}

Al integrar Infobip con Adobe Journey Optimizer, puede enviar mensajes de texto a sus perfiles como parte de sus recorridos y campañas.

Para configurar Infobip como su proveedor de SMS, siga los pasos a continuación:

1. [Crear credencial de API](#api-credential)
1. [Crear webhook](mobile-webhook.md)
1. [Crear configuración de canal](mobile-configuration-surface.md)
1. [Creación de un Recorrido o una campaña con una acción de canal SMS](create-mobile-message.md)

## Configuración de credenciales de API para SMS {#api-credential}

Para configurar Infobip con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   +++ Lista de credenciales de SMS para la configuración

   | Campos de configuración | Descripción |
   |---|---|
   | Proveedor de SMS | Infobip |
   | Nombre | Elija un nombre para su credencial de API. |
   | URL base de API y clave de API | Acceda a la página de inicio de la interfaz web o a la página de administración de claves de API para encontrar sus credenciales. Para extremos de dominio regionales o alternativos, como `api-ny2.infobip.com`, especifique la dirección URL base completa y compruebe el token de autorización con la compatibilidad con Infobip. </br>Obtenga más información en [Documentación de Infobip](https://www.infobip.com/docs/api){target="_blank"} |
   | ID de entidad principal | Introduzca el ID de entidad principal de DLT asignado. |
   | ID de plantilla de contenido | Introduzca su ID de plantilla de contenido DLT registrado. |
   | Período de validez | Introduzca el periodo de validez del mensaje en horas. En caso de que los mensajes no se puedan enviar dentro de este periodo de tiempo, el sistema intentará reenviarlos de nuevo. El periodo de validez predeterminado es de 48 horas. |
   | Datos de llamada de retorno | Introduzca los datos de cliente adicionales que se enviarán en la dirección URL de notificación. |
   | Número entrante | Añada su número de entrada único. Esto le permite utilizar las mismas credenciales de API en diferentes zonas protegidas, cada una con su propio número de entrada. |

   +++

1. Habilite la opción **[!UICONTROL exclusión aproximada]** para detectar mensajes que se parezcan a palabras clave de exclusión (por ejemplo, &quot;CANCIL&quot;) y personalizar la respuesta de confirmación en el campo **[!UICONTROL Respuesta automática aproximada]**.

   **[!UICONTROL Exclusión parcial]** identifica los mensajes SMS que indican que un usuario desea cancelar la suscripción, aunque el mensaje no coincida exactamente con una palabra clave de exclusión definida. Puede detectar frases de exclusión comunes y ciertos términos ofensivos, lo que ayuda a garantizar que las campañas respeten las preferencias del usuario y sigan cumpliendo las normas.

1. Seleccione **[!UICONTROL Usar conjunto de datos personalizado para entrante]** para enrutar el SMS entrante de esta credencial a un conjunto de datos creado previamente que elija en el menú desplegable. [Más información acerca del uso de un conjunto de datos personalizado para palabras clave entrantes](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >El esquema del conjunto de datos debe ser **[!UICONTROL XDM ExperienceEvent]** e incluir al menos estos grupos de campos:
   >* Adobe CJM ExperienceEvent: Detalles de interacción del mensaje
   >* Adobe CJM ExperienceEvent: Detalles de ejecución de mensajes
   >* Adobe CJM ExperienceEvent: Detalles del perfil de mensaje
   >
   >El esquema y el conjunto de datos deben estar habilitados para el perfil.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

1. En el menú **[!UICONTROL Credenciales de API]**, haga clic en el icono bin para eliminar sus credenciales de API.

1. Para modificar las credenciales existentes, busque las credenciales de API que desee y haga clic en la opción **[!UICONTROL Editar]** para realizar los cambios necesarios.

1. Haga clic en **[!UICONTROL Verificar conexión de SMS]**, a partir de las credenciales de la API existente, para probar y comprobar las credenciales de la API de SMS enviando un mensaje de ejemplo a un dispositivo designado.

1. Rellene los campos **Número** y **Mensaje** y haga clic en **[!UICONTROL Verificar conexión]**.

   >[!IMPORTANT]
   >
   >El mensaje debe estar estructurado para alinearse con el formato de carga útil del proveedor.

   ![](assets/verify-connection.png)

Después de crear y configurar las credenciales de la API, debe crear una configuración de canal para los mensajes SMS y MMS. [Más información](mobile-configuration-surface.md)

## Configurar las credenciales de API para RCS

La mensajería RCS se admite en Adobe Journey Optimizer a través de Infobip mediante la característica [Proveedor de SMS personalizado](mobile-configuration-custom.md). Esto permite enviar mensajes interactivos enriquecidos a través de perfiles comerciales verificados, incorporando elementos como carruseles, botones y contenido multimedia.

➡️ [Descubra cómo Infobip admite RCS en la documentación de Infobip](https://www.infobip.com/docs/api/channels/rcs)

Para habilitar la mensajería RCS con Infobip, se deben configurar nuevas credenciales de API mediante un proveedor de SMS personalizado. Las credenciales existentes de Infobip SMS no son compatibles, ya que RCS requiere un formato de carga útil distinto.

Para configurar RCS con Infobip:

1. **Registre su empresa para RCS a través de Infobip**

   Comience por completar el proceso de incorporación y registro de RCS en la plataforma Infobip. Esto implica configurar el perfil del remitente de RCS y asegurarse de que la cuenta esté habilitada para RCS. Obtenga más información en [Documentación de Infobip](https://www.infobip.com/docs/rcs/get-started)

1. **Crear un webhook de SMS**

   [Configurar un webhook de SMS personalizado](mobile-configuration-custom.md#webhook) en Journey Optimizer. Este webhook será responsable de gestionar las confirmaciones de entrega, los mensajes RCS entrantes y las actualizaciones de estado desde la plataforma de Infobip.

1. **Crear credencial de API usando Personalizado como proveedor de SMS**

   [Cree una nueva credencial de API](mobile-configuration-custom.md#api-credential) en Journey Optimizer, seleccionando &quot;Personalizado&quot; como proveedor de SMS. Utilice el método de autenticación de extremo RCS adecuado, la dirección URL base y los encabezados.

Después de crear y configurar tu credencial de API, ahora necesitas crear [tu webhook](mobile-webhook.md) y una configuración de canal para tus mensajes RCS. [Más información](mobile-configuration-surface.md)
