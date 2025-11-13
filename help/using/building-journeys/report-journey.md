---
solution: Journey Optimizer
product: journey optimizer
title: Publicación del recorrido
description: Obtenga información sobre cómo informar sobre su recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 1%

---

# Informe en vivo en el lienzo de recorrido {#report-journey}

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


>[!MORELIKETHIS]
>
>* [Introducción a creación de informes](../reports/gs-reports.md)
>* [Publicar su recorrido](publish-journey.md)
>* [Recorrido en seco](journey-dry-run.md)
>* [Configura y realiza un seguimiento de tus métricas de recorridos](success-metrics.md)
>* [Informes de recorridos personalizados](../reports/sharing-overview.md)