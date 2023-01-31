---
solution: Journey Optimizer
product: journey optimizer
title: Creación de plantillas de contenido
description: Aprenda a crear plantillas para reutilizar contenido en campañas y recorridos de Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 1%

---

# Creación de plantillas de contenido {#content-templates}

>[!CONTEXTUALHELP]
>id="ajo_content_templates"
>title="Creación de plantillas de contenido"
>abstract="Cree plantillas independientes para reutilizar el contenido en todos los recorridos y campañas."

Para un proceso de diseño acelerado y mejorado, puede crear plantillas independientes para reutilizar fácilmente el contenido personalizado en [!DNL Journey Optimizer] campañas y recorridos.

Esta funcionalidad permite a los usuarios orientados al contenido trabajar con plantillas fuera de campañas o recorridos. Los usuarios de marketing pueden reutilizar y adaptar estas plantillas de contenido independientes dentro de sus propios recorridos o campañas.

>[!CAUTION]
>
>Para crear, editar y eliminar plantillas de contenido, debe tener la variable **[!DNL Manage Library Items]** permiso incluido en la variable **[!DNL Content Library Manager]** perfil de producto. [Más información](../administration/ootb-product-profiles.md#content-library-manager)

Por ejemplo, un usuario de su empresa está a cargo solo del contenido y, por lo tanto, no tiene acceso a campañas o recorridos. Sin embargo, este usuario puede crear una plantilla de correo electrónico que los especialistas en marketing de la organización podrán seleccionar para su uso en todos los correos electrónicos como punto de partida.

>[!NOTE]
>
>* Los cambios realizados en las plantillas de contenido no se propagan a campañas ni recorridos, ya sean en directo o en borrador.
>
>* Del mismo modo, cuando las plantillas se utilizan en una campaña o un recorrido, las ediciones que realice en el contenido de la campaña y del recorrido no afectarán a la plantilla de contenido utilizada anteriormente.


➡️ [Aprenda a crear y utilizar plantillas en este vídeo](#video-templates)

Para crear una plantilla de contenido, siga los pasos a continuación.

1. Para acceder a la lista de plantillas de contenido, seleccione **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Plantillas de contenido]** en el menú de la izquierda.

   ![](assets/content-template-list.png)

1. Todas las plantillas creadas en el entorno limitado actual, ya sea desde un recorrido, una campaña o desde el **[!UICONTROL Plantillas de contenido]** menú , se muestran.

   >[!NOTE]
   >
   >Puede ordenar las plantillas de contenido por fecha de creación o modificación.

1. Select **[!UICONTROL Crear plantilla]**.

1. Rellene los detalles de la plantilla.

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >Actualmente solo el **Correo electrónico** canal y **HTML** son compatibles.

1. Para asignar etiquetas de uso de datos principales o personalizadas a la plantilla, seleccione **[!UICONTROL Administrar acceso]**. [Más información sobre Control de acceso a nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Haga clic en **[!UICONTROL Crear]** y elija cómo desea diseñar su correo electrónico desde las siguientes opciones:

   * **[!UICONTROL Diseño desde cero]**
   * **[!UICONTROL Codifique sus propios]**
   * **[!UICONTROL Importar HTML]**
   * **[!UICONTROL Seleccionar plantilla de diseño]**

   ![](assets/content-template-design.png)

   >[!NOTE]
   >
   >Si selecciona una plantilla, puede elegir entre **[!UICONTROL Plantillas de ejemplo]**, que son plantillas de correo electrónico predeterminadas, y **[!UICONTROL Plantillas guardadas]**, que son los que se crearon a partir de un recorrido, una campaña o desde el **[!UICONTROL Plantillas de contenido]** para abrir el Navegador. [Más información](email-templates.md#save-as-template)

1. Se muestra el Diseñador de correo electrónico. Edite el contenido según sea necesario, del mismo modo que lo haría con cualquier correo electrónico dentro de un recorrido o una campaña, según la opción seleccionada:

   * [Diseñe su correo electrónico desde cero](content-from-scratch.md) a través de la interfaz del diseñador y aproveche las imágenes de [Adobe Experience Manager Assets Essentials](assets-essentials.md).

   * [Código o copiar y pegar HTML sin procesar](code-content.md) directamente en el Diseñador de correo electrónico.

   * [Importar contenido de HTML existente](existing-content.md) desde un archivo o una carpeta .zip.

   * [Usar contenido existente](email-templates.md) de una lista de plantillas integradas o personalizadas.

   ![](assets/content-template-designer.png)

1. Haga clic en **[!UICONTROL Simular contenido]** para comprobar la renderización del correo electrónico. Puede elegir la vista de escritorio o la vista móvil. [Más información](preview.md)

   >[!CAUTION]
   >
   >Para simular contenido, debe tener la variable **[!DNL Manage Simulate Content]** permiso incluido en la variable **[!DNL Content Library Manager]** perfil de producto. [Más información](../administration/ootb-product-profiles.md#content-library-manager)

   ![](assets/content-template-stimulate.png)

1. Puede enviar una prueba para probar el contenido y conseguir que lo aprueben algunos usuarios internos antes de utilizarlo en un recorrido o una campaña.

   * Para ello, haga clic en el botón **[!UICONTROL Enviar prueba]** y siga los pasos descritos en [esta sección](preview.md#send-proofs).

   * Antes de enviar la prueba, debe seleccionar la opción [superficie del correo electrónico](../configuration/channel-surfaces.md) que se utilizará para probar el contenido.

      ![](assets/content-template-stimulate-proof-surface.png)

1. Una vez que la plantilla esté lista, haga clic en **[!UICONTROL Guardar]**.

1. Si es necesario, haga clic en la flecha situada junto al nombre de la plantilla para volver al **[!UICONTROL Detalles]** y edite la plantilla.

   ![](assets/content-template-designer-back.png)

1. Ahora puede usar esta plantilla de contenido al crear cualquier [email](get-started-email-design.md) en [!DNL Journey Optimizer]. Más información sobre [uso de una plantilla guardada](email-templates.md#use-saved-template).

   ![](assets/email_designer-saved-templates.png)

## Vídeo explicativo{#video-templates}

Obtenga información sobre cómo crear, editar y utilizar plantillas de contenido en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)