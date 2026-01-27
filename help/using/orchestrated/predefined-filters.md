---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con filtros predefinidos
description: Obtenga información sobre cómo guardar, aplicar y administrar filtros predefinidos en campañas organizadas
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 11%

---


# Trabajo con filtros predefinidos {#predefined-filters}

Los filtros predefinidos son reglas guardadas que se pueden reutilizar en el generador de reglas. Utilícelos para evitar reconstruir consultas comunes y estandarizar la lógica de segmentación en todas las campañas orquestadas.

Puede marcar filtros predefinidos como favoritos, compartirlos con otros usuarios y agregar parámetros para que los campos seleccionados se puedan editar cuando se aplique el filtro.

## Creación de un filtro predefinido {#create}

Guarde un filtro personalizado del generador de reglas para que esté disponible para uso futuro. Siga estos pasos:

1. Abra el generador de reglas y defina las condiciones de filtrado. [Descubra cómo generar una regla](../orchestrated/build-query.md)

1. Opcional: para que ciertos campos se puedan editar al usar el filtro, seleccione el campo y active **[!UICONTROL Establecer como parámetro]**. Al aplicar el filtro, solo se pueden editar estos campos.

   ![](assets/predefined-filter-parameter-enable.png)

1. Para guardar el filtro, haga clic en **[!UICONTROL Seleccionar o guardar filtro]** y seleccione **[!UICONTROL Guardar como filtro]**.

   ![](assets/predefined-filter-save.png)

1. Escriba una etiqueta y una descripción para el filtro, luego haga clic en **[!UICONTROL Guardar]**.

   * Para guardar el filtro como favorito, active la opción **[!UICONTROL Filtro favorito]**. Obtenga más información en [esta sección](#fav-filter).
   * Para que otros usuarios tengan acceso al filtro, habilite la opción **[!UICONTROL Filtro compartido]**. Obtenga más información en [esta sección](#share-filter).

   ![](assets/predefined-filter-save-name.png)

El filtro personalizado está ahora disponible en la lista **Filtros predefinidos**.

## Uso de un filtro predefinido en una regla {#apply}

Los filtros predefinidos están disponibles al definir consultas en el generador de reglas.

1. En el panel **[!UICONTROL Propiedades de regla]**, haga clic en **[!UICONTROL Seleccionar o guardar filtro]**.

1. Elija **[!UICONTROL Seleccionar filtro predefinido]** y seleccione un filtro. También puede seleccionar directamente un filtro predefinido de la lista si se ha añadido a Favoritos.

   ![](assets/predefined-filter-apply.png)

   >[!IMPORTANT]
   >
   >Al seleccionar un filtro predefinido, se sustituye la regla que se ha creado en el lienzo por el filtro seleccionado.

1. El filtro se abre en el lienzo. Continúe editando la condición según sea necesario.

   ![](assets/predefined-filter-added.png)

   Si el filtro seleccionado incluye parámetros, solo se pueden editar los campos marcados como parámetros. Aparecen en el panel situado junto al panel **[!UICONTROL Propiedades de regla]**.

   ![](assets/predefined-filter-parameter-apply.png)

   Para editar el filtro predefinido, haga clic en el botón ![elipsis button](assets/do-not-localize/rule-builder-icon-more.svg) y seleccione **[!UICONTROL Cambiar a la edición de regla]**. Todos los cambios se aplican únicamente a la regla actual que está creando. El filtro predefinido no se modifica.

   ![](assets/predefined-filter-parameter-edit.png)

## Guardar un filtro como favorito {#fav-filter}

Al crear un filtro predefinido, habilite la opción **[!UICONTROL Filtro favorito]** para ver este filtro predefinido en sus favoritos.

Cuando un filtro se guarda como favorito, aparece en la sección **[!UICONTROL Filtros favoritos]** de la lista de filtros, como se muestra a continuación:

![Sección de filtros favoritos](assets/predefined-filter-favorites.png)

## Uso compartido de un filtro predefinido {#share-filter}

De forma predeterminada, los filtros predefinidos que cree serán privados y solo podrán verlos los suyos. Para que otros operadores de su organización puedan acceder a un filtro, habilite la opción **[!UICONTROL Filtro compartido]**.

![Opción de filtro compartido](assets/predefined-filter-shared.png)

Los filtros compartidos aparecen en la lista de filtros predefinidos para todos los usuarios, lo que les permite utilizar estos filtros en sus propias reglas.

## Administración de filtros predefinidos {#manage-predefined-filter}

Para editar o eliminar filtros predefinidos, siga estos pasos:

1. Abra la lista de filtros predefinidos con el botón **[!UICONTROL Seleccionar o guardar filtro]** de la generación de reglas.

1. Seleccione el botón de ![puntos suspensivos](assets/do-not-localize/rule-builder-icon-more.svg) junto a un filtro y elija la acción que desee.

![](assets/predefined-filters-edit.png)
