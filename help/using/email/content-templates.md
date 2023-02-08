---
solution: Journey Optimizer
product: journey optimizer
title: Creación de plantillas de contenido
description: Aprenda a crear plantillas para reutilizar contenido en campañas y recorridos de Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 08d842a877ed52349eef5a901aaf9c75187c69d3
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 2%

---

# Trabajar con plantillas de contenido {#content-templates}

Para un proceso de diseño acelerado y mejorado, puede crear plantillas independientes para reutilizar fácilmente el contenido personalizado en [!DNL Journey Optimizer] campañas y recorridos.

Esta funcionalidad permite a los usuarios orientados al contenido trabajar con plantillas fuera de campañas o recorridos. Los usuarios de marketing pueden reutilizar y adaptar estas plantillas de contenido independientes dentro de sus propios recorridos o campañas.

Por ejemplo, un usuario de su empresa está a cargo solo del contenido y, por lo tanto, no tiene acceso a campañas o recorridos. Sin embargo, este usuario puede crear una plantilla de correo electrónico que los especialistas en marketing de la organización podrán seleccionar para su uso en todos los correos electrónicos como punto de partida.

➡️ [Aprenda a crear y utilizar plantillas en este vídeo](#video-templates)

>[!CAUTION]
>
>Para crear, editar y eliminar plantillas de contenido, debe tener la variable **[!DNL Manage Library Items]** permiso incluido en la variable **[!DNL Content Library Manager]** perfil de producto. [Más información](../administration/ootb-product-profiles.md#content-library-manager)

## Acceso y administración de plantillas {#access-manage-templates}

Para acceder a la lista de plantillas de contenido, seleccione **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Plantillas de contenido]** en el menú de la izquierda.

![](assets/content-template-list.png)

Todas las plantillas creadas en el entorno limitado actual, ya sea desde un recorrido o desde una campaña utilizando la variable [Guardar como plantilla](#save-as-template) , ya sea desde la **[!UICONTROL Plantillas de contenido]** menú , se muestran.

Puede ordenar las plantillas de contenido por fecha de creación o modificación. También puede elegir mostrar solo los elementos que ha creado o modificado.

![](assets/content-template-list-filters.png)

Para editar el contenido de una plantilla, haga clic en el elemento deseado de la lista y seleccione **[!UICONTROL Editar contenido]**.

![](assets/content-template-list-edit.png)

Para eliminar una plantilla, seleccione el icono de papelera situado junto a la plantilla deseada.

![](assets/content-template-list-delete.png)

>[!NOTE]
>
>Cuando se edita o elimina una plantilla, las campañas o recorridos, incluidos los correos electrónicos creados con esta plantilla, no se ven afectados.

## Creación de plantillas de contenido {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Defina su propia plantilla de contenido"
>abstract="Cree una plantilla personalizada independiente desde cero para que el contenido se pueda reutilizar en varios recorridos y campañas."

Existen dos formas de crear plantillas de contenido:

* Cree una plantilla de contenido desde cero, utilizando el carril izquierdo **[!UICONTROL Plantillas de contenido]** para abrir el Navegador. [Descubra cómo](#create-template-from-scratch)

* Al diseñar un correo electrónico dentro de una campaña o un recorrido, guarde el contenido del correo electrónico como una plantilla. [Descubra cómo](#save-as-template)

Una vez guardada, la plantilla de contenido estará disponible para su uso en una campaña o un recorrido. Tanto si se crea desde cero como a partir de un correo electrónico anterior, ahora puede utilizar esta plantilla al crear cualquier [email](get-started-email-design.md) en [!DNL Journey Optimizer]. [Descubra cómo](email-templates.md)

>[!NOTE]
>
>* Los cambios realizados en las plantillas de contenido no se propagan a campañas ni recorridos, ya sean en directo o en borrador.
>
>* Del mismo modo, cuando las plantillas se utilizan en una campaña o un recorrido, cualquier edición que realice en el contenido de la campaña y del recorrido no afectará a la plantilla de contenido utilizada anteriormente.


### Crear plantilla desde cero {#create-template-from-scratch}

Para crear una plantilla de contenido desde cero, siga los pasos a continuación.

1. Acceda a la lista de plantillas de contenido a través de la **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Plantillas de contenido]** menú izquierdo.

   ![](assets/content-template-list.png)

1. Select **[!UICONTROL Crear plantilla]**.

1. Rellene los detalles de la plantilla.

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >Actualmente solo el **Correo electrónico** canal y **HTML** son compatibles.

1. Para asignar etiquetas de uso de datos principales o personalizadas a la plantilla, seleccione **[!UICONTROL Administrar acceso]**. [Más información sobre Control de acceso a nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Haga clic en **[!UICONTROL Crear]** y elija cómo desea diseñar su correo electrónico desde las diferentes opciones:

   * [Diseñe su correo electrónico desde cero](content-from-scratch.md) a través de la interfaz del Diseñador de correo electrónico.

   * [Código o copiar y pegar HTML sin procesar](code-content.md) directamente en el Diseñador de correo electrónico.

   * [Importar contenido de HTML existente](existing-content.md) desde un archivo o una carpeta .zip.

   * Utilice contenido existente de una lista de plantillas integradas o personalizadas. Los pasos para utilizar una plantilla de contenido en un correo electrónico se describen en [esta sección](email-templates.md).

   ![](assets/content-template-design.png)

1. La variable [Diseñador de correo electrónico](get-started-email-design.md) se muestra. Edite el contenido según sea necesario, del mismo modo que lo haría para cualquier correo electrónico dentro de un recorrido o una campaña, según la opción seleccionada.

   ![](assets/content-template-designer.png)

1. Puede probar el contenido si es necesario. [Descubra cómo](#test-template)

1. Una vez que la plantilla esté lista, haga clic en **[!UICONTROL Guardar]**.

1. Si es necesario, haga clic en la flecha situada junto al nombre de la plantilla para volver al **[!UICONTROL Detalles]** y edite la plantilla.

   ![](assets/content-template-designer-back.png)

Esta plantilla ya está lista para utilizarse al crear cualquier correo electrónico dentro de [!DNL Journey Optimizer]. [Descubra cómo](email-templates.md)

### Guardar como plantilla {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Descubra cómo migrar sus mensajes"
>abstract="El 25 de julio de 2022, desapareció el menú Mensajes y ahora los mensajes se crean directamente desde un Recorrido. Si desea reutilizar los mensajes heredados en recorrido, debe guardarlos como plantillas."

Al diseñar una [email](get-started-email-design.md) en una campaña o un recorrido, puede guardar el contenido del correo electrónico para reutilizarlo en el futuro. Para realizar esto, siga los pasos a continuación.

1. En el Diseñador de correo electrónico, haga clic en los puntos suspensivos en la parte superior derecha de la pantalla.

1. Select **[!UICONTROL Guardar como plantilla de contenido]** en el menú desplegable.

   ![](assets/email_designer-save-template.png)

1. Añada un nombre y una descripción para esta plantilla.

   ![](assets/email_designer-template-name.png)

1. Haga clic en **[!UICONTROL Guardar]**.

1. La plantilla se guarda en el **[!UICONTROL Plantillas de contenido]** lista, accesible desde la [!DNL Journey Optimizer] menú específico. Se convierte en una plantilla de contenido independiente a la que se puede acceder, editar y eliminar como cualquier otro elemento de la lista. [Más información](#access-manage-templates)

Ahora puede usar esta plantilla al crear cualquier [email](get-started-email-design.md) en [!DNL Journey Optimizer]. [Descubra cómo](email-templates.md)

>[!NOTE]
>
>Cualquier cambio en esa nueva plantilla no se propaga al correo electrónico del que procede. Del mismo modo, cuando el contenido original se edita dentro de ese correo electrónico, la nueva plantilla no se modifica.

## Probar la plantilla de contenido {#test-template}

Puede probar la renderización de cualquier plantilla de contenido de correo electrónico, ya sea creada desde cero o a partir de un correo electrónico. Para ello, siga los pasos que aparecen a continuación.

>[!CAUTION]
>
>Para simular contenido, debe tener la variable **[!DNL Manage Simulate Content]** permiso incluido en la variable **[!DNL Content Library Manager]** perfil de producto. [Más información](../administration/ootb-product-profiles.md#content-library-manager)

1. Acceda a la lista de plantillas de contenido a través de la **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Plantillas de contenido]** y seleccione cualquier plantilla.

1. Haga clic en **[!UICONTROL Editar contenido]** de la variable **[!UICONTROL Propiedades de plantilla]**.

1. Haga clic en **[!UICONTROL Simular contenido]** y seleccione un perfil de prueba para comprobar el procesamiento de correo electrónico. Puede elegir la vista de escritorio o la vista móvil. [Más información](preview.md)

   ![](assets/content-template-stimulate.png)

1. Puede enviar una prueba para probar el contenido y conseguir que lo aprueben algunos usuarios internos antes de utilizarlo en un recorrido o una campaña.

   * Para ello, haga clic en el botón **[!UICONTROL Enviar prueba]** y siga los pasos descritos en [esta sección](preview.md#send-proofs).

   * Antes de enviar la prueba, debe seleccionar la opción [superficie del correo electrónico](../configuration/channel-surfaces.md) que se utilizará para probar el contenido.

      ![](assets/content-template-stimulate-proof-surface.png)

## Vídeo explicativo {#video-templates}

Obtenga información sobre cómo crear, editar y utilizar plantillas de contenido en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)