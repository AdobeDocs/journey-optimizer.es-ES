---
solution: Journey Optimizer
product: journey optimizer
title: campos del recorrido
description: campos del recorrido
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 177b4a97-c757-40ca-a190-fbd88169e5e2
source-git-commit: 6961a07e2874f9beb76a9beaebb29997d114d8e7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 6%

---

# Campos del recorrido {#sharing-journey-fields}

Este grupo de campos se usa en el esquema **recorrido** (en relación con **journeyStepEvent**). Contiene los campos que se enumeran a continuación.


>[!NOTE]
>
>Obtenga más información acerca de los atributos de propiedades de recorrido [en esta sección](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## journeyID {#journeyid-field}

ID del recorrido principal.

Tipo: cadena

## journeyVersionID {#journeyversionid-field}

ID de la versión del recorrido. Este ID representa la identidad de un recorrido.

Tipo: cadena

## name {#name-field}

Nombre del recorrido.

Tipo: cadena

>[!NOTE]
>
>El nombre del recorrido se utiliza para vincular los datos de ejecución del recorrido con los conjuntos de datos de informes. Si cambia el nombre de un recorrido, asegúrese de que el nuevo nombre coincida con el nombre del conjunto de datos de informes para mantener un sistema de informes preciso. Una discrepancia puede hacer que los datos de los informes no aparezcan según lo esperado. Obtenga más información sobre [solución de problemas con datos de informes que faltan](../building-journeys/report-journey.md#troubleshooting-missing-data).

## descripción {#description-field}

Descripción del recorrido.

Tipo: cadena

## version {#version-field}

Versión, representada como `major`.`minor`

Tipo: cadena
