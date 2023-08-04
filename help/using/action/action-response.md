---
solution: Journey Optimizer
product: journey optimizer
title: Configurar una acción personalizada
description: Obtenga información sobre cómo configurar una acción personalizada
feature: Actions
topic: Administration
role: Admin
level: Experienced
badge: label="Beta" type="Informative"
keywords: acción, terceros, personalizado, recorrido, API
hide: true
hidefromtoc: true
source-git-commit: 1674eceb1b9ae4cf8cd3f19deda26a9e72290106
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 10%

---

# Mejoras de acciones personalizadas

Ahora puede utilizar las respuestas de llamadas de API en acciones personalizadas y organizar su recorrido en función de estas respuestas.

Esta capacidad solo estaba disponible cuando se utilizaban fuentes de datos. Ahora puede utilizarlo con acciones personalizadas.

>[!AVAILABILITY]
>
>Actualmente, esta función está disponible como una versión beta privada.

## Definición de la acción personalizada

Al definir la acción personalizada, se han implementado dos mejoras: la adición del método de GET y el nuevo campo de respuesta de carga útil. Las demás opciones y parámetros no cambiarán. Consulte [esta página](../action/about-custom-action-configuration.md).

### Configuración de extremo

El **Configuración de URL** se ha cambiado el nombre de la sección **Configuración de extremo**.

En el **Método** desplegable, ahora puede seleccionar **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### Cargas útiles

El **Parámetros de acción** se ha cambiado el nombre de la sección **Cargas útiles**. Hay dos campos disponibles:

* El **Solicitud** field: este campo solo está disponible para métodos de llamada de POST y PUT.
* El **Respuesta** campo: esta es la nueva capacidad. Este campo está disponible para todos los métodos de llamada.

>[!NOTE]
> 
>Ambos campos son opcionales.

![](assets/action-response2.png){width="70%" align="left"}

1. Haga clic dentro de **Respuesta** field.

   ![](assets/action-response3.png){width="70%" align="left"}

1. Pegue un ejemplo de la carga útil devuelta por la llamada. Compruebe que los tipos de campo son correctos (cadena, entero, etc.).

   ![](assets/action-response4.png){width="70%" align="left"}

1. Haga clic en **Guardar**.

Cada vez que se llama a la API, el sistema recupera todos los campos incluidos en el ejemplo de carga útil. Observe que puede hacer clic en **Pegar una nueva carga útil** si desea cambiar la carga útil que se mueve actualmente.

Este es un ejemplo de una carga útil de respuesta capturada durante la llamada a un servicio de API meteorológica:

```
{
    "coord": {
        "lon": 2.3488,
        "lat": 48.8534
    },
    "weather": [
        {
            "id": 800,
            "main": "Clear",
            "description": "clear sky",
            "icon": "01d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 29.78,
        "feels_like": 29.78,
        "temp_min": 29.92,
        "temp_max": 30.43,
        "pressure": 1016,
        "humidity": 31
    },
    "visibility": 10000,
    "wind": {
        "speed": 5.66,
        "deg": 70
    },
    "clouds": {
        "all": 0
    },
    "dt": 1686066467,
    "sys": {
        "type": 1,
        "id": 6550,
        "country": "FR",
        "sunrise": 1686023350,
        "sunset": 1686080973
    },
    "timezone": 7200,
    "id": 2988507,
    "name": "Paris",
    "cod": 200
}
```

## Aprovechamiento de la respuesta en un recorrido

Simplemente, agregue la acción personalizada a un recorrido. A continuación, puede aprovechar los campos de carga útil de respuesta en condiciones, otras acciones y la personalización de mensajes.

### Condiciones y acciones

Por ejemplo, puede agregar una condición para comprobar la velocidad del viento. Cuando la persona entra en la tienda de surf puede enviar un empujón si el clima es demasiado ventoso .

![](assets/action-response5.png){width="70%" align="left"}

En la condición, debe utilizar el editor avanzado para aprovechar los campos de respuesta de acción, en **Contexto** nodo.

![](assets/action-response6.png){width="70%" align="left"}

También puede aprovechar las **jo_status** código para crear una nueva ruta en caso de error.

![](assets/action-response7.png){width="70%" align="left"}

>[!WARNING]
>
>Solo las acciones personalizadas recién creadas incluyen este campo de forma predeterminada. Si desea utilizarlo con una acción personalizada existente, debe actualizar la acción. Por ejemplo, puede actualizar la descripción y guardar.

Estos son los valores posibles de este campo:

* código de estado http: por ejemplo **http_200** o **http_400**
* error de tiempo de espera: **timeout**
* error de límite: **tapado**
* error interno: **internalError**

### Personalización de mensajes

Puede personalizar los mensajes mediante los campos de respuesta. En nuestro ejemplo, en la notificación push, personalizamos el contenido mediante el valor de velocidad.

![](assets/action-response8.png){width="70%" align="left"}

>[!NOTE]
>
>La llamada de se realiza solo una vez por perfil en un recorrido determinado. Si hay varios mensajes, las nuevas llamadas no se almacenarán en déclencheur.

## Sintaxis de expresión

Esta es la sintaxis:

```json
#@action{myAction.myField} 
```

A continuación se muestran algunos ejemplos:

```json
// action response field
@action{<action name>.<path to the field>}
@action{OpenWeatherMap.main.temp}
```

```json
// action response field
@action{<action name>.<path to the field>, defaultValue: <default value expression>}
@action{OpenWeatherMap.main.temp, defaultValue: 273.15}
@action{OpenWeatherMap.main.temp, defaultValue: @{myEvent.temperature}} 
```


