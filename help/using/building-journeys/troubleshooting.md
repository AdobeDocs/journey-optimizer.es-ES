---
solution: Journey Optimizer
product: journey optimizer
title: Solucionar errores antes de probar o publicar el recorrido
description: Obtenga información sobre cómo solucionar errores antes de probar o publicar el recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: solución de problemas, solución de problemas, recorrido, comprobación, errores
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 38%

---

# Solucionar errores antes de probar el recorrido {#troubleshooting}

En esta sección, aprenderá a solucionar problemas de recorridos antes de realizar pruebas o publicar. Todas las comprobaciones que se indican a continuación se pueden realizar cuando el recorrido está en modo de prueba o cuando el recorrido está activo. La recomendación es realizar todas las comprobaciones siguientes en el modo de prueba y luego proceder a la publicación. Obtenga más información acerca del modo de prueba en [esta página](../building-journeys/testing-the-journey.md).

Obtenga información sobre cómo solucionar problemas de eventos de recorrido, comprobar si los perfiles ingresaron al recorrido, cómo navegan por él y si los mensajes se envían [en esta página](troubleshooting-execution.md).

Si usa acciones entrantes, aprenda a solucionarlas [en esta página](troubleshooting-inbound.md).

## Errores en las actividades {#activity-errors}

Antes de probar y publicar el recorrido, compruebe que todas las actividades estén correctamente configuradas. No puede realizar pruebas ni publicaciones si el sistema sigue detectando errores.

Los errores aparecen con un símbolo de advertencia en las mismas actividades del lienzo. Coloque el cursor en el signo de exclamación para mostrar el mensaje de error. Si selecciona la actividad, debería ver la línea por error con una advertencia. Por ejemplo:

* si un campo obligatorio está vacío, se mostrará un error

  ![Errores de validación de Recorrido mostrados en lienzo con indicadores de error](assets/journey63.png)

* en el lienzo, cuando se desconectan dos actividades, se muestra una advertencia

  ![Icono de advertencia que muestra actividades desconectadas en el lienzo del recorrido](assets/canvas-disconnected.png)

## Errores en el recorrido {#canvas-errors}

Los errores también se pueden ver desde el botón **[!UICONTROL Alertas]** situado sobre el lienzo. Este botón permite ver los errores detectados por el sistema y que impiden la activación del modo de prueba o la publicación del recorrido.

El sistema detecta dos tipos de problemas: **errores** y **advertencias**. Los errores bloquean la publicación y la activación de prueba. Las advertencias indican posibles problemas que no bloquean la activación o publicación de pruebas. Verá una descripción de la publicación y un ID de registro de la publicación del tipo ERR_XXX_XXX. Esto puede ayudar a identificar el problema.

![Indicadores de error y advertencia en recorrido con información sobre herramientas de descripción](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

Los errores y las advertencias que son globales para el recorrido aparecen primero en la lista. Los errores y las advertencias relacionados con actividades específicas se enumeran después, por orden de actividad o por su apariencia en el recorrido de izquierda a derecha. En la parte inferior de la lista de alertas, el botón **[!UICONTROL Copiar detalles]** le permite copiar información técnica sobre el recorrido que resulta útil para solucionar los problemas.

## Añadir una ruta alternativa {#canvas-add-path}

Puede definir una acción de reserva en caso de error en las siguientes actividades de recorrido: **[!UICONTROL Optimizar]** y **[!UICONTROL Acción]**.

Cuando se produce un error en una acción o condición, se detiene el recorrido de un individuo. La única manera de continuar es resolver el problema. Para evitar interrumpir el recorrido, también puede marcar la opción **[!UICONTROL Agregar una ruta alternativa en caso de tiempo de espera o error]** en las propiedades de la actividad. Obtenga más información en [esta sección](../building-journeys/using-the-journey-designer.md#paths).
