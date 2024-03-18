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
source-git-commit: 4b3ec38154d01eb3f15c30c26b427ee34a324be7
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 27%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan al final de cada mes en la [notas de la versión](release-notes.md).

Las notas de la primera versión están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

## Notas de la versión anteriores de marzo de 2024 {#e-2024}

**Fecha de lanzamiento**: 19 y 20 de marzo de 2024

### Nueva capacidad {#e-features}

Esta versión incorpora la nueva funcionalidad detallada a continuación.

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
<ul><li> Personalización universal: Amplíe las experiencias personalizadas en todos los puntos de contacto, lo que garantiza un recorrido de usuario coherente y personalizado</li>
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

* **Miniatura** - A **vista de miniaturas** ya está disponible para plantillas de contenido y fragmentos para mejorar el acceso visual. [Más información](../content-management/content-templates.md#template-thumbnails)

**Recorridos**

Se han añadido nuevos estados intermedios al ciclo vital de creación de recorridos:

* **Publicación** estado entre las variables **Borrador** estado y el **Activo** status
* **Deteniendo** estado entre las variables **Activo** estado y el **Detenido** status
* **Activando modo de prueba** o **Desactivando modo de prueba** estados entre los **Borrador** estado y el **Borrador (pruebas)** status
