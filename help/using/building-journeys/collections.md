---
solution: Journey Optimizer
product: journey optimizer
title: Paso de colecciones de forma dinámica mediante acciones personalizadas
description: Envío de un mensaje mediante Campaign v7/v8
feature: Journeys, Use Cases, Custom Actions, Collections
topic: Content Management
role: Developer, Data Engineer
level: Experienced
exl-id: 8832d306-5842-4be5-9fb9-509050fcbb01
version: Journey Orchestration
source-git-commit: 8f25fd5110777c148246864b364d02e4c6bf00da
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 6%

---


# Paso de colecciones de forma dinámica mediante acciones personalizadas{#passing-collection}

Puede pasar una colección en parámetros de acción personalizados que se rellenarán dinámicamente durante la ejecución. Se admiten dos tipos de colecciones:

* **colecciones simples**: matrices de tipos de datos simples, por ejemplo, con un listString:

  ```json
  {
   "deviceTypes": [
       "android",
       "ios"
   ]
  }
  ```

* o **colecciones de objetos**: una matriz de objetos JSON, por ejemplo:

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

   ![](assets/uc-collection-1.png)

1. Si es necesario, ajuste los tipos de campo. Se admiten los siguientes tipos de campos para colecciones: listString, listInteger, listDecimal, listBoolean, listDateTime, listDateTimeOnly, listDateOnly, listObject

   >[!NOTE]
   >
   >El tipo de campo se infiere automáticamente según el ejemplo de carga útil.

1. Si desea pasar objetos de forma dinámica, debe establecerlos como variables. En este ejemplo establecemos `products` como variable. Todos los campos de objeto incluidos en el objeto se establecen en variables automáticamente.

   >[!NOTE]
   >
   >El primer objeto del ejemplo de carga útil se utiliza para definir los campos.

1. Para cada campo, defina la etiqueta que se mostrará en el lienzo de recorrido.

   ![](assets/uc-collection-2.png){width="70%" align="left"}

1. Cree el recorrido y añada la acción personalizada que ha creado. Obtenga más información en [esta página](../building-journeys/using-custom-actions.md).

1. En la sección **[!UICONTROL Parámetros de acción]**, defina el parámetro de matriz (`products` en nuestro ejemplo) utilizando el editor de expresiones avanzadas.

   ![](assets/uc-collection-3.png)

1. Para cada uno de los siguientes campos de objeto, escriba el nombre del campo correspondiente del esquema XDM de origen. Si los nombres son idénticos, no es necesario. En nuestro ejemplo, solo necesitamos definir `product id` y &quot;color&quot;.

   ![](assets/uc-collection-4.png){width="50%" align="left"}

Para el campo de matriz, también puede utilizar el editor de expresiones avanzadas para realizar la manipulación de datos. En el ejemplo siguiente, utilizamos las funciones [filter](functions/functionfilter.md) y [intersect](functions/functionintersect.md):

![](assets/uc-collection-5.png)

## Limitaciones {#limitations}

* **Compatibilidad con matrices anidadas en acciones personalizadas**

  Adobe Journey Optimizer admite matrices anidadas de objetos en **cargas de respuesta** de acción personalizada, pero esta compatibilidad está limitada en **cargas de solicitud**.

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


* Para probar colecciones con el modo de prueba, debe utilizar el modo de vista de código. El modo de vista de código no es compatible con eventos empresariales en este momento. Solo puede enviar una colección con un solo elemento.


## Casos particulares{#examples}

Para los tipos y matrices heterogéneos de matrices, la matriz se define con el tipo listAny. Solo puede asignar elementos individuales, pero no puede cambiar la matriz a variable.

![](assets/uc-collection-heterogeneous.png){width="70%" align="left"}

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

**Temas relacionados**

[Uso de acciones personalizadas](../building-journeys/using-custom-actions.md)
