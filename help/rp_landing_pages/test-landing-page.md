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
source-git-commit: 5b1a68bb64fc55de894cb97a5239f4e1cd77fb40
workflow-type: tm+mt
source-wordcount: '2308'
ht-degree: 5%

---

# Prueba, validación y aprobación{#section-overview}

Esta sección cubre todas las funcionalidades de prueba y aprobación de Journey Optimizer. Encontrará herramientas para obtener una vista previa del contenido con perfiles de prueba, validar la lógica de recorrido, comprobar el procesamiento de los correos electrónicos y las puntuaciones de spam, ejecutar experimentos A/B, detectar conflictos y configurar flujos de trabajo de aprobación.

Esta página de aterrizaje le ayuda a elegir el método de prueba adecuado según lo que esté creando (campañas frente a recorridos), le guía por los flujos de trabajo de prueba recomendados y le proporciona un acceso rápido a todos los recursos de prueba y aprobación. Empiece por [Elija su método de prueba](#choose-your-testing-approach) a continuación para identificar qué herramientas se aplican a su caso de uso. Para ver definiciones de términos clave de prueba, consulte [Terminología clave](#key-terminology).

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

## Por qué importan las pruebas y la aprobación

Los procesos de prueba y aprobación sirven como puertas de calidad esenciales que protegen la reputación de su marca y garantizan el éxito de la campaña. He aquí por qué importan:

* **Detecte errores antes de que lleguen a los clientes**: identifique los vínculos rotos, la personalización incorrecta, los problemas de procesamiento y los errores lógicos en un entorno controlado en el que las correcciones sean rápidas y sin riesgos.

* **Mejore la capacidad de envío**: pruebe las puntuaciones de spam, valide la autenticación de correos electrónicos y compruebe el procesamiento en todos los clientes de correo electrónico para maximizar la ubicación de la bandeja de entrada y las tasas de participación.

* **Garantizar la coherencia de la marca**: obtenga una vista previa del contenido con diferentes perfiles de prueba para verificar que la personalización se muestre correctamente para varios segmentos de clientes y mantenga los estándares de marca.

* **Validar recorridos complejos**: simule flujos de recorrido de varios pasos para confirmar que los déclencheur se activan correctamente, que las condiciones se evalúan correctamente y que los clientes reciben los mensajes correctos en el momento adecuado.

* **Establecer la responsabilidad**: Implemente flujos de trabajo de aprobación formales que requieran la firma de las partes interesadas, lo que crea una propiedad clara y reduce los inicios de campaña no autorizados o prematuros.

* **Ahorre tiempo y recursos**: detecte problemas al principio del ciclo de desarrollo cuando las correcciones sean más baratas y rápidas, lo que evitará costosas correcciones posteriores al inicio o escalaciones del servicio de atención al cliente.

<!--## Testing capabilities overview

**Testing types available:**

* Content testing: Preview and validate message content before sending → [Choose your testing approach](#choose-your-testing-approach)
* Journey logic testing: Simulate customer progression through journey paths → [Choose your testing approach](#choose-your-testing-approach)
* Technical testing: Validate rendering, deliverability, and authentication → [Technical validation](#2-technical-validation)
* Performance testing: Compare content variations using A/B experiments → [Content Experiments & A/B Testing](#test--approve-content)
* Conflict testing: Detect campaign and journey overlaps → [Conflict Detection](#test--approve-content)
* Approval testing: Structured review workflows before activation → [Approval Workflows](#test--approve-content)

**Key capabilities by context:**

| Capability | Applies to | Channel restrictions | Prerequisites | Primary purpose |
|------------|-----------|---------------------|--------------|-----------------|
| [Test profiles](../using/content-management/test-profiles.md) | Campaigns, Journeys | All channels | Test profiles created | Preview personalized content |
| [Sample input data](../using/test-approve/simulate-sample-input.md) | Campaigns, Journeys | Email, SMS, Push, Web, Code-based, In-app, Content cards | CSV/JSON file | Test multiple personalization variants |
| [Test mode](../using/building-journeys/testing-the-journey.md) | Journeys only | N/A | Draft journey, namespace configured | Simulate profile progression |
| [Dry run](../using/building-journeys/journey-dry-run.md) | Journeys only | N/A | Journey created | Analyze execution paths |
| [Email rendering](../using/content-management/rendering.md) | Campaigns, Journeys | Email only | Litmus integration | Verify display across clients |
| [Spam score](../using/content-management/spam-report.md) | Campaigns, Journeys | Email only | None | Deliverability validation |
| [Seed lists](../using/configuration/seed-lists.md) | Campaigns, Journeys | Email only | Seed list configured | Stakeholder monitoring |
| [Content experiments](../using/content-management/get-started-experiment.md) | Campaigns only | All channels | None | A/B and multi-armed bandit testing |
| [Conflict detection](../using/conflict-prioritization/conflicts.md) | Campaigns, Journeys (limited) | All channels | None | Prevent customer over-messaging |
| [Approval workflows](../using/test-approve/gs-approval.md) | Campaigns, Journeys | All channels | Approval policy created | Structured review process |
| [Personalization playground](../using/personalization/personalize.md#playground) | All | All channels | None | Learn and test personalization syntax |

**Common testing workflows:**

1. Pre-development: Use [personalization playground](#test--approve-content) to learn syntax
2. During development: Preview with [test profiles](#choose-your-testing-approach), validate with [sample input data](#choose-your-testing-approach)
3. Pre-launch: Run [technical tests](#2-technical-validation) (rendering, spam), check [conflicts](#test--approve-content), submit for [approval](#test--approve-content)
4. Post-launch: Monitor with live reports (see [Monitoring & Troubleshooting](#test--approve-content)), iterate based on results

-->

<!--
## Decision tree for testing method selection

Use this decision tree to quickly identify the right testing tools for your specific scenario. Answer each question based on your context (what you're building, what you need to validate, and which channel you're using) to navigate directly to the relevant capabilities and documentation.

+++ **Question 1: What are you testing?**

* Campaign → [Choose your testing approach](#choose-your-testing-approach)
* Journey → [Choose your testing approach](#choose-your-testing-approach)
* Personalization expressions → [Personalization playground](#test--approve-content)
+++

+++**Question 2: What aspect needs validation?**

* Content and personalization → [Test profiles](#choose-your-testing-approach) or [sample input data](#choose-your-testing-approach)
* Email display → [Email rendering tests](#2-technical-validation)
* Deliverability → [Spam score checks](#2-technical-validation)
* Journey logic and flow → [Test mode](#choose-your-testing-approach) or [dry run](#test--approve-content)
* Performance comparison → [Content experiment](#test--approve-content) (campaigns only)
* Timing conflicts → [Conflict detection](#test--approve-content)
* Stakeholder review → [Approval workflow](#test--approve-content)
+++

+++**Question 3: What channel?**

* Email → All testing methods available (see [Choose your testing approach](#choose-your-testing-approach))
* SMS, Push → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Web, In-app, Code-based → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Multiple channels → Test each channel separately
+++

+++**Question 4: When in the workflow?**

* Before building → [Personalization playground](#test--approve-content) for learning
* During building → [Test profiles](#choose-your-testing-approach) and [sample input data](#choose-your-testing-approach) for validation
* Before launch → [Rendering tests](#2-technical-validation), [spam checks](#2-technical-validation), [conflict detection](#test--approve-content), [approvals](#test--approve-content)
* After launch → [Live reports](../using/building-journeys/report-journey.md) and [monitoring](#test--approve-content)
+++

-->

## Elija su método de prueba

El método de prueba adecuado depende de lo que esté creando y de lo que necesite validar. Utilice esta guía para identificar las herramientas de prueba más relevantes para su escenario.

>[!BEGINTABS]

>[!TAB Campañas de prueba]

**Para todas las campañas:**

* Previsualizar y probar contenido usando [perfiles de prueba](../using/content-management/test-profiles.md) o [datos de entrada de muestra](../using/test-approve/simulate-sample-input.md)
* Comprobar [procesamiento de correo electrónico](../using/content-management/rendering.md) entre dispositivos y clientes (solo canal de correo electrónico)
* Ejecutar [comprobaciones de puntuación de correo no deseado](../using/content-management/spam-report.md) (solo canal de correo electrónico)
* Revisar [conflictos](../using/conflict-prioritization/conflicts.md) con otras campañas y recorridos
* Configurar [listas semilla](../using/configuration/seed-lists.md) para la supervisión de partes interesadas (solo canal de correo electrónico)
* Enviar para [aprobación](../using/test-approve/gs-approval.md) antes de la activación

**Para pruebas A/B y optimización:**

* Cree [experimentos de contenido](../using/content-management/get-started-experiment.md) para probar varios tratamientos y medir el rendimiento

**Para campañas activadas por API:**

* Use la [API de simulación de campaña](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} para almacenar en déclencheur los trabajos de revisión mediante programación

>[!TAB recorridos de prueba]

**Para todos los recorridos:**

* Utilice [modo de prueba](../using/building-journeys/testing-the-journey.md) para simular la progresión del perfil (solo recorridos de borrador, requiere área de nombres) o [ejecución en seco](../using/building-journeys/journey-dry-run.md) para analizar las rutas de ejecución sin enviar mensajes
* Probar mensajes individuales usando [vista previa y pruebas](../using/content-management/preview-test.md)
* Comprobar [conflictos](../using/conflict-prioritization/conflicts.md) con otros recorridos y campañas
* Enviar para [aprobación](../using/test-approve/gs-approval.md) antes de publicar

**Para recorridos complejos:**

* Utilice el modo de prueba y la ejecución en seco juntos para validar completamente la lógica de ramificación y las rutas de ejecución
* Prueba sistemática de diferentes condiciones de entrada y atributos de perfil

**Nota:** La detección de conflictos y la restricción de recorrido solo están disponibles para recorridos unitarios, de calificación de audiencias y de lectura de audiencias.

>[!TAB Personalización de prueba]

**Antes de generar contenido:**

* Experimente en el [área de reproducción de personalización](../using/personalization/personalize.md#playground) para aprender sintaxis y probar expresiones con datos de ejemplo

**Durante la creación del contenido:**

* Vista previa con [perfiles de prueba](../using/content-management/test-profiles.md) para validar los procesamientos de personalización correctamente
* Pruebe varios escenarios usando [datos de entrada de muestra](../using/test-approve/simulate-sample-input.md) de archivos CSV/JSON (admite hasta 30 variantes)

>[!ENDTABS]

## Prácticas recomendadas de prueba

Para maximizar la eficacia de sus esfuerzos de prueba, siga estas prácticas recomendadas:

1. **Realizar pruebas antes y con frecuencia**: no espere hasta que una campaña esté completamente creada. Pruebe el contenido, la personalización y la lógica gradualmente a medida que desarrolla.

1. **Use perfiles de prueba realistas** - [Cree perfiles de prueba](../using/audience/creating-test-profiles.md) que representen con precisión los segmentos de audiencia de destino, incluidos casos extremos y diferentes escenarios de personalización.

1. **Realizar pruebas entre dispositivos y clientes**: compruebe el [procesamiento de correo electrónico](../using/content-management/rendering.md) en clientes de correo electrónico (Gmail, Outlook, Apple Mail) y dispositivos (escritorio, móvil, tableta) populares para garantizar una visualización coherente (solo canal de correo electrónico).

1. **Validar la personalización a fondo**: realice pruebas con varios [perfiles de prueba](../using/content-management/test-profiles.md) que tengan valores de atributo diferentes para confirmar que los tokens de personalización se representen correctamente y que los valores de reserva funcionen. Use [personalization playground](../using/personalization/personalize.md#playground) para experimentar con expresiones de personalización y probar código con datos de ejemplo antes de aplicarlos a sus campañas.

1. **Probar variaciones de contenido con datos de ejemplo**. Use [datos de entrada de muestra](../using/test-approve/simulate-sample-input.md) de archivos CSV o JSON para probar hasta 30 escenarios de personalización sin crear numerosos perfiles de prueba, lo que ahorra tiempo a la vez que garantiza una cobertura completa. Admite canales de correo electrónico, SMS, push, web, experiencia basada en código, en la aplicación y tarjetas de contenido.

1. **Use listas semilla para la supervisión de partes interesadas**. Configure [listas semilla](../using/configuration/seed-lists.md) para incluir automáticamente a las partes interesadas internas que recibirán copias de todos los envíos en el momento de la ejecución para la supervisión de la calidad y la verificación del cumplimiento (solo canal de correo electrónico).

1. **Simular rutas de recorrido**: para recorridos complejos con varias ramas, use [modo de prueba](../using/building-journeys/testing-the-journey.md) para probar diferentes condiciones de entrada y atributos de perfil y validar todas las rutas posibles. Disponible para recorridos de borrador que utilizan un área de nombres.

1. **Comprobar indicadores de entrega**: revise [puntuaciones de correo no deseado](../using/content-management/spam-report.md), estado de autenticación y métricas de estado de correo electrónico antes de envíos grandes (solo canal de correo electrónico).

1. **Documentar resultados de pruebas**: mantenga registros de los resultados de las pruebas, los problemas encontrados y las resoluciones para mejorar los procesos de pruebas futuros y compartir los conocimientos con su equipo.

1. **Involucre a las partes interesadas desde el principio** - Comparta vistas previas y resultados de pruebas con las partes interesadas antes de la [aprobación formal](../using/test-approve/gs-approval.md) para recopilar comentarios y alinear expectativas.

## Flujo de trabajo de pruebas recomendado

Siga este enfoque de 4 fases para validar sus campañas y recorridos antes del lanzamiento:

| Fase | Qué se va a probar | Acciones clave |
|-------|-------------|-------------|
| **1. Validación de contenido** | Personalization, diseño, renderización | [Vista previa con perfiles de prueba](../using/content-management/preview-test.md), probar [múltiples variaciones](../using/test-approve/simulate-sample-input.md) con CSV/JSON, comprobar [procesamiento](../using/content-management/rendering.md) entre dispositivos |
| **2. Comprobaciones técnicas** | Entrega, vínculos, conflictos | Ejecutar [comprobaciones de puntuación de correo no deseado](../using/content-management/spam-report.md), validar vínculos, comprobar [conflictos](../using/conflict-prioritization/conflicts.md) con otras campañas |
| **3. lógica de recorrido** (solo recorridos) | Condiciones de entrada, flujo, ramificación | Use [modo de prueba](../using/building-journeys/testing-the-journey.md) para simular la progresión, ejecute [ejecución en seco](../using/building-journeys/journey-dry-run.md) para las rutas complejas |
| **4. Antes del lanzamiento** | Configuración, aprobaciones, monitorización | Enviar para [aprobación](../using/test-approve/gs-approval.md), comprobar programaciones y audiencias, habilitar [alertas](../using/reports/alerts.md) |

**Sugerencia profesional:** Comience con el [área de reproducción de personalización](../using/personalization/personalize.md#playground) para probar las expresiones antes de generar contenido y compruebe siempre la [detección de conflictos](../using/conflict-prioritization/conflicts.md) antes del inicio para evitar mensajes excesivos.

## Pruebas en acción: Casos de uso

Consulte cómo se aplican los conceptos de prueba a los escenarios reales:

| Caso de uso | Lo que aprenderá | Enfoque clave de las pruebas |
|----------|-------------------|-------------------|
| **[Enviar mensajes multicanal](../using/building-journeys/journeys-uc.md)** | Pruebe un recorrido que combine Leer audiencia, eventos de reacción y mensajes push/de correo electrónico. Valide todo el flujo desde la segmentación de audiencia hasta la entrega de mensajes. | Coordinación multicanal, eventos de reacción, validación de flujo de extremo a extremo, pasos de prueba y publicación |
| **[Enviar un mensaje a los suscriptores](../using/building-journeys/message-to-subscribers-uc.md)** | Recorridos de prueba dirigidos a listas de suscripción con direccionamiento de correo electrónico dinámico. Valide expresiones de personalización para la segmentación correcta de suscriptores. | expresiones Personalization, direccionamiento dinámico, segmentación de listas de suscripción |
| **[Enviar mensajes con límite de tiempo](../using/building-journeys/weekday-email-uc.md)** | Recorridos de prueba con condiciones basadas en el tiempo para garantizar que los mensajes se envíen en días específicos. Validar las actividades de espera y la lógica de programación. | Condiciones basadas en el tiempo, actividades de espera, validación de programación |
| **[Explorar más casos de uso de recorrido](../using/building-journeys/jo-use-cases.md)** | Acceda a una colección completa de ejemplos prácticos que abarcan eventos de experiencia, mensajería multicanal e integraciones de sistemas externos. | Varios escenarios, patrones avanzados, pruebas de integración |

## Terminología clave

Familiarícese con estos conceptos esenciales de prueba para comprender mejor las capacidades de prueba y aprobación de Journey Optimizer. Cada término vincula a documentación detallada.

**[Perfiles de prueba](../using/content-management/test-profiles.md)**: perfiles de cliente sintéticos (clientes no reales) que se usan para obtener una vista previa del contenido personalizado. Marcado en el servicio de Perfil del cliente en tiempo real. Necesario para el modo de prueba y la previsualización de contenido. [Aprenda a crear perfiles de prueba](../using/audience/creating-test-profiles.md)

**[Modo de prueba](../using/building-journeys/testing-the-journey.md)**: característica de simulación de Recorrido que envía perfiles de prueba a través de rutas de recorrido. Limitaciones: solo recorridos de borrador, requiere área de nombres, solo perfiles de prueba. [Ver documentación del modo de prueba](../using/building-journeys/testing-the-journey.md)

**[Ejecución en seco](../using/building-journeys/journey-dry-run.md)**: herramienta de análisis de ejecución de Recorrido que rastrea rutas sin enviar mensajes ni realizar llamadas de API. Caso de uso: Validación de la lógica sin consumir recursos. [Más información sobre la ejecución en seco](../using/building-journeys/journey-dry-run.md)

**[Datos de entrada de muestra](../using/test-approve/simulate-sample-input.md)**: archivos CSV o JSON que contienen valores de atributo de perfil para probar la personalización. Admite hasta 30 variantes. Alternativa a la creación de perfiles de prueba. [Cómo simular variaciones de contenido](../using/test-approve/simulate-sample-input.md)

**[Listas semilla](../using/configuration/seed-lists.md)**: las direcciones de correo electrónico de las partes interesadas internas se incluyen automáticamente en los envíos reales (no en los envíos de prueba). Solo canal de correo electrónico. Caso de uso: Monitorización de la calidad y cumplimiento normativo. [Configurar listas semilla](../using/configuration/seed-lists.md)

**[Experimentos de contenido](../using/content-management/get-started-experiment.md)**: pruebas A/B o experimentos de bandidos multibrazo que comparan variaciones de contenido. Solo campañas, no disponible en recorridos. [Introducción a los experimentos](../using/content-management/get-started-experiment.md) | [Crear experimentos](../using/content-management/content-experiment.md)

**[Pruebas](../using/content-management/proofs.md)**: pruebe los envíos de correo electrónico enviados a direcciones de correo electrónico específicas mediante datos de perfil de prueba. A diferencia de las listas semilla (las pruebas son envíos de prueba manuales, las listas semilla son copias automáticas de las partes interesadas). [Enviar pruebas](../using/content-management/proofs.md)

**[Detección de conflictos](../using/conflict-prioritization/conflicts.md)**: herramienta que identifica campañas y recorridos superpuestos dirigidos a las mismas audiencias. Compatibilidad de recorrido limitada: tipos de audiencia unitarios, de calificación de audiencia y de lectura de audiencia solamente. [Más información acerca de la administración de conflictos](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Flujos de trabajo de aprobación](../using/test-approve/gs-approval.md)**: proceso de revisión de varios pasos que requiere la aprobación de las partes interesadas antes de la activación. Requiere la configuración de directiva de aprobación. [Configurar aprobaciones](../using/test-approve/gs-approval.md) | [Crear directivas](../using/test-approve/approval-policies.md)

**[Pruebas de procesamiento](../using/content-management/rendering.md)**: validación de visualización de correo electrónico en clientes de correo electrónico (Gmail, Outlook, Apple Mail) y dispositivos. Requiere integración con Litmus. [Probar procesamiento de correo electrónico](../using/content-management/rendering.md)

**[Área de reproducción de Personalization](../using/personalization/personalize.md#playground)**: entorno de aprendizaje interactivo para experimentar con sintaxis de personalización y expresiones de prueba con datos de ejemplo. No se requieren conjuntos de datos activos. [Acceso al área de reproducción](../using/personalization/personalize.md#playground)

## Recursos adicionales

>[!BEGINTABS]

>[!TAB Guías esenciales]

* [Simular variaciones de contenido](../using/test-approve/simulate-sample-input.md): pruebe hasta 30 escenarios de personalización con archivos CSV o JSON. Ideal para pruebas de contenido multilingües sin crear varios perfiles de prueba. Admite tarjetas de correo electrónico, SMS, push, web, basadas en código, en la aplicación y de contenido.

* [Creación de perfiles de prueba](../using/audience/creating-test-profiles.md): cree y administre perfiles de prueba para simular escenarios de cliente. Obtenga información sobre cómo marcar perfiles para pruebas, establecer atributos y organizar segmentos de prueba.

* [Informe de correo no deseado](../using/content-management/spam-report.md): compruebe las puntuaciones de correo no deseado antes de enviarlo para mejorar la entrega y la ubicación en la bandeja de entrada. Obtenga recomendaciones procesables para la optimización de contenido.

* [Preguntas frecuentes sobre el Recorrido](../using/building-journeys/journey-faq.md): referencia rápida para preguntas comunes sobre pruebas de recorrido, ejecución y solución de problemas.

>[!TAB Dependencias y relaciones]

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

* Flujos de trabajo Prueba + Aprobación: proceso de garantía de calidad
* Pruebas + Detección de conflictos: prevención del exceso de mensajes de los clientes
* Pruebas + Experimentos de contenido: optimización del rendimiento
* Pruebas y creación de informes: ciclo de mejora continua
* Perfiles de prueba + Personalization: validación de contenido
* Ejecución en seco + Modo de prueba: validación completa del recorrido

+++

+++**Combinaciones de capacidades comunes**

* Prueba de contenido: Perfiles de prueba + Datos de entrada de muestra + Área de reproducción de Personalization
* Validación de correo electrónico: pruebas de procesamiento + puntuaciones de correo no deseado + Perfiles de prueba + Pruebas
* Validación de recorrido: modo de prueba + Ejecución en seco + Perfiles de prueba
* Lista de comprobación previa al lanzamiento: todas las pruebas técnicas + detección de conflictos + flujos de trabajo de aprobación

+++

>[!TAB Preguntas frecuentes]

+++**Q: ¿Qué pruebas se requieren antes de iniciar una campaña?**

**Mínimo:** Vista previa del contenido con perfiles de prueba + comprobación de puntuación de spam (correo electrónico)
**Recomendado:** + Procesamiento de correo electrónico + Detección de conflictos + Flujo de trabajo de aprobación
**Práctica recomendada:** + Prueba de datos de entrada de muestra + Listas semilla + Experimento A/B (si se optimiza)

+++

+++**Q: ¿Cómo puedo probar la personalización sin crear muchos perfiles de prueba?**

**Solución principal:** Use [datos de entrada de ejemplo](../using/test-approve/simulate-sample-input.md) con archivos CSV/JSON (admite hasta 30 variantes)
**Alternativa:** Cree de 3 a 5 [perfiles de prueba](../using/audience/creating-test-profiles.md) representativos que cubran segmentos clave
**Herramienta de aprendizaje:** Experimente primero en [área de reproducción de personalización](../using/personalization/personalize.md#playground)

+++

+++**Q: ¿Cuál es la diferencia entre el modo de prueba y la ejecución en seco para recorridos?**

**Modo de prueba:** Envía perfiles de prueba a través del recorrido, déclencheur acciones reales y genera mensajes de prueba. Requiere recorrido de borrador + área de nombres.
**Ejecución en seco:** Rastrea las rutas de ejecución sin enviar nada. Funciona en cualquier estado de recorrido. No se envían mensajes ni se ejecutan acciones.
**Usar juntos:** Modo de prueba para la prueba de mensajes + Ejecución en seco para la validación lógica: cobertura completa.

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

**Opción 1:** Use [API de simulación de campaña](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} para pruebas programáticas
**Opción 2:** Vista previa del contenido con perfiles de prueba en la interfaz de usuario
**Opción 3:** Enviar pruebas para probar las direcciones de correo electrónico
**Práctica recomendada:** Combine los tres para obtener una validación completa

+++

>[!ENDTABS]
