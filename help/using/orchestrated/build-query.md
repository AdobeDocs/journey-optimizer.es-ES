---
solution: Journey Optimizer
product: journey optimizer
title: Cree su primera regla
description: Aprenda a crear reglas para sus campañas organizadas
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 5e956a6a-0b89-4d78-8f16-fe9fceb25674
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '1834'
ht-degree: 95%

---

# Cree su primera regla {#build-query}

+++ Índice

| Bienvenido a campañas orquestadas | Inicie su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Creación y programación de las campañas](create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabajo con el generador de reglas](orchestrated-rule-builder.md)<br/><br/><b>[Creación de su primera consulta](build-query.md)</b><br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/>[Resegmentación](retarget.md) | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Los pasos principales para crear reglas para las campañas orquestadas son los siguientes:

1. **Añadir condiciones**: cree condiciones personalizadas para filtrar su consulta al generar su propia condición con atributos de la base de datos y expresiones avanzadas.
1. **Combinar condiciones**: organice las condiciones en el lienzo mediante grupos y operadores lógicos.
1. **Comprobar y validar la regla**: compruebe los datos resultantes de la regla antes de guardarla.

## Añada una condición  {#conditions}

Para añadir condiciones en la consulta, siga estos pasos:

1. Acceda al generador de reglas desde la actividad **[!UICONTROL Generar público]**.

1. Haga clic en el botón **Añadir condición** para crear una primera condición para la consulta.

   También puede iniciar la consulta utilizando un filtro predefinido. Para ello, haga clic en el botón **[!UICONTROL Seleccionar o guardar filtro]** y elija **[!UICONTROL Seleccionar filtro predefinido]**.

   ![imagen que muestra el generador de reglas](assets/rule-builder-add.png)

1. Identifique el atributo de la base de datos que se utilizará como criterio para la condición. El icono “i” junto a un atributo proporciona información sobre la tabla donde se almacena y su tipo de datos.

   ![imagen que muestra la selección de un atributo](assets/rule-builder-select-attribute.png)

   >[!NOTE]
   >
   >El botón **Editar expresión** le permite utilizar el editor de expresiones para definir manualmente una expresión con campos de la base de datos y funciones de ayuda. [Más información sobre cómo editar expresiones](../orchestrated/edit-expressions.md)

1. Haga clic en la imagen ![que muestra el botón Más acciones](assets/do-not-localize/rule-builder-icon-more.svg) situado junto a un atributo para acceder a estas opciones adicionales:

+++ Distribución de valores

   Analice la distribución de los valores de un atributo determinado dentro de la tabla. Esta función es útil para comprender los valores disponibles, sus recuentos y sus porcentajes. También ayuda a evitar problemas como la incoherencia en las mayúsculas o en la ortografía al crear consultas o expresiones.

   En el caso de los atributos con un gran número de valores, la herramienta solo muestra los veinte primeros. En estos casos, aparece una notificación **[!UICONTROL Carga parcial]** para indicar esta limitación. Puede aplicar filtros avanzados para restringir los resultados mostrados y centrarse en valores específicos o subconjuntos de datos.

   ![imagen que muestra la interfaz Distribución de valores](assets/rule-builder-distribution-values.png)

+++

+++ Añadir a favoritos

   Añadir atributos al menú de favoritos le permite acceder rápidamente a los atributos utilizados con más frecuencia. Puede añadir hasta 20 atributos a favoritos. Los atributos favoritos y recientes están asociados con cada usuario dentro de una organización, lo que garantiza la accesibilidad entre diferentes máquinas y proporciona una experiencia perfecta en toda dispositivos.

   Para tener acceso a los atributos que ha marcado como favoritos, use el menú **[!UICONTROL Favoritos y recientes]**. Los atributos favoritos aparecen primero, seguidos por los utilizados recientemente, lo que facilita la localización de los atributos necesarios. Para eliminar un atributo de favoritos, vuelva a seleccionar el icono de estrella.

   ![imagen que muestra la interfaz de favoritos](assets/rule-builder-favorites.png)

+++

1. Haga clic en **[!UICONTROL Confirmar]** para añadir el atributo seleccionado a la condición.

1. Se muestra un panel de propiedades, donde puede configurar el valor deseado para el atributo.

   ![imagen que muestra el generador de reglas con una condición añadida](assets/rule-builder-condition.png)

1. Seleccione de la lista desplegable el **[!UICONTROL operador]** a aplicar. Hay varios operadores disponibles que se pueden utilizar. Los operadores disponibles en la lista desplegable dependen del tipo de datos del atributo.

   +++Lista de operadores disponibles

   | Operador | Objetivo | Ejemplo |
   |---|---|---|
   | Igual a | Devuelve un resultado idéntico a los datos introducidos en la segunda columna Valor. | El apellido (@lastName) equivalente a “Jones” solo devolverá como resultado los destinatarios cuyo apellido sea Jones. |
   | No igual a | Devuelve todos los valores que no son idénticos al valor entrado. | El idioma (@language) no es equivalente a “inglés”. |
   | Mayor que | Devuelve un valor mayor que el valor entrado. | La edad (@age) mayor que 50 devolverá como resultado todos los valores mayores que 50, es decir 51, 52, etc. |
   | Menor que | Devuelve un valor menor que el valor entrado. | La fecha de creación (@created) antes de “DaysAgo(100)” devolverá como resultado todos los destinatarios creados hace menos de 100 días. |
   | Mayor o igual que | Devuelve todos los valores iguales o mayores que el valor entrado. | La edad (@age) mayor o igual que “30” devolverá como resultado todos los destinatarios de 30 años o más. |
   | Menor o igual que | Devuelve todos los valores iguales o inferiores al valor entrado. | La edad (@age) menor o igual que “60” devolverá como resultado todos los destinatarios de 60 años o menos. |
   | Incluido en | Devuelve los resultados incluidos entre los valores indicados. Estos valores deben separarse con una coma. | La fecha de nacimiento (@birthDate) incluida en “10/12/1979,10/12/1984” devolverá como resultado los destinatarios nacidos entre esas fechas. |
   | No en | Funciona como el operador Incluido en. Aquí, los destinatarios se excluyen según los valores introducidos. | La fecha de nacimiento (@birthDate) no está incluida en “10/12/1979,10/12/1984”. No se devolverá como resultado los destinatarios nacidos dentro de estas fechas. |
   | Está vacío | Devuelve los resultados que coinciden con un valor vacío en la segunda columna Valor. | El móvil (@mobilePhone) está vacío y devuelve todos los destinatarios que no tienen un número de móvil. |
   | No está vacío | Funciona de forma inversa al operador Está vacío. No es necesario introducir datos en la segunda columna Valor. | El correo electrónico (@email) no está vacío. |
   | Comienza por | Devuelve los resultados que comienzan con el valor entrado. | El n.º cuenta (@account) comienza con “32010”. |
   | No empieza por | Devuelve los resultados que no empiezan con el valor introducido. | El n.º de cuenta (@account) no comienza con “20”. |
   | Contiene | Devuelve los resultados que contienen al menos el valor entrado. | El dominio de correo electrónico (@domain) que contiene “correo” devuelve todos los nombres de dominio que contengan “correo”, por ejemplo, “gmail.com”. |
   | No contiene | Devuelve los resultados que no contienen el valor entrado. | El dominio de correo electrónico (@domain) no contiene “vo”. Los nombres de dominio que contengan &quot;vo&quot;, como &quot;voila.fr&quot;, no aparecerán en los resultados. |
   | Como | De forma similar al operador Contiene, permite insertar un carácter comodín % en el valor. | Apellido (@lastName) como “Jon%s”. El carácter comodín actúa para encontrar nombres como “Jones”. |
   | No igual | De forma similar al operador Contiene, permite insertar un carácter comodín % en el valor. | Apellido (@lastName) no igual a “Smi%h”. No se devolverán los resultados de los destinatarios cuyo apellido sea “Smith”. |

+++

1. En el campo **Valor**, defina el valor previsto. También puede utilizar el editor de expresiones para definir manualmente una expresión utilizando los campos de la base de datos y las funciones de ayuda. Para ello, haga clic en el icono ![imagen que muestra el icono del editor de expresiones](assets/do-not-localize/rule-builder-icon-editor.svg). [Más información sobre cómo editar expresiones](../orchestrated/edit-expressions.md)

   Para los atributos de tipo fecha, hay valores predefinidos disponibles mediante la opción **[!UICONTROL Ajustes preestablecidos]**.

   +++Ver ejemplo

   ![imagen que muestra la opción de ajuste preestablecido](assets/rule-builder-attribute-preset.png)

+++

### Condiciones personalizadas en las tablas vinculadas (vínculos 1-1 y 1-N){#links}

Las condiciones personalizadas permiten consultar tablas vinculadas a la tabla que utiliza actualmente la regla. Esto incluye tablas con un vínculo de cardinalidad 1-1 o tablas de colección (vínculo 1-N).

Para un **vínculo 1-1**, vaya a la tabla vinculada, seleccione el atributo deseado y defina el valor previsto.

También puede seleccionar directamente un vínculo de tabla en el selector **Valor** y confirmar. En ese caso, los valores disponibles para la tabla seleccionada deben seleccionarse mediante un selector específico, como se muestra en el ejemplo siguiente.

+++Ejemplo de consulta

En este caso, la consulta está dirigida a marcas cuya etiqueta es “en ejecución”.

1. Vaya dentro de la tabla **Marca** y seleccione el atributo **Etiqueta**.

   ![Captura de pantalla de la tabla Marca](assets/rule-builder-1-1-attribute.png)

1. Defina el valor previsto para el atributo.

   ![Captura de pantalla de la tabla Marca](assets/rule-builder-1-1-attribute-value.png)

Este es un ejemplo de consulta en el que se ha seleccionado directamente un vínculo de tabla. Los valores disponibles para esta tabla deben seleccionarse en un selector específico.

![Captura de pantalla de la tabla Marca](assets/rule-builder-1-1-attribute-table.png)

+++

Para un **vínculo 1-N**, puede definir subcondiciones para restringir la consulta, como se muestra en el ejemplo siguiente.

+++Ejemplo de consulta

En este caso, la consulta se dirige a los destinatarios que han realizado compras relacionadas con el producto Brewmsaster, por más de 100 USD.

1. Seleccione la tabla **Compras** y confirme.

1. Haga clic en **[!UICONTROL Añadir condición]** para definir las subcondiciones que se aplicarán a la tabla seleccionada.

   ![Captura de pantalla de la tabla Compra](assets/rule-builder-1-n-purchase.png)

1. Añada subcondiciones para adaptarlas a sus necesidades.

   ![Captura de pantalla de la tabla Compra](assets/rule-builder-1-n-collection.png)

+++

### Condiciones personalizadas con Agregar datos {#aggregate}

Las condiciones personalizadas le permiten realizar operaciones de agregado. Para ello, debe seleccionar directamente un atributo de una tabla de colección:

1. Desplácese por la tabla de colección deseada y seleccione el atributo en el que desea realizar una operación de agregado.

1. En el panel de propiedades, active la opción **Agregar datos** y seleccione la función de agregado que desee.

   ![Captura de pantalla de la opción Agregar datos](assets/rule-builder-aggregate.png)

## Combinación de condiciones mediante operadores {#operators}

Cada vez que añade una nueva condición a la regla, un operador **AND** la vincula automáticamente a la condición existente. Esto significa que los resultados de las dos condiciones se combinan.

Para cambiar el operador entre condiciones, haga clic en él y seleccione el operador deseado.

![Ejemplo de consulta](assets/rule-builder-change-operator.png)

Los operadores disponibles son los siguientes:

* **AND (intersección)**: combina los resultados que coinciden con todos los componentes de filtrado en las transiciones de salida.
* **OR (unión)**: incluye resultados que coinciden con al menos uno de los componentes de filtrado en las transiciones de salida.
* **EXCEPT (exclusión)**: excluye los resultados que coinciden con todos los componentes de filtrado en la transición de salida.

## Manipulación de condiciones {#manipulate}

La barra de herramientas del lienzo del generador de reglas proporciona opciones para manipular fácilmente las condiciones dentro de la regla:

| Icono Barra de herramientas | Descripción |
|--- |--- |
| ![Icono Mover selección hacia arriba](assets/do-not-localize/rule-builder-icon-up.svg) | Mueve el componente una fila hacia arriba. |
| ![Icono Mover selección hacia abajo](assets/do-not-localize/rule-builder-icon-down.svg) | Mueve el componente una fila hacia abajo. |
| ![Icono Agrupar selección](assets/do-not-localize/rule-builder-icon-group.svg) | Coloca dos componentes en un grupo. |
| ![Icono Desagrupar selección](assets/do-not-localize/rule-builder-icon-ungroup.svg) | Separa los componentes de un solo grupo. |
| ![Icono Expandir todo](assets/do-not-localize/rule-builder-icon-expand.svg) | Expande todos los grupos. |
| ![Icono Contraer todo](assets/do-not-localize/rule-builder-icon-collapse.svg) | Contrae todos los grupos. |
| ![Icono Quitar todo](assets/do-not-localize/rule-builder-icon-delete.svg) | Quita todos los grupos y componentes. |

Según sus necesidades, es posible que tenga que crear grupos intermedios de componentes agrupándolos en un mismo grupo y vinculándolos juntos.

* Para agrupar dos condiciones existentes, seleccione una de las dos condiciones y haga clic en el botón ![icono Mover selección hacia arriba](assets/do-not-localize/rule-builder-icon-up.svg) o ![icono Mover selección hacia abajo](assets/do-not-localize/rule-builder-icon-down.svg) para agruparla con la condición por encima o por debajo.

* Para agrupar una condición existente por una nueva, seleccione la condición, haga clic en el botón ![imagen que muestra el botón Más acciones](assets/do-not-localize/rule-builder-icon-more.svg) y seleccione **[!UICONTROL Añadir grupo]**. Seleccione el nuevo atributo que desea añadir al grupo y confirme.

  ![](assets/rule-builder-edit-groups.png)

En el siguiente ejemplo, hemos creado un grupo intermedio para clientes de destinatario que compraron el producto BrewMaster o VanillaVelvet.

![](assets/rule-builder-groups.png)

## Compruebe y valide la consulta

Una vez que haya creado la consulta en el lienzo, puede comprobarla con el panel **Propiedades de la regla**. Las operaciones disponibles son las siguientes:

* **Ver resultados:** muestra los datos resultantes de la consulta.
* **Vista de código**: muestra una versión basada en código de la consulta en SQL.
* **Calcular**: actualiza y muestra el número de registros a los que se destina la regla.
* **Seleccionar o guardar filtro**: elija un filtro predefinido existente para utilizarlo en el lienzo o guarde la consulta como un filtro predefinido para reutilizarlo en el futuro.

<br/>

    >[!IMPORTANTE]
    >
    >Seleccione un filtro predefinido en el panel Propiedades de la regla para reemplazar la regla que se ha creado en el lienzo por el filtro seleccionado.

Cuando la regla esté lista, haga clic en el botón **[!UICONTROL Confirmar]** para guardarla.
