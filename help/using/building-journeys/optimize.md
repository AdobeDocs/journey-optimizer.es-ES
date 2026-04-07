---
solution: Journey Optimizer
product: journey optimizer
title: Actividad Optimizar
description: Descubra más información sobre la actividad Optimizar
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: actividad, condición, lienzo, recorrido, optimización
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
source-git-commit: 8521e59022c221c0ca4e5b69b5b3aefe6304b417
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 3%

---

# Introducción a la actividad de optimización {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Actividad Optimizar"
>abstract="La actividad **Optimizar** le permite definir el progreso de las personas en su recorrido mediante la creación de varias rutas basadas en criterios específicos, incluida la experimentación, el direccionamiento y las condiciones específicas. Tenga en cuenta que la actividad **Optimize** es el nuevo vehículo para crear rutas condicionales en recorridos. Reemplaza la actividad **Condition** anterior."

>[!IMPORTANT]
>
>La actividad **Optimize** es el nuevo vehículo para crear rutas condicionales en recorridos. Reemplaza la actividad **Condition** anterior, que se ha eliminado de la interfaz de usuario. Se conserva toda la lógica condicional y ahora se gestiona mediante las **condiciones** de la actividad [Optimizar](conditions.md).
>
>Si tiene recorridos existentes que usaron actividades **[!UICONTROL Condition]**, puede seguir usándolos como antes. Ahora aparecen con un nuevo icono como actividades **[!UICONTROL Optimize]** mediante el método **[!UICONTROL Condition]**, pero el comportamiento no ha cambiado. Se conservará cualquier etiqueta personalizada que haya establecido en el nodo.

La actividad **Optimizar** le permite definir el progreso de las personas en su recorrido mediante la creación de múltiples **rutas** basadas en criterios específicos, incluida la experimentación, el direccionamiento y las condiciones específicas, lo que garantiza la máxima participación y éxito para crear recorridos altamente personalizados y eficaces.

![Botón Optimizar en la paleta de actividades de recorrido](assets/journey-optimize.png)

## ¿Qué es una ruta de recorrido?

Un recorrido **ruta** puede consistir en cualquiera de las siguientes opciones: secuenciación de las comunicaciones, tiempo entre ellas, número de comunicaciones o cualquier combinación de estas tres variables.

Por ejemplo, una ruta puede contener un correo electrónico, otra puede contener dos mensajes SMS y una tercera puede contener un correo electrónico, un nodo de espera de dos horas y, a continuación, un mensaje SMS.

## Tres formas de optimizar los recorridos

A través de la actividad **Optimizar**, puede realizar las siguientes acciones en sus rutas de recorrido:

* [Ejecutar experimentos de rutas](path-experimentation.md): Pruebe diferentes rutas basadas en divisiones aleatorias para determinar cuál tiene el mejor rendimiento según las métricas de éxito predefinidas (por ejemplo: tasa de conversión, ingresos, participación).

* [Aprovechar reglas de segmentación](path-targeting.md): defina las reglas específicas que deben cumplirse para que un cliente pueda ingresar a una de las rutas de recorrido, según segmentos de audiencia, atributos de perfil o datos contextuales. Esto garantiza que la audiencia correcta entre en la ruta especificada.

  >[!AVAILABILITY]
  >
  >Actualmente, esta capacidad está en disponibilidad limitada. Para solicitar acceso, póngase en contacto con su representante de Adobe.

* [Aplicar condiciones](conditions.md): cree rutas condicionales basadas en criterios específicos, como fuentes de datos, hora, fecha, divisiones de porcentaje o límites de perfil. Es el equivalente de la actividad Condición anterior.

## Funcionamiento

Una vez que el recorrido está activo, los perfiles se evalúan según los criterios definidos y, en función de los criterios coincidentes, se envían por la ruta adecuada desde el recorrido.

## Próximos pasos

Seleccione el método de optimización que mejor se adapte a su caso de uso:

* ¿Quiere probar y aprender qué ruta ofrece el mejor rendimiento? → Ir a [experimentación de ruta](path-experimentation.md)
* ¿Quiere enviar distintas audiencias por rutas específicas? → Ir a [Segmentación de ruta](path-targeting.md)
* ¿Quiere crear una lógica condicional (si/entonces hay escenarios)? → Ir a [Condiciones](conditions.md)
