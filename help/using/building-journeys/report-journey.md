---
solution: Journey Optimizer
product: journey optimizer
title: Publicación del recorrido
description: Obtenga información sobre cómo informar sobre su recorrido
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/pclOxVDnQikU-2nLYMJ8mqEog9QL4WZBC7-NbvhuzIg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1134
ht-degree: 0%

---

# Informe en vivo en el lienzo de recorrido {#report-journey}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a usar Live Reporting para monitorizar las métricas de recorrido clave de las últimas 24 horas directamente dentro del lienzo de recorrido.

>[!ENDSHADEBOX]

Una vez que se haya publicado el recorrido, [Modo de ejecución en seco](journey-dry-run.md) se activará y **Live Reporting** proporcionará métricas de las últimas 24 horas directamente en el lienzo del recorrido.


>[!AVAILABILITY]
>
>Si no puedes ver los datos en tu informe de recorrido activo, tus derechos de acceso deben ampliarse para incluir el permiso **[!UICONTROL Ver informe de recorridos]**. [Más información](../administration/permissions.md)


Los eventos mostrados se han producido en las últimas 24 horas, con un intervalo mínimo de dos minutos entre el evento y su visualización, normalmente en un plazo de cinco minutos.

![Tablero de informes en vivo de Recorrido que muestra métricas de rendimiento en tiempo real](assets/journey_live_report.png)

Para sus recorridos en el modo Activo o [Modo de ejecución en seco](journey-dry-run.md), puede comprobar:

* **[!UICONTROL Perfiles ingresados]**: Cantidad total de individuos que ingresaron al recorrido.
* **[!UICONTROL Perfiles abandonados]**: Número total de personas que salieron del recorrido (incluidos los errores).
* **[!UICONTROL Perfiles con error]**: Número total de personas que encontraron un error durante su recorrido.
* **[!UICONTROL Perfiles descartados]**: Número total de individuos que se descartaron de la recorrido por uno de los siguientes motivos:

   * Para las actividades de **Calificación de audiencias**, puede descartarse si el verbo esperado para la calificación de audiencia no coincide con el recorrido recibido (por ejemplo, &quot;saliente&quot; en lugar de &quot;realizado&quot;).
   * Para **recorridos activados por eventos**, puede ocurrir una descarte si el individuo intentó volver a entrar al recorrido demasiado pronto o cuando no se permitió la reentrada.
   * En **recorridos recurrentes**, se cuenta un descarte en cada periodicidad si el individuo ya está en el recorrido y la directiva de reentrada no está establecida en &quot;forzar reentrada&quot;.
   * En las actividades **Leer audiencia**, se produce un descarte si no se establece ninguna identidad para el individuo exportado o si el área de nombres de identidad recibida no coincide con la esperada para el recorrido.

Para cada actividad dentro de cada recorrido en Activo o [Modo de ejecución en seco](journey-dry-run.md), tiene acceso a:

* **[!UICONTROL Ingresado]**: Cantidad total de personas que ingresaron a esta actividad. Para las actividades **Action**, ya que no se ejecutan en el modo de ejecución en seco, esta métrica indica los perfiles que pasan.
* **[!UICONTROL Salidas (se cumplen los criterios de salida)]**: Número total de personas que salieron de la recorrido de esa actividad debido a criterios de salida (incluidos errores).
* **[!UICONTROL Salida forzada]**: Número total de personas que salieron del recorrido mientras estaba en pausa debido a una configuración del profesional del recorrido. Esta métrica siempre es igual a cero para los recorridos en el modo de ejecución en seco.
* **[!UICONTROL Error]**: Número total de personas que tuvieron un error en esa actividad.

## Solución de problemas de datos de informes faltantes {#troubleshooting-missing-data}

Si no ve los datos esperados en sus informes de recorrido, tenga en cuenta lo siguiente:

* **Sincronización de nombres de Recorrido**: compruebe que el nombre de recorrido de [!DNL Adobe Journey Optimizer] coincida con el nombre almacenado en el conjunto de datos de informes. Una discrepancia entre estos nombres puede impedir que los datos de los informes aparezcan correctamente.

* **Intervalo de actualización de datos**: después de actualizar el nombre o la configuración de un recorrido, deje tiempo suficiente para que se actualicen los datos. Los datos de creación de informes suelen aparecer en unos minutos, pero en algunos casos pueden tardar más.

* **Permisos de acceso**: Asegúrese de que dispone de los permisos necesarios para ver los informes de recorrido. Si no ve datos, comuníquese con el administrador para comprobar que tiene habilitado el permiso **[!UICONTROL Ver informe de recorridos]**. [Más información sobre los permisos](../administration/permissions.md)

* **Estado del Recorrido**: los datos del informe solo están disponibles para los recorridos publicados o los recorridos que se ejecutan en [Modo de ejecución en seco](journey-dry-run.md). Los recorridos de borrador no generan datos de informes.

Si los problemas persisten después de comprobar estos elementos, póngase en contacto con el administrador de Adobe o con el [soporte técnico de Adobe](../start/user-interface.md#support-ticket-guidelines) para obtener ayuda.

>[!MORELIKETHIS]
>
>* [Introducción a creación de informes](../reports/gs-reports.md)
>* [Publicar su recorrido](publish-journey.md)
>* [Recorrido en seco](journey-dry-run.md)
>* [Configura y realiza un seguimiento de tus métricas de recorridos](success-metrics.md)
>* [Informes de recorridos personalizados](../reports/sharing-overview.md)

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo ver e interpretar el informe en vivo incrustado en el lienzo de recorrido, que cubre las métricas de flujo de perfil clave disponibles para los recorridos y recorridos publicados en el modo de ejecución en seco.

**Intenciones:**
* Ver métricas de rendimiento de recorridos en tiempo real directamente en el lienzo de recorridos
* Recuentos de perfiles de Interpretación introducida, Salida, Error y Descartada para el recorrido y cada actividad
* Comprender por qué los perfiles se descartan de un recorrido
* Solución de problemas de datos inesperados o no presentes en los informes en directo de recorrido
* Compruebe el permiso necesario para acceder a los informes en directo del recorrido

**Glosario:**
* **Informes en vivo**: las métricas en tiempo real se mostraron directamente en el lienzo del recorrido durante las últimas 24 horas *(específicas del producto)*
* **Modo de ejecución en seco**: Modo de ejecución en recorrido que simula el recorrido sin enviar mensajes reales, en el que también está disponible la creación de informes en directo *(específico del producto)*
* **Perfiles descartados**: Perfiles que intentaron entrar al recorrido pero que fueron rechazados debido a diferencias de calificación, restricciones de reentrada o problemas de identidad *(específicos del producto)*
* **Salido (salida forzada)**: Perfiles que se quitaron del recorrido mientras un profesional del recorrido lo pausó; siempre cero en el modo de ejecución en seco *(específico del producto)*

**Protecciones:**
* Los datos del informe en directo solo abarcan las últimas 24 horas.
* Los eventos se muestran con un intervalo mínimo de dos minutos desde que se produjeron, normalmente en un plazo de cinco minutos.
* El permiso Ver informes de recorridos es necesario para ver los datos del informe activo.
* Los datos de informes solo están disponibles para los recorridos publicados o los recorridos en el modo de ejecución en seco; los recorridos de borrador no generan datos.
* Para las actividades de Acción, la métrica Introducida muestra los perfiles que pasan (no se ejecutan) en el modo de Ejecución en seco.
* La métrica Salida (salida forzada) siempre es cero en el modo de ejecución en seco.

**Terminología:**
* Nombre canónico: Informe en vivo (lienzo de recorrido) — Acrónimo: none — variantes: Informe en vivo de recorrido, Informe en lienzo
* Sinónimos: &quot;Perfiles introducidos&quot; = &quot;perfiles que ingresaron al recorrido&quot;
* No confunda: &quot;Informe en vivo&quot; ≠ &quot;Informe global de Recorrido&quot; (el informe en vivo son las últimas 24 horas en el lienzo; el informe global cubre un intervalo de tiempo histórico más amplio en la interfaz de usuario del informe)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Cuán actuales son los datos mostrados en el informe en vivo?** — Se muestran los eventos de las últimas 24 horas, con un retraso de visualización mínimo de dos minutos y, por lo general, en un plazo de cinco minutos.
* **Q: ¿Por qué no puedo ver ningún dato en mi informe de recorrido en vivo?** — Compruebe que tiene el permiso de informe Ver recorridos, que el recorrido está publicado (no en borrador) y que el nombre del recorrido coincide con el nombre del conjunto de datos de informes.
* **Q: ¿Qué causa que se descarten perfiles?** — Pueden producirse descartes debido a discrepancias de verbos de cualificación de audiencia, infracciones de directivas de reentrada en recorridos recurrentes o activados por eventos, o espacios de nombres de identidad que faltan o no coinciden en actividades de Leer audiencia.
* **Q: ¿Está disponible el informe en vivo durante el modo de ejecución en seco?** — Sí; los informes en directo están disponibles tanto para los recorridos publicados como para los recorridos que se ejecutan en el modo de ejecución en seco.
* **Q: ¿Qué significa la métrica Introducida para las actividades de Acción en el modo de ejecución en seco?** : indica los perfiles que pasan por la actividad, ya que las acciones no se ejecutan realmente en el modo de ejecución en seco.

+++
