---
solution: Journey Optimizer
product: journey optimizer
title: Ciclo de lanzamiento de Adobe Journey Optimizer
feature: Release Notes
description: Explicación del ciclo de lanzamiento de Adobe Journey Optimizer
keywords: ciclo de lanzamiento, versión beta, disponibilidad limitada, disponibilidad general, GA, LA, notas de la versión
role: User
level: Beginner, Intermediate
exl-id: 344ae3cf-923c-4f0e-b3bc-0313993243c8
TQID: https://experienceleague.adobe.com/u8FJOgdav9VhwCk4CzrJoLrbFkVAa7BO83BCZ4SWsBc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 1f2a71d3323b6a64b346a83aa58b23aed035eb29
workflow-type: tm+mt
source-wordcount: 993
ht-degree: 90%

---

# Ciclo de lanzamiento de Journey Optimizer {#releases}

[!DNL Adobe Journey Optimizer] se actualiza con regularidad para ofrecer nuevas funcionalidades, mejoras y correcciones. En esta página se explica cómo funciona el ciclo de lanzamiento y qué significa cada fase de lanzamiento, para que pueda comprender fácilmente cuándo las funciones están disponibles para su organización.

## Modelo de envío continuo {#continuous-delivery-model}

[!DNL Adobe Journey Optimizer] funciona en un modelo de envío continuo, lo que permite un enfoque escalable y gradual de la implementación de funciones. Este modelo permite a Adobe ofrecer innovación con mayor rapidez y garantizar una estabilidad y un rendimiento continuos durante el despliegue.

>[!NOTE]
>
> Dado que [!DNL Adobe Journey Optimizer] utiliza el envío continuo, es posible que las nuevas funciones aparezcan de forma progresiva en todas las organizaciones o regiones.

Como parte de este modelo:

* Las nuevas funcionalidades y mejoras se implementan en producción en cuanto están listas.

* Las [**Notas de la versión**](release-notes.md) se actualizan entre versiones mensuales con una sección de _Últimas actualizaciones_, que anuncia nuevas funcionalidades y mejoras a medida que se implementan, para que esté informado en tiempo real.

## Programación y cadencia del lanzamiento {#release-timing}

[!DNL Adobe Journey Optimizer] suele seguir una cadencia de lanzamiento mensual, y las implementaciones suelen realizarse durante la última semana de cada mes. Las notas de la versión mensual y la documentación relacionada se publican los martes de la semana de lanzamiento. Las notas de las versiones preliminares se publican los viernes anteriores a la semana de publicación.

>[!TIP]
>
> Al final de cada trimestre, las versiones se pueden anticipar y desplegar hasta dos semanas antes del final del mes para alinearse con los programas trimestrales o con las versiones de productos dependientes.

Aunque la versión mensual introduce el conjunto principal de nuevas funcionalidades y correcciones, el método de envío continuo permite implementar actualizaciones adicionales entre ciclos cuando están listas. Las notas de la versión se actualizan según corresponda en la sección _Últimas actualizaciones_ y se menciona la fecha de disponibilidad. Todos los cambios publicados durante el mes se consolidan en las notas de la versión mensual en la fecha de publicación.


## Rutas de lanzamiento {#release-paths}

Las características de [!DNL Journey Optimizer] siguen diferentes rutas de lanzamiento según su complejidad, dependencias y ámbito. La plataforma utiliza varias etiquetas de disponibilidad (Beta, disponibilidad limitada, disponibilidad general), pero no todas las funciones pasan por todas ellas.

Las rutas comunes de las versiones incluyen:

* **Directo a GA**: algunas nuevas funcionalidades y mejoras van directamente a disponibilidad general (GA).
* **LA → GA**: algunas funciones están disponibles por primera vez para un público limitado (disponibilidad limitada, LA) antes del despliegue general.
* **Beta → LA → GA**: las funcionalidades más grandes o experimentales progresan por todas las fases para las pruebas y la validación.
* **Beta → GA**: algunas funciones estables Beta pueden pasar directamente a GA sin una fase intermedia LA.

>[!TIP]
>
> Si le interesa el acceso rápido a las funciones Beta o en disponibilidad limitada, póngase en contacto con su representante de Adobe para debatir las opciones de participación.


## Etiquetas de disponibilidad {#availability-labels}

La tabla siguiente describe cada etiqueta de disponibilidad utilizada en las rutas de versión, qué significa para el acceso y la asistencia, y qué esperar en cada fase.

| **Etiqueta** | **Finalidad** | **Disponibilidad** | **Notas clave** |
|------------|-------------|------------------|----------------|
| **Beta** | Pruebas rápidas y recopilación de comentarios. | Limitado a los clientes u organizaciones seleccionados que participan en el programa Beta de Adobe. | - No destinado al uso en producción.<br>- La funcionalidad o el diseño pueden cambiar antes de GA.<br>- Los comentarios ayudan a perfeccionar la implementación final. |
| **Disponibilidad limitada (LA)** | Despliegue controlado para la validación y la monitorización. | Habilitado solo para clientes o entornos seleccionados (por ejemplo, zonas protegidas de desarrollo). | - Listo para la producción y totalmente compatible.<br>- Se usa para validar el rendimiento y la escalabilidad antes del lanzamiento general.<br>- El acceso requiere la aprobación de Adobe. |
| **Disponibilidad general (GA)** | Lanzamiento general de funcionalidad totalmente compatible. | Habilitado de forma predeterminada para todas las organizaciones aptas. | - Listo para la producción y totalmente compatible.<br> - Pueden aplicarse licencias o derechos.<br> - Se puede implementar progresivamente en todas las regiones. |


## Despliegue y disponibilidad {#rollout}

Incluso después de un anuncio de GA, el despliegue puede ocurrir gradualmente entre organizaciones o regiones. Si una nueva funcionalidad no aparece inmediatamente en su entorno, normalmente estará disponible unos días después del lanzamiento.

Esta implementación gradual ayuda a Adobe a monitorizar la estabilidad, el rendimiento y la experiencia del usuario antes de completar la implementación.


## Mantenerse informado {#staying-informed}

Para mantenerse al día:

* Revise las [**últimas notas de la versión**](release-notes.md) para ver si hay funcionalidades nuevas y actualizadas.
* Consulte la sección **_Últimas actualizaciones_** entre las versiones mensuales para implementaciones en tiempo real.
* Monitorice las **Notas de la versión preliminar** (cuando estén disponibles) para obtener una vista previa de las próximas funciones.
* Póngase en contacto con su representante de Adobe para obtener información sobre el acceso o la asignación de derechos Beta o de disponibilidad limitada.

Puede suscribirse a **correos electrónicos y alertas internas del producto** para [!DNL Journey Optimizer] versiones de productos. Para suscribirse:

1. Vaya a **Preferencias de Adobe Experience Cloud**.
1. En **Notificaciones**, busque **Journey Optimizer**.
1. Habilite las notificaciones de **nuevas versiones** en la aplicación y por correo electrónico

![Panel de preferencias de notificaciones de Adobe Experience Cloud para Journey Optimizer, con notificaciones en la aplicación y por correo electrónico habilitadas para las categorías Alertas, Aprobaciones y Nuevas versiones](assets/do-not-localize/pulse-notif.png){width="70%"}

## Preguntas frecuentes {#faq}

A continuación encontrará las preguntas más frecuentes sobre el ciclo de lanzamiento de [!DNL Adobe Journey Optimizer].

¿Necesita más información? Use las opciones de comentarios situados en la parte inferior de esta página para plantear su pregunta o conecte con la [comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=es){target="_blank"}.

+++ ¿Cuándo están programadas las versiones de [!DNL Adobe Journey Optimizer]?

[!DNL Adobe Journey Optimizer] generalmente publica actualizaciones durante la última semana de cada mes. Al final de cada trimestre, la versión puede tardar hasta dos semanas en alinearse con las actualizaciones entre soluciones o en toda la plataforma.

+++

+++ ¿Por qué no veo una nueva función inmediatamente después de que se anuncie?

Algunas funciones de GA se implementan progresivamente para garantizar la estabilidad y el rendimiento de la plataforma. Si no ve una función de inmediato, aparecerá una vez que se haya completado la implementación para su región u organización.

+++

+++ ¿Cuál es la diferencia entre Beta, disponibilidad limitada y GA?

* **Beta**: fase de prueba rápida, acceso limitado, basado en comentarios.
* **Disponibilidad limitada (LA)**: despliegue controlado para la validación final.
* **Disponibilidad general (GA)**: versión completa para todos los clientes autorizados.

+++

+++ ¿Todas las funciones pasan por Beta y disponibilidad limitada?

No. Algunas funciones se publican directamente en GA o solo en LA, según su naturaleza y estado de preparación. La ruta de lanzamiento está adaptada a cada capacidad para equilibrar agilidad, calidad y estabilidad.

+++

+++ ¿Cómo puedo participar en los programas Beta o de disponibilidad limitada?

El acceso se realiza por invitación o solicitud a través de su representante de Adobe. La participación ayuda a dar forma al diseño de funciones y garantiza que los casos de uso se tengan en cuenta en la versión final.

+++

+++ ¿Con qué frecuencia se actualizan las notas de la versión?

Las notas de la versión se actualizan continuamente. Más allá de las versiones mensuales, la sección _Últimas actualizaciones_ se actualiza cada vez que se insertan nuevas funciones o mejoras en la producción.

+++
