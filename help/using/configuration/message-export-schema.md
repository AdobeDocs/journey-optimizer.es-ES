---
solution: Journey Optimizer
product: journey optimizer
title: Esquema de exportación de mensajes de AJO
description: Obtenga información sobre los campos disponibles en el conjunto de datos de exportación de mensajes de AJO
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: exportación, mensajes, conjunto de datos, esquema, correos electrónicos, SMS
source-git-commit: cc84ad59f4233967c484c99651edb0558518c58c
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 3%

---

# Esquema de exportación de mensajes de AJO {#ajo-message-export-schema}

Cuando **Message Export** está habilitado en una configuración de canal de correo electrónico o SMS, el contenido de los mensajes enviados se escribe en el **conjunto de datos de exportación de mensajes de AJO** en [!DNL Adobe Experience Platform].

Esta sección enumera los campos disponibles en el conjunto de datos exportado.

## Campos del conjunto de datos

+++ _experience

**Campo:** `_experience`\
**Tipo:** objeto

+++

+++ _experience > customerJourneyManagement

**Campo:** `customerJourneyManagement`\
**Tipo:** objeto

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata

**Campo:** `messageDeliveryMetadata`\
**Tipo:** objeto

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > emailMetadata

**Campo:** `emailMetadata`\
**Tipo:** objeto

* destinatario

  **Campo:** `recipient`\
  **Tipo:** objeto

   * cco

     **Campo:** `bcc`\
     **Tipo:** matriz de cadenas

   * cc

     **Campo:** `cc`\
     **Tipo:** matriz de cadenas

   * correo electrónico

     **Campo:** `email`\
     **Tipo:** cadena

   * name

     **Campo:** `name`\
     **Tipo:** cadena

* remitente

  **Campo:** `sender`\
  **Tipo:** objeto

   * correo electrónico

     **Campo:** `email`\
     **Tipo:** cadena

   * errorEmail

     **Campo:** `errorEmail`\
     **Tipo:** cadena

   * name

     **Campo:** `name`\
     **Tipo:** cadena

   * replyToEmail

     **Campo:** `replyToEmail`\
     **Tipo:** cadena

   * replyToName

     **Campo:** `replyToName`\
     **Tipo:** cadena

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > smsMetadata

**Campo:** `smsMetadata`\
**Tipo:** objeto

* destinatario

  **Campo:** `recipient`\
  **Tipo:** objeto

   * número

     **Campo:** `number`\
     **Tipo:** cadena

* remitente

  **Campo:** `sender`\
  **Tipo:** objeto

   * números

     **Campo:** `numbers`\
     **Tipo:** matriz de cadenas

+++

+++ _experience > customerJourneyManagement > messageExecution

**Campo:** `messageExecution`\
**Tipo:** objeto

* público

  **Campo:** `audience`\
  **Tipo:** objeto

   * id

     **Campo:** `id`\
     **Tipo:** cadena

   * tipo

     **Campo:** `type`\
     **Tipo:** cadena

* fragmentPublicationIDs

  **Campo:** `fragmentPublicationIDs`\
  **Tipo:** matriz de cadenas

* metadatos

  **Campo:** `metadata`\
  **Tipo:** mapa

   * [Clave de mapa]

     **Tipo:** cadena

* parentSourceMeta

  **Campo:** `parentSourceMeta`\
  **Tipo:** objeto

   * sourceActionID

     **Campo:** `sourceActionID`\
     **Tipo:** cadena

   * sourceID

     **Campo:** `sourceID`\
     **Tipo:** cadena

   * sourceType

     **Campo:** `sourceType`\
     **Tipo:** cadena

   * sourceVersionID

     **Campo:** `sourceVersionID`\
     **Tipo:** cadena

* batchInstanceID

  **Campo:** `batchInstanceID`\
  **Tipo:** cadena

* campaignActionID

  **Campo:** `campaignActionID`\
  **Tipo:** cadena

* campaignID

  **Campo:** `campaignID`\
  **Tipo:** cadena

* campaignVersionID

  **Campo:** `campaignVersionID`\
  **Tipo:** cadena

* journeyActionID

  **Campo:** `journeyActionID`\
  **Tipo:** cadena

* journeyVersionID

  **Campo:** `journeyVersionID`\
  **Tipo:** cadena

* journeyVersionInstanceID

  **Campo:** `journeyVersionInstanceID`\
  **Tipo:** cadena

* journeyVersionNodeID

  **Campo:** `journeyVersionNodeID`\
  **Tipo:** cadena

* messageExecutionID

  **Campo:** `messageExecutionID`\
  **Tipo:** cadena

* messageID

  **Campo:** `messageID`\
  **Tipo:** cadena

* messagePublicationID

  **Campo:** `messagePublicationID`\
  **Tipo:** cadena

* messageType

  **Campo:** `messageType`\
  **Tipo:** cadena

* waveID

  **Campo:** `waveID`\
  **Tipo:** cadena

+++

+++ _experience > customerJourneyManagement > messageProfile

**Campo:** `messageProfile`\
**Tipo:** objeto

* canal

  **Campo:** `channel`\
  **Tipo:** objeto

   * contentTypes

     **Campo:** `contentTypes`\
     **Tipo:** matriz de cadenas

   * locationTypes

     **Campo:** `locationTypes`\
     **Tipo:** matriz de cadenas

   * metricTypes

     **Campo:** `metricTypes`\
     **Tipo:** matriz de cadenas

   * _id

     **Campo:** `_id`\
     **Tipo:** cadena

   * _type

     **Campo:** `_type`\
     **Tipo:** cadena

   * mediaAction

     **Campo:** `mediaAction`\
     **Tipo:** cadena

   * mediaType

     **Campo:** `mediaType`\
     **Tipo:** cadena

   * modo

     **Campo:** `mode`\
     **Tipo:** cadena

   * referenceSource

     **Campo:** `referringSource`\
     **Tipo:** cadena

   * typeAtSource

     **Campo:** `typeAtSource`\
     **Tipo:** cadena

* isSendTimeOptimized

  **Campo:** `isSendTimeOptimized`\
  **Tipo:** booleano

* isTestExecution

  **Campo:** `isTestExecution`\
  **Tipo:** booleano

* messageProfileID

  **Campo:** `messageProfileID`\
  **Tipo:** cadena

* messageProfileTrackingID

  **Campo:** `messageProfileTrackingID`\
  **Tipo:** cadena

* requestID

  **Campo:** `requestID`\
  **Tipo:** cadena

* secondaryDimensionID

  **Campo:** `secondaryDimensionID`\
  **Tipo:** cadena

* secondaryDimensionName

  **Campo:** `secondaryDimensionName`\
  **Tipo:** cadena

* variante

  **Campo:** `variant`\
  **Tipo:** cadena

+++

+++ _experience > customerJourneyManagement > messageRenderedContent

**Campo:** `messageRenderedContent`\
**Tipo:** objeto

* emailContent

  **Campo:** `emailContent`\
  **Tipo:** objeto

   * html

     **Campo:** `html`\
     **Tipo:** cadena

   * sujeto

     **Campo:** `subject`\
     **Tipo:** cadena

   * texto

     **Campo:** `text`\
     **Tipo:** cadena

* smsContent

  **Campo:** `smsContent`\
  **Tipo:** objeto

   * medios

     **Campo:** `media`\
     **Tipo:** cadena

   * message

     **Campo:** `message`\
     **Tipo:** cadena

   * título

     **Campo:** `title`\
     **Tipo:** cadena

+++

+++ identityMap

**Campo:** `identityMap`\
**Tipo:** mapa

* [Clave de mapa]

  **Tipo:** matriz de objetos

   * authenticatedState

     **Campo:** `authenticatedState`\
     **Tipo:** cadena

   * id

     **Campo:** `id`\
     **Tipo:** cadena

   * principal

     **Campo:** `primary`\
     **Tipo:** booleano

+++

+++ eventType

**Campo:** `eventType`\
**Tipo:** cadena

+++

+++ productionBy

**Campo:** `producedBy`\
**Tipo:** cadena

+++

+++ timestamp

**Campo:** `timestamp`\
**Tipo:** dateTime

+++

