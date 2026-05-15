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
TQID: https://experienceleague.adobe.com/hbDoGEHdCBcOe-e9h06kGY2Rvb129cIzto6jJAuGkX4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 470
ht-degree: 12%

---

# Introducción a la actividad de optimización {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Actividad Optimizar"
>abstract="La actividad **Optimizar** le permite definir cómo progresan los individuos a través de su recorrido creando múltiples rutas basadas en criterios específicos, incluida la experimentación, la segmentación y condiciones específicas. Tenga en cuenta que la actividad **Optimize** es el nuevo vehículo para crear rutas condicionales en recorridos. Reemplaza la actividad **Condition** anterior."

>[!IMPORTANT]
>
>La actividad **Optimize** es el nuevo vehículo para crear rutas condicionales en recorridos. Reemplaza la actividad **Condición** anterior, que se ha eliminado de la interfaz de usuario. Se conserva toda la lógica condicional y ahora se gestiona mediante las [condiciones](conditions.md) de la actividad **Optimizar**.
>
>Si tiene recorridos existentes que usaron actividades **[!UICONTROL Condition]**, puede seguir usándolos como antes. Ahora aparecen con un nuevo icono como actividades **[!UICONTROL Optimize]** mediante el método **[!UICONTROL Condition]**, pero el comportamiento no ha cambiado. Se conservará cualquier etiqueta personalizada que haya establecido en el nodo.

La actividad **Optimizar** le permite definir el progreso de las personas en su recorrido mediante la creación de múltiples **rutas** basadas en criterios específicos, incluida la experimentación, el direccionamiento y las condiciones específicas, lo que garantiza la máxima participación y éxito para crear recorridos altamente personalizados y eficaces.

![Botón Optimizar en la paleta de actividades de recorrido](assets/journey-optimize.png)

## ¿Qué es una ruta de recorrido? {#journey-path}

Un recorrido **ruta** puede consistir en cualquiera de las siguientes opciones: secuenciación de las comunicaciones, tiempo entre ellas, número de comunicaciones o cualquier combinación de estas tres variables.

Por ejemplo, una ruta puede contener un correo electrónico, otra puede contener dos mensajes SMS y una tercera puede contener un correo electrónico, un nodo de espera de dos horas y, a continuación, un mensaje SMS.

## Tres formas de optimizar los recorridos {#optimization-methods}

A través de la actividad **Optimizar**, puede realizar las siguientes acciones en sus rutas de recorrido:

* [Ejecutar experimentos de rutas](path-experimentation.md): Pruebe diferentes rutas basadas en divisiones aleatorias para determinar cuál tiene el mejor rendimiento según las métricas de éxito predefinidas (por ejemplo: tasa de conversión, ingresos, participación).

* [Aprovechar reglas de segmentación](path-targeting.md): defina las reglas específicas que deben cumplirse para que un cliente pueda ingresar a una de las rutas de recorrido, según segmentos de audiencia, atributos de perfil o datos contextuales. Esto garantiza que la audiencia correcta entre en la ruta especificada.

  >[!AVAILABILITY]
  >
  >Actualmente, esta capacidad está en disponibilidad limitada. Para solicitar acceso, póngase en contacto con su representante de Adobe.

* [Aplicar condiciones](conditions.md): cree rutas condicionales basadas en criterios específicos, como fuentes de datos, hora, fecha, divisiones de porcentaje o límites de perfil. Es el equivalente de la actividad Condición anterior.

## Funcionamiento {#how-it-works}

Una vez que el recorrido está activo, los perfiles se evalúan según los criterios definidos y, en función de los criterios coincidentes, se envían por la ruta adecuada desde el recorrido.

## Próximos pasos {#next-steps}

Seleccione el método de optimización que mejor se adapte a su caso de uso:

* ¿Quiere probar y aprender qué ruta ofrece el mejor rendimiento? → Ir a [experimentación de ruta](path-experimentation.md)
* ¿Quiere enviar distintas audiencias por rutas específicas? → Ir a [Segmentación de ruta](path-targeting.md)
* ¿Quiere crear una lógica condicional (si/entonces hay escenarios)? → Ir a [Condiciones](conditions.md)
