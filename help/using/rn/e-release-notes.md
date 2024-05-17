---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 7addbcaf12611860c0dde239b68be54493b99bb9
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 25%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

**Las notas de la versión anteriores siguientes están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

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
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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
<p>La funcionalidad de reglas empresariales está disponible actualmente como una versión beta. Para unirse al programa beta, póngase en contacto con el representante del Adobe.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Experience Decisioning** (Disponibilidad limitada)

Desde la versión beta hasta esta versión, se han añadido las siguientes mejoras:

* **Experience Decisioning + Experiencias basadas en código** : Ahora puede aprovechar la función Experience Decisioning para utilizar elementos de decisión en sus campañas basadas en código. Nota: El canal de experiencia basado en código y Experience Decisioning no están disponibles para las organizaciones que han adquirido las ofertas adicionales Escudo de Adobe Healthcare y Escudo de privacidad y seguridad. [Más información](../code-based/get-started-code-based.md)
* **Datos de contexto** : ahora puede aprovechar los datos de contexto de Adobe Experience Platform en las reglas de decisión y fórmulas de clasificación. [Más información](../experience-decisioning/context-data.md)
* **Nuevo permiso** : Ya está disponible un nuevo permiso para &quot;Administrar decisiones de experiencia&quot; para el recurso Administración de decisiones. Permite administrar derechos relacionados con Experience Decisioning. [Más información](../experience-decisioning/gs-experience-decisioning.md)
* **Reglas de límite** : Ahora puede agregar varias reglas de límite para un elemento de decisión determinado en Experience Decisioning. Esto le permite aumentar el nivel de control sobre la forma en que se envían las ofertas. [Más información](../experience-decisioning/items.md#capping)
* **Informes** : Ahora puede crear paneles de informes personalizados de campañas de Experience Decisioning mediante [!DNL Customer Journey Analytics]. [Más información](../experience-decisioning/cja-reporting.md)


**Gestión de decisiones**

* **Compatibilidad con varias reglas** : Ahora puede añadir hasta 10 reglas de límite para una oferta determinada en Gestión de decisiones. Esto le permite aumentar el nivel de control sobre la forma en que se envían las ofertas.
* **Auditorías** - El **Registro de cambios** que le permite ver todos los cambios realizados en una oferta o que se ha eliminado una decisión. Los cambios relacionados con ofertas y decisiones ahora se pueden ver en el menú **Auditorías**.


**Canal de correo electrónico**

* **Cancelación de suscripción a lista** - Después de los recientes anuncios de Gmail y Yahoo para remitentes masivos, Journey Optimizer admite la opción de cancelación de suscripción a una lista &quot;posterior/1 clic&quot;.
* **Puntuación de spam** (Beta): Ahora puede comprobar la puntuación de correo no deseado del contenido en un informe de correo no deseado dedicado. Con SpamAssassin, Adobe Journey Optimizer ahora puede probar el contenido del correo electrónico y asignarle una puntuación para indicar si los proveedores de ISP lo considerarán como correo no deseado o no.
  <!--[Read more](../content-management/spam-report.md)-->

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

**Personalización**

* **Fragmento de expresión** - Los fragmentos de expresiones ya están disponibles para **Canal en la aplicación**.
  <!--[Read more](../personalization/use-expression-fragments.md)-->

**Recorridos**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Compatibilidad con mTLS** - La autenticación mTLS ahora se admite en acciones personalizadas. No se requiere ninguna configuración adicional en la acción personalizada o en el recorrido para activar mTLS; se produce automáticamente cuando se detecta un punto de conexión habilitado para mTLS.
* **Tablas de búsqueda en eventos** - Ahora puede aprovechar los datos de un conjunto de datos de búsqueda cuando se ha definido una relación con un atributo dentro de una matriz de objetos. Los valores de búsqueda estarán disponibles en recorridos (condiciones, acciones personalizadas, etc.) y personalización de mensajes.
