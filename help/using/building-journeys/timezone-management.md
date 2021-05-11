---
title: Administración de husos horarios
description: Obtenga información sobre la administración de husos horarios
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 2%

---

# Administración de husos horarios {#timezone_management}

![](../assets/do-not-localize/badge.png)

Puede definir una zona horaria en las [propiedades](../building-journeys/journey-gs.md#change-properties) del recorrido.

Para acceder a Propiedades, haga clic en el icono de lápiz en la parte superior derecha de la pantalla.

Esta zona horaria se utilizará para todas las actividades del recorrido que contengan un elemento horario como:

* [Condición horaria](../building-journeys/condition-activity.md#time_condition)
* [Condición de fecha](../building-journeys/condition-activity.md#date_condition)
* [Espera personalizada](../building-journeys/wait-activity.md#custom)
* [Fecha de espera fija](../building-journeys/wait-activity.md#fixed_date)

Puede seleccionar una zona horaria o elegir usar la zona horaria definida en el perfil del usuario.

## Definición de una zona horaria fija {#fixed-timezone}

La zona horaria también se puede corregir. Borre la zona horaria predefinida y elija una de la lista desplegable. Si utiliza una zona horaria fija, será la misma para todas las personas que entren en el recorrido.

Para ello, en **[!UICONTROL Properties]**, seleccione una zona horaria.

![](../assets/journey73.png)

## Uso de perfiles para definir la zona horaria del recorrido {#timezone-from-profiles}

Si el evento de entrada del recorrido tiene un área de nombres, lo que significa que el recorrido puede llegar al servicio Perfil del cliente en tiempo real de Adobe Experience Platform, el huso horario se predefine con el especificado en el perfil del individuo que fluye en el recorrido.

Si se define una zona horaria en el perfil de Adobe Experience Platform, se puede recuperar en el recorrido .

Si el perfil de la persona no contiene una zona horaria, la zona horaria recuperada será la definida en el campo de zona horaria.

Para ello, en **[!UICONTROL Properties]**, marque **[!UICONTROL Use Profile timezone in timers and conditions]**.

![](../assets/journey72.png)

## Uso de zonas horarias en expresiones {#timezone-in-expressions}

Las fechas de inicio y finalización de un recorrido no se pueden vincular a un huso horario específico. Se asocian automáticamente al huso horario de la instancia.
