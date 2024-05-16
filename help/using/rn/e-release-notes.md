---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 628d49ee45ce161fc5e213bda60cb44d41223369
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 26%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

## Notas de la versión anteriores de mayo de 2024 {#e-2024}

**Fecha de lanzamiento**: 21 y 22 de mayo de 2024

### Nuevas funciones {#e-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.


<table>
<thead>
<tr>
<th><strong>Toma de decisiones sobre experiencias: disponibilidad limitada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La toma de decisiones sobre experiencias simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como “elementos de decisión” y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar a cada persona los elementos de decisión más relevantes.</p>
<p>Estos elementos de decisión se integran perfectamente en una amplia gama de superficies entrantes a través del nuevo canal de experiencia basado en código, ahora accesible dentro de las campañas de Journey Optimizer. Las políticas de decisión de Experience Decisioning solo están disponibles para su uso en campañas de experiencia basadas en código.</p>
<p>Ahora mismo, la toma de decisiones sobre experiencias solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/gs-experience-decisioning.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Flujo de trabajo de preparación IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Si envía correos electrónicos en una dirección IP completamente nueva, ahora puede realizar fácilmente flujos de trabajo de calentamiento de IP directamente desde la interfaz de usuario. Adobe Journey Optimizer ofrece una forma estandarizada y eficaz de calentar las direcciones IP que sigue las prácticas recomendadas para lograr una entrega óptima.</p>
<p>Para obtener más información, consulte la <a href="../configuration/ip-warmup-gs.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reglas empresariales: beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear reglas de límite de frecuencia granulares y aplicarlas a diferentes tipos de comunicaciones de marketing a través de conjuntos de reglas. Esta nueva funcionalidad le permite controlar la frecuencia con la que las audiencias reciben un mensaje configurando reglas en canales múltiples que excluyen automáticamente los perfiles saturados de los mensajes y las acciones.</p>
<p>La funcionalidad de reglas empresariales está disponible actualmente como una versión beta pública.</p>
<p>Para obtener más información, consulte la <a href="../configuration/business-rules.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Datos de personalización extendidos: beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede buscar y recuperar valores de datos dentro de conjuntos de datos de Adobe Experience Platform y utilizar estos valores para crear condiciones en Adobe Journey Optimizer. Puede aprovechar los datos de un conjunto de datos de búsqueda cuando se ha definido una relación con un atributo dentro de una matriz de objetos. Puede especificar conjuntos de datos que no tengan perfil habilitado para la búsqueda. Una vez habilitado, puede utilizar un atributo de perfil como clave de unión al conjunto de datos especificado para recuperar más datos para personalizar.</p>
<p>Actualmente, esta funcionalidad está disponible como una versión beta pública.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Experience Decisioning**

Desde la versión beta hasta esta versión, se han añadido las siguientes mejoras:

* **Experience Decisioning + Experiencias basadas en código (LA)** : Ahora puede aprovechar la función Experience Decisioning para utilizar elementos de decisión en sus campañas basadas en código. Nota: El canal de experiencia basado en código y Experience Decisioning no están disponibles para las organizaciones que han adquirido las ofertas adicionales Escudo de Adobe Healthcare y Escudo de privacidad y seguridad. [Más información](../code-based/get-started-code-based.md)
* **Datos de contexto** : ahora puede aprovechar los datos de contexto de Adobe Experience Platform en las reglas de decisión y fórmulas de clasificación. [Más información](../experience-decisioning/context-data.md)
* **Nuevo permiso** : Ya está disponible un nuevo permiso para &quot;Administrar decisiones de experiencia&quot; para el recurso Administración de decisiones. Permite administrar derechos relacionados con Experience Decisioning. [Más información](../experience-decisioning/gs-experience-decisioning.md)
* **Reglas de límite** : Ahora puede agregar varias reglas de límite para un elemento de decisión determinado en Experience Decisioning. Esto le permite aumentar el nivel de control sobre la forma en que se envían las ofertas. [Más información](../experience-decisioning/items.md#capping)
* **Informes** : Ahora puede crear paneles de informes personalizados de campañas de Experience Decisioning mediante [!DNL Customer Journey Analytics]. [Más información](../experience-decisioning/cja-reporting.md)


**Gestión de decisiones**

* **Compatibilidad con varias reglas** : Ahora puede añadir hasta 10 reglas de límite para una oferta determinada en Gestión de decisiones. Esto le permite aumentar el nivel de control sobre la forma en que se envían las ofertas.
* **Auditorías** - El **Registro de cambios** que le permite ver todos los cambios realizados en una oferta o que se ha eliminado una decisión. Los cambios relacionados con ofertas y decisiones ahora se pueden ver en el menú **Auditorías**.


**Canal de correo electrónico**

* **Cancelación de suscripción a lista** - Después de los recientes anuncios de Gmail y Yahoo para remitentes masivos, Journey Optimizer admite la opción de cancelación de suscripción a una lista &quot;posterior/1 clic&quot;.
* **Puntuación de spam** (Beta): Ahora puede comprobar la puntuación de correo no deseado del contenido en un informe de correo no deseado dedicado. Con SpamAssassin, Adobe Journey Optimizer ahora puede probar el contenido del correo electrónico y asignarle una puntuación para indicar si los proveedores de ISP lo considerarán como correo no deseado o no. [Más información](../content-management/spam-report.md)


**Públicos**

* El uso de audiencias y atributos de composición de audiencias y carga personalizada (archivo CSV) ya está disponible para su uso con Healthcare Shield o Privacy and Security Shield.

**Personalización**

* **Fragmento de expresión** - Los fragmentos de expresiones ya están disponibles para **Canal en la aplicación**. [Más información](../personalization/use-expression-fragments.md)

**Recorridos**

* **Políticas de combinación** (Disponibilidad limitada): Las políticas de combinación utilizadas por un recorrido ahora son visibles y coherentes en todo el recorrido.
* **Compatibilidad con mTLS** : el protocolo mTLS ahora se admite en las API de Journey Optimizer y en las acciones personalizadas.
* **Tablas de búsqueda en eventos** - Ahora puede aprovechar los datos de un conjunto de datos de búsqueda cuando se ha definido una relación con un atributo dentro de una matriz de objetos. Los valores de búsqueda estarán disponibles en recorridos (condiciones, acciones personalizadas, etc.) y personalización de mensajes.
