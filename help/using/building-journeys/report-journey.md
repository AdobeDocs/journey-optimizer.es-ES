---
solution: Journey Optimizer
product: journey optimizer
title: Publicar el recorrido
description: Obtenga información sobre cómo informar sobre su recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
source-git-commit: b604ab6d94f414b96378f15986edbcf92cee77dc
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 1%

---

# Informe en vivo en el lienzo de recorrido {#report-journey}

>[!NOTE]
>
>Si no puedes ver los datos en tu informe de recorrido activo, tus derechos de acceso deben ampliarse para incluir el permiso **[!UICONTROL Ver informe de recorridos]**. [Más información](../administration/permissions.md)

Una vez publicado el recorrido, **Informes en vivo** proporciona métricas de las últimas 24 horas, directamente en el lienzo del recorrido.

Los eventos mostrados se han producido en las últimas 24 horas, con un intervalo mínimo de dos minutos entre el evento y su visualización, normalmente en un plazo de cinco minutos.

![](assets/journey_live_report.png)

Para su recorrido en directo, tiene acceso a:

* **[!UICONTROL Perfiles ingresados]**: Cantidad total de individuos que ingresaron al recorrido.
* **[!UICONTROL Perfiles abandonados]**: Número total de personas que salieron del recorrido (incluidos los errores).
* **[!UICONTROL Perfiles con error]**: Número total de personas que encontraron un error durante su recorrido.
* **[!UICONTROL Perfiles descartados]**: Número total de individuos que se descartaron de la recorrido por uno de los siguientes motivos:

   * Para las actividades de **Calificación de audiencias**, puede descartarse si el verbo esperado para la calificación de audiencia no coincide con el recorrido recibido (por ejemplo, &quot;saliente&quot; en lugar de &quot;realizado&quot;).
   * Para **recorridos activados por eventos**, puede ocurrir una descarte si el individuo intentó volver a entrar al recorrido demasiado pronto o cuando no se permitió la reentrada.
   * En **recorridos recurrentes**, se cuenta un descarte en cada periodicidad si el individuo ya está en el recorrido y la directiva de reentrada no está establecida en &quot;forzar reentrada&quot;.
   * En las actividades **Leer audiencia**, se produce un descarte si no se establece ninguna identidad para el individuo exportado o si el área de nombres de identidad recibida no coincide con la esperada para el recorrido.

Para cada actividad dentro de cada recorrido activo, tiene acceso a:

* **[!UICONTROL Ingresado]**: Cantidad total de personas que ingresaron a esta actividad.
* **[!UICONTROL Salidas (se cumplen los criterios de salida)]**: Número total de personas que salieron del recorrido de esa actividad debido a un criterio de salida.
* **[!UICONTROL Error]**: Número total de personas que tuvieron un error en esa actividad.
