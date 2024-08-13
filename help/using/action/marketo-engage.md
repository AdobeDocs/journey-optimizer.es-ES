---
solution: Journey Optimizer
product: journey optimizer
title: Integración con Marketo Engage
description: Aprenda a utilizar la acción del Marketo Engage
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
hide: true
hidefromtoc: true
keywords: integración de marketo, marketo engage
source-git-commit: 6a49f4b2e0220b1c875b42f70dcb44f3405c6ad2
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Integración con Marketo Engage {#integrating-with-marketo-engage}

Empiece con un recorrido de integración de datos perfecta con Marketo Engage. Esta acción personalizada específica en Journey Optimizer admite la ingesta de dos tipos de datos clave:

* Personas (perfiles): Marketo transforma los perfiles en perspectivas procesables.
* Objetos personalizados: adapte sus datos con objetos personalizados, como productos, para un enfoque de marketing personalizado.

## Requisitos previos {#prerequisites}

* La instancia de cliente de Marketo Engage debe estar habilitada para IMS.
* La instancia de Marketo Engage y la instancia de AEP/AJO deben estar en la misma organización de IMS. +vínculo
* El cliente debe tener acceso a MktoSync: Ingestion Service (NOTA PARA AÑADIR AQUÍ + vínculo)

## Configuración de la acción {#configure-marketo-action}

* Vaya a Administración > Configuraciones > Acciones y haga clic en Administrar
* En la lista Acciones, haga clic en Crear acción. Obtenga más información sobre la creación de acciones personalizadas aquí (+vínculo)
* Introduzca el nombre, la descripción y seleccione Adobe Marketo Engage como tipo de acción

![](assets/engage-customaction-creation.png)

* Haga clic en Editar carga para sus cargas de **Solicitud** y **Respuesta**.
* Para ambos, componga la carga útil y péguela en la ventana emergente dedicada.

![](assets/engage-customaction-payload.png)

* Inspect y configuración de valores de carga útil
Nota: Para pasar valores dinámicamente, cambie **Constant** a **Variable** para cada campo.

![](assets/engage-customaction-payload-fields.png)

* Haga clic en **Guardar** en la ventana de configuración del campo y, a continuación, **Guardar** para la acción personalizada.

Ahora puede utilizar la acción personalizada en el lienzo dedicado.


## Sintaxis de carga útil {#payload-syntax}

### Persona

![](assets/payload-person.png)

### CustomObject

![](assets/payload-customobject.png)


**Ejemplo de carga útil para la persona**

```json
{
   "munchkinID": "388-KKG-245",  
   "person": {
    "priority": "normal",
    "partitionName": "XYZ",
    "dedupeFields": {
      "field1": "email",
      "field2": "firstName"
    },
    "objects": [
      {
        "email": "Email address",
        "firstName": "First name",
        "lastName": "Last name"
      }
    ]
  }
}
```

**Ejemplo de carga útil para el objeto personalizado**

```json
{
  "munchkinID": "388-KKG-245", 
  "customObject": {
    "priority": "normal",
    "objectName": "products",
    "objects": [
      {
        "email": "Email Address",
        "productName": "Product Name",
        "productQty": "Product Quantity",
        "priceTotal": "Price Total"
      }
    ]
  }
}
```


## Uso de la acción {#engage-using}

* Arrastre la acción personalizada al lienzo de recorrido. (Consulte cómo utilizar una acción/vínculo personalizado)
* En Parámetros de solicitud, haga clic en Editar para cada uno de los parámetros con valores dinámicos que haya configurado en la carga útil.

![](assets/engage-use-canvas.png)

