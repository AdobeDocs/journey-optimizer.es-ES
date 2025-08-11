---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión anterior (2021)
description: Notas de la versión de Journey Optimizer de 2021
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
hide: true
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: 8b755351e25ecae9a2058e63919d6512ea0bf153
workflow-type: ht
source-wordcount: '2035'
ht-degree: 100%

---

# Notas de la versión 2021 {#release-notes-2021}

Esta página enumera todas las funciones y mejoras de [!DNL Journey Optimizer] lanzado en 2021.

## Versión de noviembre de 2021 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>Delegación de subdominios CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora es compatible con CNAME. Un registro CNAME o de nombre canónico es un registro que señala a otra dirección de dominio en lugar de a una dirección IP. La delegación de subdominios CNAME le permite crear un subdominio y utilizar CNAME para señalar registros específicos de Adobe. Con esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS para configurar el entorno de envío, procesamiento y seguimiento de correos electrónicos.</p>
<p>Se recomienda utilizar este método si las políticas de su organización restringen el método de delegación de subdominios completo.</p>
<p>Obtenga más información sobre la delegación de subdominios CNAME en esta <a href="../configuration/delegate-subdomain.md#cname-subdomain-setup">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


## Versión de octubre de 2021 {#oct-2021-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Administración de decisiones: simulaciones de ofertas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede simular qué ofertas se enviarán a un perfil de prueba para una ubicación determinada en la IU de Journey Optimizer. Esto le permite validar la lógica de toma de decisiones, incluidas las restricciones de idoneidad y los algoritmos de clasificación fácilmente antes de ponerlos en producción. Esta posibilidad permite a los usuarios no técnicos y técnicos probar rápidamente la gestión de decisiones y solucionar posibles problemas.</p>
<p>Para obtener más información, consulte la <a href="../offers/offer-activities/simulation.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Administración de decisiones: personalice sus ofertas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede personalizar el contenido de sus ofertas utilizando los atributos de perfil y públicos de Adobe Experience Platform, con el mismo componente de editor de expresiones que se encuentra en la IU de Journey Optimizer. </p>
<p>Para obtener más información, consulte la <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


Consulte también las [Notas de la versión de octubre de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=es){target="_blank"} para obtener más cambios.

### Mejoras

**Recorridos**

* **Editor de expresiones**: como usuario avanzado, ahora puede usar funciones para trabajar con mapas. Esta capacidad se puede aprovechar con las listas de suscripción. Por ejemplo, desde un público, ahora puede obtener una dirección de correo electrónico de una lista de suscripción. [Obtenga más información en esta muestra](../building-journeys/message-to-subscribers-uc.md)

* **Monitorización**: se han mejorado los eventos de paso para los recorridos en directo y el modo de prueba. Se han añadido [nuevos campos](../reports/sharing-field-list.md#serviceevents) en relación con los trabajos de exportación de perfiles. Para mejorar la experiencia del usuario, los campos de eventos de paso ahora están organizados en diferentes categorías. Todos los campos de eventos de paso anteriores siguen disponibles en la categoría [stepEvents](../reports/sharing-legacy-fields.md).
* **Accesibilidad**: se han implementado mejoras de accesibilidad en los recorridos.
* **Colecciones**: ahora se admiten matrices de objetos que contienen subobjetos. [Más información](../building-journeys/collections.md)
* **Listas**: se han mejorado las pantallas de listas para recorridos, eventos, acciones y fuentes de datos.

**Informes**

* **Formato de datos en la vista Global**: ahora puede alternar entre números y porcentajes en la **Vista global** de la pestaña **Ejecución.**


**Administración**

* **Editar ajustes preestablecidos de mensaje**: ahora puede editar los ajustes preestablecidos de mensajes y controlar su estado de actualización. [Más información](../configuration/channel-surfaces.md#edit-channel-surface)
* **Editar registros PTR**: ahora puede editar registros PTR y monitorizar su estado de actualización. [Más información](../configuration/ptr-records.md#edit-ptr-record)

**Personalización**

* **Nueva función de ayuda para el formato de fecha**: ahora puede especificar cómo se debe representar una cadena de fecha. [Más información](../personalization/functions/dates.md#format-date)


**Administración de decisiones**

* **Secuencia de evaluación**: el nuevo y mejorado flujo de creación de decisiones le permite no solo navegar entre objetos de decisión de forma más fluida, sino que también le ofrece un control completo de cómo el motor de decisión evalúa las colecciones de ofertas. Esto incluye qué colecciones se evalúan juntas en lugar de por separado y en qué orden se deben evaluar las colecciones. [Más información](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Correcciones

* Se ha corregido un problema que impedía que se mostraran la lista de recorridos, la lista de mensajes y el Diseñador de correo electrónico cuando el idioma del explorador no era inglés.
* Se ha corregido un error de sintaxis que se producía al añadir una personalización mediante una expresión en el Diseñador de correo electrónico: los caracteres se han escapaban erróneamente.
* Se ha corregido un problema que provocaba un error 404 al navegar en el menú **Administración**.
* Se ha corregido un problema que activaba otros recorridos activos al probar un recorrido con un evento comercial.


## Versión de septiembre de 2021 {#september-2021-release}

### Nuevas funciones

<table>
<thead>
<tr>

<th><strong>Informes: mejor conocimiento del público de destino</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Las nuevas métricas están disponibles en los informes: los mensajes push y segmentados excluidos para correo electrónico son visibles tanto en los informes activos como en los globales. </br> Para tener acceso a las métricas más recientes, tenga en cuenta que tendrá que restablecer los diferentes paneles de informes para cada canal y tipo de informe. Para obtener más información sobre la personalización de tableros, consulte la <a href="../reports/live-report.md">documentación detallada.</a></p>
<p>Una nueva columna de la lista de ejecución de mensajes muestra el número de perfiles objetivo para cada ejecución de mensaje. </p>
<p>Para obtener más información, consulte la <a href="../reports/report-gs-cja.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Paso de listas de datos dinámicamente mediante acciones personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede pasar colecciones o una lista de datos en los parámetros de acción personalizados que se rellenarán dinámicamente durante la ejecución. Se admiten dos tipos de colecciones: simples y de objetos. Las acciones personalizadas creadas anteriormente seguirán funcionando. </p>
<p>Para obtener más información, consulte la <a href="../building-journeys/collections.md">documentación detallada</a>. </p>
<p>Las funciones de filtro e intersección se han añadido a la lista de funciones disponibles en el editor de expresiones avanzadas. Esto ofrece más posibilidades para filtrar y comparar colecciones.</p>
<p>Consulte la documentación de las funciones <a href="../building-journeys/functions/functionfilter.md">filtro</a> e <a href="../building-journeys/functions/functionintersect.md">intersección</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* Los esquemas y conjuntos de datos generados por el sistema que se han creado durante el aprovisionamiento para eventos de paso ahora están en modo de solo lectura, lo que protege contra cualquier modificación involuntaria de esquemas críticos. [Más información](../reports/sharing-overview.md)
* Etiquete claramente la actividad **Espera** con una etiqueta que se mostrará en el lienzo. La etiqueta también se utiliza en los registros de modo de informes y prueba para identificar claramente lo que está haciendo. [Más información](../building-journeys/about-journey-activities.md#best-practices)
* Busque sus eventos y acciones más rápido filtrando los elementos de las categorías **Eventos** y **Acción** usando la búsqueda. Las actividades de orquestación ya no se filtran. [Más información](../building-journeys/using-the-journey-designer.md)
* Al definir una condición de ID de evento en un evento comercial o basado en reglas, el operador “contains” ya está disponible para tipos de cadena de campos. [Más información](../event/about-creating.md)

**Configuración de correo electrónico**

* Cuando se ha asociado un grupo de IP con un ajuste preestablecido de mensaje, ahora puede editarlo; la actualización es asíncrona. También puede comprobar el estado de actualización de cada grupo de IP. [Más información](../configuration/ip-pools.md#edit-ip-pool)


## Versión de agosto de 2021 {#august-2021-release}

### Nuevas funciones

<table>
<thead>
<tr>

<th><strong>Envíe mensajes en el mejor momento: optimización del tiempo de envío</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Envíe automáticamente su mensaje push o de correo electrónico en el mejor momento para cada cliente con el que interactúe con Adobe Journey Optimizer. La optimización del tiempo de envío, con tecnología de los servicios de IA de Adobe, predice el mejor momento para enviar un mensaje push o de correo electrónico para maximizar la participación en función de la apertura histórica y las tasas de clics predefinidas.</p>
<p>Actualmente, esta función está en versión beta y solo está disponible para los clientes de la versión beta. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/send-time-optimization.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Aproveche las relaciones de esquema en eventos empresariales: administración de tablas de búsqueda</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aprovechar las relaciones entre esquemas al configurar un evento empresarial. Esto se suma a la capacidad de aprovechar los campos de tablas vinculadas al configurar un evento unitario, al utilizar condiciones en un recorrido, en la personalización de mensajes y en la personalización de acciones personalizadas.</p>
<p>Para obtener más información, consulte la <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Direcciones URL personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las direcciones URL personalizadas llevan a los destinatarios a páginas específicas de un sitio web o a un micrositio personalizado, según los atributos del perfil. En Adobe Journey Optimizer, ahora puede añadir personalización a las direcciones URL en el contenido del mensaje. La personalización de URL se puede aplicar a texto e imágenes, y puede utilizar datos de perfil o datos contextuales.</p>
<p>Para obtener más información, consulte la <a href="../personalization/personalization-syntax.md#perso-urls">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Asegúrese de que los correos electrónicos lleguen a los usuarios: reintento de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir el período de reintento por ajuste preestablecido para garantizar que los reintentos no se hagan más cuando ya no sean necesarios. Por ejemplo, puede establecer el periodo de reintento en 24 horas para un mensaje transaccional de restablecimiento de contraseña que contenga un vínculo válido solo para un día. Tenga en cuenta que la configuración de reintentos solo se aplica al canal de correo electrónico.</p>
<p>Para obtener más información, consulte la <a href="../configuration/retries.md#retry-duration">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Defina direcciones que excluir del envío: lista de supresión</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La adición de direcciones de correo electrónico y dominios a la lista de supresión ya está disponible en la interfaz de usuario, ya sea una por una o en modo masivo a través de la carga de un archivo CSV.</p>
<p>Para obtener más información, consulte la <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


### Mejoras

**Recorridos**

* **Encabezados dinámicos**: ahora puede pasar datos dinámicos en parámetros de encabezado HTTP. Estos parámetros los pueden utilizar los sistemas de integración que reciben las llamadas HTTP de acción del recorrido, por ejemplo, la marca de tiempo o el ID de seguimiento. [Más información](../action/about-custom-action-configuration.md#url-configuration)
* **Rutas de URL dinámicas**: ahora puede configurar rutas de URL dinámicas para acciones personalizadas. [Más información](../action/about-custom-action-configuration.md#url-configuration)
* La velocidad de regulación general de los públicos de lectura ha cambiado de 17 000 a 20 000 mensajes por segundo. [Más información](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Interfaz de usuario**

* **Buscar**: en todas las páginas, ahora puede buscar objetos empresariales y artículos de ayuda directamente desde el campo de búsqueda unificado de Experience Cloud. [Más información](../start/user-interface.md#unified-search)
* **Recientes**: la visualización de elementos recientes de la página principal de Adobe Journey Optimizer ahora se amplía a objetos comerciales adicionales. Con esta actualización, los accesos directos a los que se ha accedido recientemente incluyen Mensajes, Recorridos, Públicos, Esquemas, Conjuntos de datos, Fuentes de datos, Eventos, Orígenes y Destinos. [Más información](../action/about-custom-action-configuration.md#passing-collection)

**Diseño de contenido**

* **Contexto**: las imágenes de fondo ahora se admiten en la vista previa en vivo. [Más información](../content-management/preview-test.md)
  <!--* **One-click opt-out link** - You can insert a new type of link into your email content: the **Opt-out** link allows users to unsubscribe from receiving your communications in just one click, without being redirected to a landing page to confirm opting out. [Learn more](../privacy/opt-out.md#one-click-opt-out-link)-->

**Personalización**

* **Editor de expresiones**: ahora puede añadir fácilmente un valor alternativo al definir la personalización. Cuando el campo de personalización está vacío para un perfil, se muestra el valor de reserva. [Más información](../personalization/functions/helpers.md)

**Configuración de correo electrónico**

* **Lista de permitidos**: ahora, la lista de permitidos se puede habilitar y deshabilitar en una zona protegida que no sea de producción mediante una llamada de API. [Más información](../configuration/allow-list.md#enable-allow-list)
* **Navegación**: la lista de supresión, a la que se podía acceder desde el menú **Administración > Canales > Configuración de correo electrónico > General**, se ha trasladado al nuevo submenú **Lista de supresión**, que recopila todas las funciones relacionadas para facilitar el acceso. [Más información](../configuration/manage-suppression-list.md#access-suppression-list)

**Administración de decisiones**

* Se ha actualizado la forma de añadir y configurar representaciones al crear una oferta para mejorar la experiencia del usuario. En concreto, la biblioteca de recursos ahora solo se muestra al definir el contenido de tipo imagen para una representación. [Más información](../offers/offer-library/creating-personalized-offers.md#representations)

### Correcciones

* Se ha corregido un problema de accesibilidad en la navegación por pestañas de mensajes.
* Se ha corregido un problema de localización en las etiquetas del Diseñador de correo electrónico.
* Se ha corregido un problema que se producía al seleccionar más de un nodo en un recorrido y al hacer clic en Eliminar en el panel de propiedades.
* Se ha corregido un problema que impedía añadir un nuevo encabezado a una acción utilizada en un recorrido.
* Ahora puede averiguar el motivo por el que la creación de un ajuste preestablecido de mensaje falló a través de una advertencia más explícita en la interfaz de usuario.


## Versión de julio de 2021 {#july-2021-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Uso de metadatos en los mensajes: administración de tablas de búsqueda</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Enriquezca sus experiencias con los datos de referencia que ha cargado en Journey Optimizer. Algunos ejemplos son la búsqueda de metadatos sobre un ID de reserva en un evento de experiencia o la búsqueda de información de producto desde un SKU en un evento de experiencia para su uso en el lienzo. </p>
<p>Ahora puede aprovechar las relaciones entre esquemas para utilizar un conjunto de datos como una tabla de búsqueda para otro. A continuación, puede aprovechar todos los campos de las tablas vinculadas al configurar un evento unitario, al utilizar condiciones en un recorrido, en la personalización de mensajes y en la personalización de acciones personalizadas.</p>
<p>Para obtener más información, consulte la <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lista de permitidos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir una lista específica de seguridad de envío en el nivel de zona protegida para disponer de un entorno seguro para realizar pruebas. En una instancia que no es de producción, donde pueden producirse errores, la lista de permitidos garantiza que no tendrá riesgo de enviar mensajes no deseados a sus clientes. Esta función se habilita aprovechando las API de supresión.</p>
<p>Para obtener más información, consulte la <a href="../configuration/allow-list.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* La velocidad de regulación general de todos los públicos de lectura que se ejecutan simultáneamente en la misma zona protegida está limitada a 17 000 mensajes por segundo. [Más información](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* El campo **Duración de la caché** se ha eliminado del panel de configuración de la fuente de datos. [Más información](../datasource/about-data-sources.md)
* Para las fuentes de datos externas, ahora se define automáticamente una regla de límite de 15 llamadas por segundo. [Más información](../configuration/external-systems.md#capping)
* En el caso de los recorridos activos, la pantalla de propiedades de recorrido ahora muestra la fecha de publicación y el nombre del usuario que publicó el recorrido. [Más información](../building-journeys/journey-gs.md#change-properties)
* En la pantalla de la lista de recorridos, se ha añadido el filtro de tipo de recorrido. [Más información](../start/user-interface.md#filter-lists)
* El parámetro **[!UICONTROL Velocidad de regulación]** se ha añadido en la actividad de Público de lectura. [Más información](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Vista previa y prueba**

* La identidad y el área de nombres ahora están visibles en la pantalla **[!UICONTROL Vista previa]**. [Más información](../content-management/preview-test.md#preview-your-messages)
* El número de correos electrónicos de prueba para pruebas ahora está restringido a 10.
* Los caracteres permitidos para el **Prefijo de línea de asunto** en las pruebas ahora están limitados. [Más información](../content-management/preview-test.md#send-proofs)

**Editor de expresiones de personalización**

* Se ha cambiado el nombre de la lista desplegable de ayuda y se ha reorganizado.

### Correcciones

* Se ha corregido un problema que hacía que se enviaran mensajes duplicados para la entrega por lotes de correo electrónico.
* Los eventos ahora se generan según corresponda cuando el envío de correo electrónico no se realiza una vez que ha finalizado el periodo de reintento.
* Se ha corregido un problema por el que faltaba información de IP en la pantalla Registros de PTR.
* Ya está implementada la localización en el carril de la oferta dentro del Editor de expresiones.
* Se ha corregido un espaciado incorrecto en las ventanas emergentes de información.
* Se ha corregido un problema en el Diseñador de correo electrónico al cargar un archivo de HTML en el que no se admitía la hoja de estilo interna con la propiedad `background-image`.
