---
solution: Journey Optimizer
product: journey optimizer
title: AEM Trabajo con plantillas de
description: AEM Obtenga información sobre cómo crear plantillas en y exportarlas a Journey Optimizer
hide: true
hidefromtoc: true
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informativo"
source-git-commit: 7a044f7c048ba797e7b857212f6d6b0cf2644b5d
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 1%

---

# Trabajo con plantillas de Adobe Experience Manager {#aem-templates}

>[!AVAILABILITY]
>
>La integración con Adobe Experience Manager está disponible actualmente como una versión beta para usuarios seleccionados.
> Como usuario beta, utilice [este formulario](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} para compartir comentarios.

Con Adobe Journey Optimizer, puede crear mensajes personalizados a través de los sitios de Adobe Experience Manager. Comience por diseñar las plantillas utilizando las fuentes de contenido de Adobe Experience Manager y, a continuación, envíelas a Adobe Journey Optimizer. Una vez compartidas, se puede acceder a estas plantillas en el diseñador de correo electrónico de Adobe Journey Optimizer, lo que simplifica el proceso de creación y envío de mensajes a la audiencia deseada.

## Requisitos previos {#prerequisites}

Antes de empezar a utilizar esta capacidad, asegúrese de estar alineado con los siguientes requisitos:

* **configuración del Experience Manager**

   Esta capacidad está disponible con [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/overview/introduction.html){target="_blank"}.

   Como parte del programa beta, la configuración del Cloud Service se realiza mediante el Adobe en Adobe Experience Manager para conectarse a Adobe Journey Optimizer.

* **Permisos**

   Para crear, editar y eliminar plantillas de contenido en Adobe Journey Optimizer, debe tener **[!DNL Manage Library Items]** permiso incluido en el **[!DNL Content Library Manager]** perfil del producto. [Más información](../administration/ootb-product-profiles.md#content-library-manager)

## Mecanismos de protección y limitaciones{#aem-templates-limitations}

Para optimizar aún más el uso de Adobe Experience Manager con Adobe Journey Optimizer, es importante tener en cuenta las siguientes limitaciones y protecciones adicionales:

* Se requiere una sintaxis de Journey Optimizer adecuada para que la personalización en la plantilla del Experience Manager sea eficaz. [Más información](../personalization/personalization-syntax.md)

* Actualmente no se admite la exportación masiva de plantillas, las plantillas deben exportarse individualmente.

* Actualmente no está disponible la sincronización entre Experience Manager y Journey Optimizer. Si se realizan cambios en una plantilla de Experience Manager después de enviarla a Journey Optimizer, el usuario deberá volver a exportarla y enviarla de nuevo a Journey Optimizer.

## Envío de una plantilla a Journey Optimizer{#aem-templates-send}

Para exportar una plantilla de Adobe Experience Manager a Adobe Journey Optimizer, siga los pasos a continuación:

1. En la página de inicio de Adobe Experience Manager, seleccione **[!UICONTROL Marketing saliente]**.

   ![](assets/aem-outbound-menu.png)

1. Desde la biblioteca de contenido, puede utilizar plantillas configuradas anteriormente o crear una desde cero. [Más información](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

1. Al incorporar la sintaxis de personalización de Journey Optimizer en la plantilla, puede mejorar sus capacidades de personalización. [Más información](../personalization/personalization-syntax.md)

   ![](assets/aem_ajo_4.png)

1. Seleccione la plantilla que desee exportar a Journey Optimizer y haga clic en **[!UICONTROL Enviar a]** en el menú avanzado.

   ![](assets/aem-advanced-menu.png)

1. Introduzca el **[!UICONTROL Nombre]** de la plantilla Content y seleccione el destinatario **[!UICONTROL Sandbox]**.

   ![](assets/aem-send-template-settings.png)

1. Después de hacer clic en el botón **[!UICONTROL Enviar]** botón, se iniciará el proceso de exportación. Una vez completada la exportación, verá el siguiente mensaje en la interfaz de usuario: &quot;Template &quot;XX&quot; sent successfully to AJO&quot;.

La plantilla se agrega a las plantillas de contenido de Adobe Journey Optimizer de la zona protegida seleccionada.

## Uso y personalización de una plantilla de Adobe Experience Manager{#aem-templates-perso}

Una vez que la plantilla de Experience Manager esté disponible en Journey Optimizer como plantilla de contenido, puede identificar e incorporar el contenido necesario para el correo electrónico, incluida la personalización.

1. En Journey Optimizer, desde el **[!UICONTROL Plantilla de contenido]** , acceda a la plantilla importada.

   ![](assets/aem_ajo_1.png)

1. Al hacer clic en **[!UICONTROL Alerta]** botón, puede comprobar rápidamente si falta alguna configuración importante. Esto le ayudará a asegurarse de que sus mensajes estén correctamente configurados y a evitar posibles errores o problemas.

   ![](assets/aem_ajo_2.png)

1. En el **[!UICONTROL Propiedades de plantilla]** , haga clic en la **[!UICONTROL Administrar acceso]** para asignar etiquetas de uso de datos personalizadas o principales a la plantilla. [Obtenga más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md)

1. Para personalizar aún más la plantilla de Experience Manager y agregar una personalización personalizada al contenido, haga clic en **[!UICONTROL Editar contenido]**. Esto le permitirá realizar cambios fácilmente y adaptar la plantilla a sus necesidades específicas. [Más información](get-started-email-design.md)

   >[!NOTE]
   >
   > Si desea editar y personalizar la plantilla, solo podrá utilizar el modo de compatibilidad.

1. Cuando la plantilla de contenido esté lista, [prueba y validación](content-templates.md#test-template).

1. Una vez definido el contenido, puede utilizarlo al crear nuevos correos electrónicos explorando el **[!UICONTROL Plantillas guardadas]** colección. A continuación, seleccione **[!UICONTROL Usar esta plantilla]**.

   ![](assets/aem_ajo_3.png)

1. Ahora puede editar y personalizar el contenido. Para obtener más información sobre cómo crear el contenido del correo electrónico, consulte esta [página](content-from-scratch.md).

   ![](assets/aem_ajo_5.png)

1. Si ha añadido contenido personalizado a la plantilla de Experience Manager, haga clic en **[!UICONTROL Simular contenido]** para previsualizar cómo aparecerá en el mensaje mediante perfiles de prueba.

[Más información sobre la vista previa y los perfiles de prueba](../email/preview.md)

   ![](assets/aem_ajo_6.png)

1. Al ver la vista previa del mensaje, los elementos personalizados se sustituyen automáticamente por los datos correspondientes del perfil de prueba seleccionado.

   Si es necesario, se pueden añadir perfiles de prueba adicionales mediante la variable **[!UICONTROL Administración de perfiles de prueba]** botón.

   ![](assets/aem_ajo_7.png)

Cuando el correo electrónico esté listo, complete la configuración de su [recorrido](../building-journeys/journey-gs.md) o [campaña](../campaigns/create-campaign.md)y actívelo para enviar el mensaje.
