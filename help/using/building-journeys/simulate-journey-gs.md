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
feature_v2: []
subfeature_v2: []
source-git-commit: df6d5f7137a3914daf545746aff559ca0d04539d
workflow-type: tm+mt
source-wordcount: 1507
ht-degree: 2%

---

# Introducción a la simulación de Recorrido {#simulate-journey-gs}

>[!BEGINSHADEBOX]

**En esta página:** Descubra cómo la simulación de recorrido le permite realizar pruebas con usuarios simulados y cómo varía la experiencia de simulación en función del tipo de recorrido antes de publicar.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>* Para usar **[!UICONTROL Simulation]**, asigne al menos un permiso de la funcionalidad **[!UICONTROL Recorrido]**: **Simular recorridos**, **Publicar recorridos** o **Aprobar y publicar recorridos**. Los mismos permisos le permiten crear y administrar usuarios simulados; los permisos de **[!UICONTROL Usuarios simulados]** no son necesarios. [Más información](../administration/permissions.md)
>
>* Para administrar usuarios simulados sin **[!UICONTROL Simulation]**, asigne a **Administrar usuarios simulados** o **Ver usuarios simulados** desde la funcionalidad **[!UICONTROL Simulated Users]**.
>
>* Para IA en simulación (**[!UICONTROL Simulación rápida]**, usuarios generados por IA, **[!UICONTROL Generar valores de evento]**), asigne **[!UICONTROL Generar contenido]** desde la capacidad **[!UICONTROL Asistente de IA]**.

Puede establecer el recorrido en **[!UICONTROL Simulación]** además de **Borrador**, **Modo de prueba** y **Activo**. En Simulación, realiza pruebas con **usuarios simulados**: entidades temporales similares a un perfil que agrega, sin usar perfiles de prueba persistentes en Adobe Experience Platform.

Adobe Journey Optimizer ofrece dos formas de probar y validar el recorrido:

* **[Simulación](simulate-journey.md#test-users)**: usa la función de recorrido **[!UICONTROL Simulación]** y usuarios simulados sin perfiles creados previamente en Adobe Experience Platform, que admiten usuarios con tecnología de IA y creados manualmente.

* **[Modo de prueba](testing-the-journey.md)**: Use perfiles persistentes marcados como perfiles de prueba en Adobe Experience Platform, reutilizables entre sesiones. Elija este método cuando necesite datos coherentes y predefinidos. [Aprenda a crear perfiles de prueba](../audience/creating-test-profiles.md).

## Simulación por tipo de recorrido {#by-journey-type}

El panel **[!UICONTROL Simulación]** solo muestra los pasos que necesita el recorrido. Eso depende de cómo entren los perfiles en el recorrido. A partir de estos factores, Adobe Journey Optimizer presenta diferentes experiencias de simulación. Expanda cada tipo siguiente para ver en qué se diferencia la ejecución y qué paneles utiliza.

Para obtener más información, consulta [Simular tu recorrido](simulate-journey.md).

+++ Recorrido por lotes con audiencia de lectura


El recorrido se activa por una **[!UICONTROL audiencia de lectura]** y el lienzo no tiene actividades de evento unitarias. Durante la simulación, la población de audiencia no se activa. Solo los usuarios simulados entran en el recorrido.
Los usuarios simulados seleccionados para la simulación aparecen en la sección **Usuarios de prueba**:

![Panel de simulación para un recorrido por lotes con solo lectura](assets/simulate-batch.png)

+++

+++ Recorrido por lotes con una audiencia de lectura y eventos unitarios

Un recorrido de déclencheur de segmento que incluye uno o más eventos unitarios a lo largo de la ruta. Primero almacene en déclencheur a los usuarios simulados para que entren en la simulación y, a continuación, almacene en déclencheur los eventos de los usuarios que esperan en un nodo de evento.
Los usuarios simulados seleccionados para la simulación y los eventos configurados se pueden ver respectivamente en las secciones Usuarios de prueba y Eventos de prueba. La sección Eventos de prueba no estará visible hasta que un usuario simulado entre en el recorrido.

![Panel de simulación para un recorrido por lotes con solo lectura](assets/simulate-batch-2.png)

+++

+++ Recorrido unitario

El recorrido comienza con un evento unitario, no con una audiencia de lectura. Un usuario simulado no entra en el recorrido hasta que se activa ese evento de inicio para ellos.
Los usuarios simulados seleccionados para la simulación y los eventos configurados serán visibles respectivamente en las secciones **Usuarios de prueba** y **Eventos de prueba**. La sección **Usuarios de prueba** no incluye una acción para almacenar en déclencheur a un usuario simulado en el recorrido. La entrada de déclencheur de **eventos de prueba**.

![Panel de simulación para un recorrido por lotes con solo lectura](assets/simulate-batch-3.png)

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

Algunos nodos impiden que **[!UICONTROL Simulation]** se inicie. Otros se ejecutan en simulación con el comportamiento descrito a continuación. Cuando se deba quitar o cambiar un nodo antes de simular, actualice primero el recorrido.

| Nodo restringido | Notas |
| --- | --- |
| Eventos empresariales | No se pueden ejecutar recorridos que comiencen con un evento empresarial en **[!UICONTROL Simulación]**. |
| ID suplementario (reentrada múltiple) | **[!UICONTROL La simulación]** no se inicia cuando se habilita la reentrada múltiple y el mismo usuario simulado podría tener varias instancias activas a la vez. |
| Nodo de decisión de contenido | Elimine o cambie esta actividad antes de simular el recorrido. |
| Búsqueda de conjuntos de datos | **[!UICONTROL La simulación]** no admite búsquedas de conjuntos de datos de clientes por clave. Elimine o cambie esta actividad antes de ejecutar una simulación. |
| Actividad **[!UICONTROL Optimizar]** | **[!UICONTROL Experimento]** y **[!UICONTROL Regla de segmentación]** no son compatibles. Elimine o cambie el nodo antes de simular.<br><br>Otros métodos **[!UICONTROL Optimize]** se comportan de la siguiente manera:<br><br>**[!UICONTROL División porcentual ]**: Journey Agent crea un usuario simulado por rama, no según los porcentajes de rama. Durante el tiempo de ejecución, la evaluación en directo selecciona la rama y puede diferir de la ruta generada. No puede burlarse de una elección de rama. Para dirigir a los usuarios, confíe en el orden de ramas en el lienzo. Siempre se elige la rama superior.<br><br>**[!UICONTROL Condición de tiempo]**: las condiciones se aplican durante la ejecución como en un recorrido activo. Por ejemplo, una ventana de 8:00 a 20:00 solo permite a los usuarios pasar mientras la simulación se ejecuta dentro de esa ventana. No se puede burlar del tiempo de ejecución. Configure la condición para que coincida con la hora actual cuando realice la prueba.<br><br>**[!UICONTROL Condición de fecha ]**: las condiciones se aplican durante la ejecución como en un recorrido activo. Por ejemplo, una fecha del 8 de junio de 2026 solo permite a los usuarios pasar cuando la simulación se ejecuta en esa fecha. No se puede burlar la fecha de ejecución. Establezca la condición en la fecha actual cuando realice la prueba.<br><br>**[!UICONTROL Límite de perfil]**: No se aplican límites durante la simulación. Journey Agent crea un usuario simulado por rama. No puede burlarse de una elección de rama. Para dirigir a los usuarios, confíe en el orden de ramas en el lienzo. Siempre se elige la rama superior. |
| Ramas de tiempo de espera y error | Journey Agent no genera usuarios para el tiempo de espera de la actividad ni para las ramas de error. Los usuarios solo introducen esas rutas si se produce un tiempo de espera o error real durante la simulación. |
| Rama de tiempo de espera (actividades de evento) | Se crean usuarios simulados, pero en **[!UICONTROL simulación manual]** Journey Agent no decide quién entra en una rama de tiempo de espera de evento. Controle la ruta enviando o no enviando el evento. Por ejemplo, para probar una rama de tiempo de espera, espere al tiempo de espera configurado y no envíe el evento. **[!UICONTROL Simulación rápida]** puede enviar o retener eventos automáticamente para cubrir las ramas de tiempo de espera. |
| Eventos de reacción | Los eventos de reacción se ejecutan en simulación, pero la acción debe ocurrir en la vida real. Por ejemplo, una reacción de correo electrónico **open** requiere que se abra el mensaje de prueba. No se pueden burlar de las reacciones en la IU de simulación. |
| Fuentes de datos externas | Las llamadas de se ejecutan durante la simulación del mismo modo que en un recorrido activo. Las actividades descendentes pueden utilizar la respuesta, pero no se puede burlar de ella. Cuando un valor de respuesta alimenta una actividad **[!UICONTROL Optimize]**, Journey Agent no puede inventar ese resultado. Solo genera entradas para la llamada de. Por ejemplo, si una llamada toma una ciudad de perfil y devuelve el tiempo, el agente establece una ciudad en el usuario simulado y la llamada en directo devuelve el tiempo. |
| Acciones personalizadas | El comportamiento coincide con las fuentes de datos externas. Las llamadas salientes son reales. El Journey Agent rellena las entradas. Los resultados provienen de la respuesta en directo. No puedes burlarte de las respuestas. |
| Enriquecimiento de atributos de audiencia externa | Los recorridos que usan atributos personalizados de orígenes de audiencia externos no se inician en **[!UICONTROL Simulación]** cuando se aplica esta validación. |

+++

</br>

+++ Limitaciones funcionales

Las siguientes capacidades no son compatibles con **[!UICONTROL Simulación]**.

| Capacidad | Notas |
| --- | --- |
| Criterios de salida | Los criterios de salida no se aplican cuando ejecuta **[!UICONTROL Simulation]**. |
| [!DNL Adobe Journey Optimizer] toma de decisiones dentro de una acción como, por ejemplo, contenido de correo electrónico con Adobe Journey Optimizer Decisioning | No se generan las revisiones de acción para el contenido que usa la toma de decisiones [!DNL Adobe Journey Optimizer]. |
| Simular respuesta de acción personalizada | [!UICONTROL Las acciones personalizadas] realizan una llamada saliente real de forma predeterminada. No se admite la burla de la respuesta para que no se ejecute ninguna llamada externa. |
| Evaluación de directiva de consentimiento | El consentimiento no se puede burlar en el nivel de usuario simulado y las políticas de consentimiento no se evalúan durante la simulación. |
| restricción y arbitraje de recorridos | No se evalúa ni se aplica durante la simulación. |
| Límite de frecuencia (por canal o tipo de comunicación) | No se evalúa ni se aplica durante la simulación. |
| Administración, supresión y listas de permitidos de la exclusión | No evaluado ni aplicado durante la simulación. |
| Subdominio dinámico y atributos dinámicos en configuraciones de canal | No compatible. |
| Optimización del tiempo de envío (STO) | No evaluado ni aplicado durante la simulación. |
| Herramientas para zonas protegidas (copie usuarios simulados en zonas protegidas) | No compatible. |
| Recorridos de envío de ondas | No compatible. |
| Horario silencioso | No evaluado ni aplicado durante la simulación. |
| Privacy service | Los usuarios simulados no son perfiles persistentes compatibles con el RGPD. No incluya datos de clientes reales en usuarios simulados. |

+++

</br>

+++ Barreras cuantitativas 

Estas protecciones se aplican a **[!UICONTROL Simulación]**. Las mayúsculas numéricas se aplican en la interfaz de recorrido y durante la ejecución. Los límites pueden cambiar en una versión posterior. Si corre cerca de un techo, verifique el comportamiento en su zona protegida.

| Barrera | Límite | Notas |
| --- | --- | --- |
| Máximo de usuarios simulados que se pueden seleccionar y activar en un lote (recorridos por lotes, flujos activados por eventos y flujos de calificación de audiencia) | 20 | Se cuenta para cada **[!UICONTROL Enviar todos]** o **[!UICONTROL los eventos seleccionados del Déclencheur]**, no un límite acumulado para todo el recorrido. |
| Máximo de usuarios simulados por solicitud de generación | 50 | Máximo de usuarios simulados que Journey Agent genera en una solicitud mediante **[!UICONTROL Simulación rápida]** o **[!UICONTROL Generación con IA]** en **[!UICONTROL Simulación manual]**. Si el recorrido tiene más de **50** rutas, Journey Agent selecciona aleatoriamente las rutas para producir esos **50** usuarios simulados. |
| Número máximo de usuarios únicos simulados probados en una sola ejecución de simulación | 100 | Se está llegando a **100** usuarios únicos en un solo bloque de ejecución **[!UICONTROL Seleccione usuarios simulados]** para nuevos usuarios simulados. Si estás en **90**, puedes agregar **10** más antes del mismo bloque. |
| Máximo de recorridos que se pueden ejecutar en **[!UICONTROL Simulation]** al mismo tiempo en una zona protegida | 20 | El límite lo comparten todos los recorridos de **[!UICONTROL Simulación]** en esa zona protegida a la vez. |
| Máximo de usuarios simulados activos en una zona protegida | 2,000 | Máximo de usuarios simulados que pueden existir en la zona protegida al mismo tiempo. Adobe puede ajustar este límite en función de los comentarios de los clientes. |
| Relleno previo de eventos (solo en el navegador) | — | Solo puede rellenar previamente los campos de carga útil de evento en la IU de simulación basada en el explorador. Los valores rellenados previamente permanecen en ese explorador y no se sincronizan con otros exploradores, dispositivos o sesiones, por lo que puede ver diferentes datos de rellenado previo en cada lugar que pruebe. |

+++
