---
solution: Journey Optimizer
product: journey optimizer
title: Correcciones de marca con tecnología de IA
description: Aprenda a configurar y utilizar correcciones de marca impulsadas por IA en Adobe Journey Optimizer.
feature: Brand Guidelines
topic: Content Management
role: User
level: Intermediate
exl-id: a872a3a4-f05b-439d-923e-5191b6e06d34
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 1016
ht-degree: 3%

---


# Correcciones de marca con tecnología de IA y sugerencias editoriales {#brand-corrections-ai}

>[!AVAILABILITY]
>
>Esta capacidad está disponible para los usuarios de Adobe Journey Optimizer con directrices de marca activas y derechos de asistente de IA. Póngase en contacto con su representante de Adobe para obtener más información.

## Información general {#overview}

Adobe Journey Optimizer amplía su herramienta de conformidad de marca basada en GenAI en todos los canales de contenido admitidos: SMS, notificaciones push, contenido web y correo electrónico. Cuando el motor de control de calidad de la marca detecta contenido que infringe las directrices de la marca o falla en los criterios de calidad editorial, el sistema genera automáticamente alternativas corregidas que puede revisar y aplicar directamente dentro del flujo de trabajo de creación.

Esto transforma la validación de marca de una lista de comprobación pasiva en una experiencia activa de corrección sobre la marcha. En lugar de identificar infracciones y volver al editor para resolver cada problema manualmente, los autores de contenido reciben sugerencias dirigidas y generadas por IA que se alinean con las directrices de voz, tono y estilo de marca establecidas de la organización, todo sin salir del editor de contenido.

Esta función está diseñada para especialistas en marketing de contenido, redactores de textos y operadores de campañas que necesiten mover contenido de borrador a activación rápidamente, manteniendo al mismo tiempo el cumplimiento de la marca a escala.

## Requisitos previos {#prerequisites}

Antes de usar correcciones de marca impulsadas por IA, confirme lo siguiente:

- **Directrices de marca** están configuradas en Adobe Journey Optimizer. Sin un perfil de marca activo, el sistema no puede generar sugerencias de corrección alineadas con la marca.
- La característica **AI Assistant** está habilitada para su organización de Adobe Experience Cloud.
- Tiene los permisos adecuados para crear y editar contenido para el canal correspondiente (SMS, push, web o correo electrónico).
- Hay al menos un elemento de contenido disponible para su revisión en el editor de contenido de Journey Optimizer.

>[!NOTE]
>
>Las sugerencias de corrección de marca se generan mediante la infraestructura de IA generativa de Adobe y están sujetas a las políticas de uso del asistente de IA aplicables a su organización. Revise siempre las sugerencias aceptadas antes de publicar.

## Funcionamiento {#how-it-works}

Las correcciones de marca se integran directamente en el flujo de validación de control de calidad de la marca dentro del editor de contenido de Journey Optimizer. El proceso de extremo a extremo funciona de la siguiente manera.

**Paso 1: Examen de control de calidad de la marca**: al ejecutar una comprobación de validación de marca en el contenido (ya sea manualmente desde el panel de revisión o desencadenada por una regla de flujo de trabajo), el sistema evalúa cada bloque de contenido en función de las directrices de marca configuradas. Las comprobaciones cubren el tono de voz, la terminología, el idioma prohibido, las normas editoriales y los requisitos reglamentarios.

**Paso 2 — Detección y marcado de infracciones**: Cualquier segmento de contenido que no cumpla los criterios de calidad de la marca o editorial se marcará con un indicador de infracción. El tipo de infracción (por ejemplo, discrepancia de tono, uso de términos prohibido o incumplimiento de directrices) se muestra junto al segmento marcado para que los autores entiendan exactamente qué debe cambiar.

**Paso 3: generación de sugerencias de IA**: Para cada segmento marcado, Journey Optimizer genera automáticamente una o más alternativas corregidas mediante el Asistente de IA. Las sugerencias se basan en las directrices de marca activas, lo que garantiza que el texto recomendado refleje la voz, la terminología y el estilo editorial correctos y específicos de su organización.

**Paso 4 — Previsualización y revisión en línea**: las correcciones sugeridas aparecen en línea, directamente adyacentes al contenido marcado en el panel lateral de control de calidad de la marca. Puede comparar el texto original con la alternativa generada por IA sin salir del editor.

**Paso 5 — Aceptar o descartar**: acepte una sugerencia con un solo clic para reemplazar el contenido marcado con la versión corregida. Como alternativa, descarte la sugerencia y edite el contenido manualmente. Al aceptar una sugerencia, se actualiza inmediatamente el bloque de contenido y se marca la infracción como resuelta en el panel Control de calidad.

**Paso 6 — Nueva validación**: después de aplicar las correcciones, vuelva a ejecutar el análisis de control de calidad de la marca para confirmar que todas las infracciones se han resuelto antes de publicar o activar el contenido en un recorrido o campaña.

## Configurar {#configure}

No se requiere ninguna configuración adicional más allá de los requisitos previos estándar. La función se activa automáticamente en el panel de control de calidad de la marca cuando se asocia un perfil de marca al contenido y el asistente de IA está habilitado para su organización.

Para empezar a utilizar correcciones de marca con tecnología de IA:

1. Abra el editor de contenido para el canal correspondiente: SMS, notificación push, web o correo electrónico.
2. En la barra de herramientas del editor, seleccione **Directrices de marca** y elija el perfil de marca aplicable en el menú desplegable.
3. Redacta o abre el contenido y, a continuación, selecciona **Control de calidad de la marca** en el panel de revisión para iniciar un análisis.
4. Revise las infracciones marcadas en el panel lateral **Control de calidad de la marca**. Para cada elemento marcado, aparece automáticamente una sugerencia generada por IA.
5. Haga clic en **Aplicar** para aceptar una sugerencia o en **Descartar** para controlar la corrección manualmente.
6. Vuelva a ejecutar **Brand QA** para verificar que se hayan resuelto todas las infracciones y luego continúe con el flujo de trabajo de aprobación o activación estándar.

### Canales admitidos {#supported-channels}

Las correcciones de marca con tecnología de IA están disponibles en los siguientes tipos de contenido en Adobe Journey Optimizer:

| Canal | Elementos de contenido admitidos |
|---|---|
| **Correo electrónico** | Línea de asunto, encabezado previo, texto independiente, etiquetas CTA |
| **SMS** | Cuerpo del mensaje |
| **Notificaciones push** | Título, texto independiente |
| **Web** | Titular, texto independiente, etiquetas de botón |

>[!NOTE]
>
>Los elementos de contenido admitidos pueden variar según la configuración del canal y las directrices de marca definidas en el perfil de marca. La validación de imágenes y recursos visuales no entra en el ámbito de las correcciones de texto generadas por IA.

## Ventajas principales {#key-benefits}

**Menor esfuerzo de edición manual**: los autores de contenido ya no necesitan hacer referencias cruzadas de las directrices de marca manualmente para cada problema marcado. Las sugerencias de IA presentan alternativas listas para aplicar, lo que reduce drásticamente el tiempo empleado en el ciclo de corrección.

**Cumplimiento coherente de la marca**: Las correcciones se basan en las mismas directrices de marca utilizadas para la validación. Las sugerencias aceptadas mantienen la coherencia con los estándares editoriales y de voz de marca aprobados en todos los canales, lo que reduce el riesgo de mensajes incoherentes en las campañas multicanal.

**Producción de contenido más rápida**: al convertir el control de calidad de la marca en un flujo de trabajo optimizado de corrección sobre la marcha, los equipos mueven el contenido a través del ciclo de revisión más rápidamente, lo que reduce el tiempo de respuesta entre el borrador y la activación. Los operadores de campaña pueden resolver un conjunto completo de infracciones en un solo paso sin cambiar entre herramientas.

**Cobertura en canales múltiples**: ya sea que produzca una campaña por SMS, una secuencia de mensajes push para móviles o un mensaje web en la aplicación, las sugerencias de corrección de marca estarán disponibles de manera consistente en todas las superficies de contenido compatibles, lo que garantiza que los estándares de marca se mantengan en todas las comunicaciones de su marca.

## Temas relacionados {#related-topics}

- [Introducción a las directrices de marca](../content-management/brands.md)
- [Uso del asistente de IA para generar contenido](../content-management/ai-assistant.md)
- [Creación de un mensaje SMS](../sms/create-sms.md)
- [Crear una notificación push](../push/create-push.md)
- [Introducción al canal web](../web/get-started-web.md)
- [Vista previa y prueba del contenido](../content-management/preview-test.md)
