---
title: Elementos de decisión
description: Aprenda a trabajar con elementos de decisión
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: b1de82a4fdba58880e21b114ec3d2b9c3c81df0c
workflow-type: tm+mt
source-wordcount: '1778'
ht-degree: 14%

---

# Creación de su primer elemento de decisión {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="Administración de elementos de decisión"
>abstract="Journey Optimizer le permite crear ofertas de marketing, conocidas como elementos de decisión, que puede crear y organizar en un catálogo y colecciones centralizados. Actualmente, todos los elementos de decisión creados se consolidan dentro de un único catálogo &quot;Ofertas&quot;. Desde esta pantalla, también puede acceder al esquema del catálogo mediante el botón **Editar esquema** y crear atributos personalizados para los elementos de decisión."

Journey Optimizer le permite crear ofertas de marketing, conocidas como elementos de decisión, que puede crear y organizar en un catálogo y colecciones centralizados. Están formadas por atributos estándar y personalizados diseñados para ajustarse con precisión a sus necesidades. Además, incorporan restricciones de perfil que le permiten definir a quién se puede mostrar un elemento de decisión.

Antes de crear un elemento de decisión, asegúrese de haber creado una **regla de decisión** si desea establecer condiciones para determinar a quién se puede mostrar el elemento de decisión. [Aprenda a crear reglas de decisión](rules.md).

Para crear un elemento de decisión, vaya a **[!UICONTROL Decisioning]** > **[!UICONTROL Catálogos]**, haga clic en **[!UICONTROL Crear elemento]** y siga los pasos detallados en las secciones siguientes.

## Definición de los atributos del elemento de decisión {#attributes}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="Definición de la prioridad del elemento de decisión"
>abstract="Si un perfil cumple los requisitos para varios elementos, la prioridad permite comparar este elemento de decisión con otros. Una prioridad mayor otorga al elemento prioridad sobre otros."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="Definición de los atributos personalizados"
>abstract="Los atributos personalizados son atributos específicos adaptados a sus necesidades que puede asignar a un elemento de decisión. Se crean en el esquema de catálogo de los elementos de decisión. Esta sección solo se muestra si ha añadido al menos un atributo personalizado al esquema del catálogo."

Comience por definir los atributos estándar y personalizados del elemento de decisión:

![](assets/item-attributes.png)

1. Proporcione un nombre y una descripción.
1. Especifique las fechas de inicio y finalización. El motor de decisión solo considerará el elemento en estas fechas.
1. Establezca la **[!UICONTROL Prioridad]** del elemento de decisión en comparación con otros, si un perfil cumple los requisitos para varios elementos. Una prioridad mayor otorga al elemento prioridad sobre otros.

   >[!NOTE]
   >
   >La prioridad es un tipo de datos entero. Todos los atributos que son tipos de datos enteros deben contener valores enteros (sin decimales).

1. El campo **Etiquetas** le permite asignar etiquetas unificadas de Adobe Experience Platform a los elementos de decisión. Esto le permite clasificarlos fácilmente y mejorar la búsqueda. [Descubra cómo trabajar con campañas](../start/search-filter-categorize.md#tags)

1. Especifique atributos personalizados (opcional). Los atributos personalizados son atributos específicos adaptados a sus necesidades que puede asignar a un elemento de decisión. Se definen en el esquema de catálogo de los elementos de decisión. [Aprenda a trabajar con catálogos](catalogs.md)

1. Una vez definidos los atributos del elemento de decisión, haga clic en **[!UICONTROL Siguiente]**.

## Configuración de la idoneidad del elemento de decisión {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="Añadir públicos o reglas de decisión"
>abstract="De forma predeterminada, todos los perfiles podrán recibir el elemento de decisión, pero puede utilizar públicos o reglas para reservar el elemento únicamente a perfiles específicos."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences" text="Uso de públicos"
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/decisioning/experience-decisioning/rules" text="Uso de reglas de decisión"

De forma predeterminada, todos los perfiles pueden recibir el elemento de decisión, pero puede utilizar audiencias o reglas para restringir el elemento solo a perfiles específicos, ambas soluciones correspondientes a usos diferentes. Expanda la sección siguiente para obtener más información:

+++Uso de audiencias frente a reglas de decisión

Básicamente, el resultado de una audiencia es una lista de perfiles, mientras que una regla de decisión es una función ejecutada a petición en un único perfil durante el proceso de toma de decisiones.

* **Audiencias**: Por un lado, las audiencias son un grupo de perfiles de Adobe Experience Platform que coinciden con una determinada lógica en función de atributos de perfil y eventos de experiencia. Sin embargo, Administración de ofertas no vuelve a calcular la audiencia, que puede no estar actualizada al presentar la oferta.

* **Reglas de decisión**: Por otro lado, una regla de decisión se basa en los datos disponibles en Adobe Experience Platform y determina a quién se puede mostrar una oferta. Una vez seleccionada en una oferta o una decisión para una ubicación determinada, la regla se ejecuta cada vez que se toma una decisión, lo que garantiza que cada perfil obtenga la última y la mejor oferta.

+++

* Para limitar la presentación del elemento de decisión a los miembros de una o varias audiencias de Adobe Experience Platform, seleccione la opción **[!UICONTROL Visitantes que pertenecen a una o varias audiencias]**, luego agregue una o varias audiencias desde el panel izquierdo y combínelas con los operadores lógicos **[!UICONTROL And]** / **[!UICONTROL Or]**. [Más información sobre los públicos](../audience/about-audiences.md)

* Para asociar una regla de decisión específica al elemento de decisión, seleccione **[!UICONTROL By rule]** y, a continuación, arrastre la regla deseada desde el panel izquierdo al área central. [Más información sobre las reglas de decisión](rules.md)

![](assets/item-constraints.png)

Al seleccionar audiencias o reglas de decisión, puede ver información sobre los perfiles cualificados estimados. Haga clic en **[!UICONTROL Actualizar]** para actualizar los datos.

>[!NOTE]
>
>Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto. Por ejemplo, una regla de idoneidad que requiere que el clima actual sea de ≥80 grados.

## Establecer reglas de límite {#capping}

El límite se utiliza como restricción para definir el número máximo de veces que se puede presentar una oferta. Limitar el número de veces que los usuarios obtienen ofertas específicas le permite evitar saturar a sus clientes y, por lo tanto, optimizar cada punto de contacto con la mejor oferta. Puede crear hasta 10 límites para un elemento de decisión determinado.

![](assets/item-capping.png)

>[!NOTE]
>
>
>El valor del contador de límite puede tardar hasta 3 segundos en actualizarse. Por ejemplo, supongamos que muestra un banner web que muestra una oferta en el sitio web. Si un usuario determinado navega a la siguiente página del sitio web en menos de 3 segundos, el valor del contador no se incrementa para ese usuario.

Para establecer reglas de límite para el elemento de decisión, haga clic en el botón **[!UICONTROL Crear límite]** y siga estos pasos:

1. Defina qué **[!UICONTROL evento de límite]** se tendrá en cuenta para aumentar el contador.

   * **[!UICONTROL Evento de decisión]** (valor predeterminado): Número máximo de veces que se puede presentar una oferta.
   * **[!UICONTROL Impresión]** (solo canales entrantes): Número máximo de veces que la oferta se puede mostrar a un usuario.
   * **[!UICONTROL Clics]**: Número máximo de veces que un usuario puede hacer clic en el elemento de decisión.
   * **[!UICONTROL Evento personalizado]**: puede definir un evento personalizado que se utilizará para limitar el número de veces que se enviará el elemento. Por ejemplo, puede limitar el número de canjes hasta que sean iguales a 10 000 o hasta que un perfil determinado se haya canjeado 1 vez. Para ello, use [esquemas XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"} de Adobe Experience Platform para generar una regla de evento personalizada.

   >[!NOTE]
   >
   >Para todos los eventos de límite, excepto el evento de decisión, es posible que los comentarios de la administración de decisiones no se recopilen automáticamente, lo que podría provocar que el contador de límite no se incremente correctamente. Para asegurarse de que se rastrea y contabiliza cada evento de límite en el contador de límite, asegúrese de que el esquema utilizado para recopilar eventos de experiencia incluya el grupo de campos correcto para ese evento. Encontrará información detallada sobre la recopilación de datos en la documentación de gestión de decisiones de Journey Optimizer:
   >* [Recopilación de datos de administración de decisiones](data-collection/data-collection.md)
   >* [Configurar la recopilación de datos](data-collection/schema-requirement.md)

1. Elija el tipo de límite:

   * Seleccione **[!UICONTROL En total]** para definir cuántas veces se puede proponer el elemento en la audiencia de destino combinada, es decir, en todos los usuarios. Por ejemplo, si es un retailer de electrónica con una &quot;oferta de venta de televisores&quot;, quiere que la oferta solo se devuelva 200 veces en todos los perfiles.

   * Seleccione **[!UICONTROL Por perfil]** para definir cuántas veces se puede proponer la oferta al mismo usuario. Por ejemplo, si es un banco con una oferta de &quot;tarjeta de crédito Platinum&quot;, no desea que esta oferta se muestre más de 5 veces por perfil. De hecho, cree que si el usuario ha visto la oferta 5 veces y no ha actuado en consecuencia, tiene una mayor oportunidad de actuar en la siguiente mejor oferta.

1. En el campo **[!UICONTROL Límite de recuento de límite]**, especifique el número de veces que la oferta se puede presentar a todos los usuarios o por perfiles, según el tipo de límite seleccionado. El número debe ser un número entero mayor que 0.

   Por ejemplo, ha definido un evento de límite personalizado como, por ejemplo, el número de cierres de compra que se tiene en cuenta. Si introduce 10 en el campo **[!UICONTROL Límite de recuento de límite]**, no se enviarán más ofertas después de 10 cierres de compra.

1. En la lista desplegable **[!UICONTROL Restablecer frecuencia de límite]**, establezca la frecuencia con la que se restablece el contador de límite. Para ello, defina el periodo de tiempo para el recuento (diario, semanal o mensual) e introduzca el número de días/semanas/meses de su elección. Por ejemplo, si desea que el recuento límite se restablezca cada 2 semanas, seleccione **[!UICONTROL Semanalmente]** en la lista desplegable correspondiente y escriba **2** en el otro campo.

   * El restablecimiento del contador de límite de frecuencia se produce a las **12 a. m. UTC**, el día que haya definido o el primer día de la semana o del mes, según corresponda. El día de inicio de la semana es **domingo**. Cualquier duración que elija no puede exceder de **2 años** (es decir, el número correspondiente de meses, semanas o días).

   * Después de publicar el elemento de decisión, no podrá cambiar el período de tiempo (mensual, semanal o diario) seleccionado para la frecuencia. Puede seguir editando el límite de frecuencia si el elemento tiene el estado **[!UICONTROL Borrador]** y nunca antes se había publicado con el límite de frecuencia habilitado.

   * Puede haber un tiempo de búfer de hasta 15 minutos antes de que los eventos se contabilicen como restricciones de límite de frecuencia, ya sea cuando se aprueba el elemento de decisión o cuando se crea el límite, lo que ocurra en último lugar.

1. Haga clic en **[!UICONTROL Crear]** para confirmar la creación de la regla de límite. Puede crear hasta 10 reglas para un solo elemento de decisión. Para ello, haga clic en el botón **[!UICONTROL Crear límite]** y repita los pasos anteriores.

   ![](assets/item-capping-rules.png)

1. Una vez definidas las reglas de elegibilidad y límite del elemento de decisión, haga clic en **[!UICONTROL Siguiente]** para revisar y guardar el elemento.

1. El elemento de decisión aparece ahora en la lista, con el estado **[!UICONTROL Borrador]**. Cuando esté listo para ser presentado a los perfiles, haga clic en el botón de puntos suspensivos y seleccione **[!UICONTROL Aprobar]**.

   ![](assets/item-approve.png)

<!--* Identifying how many times a given customer has been shown a decision item. 
If a marketer wants to determine how many times a specific customer has been shown an offer, they can do that. Go to Profiles menu, Attributes tab. You'll see all counter values. The alphanumeric string is associated to the offer. To make the map, go to an item, in the URL check the last alphanumeric strings. D stands for day, w stands for week, m for month. "Ce" custom event-->

## Administración de elementos de decisión {#manage}

Desde la lista de elementos de decisión, puede editar un elemento de decisión, cambiar su estado (**Borrador**, **Aprobado**, **Archivado**), duplicarlo o eliminarlo.

Para modificar un elemento de decisión, ábralo, realice las modificaciones y guárdelo.

Al seleccionar un elemento de decisión o hacer clic en el botón de puntos suspensivos, se habilitan las acciones que se describen a continuación.

* **[!UICONTROL Aprobar]**: establece el estado del elemento de decisión en Aprobado.
* **[!UICONTROL Deshacer aprobación]**: vuelve a establecer el estado del elemento de decisión en **[!UICONTROL Borrador]**.
* **[!UICONTROL Duplicate]**: crea un elemento de decisión con atributos y restricciones idénticos. De manera predeterminada, el nuevo elemento tiene el estado **[!UICONTROL Borrador]**.
* **[!UICONTROL Eliminar]**: quita el elemento de decisión de la lista.

  >[!IMPORTANT]
  >
  >Una vez eliminado, el elemento de decisión y su contenido ya no son accesibles. Esta acción no se puede deshacer.

  Los elementos de oferta aprobados no se pueden eliminar si se utilizan en una colección o una decisión. Para eliminarlos, cambie su estado a Borrador. Para ello, haga clic en el botón de los tres puntos y seleccione **[!UICONTROL Deshacer aprobación]**.

  ![](assets/item-undo.png)

* **[!UICONTROL Archivo]**: Establece el estado del elemento de decisión en **[!UICONTROL Archivado]**. El elemento de decisión aún está disponible en la lista, pero no puedes volver a establecer su estado en **[!UICONTROL Borrador]** o **[!UICONTROL Aprobado]**. Solo puede duplicarlo o eliminarlo.
