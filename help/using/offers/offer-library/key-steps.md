---
title: Pasos clave para crear una oferta
description: Descubra los pasos clave necesarios para crear una oferta
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 11%

---

# Pasos clave para crear y administrar ofertas {#key-steps-to-manage-offers}

A continuación se presentan los pasos principales para crear, configurar y administrar ofertas, así como para utilizarlas en una decisión.

![](../assets/offer-create-manage-process.png)

Para ver un ejemplo completo de extremo a extremo que muestra cómo configurar ofertas, utilizarlas en una decisión y aprovechar esta decisión en un correo electrónico, consulte [esta página](../offers-e2e.md).

## Creación de componentes {#create-components}

Antes de empezar a crear ofertas, debe definir varios componentes que utilizará en las ofertas.

1. **Crear ubicaciones**, que son contenedores que se utilizarán para mostrar sus ofertas. Por ejemplo, puede crear una ubicación que esté dedicada únicamente a ofertas en formato de imagen y situada en la parte superior de los mensajes.

1. **Creación de reglas de decisión** que especificará las condiciones en las que se presentarán las ofertas.

1. **Crear calificadores de colección** (anteriormente conocidas como &quot;etiquetas&quot;) que asociará a las ofertas, lo que le permite organizarlas fácilmente y buscarlas en la biblioteca.

1. Si desea definir reglas que determinen qué oferta debe presentarse primero para una ubicación determinada (en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas), puede **crear una fórmula de clasificación**.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Creación de ubicaciones</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Crear reglas de decisión</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Creación de etiquetas</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Creación de fórmulas de clasificación</a>
</div>
<p>
</td>
</tr>
</table>

## Creación y administración de ofertas {#create-and-manage-offers}

1. **Creación de ofertas** y configurar su contenido y propiedades.

1. **Crear ofertas de reserva**, que son las ofertas de último recurso que se muestran si los clientes no cumplen los requisitos para ninguna de las ofertas seleccionadas.

1. **Crear una colección** para incluir las ofertas personalizadas que creó y utilizarlas en una decisión.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Creación de ofertas</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Creación de ofertas de reserva</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Creación de colecciones</a>
</div>
<p>
</td>
</tr>
</table>

## Creación y configuración de decisiones {#create-and-configure-decisions}

1. **Crear una decisión** que combinará ubicaciones con las ofertas personalizadas y las ofertas de reserva. El motor de decisión utilizará esta combinación para encontrar la mejor oferta para un perfil específico.

1. **Configurar la decisión**. Para ello, seleccione las ubicaciones y, para cada ubicación, seleccione una colección y una reserva.

1. Si es necesario, puede **asignar una fórmula de clasificación** a una ubicación al configurar la decisión.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Crear decisiones</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configuración de decisiones</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Asignar clasificación</a>
</div>
<p>
</td>
</tr>
</table>
