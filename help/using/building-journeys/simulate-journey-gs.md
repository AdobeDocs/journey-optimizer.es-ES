---
solution: Journey Optimizer
product: journey optimizer
title: Simulación del recorrido
description: Descubra cómo simular su recorrido
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: comprobación, recorrido, comprobación, error, solución de problemas
version: Journey Orchestration
hide: true
feature_v2: []
subfeature_v2: []
source-git-commit: 62ae2ce8fc9eeea58a2f4028a34492276723e98a
workflow-type: tm+mt
source-wordcount: 1031
ht-degree: 2%

---

# Introducción a la simulación de Recorrido {#simulate-journey-gs}

Puede establecer el recorrido en **[!UICONTROL Simulación]** además de **Borrador**, **Modo de prueba** y **Activo**. En Simulación, realiza pruebas con **usuarios simulados**: entidades temporales similares a un perfil que agrega, sin usar perfiles de prueba persistentes en Adobe Experience Platform.

Adobe Journey Optimizer ofrece dos formas de probar y validar el recorrido:

* **[Simulación](#test-users)**: usa la función de recorrido **[!UICONTROL Simulación]** y usuarios simulados sin perfiles creados previamente en Adobe Experience Platform, que admiten usuarios con tecnología de IA y creados manualmente.

* **[Modo de prueba](testing-the-journey.md)**: Use perfiles persistentes marcados como perfiles de prueba en Adobe Experience Platform, reutilizables entre sesiones. Elija este método cuando necesite datos coherentes y predefinidos. [Aprenda a crear perfiles de prueba](../audience/creating-test-profiles.md).

## Simulación por tipo de recorrido {#by-journey-type}

El panel **[!UICONTROL Simulación]** solo muestra los pasos que necesita el recorrido. Eso depende de cómo entren los perfiles en el recorrido. A partir de estos factores, Adobe Journey Optimizer presenta diferentes experiencias de simulación. Expanda cada tipo siguiente para ver en qué se diferencia la ejecución y qué paneles utiliza.

Para obtener más información, consulta [Simular tu recorrido](simulate-journey.md).

+++ Recorrido por lotes con una audiencia de lectura

El recorrido se activó por una **audiencia de lectura**. El lienzo no tiene actividades de evento unitarias, los perfiles solo se mueven a través de condiciones, esperas y acciones de canal.

Con **recorrido por lotes con una audiencia de lectura**, puede acceder a la simulación rápida o a la simulación manual.

![Panel de simulación para un recorrido por lotes con solo lectura](assets/simulate-14.png)

+++

+++ Recorrido por lotes con una audiencia de lectura y eventos unitarios

Un recorrido de déclencheur de segmento que incluye uno o más eventos unitarios a lo largo de la ruta. Después de enviar usuarios en, almacene en déclencheur los eventos de los usuarios que esperan en un nodo de evento.

Con **recorrido por lotes con una audiencia de lectura y eventos unitarios**, puede acceder a la simulación rápida o a la simulación manual.

![Botón de modo de prueba en la interfaz de recorrido](assets/simulate-12.png)

+++

+++ Recorrido unitario

El recorrido **comienza** con un evento unitario, no con una audiencia de lectura. Un usuario simulado no entra en el recorrido hasta que se activa ese evento de inicio para ellos.

Con **recorrido unitario**, se accede directamente al menú de simulación Manual.

![Panel de simulación para un recorrido unitario](assets/simulate-13.png)

+++

## Simulación de lanzamiento {#launch}

Cambie el recorrido a **[!UICONTROL Simulation]** para probarlo con usuarios simulados. Las tareas paso a paso se detallan en [Simular el recorrido](simulate-journey.md).

1. En el recorrido, haz clic en **[!UICONTROL Simular]** y elige **[!UICONTROL Simulación]**.

   ![Botón de modo de prueba en la interfaz de recorrido](assets/test-mode-simulated.png)

1. Espere a que se complete la activación. Mientras el recorrido cambia a **[!UICONTROL Simulation]**, los controles del panel se desactivan y se vuelven a habilitar automáticamente una vez finalizada la activación.

## Limitaciones {#limitations}

En esta versión, es posible que **[!UICONTROL Simulation]** no admita todas las actividades, canales o integraciones compatibles con **[!UICONTROL Test mode]** o un recorrido en directo, y que el comportamiento cambie a medida que la funcionalidad madure. Utilice este artículo para ver los flujos de trabajo admitidos.

Consulte los menús desplegables siguientes para obtener más información sobre las limitaciones de la simulación.

+++ Restricciones de nivel de nodo

Si un recorrido contiene cualquiera de los siguientes nodos, no se puede iniciar en **[!UICONTROL Simulación]**. Para que la simulación pueda ejecutarse, debe modificarse el recorrido o eliminarse el nodo correspondiente.

| Nodo restringido | Notas |
| --- | --- |
| Eventos empresariales | Los recorridos que comienzan con un evento empresarial no se pueden ejecutar en **[!UICONTROL Simulación]**. |
| ID suplementario (reentrada múltiple) | La reentrada simultánea (varias instancias activas para el mismo usuario simulado) impide que se inicie **[!UICONTROL Simulation]**. |
| Nodo de decisión de contenido | Esta actividad debe eliminarse o cambiarse antes de poder simular el recorrido. |
| Búsqueda de conjuntos de datos | No se admiten las búsquedas de conjuntos de datos de clientes por clave; los recorridos que incluyen esta actividad no se pueden ejecutar en **[!UICONTROL Simulación]**. |
| Actividad **[!UICONTROL Optimizar]** | Los siguientes métodos de **[!UICONTROL Optimize]** no son compatibles con **[!UICONTROL Simulation]**: **[!UICONTROL Experimento]**, **[!UICONTROL Regla de segmentación]**, **[!UICONTROL División de porcentaje]**, **[!UICONTROL Condición de tiempo]**, **[!UICONTROL Condición]**, **[!UICONTROL Condición de fecha]**, **[!UICONTROL Límite de perfil]** y **[!UICONTROL Source de datos externos]**. Elimine o cambie el nodo antes de simular. |
| Enriquecimiento de atributos de audiencia externa | Los recorridos que usen atributos personalizados de orígenes de audiencia externos no se iniciarán en **[!UICONTROL Simulación]** cuando esta validación esté activa. |

+++

</br>

+++ Limitaciones funcionales

Las siguientes capacidades no son compatibles con **[!UICONTROL Simulación]**.

| Capacidad | Notas |
| --- | --- |
| Criterios de salida | Los criterios de salida no se aplican cuando ejecuta **[!UICONTROL Simulation]**. |
| [!DNL Adobe Journey Optimizer] decisiones dentro de una acción (por ejemplo, contenido de correo electrónico con Adobe Journey Optimizer decisioning) | No se generan las revisiones de acción para el contenido que usa la toma de decisiones [!DNL Adobe Journey Optimizer]. |
| Simular respuesta de acción personalizada | [!UICONTROL Las acciones personalizadas] realizan una llamada saliente real de forma predeterminada. No se admite la burla de la respuesta para que no se ejecute ninguna llamada externa. |
| Evaluación de directiva de consentimiento | El consentimiento no se puede burlar en el nivel de usuario simulado. |
| restricción y arbitraje de recorridos | No admitido en **[!UICONTROL Simulación]**. |
| Límite de frecuencia (por canal o tipo de comunicación) | No admitido en **[!UICONTROL Simulación]**. |
| Administración, supresión y listas de permitidos de la exclusión | Sigue la configuración de enrutamiento de mensajería donde se aplica. |
| Subdominio dinámico y atributos dinámicos en configuraciones de canal | Sigue la configuración de enrutamiento de mensajería donde se aplica. |
| Optimización del tiempo de envío (STO) | No admitido en **[!UICONTROL Simulación]**. |
| Herramientas para zonas protegidas (copie usuarios simulados en zonas protegidas) | No compatible. |
| Recorridos de envío de ondas | No compatible. |
| Horario silencioso | No compatible. |
| Administración, supresión y listas de permitidos de la exclusión | No compatible. |
| Subdominio dinámico y atributos dinámicos en configuraciones de canal | No compatible. |
| Privacy service | Los usuarios simulados no son perfiles persistentes compatibles con el RGPD. No incluya datos de clientes reales en usuarios simulados. |

+++

</br>

+++ Barreras cuantitativas 

Estas protecciones se aplican a **[!UICONTROL Simulación]**. Las mayúsculas numéricas se aplican en la interfaz de recorrido y durante la ejecución. Los límites pueden cambiar en una versión posterior; si se ejecuta cerca de un techo, compruebe el comportamiento en la zona protegida.

| Barrera | Límite | Notas |
| --- | --- | --- |
| Máximo de usuarios simulados que se pueden seleccionar y activar en un lote (recorridos por lotes, flujos activados por eventos y flujos de calificación de audiencia) | 20 | Se cuenta para cada **[!UICONTROL Enviar todos]** o **[!UICONTROL los eventos seleccionados del Déclencheur]**; no es un límite acumulado para todo el recorrido. |
| Número máximo de usuarios únicos simulados probados en una sola ejecución de simulación | 100 | Se está llegando a **100** usuarios únicos en un solo bloque de ejecución **[!UICONTROL Seleccione usuarios simulados]** para nuevos usuarios simulados. Si estás en **90**, puedes agregar **10** más antes del mismo bloque. |
| Máximo de recorridos que se pueden ejecutar en **[!UICONTROL Simulation]** al mismo tiempo en una zona protegida | 20 | El límite lo comparten todos los recorridos de **[!UICONTROL Simulación]** en esa zona protegida a la vez. |
| Máximo de usuarios simulados activos en una zona protegida | 2,000 | Máximo de usuarios simulados que pueden existir en la zona protegida al mismo tiempo. Adobe puede ajustar este límite en función de los comentarios de los clientes. |
| Relleno previo de eventos (solo en el navegador) | — | Solo puede rellenar previamente los campos de carga útil de evento en la IU de simulación basada en el explorador. Los valores rellenados previamente permanecen en ese explorador y no se sincronizan con otros exploradores, dispositivos o sesiones, por lo que puede ver diferentes datos de rellenado previo en cada lugar que pruebe. |

+++
