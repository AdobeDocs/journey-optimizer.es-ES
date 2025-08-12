---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1f53a578e91cd26e0e062c20b371a344ad709a8f
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 47%

---

# Notas de versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).


## Notas previas al lanzamiento de agosto de 2025 {#25-8-rn}

**Las notas anteriores al lanzamiento que se indican a continuación están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión, en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de lanzamiento**: miércoles, 19 de agosto de 2025


### Nuevas funciones {#Aug-25-8-features}

<table>
<thead>
<tr>
<th><strong>Pausar y reanudar recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede poner en pausa y reanudar los recorridos. Esta funcionalidad proporciona a los profesionales del recorrido un mayor control y flexibilidad al permitir que los recorridos en directo se suspendan temporalmente sin interrumpir la experiencia del cliente. Cuando están en pausa, no se envían comunicaciones y los perfiles permanecen en estado suspendido hasta que se reanuda el recorrido.</p>
<p>Puede poner en pausa y reanudar solo un recorrido, o realizar pausas masivas y reanudar operaciones en un grupo de recorridos.</p>
<p>Además, puede aplicar filtros globales a los recorridos en pausa para excluir perfiles en función de sus atributos.</p>
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vista de calendario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una vista de calendario en las listas de recorridos y campañas. Permite visualizar todas las activaciones de recorridos y campañas en las listas respectivas.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, la función incluye:</p>
<ul>
<li>Mejoras de diseño para la navegación en fechas,</li>
<li>La capacidad de ver borradores de campañas si ha establecido una fecha de inicio y de finalización,</li>
<li>Una nueva configuración para ocultar y mostrar los elementos de calendario que se ejecutan durante mucho tiempo.</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modo oscuro en el Diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Diseñador de correo electrónico de Journey Optimizer ahora permite cambiar a la vista en modo oscuro, donde además puede definir configuraciones personalizadas específicas que se mostrarán solo para los destinatarios que lean sus correos electrónicos en modo oscuro.</p>
<p>Tenga en cuenta lo siguiente:</p>
<ul>
<li>El renderizado final del modo oscuro puede variar y depende del cliente de correo electrónico del destinatario.</li>
<li>No todos los clientes de correo electrónico admiten el modo oscuro personalizado. Además, algunos clientes de correo electrónico solo aplican su propio modo oscuro predeterminado a todos los correos electrónicos recibidos. En ambos casos, no se puede procesar la configuración personalizada que definió en el Diseñador de correo electrónico.</li>
</ul>
<P>Actualmente, esta función está en versión Beta y solo se encuentra disponible para los clientes de dicha versión. Para unirse al programa beta, póngase en contacto con su representante de Adobe.</p>
<p><!--img src="assets/do-not-localize/dark-mode.gif"/>--></p>
<p><!--For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Uso de datos de Adobe Experience Platform para la personalización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveche los datos de Adobe Experience Platform en el editor de personalización para personalizar su contenido. Para ello, los conjuntos de datos necesarios para la personalización de la búsqueda deben habilitarse primero mediante una llamada de la API. Cuando haya terminado, puede usar sus datos para personalizar su contenido en [!DNL Journey Optimizer].</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, se han introducido las siguientes mejoras:</p>
<ul>
<li>Compatibilidad con canales entrantes,</li>
<li>La función de ayuda "datasetLookup" ahora se puede utilizar dentro de la expresión y los fragmentos visuales para personalizar el contenido mediante datos de conjuntos de datos de Adobe Experience Platform,</li>
<li>Una opción del conjunto de datos ahora le permite habilitar conjuntos de datos para la personalización de la búsqueda, sin tener que realizar una llamada de API.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Use Decisioning en el canal de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede añadir directivas de Decisión a recorridos de correo electrónico y campañas. Las políticas de decisión son contenedores para sus ofertas que aprovechan el motor de Decisioning para devolver dinámicamente el mejor contenido para entregar a cada miembro del público.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formularios personalizados de página de aterrizaje</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le permite crear formularios personalizados y aprovecharlos en páginas de aterrizaje para capturar atributos de perfil en el conjunto de datos definido para cada formulario.</p>
<p>Actualmente, esta función está en versión Beta y solo se encuentra disponible para los clientes de dicha versión. Para unirse al programa beta, póngase en contacto con su representante de Adobe.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>optimización del recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le ofrece las herramientas necesarias para optimizar sus recorridos mediante el uso de la IA y los marcos de experimentación, a la vez que garantiza una facilidad de uso y una diferenciación perfectas entre las funcionalidades de optimización y condición.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### Mejoras {#Aug-25-8-improv}

A continuación, se describen las mejoras incluidas en esta versión.

- **Administración**
   - **Alertas de supervisión de configuración de canal**: ahora puede suscribirse para recibir alertas del sistema, ya sea por correo electrónico o en el centro de notificaciones de Journey Optimizer, en caso de que se produzca un error de configuración de canal o si falta un registro DNS.

- **Campañas**
   - **Control de tasa en campañas salientes**: ahora puede habilitar el control de tasa de regulación para campañas salientes (correo electrónico, SMS, notificaciones push), lo que le permite evitar sobrecargas en sistemas descendentes, como páginas de aterrizaje o plataformas de atención al cliente.
   - **Programación de campañas de acción**: los programadores de campañas diarias, semanales y mensuales se han actualizado para mejorar la granularidad. Por ejemplo, ahora puede establecer el número de semanas/meses entre programaciones, definir en qué día se va a ejecutar y decidir si se detiene después de un número específico de incidencias o en una fecha específica.

- **Canal - Push**
   - **Fecha de caducidad de la notificación push**: ahora puede especificar una fecha de caducidad para cada notificación push, lo que evita que los mensajes con distinción de tiempo (como la venta del Black Friday) se envíen después de una fecha determinada y, por lo tanto, evita ofrecer una mala experiencia a sus clientes.

- **Canal: correo electrónico**
   - **Archivos adjuntos de PDF a correos electrónicos**: ahora puede adjuntar archivos PDF estáticos a los mensajes de correo electrónico enviados con Journey Optimizer.

- **Configuración**
   - **Compatibilidad con dominios dinámicos**: Journey Optimizer ahora admite la personalización en las direcciones URL de seguimiento para los dominios predefinidos enumerados en el nivel de configuración de canal.
   - **Compatibilidad con atributos personalizados con la URL para cancelar la suscripción con un clic**: con Journey Optimizer, si administra el consentimiento fuera de Adobe, puede establecer un extremo personalizado externo definiendo su propio vínculo para cancelar la suscripción con un clic en la configuración del correo electrónico. Cuando los destinatarios hacen clic en el vínculo unsubscribe, Journey Optimizer añade algunos parámetros predeterminados específicos del perfil al evento de actualización de consentimiento.

     Para personalizar aún más el vínculo de cancelación de suscripción de un clic, ahora puede definir atributos personalizados que se adjuntarán al evento de consentimiento.

- **Recorridos**
   - **Actividad de acción en recorrido**: Journey Optimizer admite una nueva actividad de acción genérica que permite configurar acciones salientes de uno o varios canales, lo que permite una configuración de acciones optimizada dentro del lienzo de recorrido. Con esta nueva actividad, también puede añadir optimización de objetivos, experimentos y variantes de idiomas multilingües a cualquier acción de canal integrada.
   - **Operaciones masivas de Recorrido**: en la lista de recorridos, puede seleccionar varios elementos. Una vez seleccionados, puede pausar o reanudar hasta 10 recorridos a la vez.