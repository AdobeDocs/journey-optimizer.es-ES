---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 00a8edd899673e2c2cf738df8a28dd53e085b680
workflow-type: tm+mt
source-wordcount: 2274
ht-degree: 6%

---


# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece continuamente nuevas funciones, mejoras en las funciones existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

## Notas previas al lanzamiento de junio de 2026 {#june-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios están activos en la producción. Aunque la mayoría de los cambios se entregan en la fecha de lanzamiento, algunos pueden implementarse más adelante. Consulte la Fecha de disponibilidad indicada para cada entrada para obtener más información.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 16 y 17 de junio de 2026

### Lealtad {#june-26-loyalty}

La siguiente funcionalidad se lanzará a Loyalty en esta versión.

<table>
<thead>
<tr>
<th><strong>Desafíos de fidelización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los Desafíos de lealtad convierten las iniciativas de lealtad en experiencias atractivas y entretenidas que motivan a los clientes a realizar acciones valiosas, como realizar compras, escribir críticas, participar en medios sociales o recomendar amigos.</p>
<p>Los administradores pueden usar el menú de administración de Fidelidad para conectar Journey Optimizer con su ecosistema de fidelidad, incluidas las API de cumplimiento de recompensas, las definiciones de eventos, el inventario de productos, las exclusiones y la configuración de identidad. Los especialistas en marketing pueden diseñar desafíos estándar, de racha o secuenciales, definir tareas y recompensas, ofrecer tarjetas de contenido de marca y mensajes, y monitorizar el rendimiento con paneles de informes integrados. Journey Optimizer genera los recorridos que organizan cada desafío en segundo plano, de modo que los equipos puedan centrarse en la experiencia del cliente y los objetivos empresariales.</p>
<p>Esta capacidad ya está disponible para todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

### Recorridos {#june-26-journeys}

Las siguientes funcionalidades y mejoras están llegando a los recorridos en esta versión.

<table>
<thead>
<tr>
<th><strong>Optimización de ruta de recorrido: segmentación</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilice el nuevo nodo Optimizar para dirigirse a audiencias específicas y determinar la mejor ruta para satisfacer los KPI centrados en el negocio.</p>
<p>Esta herramienta le permite desarrollar campañas de marketing más efectivas que tengan más probabilidades de interesar en el nivel 1:1, mejorar los esfuerzos de personalización de marketing para los clientes y mejorar los KPI de participación del cliente esencial, como las conversiones y los ingresos.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitraje de recorrido - Fórmulas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar fórmulas para aumentar automáticamente las puntuaciones de prioridad de recorridos en función de atributos de perfil del cliente y factores contextuales, lo que garantiza que los clientes ingresen los recorridos más relevantes.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

* **Mayor límite de recorridos activos y nuevas protecciones**: ahora puede tener hasta 200 recorridos activos, más que el límite anterior de 100.

* **Fechas de inicio y finalización en el encabezado del recorrido**: cuando las fechas de inicio o finalización se configuran en un recorrido activo, ahora aparecen en el encabezado del recorrido junto al distintivo de estado activo. La etiqueta mostrada se adapta en función de si cada fecha es próxima o ya ha pasado.

* **Detener o cerrar un recorrido pausado directamente**: ahora puede detener un recorrido o cerrarlo a nuevas entradas directamente desde el estado Pausado. Anteriormente, un recorrido pausado tenía que reanudarse a Activo antes de que se pudiera detener o cerrar.

* **Compatibilidad con ID suplementario en recorridos para audiencias externas**. Ahora se admiten identificadores suplementarios en recorridos para audiencias externas, incluidas audiencias importadas de un archivo CSV y audiencias creadas con Composición de audiencia federada. Puede designar cualquier atributo que no sea de identidad o de identidad que no sea de persona de la audiencia como ID suplementario; no se requiere un etiquetado de esquema.

### Campañas orquestadas {#june-26-oc}

Las siguientes funcionalidades y mejoras están llegando a las campañas orquestadas en esta versión.

<table>
<thead>
<tr>
<th><strong>Actividad de carga de archivos en campañas organizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las campañas orquestadas ahora admiten la carga de un archivo CSV o TXT directamente en el lienzo de campaña como audiencia de destino, sin ingerir primero el archivo en Adobe Experience Platform. Los datos del archivo se consumen en el momento de la ejecución y no persisten como un conjunto de datos de Adobe Experience Platform. Durante la configuración del archivo, puede definir asignaciones de columnas, tipos de datos, control de valores NULL y directivas de error por columna. Esto admite campañas de envíos específicos o de listas de socios en las que no es práctico crear una canalización de ingesta completa.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad con Horas de silencio para campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar horas tranquilas a las campañas orquestadas. Las horas tranquilas le permiten definir exclusiones basadas en el tiempo para evitar que los mensajes se envíen durante períodos específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento en los casos de uso de la orquestación de la campaña.</p>
</td>
</tr>
</tbody>
</table>

* **Personalización basada en bucles para datos relacionales en campañas orquestadas**: el editor de personalización ahora admite un bloque de Bucle que se repite en colecciones relacionales, como pedidos, cuentas o reservas, y procesa un bloque de contenido por registro en un solo correo electrónico o SMS. Las colecciones se configuran mediante el selector de datos utilizando tokens de personalización, sin necesidad de escribir expresiones.

* **Personalizar los detalles del remitente del correo electrónico por destinatario y campaña**: las campañas organizadas ahora admiten la personalización de los campos de encabezado de correo electrónico, incluidos el nombre del remitente, la dirección del remitente y la respuesta a, mediante atributos de perfil o datos relacionales. Esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa. Los valores del encabezado se pueden establecer en el nivel de canal y anularse por campaña utilizando datos contextuales para un control más preciso.

* **Simplificación de la dimensión de destino en campañas orquestadas**: la dimensión de segmentación activa ahora se muestra en el lienzo del flujo de trabajo, para que pueda ver qué dimensión utiliza una actividad de canal. El flujo de segmentación de varias entidades es más sencillo, ya que ya no necesita una actividad &quot;Change dimension&quot; independiente. Además, ahora puede elegir explícitamente si los mensajes se envían en el nivel de perfil o en un nivel de dimensión secundario.

* **Anular el campo de ejecución predeterminado en las campañas**: antes disponible en el nivel de recorrido, ahora se puede anular el campo de ejecución predeterminado establecido globalmente para las entregas de correo electrónico, SMS y WhatsApp en los parámetros de campaña.

### Toma de decisiones {#june-26-decisioning}

La siguiente funcionalidad llega a Decisioning en esta versión.

<table>
<thead>
<tr>
<th><strong>Aprovechamiento del fragmento de contenido de Adobe Experience Manager en Decisioning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede asignar fragmentos de contenido de Adobe Experience Manager a elementos de decisión en Toma de decisiones y aprovecharlos dentro de las políticas de decisión para entregar el fragmento adecuado al cliente correcto en el momento adecuado.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

### Canal de correo electrónico {#june-26-email}

Las siguientes funcionalidades y mejoras están llegando al canal de correo electrónico en esta versión.

<table>
<thead>
<tr>
<th><strong>Componentes avanzados: diseños (supercomponentes)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Email Designer ahora incluye una biblioteca de componentes de diseño listos para usar, como encabezados, tarjetas de producto (1, 2 o 3 columnas), bloques de información y pies de página, que puede arrastrar y soltar directamente en el lienzo del correo electrónico. Cada componente viene preconfigurado con propiedades editables (imagen, título, texto, botón, vínculos) y se puede personalizar completamente a través de la interfaz de WYSIWYG, lo que acelera la creación de correos electrónicos sin necesidad de crear estructuras desde cero.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Comprobación de contenido en Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora permite a los usuarios validar la calidad de su contenido de correo electrónico, incluida la legibilidad, la eficacia y la coherencia del contenido, directamente en la interfaz de Designer de correo electrónico.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activar reducción de tamaño de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta nueva opción permite reducir el tamaño del HTML en un correo electrónico eliminando los espacios en blanco, los comentarios y el código redundante innecesarios, sin cambiar el aspecto del correo electrónico. Esto ayuda a mejorar la capacidad de entrega (algunos proveedores de correo electrónico rechazan o marcan correos electrónicos de gran tamaño) y puede acelerar el tiempo de carga de los destinatarios.</p>
<p>Fecha de disponibilidad: 10 de junio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Compatibilidad con modo de texto en fragmentos**: para admitir flujos de trabajo de correo electrónico basados en texto, ahora puede crear y administrar versiones de texto de los fragmentos visuales para un uso óptimo en la versión de texto sin formato de los correos electrónicos que incluyen ese fragmento. Al utilizar un fragmento creado antes de la versión actual, la versión de texto del fragmento puede procesarse incorrectamente, tanto en el Designer de correo electrónico como en el correo electrónico final enviado a los destinatarios. Para obtener los mejores resultados con fragmentos antiguos, edite, guarde y vuelva a publicar cada fragmento.

* **Se han actualizado los puntos de referencia de rendimiento de envío por lotes con escenarios orientados al cliente** - Los puntos de referencia de rendimiento de envío por lotes de Adobe Journey Optimizer se han actualizado para reflejar el rendimiento de nivel de producción en varios escenarios de personalización - desde envíos básicos hasta contenido dinámico complejo con lógica condicional. Las métricas actualizadas ahora están disponibles en la documentación del producto para ayudar a los clientes a planificar con precisión sus volúmenes de mensajería.

* **Proceso OTP del bucle de comentarios para subdominios personalizados**: el proceso de configuración del subdominio personalizado del Bucle de comentarios (FBL) se ha mejorado al mostrar la contraseña única (OTP) de Yahoo sender hub directamente dentro de la interfaz de usuario del producto. Los usuarios ahora pueden recuperar y mostrar automáticamente el OTP generado durante la verificación de propiedad del dominio del centro de remitentes de Yahoo.

* **Excluir clics de bots para informes de correo electrónico y SMS**: para proporcionar una vista más precisa de la participación real de los clientes, ahora hay disponibles nuevas métricas estimadas en los informes de Recorridos, campañas y canales. Estas métricas ayudan a filtrar las interacciones no humanas (NHI) y los clics de bots a partir de los datos de informes: Clics estimados (los clics totales se cuentan después de eliminar el tráfico de bots y no humanos identificados), CTR estimados (los clics estimados en relación con los envíos totales) y CTOR estimado solo para correo electrónico (los clics estimados en relación con las aperturas estimadas).

### Mensajería móvil (SMS, MMS, RCS y LINE) {#june-26-mobile}

Las siguientes mejoras se incluyen en la mensajería móvil en esta versión.

* **Clics únicos para informes de SMS**: Se ha introducido un nuevo módulo de Clics únicos en los informes de SMS, que ofrece el mismo nivel de seguimiento granular de rendimiento para los informes de SMS que está disponible actualmente para los informes de correo electrónico.

* **Canal LINE - Creación de cambios** - La interfaz de usuario del canal LINE se ha actualizado con funciones avanzadas de creación de mensajes. Esta versión incorpora compatibilidad con varios formatos de mensaje, incluidos Texto, Imagen, Mapa de imágenes, Carrusel y Flex (Editor JSON), además de vistas previas de dispositivos en tiempo real. Los usuarios ahora pueden administrar mensajes agrupados de hasta cinco mensajes ordenados (con controles de adición, eliminación y reordenación) y aprovechar el editor de personalización integrado para mensajes validados y dinámicos.

* **Reventa de Journey Optimizer - Mostrar métricas de uso** - Para los clientes que compran SMS directamente a través de Adobe Journey Optimizer, se ha introducido un nuevo panel de uso de SMS. Ahora puede ver y rastrear las métricas de envío de mensajes de los últimos 90 días, clasificadas por mensajes móviles originados (MO) y móviles terminados (MT). Estos datos también están disponibles para su descarga a través de CSV, lo que proporciona una mayor visibilidad y control sobre la inversión en SMS.

### Contenido e integraciones {#june-26-content}

En esta versión se incluyen las siguientes funcionalidades y mejoras para la administración de contenido y las integraciones.

<table>
<thead>
<tr>
<th><strong>Fragmentos de contenido con Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta versión incorpora varias mejoras para que los fragmentos de contenido de Adobe Experience Manager sean más utilizables, gobernables y estén más listos para la producción dentro de los flujos de trabajo de creación de Journey Optimizer:</p>
<ul>
<li>Journey Optimizer ahora admite la captura de fragmentos de contenido desde varias configuraciones de Adobe Experience Manager, incluidos los niveles de creación, publicación y publicación autenticada.</li>
<li>Una vez seleccionado un fragmento, su contexto se conserva en todo el mensaje, lo que permite a los autores reutilizar los campos de fragmento en bloques de contenido sin volver a seleccionar.</li>
<li>Se ha introducido una nueva página de lista de fragmentos de contenido en Journey Optimizer para mejorar la administración del ciclo vital; los usuarios pueden identificar fragmentos no sincronizados y sincronizar manualmente el déclencheur para mantenerse al día.</li>
<li>La compatibilidad con la configuración regional y las variaciones ahora permite a los especialistas en marketing trabajar con versiones alternativas del mismo fragmento de contenido de forma más deliberada.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configuración del repositorio de Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora tiene flexibilidad en la forma en que Adobe Journey Optimizer accede al contenido de Adobe Experience Manager. Esta versión presenta la capacidad de cambiar el repositorio de origen para los fragmentos de contenido utilizados en sus recorridos y campañas.</p>
</td>
</tr>
</tbody>
</table>

* Integración de **fragmentos de contenido AEM nativos (Managed Services) en AJO**: ahora compatible con Managed Services, puede ver, acceder y usar fragmentos de contenido Adobe Experience Manager directamente en Journey Optimizer para personalización. Simplemente agregue la URL del repositorio de Adobe Experience Manager Managed Services en los ajustes de configuración como una configuración única.

* **Integración de Emagica con AEM Asset Essentials**: El asistente de IA ahora recupera automáticamente imágenes aprobadas por la marca directamente de su Adobe Experience Manager Assets al generar correos electrónicos, páginas web y notificaciones push. Esto elimina la necesidad de buscar manualmente en Assets o confiar en las retrospectivas de IA genéricas, lo que garantiza que cada imagen sea perfectamente precisa y compatible con la marca.

### Canales personalizados {#june-26-channels}

La siguiente funcionalidad está llegando a los canales en esta versión.

<table>
<thead>
<tr>
<th><strong>Canal de salida personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora presenta Canales personalizados, una nueva funcionalidad que permite a los administradores introducir cualquier canal de mensajería saliente basado en HTTP, como WeChat, Kakao Talk, Messenger o un proveedor propietario, directamente en AJO a través de un Generador de canales sin código. Una vez configurados, los canales personalizados están disponibles en Campañas, Recorridos y Campañas orquestadas, con el mismo conjunto completo de funcionalidades que los canales nativos: personalización con el editor de expresiones, experimentación de contenido, previsualización y prueba, informes predeterminados y aplicación de consentimiento y gobernanza. Esto colma el vacío que anteriormente subsanaban las acciones personalizadas, que se limitaban a los Recorridos y carecían de creación de contenido dedicada.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>

### Configuración {#june-26-configuration}

Las siguientes mejoras se incluyen en la configuración y administración de esta versión.

* **Lista blanca de IP de Firewall de aplicaciones web (WAF) para páginas de destino de AJO**: Adobe Journey Optimizer ahora admite la lista blanca de IP de Firewall de aplicaciones web (WAF) para páginas de destino, lo que permite a las organizaciones aplicar que todas las solicitudes entrantes se enruten exclusivamente a través de su infraestructura de WAF configurada. Con esta mejora, los clientes pueden configurar AJO para que rechace cualquier solicitud directa que omita el nivel de WAF, lo que garantiza que las políticas de seguridad definidas en herramientas como Imperva se apliquen de forma coherente. Esta capacidad refuerza la postura de seguridad de las empresas con requisitos estrictos de acceso a la red, lo que les permite un control total del flujo de tráfico a sus páginas de aterrizaje alojadas en AJO.

* **Conjunto de datos que se mueve de flujo a modo por lotes** - El conjunto de datos de evento de comentarios de mensajes de AJO está pasando de flujo a modo de ingesta por lotes. Este cambio garantiza que la ingesta de datos no supere los límites de ingesta de transmisión. Si utiliza este conjunto de datos en informes de Customer Journey Analytics o ejecuta consultas en él, espere un aumento de la latencia de datos de hasta dos horas en adelante.

### Mejoras de uso {#june-26-usability}

La siguiente mejora de uso se publicará en esta versión.

* **Carpetas para Recorridos y campañas**: ahora puede organizar sus recorridos y campañas en carpetas para mejorar la navegación y la administración en la interfaz.

