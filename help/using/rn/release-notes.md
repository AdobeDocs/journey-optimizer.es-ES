---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 378ead41924496f52f22026b3f0e05a9c9c76f89
workflow-type: tm+mt
source-wordcount: '1428'
ht-degree: 33%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.


## Orquestación de campañas 

**Fecha de disponibilidad**: 4 de agosto de 2025

Journey Optimizer ahora incluye **Campaign Orchestration**, una nueva funcionalidad diseñada específicamente para campañas por lotes iniciadas por la marca. Esta versión presenta un lienzo de orquestación de campaña y un modelado de datos mejorado, trabajando juntos para permitir que los especialistas en marketing planifiquen, dirijan y entreguen campañas personalizadas en canales múltiples.

![GIF de Campaign Orchestration](assets/do-not-localize/release.gif)

Incluye [esquemas y conjuntos de datos relacionales](#oc-relational) y [lienzo de Campaign](#oc-canvas). Juntas, estas dos innovaciones desbloquean un nuevo estándar para orquestar campañas por lotes en Journey Optimizer. A continuación se enumeran las funcionalidades clave.

### Capacidades clave {#oc-capabilities}

* **Flujos de trabajo de varios pasos**

  Impulse campañas por lotes multicanal sofisticadas con el nuevo lienzo de orquestación de campañas creado específicamente.

* **Audiencias a petición**

  Segmentar audiencias bajo demanda para su activación inmediata.

* **Segmentación de varias entidades**

  Cree audiencias con el contexto empresarial (dimensiones que no sean personas), como productos, tiendas, renovaciones, reservas y mucho más.

* **Visibilidad previa al envío**

  Revise, perfeccione y optimice audiencias y campañas antes del lanzamiento y mientras se ejecutan las campañas

### Lienzo de campaña {#oc-canvas}

Una interfaz de orquestación visual completamente nueva diseñada específicamente para campañas por lotes. Este lienzo habilita:

* Planificación visual de flujos de campaña de varios pasos y canales

* Compatibilidad con audiencias bajo demanda creadas a partir de consultas relacionales

* División de audiencias avanzada, esperas y lógica condicional

* Recuentos precisos de preenvío después de aplicar reglas y filtros empresariales

### Esquemas relacionales y conjuntos de datos {#oc-relational}

Adobe Journey Optimizer ahora admite entidades relacionales (por ejemplo, productos, tiendas, reservas, contratos) vinculadas a perfiles basados en personas. Esto permite la segmentación y personalización en estructuras de datos multidimensionales, lo que permite casos de uso como:

* Un mensaje por reserva, suscripción o contrato

* Segmentación basada en atributos de entidad relacionados (por ejemplo, categoría de producto o ubicación de tienda)

* Mejor direccionamiento (por ejemplo, enviar a todos los contactos conocidos vinculados a una entidad)

### Por qué importa

Esta versión proporciona a los especialistas en marketing un control total sobre el marketing por lotes iniciado por la marca y basado en audiencias, lo que combina un modelado de datos flexible con una experiencia de orquestación diseñada específicamente. Está diseñada específicamente para la orquestación de campañas por lotes desde recorridos en tiempo real, a la vez que ofrece personalización y escalabilidad avanzadas.

### Más información

Obtenga más información en la [documentación de orquestación de Campaign](../orchestrated/gs-orchestrated-campaigns.md).

<!--
## August '25 pre release notes {#25-7-rn}

**Pre release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: August 19, 2025


### New capabilities {#Aug-25-8-features}

New capabilities coming with this release are detailed below.

### Improvements {#Aug-25-8-improv}

Improvements coming with this release are listed below.
-->

## Actualizaciones del 25 de agosto {#25.8-rn}

<table>
<thead>
<tr>
<th><strong>Optimización en campañas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, Journey Optimizer le ofrece las herramientas necesarias para ofrecer contenido personalizado y optimizado a la audiencia de sus campañas, lo que le permite ejecutar experimentos de contenido, crear objetivos basados en reglas y utilizar combinaciones avanzadas de ambos para maximizar la eficacia de sus campañas.</p>
<p>Con Optimización, puede:</p>
<ul>
<li>Pruebe múltiples variaciones de contenido para identificar la mensajería más eficaz.</li>
<li>Ofrezca contenido personalizado basado en atributos de usuario y datos contextuales.</li>
<li>Combine segmentación y experimentación para estrategias de campaña avanzadas.</li>
<li>Filtrar los usuarios que no coincidan con los criterios de variante.</li>
<li>Garantizar mecanismos de reserva para mantener la participación del usuario.</li>
</ul>
<P>Una vez que la campaña está activa, los perfiles se evalúan según los criterios definidos y, según los criterios coincidentes, se envían con la experiencia o el contenido adecuados de la campaña.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Fecha de lanzamiento: 8 de agosto de 2025</p>
<p>Para obtener más información, consulte la <a href="../campaigns/campaigns-message-optimization.md">documentación detallada</a></p>
</td>
</tr>
</tbody>
</table>



## Notas de la versión de julio de 2025 {#25-7-rn}

**Fecha de lanzamiento**: miércoles, 29 de julio de 2025

### Nuevas funciones {#features-25-7}

A continuación, se describen las nuevas funciones incluidas en esta versión.

#### Funcionalidades

<table>
<thead>
<tr>
<th><strong>Marcas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear y personalizar sus propias marcas para definir claramente su identidad visual y verbal en todas las comunicaciones. Con la puntuación de alineación de marca, puede recibir comentarios en tiempo real sobre cómo el contenido refleja el tono, el estilo y las directrices de su marca, lo que le ayuda a mantenerse constantemente al día con la marca con cada mensaje que envía.</p>
<p>Esta funcionalidad, lanzada anteriormente en Beta, ya está disponible para todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>Para obtener más información, consulte la <a href="../content-management/brands.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usar Decisioning en el canal de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede agregar directivas de Decisión a recorridos de correo electrónico y campañas. Las políticas de decisión son contenedores para sus ofertas que aprovechan el motor de decisión para devolver dinámicamente el mejor contenido para entregar a cada miembro de la audiencia.</p>
<p>Esta funcionalidad está disponible con disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.</p>
Para obtener más información, consulte la <a href="../experience-decisioning/create-decision.md">documentación detallada</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal LINE</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ha ampliado sus funcionalidades en canales múltiples para incluir la compatibilidad con el canal LINE. Esta mejora le permite crear, editar y previsualizar experiencias de LINE, permitiendo interacciones más personalizadas y atractivas. Con LINE, puede conectarse con más clientes, enviar contenido relevante y mejorar su participación.</p>
<p>Anteriormente disponible solo para solicitudes, el canal LINE ahora está disponible para todos los usuarios (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../line/get-started-line.md">documentación detallada</a>.</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Recorrido Dry Run</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El ensayo del recorrido es un modo especial de publicación de recorrido en Adobe Journey Optimizer que permite a los profesionales del recorrido probar un recorrido utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar la información de perfil. Esta función ayuda a los profesionales del recorrido a confiar en el diseño del recorrido y en la segmentación del público antes de publicarlo en directo.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-dry-run.md">documentación detallada</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>ID suplementario para recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede activar recorridos utilizando un ID de perfil junto con otro identificador, como un ID de pedido, un ID de suscripción o un ID de prescripción, lo que permite que el mismo perfil esté en el mismo recorrido varias veces a la vez. Esto permite situaciones como administrar varios pedidos o suscripciones en paralelo, y que cada instancia siga su propia ruta a través del recorrido.</p>
<p>Publicado anteriormente en Disponibilidad limitada, el uso de ID suplementarios en recorrido ya está disponible para todos los entornos. Con esta versión de Disponibilidad general, la función ahora es compatible con los recorridos de Lectura de audiencia.</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/supplemental-identifier.md">documentación detallada</a></p>
</td>
</tr>
</tbody>
</table>

### Alertas en el producto

Ahora puede suscribirse a **alertas por correo electrónico y en el producto** para las versiones de productos de Journey Optimizer.

Para suscribirse:

* Vaya a **Preferencias de Adobe Experience Cloud**
* En **Notificaciones**, busque **Nuevas versiones de Journey Optimizer**
* Habilitar notificaciones en la aplicación y por correo electrónico

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### Cambio en las condiciones del recorrido {#ee-change@}

A partir del 8 de julio, en las nuevas organizaciones de clientes, la creación de expresiones mediante eventos de experiencia dejará de ser compatible con el editor de expresiones utilizado en las condiciones del recorrido. Como resultado, no se pueden usar eventos de experiencia en la [fuente de datos de Experience Platform](../datasource/adobe-experience-platform-data-source.md) para crear expresiones. [Aquí](../building-journeys/exp-event-lookup.md) encontrará referencias a enfoques alternativos y prácticas recomendadas para crear expresiones y lógicas con eventos de experiencia.

No hay cambios en la forma de acceder a los datos de evento de contexto de recorrido en los recorridos unitarios. En los editores de expresiones y personalización, los usuarios pueden seguir accediendo a los datos pasados con el evento de recorrido inicial.

Obtenga más información [en estas preguntas frecuentes](../building-journeys/exp-event-lookup.md#faq-ee).

### Mejoras {#25-7-improv}

A continuación, se describen las mejoras incluidas en esta versión.

* **Campañas**

   * **Varias acciones entrantes en las campañas**: para simplificar la orquestación de la campaña, ahora puede definir varias acciones entrantes en una sola campaña. Esta capacidad le permite enviar varias experiencias basadas en código, mensajes en la aplicación, tarjetas de contenido o acciones web a diferentes ubicaciones al mismo tiempo, cada acción con un contenido específico.
     [Más información](../campaigns/campaign-action.md#multi-action)

   * **Reorganización del inventario de campañas**: las campañas programadas y activadas por API ahora se dividen en pestañas independientes en el inventario de campañas para facilitar la navegación y la administración.

[Más información](../campaigns/modify-stop-campaign.md)

* **Administración de datos**
   * **Actualización de conjuntos de datos del sistema de Administración de decisiones**: las ofertas personalizadas y de reserva eliminadas ahora se marcan como archivadas en los conjuntos de datos &quot;decision_object_repository_personalized_offers&quot; y &quot;decision_object_repository_fallback_offers&quot;. Los registros existentes en el conjunto de datos no cambian.

[Más información](../offers/export-catalog/access-dataset.md)

* **Recorridos**
   * **Mejoras en la herramienta de espacio aislado para Recorridos**: al copiar recorridos en varios espacios aislados mediante las funciones de exportación e importación de paquetes, ahora también están disponibles las siguientes funciones:
      * Selección de un evento existente en el destino
      * Copia de un evento independientemente de un recorrido
      * Detectar relaciones entre grupos de campos y fuentes de datos, vincularlas en el destino si existen y crearlas en caso contrario.

[Más información](../configuration/copy-objects-to-sandbox.md)

* **Canal: en la aplicación**
   * **Pares de clave/valor en la aplicación**: con los mensajes en la aplicación, puede definir pares de clave y valor para incluir variables personalizadas en la carga útil del mensaje. Estos pares clave-valor le permiten pasar datos adicionales según su configuración específica y el caso de uso. [Más información](../in-app/design-in-app.md)

* **Canal - Tarjeta de contenido**

   * **Descalificación de campaña basada en reglas**: al editar reglas de entrega adicionales, la opción de reglas de entrega anteriores se ha reemplazado con tres tipos de reglas diferentes para controlar mejor el tiempo y la visibilidad del mensaje:
      * Mostrar mensaje si: Condiciones que determinan cuándo se muestra la tarjeta de contenido.
      * Descartar mensaje si: Condiciones que ocultan temporalmente la tarjeta de contenido. Puede volver a aparecer si se vuelven a cumplir las condiciones de visualización.
      * Descalificar mensaje si: Condiciones que impiden permanentemente que se vuelva a mostrar la tarjeta de contenido.

[Más información](../content-card/design-content-card.md)

* **Toma de decisiones**
   * **API de herramientas de migración**: el equipo de Journey Optimizer está trabajando en las API de herramientas de migración para migrar entidades de administración de decisiones a Decisioning. Esta herramienta permite una migración perfecta entre entornos limitados con resolución de dependencia y funciones de reversión. Si está interesado, póngase en contacto con su representante de Adobe.

* **Personalización**
   * Se ha añadido una nueva función de ayuda, &quot;SHA256&quot;, al editor de personalización. Esta función se utiliza para calcular y devolver el hash sha256 de una cadena.

[Más información](../personalization/functions/string.md#sha256)
