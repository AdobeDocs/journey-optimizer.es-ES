---
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 76eb73e875cbdeb7b5821f0c63435cf96c532adc
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 35%

---

# Notas de la versión {#release-notes}

En esta página se enumeran todas las nuevas funciones y mejoras de [!DNL Journey Optimizer]. También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Lanzamiento de mayo de 2022 {#may-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Reglas de frecuencia de mensaje</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede establecer reglas comerciales multicanal que excluyan automáticamente los perfiles saturados de mensajes y acciones.</p>
<img src="assets/frequency-rn.gif"/>
<p>Para obtener más información, consulte la <a href="../configuration/frequency-rules.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Email BCC</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Availability date: <strong>May, 31</strong></p>
<p>You can now use the Email BCC (blind carbon copy) capability to store emails sent by Adobe Journey Optimizer. Enable this option in your email presets so that every email sent is blind-copied to your BCC address.</p>
<img src="assets/bcc-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/email-settings.md#bcc-email">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Administración de decisiones: modelo de optimización automática de la clasificación de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar sistemas de modelos formados en Administración de decisiones. Esta nueva capacidad clasifica las ofertas que se muestran para un perfil determinado.</p>
<img src="assets/optimization.gif"/>
<p>Para obtener más información, consulte la <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Registros de auditoría de Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede supervisar las acciones realizadas por los usuarios en los recursos de Adobe Journey Optimizer.</p>
<img src="assets/audit-rn.gif"/>
<p>Para obtener más información, consulte la <a href="../reports/audit-logs.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Personalización**

* **Nueva función de ayuda para la ocultación de caracteres** - El `mask` la función de ayuda le permite reemplazar una parte de una cadena con caracteres &quot;X&quot;. [Más información](../personalization/functions/string.md#mask)

**Páginas de aterrizaje**

* **Páginas de aterrizaje sin formulario** - Ahora puede crear y publicar una página de aterrizaje que no contenga un formulario y que no requiera que los visitantes realicen ninguna acción.
* **Plantillas de página de aterrizaje** : Ahora puede guardar una página de aterrizaje como plantilla y reutilizarla al crear otras páginas de aterrizaje. [Más información](../landing-pages/lp-templates.md)
* **Volver a la página principal** - Ahora puede agregar un vínculo a la página principal desde cualquier subpágina dentro de la misma página de aterrizaje.
* **Compatibilidad con JavaScript personalizado** - Ahora puede agregar JavaScript personalizado al contenido de la página de aterrizaje para realizar estilos avanzados o agregar comportamientos personalizados a las páginas de aterrizaje.	[Más información](../landing-pages/lp-custom-js.md)

<!--**Decision management**

* **HTML and JSON files support** - You can now drag and drop external HTML and JSON files from the AEM repository into the offer representation content.-->

**Recorridos**

* **Leer segmento** - Los recorridos de segmento de lectura de una sola toma ahora pasan al estado Finalizado 30 días después de la ejecución del recorrido. Para segmentos de lectura programados, son 30 días después de la ejecución de la última incidencia. [Más información](../building-journeys/read-segment.md)
* **Editor de expresiones** - El [límite](../building-journeys/functions/functionlimit.md) para permitirle limitar el número de elementos de una lista. La variable [sort](../building-journeys/functions/functionsort.md) ahora permite ordenar un objeto de lista. La compatibilidad de listObject también se ha agregado al [disctinct](../building-journeys/functions/functiondistinct.md) y [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) funciones.
