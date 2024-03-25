---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
hide: true
hidefromtoc: true
source-git-commit: f957737aa741cc8b854912414d15154489d1b0b0
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 100%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

## Notas de la versión preliminar de marzo de 2024 {#e-2024}

**Fecha de lanzamiento**: 19 y 20 de marzo de 2024

### Nuevas funciones {#e-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.

<table>
<thead>
<tr>
<th><strong>Experiencias basadas en código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con el nuevo canal de experiencia basado en código, Adobe Journey Optimizer le permite realizar personalizaciones y pruebas avanzadas para cualquiera de sus propiedades de entrada, lo que permite ofrecer experiencias adaptadas en diversos puntos de contacto, como aplicaciones web, aplicaciones móviles, aplicaciones de escritorio, consolas de vídeo, dispositivos conectados a TV, televisores inteligentes, quioscos, cajeros automáticos, dispositivos IoT y mucho más.</p>
<P>Las funcionalidades clave incluyen:</p>
<ul><li> Personalización universal: amplíe las experiencias personalizadas en todos los puntos de contacto, lo que garantiza un recorrido de usuario coherente y personalizado</li>
<li>Precisión de edición granular: editar contenido específico en ubicaciones individuales dentro de sus aplicaciones o páginas web</li>
<li>Implementación versátil: compatibilidad con métodos de implementación del lado del servidor, basados en API o basados en SDK para integrarse sin problemas con su entorno de desarrollo.</li></ul></p>
<p>Para obtener más información, consulte la <a href="../code-based/get-started-code-based.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/code-based.gif">
</tr>
</tbody>
</table>

### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Plantillas de contenido**

* **Miniaturas**: ahora, hay un modo **Vista de cuadrícula** disponible para plantillas de contenido, mostrando miniaturas a fin de mejorar el acceso visual. Actualmente, solo se admiten plantillas de HTML de correo electrónico. [Más información](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Esta capacidad se lanza con disponibilidad limitada (LA) para un pequeño conjunto de clientes.

**Recorridos**

Se han añadido nuevos estados intermedios al ciclo vital de creación de recorridos:

* Estado de **Publicación** entre el estado **Borrador** y el estado **Activo**
* Estado **Deteniendo** entre los estados **Activo** y **Detenido**
* Estados **Activando modo de prueba** o **Desactivando modo de prueba** entre el estado **Borrador** y el estado **Borrador (pruebas)**

Cuando un recorrido está en un estado intermedio, es de solo lectura.