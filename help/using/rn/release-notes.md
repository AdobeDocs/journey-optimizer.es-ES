---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: e80554570d62d1ddb52516366be55711387c5d19
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 40%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.


## Notas de la versión de marzo de 2025 {#25-3-rn}


### Nuevas funciones {#25-03-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Integración con Adobe Express (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La integración de Adobe Express en Adobe Journey Optimizer permite utilizar las herramientas de edición de Adobe Express directamente durante la creación de contenido, lo que permite cambiar el tamaño, eliminar fondos, recortar y convertir recursos a JPEG o PNG.<p>
<p>Actualmente, la integración de Adobe Express en Adobe Journey Optimizer solo está disponible para un conjunto de organizaciones (disponibilidad limitada). No se puede implementar para su uso con Healthcare Shield o Privacy and Security Shield.</p>
<p>Para obtener más información, consulte la <a href="../integrations/express.md">documentación detallada</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>métricas de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya están disponibles las métricas de recorridos, lo que le permite medir el impacto de sus actividades en las métricas clave de su empresa y proporcionar información más clara sobre su rendimiento.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/success-metrics.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Integración con Dynamic Media (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los recursos de Dynamic Media ahora están disponibles y accesibles directamente en Journey Optimizer. Esta integración le permite:
<ul>
<li>Administración centralizada de recursos con actualizaciones en tiempo real</li>
<li>Modifique la configuración de los recursos, como la anchura y la altura, al instante</li>
<li>Personalice las plantillas de Dynamic Media actualizando el contenido y añadiendo campos de personalización</li>
</ul>
<p>
<p>Esta integración solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../integrations/aem-dynamic.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Integración con Adobe GenStudio (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para mejorar la eficacia del marketing y mantener la coherencia de la marca, ahora puede integrar sin problemas las experiencias de GenStudio for Performance Marketing con Journey Optimizer. Esto le permite aprovechar la creación de contenido con potencia IA de GenStudio junto con las funcionalidades de orquestación avanzadas de Journey Optimizer.<p>
<p>El uso de la integración de GenStudio en Journey Optimizer no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield (disponibilidad limitada).</p>
<p>Para obtener más información, consulte la <a href="../integrations/genstudio.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### Mejoras {#25-03-improv}

**Editor de Personalization** (fecha de disponibilidad: 12 de marzo)

El editor de personalización de Journey Optimizer se ha actualizado con nuevas funciones:
* **Diseño actualizado del editor de código**: una interfaz más clara y moderna para mejorar la facilidad de uso y el enfoque.
* **Buscar y reemplazar**: funcionalidad añadida para buscar y reemplazar contenido rápidamente en el editor.
* **Compatibilidad con Deshacer y Rehacer**: permite revertir o volver a aplicar fácilmente los cambios.
* **Tamaño de fuente personalizable**: habilita el ajuste del tamaño de fuente del editor para mejorar la legibilidad.
* **Validación JSON en línea**: proporciona validación en tiempo real del lado del cliente para el contenido JSON a fin de acelerar la detección de errores.
* **Completar automáticamente atributos de perfil y contexto**: ofrece sugerencias inteligentes para optimizar la creación de contenido.
* **Resaltado de sintaxis mejorado**: mejora la legibilidad al hacer que la estructura del código quede visualmente más diferenciada.

![Vídeo que muestra la nueva función en el editor de Personalization](assets/do-not-localize/personalization-editor.gif)

Para obtener más información, consulte la [documentación detallada](../personalization/personalization-build-expressions.md).

**Aprobaciones**

Al definir las condiciones de una directiva de aprobación, ahora tiene la opción de filtrar por Etiqueta o Categoría de objeto.

Para obtener más información, consulte la [documentación detallada](../test-approve/approval-policies.md).

Configuración de ****

* Ahora puede asignar etiquetas unificadas de Adobe Experience Platform a las configuraciones de canal. Esto le permite clasificarlas fácilmente y mejorar la búsqueda y la navegación en todas las listas. [Más información](../configuration/channel-surfaces.md#channel-config-tags)

* Al configurar o editar un subdominio de correo electrónico en Journey Optimizer, ahora puede elegir administrar el registro de DMARC asociado por su cuenta, si está disponible en el dominio principal. [Más información](../configuration/dmarc-record.md#set-up-dmarc)

**Reglas de negocio**

Ahora puede utilizar un límite de frecuencia diario en recorridos y campañas con segmentación por lotes. Para garantizar la precisión de las reglas de límite de frecuencia diarias, asegúrese de elegir el área de nombres de prioridad más alta durante la creación de una campaña o recorrido. Obtenga más información sobre la prioridad del área de nombres en la [Guía del servicio de identidad de Platform](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

Como recordatorio, el límite de frecuencia diario en los conjuntos de reglas solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

Para obtener más información sobre las reglas de negocio, consulte la [documentación detallada](../configuration/rule-sets.md).

<!--**Content management**

To easily manage your fragments and your content templates, you can now use folders to organize them more effectively into a structured hierarchy. This improvement is only available for a set of organizations (Limited Availability). <!--To gain access, contact your Adobe representative.

**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->


