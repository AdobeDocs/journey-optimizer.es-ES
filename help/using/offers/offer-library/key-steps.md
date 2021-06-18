---
title: Pasos clave para crear una oferta
description: Descubra los pasos clave necesarios para crear una oferta.
feature: Ofertas
topic: Integraciones
role: User
level: Intermediate
source-git-commit: 5631a1937b854c3e14d1816df9e8d30690588303
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 12%

---

# Pasos clave para crear y administrar ofertas {#key-steps}

A continuación se presentan los pasos principales para crear, configurar y administrar ofertas, así como para utilizarlas en una decisión.

![](../../assets/offer-create-manage-process.png)

Para ver un ejemplo completo de extremo a extremo que muestra cómo configurar ofertas, utilícelas en una decisión y aproveche esta decisión en un mensaje de correo electrónico, consulte [esta página](../offers-e2e.md).

## Crear componentes

Antes de comenzar a crear ofertas, debe definir varios componentes que utilizará en las ofertas.

1. **Cree ubicaciones**, que son contenedores que se utilizarán para mostrar las ofertas. Por ejemplo, puede crear una ubicación que se dedique solo a ofertas en formato de imagen y se sitúe en la parte superior de los mensajes.

1. **Cree** reglas de decisión que especifiquen las condiciones en las que se presentarán las ofertas.

1. **Cree** etiquetas que asocie a las ofertas, lo que le permite organizarlas y buscarlas fácilmente en la biblioteca.

1. Si desea definir reglas que determinen qué oferta debe presentarse primero para una ubicación determinada (en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas), puede **crear una fórmula de clasificación**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">Crear ubicaciones</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">Crear reglas de decisión</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">Crear etiquetas</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../offer-library/create-ranking-formulas.md">Creación de fórmulas de clasificación</a></p></td>
</table>

## Crear y administrar ofertas

1. **Cree ofertas** y configure su contenido y propiedades.

1. **Cree ofertas de reserva**, que son las últimas ofertas de recurso que se mostrarán si los clientes no cumplen los requisitos para ninguna de las ofertas seleccionadas.

1. **Cree una** colección para incluir las ofertas personalizadas que ha creado y utilizarlas en una decisión.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">Cree ofertas</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">Crear ofertas de reserva</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">Crear colecciones</a></p></td></tr>
</table>

## Crear y configurar decisiones

1. **Cree una** decisión que combine ubicaciones con las ofertas personalizadas y las ofertas de reserva. El motor de Offer decisioning utilizará esta combinación para encontrar la mejor oferta para un perfil específico.

1. **Configure la decisión**. Para ello, seleccione las ubicaciones y, para cada ubicación, seleccione una colección y una alternativa.

1. Si es necesario, puede **asignar una fórmula de clasificación** a una ubicación al configurar la decisión.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">Crear decisiones</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">Configuración de decisiones</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Asignar clasificación</a></p></td>
</tr>
</table>
