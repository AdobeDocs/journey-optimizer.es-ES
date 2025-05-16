---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión preliminar
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 264927ba06ccb8cb1c7e7709e8fef053c1b37608
workflow-type: tm+mt
source-wordcount: '1554'
ht-degree: 23%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.


## Notas de la versión anteriores de mayo de 2025 {#25-5-rn}


**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en la fecha de la versión.

**Fecha de la versión**: 20-21 de mayo de 2025


### Nuevas funciones {#25-04-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Sincronizar programación de lectura de audiencia con trabajo de segmentación por lotes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede almacenar en déclencheur las ejecuciones de recorridos diarias después de la finalización de la segmentación por lotes. Esta opción ahora está disponible en recorridos programados diariamente para todos los clientes. Permite definir para una ventana de tiempo de hasta 6 horas a la espera de datos de audiencia de trabajos de segmentación por lotes, lo que garantiza que los recorridos se ejecuten con los datos más actualizados o se omitan si no están listos.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning: nuevo generador de fórmulas de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear fórmulas de clasificación de toma de decisiones específicas al definir y combinar criterios a partir de una nueva interfaz mejorada. En lugar de depender únicamente de una prioridad de oferta estática, puede definir fórmulas de clasificación personalizadas que combinen puntuaciones del modelo de IA, prioridades de oferta, atributos de perfil, atributos de oferta y señales contextuales a través de una interfaz guiada.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Para obtener más información, consulte la <a href="../experience-decisioning/exd-ranking-formulas.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: jueves, 14 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de fragmentos de contenido de Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con la integración de Adobe Experience Manager y Adobe Journey Optimizer, ahora puede utilizar sin esfuerzo fragmentos de contenido de Adobe Experience Manager dentro de su contenido de Journey Optimizer. Esta conexión perfecta facilita el acceso y el uso del contenido de AEM directamente en Journey Optimizer.</p>
<p>Esta capacidad, que antes estaba disponible para un conjunto limitado de organizaciones (LA), ahora es GA con las siguientes mejoras:</p>
<ul>
<li>Cree ofertas seleccionando directamente un fragmento de contenido de AEM.</li>
<li>Defina los marcadores de posición y asigne los valores de personalización dentro de la firma del fragmento con el modo Editor.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vista de calendario para el inventario de campañas y Recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una vista de calendario en las listas de recorridos y campañas. Permite visualizar todas las activaciones de recorridos y campañas en las listas respectivas.</p>
<p>Este cambio solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de Dynamic Media de Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los recursos de Dynamic Media ahora están disponibles y son accesibles directamente en Journey Optimizer. Esta actividad le permite lo siguiente:</p>
<ul>
<li>Administre los recursos de forma centralizada con actualizaciones en tiempo real.</li>
<li>Modifique la configuración de los recursos, como la anchura y la altura, instantáneamente.</li>
<li>Personalice las plantillas de Dynamic Media actualizando el contenido y añadiendo campos de personalización.</li>
</ul>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas en el Designer de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar rápidamente temas preaprobados para garantizar la coherencia de la marca en todos los correos electrónicos, acelerar el proceso de creación de campañas y producir correos electrónicos de alta calidad de forma independiente, al tiempo que reduce la dependencia en los equipos de diseño.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Actualmente, esta función está en versión beta y solo se encuentra disponible para los clientes de dicha versión. Para unirse al programa beta, póngase en contacto con su representante de Adobe.</p>
<p>Fecha de disponibilidad: jueves, 14 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflicto y priorización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En Journey Optimizer, la administración del volumen y la sincronización de las campañas y los recorridos tiene vital importancia, ya que reducen las interacciones para los clientes. Journey Optimizer ahora ofrece varias herramientas para la administración de conflictos y la priorización (antes disponibles solo para organizaciones de acceso limitado (LA)) que ahora están disponibles de forma general (GA).</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de General Availability, se han introducido las siguientes mejoras:</p>
<ul>
<li>Compatibilidad ampliada: las herramientas de administración de conflictos ahora admiten Recorridos unitarios y Recorridos de calificación de audiencias, además de recorridos de audiencia de lectura.</li>
<li>Solución de problemas mejorada: ahora hay dos nuevos campos de evento de paso disponibles en el servicio de consultas, lo que permite analizar por qué se rechazó un perfil de un recorrido o una campaña.</li>
<li>Informes mejorados: ahora los informes indican qué regla específica excluyó un perfil de un recorrido o campaña, lo que proporciona una mayor transparencia y perspectivas procesables.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simular variaciones de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente disponible en la versión Beta, ahora la simulación de variaciones de contenido ya está disponible de forma general (GA). Le permite obtener una vista previa de diferentes variaciones del contenido usando los datos de entrada de muestra cargados desde un archivo CSV o JSON o añadidos manualmente. El sistema detecta automáticamente todos los atributos utilizados en el contenido para la personalización y los puede utilizar en las pruebas para crear varias variantes.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de Disponibilidad general, la función ahora es compatible con experimentos de contenido y contenido multilingües, lo que le permite probar variaciones en diferentes idiomas y tratamientos. Además, ahora admite atributos contextuales (además de los atributos de perfil), lo que permite realizar pruebas de contenido aún más dinámicas y adaptadas a cada situación.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Escalar el ganador de la experimentación</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Escalar el ganador permite desplegar automática o manualmente la variación ganadora de un experimento para toda la audiencia. Esta función garantiza que, una vez que se identifique a un usuario de mayor rendimiento, pueda maximizar su alcance y eficacia sin una supervisión manual constante.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Proveedor de SMS personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le permite configurar proveedores de SMS adicionales más allá de las opciones predeterminadas: Sinch, Infobip y Twilio. Con la configuración personalizada del proveedor de SMS, puede integrar proveedores de terceros directamente, aprovechar la personalización avanzada de la carga útil para la mensajería dinámica y administrar las preferencias de consentimiento (inclusión/exclusión) para garantizar el cumplimiento.</p>
<p>Para obtener más información, consulte la <a href="../sms/sms-configuration-custom.md">documentación detallada</a>.</p></td>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisiones de contenido en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede agregar ofertas a sus recorridos a través de una acción de toma de decisiones específica en el lienzo de recorrido y utilizarlas en sus acciones personalizadas.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>ID suplementario para recorridos activados por eventos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede almacenar en déclencheur los recorridos utilizando un ID de perfil junto con otro identificador, como un ID de pedido, un ID de suscripción o un ID de prescripción, lo que permite que el mismo perfil esté en el mismo recorrido varias veces a la vez. Esto permite situaciones como administrar varios pedidos o suscripciones en paralelo, y cada instancia sigue su propia ruta a través del recorrido.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>



### Mejoras {#25-05-improv}

Las mejoras incluidas en esta versión se enumeran a continuación.

* Activación de **píldoras para personalización** - Fecha de disponibilidad: 5 de mayo de 2025

  Se ha añadido un nuevo botón &quot;Píldoras&quot; al editor de personalización. Cuando se habilita, los atributos contextuales y de perfil se muestran como píldoras, lo que mejora la legibilidad del código. [Más información](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Esta capacidad se implementará gradualmente en todos los entornos en los próximos 30 días.

* **Carpetas para páginas de aterrizaje** - Fecha de disponibilidad: 9 de mayo de 2025
Para administrar fácilmente las páginas de aterrizaje, ahora puede utilizar carpetas para organizarlas de forma más eficaz en una jerarquía estructurada. [Más información](../landing-pages/manage-lp.md)

* **Seguimiento de clics en plantillas de correo electrónico**\
  El rastreo de clics en `<area>` elementos dentro de mapas de imagen en plantillas de correo electrónico ahora se admite de forma nativa en Journey Optimizer. Esto sirve para garantizar que las áreas de mapa de imagen reciban el mismo ajuste de seguimiento, datos de seguimiento y parámetros añadidos que los hipervínculos estándar.

* **Toma de decisiones - Aprovechar conjuntos de datos de Adobe Experience Platform**\
  Journey Optimizer ahora le permite aprovechar los conjuntos de datos de Adobe Experience Platform en los siguientes objetos de Decisioning: reglas de idoneidad, fórmulas de clasificación y reglas de límite.

* **Carpetas en plantillas y fragmentos**\
  Las carpetas permiten organizar las plantillas y los fragmentos de contenido de forma más fácil y eficaz en una jerarquía estructurada. Antes disponibles para un conjunto de organizaciones (LA), las carpetas ya están disponibles para todos los usuarios (GA) para administrar sus plantillas de contenido y fragmentos.

* **Nueva compatibilidad con objetos de campaña para la copia de zona protegida** <!-- - Availability date: -->
Al copiar campañas en varios entornos limitados mediante las funciones de exportación e importación de paquetes, ahora también se copian las siguientes dependencias: configuraciones de canal, variantes y configuración de experimento, políticas de decisión y elementos. [Más información](../configuration/copy-objects-to-sandbox.md)

* Compatibilidad con **&#39;Redireccionar a dirección URL&#39; en el canal Web**\
  El canal Web de Journey Optimizer ahora permite redirigir a los visitantes a otra URL existente, en lugar de crear una nueva variación en el editor visual. Esta capacidad se puede utilizar para ejecutar experimentos comparando dos páginas completamente diferentes en lugar de cambiar solo unos pocos elementos dentro de una página.

* **Herramientas de espacio aislado - Nuevos objetos de campañas compatibles**\
  Al copiar campañas en varios entornos limitados mediante las funciones de exportación e importación de paquetes, ahora también se copian las siguientes dependencias: configuraciones de canal, variantes y configuración de experimento, políticas de decisión y elementos.

* **Carril derecho en la lista de campañas**\
  En la lista de campañas, al seleccionar una campaña, ahora se abre un panel que muestra sus detalles.

* **Campos de formulario en contenido de experiencia basado en código**\
  En las plantillas de contenido, ahora puede definir campos JSON o HTML específicos que permitan a los usuarios no técnicos editar fácilmente el contenido en experiencias basadas en código sin necesidad de manipular el código.

* **Compatibilidad con atributos de elementos de decisión para reglas de toma de decisiones**\
  Ahora puede aprovechar los atributos de elementos de decisión para crear reglas de toma de decisiones.


* **Subdominios - método &#39;Sin delegación&#39;**\
  Además de la delegación completa y del método CNAME, ahora hay disponible un nuevo método de configuración de subdominios: el método de delegación No, que le permite ser el propietario total del control y el mantenimiento de todos los aspectos de DNS necesarios para enviar, procesar y rastrear mensajes.

* **Compatibilidad con orígenes de datos personalizados en Personalization**\
  Ahora puede crear una consulta y obtener datos de una fuente externa (es decir, no almacenada en Adobe Experience Platform) para utilizarlos en las superficies entrantes y salientes de Journey Optimizer para la personalización y la orquestación de recorrido.

* **Correo directo - Soporte SSH**\
  Además del SFTP existente con tipo de autenticación por contraseña, ahora puede exportar el archivo de correo postal a un servidor SFTP con autenticación por clave SSH.