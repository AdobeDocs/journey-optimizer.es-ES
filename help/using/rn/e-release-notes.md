---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: b3e5a825b881736516b3bcd1d368843c3a601100
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 23%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la primera versión están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md), en la fecha de la versión.

## Notas de la versión anteriores de septiembre de 2023 {#sept-rn-2023}

**Fecha de lanzamiento**: 26-27 de septiembre de 2023

### Nuevas funciones{#sept-2023-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.


<table>
<thead>
<tr>
<th><strong>Informes de canales consolidados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La función Informe de canal ofrece a analistas y expertos en marketing una descripción general completa de las métricas de tráfico y participación a nivel de canal. Para acceder al menú "Informe", debe tener el permiso "Ver informes de canal".</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Destinos de exportación de conjuntos de datos (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La exportación de conjuntos de datos de Journey Optimizer a destinos de almacenamiento en la nube ya está disponible de forma general. Ahora, puede establecer una conexión activa con las ubicaciones de almacenamiento en la nube para exportar el contenido de los conjuntos de datos.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Almacenamiento de credenciales de aplicación móvil por zona protegida</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta nueva función le permite administrar y asociar fácilmente credenciales push con una zona protegida dedicada en las superficies de la aplicación.</p>
<p>Para obtener más información, consulte la <a href="../in-app/inapp-configuration.md">documentación detallada</a>.</p>
</tr>
</tbody>
</table>

### Mejoras {#sept-2023-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**Personalización**

* Además de los fragmentos visuales, ahora es posible crear, guardar y reutilizar fragmentos de expresiones desde la interfaz de Journey Optimizer a través del Editor de expresiones. Los fragmentos de expresión reemplazan a las expresiones guardadas anteriormente.
* Ahora puede utilizar atributos calculados de Adobe Experience Platform para la personalización en Journey Optimizer. Los atributos calculados son valores agregados que se calculan en función de conjuntos de datos de evento de experiencia con perfil habilitado introducidos en Adobe Experience Platform.

**Alerta**

* Se ha introducido un nuevo tipo de alerta del sistema. Ahora puede recibir notificaciones cuando falle una audiencia de lectura.

**Canal web**

* SPA Ahora, las aplicaciones de una sola página () se pueden crear en el editor visual del diseñador web, lo que le permite seleccionar a qué vistas específicas desea aplicar las modificaciones de la página web. Una vista puede definirse como un sitio completo o como un grupo de elementos visuales en un sitio, como la página de inicio, la totalidad del sitio de productos o el marco de preferencias de envío en todas las páginas de cierre de compra. Para crear y ejecutar campañas web de Adobe Journey Optimizer SPA en el tiempo de ejecución, se necesita una configuración de desarrollador única para definir las vistas en la implementación del SDK web de Adobe Experience Platform.

* Al editar una página con el diseñador web, ahora puede agregar nuevos cambios al contenido directamente desde el **Modificaciones** panel: sin necesidad de seleccionar un componente y editarlo desde la interfaz del diseñador.
* Al configurar subdominios web, ahora tiene la opción de agregar su propio subdominio, además de utilizar un subdominio ya delegado al Adobe.

**Recorridos**

* La compatibilidad con las respuestas de acciones personalizadas ahora es GA. Esto le permite aprovechar las respuestas de llamadas de API en acciones personalizadas y organizar el recorrido en función de estas respuestas. Además, se ha añadido una nueva protección para limitar todas las acciones aduaneras a 5000 llamadas/s por punto final.
* Al duplicar un recorrido, ahora puede definir el nombre de la copia de recorrido.

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**Canal de correo electrónico**

Una nueva opción en la configuración de superficie de correo electrónico permite elegir enviar mensajes transaccionales a perfiles incluso si sus direcciones de correo electrónico están en la lista de supresión de Adobe Journey Optimizer.

**Canal de SMS**

Dos campos nuevos, **Mensaje de inclusión** y **Mensaje de ayuda**, se han agregado a la pantalla de configuración de la API, lo que permite a los usuarios personalizar las respuestas para palabras clave entrantes. Tenga en cuenta que esto solo está disponible para el proveedor de SMS de Sinch.

**Creación de informes**

Ahora puede exportar informes de Journey Optimizer como archivo CSV. [Más información](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->