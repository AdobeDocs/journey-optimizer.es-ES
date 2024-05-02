---
solution: Journey Optimizer
product: journey optimizer
title: Creación de plantillas de contenido
description: Aprenda a crear plantillas para reutilizar contenido en campañas y recorridos de Journey Optimizer
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 327de13a-1c99-4d5e-86cf-8180fb7aaf23
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '1411'
ht-degree: 10%

---

# Trabajo con plantillas de contenido {#content-templates}

Para un proceso de diseño acelerado y mejorado, puede crear plantillas independientes para reutilizar fácilmente el contenido personalizado en [!DNL Journey Optimizer] campañas y recorridos.

Esta funcionalidad permite a los usuarios orientados a contenido trabajar en plantillas fuera de campañas o recorridos. Los usuarios de marketing pueden reutilizar y adaptar estas plantillas de contenido independientes dentro de sus propios recorridos o campañas.

<!--![](../rn/assets/do-not-localize/content-template.gif)-->

>[!NOTE]
>
>Actualmente, las plantillas de contenido no están disponibles para el canal Web.

Por ejemplo: un usuario de su compañía solo está a cargo del contenido y, por lo tanto, no tiene acceso a campañas ni recorridos. Sin embargo, este usuario puede crear una plantilla de correo electrónico que los especialistas en marketing de su organización podrán seleccionar para utilizarla en todos los correos electrónicos como punto de partida.

También puede crear y administrar plantillas de contenido mediante API. Para obtener más información, consulte [Documentación de API de Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.

➡️ [Aprenda a crear y utilizar plantillas en este vídeo](#video-templates)

>[!CAUTION]
>
>Para crear, editar y eliminar plantillas de contenido, debe tener **[!DNL Manage library items]** permiso incluido en el **[!DNL Content Library Manager]** perfil del producto. [Más información](../administration/ootb-product-profiles.md#content-library-manager)

## Acceso y administración de plantillas {#access-manage-templates}

Para acceder a la lista de plantillas de contenido, seleccione **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Plantillas de contenido]** en el menú de la izquierda.

![](assets/content-template-list.png)

Todas las plantillas que se crearon en la zona protegida actual, ya sea desde un recorrido o desde una campaña utilizando **[!UICONTROL Guardar como plantilla]** , ya sea desde la opción **[!UICONTROL Plantillas de contenido]** menú: se muestran. [Aprenda a crear plantillas](#create-content-templates)

Puede ordenar las plantillas de contenido por:
* Tipo
* Canal
* Fecha de creación o modificación
* Etiquetas - [Más información sobre las etiquetas](../start/search-filter-categorize.md#tags)

También puede elegir mostrar únicamente los elementos que ha creado o modificado.

![](assets/content-template-list-filters.png)

* Para editar el contenido de una plantilla, haga clic en el elemento deseado de la lista y seleccione **[!UICONTROL Editar contenido]**.

  ![](assets/content-template-edit.png)

* Para eliminar una plantilla, seleccione la **[!UICONTROL Más acciones]** junto a la plantilla deseada y seleccione **[!UICONTROL Eliminar]**.

  ![](assets/content-template-list-delete.png)

>[!NOTE]
>
>Cuando se edita o elimina una plantilla, las campañas o los recorridos, incluido el contenido creado con esta plantilla, no se ven afectados.

### Mostrar plantillas como miniaturas {#template-thumbnails}

Seleccione el **[!UICONTROL Vista de cuadrícula]** para mostrar cada plantilla como una miniatura.

>[!AVAILABILITY]
>
>Esta capacidad se lanza con disponibilidad limitada (LA) para un pequeño conjunto de clientes.

![](assets/content-template-grid-view.png)

>[!NOTE]
>
>Actualmente, solo se pueden generar las miniaturas adecuadas para plantillas de contenido de correo electrónico de tipo HTML.

Al actualizar un contenido, es posible que tenga que esperar unos segundos antes de que los cambios se reflejen en la miniatura.

## Creación de plantillas de contenido {#create-content-templates}

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

### Crear una plantilla desde cero {#create-template-from-scratch}

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

### Guardar como plantilla {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Aprenda a migrar sus mensajes"
>abstract="El 25 de julio de 2022, desapareció el menú Mensajes y ahora los mensajes se crean directamente desde un recorrido. Si desea reutilizar los mensajes heredados en recorridos, debe guardarlos como plantillas."

Al diseñar cualquier contenido en una campaña o un recorrido, puede guardarlo para su reutilización futura. Para realizar esto, siga los pasos a continuación.

1. Desde el mensaje **[!UICONTROL Editar contenido]** , haga clic en **[!UICONTROL Plantilla de contenido]** botón.

1. Seleccionar **[!UICONTROL Guardar como plantilla de contenido]** en el menú desplegable.

   ![](assets/content-template-button-save.png)

   Si está en la [Diseñador de correo electrónico](../email/get-started-email-design.md), también puede seleccionar esta opción desde el **[!UICONTROL Más]** en la parte superior derecha de la pantalla.

   ![](assets/content-template-more-button-save.png)

1. Añada un nombre y una descripción para esta plantilla.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >El canal y el tipo actuales se rellenan automáticamente y no se pueden editar. Para plantillas de correo electrónico creadas a partir de [Diseñador de correo electrónico](../email/get-started-email-design.md), el **[!UICONTROL HTML]** el tipo se selecciona automáticamente.

1. Seleccione o cree una etiqueta de Adobe Experience Platform en la **Etiquetas** para categorizar la plantilla. [Más información](../start/search-filter-categorize.md#tags)

1. Para asignar etiquetas de uso de datos personalizadas o principales a la plantilla, puede seleccionar **[!UICONTROL Administrar acceso]**. [Más información](../administration/object-based-access.md).

1. Haga clic en **[!UICONTROL Guardar]**.

1. La plantilla se guarda en el **[!UICONTROL Plantillas de contenido]** , accesible desde el [!DNL Journey Optimizer] menú específico. Se convierte en una plantilla de contenido independiente a la que se puede acceder, editar y eliminar como cualquier otro elemento de la lista. [Más información](#access-manage-templates)

Ahora puede utilizar esta plantilla al crear cualquier contenido en [!DNL Journey Optimizer]. [Descubra cómo](#use-content-templates)

>[!NOTE]
>
>Los cambios que se realicen en esa nueva plantilla no se propagarán al contenido del que procedan. Del mismo modo, cuando el contenido original se edita dentro de ese contenido, la nueva plantilla no se modifica.

## Prueba de plantillas de contenido de correo electrónico {#test-template}

Puede probar la renderización de algunas de las plantillas de correo electrónico, tanto si se crean desde cero como a partir de contenido existente. Para ello, siga los pasos que aparecen a continuación.

1. Acceda a la lista de plantillas de contenido a través de **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Plantillas de contenido]** y seleccione cualquier plantilla de correo electrónico.

1. Clic **[!UICONTROL Editar contenido]** desde el **[!UICONTROL Propiedades de plantilla]**.

1. Clic **[!UICONTROL Simular contenido]** y seleccione un perfil de prueba para comprobar la renderización. [Más información](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. Puede enviar una prueba para probar el contenido y que sea aprobado por algunos usuarios internos antes de utilizarlo en un recorrido o una campaña.

   * Para ello, haga clic en el **[!UICONTROL Enviar prueba]** y siga los pasos descritos en [esta sección](../content-management/proofs.md).

   * Antes de enviar la prueba, debe seleccionar [superficie de correo electrónico](../configuration/channel-surfaces.md) que se utilizará para probar el contenido.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Actualmente, el seguimiento no es compatible con las plantillas de contenido de prueba de correo electrónico, lo que significa que el seguimiento de eventos, parámetros de UTM y vínculos de página de aterrizaje no serán efectivos en las pruebas que se envían desde una plantilla. Para probar el seguimiento, [usar la plantilla de contenido](../email/use-email-templates.md) en un correo electrónico y [enviar una prueba](../content-management/preview-test.md#send-proofs).

## Uso de plantillas de contenido {#use-content-templates}

Al crear contenido para cualquier canal (excepto Web) en [!DNL Journey Optimizer], puede utilizar una plantilla personalizada que le permita:

* Creado desde cero utilizando **[!UICONTROL Plantillas de contenido]** menú. [Más información](#create-template-from-scratch)

* Se guardan desde un contenido existente en un recorrido o una campaña utilizando **[!UICONTROL Guardar como plantilla de contenido]** opción. [Más información](#save-as-template)

Para empezar a crear contenido con una de estas plantillas, siga los pasos a continuación.

1. Ya sea en una campaña o en un recorrido, después de seleccionar **[!UICONTROL Editar contenido]**, haga clic en **[!UICONTROL Plantilla de contenido]** botón.

1. Seleccionar **[!UICONTROL Aplicar plantilla de contenido]**.

   ![](assets/content-template-button.png)

1. Seleccione la plantilla que desee en la lista. Solo se muestran las plantillas compatibles con el canal o tipo seleccionado.

   ![](assets/content-template-select.png)

   >[!NOTE]
   >
   >Desde esta pantalla, también puede crear una nueva plantilla con el botón dedicado, que abre una nueva pestaña.

1. Clic **[!UICONTROL Confirmar]**. La plantilla se aplicará al contenido.

1. Continúe editando el contenido como desee.

>[!NOTE]
>
>Para empezar a diseñar un correo electrónico a partir de una plantilla de contenido con [Diseñador de correo electrónico](../email/get-started-email-design.md), siga los pasos descritos en [esta sección](../email/use-email-templates.md).

## Vídeo explicativo {#video-templates}

Aprenda a crear, editar y utilizar plantillas de contenido en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)
