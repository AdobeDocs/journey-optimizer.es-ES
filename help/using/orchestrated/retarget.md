---
solution: Journey Optimizer
product: journey optimizer
title: Inicio y monitorización de campañas organizadas con Adobe Journey Optimizer
description: Obtenga información sobre cómo iniciar y monitorizar campañas orquestadas con Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 7%

---

# Creación de consultas de retargeting {#retarget}

+++ Índice

| Bienvenido a campañas orquestadas | Inicie su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Creación y programación de las campañas](create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabajo con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](build-query.md)<br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/><b>[Resegmentación](retarget.md)</b> | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

La reorientación le permite hacer un seguimiento de los destinatarios según su respuesta a una campaña orquestada anterior. Por ejemplo, puede enviar un segundo correo electrónico a los destinatarios que recibieron pero no hicieron clic en el primero.

**[!UICONTROL La campaña orquestada]** proporciona dos atributos principales para esto:

* **[!UICONTROL Comentarios del mensaje]**: captura eventos relacionados con la entrega, por ejemplo: mensajes enviados, abiertos, rechazados, etc.
* **[!UICONTROL Seguimiento de correo electrónico]**: captura las acciones del usuario, por ejemplo, clics y aperturas.

![](assets/do-not-localize/retarget-schema.png){zoomable="yes"}


## Crear una regla de redireccionamiento basada en comentarios {#feedback-retarget}

La regla de redireccionamiento basada en comentarios permite redireccionar los destinatarios según los eventos de envío de mensajes capturados con el atributo **[!UICONTROL Comentarios del mensaje]**. Estos eventos incluyen resultados como mensajes enviados, abiertos, rechazados o marcados como correo no deseado.

Con estos datos, se pueden definir reglas para identificar a los destinatarios que recibieron un mensaje anterior, lo que permite una comunicación de seguimiento basada en estados de entrega específicos.

1. Crear una nueva **[!UICONTROL campaña orquestada]**.

1. Agregue una actividad **[!UICONTROL Generar audiencia]** y establezca la dimensión de segmentación en **[!UICONTROL Destinatario (caas)]**.

1. En el **[!UICONTROL Generador de reglas]**, haga clic en **[!UICONTROL Agregar condición]** y seleccione **[!UICONTROL Comentarios sobre mensajes]** del **[!UICONTROL Selector de atributos]**. Haga clic en **[!UICONTROL Confirmar]** para crear un **mensaje de comentarios ya existe como** condición.

   ![](assets/retarget_1.png){zoomable="yes"}

1. Elija el atributo **[!UICONTROL Estado de comentarios]** para segmentar los eventos de envío de mensajes.

+++ Detallado paso a paso

   1. Agregue otra condición vinculada al atributo **[!UICONTROL Message feedback]**.

   1. Busque el atributo **[!UICONTROL Estado de comentarios]** y haga clic en **[!UICONTROL Confirmar]**.

      ![](assets/retarget_3.png){zoomable="yes"}

   1. En el menú **[!UICONTROL Condición personalizada]**, elija qué estado de entrega rastrear en la lista desplegable **[!UICONTROL Valor]**.

      ![](assets/retarget_4.png){zoomable="yes"}

+++

1. Elija el atributo **[!UICONTROL Nombre de campaña orquestada]** para segmentar una campaña orquestada específica.

+++ Detallado paso a paso

   1. Agregue otra condición vinculada al atributo **[!UICONTROL Message feedback]**, busque **[!UICONTROL entity]** y navegue hasta:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Seleccione **[!UICONTROL Nombre de campaña orquestada]**.

      ![](assets/retarget_5.png){zoomable="yes"}

   1. En el menú **[!UICONTROL Condición personalizada]**, especifique el nombre de la campaña en el campo **[!UICONTROL Valor]**.

+++

1. Elija el atributo **[!UICONTROL Nombre de acción de campaña orquestada]** para segmentar un mensaje o una actividad específicos dentro de una campaña orquestada.

+++ Detallado paso a paso

   1. Agregue otra condición vinculada al atributo **[!UICONTROL Message feedback]**, busque **[!UICONTROL entity]** y navegue hasta:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Seleccione **[!UICONTROL Nombre de acción de campaña orquestada]**.

      ![](assets/retarget_6.png){zoomable="yes"}

   1. En el menú **[!UICONTROL Custom condition]**, especifique el nombre de la acción de campaña en el campo **[!UICONTROL Value]**.

      Para encontrar los nombres de las acciones, haga clic en el ![icono de información](assets/do-not-localize/info-icon.svg) junto al campo Etiqueta de su actividad.

+++

1. También puede filtrar por **[!UICONTROL ID de campaña]** (UUID), que se encuentra en las propiedades de Campaign.

Ahora ha configurado una regla de redireccionamiento basada en los comentarios para identificar a los destinatarios en función del estado de entrega de un mensaje anterior, como enviado, abierto, devuelto o marcado como correo no deseado. Con esta audiencia definida, puede agregar un correo electrónico de seguimiento o refinar aún más su segmentación si [configura una regla de retargeting basada en seguimiento](#tracking-based), que usa datos de interacción del usuario.

![](assets/retarget_9.png){zoomable="yes"}


## Creación de una regla de retargeting basada en seguimiento {#tracking-based}

La regla de retargeting basada en el seguimiento identifica a los destinatarios según sus interacciones con un mensaje mediante los datos del atributo **[!UICONTROL Email Tracking]**. Registra acciones del usuario como aperturas de correo electrónico y clics en vínculos.

Para redirigir a los destinatarios en función de las interacciones de mensajes (p. ej., abrir o hacer clic), use la entidad **[!UICONTROL Seguimiento de correo electrónico]** de la siguiente manera:

1. Crear una nueva **[!UICONTROL campaña orquestada]**.

1. Agregue una actividad **[!UICONTROL Generar audiencia]** y establezca la dimensión de segmentación en **[!UICONTROL Destinatario (caas)]** para que se centre en destinatarios de campañas orquestadas anteriores.

1. En el **[!UICONTROL Generador de reglas]**, haga clic en **[!UICONTROL Agregar condición]** y seleccione **[!UICONTROL Seguimiento de correo electrónico]** del **[!UICONTROL Selector de atributos]**.

   Haga clic en **[!UICONTROL Confirmar]** para crear una condición **Existe seguimiento de correo electrónico como**.

   ![](assets/retarget_2.png){zoomable="yes"}

1. Para segmentar las interacciones de los destinatarios con un mensaje, agregue otra condición vinculada al atributo **[!UICONTROL Email tracking]** y busque el atributo **[!UICONTROL Interaction Type]**.

   ![](assets/retarget_7.png){zoomable="yes"}

1. En las opciones de condición personalizadas, usa **[!UICONTROL Incluido en]** como operador y selecciona uno o más valores según tu caso de uso, por ejemplo **[!UICONTROL Mensaje abierto]** o **[!UICONTROL Se hizo clic en el vínculo del mensaje]**.

   ![](assets/retarget_8.png){zoomable="yes"}

Ahora ha configurado una regla de retargeting basada en el seguimiento para segmentar destinatarios según sus interacciones con un mensaje anterior, como aperturas de correo electrónico o clics en vínculos, con datos del atributo **[!UICONTROL Email Tracking]**. Con esta audiencia definida, puede agregar una acción de seguimiento o refinar aún más su segmentación combinándola con una [regla de retargeting basada en comentarios](#feedback-retarget) para incluir resultados de mensajes como enviados, rechazados o marcados como correo no deseado.


![](assets/retarget_10.png){zoomable="yes"}
