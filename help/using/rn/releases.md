---
solution: Journey Optimizer
product: journey optimizer
title: Ciclo de lanzamiento de Adobe Journey Optimizer
feature: Release Notes
description: Explicación del ciclo de versiones de Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: c70cdb0f12b484844ab0222cec8922f30b0ee7dc
workflow-type: tm+mt
source-wordcount: '823'
ht-degree: 0%

---

# Ciclo de lanzamiento de Journey Optimizer {#releases}

[!DNL Adobe Journey Optimizer] se actualiza con regularidad para ofrecer nuevas funciones, mejoras y correcciones. Esta página explica cómo funciona el ciclo de lanzamiento y qué significa cada fase de lanzamiento, para que pueda comprender fácilmente cuándo las funciones están disponibles para su organización.

## Modelo de envío continuo {#continuous-delivery-model}

[!DNL Adobe Journey Optimizer] funciona en un modelo de envío continuo, lo que permite un enfoque escalable y gradual de la implementación de funcionalidades. Este modelo permite a Adobe ofrecer innovación con mayor rapidez y garantizar una estabilidad y un rendimiento continuos durante el despliegue.

> [!NOTE]
>
> Dado que [!DNL Adobe Journey Optimizer] utiliza el envío continuo, es posible que las nuevas funciones aparezcan de forma progresiva en todas las organizaciones o regiones.

Como parte de este modelo:

* Las nuevas funciones y mejoras se implementan en producción en cuanto están listas.

* Las [**Notas de la versión**](release-notes.md) se actualizan entre versiones mensuales con una sección de _Últimas actualizaciones_, que anuncia nuevas funciones y mejoras a medida que se implementan, para que se mantenga informado en tiempo real.

## Programación y cadencia de versiones {#release-timing}

[!DNL Adobe Journey Optimizer] suele seguir una cadencia de lanzamiento mensual, y las implementaciones suelen realizarse durante la última semana de cada mes. Las notas de la versión mensuales y la documentación relacionada se publican los martes. Las notas previas al lanzamiento se publican los viernes anteriores a la semana de lanzamiento.

> [!TIP]
>
> Al final de cada trimestre, los lanzamientos se pueden anticipar y desplegar hasta dos semanas antes del final del mes para alinearse con los programas trimestrales o con los lanzamientos de productos dependientes.

Aunque la versión mensual introduce el conjunto principal de nuevas funciones y correcciones, el método de entrega continua permite implementar actualizaciones adicionales entre ciclos cuando están listas. Las notas de la versión y la documentación relacionada se actualizan en consecuencia.


## Rutas de lanzamiento {#release-paths}

Las funciones de Journey Optimizer siguen diferentes rutas de versión según su complejidad, dependencias y ámbito. La plataforma utiliza varias etiquetas de disponibilidad (Beta, disponibilidad limitada, disponibilidad general), pero no todas las funcionalidades pasan por todas ellas.

Las rutas comunes de versiones incluyen:

* **Directo a GA** — Algunas mejoras menores o incrementales van directamente a General Availability (GA).
* **LA → GA**: las funciones primero están disponibles para una audiencia limitada (disponibilidad limitada) antes del despliegue general.
* **Beta → LA → GA**: las capacidades más grandes o experimentales progresan en todas las fases para pruebas y validación.
* **Beta → GA**: Algunas funciones de Beta estables pueden pasar directamente a GA sin una fase de LA intermedia.

> [!TIP]
>
> Si está interesado en acceder anticipadamente a las funciones de Beta o en disponibilidad limitada, póngase en contacto con su representante de Adobe para discutir las opciones de participación.


## Etiquetas de disponibilidad {#availability-labels}

| **Etiqueta** | **Finalidad** | **Disponibilidad** | **Notas de clave** |
|------------|-------------|------------------|----------------|
| **Beta** | Pruebas tempranas y recopilación de comentarios. | Limitado a los clientes u organizaciones seleccionados que participan en el programa Beta de Adobe. | * No destinado a uso en producción.<br>* La funcionalidad o el diseño pueden cambiar antes de GA.<br>: los comentarios ayudan a perfeccionar la implementación final. |
| **Disponibilidad limitada (LA)** | Implementación controlada para validación y monitorización. | Habilitado solo para clientes o entornos seleccionados (por ejemplo, entornos limitados de desarrollo). | * Función es casi final y monitoreado activamente.<br>: se usa para validar el rendimiento y la escalabilidad antes del lanzamiento general.<br>* El acceso requiere la aprobación de Adobe. |
| **Disponibilidad general (GA)** | Amplia versión de funcionalidad totalmente compatible. | Habilitado de forma predeterminada para todas las organizaciones aptas. | * Listo para la producción y totalmente compatible.<br>* Pueden aplicarse licencias o derechos.<br>* puede implementarse progresivamente en todas las regiones. |


## Despliegue y disponibilidad {#rollout}

Incluso después de un anuncio de GA, el despliegue puede ocurrir gradualmente entre organizaciones o regiones. Si una nueva funcionalidad no aparece inmediatamente en su entorno, normalmente estará disponible unos días o semanas después del lanzamiento.

Esta implementación gradual ayuda a Adobe a supervisar la estabilidad, el rendimiento y la experiencia del usuario antes de completar la implementación.


## Mantenerse informado {#staying-informed}

Para mantenerse al día:

* Revise las [**últimas notas de la versión**](release-notes.md) para ver si hay funciones nuevas y actualizadas.
* Consulte la sección **_Últimas actualizaciones_** entre las versiones mensuales para implementaciones en tiempo real.
* Supervisar **Notas previas al lanzamiento** (cuando estén disponibles) para obtener una vista previa de las próximas funciones.
* Póngase en contacto con su representante de Adobe para obtener información sobre el acceso o la asignación de derechos de Beta o disponibilidad limitada.


## Preguntas frecuentes {#faq}

+++ ¿Cuándo se programan las versiones de Adobe Journey Optimizer?

[!DNL Adobe Journey Optimizer] generalmente publica actualizaciones durante la última semana de cada mes. Al final de cada trimestre, la versión puede tardar hasta dos semanas en alinearse con las actualizaciones entre soluciones o en toda la plataforma.

+++

+++ ¿Por qué no veo una nueva función inmediatamente después de anunciarla?

Algunas funciones de GA se implementan progresivamente para garantizar la estabilidad y el rendimiento de la plataforma. Si no ve una función de inmediato, aparecerá una vez que se haya completado la implementación para su región u organización.

+++

+++ ¿Cuál es la diferencia entre Beta, disponibilidad limitada y GA?

* **Beta**: fase de prueba temprana, acceso limitado, basado en comentarios.
* **Disponibilidad limitada (LA)**: Despliegue controlado para validación final.
* **Disponibilidad general (GA)**: Versión completa para todos los clientes autorizados.

+++

+++ ¿Todas las funciones pasan por Beta y disponibilidad limitada?

No. Algunas funciones se publican directamente en GA o solo en LA, según su naturaleza y preparación. La ruta de lanzamiento está adaptada a cada capacidad para equilibrar agilidad, calidad y estabilidad.

+++

+++ ¿Cómo puedo participar en los programas de Beta o de disponibilidad limitada?

El acceso se realiza por invitación o solicitud a través de su representante de Adobe. La participación ayuda a dar forma al diseño de funciones y garantiza que los casos de uso se tengan en cuenta en la versión final.

+++

+++ ¿Con qué frecuencia se actualizan las notas de la versión?

Las notas de la versión se actualizan continuamente. Más allá de las versiones mensuales, la sección _Últimas actualizaciones_ se actualiza cada vez que se insertan nuevas funciones o mejoras en la producción.

+++
