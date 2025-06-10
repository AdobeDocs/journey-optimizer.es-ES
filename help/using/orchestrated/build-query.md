---
solution: Journey Optimizer
product: journey optimizer
title: Cree su primera regla
description: Aprenda a crear reglas para sus campañas orquestadas
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 5e956a6a-0b89-4d78-8f16-fe9fceb25674
source-git-commit: dd1a9b6e14617014756e5b4449578a1f7bf805b4
workflow-type: tm+mt
source-wordcount: '1801'
ht-degree: 7%

---

# Cree su primera regla {#build-query}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Orqueste actividades](orchestrate-activities.md)<br/><br/>[Envíe mensajes con campañas orquestadas](send-messages.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/><b>[Cree su primera consulta](build-query.md)</b><br/><br/>[Edite expresiones](edit-expressions.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [División](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Los pasos principales para crear reglas para las campañas orquestadas son los siguientes:

1. **Agregar condiciones**: cree condiciones personalizadas para filtrar la consulta creando su propia condición con atributos de la base de datos y expresiones avanzadas.
1. **Combinar condiciones**: organice las condiciones en el lienzo mediante grupos y operadores lógicos.
1. **Compruebe y valide la regla**: compruebe los datos resultantes de la regla antes de guardarla.

## Añadir una condición {#conditions}

Para agregar condiciones en la consulta, siga estos pasos:

1. Acceda al generador de reglas desde una actividad **[!UICONTROL Generar audiencia]**.

1. Haga clic en el botón **Agregar condición** para crear una primera condición para la consulta.

   También puede iniciar la consulta utilizando un filtro predefinido. Para ello, haga clic en el botón **[!UICONTROL Seleccionar o guardar filtro]** y elija **[!UICONTROL Seleccionar filtro predefinido]**.

   ![imagen que muestra el generador de reglas](assets/rule-builder-add.png)

1. Identifique el atributo de la base de datos para utilizarlo como criterio para la condición. El icono &quot;i&quot; junto a un atributo proporciona información sobre la tabla donde se almacena y su tipo de datos.

   ![imagen que muestra la selección de un atributo](assets/rule-builder-select-attribute.png)

   >[!NOTE]
   >
   >El botón **Editar expresión** le permite utilizar el editor de expresiones para definir manualmente una expresión con campos de la base de datos y funciones de ayuda. [Obtenga información sobre cómo editar expresiones](../orchestrated/edit-expressions.md)

1. Haga clic en la imagen ![que muestra el botón Más acciones](assets/do-not-localize/rule-builder-icon-more.svg) junto a un atributo para acceder a estas opciones adicionales:

+++ Distribución de valores

   Analice la distribución de los valores de un atributo determinado dentro de la tabla. Esta función es útil para comprender los valores disponibles, sus recuentos y sus porcentajes. También ayuda a evitar problemas como la incoherencia en las mayúsculas o en la ortografía al crear consultas o expresiones.

   En el caso de los atributos con un gran número de valores, la herramienta solo muestra los veinte primeros. En estos casos, aparece una notificación **[!UICONTROL Carga parcial]** para indicar esta limitación. Puede aplicar filtros avanzados para restringir los resultados mostrados y centrarse en valores específicos o subconjuntos de datos.

   ![imagen que muestra la interfaz Distribution of values](assets/rule-builder-distribution-values.png)

+++

+++ Añadir a favoritos

   Añadir atributos al menú de favoritos permite acceder rápidamente a los atributos más utilizados. Se pueden agregar hasta 20 atributos a los favoritos. Los atributos favoritos y recientes están asociados con cada usuario dentro de una organización, lo que garantiza la accesibilidad entre diferentes máquinas y proporciona una experiencia perfecta en toda dispositivos.

   Para tener acceso a los atributos que ha marcado como favoritos, use el menú **[!UICONTROL Favoritos y recientes]**. Los atributos favoritos aparecen primero, seguidos de los utilizados recientemente, lo que facilita la localización de los atributos necesarios. Para eliminar un atributo de favoritos, vuelva a seleccionar el icono de estrella.

   ![imagen que muestra la interfaz de favoritos](assets/rule-builder-favorites.png)

+++

1. Haga clic en **[!UICONTROL Confirmar]** para agregar el atributo seleccionado a la condición.

1. Se muestra un panel de propiedades, donde puede configurar el valor deseado para el atributo.

   ![imagen que muestra el generador de reglas con una condición agregada](assets/rule-builder-condition.png)

1. Seleccione el **[!UICONTROL Operador]** que se aplicará en la lista desplegable. Hay varios operadores disponibles. Los operadores disponibles en la lista desplegable dependen del tipo de datos del atributo.

   +++Lista de operadores disponibles

   | Operador | Objetivo | Ejemplo |
   |---|---|---|
   | Igual a | Devuelve un resultado idéntico a los datos introducidos en la segunda columna Valor. | Apellido (@lastName) igual a &quot;Jones&quot; solo devuelve como resultado los destinatarios cuyo apellido sea Jones. |
   | No igual a | El resultado son todos los valores que no son idénticos al valor introducido. | Idioma (@language) distinto de &quot;inglés&quot;. |
   | Mayor que | El resultado es un valor mayor que el valor introducido. | Edad (@age) mayor que 50 devuelve como resultado todos los valores mayores que 50, como 51 o 52. |
   | Menor que | El resultado es un valor menor que el valor introducido. | Fecha de creación (@created) antes de &quot;DaysAgo(100)&quot; devuelve como resultado todos los destinatarios creados hace menos de 100 días. |
   | Mayor o igual que | El resultado son todos los valores iguales o mayores que el valor introducido. | Edad (@age) mayor o igual que &quot;30&quot; devuelve como resultado todos los destinatarios de 30 años o más. |
   | Menor o igual que | El resultado son todos los valores iguales o inferiores al valor introducido. | Edad (@age) menor o igual que &quot;60&quot; devuelve como resultado todos los destinatarios de 60 años o menos. |
   | Incluido en | Devuelve los resultados incluidos entre los valores indicados. Estos valores deben separarse con una coma. | Fecha de nacimiento (@birthDate) incluida en &quot;12/10/1979,12/10/1984&quot; devuelve como resultado los destinatarios que nacieran entre esas fechas. |
   | No en | Funciona como el operador Is included in. En este caso, los destinatarios se excluyen según los valores introducidos. | Fecha de nacimiento (@birthDate) no incluida en &quot;12/10/1979,12/10/1984&quot;. Los destinatarios nacidos dentro de estas fechas no se devolverán. |
   | Is empty | Devuelve los resultados que coinciden con un valor vacío en la segunda columna Valor. | Móvil (@mobilePhone) está vacío devuelve todos los destinatarios que no tienen número de móvil. |
   | Is not empty | Funciona de forma inversa al operador Is empty. No es necesario introducir datos en la segunda columna Valor. | Correo electrónico (@email) no está vacío. |
   | Comienza por | Devuelve los resultados que comienzan con el valor ingresado. | N.º cuenta (@account) comienza con &quot;32010&quot;. |
   | No empieza por | Devuelve los resultados que no comienzan con el valor introducido. | N.º cuenta (@account) no comienza con &quot;20&quot;. |
   | Contains | Devuelve los resultados que contienen al menos el valor introducido. | Dominio de correo electrónico (@domain) contiene &quot;mail&quot; devuelve todos los nombres de dominio que contienen &quot;mail&quot;, como &quot;gmail.com&quot;. |
   | No contiene | Devuelve los resultados que no contienen el valor introducido. | Email domain (@domain) no contiene &quot;vo&quot;. Los nombres de dominio que contengan &quot;vo&quot;, como &quot;voila.fr&quot;, no aparecerán en los resultados. |
   | Como | De forma similar al operador Contains, permite insertar un carácter comodín % en el valor. | Apellido (@lastName) como &quot;Jon%s&quot;. El carácter comodín actúa como un &quot;joker&quot; para encontrar nombres como &quot;Jones&quot;. |
   | Not like | De forma similar al operador Contains, permite insertar un carácter comodín % en el valor. | Apellido (@lastName) como &quot;Smi%h&quot;. Los destinatarios cuyo apellido sea &quot;Smith&quot; no se devolverán. |

+++

1. En el campo **Value**, defina el valor esperado. También puede utilizar el editor de expresiones para definir manualmente una expresión utilizando los campos de la base de datos y las funciones de ayuda. Para ello, haga clic en la imagen ![que muestra el icono del editor de expresiones](assets/do-not-localize/rule-builder-icon-editor.svg). [Obtenga información sobre cómo editar expresiones](../orchestrated/edit-expressions.md)

   Para los atributos de tipo fecha, hay valores predefinidos disponibles mediante la opción **[!UICONTROL Ajustes preestablecidos]**.

   +++Ver ejemplo

   ![imagen que muestra la opción de ajuste preestablecido](assets/rule-builder-attribute-preset.png)

+++

### Condiciones personalizadas en las tablas vinculadas (vínculos 1-1 y 1-N){#links}

Las condiciones personalizadas permiten consultar tablas vinculadas a la tabla que utiliza actualmente la regla. Esto incluye tablas con un vínculo de cardinalidad 1-1 o tablas de recopilación (vínculo 1-N).

Para un vínculo **1-1**, vaya a la tabla vinculada, seleccione el atributo deseado y defina el valor esperado.

También puede seleccionar directamente un vínculo de tabla en el selector **Value** y confirmar. En ese caso, los valores disponibles para la tabla seleccionada deben seleccionarse mediante un selector dedicado, como se muestra en el ejemplo siguiente.

+++Ejemplo de consulta

En este caso, la consulta está dirigida a marcas cuya etiqueta está &quot;en ejecución&quot;.

1. Vaya dentro de la tabla **Brand** y seleccione el atributo **Label**.

   ![Captura de pantalla de la tabla de marca](assets/rule-builder-1-1-attribute.png)

1. Defina el valor esperado para el atributo.

   ![Captura de pantalla de la tabla de marca](assets/rule-builder-1-1-attribute-value.png)

Este es un ejemplo de consulta en el que se ha seleccionado directamente un vínculo de tabla. Los valores disponibles para esta tabla deben seleccionarse de un selector específico.

![Captura de pantalla de la tabla de marca](assets/rule-builder-1-1-attribute-table.png)

+++

Para un vínculo **1-N**, puede definir subcondiciones para restringir la consulta, como se muestra en el ejemplo siguiente.

+++Ejemplo de consulta

En este caso, la consulta se dirige a los destinatarios que han realizado compras relacionadas con el producto Brewmsaster, por más de 100 $.

1. Seleccione la tabla **Purchases** y confirme.

1. Haga clic en **[!UICONTROL Agregar condición]** para definir las subcondiciones que se aplicarán a la tabla seleccionada.

   ![Captura de pantalla de la tabla de compra](assets/rule-builder-1-n-purchase.png)

1. Añada subcondiciones para adaptarlas a sus necesidades.

   ![Captura de pantalla de la tabla de compra](assets/rule-builder-1-n-collection.png)

+++

### Condiciones personalizadas con datos acumulados {#aggregate}

Las condiciones personalizadas le permiten realizar operaciones acumuladas. Para ello, debe seleccionar directamente un atributo de una tabla de recopilación:

1. Desplácese dentro de la tabla de recopilación deseada y seleccione el atributo en el que desea realizar una operación de acumulado.

1. En el panel de propiedades, active la opción **Agregar datos** y seleccione la función de agregado que desee.

   ![Captura de pantalla de la opción de datos agregados](assets/rule-builder-aggregate.png)

## Combinación de condiciones mediante operadores {#operators}

Cada vez que agrega una nueva condición a la regla, un operador **AND** la vincula automáticamente a la condición existente. Esto significa que los resultados de las dos condiciones se combinan.

Para cambiar el operador entre condiciones, haga clic en él y seleccione el operador deseado.

![Ejemplo de consulta](assets/rule-builder-change-operator.png)

Los operadores disponibles son:

* **AND (intersección)**: combina los resultados que coinciden con todos los componentes de filtrado en las transiciones salientes.
* **OR (Union)**: incluye resultados que coinciden con al menos uno de los componentes de filtrado en las transiciones salientes.
* **EXCEPT (Exclusion)**: Excluye los resultados que coinciden con todos los componentes de filtrado de la transición saliente.

## Manipulación de condiciones {#manipulate}

La barra de herramientas del lienzo del generador de reglas proporciona opciones para manipular fácilmente las condiciones dentro de la regla:

| Icono Barra de herramientas | Descripción |
|--- |--- |
| ![Icono de subir selección](assets/do-not-localize/rule-builder-icon-up.svg) | Mueva el componente una fila hacia arriba. |
| ![Icono de bajar selección](assets/do-not-localize/rule-builder-icon-down.svg) | Desplace el componente una fila hacia abajo. |
| ![Icono de selección de grupo](assets/do-not-localize/rule-builder-icon-group.svg) | Coloque dos componentes en un grupo. |
| ![Icono de selección de desagrupar](assets/do-not-localize/rule-builder-icon-ungroup.svg) | Separe los componentes de un solo grupo. |
| ![Expandir todo el icono](assets/do-not-localize/rule-builder-icon-expand.svg) | Expanda todos los grupos. |
| ![Contraer todos los iconos](assets/do-not-localize/rule-builder-icon-collapse.svg) | Contraer todos los grupos. |
| ![Quitar todos los iconos](assets/do-not-localize/rule-builder-icon-delete.svg) | Elimine todos los grupos y componentes. |

Según sus necesidades, es posible que tenga que crear grupos intermedios de componentes agrupándolos en un mismo grupo y vinculándolos juntos.

* Para agrupar dos condiciones existentes, seleccione una de las dos condiciones y haga clic en el botón ![Subir icono de selección](assets/do-not-localize/rule-builder-icon-up.svg) o ![Bajar icono de selección](assets/do-not-localize/rule-builder-icon-down.svg) para agruparla con la condición por encima o por debajo.

* Para agrupar una condición existente por una nueva, seleccione la condición, haga clic en la ![imagen que muestra el botón Más acciones](assets/do-not-localize/rule-builder-icon-more.svg) y seleccione **[!UICONTROL Agregar grupo]**. Seleccione el nuevo atributo que desea añadir al grupo y confirme.

  ![](assets/rule-builder-edit-groups.png)

En el siguiente ejemplo, hemos creado un grupo intermedio para clientes de destinatario que compraron el producto BrewMaster o VanillaVelvet.

![](assets/rule-builder-groups.png)

## Compruebe y valide la consulta

Una vez que haya creado la consulta en el lienzo, puede comprobarla con el panel **Propiedades de regla**. Las operaciones disponibles son:

* **Ver resultados:** Muestra los datos resultantes de la consulta.
* **Vista de código**: muestra una versión basada en código de la consulta en SQL.
* **Calcular**: actualiza y muestra el número de registros dirigidos por la regla.
* **Seleccione o guarde el filtro**: elija un filtro predefinido existente para utilizarlo en el lienzo o guarde la consulta como un filtro predefinido para reutilizarlo en el futuro.

<br/>

    >[!IMPORTANT]
    >
    >Seleccione un filtro predefinido en el panel Propiedades de regla para reemplazar la regla que se ha creado en el lienzo por el filtro seleccionado.

Cuando la regla esté lista, haga clic en el botón **[!UICONTROL Confirmar]** de para guardarla.
