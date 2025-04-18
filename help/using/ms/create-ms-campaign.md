---
solution: Journey Optimizer
product: journey optimizer
title: Creación de campañas orquestadas con Journey Optimizer
description: Obtenga información sobre cómo crear una campaña orquestada con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 2%

---

# Creación de una campaña organizada {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Lista de campañas organizadas"
>abstract="La pestaña **multi-step** enumera todas las campañas orquestadas. Haga clic en el nombre de una campaña orquestada para editarla. Utilice el botón **Crear campaña orquestada** para agregar una nueva campaña orquestada."

## Requisitos previos

### Permisos

### Configuración

Información general sobre la nueva configuración de administración > esquemas, campos de ejecución, política de combinación. [Más información](ms-schemas.md)


## Pasos para la creación

Para crear una campaña orquestada, siga estos pasos:

1. Para crear una **campaña orquestada**, vaya al menú **Campañas**.

1. Haga clic en el botón **[!UICONTROL Crear campaña orquestada]** en la esquina superior derecha de la pantalla.

1. En el cuadro de diálogo **Propiedades** de la campaña orquestada, seleccione la plantilla que desee utilizar para crear la campaña orquestada (también puede utilizar la plantilla integrada predeterminada). [Más información sobre las plantillas de campañas orquestadas](#campaign-templates).

1. Introduzca una etiqueta para la campaña organizada. Además, le recomendamos encarecidamente que agregue una descripción a su campaña orquestada, en el campo dedicado de la sección **[!UICONTROL Opciones adicionales]** de la pantalla.

1. Expanda la sección **[!UICONTROL Opciones adicionales]** para configurar más opciones para la campaña orquestada.

1. Haga clic en el botón **[!UICONTROL Crear campaña orquestada]** para confirmar la creación de la campaña orquestada.

La campaña orquestada se habrá creado y estará disponible en la lista de flujos de trabajo. Ahora puede acceder a su lienzo visual y empezar a agregar, configurar y organizar las tareas que va a realizar. [Aprenda a organizar actividades de campañas orquestadas](orchestrate-activities.md).

## Uso de plantillas de campaña orquestadas {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Plantillas de campaña organizadas"
>abstract="Las plantillas de campaña orquestadas contienen configuraciones y actividades preconfiguradas que se pueden reutilizar para crear una nueva campaña orquestada."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Propiedades de campaña organizadas"
>abstract="Las plantillas de campaña orquestadas contienen configuraciones y actividades preconfiguradas que se pueden reutilizar para crear nuevas campañas orquestadas. En esta pantalla, introduzca la etiqueta de la plantilla de campaña orquestada y configure sus opciones, como el nombre interno, las carpetas de carpeta y ejecución, la zona horaria y el grupo del supervisor."

Las plantillas de campaña orquestadas contienen configuraciones y actividades preconfiguradas que se pueden reutilizar para crear nuevas campañas orquestadas. Puede seleccionar la plantilla de la campaña orquestada desde las propiedades de la campaña orquestada al crear una campaña orquestada. De forma predeterminada, se proporciona una plantilla vacía.

Puede crear una plantilla a partir de una campaña orquestada existente o crear una nueva plantilla desde cero. Ambos métodos se detallan a continuación.

>[!BEGINTABS]

>[!TAB Crear una plantilla a partir de una campaña orquestada existente]

Para crear una plantilla de campaña orquestada a partir de una campaña orquestada existente, siga estos pasos:

1. Abra el menú **Campaign** y vaya a la campaña orquestada para guardarla como plantilla.
1. Haga clic en los tres puntos a la derecha del nombre de la campaña orquestada y elija **Copiar como plantilla**.
1. En la ventana emergente, confirme la creación de la plantilla.
1. En el lienzo de la plantilla de campaña orquestada, compruebe, añada y configure las actividades según sea necesario.
1. Vaya a la configuración, en el botón **Configuración**, para cambiar el nombre de la plantilla de campaña orquestada e introduzca una descripción.
1. Seleccione la **carpeta** y la **carpeta de ejecución** de la plantilla. La carpeta es la ubicación donde se guarda la plantilla de campaña orquestada. La carpeta de ejecución es la carpeta en la que se guardan las campañas orquestadas creadas en función de esta plantilla.
1. Guarde los cambios.

La plantilla de campaña orquestada ya está disponible en la lista de plantillas. Puede crear una campaña orquestada basada en esta plantilla. Esta campaña orquestada se preconfigura con la configuración y las actividades definidas en la plantilla.


>[!TAB Crear una plantilla desde cero]


Para crear una plantilla de campaña orquestada desde cero, siga estos pasos:

1. Abra el menú **Campaign** y vaya a la ficha **Plantillas**. Puede ver la lista de plantillas de campaña organizadas disponibles.
1. Haga clic en el botón **[!UICONTROL Crear plantilla]** en la esquina superior derecha de la pantalla.
1. Introduzca la etiqueta y abra las opciones adicionales para introducir una descripción de la plantilla de campaña orquestada.
1. Seleccione la carpeta y la carpeta de ejecución de la plantilla. La carpeta es la ubicación donde se guarda la plantilla de campaña orquestada. La carpeta de ejecución es la carpeta en la que se guardan las campañas orquestadas creadas en función de esta plantilla.
1. Haga clic en el botón **Crear** para confirmar la configuración.
1. En el lienzo de la plantilla de campaña orquestada, añada y configure las actividades según sea necesario.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Guarde los cambios.

La plantilla de campaña orquestada ya está disponible en la lista de plantillas. Puede crear una campaña orquestada basada en esta plantilla. Esta campaña orquestada se preconfigura con la configuración y las actividades definidas en la plantilla.

>[!ENDTABS]
