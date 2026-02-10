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
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 3%

---


# Pasar colecciones a parámetros de acción personalizados {#passing-collection}

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

   ![Función de colección de filtros con interfaz de generador de condiciones](assets/uc-collection-2.png){width="70%" align="left"}

1. Cree el recorrido y añada la acción personalizada que ha creado. Obtenga más información en [esta página](../building-journeys/using-custom-actions.md).

1. En la sección **[!UICONTROL Parámetros de acción]**, defina el parámetro de matriz (`products` en nuestro ejemplo) utilizando el editor de expresiones avanzadas.

   ![Expresión de filtrado de colección con selección de campo](assets/uc-collection-3.png)

1. Para cada uno de los siguientes campos de objeto, escriba el nombre del campo correspondiente del esquema XDM de origen. Si los nombres son idénticos, no es necesario. En nuestro ejemplo, solo necesitamos definir `product id` y &quot;color&quot;.

   ![Función de ordenación de colecciones con la configuración de pedidos](assets/uc-collection-4.png){width="50%" align="left"}

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

![Colección heterogénea con tipos de datos mixtos y selección de campos](assets/uc-collection-heterogeneous.png){width="70%" align="left"}

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

