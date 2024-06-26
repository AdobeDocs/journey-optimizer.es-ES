---
solution: Journey Optimizer
product: journey optimizer
title: Creación de plantillas de contenido
description: Aprenda a crear plantillas para reutilizar contenido en campañas y recorridos de Journey Optimizer
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 14%

---


# Creación de plantillas de contenido {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Definir su propia plantilla de contenido"
>abstract="Cree una plantilla personalizada independiente desde cero para que el contenido se pueda reutilizar en varios recorridos y campañas."

Existen dos formas de crear plantillas de contenido:

* Cree una plantilla de contenido desde cero mediante el carril izquierdo **[!UICONTROL Plantillas de contenido]** menú. [Descubra cómo](#create-template-from-scratch)

* Al diseñar el contenido dentro de una campaña o un recorrido, guárdelo como una plantilla. [Descubra cómo](#save-as-template)

Una vez guardada, la plantilla de contenido está disponible para usarla en una campaña o un recorrido. Tanto si se crea desde cero como a partir de contenido anterior, ahora puede utilizar esta plantilla al crear cualquier contenido dentro de [!DNL Journey Optimizer]. [Descubra cómo](#use-content-templates)

>[!NOTE]
>
>* Los cambios realizados en las plantillas de contenido no se propagan a las campañas ni a los recorridos, ya estén activos o en borrador.
>
>* Del mismo modo, cuando las plantillas se utilizan en una campaña o un recorrido, las ediciones que realice en el contenido de la campaña y del recorrido no afectan a la plantilla de contenido utilizada anteriormente.

## Crear una plantilla desde cero {#create-template-from-scratch}

Para crear una plantilla de contenido desde cero, siga los pasos a continuación.

1. Acceda a la lista de plantillas de contenido a través de **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Plantillas de contenido]** menú izquierdo.

1. Seleccionar **[!UICONTROL Crear plantilla]**.

1. Complete los detalles de la plantilla y seleccione el canal deseado.

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >Actualmente, todos los canales están disponibles excepto la web.

1. Elija una **[!UICONTROL Tipo]** para el canal seleccionado.

   ![](assets/content-template-type.png)

   * Para **[!UICONTROL Correo electrónico]**, si selecciona **[!UICONTROL Contenido]**, puede definir la variable [Línea de asunto](../email/create-email.md#define-email-content) como parte de la plantilla. Si selecciona **[!UICONTROL HTML]**, solo puede definir el contenido del cuerpo del correo electrónico.

   * Para **[!UICONTROL SMS]**, **[!UICONTROL Push]**, **[!UICONTROL En la aplicación]** y **[!UICONTROL Correo directo]**, solo el tipo predeterminado está disponible para el canal actual. Aún debe seleccionarlo.

1. Seleccione o cree etiquetas de Adobe Experience Platform en **[!UICONTROL Etiquetas]** para categorizar la plantilla y mejorar la búsqueda. [Más información](../start/search-filter-categorize.md#tags)

1. Para asignar etiquetas de uso de datos personalizadas o principales a la plantilla, puede seleccionar **[!UICONTROL Administrar acceso]**. [Obtenga más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Clic **[!UICONTROL Crear]** y diseñe el contenido según sea necesario, del mismo modo que lo haría para cualquier contenido dentro de un recorrido o una campaña, según el canal que haya seleccionado.

   ![](assets/content-template-edition.png)

   Aprenda a crear contenido para los diferentes canales en las siguientes secciones:
   * [Definición del contenido del correo electrónico](../email/get-started-email-design.md)
   * [Definición del contenido push](../push/design-push.md)
   * [Definición del contenido SMS](../sms/create-sms.md#sms-content)
   * [Definición del contenido de correo directo](../direct-mail/create-direct-mail.md)
   * [Definición del contenido en la aplicación](../in-app/design-in-app.md)

1. Si está creando un **[!UICONTROL Correo electrónico]** plantilla con el **[!UICONTROL HTML]** escriba, puede probar el contenido. [Descubra cómo](#test-template)

1. Una vez preparada la plantilla, haga clic en **[!UICONTROL Guardar]**.

1. Haga clic en la flecha situada junto al nombre de la plantilla para volver al **[!UICONTROL Detalles]** pantalla.

   ![](assets/content-template-back.png)

Esta plantilla ya está lista para utilizarse al crear contenido en [!DNL Journey Optimizer]. [Descubra cómo](#use-content-templates)

## Guardar contenido como plantilla de contenido {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Aprenda a migrar sus mensajes"
>abstract="El 25 de julio de 2022, desapareció el menú Mensajes y ahora los mensajes se crean directamente desde un recorrido. Si desea reutilizar los mensajes heredados en recorridos, debe guardarlos como plantillas."

Al diseñar cualquier contenido en una campaña o un recorrido, puede guardarlo para su reutilización futura. Para realizar esto, siga los pasos a continuación.

1. Desde el mensaje **[!UICONTROL Editar contenido]** , haga clic en **[!UICONTROL Plantilla de contenido]** botón.

1. Seleccionar **[!UICONTROL Guardar como plantilla de contenido]** en el menú desplegable.

   ![](assets/content-template-button-save.png)

   Si está en la [Correo electrónico Designer](../email/get-started-email-design.md), también puede seleccionar esta opción desde el **[!UICONTROL Más]** en la parte superior derecha de la pantalla.

   ![](assets/content-template-more-button-save.png)

1. Añada un nombre y una descripción para esta plantilla.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >El canal y el tipo actuales se rellenan automáticamente y no se pueden editar. Para plantillas de correo electrónico creadas a partir de [Correo electrónico Designer](../email/get-started-email-design.md), el **[!UICONTROL HTML]** el tipo se selecciona automáticamente.

1. Seleccione o cree una etiqueta de Adobe Experience Platform en la **Etiquetas** para categorizar la plantilla. [Más información](../start/search-filter-categorize.md#tags)

1. Para asignar etiquetas de uso de datos personalizadas o principales a la plantilla, puede seleccionar **[!UICONTROL Administrar acceso]**. [Más información](../administration/object-based-access.md).

1. Haga clic en **[!UICONTROL Guardar]**.

1. La plantilla se guarda en el **[!UICONTROL Plantillas de contenido]** , accesible desde el [!DNL Journey Optimizer] menú específico. Se convierte en una plantilla de contenido independiente a la que se puede acceder, editar y eliminar como cualquier otro elemento de la lista. [Más información](#access-manage-templates)

Ahora puede utilizar esta plantilla al crear cualquier contenido en [!DNL Journey Optimizer]. [Descubra cómo](#use-content-templates)

>[!NOTE]
>
>Los cambios que se realicen en esa nueva plantilla no se propagarán al contenido del que procedan. Del mismo modo, cuando el contenido original se edita dentro de ese contenido, la nueva plantilla no se modifica.
