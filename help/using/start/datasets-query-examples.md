---
title: Ejemplos de consultas de conjuntos de datos
description: Ejemplos de consultas de conjuntos de datos
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 5a6e18e6ff236d25bd5f81b42430be2998208321
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---

# Casos de uso de conjuntos de datos {#tracking-datasets}

En esta página, encontrará la lista de conjuntos de datos de Adobe Journey Optimizer y casos de uso relacionados:

[Conjunto de datos de evento de seguimiento de correo electrónico](../start/datasets-query-examples.md#email-tracking-experience-event-dataset)
[Conjunto de datos del evento de comentarios del mensaje](../start/datasets-query-examples.md#message-feedback-event-dataset)
[Conjunto de datos del evento de seguimiento push](../start/datasets-query-examples.md#push-tracking-experience-event-dataset)
[Evento de paso de recorrido](../start/datasets-query-examples.md#journey-step-event)
[Conjunto de datos de evento de offer decisioning](../start/datasets-query-examples.md#ode-decisionevents)
[Conjunto de datos del servicio de consentimiento](../start/datasets-query-examples.md#consent-service-dataset)
[Conjunto de datos de evento de comentarios de BCC](../start/datasets-query-examples.md#bcc-feedback-event-dataset)

## Conjunto de datos de evento de seguimiento de correo electrónico{#email-tracking-experience-event-dataset}

_Nombre en la interfaz : Conjunto de datos del evento de experiencia de seguimiento de correo electrónico CJM_

Conjunto de datos del sistema para la ingesta de eventos de experiencia de seguimiento de correo electrónico desde Journey Optimizer.

El esquema relacionado es CJM Email Tracking Experience Event Schema.

Esta consulta muestra los recuentos de diferentes interacciones de correo electrónico (aperturas, clics) para un mensaje determinado:

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageInteraction.interactionType
```

Esta consulta muestra el desglose de recuentos de diferentes interacciones de correo electrónico (aperturas, clics) por mensaje para un recorrido determinado:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
limit 100;
```

## Conjunto de datos del evento de comentarios del mensaje{#message-feedback-event-dataset}

_Nombre en la interfaz: Conjunto de datos del evento de comentarios de mensajes CJM_

Conjunto de datos para la ingesta de correos electrónicos y eventos de comentarios de aplicaciones push desde Journey Optimizer.

El esquema relacionado es Esquema de eventos de comentarios de mensajes CJM.

Esta consulta muestra los recuentos de diferentes estados de comentarios de correo electrónico (enviado, rechazado, etc.) para un mensaje determinado:

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus;
```

Esta consulta muestra el desglose de recuentos de diferentes estados de comentarios de correo electrónico (enviados, rechazados, etc.) por mensaje para un recorrido determinado:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
limit 100;
```

En el nivel de agregado, informe de nivel de dominio (ordenado por dominios principales): Nombre de dominio, mensaje enviado, devoluciones

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

Los envíos de correo electrónico se realizan diariamente:

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Encuentre si un id. de correo electrónico en particular recibió un correo electrónico o no y, si no, cuál fue el error, la categoría de rechazo, el código:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Encuentre la lista de todos los id de correo electrónico individuales que han tenido un error en particular, una categoría de rechazo o un código en las últimas x horas/días o que están asociados a un envío de mensaje en particular:

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Tasa de salida hacia otro sitio a nivel agregado:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Errores permanentes agrupados por código de rechazo:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

## Conjunto de datos del evento de seguimiento push {#push-tracking-experience-event-dataset}

_Nombre en la interfaz: Conjunto de datos del evento de experiencia de seguimiento push CJM_

Conjunto de datos para la ingesta de eventos de experiencia de seguimiento móvil para la inserción desde Journey Optimizer.

El esquema relacionado es CJM Push Tracking Experience Event Schema.

Ejemplo de consulta:

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from cjm_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from cjm_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```
## Evento de paso de recorrido{#journey-step-event}

_Nombre interno: Eventos de paso de recorrido (conjunto de datos del sistema)_

Conjunto de datos para la ingesta de eventos de paso en el recorrido.

El esquema relacionado es Recorrido Step Event schema for Journey Orchestration.

Esta consulta muestra el desglose de recuentos de éxito de acción por etiqueta de acción para un recorrido determinado:

```sql
select
    _experience.journeyOrchestration.stepEvents.actionName AS actionLabel,
    count(1) actionSuccessCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.actionID IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionType IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode IS NULL
group by
    _experience.journeyOrchestration.stepEvents.actionName;   
```

Esta consulta muestra el desglose de los recuentos de pasos introducidos por nodeId y nodeLabel para un recorrido determinado. nodeId se incluye aquí ya que nodeLabel puede ser el mismo para diferentes nodos de recorrido.

```sql
select
    _experience.journeyOrchestration.stepEvents.nodeID AS nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName AS nodeLabel,
    count(1) stepEnteredCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = TRUE
     AND _experience.journeyOrchestration.stepEvents.eventID IS DISTINCT FROM 'createInstance'
group by
    _experience.journeyOrchestration.stepEvents.nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName; 
```

## Conjunto de datos de evento de offer decisioning{#ode-decisionevents}

_Nombre en la interfaz: Eventos de decisión de ODE (conjunto de datos del sistema)_

Conjunto de datos para la ingesta de propuestas de oferta a los usuarios.

El esquema relacionado es ODE decisionEvents.

Esta consulta muestra todas las ofertas devueltas el día anterior:

```sql
SELECT date_format(Decision.Timestamp, 'MM/dd/yyyy') as Date
,HOUR(Decision.timestamp) as Hour
,COUNT(*)  as Count
FROM ode_decisionevents_b699fa78_efec_41b1_99fa_78efecc1b1ef_decision AS Decision
WHERE date_format(Decision.timestamp, 'MM/dd/yyyy') = date_format(CURRENT_DATE, 'MM/dd/yyyy') and Decision._experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:13ab41890a335ad6'
GROUP BY date_format(Decision.Timestamp, 'MM/dd/yyyy')
,HOUR(Decision.timestamp)
ORDER BY 1, 2 DESC;
```

Esta consulta muestra el número de veces que se propusieron ofertas durante los últimos 30 días de una actividad/decisión en particular y su prioridad de oferta asociada.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

## Conjunto de datos del servicio de consentimiento{#consent-service-dataset}

_Nombre en la interfaz: Conjunto de datos del servicio de consentimiento CJM (conjunto de datos del sistema)_

Conjunto de datos para el servicio de consentimiento de Journey Optimizer.

El esquema relacionado es CJM Consent Service Schema.

Consulte la lista de ID de correo electrónico que han consentido en recibir correo electrónico:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Consulta para devolver el valor de consentimiento de un ID de correo electrónico en el que el ID de correo electrónico sería la entrada:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```

## Conjunto de datos de evento de comentarios de BCC{#bcc-feedback-event-dataset}

_Nombre en la interfaz: Conjunto de datos del evento de comentarios de AJO BCC (conjunto de datos del sistema)_

Conjunto de datos para almacenar información para mensajes CCO.

Consulte todos los mensajes CCO en un plazo de 2 días (para una campaña en particular):

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

Consulte con el conjunto de datos de comentarios para mostrar a los usuarios que no recibieron (todas las devoluciones y supresiones) y que tienen una entrada CCO para un mensaje determinado:

```sql
SELECT 
    distinct bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS OriginalRecipientAddress 
FROM ajo_bcc_feedback_event_dataset  AS bcc 
WHERE 
    bcc.timestamp > now() - INTERVAL '2' DAY AND     bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND      bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress != '' AND
    ( 
            bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress NOT IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```
