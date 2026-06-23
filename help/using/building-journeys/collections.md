---
solution: Journey Optimizer
product: journey optimizer
title: Pasar colecciones a parámetros de acción personalizados
description: Aprenda a pasar colecciones de forma dinámica en Journey Optimizer mediante acciones personalizadas
feature: Journeys, Use Cases, Custom Actions, Collections
topic: Content Management
role: Developer
level: Experienced
exl-id: 8832d306-5842-4be5-9fb9-509050fcbb01
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/zhAlHWwS8UOup7yqqVc2d0lqj4JUj5gOvz7JAwVwZPk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1382
ht-degree: 2%

---

# Pasar colecciones a parámetros de acción personalizados {#passing-collection}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a pasar colecciones simples y de objetos a parámetros de acción personalizados para que se rellenen dinámicamente durante la ejecución.

>[!ENDSHADEBOX]

Puede pasar una colección en parámetros de acción personalizados que se rellenan dinámicamente durante la ejecución.

Se admiten dos tipos de colecciones:

* **Colecciones simples**

  Utilice colecciones simples para listas de valores básicos, como cadenas, números o valores booleanos. Son útiles cuando solo necesita pasar una lista de elementos sin propiedades adicionales.

  Por ejemplo, una lista de tipos de dispositivos:

  ```json
  {
   "deviceTypes": [
       "android",
       "ios"
   ]
  }
  ```

* **Colecciones de objetos**

  Utilice colecciones de objetos cuando cada elemento incluya varios campos o propiedades. Normalmente se utilizan para pasar datos estructurados, como detalles de productos, registros de eventos o atributos de elementos.

  Por ejemplo:

  ```json
  {
  "products":[
     {
        "id":"productA",
        "name":"A",
        "price":20.1
     },
     {
        "id":"productB",
        "name":"B",
        "price":10.0
     },
     {
        "id":"productC",
        "name":"C",
        "price":5.99
     }
   ]
  }
  ```

>[!NOTE]
>
>Las matrices anidadas dentro de colecciones solo se admiten parcialmente en las cargas útiles de solicitudes de acciones personalizadas. Para obtener más información, consulte [Limitaciones](#limitations).

## Procedimiento general {#general-procedure}

En esta sección, utilizamos el siguiente ejemplo de carga útil JSON. Es una matriz de objetos con un campo que es una colección simple.

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "A",
        "price": 20.1,
        "color":"blue",
        "locations": [
          "Paris",
          "London"
        ]
      },
      {
        "id": "productB",
        "name": "B",
        "price": 10.99
      }
    ]
  }
}
```

Puede ver que `products` es una matriz de dos objetos. Debe tener al menos un objeto.

1. Cree su acción personalizada. Obtenga más información en [esta página](../action/about-custom-action-configuration.md).

1. En la sección **[!UICONTROL Parámetros de acción]**, pegue el ejemplo JSON. La estructura mostrada es estática: al pegar la carga útil, todos los campos se definen como constantes.

   ![Editor de expresiones que muestra funciones y operaciones de colección](assets/uc-collection-1.png)

1. Si es necesario, ajuste los tipos de campo. Se admiten los siguientes tipos de campos para colecciones: listString, listInteger, listDecimal, listBoolean, listDateTime, listDateTimeOnly, listDateOnly, listObject

   >[!NOTE]
   >
   >El tipo de campo se infiere automáticamente según el ejemplo de carga útil.

1. Si desea pasar objetos de forma dinámica, debe establecerlos como variables. En este ejemplo establecemos `products` como variable. Todos los campos de objeto incluidos en el objeto se establecen en variables automáticamente.

   >[!NOTE]
   >
   >El primer objeto del ejemplo de carga útil se utiliza para definir los campos.

1. Para cada campo, defina la etiqueta que se mostrará en el lienzo de recorrido.

   ![Función de colección de filtros con interfaz de generador de condiciones](assets/uc-collection-2.png){width="70%"}

1. Cree el recorrido y añada la acción personalizada que ha creado. Obtenga más información en [esta página](../building-journeys/using-custom-actions.md).

1. En la sección **[!UICONTROL Parámetros de acción]**, defina el parámetro de matriz (`products` en nuestro ejemplo) utilizando el editor de expresiones avanzadas.

   ![Expresión de filtrado de colección con selección de campo](assets/uc-collection-3.png)

1. Para cada uno de los siguientes campos de objeto, escriba el nombre del campo correspondiente del esquema XDM de origen. Si los nombres son idénticos, no es necesario. En nuestro ejemplo, solo necesitamos definir `product id` y &quot;color&quot;.

   ![Función de ordenación de colecciones con la configuración de pedidos](assets/uc-collection-4.png){width="50%"}

Para el campo de matriz, también puede utilizar el editor de expresiones avanzadas para realizar la manipulación de datos. En el ejemplo siguiente, utilizamos las funciones [filter](functions/list-functions.md#filter) y [intersect](functions/list-functions.md#intersect):

![Expresión de colección completa con operaciones de filtro, ordenación y límite](assets/uc-collection-5.png)

## Limitaciones {#limitations}

Aunque las colecciones en acciones personalizadas proporcionan flexibilidad para pasar datos dinámicos, hay que tener en cuenta ciertas restricciones estructurales:

* **Compatibilidad con matrices anidadas en acciones personalizadas**

  [!DNL Adobe Journey Optimizer] admite matrices anidadas de objetos en **cargas de respuesta** de acción personalizada, pero esta compatibilidad está limitada en **cargas de solicitud**.

  En las cargas útiles de solicitud, las matrices anidadas solo se admiten cuando contienen un número fijo de elementos, como se define en la configuración de acción personalizada. Por ejemplo, si una matriz anidada siempre incluye exactamente tres elementos, se puede configurar como una constante. Cuando el número de elementos debe ser dinámico, solo las matrices no anidadas (matrices en el nivel inferior) pueden definirse como variables.

  Por ejemplo:

   1. El siguiente ejemplo ilustra un **caso de uso no admitido**.

      En este ejemplo, la matriz de productos incluye una matriz anidada (`locations`) con un número dinámico de elementos, que no se admite en las cargas útiles de solicitud.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "locations": [
            { "name": "Paris" },
            { "name": "London" }
            ]
         }
      ]
      }
      ```

   2. Ejemplo compatible, con elementos fijos definidos como constantes.

      En este caso, las ubicaciones anidadas se reemplazan por campos fijos (`location1`, `location2`), lo que permite que la carga útil siga siendo válida dentro de la configuración admitida.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "location1": { "name": "Paris" },
            "location2": { "name": "London" }
         }
      ]
      }
      ```


* **Colecciones de prueba**: para probar las colecciones con el modo de prueba, debe usar el modo de vista de código. Tenga en cuenta que el modo de vista de código no es compatible con eventos empresariales, por lo que en ese caso, solo puede enviar una colección que contenga un solo elemento.


## Casos particulares{#examples}

Para los tipos y matrices heterogéneos de matrices, la matriz se define con el tipo listAny. Solo puede asignar elementos individuales, pero no puede cambiar la matriz a variable.

![Colección heterogénea con tipos de datos mixtos y selección de campos](assets/uc-collection-heterogeneous.png){width="70%"}

Ejemplo de tipo heterogéneo:

```json
{
    "data_mixed-types": [
        "test",
        "test2",
        null,
        0
    ]
}
```

Ejemplo de matriz de matrices:

```json
{
    "data_multiple-arrays": [
        [
            "test",
            "test1",
            "test2"
        ]
    ]
}
```

## Recursos adicionales

Examine las secciones siguientes para obtener más información sobre la configuración, el uso y la resolución de problemas de sus acciones personalizadas:

* [Empiece a usar las acciones personalizadas](../action/action.md): descubra qué es una acción personalizada y cómo le ayudan a conectarse a sistemas de terceros
* [Configurar las acciones personalizadas](../action/about-custom-action-configuration.md): aprenda a crear y configurar una acción personalizada
* [Usar acciones personalizadas](../building-journeys/using-custom-actions.md): aprenda a usar acciones personalizadas en sus recorridos
* [Solución de problemas con acciones personalizadas](../action/troubleshoot-custom-action.md) - Aprenda a solucionar problemas de una acción personalizada
* [Iterar en datos contextuales](../personalization/iterate-contextual-data.md#arrays-in-journeys): aprenda a trabajar con matrices en expresiones de Recorrido e iterar en respuestas de acciones personalizadas, datos de eventos y búsquedas de conjuntos de datos en la personalización de mensajes

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo pasar colecciones simples y de objetos dinámicamente a parámetros de acción personalizados en Journey Optimizer, incluidos los tipos de campo admitidos, el procedimiento de configuración y las limitaciones conocidas en torno a las matrices anidadas.

**Intenciones:**
* Configure una acción personalizada para aceptar una colección (simple u objeto) como parámetro dinámico
* Defina parámetros de matriz como variables en el editor de expresiones avanzadas al crear un recorrido
* Aplique funciones de filtro e intersección para manipular los datos de la matriz en el editor de expresiones
* Comprenda y trabaje dentro de las limitaciones de matrices anidadas para cargas útiles de solicitudes de acciones personalizadas
* Probar parámetros de colección utilizando el modo de vista de código en el modo de prueba de recorrido

**Glosario:**
* **Colección simple**: Una lista de valores escalares básicos (cadenas, números, valores booleanos) pasados como parámetro de acción personalizada *(específico del producto)*
* **Colección de objetos**: Se pasó una lista de objetos estructurados, cada uno con varios campos, como parámetro de acción personalizada *(específico del producto)*
* **listObject**: tipo de campo utilizado en la configuración de acción personalizada para representar una matriz de objetos *(específicos del producto)*
* **listAny**: Tipo de campo utilizado para matrices heterogéneas o matrices de matrices donde los elementos tienen tipos mixtos *(específicos del producto)*
* **Variable (frente a constante)**: en la configuración de parámetros de acción, un campo establecido en &quot;variable&quot; se rellena dinámicamente en tiempo de ejecución desde el contexto de recorrido, mientras que una &quot;constante&quot; es un valor fijo establecido en el tiempo de configuración *(específico del producto)*

**Protecciones:**
* Las matrices anidadas en cargas útiles de solicitud solo se admiten cuando contienen un número fijo de elementos (definidos como constantes); no se admiten matrices anidadas dinámicas
* El modo de vista de código es necesario para probar colecciones en modo de prueba; la vista de código no es compatible con eventos empresariales, por lo que en ese caso solo se pueden enviar colecciones de un solo elemento
* Debe haber al menos un objeto presente en el ejemplo de carga útil utilizado para definir los campos de recopilación
* El primer objeto del ejemplo de carga útil define los campos de toda la colección

**Terminología:**
* Nombre canónico: Collection — Acrónimo: none — variantes: array, list, dynamic collection
* Sinónimos: &quot;colección simple&quot; = &quot;lista de valores escalares&quot; ; &quot;colección de objetos&quot; = &quot;matriz de objetos&quot;
* No confunda: &quot;listAny&quot; ≠ &quot;listObject&quot; (listAny controla matrices heterogéneas o anidadas; listObject controla matrices uniformes de objetos estructurados)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Cuál es la diferencia entre una colección simple y una colección de objetos?** — Una colección simple contiene valores escalares básicos (cadenas, números, valores booleanos), mientras que una colección de objetos contiene objetos estructurados, cada uno con varios campos con nombre.
* **Q: ¿Cómo puedo hacer que un parámetro de colección sea dinámico durante la ejecución?** — En la sección Parámetros de acción de la acción personalizada, establezca el campo de matriz en &quot;variable&quot;; todos los campos de objeto dentro de él se establecen automáticamente en variables.
* **Q: ¿Se admiten matrices anidadas en cargas útiles de solicitud de acción personalizada?** — Solo parcialmente. Las matrices anidadas con un número fijo y conocido de elementos se pueden definir como constantes. Las matrices anidadas con un número dinámico de elementos no son compatibles con las cargas útiles de solicitud.
* **Q: ¿Cómo se prueba una colección en el modo de prueba de recorrido?** — Utilice el modo de vista de código en la interfaz de prueba. Tenga en cuenta que los eventos empresariales no admiten la vista de código, por lo que solo se pueden probar colecciones de un solo elemento en ese contexto.
* **Q: ¿Qué tipos de campo se admiten en las colecciones?** — se admiten listString, listInteger, listDecimal, listBoolean, listDateTime, listDateTimeOnly, listDateOnly y listObject.

+++
