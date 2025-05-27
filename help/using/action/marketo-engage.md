---
solution: Journey Optimizer
product: journey optimizer
title: Integración con Marketo Engage
description: Aprenda a utilizar la acción de Marketo Engage
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: integración de marketo, marketo engage
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: ffce95a074c5827b637d081ad23f4cd3754515fe
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 3%

---

# Integración con Marketo Engage {#integrating-with-marketo-engage}

Hay una acción personalizada específica disponible en sus recorridos para integrar Adobe Journey Optimizer y Marketo Engage.

Empiece con un recorrido de integración de datos perfecta con Marketo Engage. Esta acción personalizada específica en Journey Optimizer admite la ingesta de dos tipos de datos clave:

* Personas (perfiles): Marketo transforma los perfiles en perspectivas procesables.
* Objetos personalizados: adapte sus datos con objetos personalizados, como productos, para un enfoque de marketing personalizado.

## Requisitos previos {#prerequisites}

* La instancia de cliente de Marketo Engage debe estar habilitada para IMS.
* La instancia de Marketo Engage y la instancia de Adobe Experience Platform/Journey Optimizer deben estar en la misma organización.
* Se debe proporcionar al cliente **MktoSync: acceso al servicio de ingesta**

## Configuración de la acción {#configure-marketo-action}

* Vaya a Administración > Configuraciones > Acciones y haga clic en Administrar
* En la lista Acciones, haga clic en Crear acción. Más información sobre [Acciones personalizadas](../building-journeys/using-custom-actions.md){target="_blank"}.
* Introduzca el nombre, la descripción y seleccione Adobe Marketo Engage como tipo de acción

![](assets/engage-customaction-creation.png){width="40%" align="left"}

* Haga clic en Editar carga para sus cargas de **Solicitud** y **Respuesta**.
* Para ambos, componga la carga útil y péguela en la ventana emergente dedicada.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

* Inspeccionar y configurar valores de carga útil
Nota: Para pasar valores dinámicamente, cambie **Constant** a **Variable** para cada campo.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

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

* Arrastre la acción personalizada al lienzo de recorrido.
* En la sección **Parámetros de solicitud**, haga clic en Editar para cada uno de los parámetros con valores dinámicos que ha configurado en la carga útil.

![](assets/engage-use-canvas.png){width="70%" align="left"}
