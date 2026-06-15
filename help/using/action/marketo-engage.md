---
solution: Journey Optimizer
product: journey optimizer
title: Integración con Marketo Engage
description: Aprenda a utilizar la acción de Marketo Engage
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: integración de marketo, marketo engage
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
TQID: https://experienceleague.adobe.com/-aRINahKmp9bI1tyW-XA-LzZOFeoEPXpWoH8JydG6Rk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 62bc5f833b5612570ba50c98519a2f9c07d0bd5e
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 3%

---

# Integración con Marketo Engage {#integrating-with-marketo-engage}

>[!BEGINSHADEBOX]

**En esta página:** configure y use la acción personalizada Marketo Engage para que pueda sincronizar datos de personas y objetos personalizados de sus recorridos en Marketo Engage.

>[!ENDSHADEBOX]

Empiece con un recorrido de integración de datos perfecta con Marketo Engage. Hay una acción personalizada específica disponible en sus recorridos para integrar Adobe Journey Optimizer y Marketo Engage. Esta acción personalizada admite la ingesta de dos tipos de datos clave:

* **Personas** (perfiles): Marketo transforma los perfiles en perspectivas procesables.
* **Objetos personalizados**: adapte sus datos con objetos personalizados, como productos, para un enfoque de marketing personalizado.

## Requisitos previos {#prerequisites}

Los siguientes requisitos previos se aplican a esta integración:

* La instancia de cliente de Marketo Engage debe estar habilitada para IMS
* La instancia de Marketo Engage y la instancia de Adobe Experience Platform/Journey Optimizer deben estar en la misma organización
* Se debe proporcionar al cliente **MktoSync: acceso al servicio de ingesta**

## Configurar la acción {#configure-marketo-action}


En Journey Optimizer, debe configurar una acción personalizada para Marketo Engage. Siga estos pasos:

1. Seleccione **[!UICONTROL Configuraciones]** en la sección del menú ADMINISTRACIÓN.
1. En la sección **[!UICONTROL Acciones]**, haga clic en **[!UICONTROL Crear acción]**. El panel de configuración de acción se abre en el lado derecho de la pantalla.
1. Escriba el nombre, la descripción y seleccione **Adobe Marketo Engage** como **tipo de acción**
   ![](assets/engage-customaction-creation.png){width="40%"}
1. Haga clic en el icono **Editar carga** para sus cargas **Solicitud** y **Respuesta**.
1. Para ambos, componga la carga útil y péguela en la ventana emergente dedicada.
   ![](assets/engage-customaction-payload.png){width="70%"}
1. Inspeccionar y configurar valores de carga útil

   Nota: Para pasar valores dinámicamente, cambie **Constant** a **Variable** para cada campo.

   ![](assets/engage-customaction-payload-fields.png){width="70%"}

1. Haz clic en **Guardar** en la pantalla de configuración del campo y, a continuación, **guarda** tu acción personalizada.

Ahora puede utilizar la acción personalizada en el lienzo de recorrido.

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

Para cada acción configurada, hay una actividad de acción Marketo Engage disponible en la paleta del diseñador de recorridos.

Para usarlo, siga estos pasos:

1. Arrastre la acción personalizada al lienzo de recorrido.

1. Introduzca la etiqueta y la descripción de esta acción.

1. En la sección **Parámetros de solicitud**, haga clic en el icono **Editar** para cada uno de los parámetros y seleccione los valores dinámicos que ha configurado en la carga útil.

![](assets/engage-use-canvas.png){width="70%"}
