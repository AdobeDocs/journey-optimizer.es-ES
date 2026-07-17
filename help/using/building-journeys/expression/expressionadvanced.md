---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con el editor de expresiones avanzado
description: Aprenda a crear expresiones avanzadas
feature: Journeys
role: Developer
level: Experienced
keywords: editor de expresiones, datos, recorrido
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/8RsF-CRRrsLiCzwsaqfJQnWcyy6frmKkdSJBKnIhGgE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: ac5d9310-7772-40fb-9d78-864562e1bfd6id: e51e8901-97d9-4f7d-a835-503025a90e32id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 423db08a3c4c5a8d9540fa0c8e03e28ca36ca299
workflow-type: tm+mt
source-wordcount: 1236
ht-degree: 31%

---

# Trabajo con el editor de expresiones avanzado {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Acerca del editor de expresiones avanzadas"
>abstract="El editor de expresiones avanzadas crea expresiones avanzadas en varias pantallas de la interfaz. Por ejemplo, se pueden generar expresiones al configurar y utilizar recorridos y al definir una condición de fuente de datos."

Utilice el editor de expresiones avanzadas de Recorrido para crear expresiones avanzadas en varias pantallas de la interfaz. Por ejemplo, se pueden generar expresiones al configurar y utilizar recorridos y al definir una condición de fuente de datos.

También está disponible cada vez que necesite definir parámetros de acción que requieran manipulaciones de datos específicas. Puede aprovechar los datos procedentes de los eventos o la información adicional recuperada del origen de datos. En un viaje, la lista mostrada de los campos de evento es contextual y varía según los eventos agregados en el recorrido.

![](../assets/journey65.png)


El editor de expresiones avanzadas oferta un conjunto de funciones y operadores integrados que le permiten manipular valores, y definir una expresión que se ajuste específicamente a sus necesidades. El editor de expresiones avanzadas también permite definir los valores del parámetro de fuente de datos externo, y manipular los campos y colecciones de mapas.

>[!NOTE]
>
>Las funciones y capacidades disponibles en el editor de expresiones avanzadas de Recorrido difieren de las disponibles en el [editor de personalización](../../personalization/functions/functions.md).

## Acceso al editor de expresiones avanzadas {#accessing-the-advanced-expression-editor}

El editor de expresiones avanzadas se puede utilizar para lo siguiente:

* crear [condiciones avanzadas ](../conditions.md#data_source_condition) en fuentes de datos e información de evento
* definir [actividades de espera personalizadas](../wait-activity.md#custom)
* definir asignación de parámetros de acción

Si es posible, puede cambiar entre los dos modos con el botón **[!UICONTROL Modo avanzado]** / **[!UICONTROL Modo simple]**. El modo simple se describe [aquí](../conditions.md#about_condition).

>[!NOTE]
>
>* Las condiciones se pueden definir en el editor de expresiones simples o avanzadas. Siempre devuelven un tipo booleano.
>
>* Los parámetros de acción se pueden definir seleccionando campos o mediante el editor de expresiones avanzadas. Devuelven un tipo de datos específico según su expresión.

Puede acceder al editor de expresiones avanzadas de diferentes maneras:

* Al crear una condición de fuente de datos, puede acceder al editor avanzado haciendo clic en **[!UICONTROL Modo avanzado]**.

  ![](../assets/journeyuc2_33.png)

* Al crear un temporizador personalizado, se mostrará directamente el editor avanzado.
* Cuando asigne un parámetro de acción, haga clic en **[!UICONTROL Modo avanzado]**.

>[!NOTE]
>
>Para generar expresiones de Recorrido utilizando indicaciones en lenguaje natural, use **[Generate expression with AI](generate-expression.md)** (**public beta**) mediante el control de IA dentro del editor avanzado.

## Descubra la interfaz {#discovering-the-interface}

Esta pantalla le permite escribir manualmente su expresión.

![](../assets/journey70.png)

En la parte izquierda de la pantalla se muestran los campos y las funciones disponibles:

* **[!UICONTROL Eventos]**: elija uno de los campos recibidos del evento entrante. La lista mostrada de los campos de evento es contextual y varía según los eventos agregados en el recorrido. [Más información](../../event/about-events.md)

  >[!CAUTION]
  >
  >No se admite la creación de expresiones mediante eventos de experiencia. Se hace referencia a enfoques alternativos y prácticas recomendadas para crear expresiones/lógica con eventos de experiencia [aquí](../../building-journeys/exp-event-lookup.md)

* **[!UICONTROL Audiencias]**: si ha eliminado un evento de **[!UICONTROL calificación de audiencias]**, elija la audiencia que desee utilizar en la expresión. [Más información](../conditions.md#using-a-segment)
* **[!UICONTROL Fuentes de datos]**: elija entre la lista de campos disponibles en los grupos de campos de las fuentes de datos. [Más información](../../datasource/about-data-sources.md)
* **[!UICONTROL propiedades de Recorrido]**: esta sección reagrupa los campos técnicos relacionados con el recorrido de un perfil determinado. [Más información](journey-properties.md)
* **[!UICONTROL Funciones]**: elija entre una lista de funciones integradas que permitan realizar filtros complejos. Las funciones están organizadas por categorías. [Más información](functions.md)

![](../assets/journey65.png)

Un mecanismo de finalización automática muestra sugerencias contextuales.

![](../assets/journey68.png)

Un mecanismo de validación de sintaxis comprueba la integridad del código. Los errores se muestran en la parte superior del editor.

![](../assets/journey69.png)


>[!TIP]
>
>Al crear condiciones en el editor de expresiones avanzadas, asegúrese de que las expresiones no contengan caracteres ocultos o no imprimibles. Además, utilice expresiones de una sola línea para evitar errores de análisis.


**Necesidad de parámetros al crear condiciones con el editor de expresiones avanzadas**

Si selecciona un campo de un origen de datos externo que requiere que se llame a un parámetro (consulte [esta página](../../datasource/external-data-sources.md)), aparecerá una nueva pestaña a la derecha que le permitirá especificar este parámetro. El valor del parámetro puede proceder de los eventos colocados en el recorrido o en la fuente de datos de Experience Platform (y no de otras fuentes de datos externas). Por ejemplo, en una fuente de datos relacionada con el tiempo, un parámetro utilizado frecuentemente será &quot;city&quot; (ciudad). Como resultado, debe seleccionar dónde desea obtener este parámetro de ciudad. Las funciones también se pueden aplicar a parámetros para realizar cambios de formato o concatenaciones.

![](../assets/journeyuc2_19.png)

Para casos de uso más complejos, si desea incluir los parámetros del origen de datos en la expresión principal, puede definir sus valores con la palabra clave &quot;params&quot;. Consulte [esta página](../expression/field-references.md).

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página presenta el editor de expresiones avanzadas de Recorrido: sus puntos de acceso, paneles de interfaz y capacidades para generar condiciones complejas, temporizadores de espera personalizados y asignaciones de parámetros de acción mediante eventos, fuentes de datos, funciones y operadores.

**Intenciones:**

* Acceso al editor de expresiones avanzadas desde una condición de fuente de datos, una actividad de espera personalizada o una asignación de parámetros de acción
* Generar condiciones booleanas avanzadas con campos de evento, campos de fuente de datos, pertenencia a audiencias y propiedades de recorrido
* Cambie entre el modo simple y el modo avanzado al configurar las condiciones
* Hacer referencia a parámetros de origen de datos externos directamente dentro de la expresión principal mediante la palabra clave `params`
* Utilice la generación de expresiones con tecnología de IA para crear expresiones a partir de peticiones de datos en lenguaje natural

**Glosario:**

* **Editor de expresiones avanzadas**: el editor de código de Journey Optimizer para escribir expresiones complejas; distinto del editor de condiciones más sencillo de apuntar y hacer clic *(específico del producto)*
* **Modo simple**: Un editor de condiciones de apuntar y hacer clic; menos flexible que el editor avanzado, pero más fácil para quienes no son desarrolladores *(específico del producto)*
* **propiedades de Recorrido**: campos técnicos sobre la instancia de recorrido (ID, versión, errores, nodo actual) accesibles en el editor de expresiones *(específico del producto)*
* **Generar expresiones con IA**: una capacidad con tecnología de IA (beta pública) dentro del editor avanzado que genera expresiones a partir de mensajes en lenguaje sencillo *(específicos del producto)*

**Protecciones:**

* No se admite la creación de expresiones utilizando directamente eventos de experiencia: utilice enfoques alternativos como atributos calculados
* Las condiciones siempre devuelven un tipo booleano independientemente del modo de edición
* Las expresiones no deben contener caracteres ocultos o no imprimibles, y deben utilizar un formato de una sola línea para evitar errores de análisis
* Los valores de parámetros de fuentes de datos externas solo pueden proceder de eventos de recorrido o de la fuente de datos de Experience Platform, no de otras fuentes de datos externas
* Las funciones avanzadas del editor de expresiones difieren de las del editor de personalización

**Terminología:**

* Nombre canónico: Editor de expresiones avanzadas — Acrónimo: none — variantes: editor avanzado, editor de expresiones
* Sinónimos: &quot;Modo avanzado&quot; = &quot;editor de expresiones avanzadas&quot;
* No confunda: editor de expresiones avanzadas (condiciones/acciones de recorrido) ≠ editor de personalización (personalización del contenido de mensajes).

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Cuándo debo usar el editor de expresiones avanzadas en lugar del modo simple?** : utilice el editor avanzado cuando necesite consultar colecciones, utilizar funciones, hacer referencia a propiedades de recorridos o crear una lógica de varias condiciones que el editor simple no pueda expresar.
* **Q: ¿Cómo paso un parámetro a un origen de datos externo en la expresión?** — Utilice la palabra clave `params` en la sintaxis de la expresión, p. ej. `#{DataSource.fieldGroup.field, params: {paramName: value}}`.
* **Q: ¿Qué hace el mecanismo de finalización automática?** — Muestra sugerencias de funciones y campos contextuales a medida que escribe, lo que le ayuda a crear expresiones válidas más rápido.
* **Q: ¿Dónde se accede a Generar expresiones con IA?** — A través del control de IA dentro del editor de expresiones avanzadas; actualmente está en versión beta pública.
* **Q: ¿Las condiciones del editor avanzado devuelven un tipo diferente al del modo simple?** — No; las condiciones siempre devuelven un valor booleano en ambos modos.

+++
