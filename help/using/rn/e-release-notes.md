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
source-git-commit: 4b779d297769bd7a0b6913a0142ee7be7775ba04
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 36%

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
<p>Ahora puede crear reglas de límite de frecuencia granulares y aplicarlas a diferentes tipos de comunicaciones de marketing a través de conjuntos de reglas. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Compatibilidad con varias entidades para la búsqueda local: beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Por determinar</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Experience Decisioning**

Desde la versión beta a LA, se han añadido las siguientes mejoras:

* **Experience Decisioning + Experiencias basadas en código (LA)**: Ahora puede aprovechar la función Experience Decisioning para utilizar elementos de decisión en sus campañas basadas en código. Nota: El canal de experiencia basado en código y Experience Decisioning no están disponibles para las organizaciones que han adquirido las ofertas adicionales Escudo de Adobe Healthcare y Escudo de privacidad y seguridad. [Más información](../code-based/get-started-code-based.md)
* Ahora puede aprovechar los datos de contexto de Adobe Experience Platform en las reglas de decisión y fórmulas de clasificación. [Más información](../experience-decisioning/context-data.md)
* Ya está disponible un nuevo permiso para “Administrar decisiones sobre experiencias” para el recurso Gestión de decisiones. Permite administrar derechos relacionados con Experience Decisioning. [Más información](../experience-decisioning/gs-experience-decisioning.md)
* Ahora puede añadir varias reglas de límite para un elemento de decisión determinado en la toma de decisiones sobre experiencias. Esto le permite aumentar el nivel de control sobre la forma en que se envían las ofertas. [Más información](../experience-decisioning/items.md#capping)
* Ahora puede crear paneles de informes personalizados de campañas de Experience Decisioning mediante [!DNL Customer Journey Analytics]. [Más información](../experience-decisioning/cja-reporting.md)


**Toma de decisiones sobre ofertas**

* **Compatibilidad con varias reglas** : Ahora puede añadir hasta 10 reglas de límite para una oferta determinada en Gestión de decisiones. Esto le permite aumentar el nivel de control sobre la forma en que se envían las ofertas.
* **Auditorías** - El **Registro de cambios** que le permite ver todos los cambios realizados en una oferta o que se ha eliminado una decisión. Los cambios relacionados con ofertas y decisiones ahora se pueden ver en el menú **Auditorías**.


**Cancelación de suscripción a lista**

* Después de los recientes anuncios de Gmail y Yahoo para remitentes masivos, Journey Optimizer admite la opción de cancelación de suscripción a una lista &quot;posterior/1 clic&quot;.

**Públicos**

* El uso de audiencias y atributos de composición de audiencias y carga personalizada (archivo CSV) ya está disponible para su uso con Healthcare Shield o Privacy and Security Shield.

**Personalización**

* **Tabla de búsqueda** - Ahora puede aprovechar los datos de un conjunto de datos de búsqueda cuando se ha definido una relación con un atributo dentro de una matriz de objetos. Los valores de búsqueda estarán disponibles en recorridos (condiciones, acciones personalizadas, etc.) y personalización de mensajes.
* **Fragmento de expresión** : Los fragmentos de expresiones ya están disponibles para el canal en la aplicación.

**Recorridos**

* **Políticas de combinación** - Las políticas de combinación ahora se pueden configurar y utilizar en los recorridos.
* **Compatibilidad con mTLS** : el protocolo mTLS ahora se admite en las API de Journey Optimizer y en las acciones personalizadas.
