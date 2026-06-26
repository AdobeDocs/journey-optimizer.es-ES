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
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
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
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1094
ht-degree: 7%

---

# Introducción a la actividad de optimización {#journey-path-optimization}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar la actividad Optimizar para crear varias rutas de recorrido basadas en la experimentación, el direccionamiento y las condiciones, reemplazando la actividad Condición anterior.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Actividad Optimizar"
>abstract="La actividad **Optimizar** le permite definir cómo progresan los individuos a través de su recorrido creando múltiples rutas basadas en criterios específicos, incluida la experimentación, la segmentación y condiciones específicas. Tenga en cuenta que la actividad **Optimizar** es el nuevo vehículo para crear rutas condicionales en recorridos. Reemplaza la actividad **Condición** anterior."

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

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página presenta la actividad Optimizar, el reemplazo de la actividad anterior Condición, que permite a los usuarios crear varias rutas de recorrido mediante experimentación, reglas de segmentación o lógica condicional.

**Intenciones:**

* Comprenda qué hace la actividad Optimizar y cómo reemplaza a la actividad de condición anterior
* Creación de varias rutas de recorrido mediante la experimentación de rutas (prueba A/B)
* Defina reglas de segmentación para dirigir segmentos de audiencia o atributos de perfil específicos a rutas independientes
* Aplique lógica condicional (si/entonces) utilizando el método Conditions dentro de la actividad de optimización
* Migre los recorridos existentes que usaron la actividad Condición a la nueva actividad Optimizar

**Glosario:**

* **Optimizar actividad**: La actividad del lienzo de recorrido que reemplaza la actividad anterior de Condición y permite crear múltiples rutas mediante experimentación, segmentación o condiciones. *(específico del producto)*
* **Ruta de acceso al Recorrido**: secuencia dentro de un recorrido que puede consistir en comunicaciones, tiempos de espera, número de mensajes o cualquier combinación; los perfiles se enrutan a una ruta de acceso según los criterios definidos en la actividad Optimizar. *(específico del producto)*
* **Experimentación de rutas**: método Optimize que divide aleatoriamente los perfiles entre rutas para determinar cuál tiene el mejor rendimiento en comparación con las métricas de éxito predefinidas, como la tasa de conversión o los ingresos. *(específico del producto)*
* **Segmentación de ruta**: un método Optimize (actualmente en disponibilidad limitada) que enruta perfiles a rutas en función de segmentos de audiencia, atributos de perfil o datos contextuales. *(específico del producto)*
* **Condiciones**: método Optimize equivalente a la actividad de condición anterior, que crea rutas condicionales basadas en fuentes de datos, hora, fecha, divisiones de porcentaje o límites de perfil. *(específico del producto)*

**Protecciones:**

* La segmentación de rutas está actualmente en disponibilidad limitada: póngase en contacto con su representante de Adobe para solicitar acceso
* La actividad de Condición anterior se ha eliminado de la interfaz de usuario; los recorridos existentes que la utilizan siguen funcionando y ahora se muestran con un nuevo icono como Optimizar actividades que utilizan el método Condiciones
* Las etiquetas personalizadas establecidas en nodos de condición anteriores se conservan después de la migración a Optimizar

**Terminología:**

* Nombre canónico: Optimizar actividad — Acrónimo: none — variantes: optimización de la ruta del recorrido, Optimizar nodo
* Sinónimos: &quot;Optimizar actividad (método de condiciones)&quot; = &quot;actividad de condición anterior&quot;
* No confunda: &quot;Experimentación con rutas&quot; ≠ &quot;Segmentación de rutas&quot;. La experimentación con rutas utiliza divisiones aleatorias para probar cuál de las rutas tiene el mejor rendimiento; la segmentación con rutas utiliza reglas definidas para dirigir audiencias específicas a rutas específicas

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Qué ha pasado con la actividad de condición?** — se ha sustituido por la actividad Optimizar y se ha eliminado de la interfaz de usuario. Los recorridos existentes que utilizaban actividades de Condición siguen funcionando sin cambios; ahora se muestran con un nuevo icono como Optimizar actividades mediante el método Conditions.
* **Q: ¿Cuáles son los tres métodos disponibles en la actividad Optimizar?** — Experimentación de rutas (divisiones A/B aleatorias para encontrar la ruta con mejor rendimiento), segmentación de rutas (enrutamiento basado en reglas por atributos de audiencia o perfil, actualmente en disponibilidad limitada) y condiciones (lógica condicional si/entonces equivalente a la actividad de condición anterior).
* **Q: ¿En qué se diferencian la experimentación de rutas y la segmentación de rutas?** — La experimentación de rutas divide aleatoriamente los perfiles para probar y comparar el rendimiento de las rutas con las métricas de éxito; la segmentación de rutas dirige audiencias específicas o tipos de perfiles por rutas designadas en función de criterios definidos.
* **Q: ¿Está disponible de forma general el direccionamiento de rutas?** — No; actualmente está en disponibilidad limitada. Póngase en contacto con su representante de Adobe para solicitar acceso.
* **Q: ¿Qué es una ruta de acceso de recorrido?** — Una ruta es una secuencia dentro de un recorrido que puede incluir una combinación de comunicaciones, períodos de espera y recuentos de mensajes; los perfiles se evalúan y enrutan a la ruta adecuada según los criterios de Optimización de actividad.

+++
