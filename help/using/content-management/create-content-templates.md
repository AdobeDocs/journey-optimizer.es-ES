---
solution: Journey Optimizer
product: journey optimizer
title: Creación de plantillas de contenido
description: Aprenda a crear plantillas para reutilizar contenido en campañas y recorridos de Journey Optimizer
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: a205539b-b7ea-4832-92b0-49637c4dac47
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 16%

---

# Creación de plantillas de contenido {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Definir su propia plantilla de contenido"
>abstract="Cree una plantilla personalizada independiente desde cero para que el contenido se pueda reutilizar en varios recorridos y campañas."

Existen dos formas de crear plantillas de contenido:

* Cree una plantilla de contenido desde cero mediante el carril izquierdo del menú **[!UICONTROL Plantillas de contenido]**. [Descubra cómo](#create-template-from-scratch)

* Al diseñar el contenido dentro de una campaña o un recorrido, guárdelo como una plantilla. [Descubra cómo](#save-as-template)

Una vez guardada, la plantilla de contenido está disponible para usarla en una campaña o un recorrido. Ya sea que se haya creado desde cero o a partir de contenido anterior, ahora puede utilizar esta plantilla al crear cualquier contenido dentro de [!DNL Journey Optimizer]. [Descubra cómo](#use-content-templates)

>[!NOTE]
>
>* Los cambios realizados en las plantillas de contenido no se propagan a las campañas ni a los recorridos, ya estén activos o en borrador.
>
>* Del mismo modo, cuando las plantillas se utilizan en una campaña o un recorrido, las ediciones que realice en el contenido de la campaña y del recorrido no afectan a la plantilla de contenido utilizada anteriormente.

## Crear una plantilla desde cero {#create-template-from-scratch}

>[!NOTE]
>
>A partir de marzo de 2025, las plantillas de contenido de tipo HTML quedarán obsoletas. Puede seguir utilizando las plantillas de contenido de HTML existentes creadas anteriormente en [!DNL Journey Optimizer].

Para crear una plantilla de contenido desde cero, siga los pasos a continuación.

1. Acceda a la lista de plantillas de contenido a través del menú de la izquierda **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas de contenido]**.

1. Seleccione **[!UICONTROL Crear plantilla]**.

1. Complete los detalles de la plantilla y seleccione el canal deseado.

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >Actualmente, todos los canales están disponibles excepto la web.

1. Seleccione o cree etiquetas Adobe Experience Platform en el campo **[!UICONTROL Etiquetas]** para categorizar la plantilla y mejorar la búsqueda. [Más información](../start/search-filter-categorize.md#tags)

1. Para asignar etiquetas de uso de datos principales o personalizadas a la plantilla, puedes seleccionar **[!UICONTROL Administrar acceso]**. [Obtenga más información acerca del Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Haga clic en **[!UICONTROL Crear]** y diseñe el contenido según sea necesario, del mismo modo que lo haría para cualquier contenido dentro de un recorrido o una campaña, según el canal que haya seleccionado.

   ![](assets/content-template-edition.png)

   Aprenda a crear contenido para los diferentes canales en las siguientes secciones:
   * [Definición del contenido del correo electrónico](../email/get-started-email-design.md)
   * [Definición del contenido push](../push/design-push.md)
   * [Definición del contenido SMS](../sms/create-sms.md#sms-content)
   * [Definición del contenido de correo directo](../direct-mail/create-direct-mail.md)
   * [Definición del contenido en la aplicación](../in-app/design-in-app.md)
   * [Definir contenido web](../web/create-web.md#edit-web-content)
   * [Definición del contenido de experiencia basado en código](../code-based/create-code-based.md)

     >[!NOTE]
     >
     >Puede agregar políticas de decisión a las plantillas de contenido de experiencia basadas en código. [Más información](../experience-decisioning/create-decision.md#add-decision)

1. Puede probar el contenido. [Descubra cómo](#test-template)

1. Una vez que la plantilla esté lista, haz clic en **[!UICONTROL Guardar]**.

1. Haga clic en la flecha situada junto al nombre de la plantilla para volver a la pantalla **[!UICONTROL Detalles]**.

   ![](assets/content-template-back.png)

Esta plantilla ya está lista para usarse al generar contenido dentro de [!DNL Journey Optimizer]. [Descubra cómo](#use-content-templates)

>[!NOTE]
>
>Al crear una plantilla de contenido de correo electrónico, para aplicar rápidamente un estilo específico que se ajuste a su marca y diseño, puede aplicar un tema al contenido. [Más información](../email/apply-email-themes.md)

## Guardar contenido como plantilla de contenido {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Aprenda a migrar sus mensajes"
>abstract="El 25 de julio de 2022, desapareció el menú Mensajes y ahora los mensajes se crean directamente desde un recorrido. Si desea reutilizar los mensajes heredados en recorridos, debe guardarlos como plantillas."

Al diseñar cualquier contenido en una campaña o un recorrido, puede guardarlo para su reutilización futura. Para realizar esto, siga los pasos a continuación.

1. En la pantalla del mensaje **[!UICONTROL Editar contenido]**, haga clic en el botón **[!UICONTROL Plantilla de contenido]**.

1. Seleccione **[!UICONTROL Guardar como plantilla de contenido]** en el menú desplegable.

   ![](assets/content-template-button-save.png)

   Si estás en [Email Designer](../email/get-started-email-design.md), también puedes seleccionar esta opción en la lista desplegable de **[!UICONTROL Más]** en la parte superior derecha de la pantalla.

   ![](assets/content-template-more-button-save.png)

1. Añada un nombre y una descripción para esta plantilla.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >El canal actual se rellena automáticamente y no se puede editar.

1. Seleccione o cree una etiqueta Adobe Experience Platform en el campo **Etiquetas** para categorizar la plantilla. [Más información](../start/search-filter-categorize.md#tags)

1. Para asignar etiquetas de uso de datos principales o personalizadas a la plantilla, puedes seleccionar **[!UICONTROL Administrar acceso]**. [Más información](../administration/object-based-access.md).

1. Haga clic en **[!UICONTROL Guardar]**.

1. La plantilla se guardará en la lista **[!UICONTROL Plantillas de contenido]**, a la que se puede acceder desde el menú dedicado [!DNL Journey Optimizer]. Se convierte en una plantilla de contenido independiente a la que se puede acceder, editar y eliminar como cualquier otro elemento de la lista. [Más información](#access-manage-templates)

Ahora puede usar esta plantilla al generar cualquier contenido dentro de [!DNL Journey Optimizer]. [Descubra cómo](#use-content-templates)

>[!NOTE]
>
>Los cambios que se realicen en esa nueva plantilla no se propagarán al contenido del que procedan. Del mismo modo, cuando el contenido original se edita dentro de ese contenido, la nueva plantilla no se modifica.
