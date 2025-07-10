---
solution: Journey Optimizer
product: journey optimizer
title: Inicio y monitorización de campañas orquestadas con Adobe Journey Optimizer
description: Obtenga información sobre cómo iniciar y supervisar campañas orquestadas con Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 0ae8372c179707a87a6b512a5420753a4aaef754
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 2%

---

# Creación de consultas de retargeting {#retarget}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/><b>[Redireccionamiento](retarget.md)</b> | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](activities/save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

Documentación en curso

>[!ENDSHADEBOX]

La reorientación le permite hacer un seguimiento de los destinatarios según su respuesta a una campaña orquestada anteriormente. Por ejemplo, puede enviar un segundo correo electrónico a los perfiles que recibieron pero no hicieron clic en el primero.

La campaña organizada proporciona dos fuentes de datos principales para esto:

- **Comentarios del mensaje**: captura eventos relacionados con la entrega, por ejemplo: mensajes enviados, abiertos, rechazados, etc.

- **Seguimiento de correo electrónico**: captura las acciones del usuario, por ejemplo, clics y aperturas.

## Crear una regla de redireccionamiento basada en comentarios

La regla de redireccionamiento basada en comentarios permite redireccionar los destinatarios según los eventos de envío de mensajes capturados en el conjunto de datos **Comentarios del mensaje**. Estos eventos incluyen resultados como mensajes enviados, abiertos, rechazados o marcados como correo no deseado.

Con estos datos, puede definir reglas para identificar a los destinatarios que recibieron un mensaje anterior pero que no interactuaron con él, lo que permite una comunicación de seguimiento basada en estados de entrega específicos.

1. Crear una nueva **campaña orquestada**.

2. Agregue una actividad **Generar audiencia** y establezca la dimensión de segmentación en **Destinatario (caas)**.

3. En el **Generador de reglas**, haga clic en **Agregar condición** y seleccione **Comentarios del mensaje** en el Selector de atributos. Haga clic en **Confirmar**.

4. Agregue una condición para **Estado de comentarios** y establezca el valor en **Mensaje enviado**.

5. Para dirigirse a una campaña orquestada específica:

   - Agregue otra condición, busque `entity` y navegue hasta:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Seleccione **Nombre de campaña organizada** y especifique el nombre de la campaña.

6. Para dirigirse a un mensaje o una actividad específicos dentro de esa campaña organizada:

   - Agregue otra condición, busque `entity` y navegue hasta:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Seleccione **Nombre de acción de campaña orquestada** y especifique el nombre de la acción de campaña.

     Para encontrar los nombres de las acciones, haga clic en el ![icono de información](assets/do-not-localize/info-icon.svg) junto a una actividad en el lienzo.

   >[!TIP]
   >
   >En lugar de usar nombres, también puede filtrar por el **ID de campaña** (UUID), que se encuentra en las propiedades de Campaign.

## Creación de una regla de retargeting basada en seguimiento

La regla de retargeting basada en el seguimiento identifica a los destinatarios según sus interacciones con un mensaje mediante los datos del conjunto de datos **Seguimiento de correo electrónico**. Registra acciones del usuario como aperturas de correo electrónico y clics en vínculos.

Para redirigir a los destinatarios en función de las interacciones de mensajes (p. ej., abrir o hacer clic), use la entidad **Seguimiento de correo electrónico** de la siguiente manera:

1. Cree una nueva **Campaña orquestada** y luego agregue una actividad **Generar audiencia** con **Destinatario (caas)** como dimensión de segmentación para centrarse en destinatarios de campañas orquestadas anteriores.

1. Agregar una nueva condición para **Seguimiento de correo electrónico**. Haga clic en **Confirmar** para crear una condición &quot;El seguimiento de correo electrónico existe como&quot;.

1. Dentro de esa condición, agregue una condición y busque el atributo **Interaction Type**.

1. En las opciones de condición personalizadas, use **Incluido en** como operador y seleccione uno o más valores según el caso de uso. Por ejemplo:
   - **Mensaje abierto**
   - **Se Hizo Clic En Vínculo De Mensaje**

1. Para asociar los datos de seguimiento a una campaña específica:

   - Añada una condición dentro del bloque de seguimiento de correo electrónico.

   - Vaya a `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Agregue condiciones tanto para **Nombre de campaña orquestada** como para **Nombre de acción de campaña orquestada**, si es necesario.

     Para encontrar los nombres de las acciones, haga clic en el ![icono de información](assets/do-not-localize/info-icon.svg) junto a una actividad en el lienzo.

   >[!TIP]
   >
   >En lugar de usar nombres, también puede filtrar por el **ID de campaña** (UUID), que se encuentra en las propiedades de Campaign.
