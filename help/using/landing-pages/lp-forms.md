---
solution: Journey Optimizer
product: journey optimizer
title: Crear y usar formularios para las páginas de aterrizaje
description: Aprenda a crear y utilizar formularios para sus páginas de aterrizaje en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: aterrizaje, página de aterrizaje, creación, página, formulario
badge: label="Disponibilidad limitada" type="Informative"
hidefromtoc: true
hide: true
source-git-commit: 67283fe92282ce23c97c29fa2c0ad78132cc184a
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 2%

---

# Uso de formularios en las páginas de aterrizaje {#lp-forms}

>[!AVAILABILITY]
>
>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

Para capturar datos de perfil con sus páginas de aterrizaje de [!DNL Journey Optimizer] y enriquecer los conjuntos de datos de [!DNL Experience Platform], puede aprovechar los formularios en sus páginas de aterrizaje.

## Crear un ajuste preestablecido de formulario {#create-form-preset}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_connection"
>title="Seleccione el extremo que desea utilizar"
>abstract="Defina el punto final de flujo continuo al que se envían los datos al enviar el formulario."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-platform/sources/ui-tutorials/create/streaming/http" text="Creación de una conexión de flujo continuo HTTP API"

>[!CONTEXTUALHELP]
>id="ajo_lp_form_dataset"
>title="Selección de un conjunto de datos"
>abstract="Defina un conjunto de datos en el que se almacenarán y reflejarán las respuestas del formulario. Puede escribir para buscar un conjunto de datos específico o seleccionarlo en la lista."

Antes de poder crear un formulario, debe crear un ajuste preestablecido dedicado en el que seleccione el punto final de conexión al que se envían los datos de envío del formulario y el conjunto de datos al que se almacenarán los datos capturados mediante el formulario.

Cuando los datos aterrizan en el extremo de flujo continuo, se vinculan con la información del conjunto de datos. Mediante las conexiones de origen/destino generadas y el flujo de origen, los datos se insertan en el conjunto de datos.

Al crear un ajuste preestablecido:

* Puede configurar varios ajustes preestablecidos utilizando diferentes combinaciones de conjuntos de datos y conexiones de flujo continuo.
* El mismo conjunto de datos o conexión de flujo continuo se puede reutilizar en varios ajustes preestablecidos.
* Cada conexión de flujo continuo genera automáticamente recursos como:
   * **Conexión de Source** - donde se originan los datos.
   * **Conexión de destino** - donde se almacenan o consumen los datos.
   * **Flujo de Source**: la canalización que mueve datos de la conexión de origen a [!DNL Experience Platform], y administra la asignación, la transformación y la validación.

>[!NOTE]
>
> Para acceder y editar los ajustes preestablecidos del formulario, debe tener el permiso **[!UICONTROL Administrar ajustes preestablecidos del formulario]** en la zona protegida de producción. Obtenga más información acerca de los permisos en [esta sección](../administration/high-low-permissions.md#administration-permissions).<!--TBC-->

1. Para obtener acceso al inventario de **[!UICONTROL Ajustes preestablecidos de formulario]**, seleccione **[!UICONTROL Administración]** > **[!UICONTROL Canales]** >**[!UICONTROL Configuración de formulario]** en el menú de la izquierda.

1. Haga clic en **[!UICONTROL Crear ajuste preestablecido de formulario]**.

1. Actualice el nombre para recuperarlo más fácilmente y añada una descripción si es necesario.

   ![](assets/lp_create-form-preset.png){width=80%}

1. Seleccione la **[!UICONTROL conexión de transmisión]** que se usará para ese formulario. Este es el punto final de streaming al que se envían los datos al enviar el formulario.

   >[!NOTE]
   >
   >Obtenga más información sobre cómo crear una conexión de origen de flujo continuo en la [documentación de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/sources/ui-tutorials/create/streaming/http){target="_blank"}.

1. Seleccione un **[!UICONTROL conjunto de datos]** para vincularlo con el formulario. Aquí es donde se almacenan y reflejan las respuestas del formulario. Puede escribir para buscar un conjunto de datos específico o seleccionarlo en la lista.

   >[!NOTE]
   >
   >Actualmente solo hay [!DNL Adobe Experience Platform] conjuntos de datos disponibles para su selección. Solo se puede seleccionar un conjunto de datos a la vez.

1. Haga clic en **[!UICONTROL Publicar]**. El ajuste preestablecido ya está listo para utilizarse en un formulario.

## Acceso y administración de formularios {#access-forms}

Para acceder a la lista del formulario, seleccione **[!UICONTROL Administración de contenido]** > **[!UICONTROL Forms]** en el menú de la izquierda.

Se muestran todos los formularios existentes. Puede filtrar los formularios en función de su estado, fecha de creación o modificación.

## Creación y diseño de un formulario {#create-form}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_preset"
>title="Seleccionar un ajuste preestablecido"
>abstract="Elija un ajuste preestablecido que contenga la conexión que se va a utilizar y un conjunto de datos predefinido para el formulario."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/content-management/landing-pages/lp-forms#create-form-preset" text="Crear un ajuste preestablecido de formulario"

Para crear un formulario, siga los pasos a continuación.

1. En la lista **[!UICONTROL Forms]**, haga clic en **[!UICONTROL Crear formulario]**.

1. Añada un nombre. Puede agregar una descripción si es necesario.

   ![](assets/lp_create-form.png)

1. Seleccione un **[!UICONTROL ajuste preestablecido]** que contenga la conexión que se utilizará y un conjunto de datos predefinido para el formulario. [Aprenda a crear un ajuste preestablecido de formulario](#create-form-preset)

1. Haga clic en **[!UICONTROL Crear]**.

   <!--![](assets/lp_create-form-filled.png){width=50%}-->

1. Se abre el diseñador de formularios. Agregue [componentes](../email/content-components.md#add-content-components) para generar el contenido del formulario. Puede usar los componentes [Texto](../email/content-components.md#text) y los componentes **[!UICONTROL Campo]**.

1. Con el componente **[!UICONTROL Field]**, puede seleccionar atributos basados en el esquema del conjunto de datos seleccionado.

   >[!NOTE]
   >
   >Para asignar los datos recopilados con un perfil, seleccione un campo de identidad de perfil. Para identificar los campos de identidad de la lista de atributos, busque los campos marcados como **[!UICONTROL Requerido]**.<!--Explain-->

   Por ejemplo, puede establecer el correo electrónico y el ID de persona. Cuando los usuarios rellenan estos campos, la información introducida se guarda en el conjunto de datos seleccionado.

   ![](assets/lp_create-form-fields.png)

1. Puede especificar cada **[!UICONTROL detalles del campo]**, como instrucciones, un valor predeterminado, un mensaje de validación, longitud máxima, etc.

   ![](assets/lp_create-form-field-details.png)

1. Puede ajustar el diseño, el estilo y las dimensiones del formulario según sea necesario mediante el panel **[!UICONTROL Estilos]**. [Más información sobre el estilo](../email/get-started-email-style.md)

1. Haga clic en **[!UICONTROL Guardar y cerrar]**.

1. Configure la página de agradecimiento. [Descubra cómo](#thank-you-page)

1. **[!UICONTROL Publicar]** el formulario para que esté disponible para su selección en páginas de aterrizaje.

### Configuración de la página de agradecimiento {#thank-you-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_forms_thankyou_page"
>title="Página de agradecimientos"
>abstract="Configure lo que sucede cuando alguien rellena o reenvía el formulario."

En la sección **[!UICONTROL Página de agradecimiento]**, configure lo que sucede cuando un usuario rellena el formulario.

![](assets/lp_create-form-thank-you.png){width=70%}

Configure una de las siguientes acciones:

* **[!UICONTROL Permanecer en la página]**: esta opción mantiene al visitante en la misma página cuando se envía el formulario.
* **[!UICONTROL Página de aterrizaje]**: seleccione una [página de aterrizaje](create-lp.md) publicada a la que se redirija al usuario después de enviar el formulario.
* **[!UICONTROL Dirección URL externa]**: escriba la dirección URL completa que desee como página de seguimiento. Una vez que el usuario ha enviado el formulario, se le dirige a la dirección URL especificada.
* **[!UICONTROL Redirección condicional]**: configure reglas para mostrar dinámicamente diferentes acciones de seguimiento basadas en las respuestas del formulario.

  Puede definir una regla para cada audiencia específica. Por ejemplo, puede mostrar una página de aterrizaje específica para residentes de EE. UU., otra página para residentes de Canadá, etc. Finalmente, configure una acción predeterminada para los usuarios que no entren en ninguna regla que haya definido.

  >[!NOTE]
  >
  >Las condiciones definidas en una regla se leen secuencialmente.

  ![](assets/lp_create-form-thank-you-conditional.png){width=40%}

## Aprovechamiento del formulario en una página de aterrizaje {#leverage-form-in-lp}

Ahora puede incrustar este formulario en una página de aterrizaje para capturar los datos correspondientes a los atributos definidos en el formulario y guardarlos en el conjunto de datos seleccionado. Siga los pasos a continuación.

1. Cree una página de aterrizaje. [Descubra cómo](create-lp.md#create-landing-page)

1. Seleccione **[!UICONTROL Captura de datos]** como tipo de página de aterrizaje y haga clic en **[!UICONTROL Crear]**.

   ![](assets/lp_create-lp-data-capture.png){width=65%}

1. Configure la página principal. [Descubra cómo](create-lp.md#configure-primary-page)

1. Abra [el diseñador de la página de aterrizaje](design-lp.md).

1. Arrastre y suelte un **[!UICONTROL componente de estructura]** en el contenido. Arrastre y suelte un componente **[!UICONTROL Form]** en esa estructura.

   >[!NOTE]
   >
   >Solo se pueden seleccionar formularios publicados en una página de aterrizaje.

1. En la sección **[!UICONTROL Incrustar formulario]**, seleccione el formulario que ha creado.

   ![](assets/lp_embed-form.png)

   >[!NOTE]
   >
   >Puede actualizar el formulario seleccionado mediante el botón **[!UICONTROL Editar formulario]**. El formulario se abrirá en una nueva pestaña. Los pasos para editar el contenido del formulario son los mismos que se describen en [esta sección](#create-form).

1. En la sección **[!UICONTROL Tipo de seguimiento]**, configure lo que sucede cuando un usuario rellena el formulario:

   * Elija **[!UICONTROL Formulario definido]** para seleccionar la acción definida en el formulario incrustado. [Más información](#thank-you-page)

   * También puede seleccionar una [página de aterrizaje](create-lp.md) publicada a la que se redireccione al usuario después de enviar el formulario.

   * O defina una **[!UICONTROL URL externa]** como la página de seguimiento a la que se dirigirá a los usuarios cuando envíen el formulario.

1. Guarde y pruebe la página de aterrizaje. [Descubra cómo](create-lp.md#test-landing-page)

Una vez que la página de aterrizaje es [publicada](create-lp.md#publish-landing-page) y se usa en un recorrido, cuando los usuarios rellenan el formulario, la información introducida se incorpora en el conjunto de datos seleccionado.

>[!NOTE]
>
>Si cancela la publicación de un formulario que se utiliza en una página de aterrizaje, edita este formulario y lo vuelve a publicar, la página de aterrizaje siempre utiliza la última versión publicada del formulario.
