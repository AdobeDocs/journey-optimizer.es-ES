---
solution: Journey Optimizer
product: journey optimizer
title: Prueba del recorrido
description: Descubra cómo simular su recorrido
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: comprobación, recorrido, comprobación, error, solución de problemas
version: Journey Orchestration
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: b858b41cf65ed28e229938102e0f44b369180da8
workflow-type: tm+mt
source-wordcount: '1858'
ht-degree: 1%

---

# Simulación del recorrido{#testing_the_journey}

>[!IMPORTANT]
>
> Esta capacidad está disponible para todos los clientes como disponibilidad limitada con funciones esenciales.

Puede establecer el recorrido en **[!UICONTROL Simulación]** además de **Borrador**, **Modo de prueba** y **Activo**. En Simulación, realiza pruebas con **usuarios simulados**: entidades temporales similares a un perfil que agrega, sin usar perfiles de prueba persistentes en Adobe Experience Platform.

Adobe Journey Optimizer ofrece dos formas de probar y validar el recorrido:

* **[Simulación](#test-users)**: usa la función de recorrido **[!UICONTROL Simulación]** y usuarios simulados para ejecuciones rápidas sin perfiles creados previamente en Adobe Experience Platform.

* **[Modo de prueba](testing-the-journey.md)**: Use perfiles persistentes marcados como perfiles de prueba en Adobe Experience Platform, reutilizables entre sesiones. Elija este método cuando necesite datos coherentes y predefinidos. [Aprenda a crear perfiles de prueba](../audience/creating-test-profiles.md).

Tenga en cuenta que la simulación de Recorrido está en **disponibilidad limitada**. Para compartir comentarios y ayudarnos a mejorar la experiencia, abre **[!UICONTROL Comentarios]** en la barra superior.

![menú de comentarios de Beta](assets/beta-feedback.png)

## Creación y administración de usuarios simulados {#test-users}

>[!IMPORTANT]
>
>Necesita el permiso **Simular recorridos** para acceder a la función **[!UICONTROL Simulación]**. [Más información](../administration/permissions.md)

Los usuarios simulados son entidades temporales similares a un perfil que usted define en **[!UICONTROL Configuración de simulación]**. En esta sección se explica cómo crearlos, desde la interfaz de usuario de o un archivo JSON, guardarlos para reutilizarlos, ajustarlos o eliminarlos de la lista y enviarlos al recorrido.

### Creación de usuarios simulados

Los siguientes pasos muestran cómo crear usuarios simulados desde la interfaz de usuario o importando un archivo JSON.

1. En el Recorrido, abre **[!UICONTROL Simular]** y elige **[!UICONTROL Simulación]**.

   ![Botón de modo de prueba en la interfaz de recorrido](assets/test-mode-simulated.png)

1. Haga clic en **[!UICONTROL Crear usuarios simulados]** para crear usuarios nuevos y seleccionar si desea crear usuarios desde la interfaz de usuario o importarlos desde JSON.

   Para reutilizar usuarios simulados en su lugar, haga clic en **[!UICONTROL Seleccionar usuarios simulados]** y elija las entradas que guardó anteriormente.

   ![Panel de selección de usuarios simulados](assets/simulate-2.png)

1. Si crea usuarios simulados a partir de JSON, actualice los campos correspondientes con los datos de usuario simulados.

1. Si crea usuarios simulados desde la interfaz de usuario, escriba un **[!UICONTROL Nombre para mostrar]** y una **[!UICONTROL Descripción]** para identificar a este usuario simulado. A continuación, seleccione los atributos del esquema de unión que desee rellenar para este usuario.

   ![Selección de atributos del esquema de unión](assets/simulate-3.png)

1. Haga clic en agregar **[!UICONTROL pertenencia a audiencias]** para simular las pertenencias a segmentos.

1. Haga clic en **[!UICONTROL Agregar perfil]** para crear varios usuarios simulados en una sola sesión.

1. Para cada usuario simulado que añadió en esta sesión, puede utilizar las siguientes acciones:

   * **[!UICONTROL Duplicate]**: Agrega un nuevo usuario simulado que replica la configuración completada de una entrada existente, entonces puede editar el duplicado según sea necesario.
   * **[!UICONTROL Aplicar a todo]**: propaga los valores o configuraciones de atributo de un usuario simulado a todos los demás usuarios simulados de la lista.
   * **[!UICONTROL Eliminar]**: quita de la lista al usuario simulado seleccionado.

1. Haga clic en **[!UICONTROL Guardar]** para almacenar uno o más usuarios simulados para uso futuro.

1. Después de guardar, los usuarios simulados que creó aparecen en la lista **[!UICONTROL Usuarios de prueba]**. Para cada entrada, abra el menú de opciones y seleccione una de las siguientes opciones:

   * ![Icono Editar](assets/do-not-localize/Smock_Edit_18_N.svg): Actualice los detalles del usuario simulado.
   * ![Icono de envío](assets/do-not-localize/Smock_Send_18_N.svg): ejecute la simulación solo para este usuario simulado.
   * ![Borrar icono](assets/do-not-localize/Smock_Close_18_N.svg): Quitar al usuario de esta lista. El usuario simulado no se elimina y permanece disponible en la selección Usuarios simulados.

   ![Panel de selección de usuarios simulados](assets/simulate-4.png)

1. Si el recorrido incluye una actividad **[!UICONTROL Wait]**, abra la pestaña **[!UICONTROL Test settings]** para ajustar el tiempo de espera durante la simulación.

1. Haga clic en **[!UICONTROL Enviar todo]** para enviar a la recorrido a todos los usuarios simulados de la lista. Aparece un mensaje de confirmación `Simulated users have been sent successfully.` cuando los usuarios simulados entran correctamente en el recorrido.

   ![Panel de selección de usuarios simulados](assets/simulate-5.png)

1. Acceda a la ficha **[!UICONTROL Resultados]** para abrir los resultados de la ejecución y revisar cómo se ejecutó cada paso. Para obtener más información, vea [Ver resultados](#viewing-logs).

Después de validar el recorrido en **[!UICONTROL Simulation]**, revise el registro de **[!UICONTROL Results]**. Si aparecen errores, deje **[!UICONTROL Simulation]**, aplique los cambios necesarios al recorrido y ejecute **[!UICONTROL Simulation]** de nuevo hasta que la ejecución parezca correcta. A continuación, puede publicar el recorrido. Ver [Publicar tu recorrido](../building-journeys/publish-journey.md).

### Seleccionar usuarios simulados

Los usuarios simulados que cree manualmente se almacenan y se pueden seleccionar de esta lista cuando la simulación está activada en otros recorridos.

1. Establezca el recorrido en **[!UICONTROL Simulación]**. Abra el punto de entrada **[!UICONTROL Simular]** y elija **[!UICONTROL Simulación]** para que el recorrido utilice la característica Simulación, por ejemplo, junto con el modo de prueba o Activo, según el espacio de trabajo.

   ![Botón de modo de prueba en la interfaz de recorrido](assets/test-mode-simulated.png)

1. En el panel **[!UICONTROL Ajustes de simulación]**, puede seleccionar usuarios simulados creados anteriormente haciendo clic en **[!UICONTROL Seleccionar usuarios simulados]**.

   ![Modo de prueba en la interfaz de recorrido](assets/simulate-11.png)

1. Seleccione de la lista de usuarios simulados que se crearon y guardaron anteriormente.

1. Una vez que haya seleccionado los usuarios simulados, ya estarán disponibles en la lista **[!UICONTROL Usuarios de prueba]**. En el menú de opciones, elija entre las siguientes opciones:

   * ![Editar icono](assets/do-not-localize/Smock_Edit_18_N.svg) para editar usuarios y cambiar sus detalles.
   * ![Enviar icono](assets/do-not-localize/Smock_Send_18_N.svg) para enviar la simulación a un solo usuario simulado.
   * ![Borrar icono](assets/do-not-localize/Smock_Close_18_N.svg) para borrar a los usuarios simulados de la lista. Tenga en cuenta que si lo borra no lo eliminará, aún puede seleccionarse de la lista Usuarios simulados.

   ![Panel de selección de usuarios simulados](assets/simulate-4.png)

1. Haga clic en **[!UICONTROL Enviar todo]** para enviar a la recorrido a todos los usuarios simulados de la lista. Aparece un mensaje de confirmación `Simulated users entered the journey successfully.` cuando los usuarios simulados entran correctamente en el recorrido.

   ![Panel de selección de usuarios simulados](assets/simulate-5.png)

1. Haga clic en **[!UICONTROL Mostrar registro]** para abrir el registro de ejecución y revisar cómo se ejecutó cada paso. Para obtener más información, vea [Ver resultados](#viewing-logs).

Después de validar el recorrido en **[!UICONTROL Simulation]**, revise el registro de **[!UICONTROL Results]**. Si aparecen errores, deje **[!UICONTROL Simulation]**, aplique los cambios necesarios al recorrido y ejecute **[!UICONTROL Simulation]** de nuevo hasta que la ejecución parezca correcta. A continuación, puede publicar el recorrido. Ver [Publicar tu recorrido](../building-journeys/publish-journey.md).

## Activación de eventos {#firing_events}

Si el recorrido incluye uno o más eventos, puede almacenarlos en déclencheur mientras Simulación está activa.

1. En **[!UICONTROL Seleccionar tipo de evento]**, seleccione el evento que se activará para esta simulación.

   ![Interfaz de configuración de eventos con campos y lista desplegable para la selección de eventos](assets/simulate-10.png)

1. Haga clic en ![Editar evento](assets/do-not-localize/Smock_Edit_18_N.svg) para ajustar el evento de este usuario simulado.

   ![Interfaz de configuración de eventos con campos y lista desplegable para la selección de eventos](assets/simulate-9.png)

1. En la lista desplegable de usuarios simulados, seleccione el usuario simulado y termine de configurar el evento y cómo se genera.

   ![Interfaz de configuración de eventos con campos y lista desplegable para la selección de eventos](assets/simulate-8.png)

1. Haga clic en **[!UICONTROL Déclencheur los eventos seleccionados]**.

   Aparece un mensaje de confirmación `Events triggered successfully` cuando los usuarios simulados entran correctamente en el recorrido.

1. Haga clic en **[!UICONTROL Mostrar registro]** para abrir el registro de ejecución y revisar cómo se ejecutó cada paso. Para obtener más información, vea [Ver resultados](#viewing-logs).

## Visualización de resultados {#viewing-logs}

La pestaña **[!UICONTROL Results]** le permite ver los resultados de la prueba. Utilice el selector de vista para elegir cómo examinar el registro:

* **Todos los usuarios simulados**: seleccione **[!UICONTROL Todos]** para ver los resultados agregados en todos los usuarios simulados de la ejecución. Esta vista le ayuda a analizar la simulación completa de un vistazo, la actividad, los resultados y los errores, sin necesidad de seleccionar primero un solo usuario simulado.

* **Un usuario simulado**: En la lista desplegable **[!UICONTROL Usuario de prueba]**, seleccione el usuario simulado cuya ejecución desee inspeccionar.

Para cada actividad, el &quot;log&quot; puede mostrar si el usuario que ha realizado la simulación ha entrado o salido del paso, así como los errores que se han producido durante la simulación.

![Registros para usuarios de prueba](assets/simulate-6.png)

Para las actividades **Wait**, el registro incluye dos valores relacionados con la duración:

* **Duración definida**: La duración especificada en la actividad **Esperar** para el recorrido publicado y aplicada una vez que el recorrido esté activo. El registro registra si la simulación aplica una anulación desde la configuración de la prueba, por ejemplo 10 segundos, en lugar de depender únicamente del valor definido en el recorrido.
* **Duración real**: El tiempo que el usuario simulado permaneció en la actividad **Esperar**. Este valor se establece desde la ficha **[!UICONTROL Configuración de pruebas]**.

Cuando aparezcan errores en el registro, deje **Simulation**, aplique los cambios necesarios al recorrido y ejecute **Simulation** de nuevo. Una vez completada la validación, publique el recorrido. Ver [Publicar tu recorrido](../building-journeys/publish-journey.md).

## Limitaciones {#limitations}

En esta versión, es posible que **[!UICONTROL Simulation]** no admita todas las actividades, canales o integraciones compatibles con **[!UICONTROL Test mode]** o un recorrido en directo, y que el comportamiento cambie a medida que la funcionalidad madure. Utilice los procedimientos de este artículo para ver los flujos de trabajo admitidos.

Consulte los menús desplegables siguientes para obtener más información sobre las limitaciones de la simulación.

+++ Restricciones de nivel de nodo

Si un recorrido contiene cualquiera de los siguientes nodos, no se puede iniciar en **[!UICONTROL Simulación]**. Para que la simulación pueda ejecutarse, debe modificarse el recorrido o eliminarse el nodo correspondiente.

| Nodo restringido | Notas |
| --- | --- |
| Eventos empresariales | Los recorridos que comienzan con un evento empresarial no se pueden ejecutar en **[!UICONTROL Simulación]**. |
| ID suplementario (reentrada múltiple) | La reentrada simultánea (varias instancias activas para el mismo usuario simulado) impide que se inicie **[!UICONTROL Simulation]**. |
| Nodo de decisión de contenido | Esta actividad debe eliminarse o cambiarse antes de poder simular el recorrido. |
| Búsqueda de conjuntos de datos | No se admiten las búsquedas de conjuntos de datos de clientes por clave; los recorridos que incluyen esta actividad no se pueden ejecutar en **[!UICONTROL Simulación]**. |
| Experimentación con rutas (Optimizar: variante de experimento) | No admitido en **[!UICONTROL Simulación]**. Puede seguir usando **[!UICONTROL Optimizar]** para flujos que solían estar bajo **[!UICONTROL Condición]** (por ejemplo, condiciones de origen de datos). |
| Segmentación de rutas (Optimizar, variante de regla de segmentación) | No admitido en **[!UICONTROL Simulación]**. |
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
| Relleno previo de eventos (solo en el navegador) | — | El rellenado previo de eventos solo se admite en el explorador. Los datos de evento precargados son específicos del explorador. |

+++
