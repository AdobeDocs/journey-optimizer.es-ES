---
title: Crear un mensaje
description: Aprenda a crear un mensaje
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 2%

---

# Crear un mensaje {#create-message}

![](assets/do-not-localize/badge.png)

Los mensajes están disponibles en el acceso directo **[!UICONTROL Messages]** del carril izquierdo. Todos los mensajes se enumeran, ordenados por fecha de publicación (para mensajes publicados) o fecha de creación (para borradores de mensajes).

>[!NOTE]
>
>Todos los usuarios pueden acceder, crear, editar y publicar mensajes. Obtenga más información sobre los permisos de usuario [en esta sección](permissions.md).

![](assets/messages-list.png)

Utilice la opción **[!UICONTROL Show recents]** para añadir vínculos directos a los mensajes a los que ha accedido en los últimos 5 días.

![](assets/show-recent-messages.png)

Utilice el icono de filtro para mostrar solo los mensajes redactados, publicados o que se están publicando. También puede buscar en una etiqueta de mensaje, como se muestra a continuación:

![](assets/filter-messages.png)

## Crear un nuevo mensaje

Para crear un nuevo mensaje, siga los pasos a continuación:

1. Acceda a la lista de mensajes y haga clic en **[!UICONTROL Create Message]**.

1. Defina las propiedades del mensaje.

   ![](assets/create-message-properties.png)

   * Introduzca un **[!UICONTROL Title]** (obligatorio) y un **[!UICONTROL Description]**.

   * Seleccione el **[!UICONTROL Preset]** que se utilizará para el mensaje.

      Los ajustes preestablecidos incluyen todos los parámetros necesarios para enviar un correo electrónico o una notificación push según la marca. [Obtenga más información sobre la promoción de la marca](administration.md#cjm-branding).

   * Seleccione los canales que desee utilizar para ese mensaje: Notificación por correo electrónico o push . Debe seleccionar al menos un canal para poder crear el mensaje.
   Tenga en cuenta que puede acceder y modificar el título, la descripción y el ajuste preestablecido del mensaje en cualquier momento mediante el botón **[!UICONTROL Properties]** de la interfaz de mensajes.

   ![](assets/message-properties.png)


1. Haga clic en **[!UICONTROL Create]** para confirmar la creación del mensaje. El mensaje se añade en la lista de mensajes, en el estado **[!UICONTROL Draft]** .

   Hay una pestaña disponible para cada canal seleccionado. Utilice estas pestañas para configurar el contenido de cada canal. Puede quitar una pestaña seleccionándola y haciendo clic en el botón **[!UICONTROL Delete channel]** de la derecha.

   ![](assets/create-messages-content.png)

   Ahora puede crear el contenido del mensaje y adaptar la configuración. Encontrará información detallada sobre la configuración del correo electrónico y las notificaciones push en las secciones siguientes:

   * [Configuración de correos electrónicos](configure-email.md)
   * [Configuración de notificaciones push](configure-push.md)

   >[!NOTE]
   >   
   >Puede personalizar los mensajes mediante los datos de los perfiles mediante el Editor de expresiones. Para obtener más información sobre personalización, consulte [esta sección](personalization/personalize.md).


1. Controle la renderización de los mensajes y compruebe la configuración de personalización con perfiles de prueba mediante la sección de previsualización de la izquierda. Para obtener más información, consulte [esta sección](preview.md).

   ![](assets/messages-simple-preview.png)

1. Compruebe las alertas en la sección superior del editor.  Algunas son simples advertencias, pero otras pueden impedir que publique el mensaje. Obtenga más información en [esta sección](alerts.md).

1. Ahora puede publicar el mensaje haciendo clic en el botón **[!UICONTROL Publish]** o mantenerlo como borrador y publicarlo más adelante. Para obtener más información sobre cómo publicar mensajes, consulte [esta sección](publish-manage-message.md).

## Duplicar un mensaje

Para crear un mensaje a partir de uno existente, utilice el botón **[!UICONTROL Duplicate]** de la interfaz de mensajes. Todos los ajustes y configuraciones se copiarán en el nuevo mensaje

![](assets/message-duplicate.png)

Puede cambiar el nombre del mensaje antes de confirmar la duplicación.

![](assets/message-duplicate-confirm.png)

Una vez creado el nuevo mensaje, aparece un mensaje de confirmación en la parte inferior de la ventana.

También puede duplicar un mensaje de la lista de mensajes mediante el icono dedicado.

![](assets/message-duplicate-from-list.png)

Se aplica el mismo proceso de confirmación.
