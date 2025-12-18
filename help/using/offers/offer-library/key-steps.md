---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Pasos clave para crear una oferta
description: Descubra los pasos clave necesarios para crear una oferta
badge: label="Heredado" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 12%

---

# Pasos clave para crear y administrar ofertas {#key-steps-to-manage-offers}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)

A continuación se presentan los pasos principales para crear, configurar y administrar ofertas, así como para utilizarlas en una decisión.

![](../assets/offer-create-manage-process.png)

Para ver un ejemplo completo de extremo a extremo que muestra cómo configurar ofertas, utilícelas en una decisión y aproveche esta decisión en un mensaje de correo electrónico, consulte [esta página](../offers-e2e.md).

## Crear componentes {#create-components}

Antes de empezar a crear ofertas, debe definir varios componentes que utilizará en las ofertas.

1. [Cree ubicaciones](creating-placements.md), que son contenedores que se utilizarán para mostrar sus ofertas. Por ejemplo, puede crear una ubicación que esté dedicada únicamente a ofertas en formato de imagen y situada en la parte superior de los mensajes.

1. [Cree reglas de decisión](creating-decision-rules.md) que especifiquen las condiciones bajo las cuales se presentarán las ofertas.

1. [Cree calificadores de colección](creating-tags.md) (anteriormente conocidos como &quot;etiquetas&quot;) que asociará a las ofertas, lo que le permitirá organizarlas y buscarlas fácilmente en la biblioteca.

1. Si desea definir reglas que determinen qué oferta debe presentarse primero para una ubicación determinada (en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas), puede [crear una fórmula de clasificación](../ranking/create-ranking-formulas.md).

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Create placements</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Create decision rules</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Create collection qualifiers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Create ranking formulas</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Creación y administración de ofertas {#create-and-manage-offers}

1. [Crear ofertas](creating-personalized-offers.md) y configurar su contenido y propiedades.

1. [Crear ofertas de reserva](creating-fallback-offers.md), que son las ofertas de último recurso que se mostrarán si los clientes no cumplen los requisitos para ninguna de las ofertas seleccionadas.

1. [Cree una colección](creating-collections.md) para incluir las ofertas personalizadas que creó y usarlas en una decisión.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Create offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Create fallback offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Create collections</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Creación y configuración de decisiones {#create-and-configure-decisions}

1. [Cree una decisión](../offer-activities/create-offer-activities.md) que combine ubicaciones con las ofertas personalizadas y las ofertas de reserva. El motor de decisión utilizará esta combinación para encontrar la mejor oferta para un perfil específico.

1. [Configurar la decisión](../offer-activities/create-offer-activities.md#add-decision-scopes). Para ello, seleccione las ubicaciones y, para cada ubicación, seleccione una colección y una reserva.

1. Si es necesario, puede [asignar una fórmula de clasificación](../offer-activities/configure-offer-selection.md#assign-ranking-formula) o [clasificación de IA](../offer-activities/configure-offer-selection.md#use-ranking-strategy) a una ubicación al configurar la decisión.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Create decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configure decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assign ranking</a>
</div>
<p>
</td>
</tr>
</table>
-->