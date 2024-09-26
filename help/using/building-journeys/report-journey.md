---
solution: Journey Optimizer
product: journey optimizer
title: Publish el recorrido
description: Obtenga información sobre cómo informar sobre su recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
source-git-commit: 0cdf61bc97baaa8df08822d62a5b9f658c44c117
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Informe en vivo en el lienzo de recorrido {#report-journey}

>[!NOTE]
>
>Si no puedes ver los datos en tu informe de recorrido activo, tus derechos de acceso deben ampliarse para incluir el permiso **[!UICONTROL Ver informe de recorridos]**. [Más información](../administration/permissions.md)

Una vez publicado el recorrido, **Informes en vivo** proporciona métricas de las últimas 24 horas, directamente en el lienzo del recorrido.

Los eventos mostrados se han producido en las últimas 24 horas, con un intervalo mínimo de dos minutos entre el evento y su visualización, normalmente en un plazo de cinco minutos.

![](assets/journey_live_report.png)

Para su recorrido en directo, tiene acceso a:

* **[!UICONTROL Perfiles ingresados]**: Cantidad total de individuos que ingresaron a esta actividad.
* **[!UICONTROL Perfil saliente]**: Número total de individuos que salieron del recorrido de esa actividad debido a criterios de salida.
* **[!UICONTROL Perfiles con error]**: Número total de personas que encontraron un error durante su recorrido.
* **[!UICONTROL Perfiles descartados]**: Número total de individuos que se descartaron de la recorrido por uno de los siguientes motivos:

   * Para las actividades de **Calificación de audiencias**, puede descartarse si el verbo esperado para la calificación de audiencia no coincide con el recorrido recibido (por ejemplo, &quot;saliente&quot; en lugar de &quot;realizado&quot;).
   * Para **recorridos activados por eventos**, puede ocurrir una descarte si el individuo intentó volver a entrar en el recorrido demasiado pronto o cuando no se permitió la reentrada.
   * En **recorridos recurrentes**, se cuenta un descarte en cada periodicidad si el individuo ya está en el recorrido y la directiva de reentrada no está establecida en &quot;forzar reentrada&quot;.
   * En las actividades **Leer audiencia**, se produce un descarte si no se establece ninguna identidad para el individuo exportado o si el área de nombres de identidad recibida no coincide con la esperada para el recorrido.

Para cada actividad dentro de cada recorrido activo, tiene acceso a:

* **[!UICONTROL Perfiles ingresados]**: Cantidad total de individuos que ingresaron a esta actividad.
* **[!UICONTROL Perfil saliente]**: Número total de individuos que salieron del recorrido de esa actividad debido a criterios de salida.
* **[!UICONTROL Error]**: Número total de personas que tuvieron un error en esa actividad.
