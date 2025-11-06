---
title: Aprovechamiento de los públicos de carga personalizados para la toma de decisiones
description: Obtenga información sobre cómo aprovechar las audiencias de carga personalizadas para la toma de decisiones.
badge: label="Heredado" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: bd950410-691b-49d8-8851-8c6c448c00fd
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 2%

---

# Aprovechamiento de los públicos de carga personalizados para la toma de decisiones {#custom-upload-decisioning}

Con Journey Optimizer, puede aprovechar los datos de audiencias creadas mediante carga personalizada (archivo CSV) en Adobe Experience Platform para admitir los flujos de trabajo de Administración de decisiones. Esto resulta especialmente útil cuando los datos no se necesitan en el perfil, pero siguen siendo esenciales para la toma de decisiones.

Los datos de las audiencias de carga personalizadas se pueden aprovechar en Administración de decisiones para lo siguiente:

1. Criterios de idoneidad en ofertas y decisiones.
2. Personalización del contenido en representaciones de oferta.

Para obtener más información sobre las audiencias de carga personalizada, consulte las secciones:

* [Introducción a audiencias y Journey Optimizer](../audience/about-audiences.md)
* [Importación de una audiencia en Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}

## Lectura obligatoria {#must-read}

* Esta funcionalidad solo es compatible con **Administración de decisiones**, no con Decisioning (anteriormente conocido como &quot;Experience Decisioning&quot;).
* Está disponible exclusivamente a través de **solicitudes de API de decisiones (Hub)** y no es compatible con **API de decisiones de Edge** o **toma de decisiones por lotes**.

## Usar una audiencia de carga personalizada como criterio de idoneidad {#eligibilty}

Puede utilizar una audiencia de carga personalizada como criterio de idoneidad tanto en el nivel de oferta como en el de decisión. Una vez añadidos, estos criterios pueden excluir de la idoneidad las ofertas o colecciones de ofertas. Estas son las distintas ubicaciones en las que puede aprovechar las audiencias de carga personalizada para restringir la elegibilidad de las ofertas y decisiones:

* Cree una regla de decisión con una audiencia de carga personalizada:

   1. Al crear una regla, accede a la pestaña **Audiencias** y busca tu audiencia CSV en la lista. Arrastre y suelte la audiencia en el lienzo de reglas.
   1. Utilice la ficha **Atributos** y navegue hasta los esquemas de enriquecimiento vinculados a la audiencia seleccionada para acceder a todos los datos del archivo CSV y utilizarlos en la regla. Esto le permite utilizar un campo del archivo CSV para restringir la regla. [Aprenda a crear una regla de decisión](../offers/offer-library/creating-decision-rules.md)
   1. Guarde la regla. Una vez creada la regla, se puede utilizar en los niveles de oferta y decisión para restringir su idoneidad.

  ![](assets/csv-rule.png)

* Utilice las audiencias de carga personalizadas como restricción de la oferta. [Aprenda a agregar restricciones a una oferta](../offers/offer-library/add-constraints.md)

  Al crear una oferta, en el paso **Agregar restricciones** puede:

   * Utilice la audiencia de carga personalizada para definir la idoneidad de la oferta,
   * Aplique una regla que aproveche la audiencia de carga personalizada.

  ![](assets/csv-offer.png)

* Usar audiencias de carga personalizadas en el nivel de decisión.

  Al configurar una decisión, en el paso **Agregar ámbito de decisión**, puede usar Audiencias de carga personalizadas como criterio de evaluación para una colección de ofertas. [Obtenga información sobre cómo definir el ámbito de decisión](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

  ![](assets/csv-decision.png)

## Utilice una audiencia de carga personalizada para personalizar las representaciones de las ofertas

Las audiencias de carga personalizadas también se pueden utilizar para personalizar el contenido de las representaciones de ofertas haciendo referencia a los datos del archivo CSV. [Aprenda a agregar representaciones a una oferta](../offers/offer-library/add-representations.md)

Para poder aprovechar los atributos de una audiencia de carga personalizada para la personalización, primero debe agregar la audiencia personalizada como restricción. Para ello, durante la creación de una oferta, en el paso **Añadir restricciones**, añada la audiencia como restricciones o seleccione una regla que aproveche la audiencia de carga personalizada.

![](assets/csv-offer.png)

Una vez añadida la audiencia como restricción, se pueden utilizar sus atributos para personalizar el contenido de representación. Para ello, acceda a la pestaña **Atributos de perfil** y busque la audiencia de carga personalizada. Seleccione los atributos relevantes de la audiencia para personalizar el contenido de la oferta.

![](assets/csv-perso.png)
