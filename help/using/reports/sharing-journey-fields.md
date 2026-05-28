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
TQID: https://experienceleague.adobe.com/dpQ6PEm-afX4PZuWSPrpAWDH7yBhUKZHZRF134VehAg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 130
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
