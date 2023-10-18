---
title: Elementos de decisión
description: Aprenda a trabajar con elementos de decisión
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 7%

---

# Elementos de decisión {#items}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción a Experience Decisioning](gs-experience-decisioning.md)
* Administración de los elementos de decisión
   * [Configuración del catálogo de elementos](catalogs.md)
   * **[Creación de elementos de decisión](items.md)**
   * [Administración de colecciones de elementos](collections.md)
* Configuración de la selección de elementos
   * [Crear reglas de decisión](rules.md)
   * [Creación de métodos de clasificación](ranking.md)
* [Creación de estrategias de selección](selection-strategies.md)
* [Creación de políticas de decisión](create-decision.md)

>[!ENDSHADEBOX]

Journey Optimizer le permite crear ofertas de marketing, conocidas como elementos de decisión, que puede crear y organizar en un catálogo y colecciones centralizados. Están formadas por atributos estándar y personalizados diseñados para ajustarse con precisión a sus necesidades. Además, incorporan restricciones de perfil que le permiten definir a quién se puede mostrar un elemento de decisión.

Antes de crear un elemento de decisión, asegúrese de haber creado un **regla de decisión** si desea establecer condiciones para determinar a quién se puede mostrar el elemento de decisión. [Obtenga información sobre cómo crear reglas de decisión](rules.md).

## Creación de su primer elemento de decisión

Para crear un elemento de decisión, siga estos pasos:

1. Vaya a **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Elementos]**.

1. Defina los atributos estándar del elemento de decisión:

   1. Proporcione un nombre y una descripción.
   1. Especifique las fechas de inicio y finalización. El motor de decisión solo considerará el elemento en estas fechas.
   1. Configure las variables **[!UICONTROL Prioridad]** del elemento de decisión en comparación con otros, si un perfil cumple los requisitos para varios elementos. Una prioridad mayor otorga al elemento prioridad sobre otros.

   ![](assets/item-attributes.png)

1. Los atributos personalizados son atributos específicos adaptados a sus necesidades que puede asignar a un elemento de decisión. Se definen en el esquema de catálogo de los elementos de decisión. [Aprenda a trabajar con catálogos](catalogs.md)

1. Una vez definidos los atributos del elemento de decisión, haga clic en **[!UICONTROL Siguiente]** para definir restricciones de perfil para el artículo.

   De forma predeterminada, todos los perfiles pueden recibir el elemento de decisión, pero puede utilizar audiencias o reglas para restringir el elemento solo a perfiles específicos, ambas soluciones correspondientes a usos diferentes. Expanda la sección siguiente para obtener más información:

   +++Uso de audiencias frente a reglas de decisión

   Básicamente, el resultado de una audiencia es una lista de perfiles, mientras que una regla de decisión es una función ejecutada a petición en un único perfil durante el proceso de toma de decisiones.

   * **Audiencias**: Por un lado, las audiencias son un grupo de perfiles de Adobe Experience Platform que coinciden con una lógica determinada en función de atributos de perfil y eventos de experiencia. Sin embargo, Administración de ofertas no vuelve a calcular la audiencia, que puede no estar actualizada al presentar la oferta.

   * **Reglas de decisión**: Por otro lado, una regla de decisión se basa en los datos disponibles en Adobe Experience Platform y determina a quién se puede mostrar una oferta. Una vez seleccionada en una oferta o una decisión para una ubicación determinada, la regla se ejecuta cada vez que se toma una decisión, lo que garantiza que cada perfil obtenga la última y la mejor oferta.

+++

   ![](assets/item-constraints.png)

   * Para limitar la presentación del elemento de decisión a los miembros de una o varias audiencias de Adobe Experience Platform, seleccione la **[!UICONTROL Visitantes de una o varias audiencias]** y, a continuación, añada una o varias audiencias desde el panel izquierdo y combínelas con la opción **[!UICONTROL Y]** / **[!UICONTROL O]** operadores lógicos. [Más información sobre las audiencias](../audience/about-audiences.md).

   * Para asociar una regla de decisión específica al elemento de decisión, seleccione **[!UICONTROL Por regla]** A continuación, arrastre la regla deseada desde el panel izquierdo al área central. [Más información sobre las reglas de decisión](rules.md).

   Al seleccionar públicos o reglas de decisión, puede ver información sobre los perfiles cualificados estimados. Clic **[!UICONTROL Actualizar]** para actualizar los datos.

   >[!NOTE]
   >
   >Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto. Por ejemplo, una regla de idoneidad que requiere que el clima actual sea de ≥80 grados.

1. Una vez definidas las restricciones del elemento de decisión, haga clic en **[!UICONTROL Siguiente]** para revisar y guardar el elemento.

1. El elemento de decisión ahora aparece en la lista, con el **[!UICONTROL Borrador]** estado. Cuando esté listo para presentarse a los perfiles, haga clic en el botón de puntos suspensivos y seleccione **[!UICONTROL Aprobar]**.

   ![](assets/item-approve.png)

## Administrar elementos de decisión

Desde la lista de elementos de decisión, puede editar un elemento de decisión y cambiar su estado (**Borrador**, **Aprobado**, **Archivado**), duplíquelo o elimínelo.

Para modificar un elemento de decisión, ábralo, realice las modificaciones y guárdelo.

Al seleccionar un elemento de decisión o hacer clic en el botón de puntos suspensivos, se habilitan las acciones que se describen a continuación.

* **[!UICONTROL Aprobar]**: establece el estado del elemento de decisión en Aprobado.
* **[!UICONTROL Deshacer aprobación]**: restablece el estado del elemento de decisión a **[!UICONTROL Borrador]**.
* **[!UICONTROL Duplicar]**: crea un elemento de decisión con atributos y restricciones idénticos. De forma predeterminada, el nuevo elemento tiene la variable **[!UICONTROL Borrador]** estado.
* **[!UICONTROL Eliminar]**: elimina el elemento de decisión de la lista.

  >[!IMPORTANT]
  >
  >Una vez eliminado, el elemento de decisión y su contenido ya no son accesibles. No se puede deshacer esta acción. Si el elemento de decisión se utiliza en una colección o una decisión, no se puede eliminar. Primero debe quitar el elemento de decisión de los objetos.

* **[!UICONTROL Archivar]**: establece el estado del elemento de decisión en **[!UICONTROL Archivado]**. El elemento de decisión aún está disponible en la lista, pero no puede volver a establecer su estado en **[!UICONTROL Borrador]** o **[!UICONTROL Aprobado]**. Solo puede duplicarlo o eliminarlo.
