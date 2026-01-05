---
solution: Journey Optimizer
product: Journey Optimizer
title: Prueba, validación y aprobación
description: Descubra todas las funcionalidades de prueba y aprobación en Journey Optimizer. Previsualizar contenido, simular recorridos, validar correos electrónicos, ejecutar experimentos, detectar conflictos y configurar flujos de trabajo de aprobación antes del lanzamiento.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: probar, validar, aprobar, aprobación, garantía de calidad, control de calidad, perfiles de prueba, personalización, procesamiento, comprobación de spam, experimento de contenido, prueba a/b, detección de conflictos, lista semilla, pruebas, datos de muestra, flujo de trabajo de aprobación, prueba de correo electrónico, flujo de trabajo de validación
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: 57f32088aa9cef55ed68729995326d3eae401bd5
workflow-type: tm+mt
source-wordcount: '3103'
ht-degree: 5%

---

# Prueba, validación y aprobación{#section-overview}

Esta sección cubre todas las funcionalidades de prueba y aprobación de Journey Optimizer. Encontrará herramientas para obtener una vista previa del contenido con perfiles de prueba, validar la lógica de recorrido, comprobar el procesamiento de los correos electrónicos y las puntuaciones de spam, ejecutar experimentos A/B, detectar conflictos y configurar flujos de trabajo de aprobación.

Esta página de aterrizaje le ayuda a elegir el método de prueba adecuado según lo que esté creando (campañas frente a recorridos), le guía por los flujos de trabajo de prueba recomendados y le proporciona un acceso rápido a todos los recursos de prueba y aprobación. Empiece por [Elija su método de prueba](#choose-your-testing-approach) a continuación para identificar qué herramientas se aplican a su caso de uso.

## Resumen de funcionalidades de prueba

**Tipos de pruebas disponibles:**

* Prueba de contenido: Previsualice y valide el contenido del mensaje antes de enviar → [Campañas de prueba](#testing-campaigns), [Prueba de personalización](#testing-personalization)
* Prueba de lógica de recorrido: simular la progresión del cliente mediante rutas de recorrido → [recorridos de prueba](#testing-journeys)
* Pruebas técnicas: Validar el procesamiento, la entrega y la autenticación → [Validación técnica](#2-technical-validation)
* Pruebas de rendimiento: compare variaciones de contenido mediante experimentos A/B → [experimentos de contenido](#content-experiments--ab-testing)
* Pruebas de conflictos: Detectar superposiciones de campañas y recorridos → [Detección de conflictos](#conflict-detection)
* Pruebas de aprobación: flujos de trabajo de revisión estructurados antes de la activación → [Flujos de trabajo de aprobación](#approval-workflows-for-journeys-and-campaigns)

**Funcionalidades clave por contexto:**

| Capacidad | Se aplica a | Restricciones de canal | Requisitos previos | Objetivo principal | Documentación |
|------------|-----------|---------------------|--------------|-----------------|---------------|
| [Perfiles de prueba](../using/content-management/test-profiles.md) | Campañas, Recorridos | Todos los canales | Perfiles de prueba creados | Previsualización de contenido personalizado | [Guía](#testing-campaigns) |
| [Datos de entrada de muestra](../test-approve/simulate-sample-input.md) | Campañas, Recorridos | Correo electrónico, SMS, push, web, basado en código, aplicación, tarjetas de contenido | Archivo CSV/JSON | Prueba de varias variantes de personalización | [Guía](#simulate-content-variations) |
| [Modo de prueba](../using/building-journeys/testing-the-journey.md) | Solo recorridos | N/A | Recorrido de borrador, área de nombres configurada | Simular progresión de perfil | [Tarjeta](#test-your-journey) |
| [Ejecución en seco](../using/building-journeys/journey-dry-run.md) | Solo recorridos | N/A | Recorrido creado | Analizar rutas de ejecución | [Tarjeta](#journey-dry-run) |
| [Representación de correo electrónico](../using/content-management/rendering.md) | Campañas, Recorridos | Solo correo electrónico | Integración de Litmus | Verificar la visualización entre clientes | [Flujo de trabajo](#2-technical-validation) |
| [Puntuación de spam](../using/content-management/spam-report.md) | Campañas, Recorridos | Solo correo electrónico | Ninguna | Validación de entrega | [Flujo de trabajo](#2-technical-validation) |
| [Listas semilla](../using/configuration/seed-lists.md) | Campañas, Recorridos | Solo correo electrónico | Lista semilla configurada | Supervisión de las partes interesadas | [Tarjeta](#seed-lists-for-stakeholder-monitoring) |
| [Experimentos de contenido](../using/content-management/get-started-experiment.md) | Solo campañas | Todos los canales | Ninguna | Pruebas A/B y multi-armed bandit | [Tarjeta](#content-experiments--ab-testing) |
| [Detección de conflictos](../using/conflict-prioritization/conflicts.md) | Campañas, Recorridos (limitado) | Todos los canales | Ninguna | Evitar mensajes excesivos de los clientes | [Tarjeta](#conflict-detection) |
| [Flujos de trabajo de aprobación](../using/test-approve/gs-approval.md) | Campañas, Recorridos | Todos los canales | Directiva de aprobación creada | Proceso de revisión estructurado | [Tarjeta](#approval-workflows-for-journeys-and-campaigns) |
| [patio de recreo de Personalization](../using/personalization/personalize.md#playground) | Todas | Todos los canales | Ninguna | Aprendizaje y prueba de la sintaxis de personalización | [Tarjeta](#personalization-playground) |

**Flujos de trabajo de pruebas comunes:**

1. Desarrollo previo: use [área de reproducción de personalización](#testing-personalization) para aprender sintaxis
2. Durante el desarrollo: vista previa con [perfiles de prueba](#testing-campaigns), validar con [datos de entrada de muestra](#simulate-content-variations)
3. Antes del inicio: ejecutar [pruebas técnicas](#2-technical-validation) (procesamiento, correo no deseado), comprobar [conflictos](#conflict-detection), enviar para [aprobación](#approval-workflows-for-journeys-and-campaigns)
4. Después del inicio: supervisar con informes en directo (consulte [supervisión y solución de problemas](#monitoring--troubleshooting)), repetir según los resultados


## Por qué importan las pruebas y la aprobación

Los procesos de prueba y aprobación sirven como puertas de calidad esenciales que protegen la reputación de su marca y garantizan el éxito de la campaña. He aquí por qué importan:

* **Detecte errores antes de que lleguen a los clientes**: identifique los vínculos rotos, la personalización incorrecta, los problemas de procesamiento y los errores lógicos en un entorno controlado en el que las correcciones sean rápidas y sin riesgos.

* **Mejore la capacidad de envío**: pruebe las puntuaciones de spam, valide la autenticación de correos electrónicos y compruebe el procesamiento en todos los clientes de correo electrónico para maximizar la ubicación de la bandeja de entrada y las tasas de participación.

* **Garantizar la coherencia de la marca**: obtenga una vista previa del contenido con diferentes perfiles de prueba para verificar que la personalización se muestre correctamente para varios segmentos de clientes y mantenga los estándares de marca.

* **Validar recorridos complejos**: simule flujos de recorrido de varios pasos para confirmar que los déclencheur se activan correctamente, que las condiciones se evalúan correctamente y que los clientes reciben los mensajes correctos en el momento adecuado.

* **Establecer la responsabilidad**: Implemente flujos de trabajo de aprobación formales que requieran la firma de las partes interesadas, lo que crea una propiedad clara y reduce los inicios de campaña no autorizados o prematuros.

* **Ahorre tiempo y recursos**: detecte problemas al principio del ciclo de desarrollo cuando las correcciones sean más baratas y rápidas, lo que evitará costosas correcciones posteriores al inicio o escalaciones del servicio de atención al cliente.

## Terminología clave

**[Perfiles de prueba](../using/content-management/test-profiles.md)** = Perfiles de cliente sintéticos (clientes no reales) utilizados para previsualizar contenido personalizado. Marcado en el servicio de Perfil del cliente en tiempo real. Necesario para el modo de prueba y la previsualización de contenido. [Aprenda a crear perfiles de prueba](../using/audience/creating-test-profiles.md)

**[Modo de prueba](../using/building-journeys/testing-the-journey.md)** = característica de simulación de Recorrido que envía perfiles de prueba a través de rutas de recorrido. Limitaciones: solo recorridos de borrador, requiere área de nombres, solo perfiles de prueba. [Ver documentación del modo de prueba](../using/building-journeys/testing-the-journey.md)

**[Ejecución en seco](../using/building-journeys/journey-dry-run.md)** = Herramienta de análisis de ejecución de Recorrido que traza las rutas sin enviar mensajes ni realizar llamadas a la API. Caso de uso: Validación de la lógica sin consumir recursos. [Más información sobre la ejecución en seco](../using/building-journeys/journey-dry-run.md)

**[Datos de entrada de muestra](../test-approve/simulate-sample-input.md)** = Archivos CSV o JSON que contienen valores de atributo de perfil para probar la personalización. Admite hasta 30 variantes. Alternativa a la creación de perfiles de prueba. [Cómo simular variaciones de contenido](../test-approve/simulate-sample-input.md)

**[Listas semilla](../using/configuration/seed-lists.md)** = Direcciones de correo electrónico de las partes interesadas internas incluidas automáticamente en los envíos reales (no en los envíos de prueba). Solo canal de correo electrónico. Caso de uso: Monitorización de la calidad y cumplimiento normativo. [Configurar listas semilla](../using/configuration/seed-lists.md)

**[Experimentos de contenido](../using/content-management/get-started-experiment.md)** = Pruebas A/B o experimentos de bandidos multibrazo que comparan variaciones de contenido. Solo campañas, no disponible en recorridos. [Introducción a los experimentos](../using/content-management/get-started-experiment.md) | [Crear experimentos](../using/content-management/content-experiment.md)

**[Pruebas](../using/content-management/proofs.md)** = Probar los envíos de correo electrónico enviados a direcciones de correo electrónico específicas mediante datos de perfil de prueba. A diferencia de las listas semilla (las pruebas son envíos de prueba manuales, las listas semilla son copias automáticas de las partes interesadas). [Enviar pruebas](../using/content-management/proofs.md)

**[Detección de conflictos](../using/conflict-prioritization/conflicts.md)** = Herramienta que identifica campañas y recorridos superpuestos dirigidos a las mismas audiencias. Compatibilidad de recorrido limitada: tipos de audiencia unitarios, de calificación de audiencia y de lectura de audiencia solamente. [Más información acerca de la administración de conflictos](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Flujos de trabajo de aprobación](../using/test-approve/gs-approval.md)** = Proceso de revisión de varios pasos que requiere la aprobación de las partes interesadas antes de la activación. Requiere la configuración de directiva de aprobación. [Configurar aprobaciones](../using/test-approve/gs-approval.md) | [Crear directivas](../using/test-approve/approval-policies.md)

**[Pruebas de procesamiento](../using/content-management/rendering.md)** = Validación de visualización de correo electrónico entre clientes de correo electrónico (Gmail, Outlook, Apple Mail) y dispositivos. Requiere integración con Litmus. [Probar procesamiento de correo electrónico](../using/content-management/rendering.md)

**[Personalization playground](../using/personalization/personalize.md#playground)** = Entorno de aprendizaje interactivo para experimentar con sintaxis de personalización y expresiones de prueba con datos de ejemplo. No se requieren conjuntos de datos activos. [Acceso al área de reproducción](../using/personalization/personalize.md#playground)

## Árbol de decisiones para la selección de métodos de prueba

Utilice este árbol de decisión para identificar rápidamente las herramientas de prueba adecuadas para su escenario específico. Responda cada pregunta en función de su contexto (lo que está creando, lo que necesita validar y el canal que está utilizando) para navegar directamente a las funciones y la documentación relevantes.

+++ **Pregunta 1: ¿Qué estás probando?**

* Campaign → [Campañas de prueba](#testing-campaigns)
* Recorrido → [recorridos de prueba](#testing-journeys)
* Expresiones de Personalization → [Personalization playground](#testing-personalization)
+++

+++**Pregunta 2: ¿Qué aspecto necesita validación?**

* Contenido y personalización → [Perfiles de prueba](#testing-campaigns) o [datos de entrada de muestra](#simulate-content-variations)
* Visualización de correo electrónico → [Pruebas de procesamiento de correo electrónico](#2-technical-validation)
* Entrega → [Comprobaciones de puntuación de spam](#2-technical-validation)
* Recorrido lógica y flujo → [Modo de prueba](#testing-journeys) o [ejecución en seco](#journey-dry-run)
* Comparación de rendimiento → [Experimento de contenido](#content-experiments--ab-testing) (solo campañas)
* Conflictos de temporización → [Detección de conflictos](#conflict-detection)
* Revisión de partes interesadas → [Flujo de trabajo de aprobación](#approval-workflows-for-journeys-and-campaigns)
+++

+++**Pregunta 3: ¿Qué canal?**

* Correo electrónico → Todos los métodos de prueba disponibles (consulte [Pruebas de campañas](#testing-campaigns))
* SMS, Push → [prueba de contenido](#testing-campaigns), [datos de entrada de muestra](#simulate-content-variations), [flujos de trabajo de aprobación](#approval-workflows-for-journeys-and-campaigns)
* [Pruebas de contenido](#testing-campaigns), [datos de entrada de muestra](#simulate-content-variations), [flujos de trabajo de aprobación](#approval-workflows-for-journeys-and-campaigns) en la web, en la aplicación → basados en código
* Varios canales → Probar cada canal por separado
+++

+++**Pregunta 4: ¿En qué momento del flujo de trabajo?**

* Antes de crear → [área de reproducción de Personalization](#personalization-playground) para aprendizaje
* Durante la generación de → [perfiles de prueba](#testing-campaigns) y [datos de entrada de muestra](#simulate-content-variations) para la validación
* Antes del inicio → [Pruebas de procesamiento](#2-technical-validation), [comprobaciones de spam](#email-spam-report), [detección de conflictos](#conflict-detection), [aprobaciones](#approval-workflows-for-journeys-and-campaigns)
* Después del inicio → [Informes en vivo](../using/building-journeys/report-journey.md) y [monitoreo](#monitoring--troubleshooting)
+++


## Elija su método de prueba

El método de prueba adecuado depende de lo que esté creando y de lo que necesite validar. Utilice esta guía para identificar las herramientas de prueba más relevantes para su escenario.

### Prueba de campañas

**Para todas las campañas:**

* Previsualizar y probar contenido usando [perfiles de prueba](../using/content-management/test-profiles.md) o [datos de entrada de muestra](../test-approve/simulate-sample-input.md)
* Comprobar [procesamiento de correo electrónico](../using/content-management/rendering.md) entre dispositivos y clientes (solo canal de correo electrónico)
* Ejecutar [comprobaciones de puntuación de correo no deseado](../using/content-management/spam-report.md) (solo canal de correo electrónico)
* Revisar [conflictos](../using/conflict-prioritization/conflicts.md) con otras campañas y recorridos
* Configurar [listas semilla](../using/configuration/seed-lists.md) para la supervisión de partes interesadas (solo canal de correo electrónico)
* Enviar para [aprobación](../using/test-approve/gs-approval.md) antes de la activación

**Para pruebas A/B y optimización:**

* Cree [experimentos de contenido](../using/content-management/get-started-experiment.md) para probar varios tratamientos y medir el rendimiento

**Para campañas activadas por API:**

* Use la [API de simulación de campaña](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} para almacenar en déclencheur los trabajos de revisión mediante programación

### Prueba de recorridos

**Para todos los recorridos:**

* Utilice [modo de prueba](../using/building-journeys/testing-the-journey.md) para simular la progresión del perfil (solo recorridos de borrador, requiere área de nombres) o [ejecución en seco](../using/building-journeys/journey-dry-run.md) para analizar las rutas de ejecución sin enviar mensajes
* Probar mensajes individuales usando [vista previa y pruebas](../using/content-management/preview-test.md)
* Comprobar [conflictos](../using/conflict-prioritization/conflicts.md) con otros recorridos y campañas
* Enviar para [aprobación](../using/test-approve/gs-approval.md) antes de publicar

**Para recorridos complejos:**

* Utilice el modo de prueba y la ejecución en seco juntos para validar completamente la lógica de ramificación y las rutas de ejecución
* Prueba sistemática de diferentes condiciones de entrada y atributos de perfil

**Nota:** La detección de conflictos y la restricción de recorrido solo están disponibles para recorridos unitarios, de calificación de audiencias y de lectura de audiencias.

### Prueba de personalización

**Antes de generar contenido:**

* Experimente en el [área de reproducción de personalización](../using/personalization/personalize.md#playground) para aprender sintaxis y probar expresiones con datos de ejemplo

**Durante la creación del contenido:**

* Vista previa con [perfiles de prueba](../using/content-management/test-profiles.md) para validar los procesamientos de personalización correctamente
* Pruebe varios escenarios usando [datos de entrada de muestra](../test-approve/simulate-sample-input.md) de archivos CSV/JSON (admite hasta 30 variantes)

## Prácticas recomendadas de prueba

Para maximizar la eficacia de sus esfuerzos de prueba, siga estas prácticas recomendadas:

1. **Realizar pruebas antes y con frecuencia**: no espere hasta que una campaña esté completamente creada. Pruebe el contenido, la personalización y la lógica gradualmente a medida que desarrolla.

1. **Use perfiles de prueba realistas** - [Cree perfiles de prueba](../using/audience/creating-test-profiles.md) que representen con precisión los segmentos de audiencia de destino, incluidos casos extremos y diferentes escenarios de personalización.

1. **Realizar pruebas entre dispositivos y clientes**: compruebe el [procesamiento de correo electrónico](../using/content-management/rendering.md) en clientes de correo electrónico (Gmail, Outlook, Apple Mail) y dispositivos (escritorio, móvil, tableta) populares para garantizar una visualización coherente (solo canal de correo electrónico).

1. **Validar la personalización a fondo**: realice pruebas con varios [perfiles de prueba](../using/content-management/test-profiles.md) que tengan valores de atributo diferentes para confirmar que los tokens de personalización se representen correctamente y que los valores de reserva funcionen. Use [personalization playground](../using/personalization/personalize.md#playground) para experimentar con expresiones de personalización y probar código con datos de ejemplo antes de aplicarlos a sus campañas.

1. **Probar variaciones de contenido con datos de ejemplo**. Use [datos de entrada de muestra](../test-approve/simulate-sample-input.md) de archivos CSV o JSON para probar hasta 30 escenarios de personalización sin crear numerosos perfiles de prueba, lo que ahorra tiempo a la vez que garantiza una cobertura completa. Admite canales de correo electrónico, SMS, push, web, experiencia basada en código, en la aplicación y tarjetas de contenido.

1. **Use listas semilla para la supervisión de partes interesadas**. Configure [listas semilla](../using/configuration/seed-lists.md) para incluir automáticamente a las partes interesadas internas que recibirán copias de todos los envíos en el momento de la ejecución para la supervisión de la calidad y la verificación del cumplimiento (solo canal de correo electrónico).

1. **Simular rutas de recorrido**: para recorridos complejos con varias ramas, use [modo de prueba](../using/building-journeys/testing-the-journey.md) para probar diferentes condiciones de entrada y atributos de perfil y validar todas las rutas posibles. Disponible para recorridos de borrador que utilizan un área de nombres.

1. **Comprobar indicadores de entrega**: revise [puntuaciones de correo no deseado](../using/content-management/spam-report.md), estado de autenticación y métricas de estado de correo electrónico antes de envíos grandes (solo canal de correo electrónico).

1. **Documentar resultados de pruebas**: mantenga registros de los resultados de las pruebas, los problemas encontrados y las resoluciones para mejorar los procesos de pruebas futuros y compartir los conocimientos con su equipo.

1. **Involucre a las partes interesadas desde el principio** - Comparta vistas previas y resultados de pruebas con las partes interesadas antes de la [aprobación formal](../using/test-approve/gs-approval.md) para recopilar comentarios y alinear expectativas.

## Flujo de trabajo de pruebas recomendado

Siga este enfoque sistemático para garantizar pruebas exhaustivas y aprobaciones sin problemas:

### &#x200B;1. Desarrollo y previsualización de contenido

Comience creando el contenido y utilizando las funcionalidades de previsualización para verificar el diseño y la personalización iniciales:

* Diseña tu [correo electrónico](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [notificación push](../using/push/create-push.md) u otro contenido del canal

* Usar la característica **[Simular contenido](../using/content-management/preview-test.md)** para obtener una vista previa con perfiles de prueba

* Compruebe [tokens de personalización](../using/personalization/personalization-syntax.md), contenido dinámico y valores de reserva

* Experimente con expresiones de personalización en **[área de reproducción de personalización](../using/personalization/personalize.md#playground)** para probar y perfeccionar su código con datos de ejemplo antes de aplicarlo al contenido en directo

* Pruebe múltiples variaciones utilizando **[datos de entrada de muestra](../test-approve/simulate-sample-input.md)** de archivos CSV/JSON para validar la personalización en diversos escenarios de perfil

* Verificar [renderización](../using/content-management/rendering.md) en diferentes tamaños de pantalla y clientes de correo electrónico

### &#x200B;2. Validación técnica

Valide los aspectos técnicos que afectan a la capacidad de entrega y la funcionalidad:

* Ejecute [comprobaciones de puntuación de correo no deseado](../using/content-management/spam-report.md) para identificar posibles problemas de envío

* Pruebe los vínculos para asegurarse de que no están rotos y de que se realiza un seguimiento adecuado

* Validar la configuración de [autenticación por correo electrónico](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC)

* Revise el procesamiento de HTML y compruebe los problemas de compatibilidad con CSS

* Probar [diseño interactivo](../using/email/content-from-scratch.md) en dispositivos móviles y de escritorio

* Compruebe si hay [posibles conflictos](../using/conflict-prioritization/conflicts.md) con otras campañas y recorridos para evitar que los mensajes de los clientes se agoten y se produzcan problemas de tiempo de espera

### &#x200B;3. Pruebas de Recorrido (solo recorridos)

Si está probando un recorrido, valide la lógica de orquestación:

* Activar **[modo de prueba](../using/building-journeys/testing-the-journey.md)** para simular la progresión del perfil a través del recorrido

* Probar diferentes [condiciones de entrada](../using/building-journeys/entry-management.md) y cualificaciones de audiencia

* Compruebe que las [actividades de espera](../using/building-journeys/wait-activity.md), las [condiciones](../using/building-journeys/condition-activity.md) y la lógica de ramificación funcionan correctamente

* Use **[Ejecución en seco](../using/building-journeys/journey-dry-run.md)** para recorridos complejos a fin de analizar las rutas de ejecución sin enviar mensajes

* Compruebe que [events](../using/event/about-events.md) se déclencheur correctamente y que [custom actions](../using/action/about-custom-action-configuration.md) se ejecutan según lo esperado

### &#x200B;4. Envío de aprobación

Una vez finalizada la prueba y resueltos los problemas:

* Envíe la campaña o el recorrido para su aprobación según la [política de aprobación](../using/test-approve/approval-policies.md) de su organización

* Incluir los resultados y la documentación de la prueba con la [solicitud de aprobación](../using/test-approve/request-approval.md)

* Enviar comentarios o solicitudes de cambio de [aprobadores](../using/test-approve/review-approve-request.md)

* Realice las revisiones necesarias y vuelva a comprobar si los cambios son significativos

### &#x200B;5. Verificación previa al lanzamiento

Antes de activar la campaña o el recorrido:

* Realizar una revisión final de todas las configuraciones, audiencias y [programaciones](../using/building-journeys/journey-properties.md)

* Verifique que todas las aprobaciones se hayan realizado y documentado

* Confirme que las horas de envío y las [zonas horarias](../using/building-journeys/timezone-management.md) son correctas

* Habilitar [supervisión y alertas](../using/reports/alerts.md) para realizar un seguimiento del rendimiento después del inicio

### &#x200B;6. Monitorizar e iterar

Después del lanzamiento, continúe con la monitorización para detectar cualquier problema de forma temprana:

* Configure [alertas del sistema](../using/reports/alerts.md) para detectar errores de recorrido, tasas de salida hacia otro sitio altas o participación baja

* Revise [informes en vivo](../using/building-journeys/report-journey.md) para hacer un seguimiento del rendimiento con respecto a las expectativas

* Prepárese para [pausar o modificar](../using/building-journeys/journey-pause.md) recorridos si surgen problemas críticos

* Documente las lecciones aprendidas para mejorar los futuros procesos de prueba

## Pruebas en acción: Casos de uso

Consulte cómo se aplican los conceptos de prueba a los escenarios reales:

| Caso de uso | Lo que aprenderá | Enfoque clave de las pruebas |
|----------|-------------------|-------------------|
| **[Enviar mensajes multicanal](../using/building-journeys/journeys-uc.md)** | Pruebe un recorrido que combine Leer audiencia, eventos de reacción y mensajes push/de correo electrónico. Valide todo el flujo desde la segmentación de audiencia hasta la entrega de mensajes. | Coordinación multicanal, eventos de reacción, validación de flujo de extremo a extremo, pasos de prueba y publicación |
| **[Enviar un mensaje a los suscriptores](../using/building-journeys/message-to-subscribers-uc.md)** | Recorridos de prueba dirigidos a listas de suscripción con direccionamiento de correo electrónico dinámico. Valide expresiones de personalización para la segmentación correcta de suscriptores. | expresiones Personalization, direccionamiento dinámico, segmentación de listas de suscripción |
| **[Enviar mensajes con límite de tiempo](../using/building-journeys/weekday-email-uc.md)** | Recorridos de prueba con condiciones basadas en el tiempo para garantizar que los mensajes se envíen en días específicos. Validar las actividades de espera y la lógica de programación. | Condiciones basadas en el tiempo, actividades de espera, validación de programación |
| **[Explorar más casos de uso de recorrido](../using/building-journeys/jo-use-cases.md)** | Acceda a una colección completa de ejemplos prácticos que abarcan eventos de experiencia, mensajería multicanal e integraciones de sistemas externos. | Varios escenarios, patrones avanzados, pruebas de integración |

## Probar y aprobar contenido

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Vista previa, prueba y validación de contenido

Obtenga información sobre cómo obtener una vista previa, probar y validar contenido personalizado mediante perfiles de prueba, pruebas de presentación de correo electrónico, evaluaciones de puntuación de spam y mucho más.

[Explorar vista previa y prueba del contenido](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

Flujos de trabajo de aprobación para recorridos y campañas

Obtenga información sobre cómo configurar, administrar y ejecutar procesos de aprobación para garantizar el control de calidad de recorridos y campañas.

[Más información sobre flujos de trabajo de aprobación](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Prueba del recorrido

Valide el recorrido antes de publicarlo probándolo con perfiles específicos para garantizar que los eventos, las condiciones y las acciones funcionan según lo esperado. Disponible para recorridos de borrador que utilizan un área de nombres.

[Prueba del recorrido](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Ensayo del recorrido 

Realice un ensayo para simular y validar la ruta de ejecución del recorrido e identificar posibles problemas antes de publicarlo.

[Más información sobre el ensayo del recorrido](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Monitorización y solución de problemas

Acceda a recursos completos de solución de problemas, alertas del sistema y códigos de error para resolver los problemas de rendimiento y ejecución del recorrido.

[Ver monitorización y solución de problemas](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

Personalization Playground

Experimente con expresiones de personalización en un entorno seguro. Pruebe el código con datos de ejemplo y previsualice los resultados antes de aplicarlo a sus campañas y recorridos.

[Obtenga información sobre el patio de Personalization](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

Experimentos de contenido y pruebas A/B

Optimice sus campañas probando varias variaciones de contenido y midiendo el rendimiento para identificar los tratamientos con mejor rendimiento. Disponible solo para campañas (admite experimentos de bandidos A/B y con varios brazos).

[Obtenga Información Sobre Los Experimentos De Contenido](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Listas semilla para la monitorización de partes interesadas

Incluya automáticamente direcciones de partes interesadas internas en los envíos para monitorizar los mensajes reales enviados a los clientes y garantizar la calidad y el cumplimiento. Disponible solo para el canal de correo electrónico.

[Configuración de listas semilla](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

Detección de conflictos

Identifique posibles superposiciones entre campañas y recorridos para evitar saturar a los clientes con demasiadas comunicaciones simultáneas. Disponible para campañas y recorridos unitarios, de cualificación de audiencias y de lectura de audiencias.

[Detectar conflictos](../using/conflict-prioritization/conflicts.md)
:::

::::

## Recursos adicionales

### Guías esenciales de prueba y validación

* [Simular variaciones de contenido](../test-approve/simulate-sample-input.md): pruebe hasta 30 escenarios de personalización con archivos CSV o JSON. Ideal para pruebas de contenido multilingües sin crear varios perfiles de prueba. Admite tarjetas de correo electrónico, SMS, push, web, basadas en código, en la aplicación y de contenido.

* [Creación de perfiles de prueba](../using/audience/creating-test-profiles.md): cree y administre perfiles de prueba para simular escenarios de cliente. Obtenga información sobre cómo marcar perfiles para pruebas, establecer atributos y organizar segmentos de prueba.

* [Informe de correo no deseado](../using/content-management/spam-report.md): compruebe las puntuaciones de correo no deseado antes de enviarlo para mejorar la entrega y la ubicación en la bandeja de entrada. Obtenga recomendaciones procesables para la optimización de contenido.

* [Preguntas frecuentes sobre el Recorrido](../using/building-journeys/journey-faq.md): referencia rápida para preguntas comunes sobre pruebas de recorrido, ejecución y solución de problemas.

### Dependencias y relaciones

Comprenda cómo las funciones de prueba se conectan entre sí y con los flujos de trabajo de Journey Optimizer en general. Esta sección asigna requisitos previos, dependencias de subida/bajada y combinaciones de capacidades comunes.

+++**Requisitos previos (necesarios antes de realizar la prueba)**

* Los perfiles de prueba deben crearse antes de utilizar el modo de prueba o la previsualización de contenido
* Las directivas de aprobación deben configurarse antes de enviar para su aprobación
* Se deben crear listas semilla antes de agregarlas a campañas/recorridos
* Integración de Litmus necesaria para las pruebas de procesamiento de correo electrónico
* El recorrido debe estar en estado de borrador para utilizar el modo de prueba
* El recorrido debe tener un área de nombres configurada para utilizar el modo de prueba

+++

+++**De qué depende la prueba (flujo ascendente)**

* Creación de contenido: Necesita campañas o recorridos para realizar pruebas
* Perfiles de prueba: necesario para el modo de prueba y la previsualización de contenido
* Políticas de aprobación: necesarias para flujos de trabajo de aprobación
* Configuración: configuraciones de canal, autenticación de correo electrónico, configuración de dominio

+++

+++**Lo que depende de las pruebas (flujo descendente)**

* Activación de campaña/recorrido: no se puede activar sin resolver errores
* Publicación: es posible que se requiera la aprobación antes de publicar
* Monitorización en directo: monitorización e informes posteriores al lanzamiento
* Optimización: utilice los resultados de las pruebas para refinar las campañas futuras

+++

+++**Funciones relacionadas**

* Pruebas + Flujos de trabajo de aprobación = Proceso de garantía de calidad
* Pruebas + Detección de conflictos = Prevención de mensajes excesivos de clientes
* Pruebas + Experimentos de contenido = Optimización del rendimiento
* Pruebas + Informes = Ciclo de mejora continua
* Perfiles de prueba + Personalization = Validación del contenido
* Ejecución en seco + Modo de prueba = Validación completa del recorrido

+++

+++**Combinaciones de capacidades comunes**

* Prueba de contenido: Perfiles de prueba + Datos de entrada de muestra + Área de reproducción de Personalization
* Validación de correo electrónico: pruebas de procesamiento + puntuaciones de correo no deseado + Perfiles de prueba + Pruebas
* Validación de recorrido: modo de prueba + Ejecución en seco + Perfiles de prueba
* Lista de comprobación previa al lanzamiento: todas las pruebas técnicas + detección de conflictos + flujos de trabajo de aprobación

+++

### Preguntas frecuentes

+++**Q: ¿Qué pruebas se requieren antes de iniciar una campaña?**

**Mínimo:** Vista previa del contenido con perfiles de prueba + comprobación de puntuación de spam (correo electrónico)
**Recomendado:** + Procesamiento de correo electrónico + Detección de conflictos + Flujo de trabajo de aprobación
**Práctica recomendada:** + Prueba de datos de entrada de muestra + Listas semilla + Experimento A/B (si se optimiza)

+++

+++**Q: ¿Cómo puedo probar la personalización sin crear muchos perfiles de prueba?**

**Solución principal:** Use [datos de entrada de ejemplo](../test-approve/simulate-sample-input.md) con archivos CSV/JSON (admite hasta 30 variantes)
**Alternativa:** Cree de 3 a 5 [perfiles de prueba](../using/audience/creating-test-profiles.md) representativos que cubran segmentos clave
**Herramienta de aprendizaje:** Experimente primero en [área de reproducción de personalización](../using/personalization/personalize.md#playground)

+++

+++**Q: ¿Cuál es la diferencia entre el modo de prueba y la ejecución en seco para recorridos?**

**Modo de prueba:** Envía perfiles de prueba a través del recorrido, déclencheur acciones reales y genera mensajes de prueba. Requiere recorrido de borrador + área de nombres.
**Ejecución en seco:** Rastrea las rutas de ejecución sin enviar nada. Funciona en cualquier estado de recorrido. No se envían mensajes ni se ejecutan acciones.
**Usar juntos:** Modo de prueba para la prueba de mensajes + Ejecución en seco para la validación lógica = cobertura completa.

+++

+++**Q: ¿Puedo probar recorridos en estado de producción/activo?**

**Modo de prueba:** No - sólo recorridos de borrador
**Ejecución en seco:** Sí, funciona en cualquier estado de recorrido
**Vista previa del contenido:** Sí, vista previa de mensajes individuales en cualquier momento
**Solución alternativa:** recorrido activo duplicado en borrador para validación completa del modo de prueba

+++

+++**Q: ¿Qué capacidades de prueba requieren integraciones externas?**

**Procesamiento de correo electrónico:** Requiere integración con Litmus (licencia independiente)
**Todas las demás:** Integrado en Journey Optimizer, no se requieren integraciones adicionales
**Nota:** Los perfiles de prueba requieren el servicio Perfil del cliente en tiempo real (incluido)

+++

+++**Q: ¿Cómo pruebo las campañas activadas por API?**

**Opción 1:** Usar [API de simulación de campaña](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} para pruebas programáticas
**Opción 2:** Vista previa del contenido con perfiles de prueba en la interfaz de usuario
**Opción 3:** Enviar pruebas para probar las direcciones de correo electrónico
**Práctica recomendada:** Combine los tres para obtener una validación completa

+++


### Temas relacionados

* [Administración de contenido](content-management-landing-page.md): aprenda a diseñar, previsualizar y administrar contenido mediante plantillas, fragmentos y Designer de correo electrónico. Domine las prácticas recomendadas de creación de contenido para lograr una marca coherente.

* [Informes y análisis](reporting-landing-page.md): Analice el rendimiento de la campaña y del recorrido con informes, paneles y métricas completos. Tome decisiones basadas en datos para optimizar las experiencias de los clientes.

* [Configuración de Recorrido](configure-journeys-landing-page.md): configure las fuentes de datos, los eventos y las acciones personalizadas para habilitar la orquestación de recorrido sofisticada. Establecer las bases técnicas para la creación de recorridos.

* [Administración de campañas](../using/campaigns/get-started-with-campaigns.md): explora diferentes tipos de campañas y aprende a crear, programar y optimizar campañas por lotes y en tiempo real para lograr el máximo impacto.
