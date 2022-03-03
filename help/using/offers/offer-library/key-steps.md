---
title: Pasos clave para crear una oferta
description: Descubra los pasos clave necesarios para crear una oferta
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 14ab70aa32f4f7978b8c72b3981d3b55f56fd08b
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 14%

---

# Pasos clave para crear y administrar ofertas {#key-steps-to-manage-offers}

A continuación se presentan los pasos principales para crear, configurar y administrar ofertas, así como para utilizarlas en una decisión.

![](../assets/offer-create-manage-process.png)

Para ver un ejemplo completo de extremo a extremo que muestre cómo configurar ofertas, utilícelas en una decisión y aproveche esta decisión en un mensaje de correo electrónico, consulte [esta página](../offers-e2e.md).

## Crear componentes {#create-components}

Before starting to create offers, you must define several components that you will use in your offers.

1. **Creación de ubicaciones**, que son contenedores que se utilizarán para mostrar sus ofertas. You can, for example, create a placement that will be dedicated to offers in the image format only, and situated to the top of your messages.

1. **Crear reglas de decisión** que especifica las condiciones en las que se presentan las ofertas.

1. **Create tags** that you will associate to the offers, allowing you to easily organize and search them into the library.

1. Si desea definir reglas que determinen qué oferta debe presentarse primero para una ubicación determinada (en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas), puede **crear una fórmula de clasificación**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">Crear ubicaciones</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">Crear reglas de decisión</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">Crear etiquetas</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../offer-library/create-ranking-formulas.md">Crear fórmulas de clasificación</a></p></td>
</table>

## Crear y administrar ofertas {#create-and-manage-offers}

1. **Crear ofertas** y configure su contenido y propiedades.

1. **Crear ofertas de reserva**, que son las ofertas de último recurso que se mostrarán si los clientes no cumplen los requisitos para cualquiera de las ofertas seleccionadas.

1. **Crear una colección** para incluir las ofertas personalizadas que ha creado y utilizarlas en una decisión.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">Cree ofertas</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">Crear ofertas de reserva</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">Crear colecciones</a></p></td></tr>
</table>

## Create and configure decisions {#create-and-configure-decisions}

1. **Crear una decisión** que combinará ubicaciones con ofertas personalizadas y ofertas de reserva. El motor de Offer decisioning utilizará esta combinación para encontrar la mejor oferta para un perfil específico.

1. **Configurar la decisión**. To do so, select the placements, and for each placement, select a collection and a fallback.

1. Si es necesario, puede **asignar una fórmula de clasificación** a una ubicación al configurar la decisión.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">Crear decisiones</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">Configure decisions</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assign ranking</a></p></td>
</tr>
</table>
