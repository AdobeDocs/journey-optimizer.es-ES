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
source-git-commit: c3535f39b351d671054031b9cc391bf6d9d83a09
workflow-type: ht
source-wordcount: '2328'
ht-degree: 100%

---

# Prueba, validación y aprobación{#section-overview}

Esta sección abarca todas las funcionalidades de prueba y aprobación de Journey Optimizer. Encontrará herramientas para obtener una vista previa del contenido con perfiles de prueba, validar la lógica de recorrido, comprobar el procesamiento de los correos electrónicos y las puntuaciones de spam, ejecutar experimentos A/B, detectar conflictos y configurar flujos de trabajo de aprobación.

Esta página de destino le ayuda a elegir el método de prueba adecuado según lo que esté creando (campañas en contraposición a recorridos), le guía por los flujos de trabajo de prueba recomendados y le proporciona un acceso rápido a todos los recursos de prueba y aprobación. Empiece por [Elija su método de prueba](#choose-your-testing-approach) a continuación para identificar qué herramientas se aplican a su caso de uso. Para ver definiciones de términos clave de prueba, consulte [Terminología clave](#key-terminology).

## Probar y aprobar contenido

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=es)

Vista previa, prueba y validación de contenido

Obtenga información sobre cómo obtener una vista previa, probar y validar contenido personalizado mediante perfiles de prueba, pruebas de presentación de correo electrónico, evaluaciones de puntuación de spam y mucho más.

[Explorar vista previa y prueba del contenido](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=es)

Flujos de trabajo de aprobación para recorridos y campañas

Obtenga información sobre cómo configurar, administrar y ejecutar procesos de aprobación para garantizar el control de calidad de recorridos y campañas.

[Más información sobre flujos de trabajo de aprobación](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=es)

Prueba del recorrido

Valide el recorrido antes de publicarlo probándolo con perfiles específicos para garantizar que los eventos, las condiciones y las acciones funcionan según lo esperado. Disponible para recorridos de borrador que utilizan un espacio de nombres.

[Prueba del recorrido](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=es)

Ensayo del recorrido 

Realice un ensayo para simular y validar la ruta de ejecución del recorrido e identificar posibles problemas antes de publicarlo.

[Más información sobre el ensayo del recorrido](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=es)

Monitorización y solución de problemas

Acceda a recursos completos de solución de problemas, alertas del sistema y códigos de error para resolver los problemas de rendimiento y ejecución del recorrido.

[Ver monitorización y solución de problemas](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg?lang=es)

Zona de juegos de personalización

Experimente con expresiones de personalización en un entorno seguro. Pruebe el código con datos de ejemplo y previsualice los resultados antes de aplicarlo a sus campañas y recorridos.

[Obtenga información sobre la Zona de juegos de personalización](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=es)

Experimentos de contenido y pruebas A/B

Optimice sus campañas probando varias variaciones de contenido y midiendo el rendimiento para identificar los tratamientos con mejor rendimiento. Disponible solo para campañas (admite experimentos de bandidos A/B y con varios brazos).

[Más información sobre los experimentos de contenido](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=es)

Listas semilla para la supervisión de partes interesadas

Incluya automáticamente direcciones de partes interesadas internas en los envíos para supervisar los mensajes reales enviados a los clientes y garantizar la calidad y el cumplimiento. Disponible solo para el canal de correo electrónico.

[Configuración de listas semilla](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=es)

Detección de conflictos

Identifique posibles superposiciones entre campañas y recorridos para evitar saturar a los clientes con demasiadas comunicaciones simultáneas. Estas herramientas están disponibles en campañas y recorridos unitarios, de calificación de público y de público de lectura.

[Detectar conflictos](../using/conflict-prioritization/conflicts.md)
:::

::::

## Por qué importan las pruebas y la aprobación

Los procesos de prueba y aprobación sirven como puertas de calidad esenciales que protegen la reputación de su marca y garantizan el éxito de la campaña. He aquí por qué importan:

* **Detecte errores antes de que lleguen a los clientes**: identifique los vínculos rotos, la personalización incorrecta, los problemas de procesamiento y los errores lógicos en un entorno controlado en el que las correcciones sean rápidas y sin riesgos.

* **Mejore la entregabilidad**: pruebe las puntuaciones de spam, valide la autenticación de correos electrónicos y compruebe el procesamiento en todos los clientes de correo electrónico para maximizar la ubicación de la bandeja de entrada y las tasas de participación.

* **Garantice la coherencia de la marca**: obtenga una vista previa del contenido con diferentes perfiles de prueba para verificar que la personalización se muestre correctamente para varios segmentos de clientes y mantenga los estándares de marca.

* **Valide recorridos complejos**: simule flujos de recorrido de varios pasos para confirmar que los activadores se ejecutan correctamente, que las condiciones se evalúan correctamente y que los clientes reciben los mensajes correctos en el momento adecuado.

* **Establezca mecanismos de rendición de cuentas**: implemente flujos de trabajo de aprobación formales que requieran la firma de las partes interesadas, lo que crea una propiedad clara y reduce los inicios de campaña no autorizados o prematuros.

* **Ahorre tiempo y recursos**: detecte problemas al principio del ciclo de desarrollo cuando las correcciones sean más baratas y rápidas, lo que evitará costosas correcciones posteriores al inicio o derivaciones al servicio de atención al cliente.

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

El método de prueba adecuado depende de lo que esté creando y de lo que necesite validar. Utilice esta guía para identificar las herramientas de prueba más relevantes para su contexto particular.

>[!BEGINTABS]

>[!TAB Campañas de prueba]

**Para todas las campañas:**

* Previsualizar y probar contenido usando [perfiles de prueba](../using/content-management/test-profiles.md) o [datos de entrada de muestra](../using/test-approve/simulate-sample-input.md)
* Comprobar [renderizado de correo electrónico](../using/content-management/rendering.md) entre dispositivos y clientes (solo canal de correo electrónico)
* Ejecutar [comprobaciones de puntuación de correo no deseado](../using/content-management/spam-report.md) (solo canal de correo electrónico)
* Revisar [conflictos](../using/conflict-prioritization/conflicts.md) con otras campañas y recorridos
* Configurar [listas semilla](../using/configuration/seed-lists.md) para la supervisión de partes interesadas (solo canal de correo electrónico)
* Enviar para [aprobación](../using/test-approve/gs-approval.md) antes de la activación

**Para pruebas A/B y optimización:**

* Crear [experimentos de contenido](../using/content-management/get-started-experiment.md) para probar varios tratamientos y medir el rendimiento

**Para campañas activadas por API:**

* Usar la [API de simulación de campaña](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} para activar los trabajos de revisión mediante programación

>[!TAB Prueba de recorridos]

**Para todos los recorridos:**

* Utilice el [modo de prueba](../using/building-journeys/testing-the-journey.md) para simular la progresión del perfil (solo recorridos de borrador, requiere espacio de nombres) o [ensayo](../using/building-journeys/journey-dry-run.md) para analizar las rutas de ejecución sin enviar mensajes
* Pruebe mensajes individuales usando [vista previa y pruebas](../using/content-management/preview-test.md)
* Compruebe [conflictos](../using/conflict-prioritization/conflicts.md) con otros recorridos y campañas
* Envíe para [aprobación](../using/test-approve/gs-approval.md) antes de publicar

**Para recorridos complejos:**

* Utilice el modo de prueba y el ensayo juntos para validar completamente la lógica de ramificación y las rutas de ejecución
* Pruebe de manera sistemática diferentes condiciones de entrada y atributos de perfil

**Nota:** La detección de conflictos y la restricción de recorridos solo están disponibles para recorridos unitarios, de calificación de públicos y de lectura de públicos.

>[!TAB Personalización de prueba]

**Antes de generar contenido:**

* Experimente en la [zona de juegos de personalización](../using/personalization/personalize.md#playground) para aprender sintaxis y probar expresiones con datos de ejemplo

**Durante la creación del contenido:**

* Vista previa con [perfiles de prueba](../using/content-management/test-profiles.md) para validar que la personalización se renderiza correctamente
* Pruebe varios contextos usando [datos de entrada de muestra](../using/test-approve/simulate-sample-input.md) desde archivos CSV/JSON (admite hasta 30 variantes)

>[!ENDTABS]

## Prácticas recomendadas para pruebas

Para maximizar la eficacia de su trabajo en las pruebas, siga estas prácticas recomendadas:

1. **Realice pruebas desde el principio y con frecuencia**: no espere hasta que una campaña esté completamente creada. Pruebe el contenido, la personalización y la lógica gradualmente a medida que desarrolla.

1. **Use perfiles de prueba realistas**: [cree perfiles de prueba](../using/audience/creating-test-profiles.md) que representen con precisión los segmentos de público destinatario, incluidos casos extremos y diferentes contextos de personalización.

1. **Realice pruebas entre dispositivos y clientes**: compruebe el [procesamiento de correo electrónico](../using/content-management/rendering.md) en clientes de correo electrónico (Gmail, Outlook, Apple Mail) y dispositivos (escritorio, móvil, tableta) populares para garantizar una visualización coherente (solo canal de correo electrónico).

1. **Compruebe minuciosamente la personalización**: realice pruebas con varios [perfiles de prueba](../using/content-management/test-profiles.md) que tengan valores de atributo diferentes para confirmar que los tokens de personalización se renderizan correctamente y que los valores fallback funcionan. Use la [zona de juegos de personalización](../using/personalization/personalize.md#playground) para experimentar con expresiones de personalización y probar código con datos de ejemplo antes de aplicarlos a sus campañas.

1. **Pruebe variaciones de contenido con datos de ejemplo**. Use [datos de entrada de muestra](../using/test-approve/simulate-sample-input.md) de archivos CSV o JSON para probar hasta 30 casos de personalización sin crear numerosos perfiles de prueba, lo que ahorra tiempo a la vez que garantiza una cobertura completa. Admite canales de correo electrónico, SMS, push, web, experiencia basada en código, en la aplicación y tarjetas de contenido.

1. **Use listas semilla para la supervisión de las partes interesadas**: configure [listas semilla](../using/configuration/seed-lists.md) para incluir automáticamente a las partes interesadas internas que recibirán copias de todos los envíos en el momento de la ejecución para la supervisión de la calidad y la verificación del cumplimiento (solo canal de correo electrónico).

1. **Simule rutas de recorrido**: para recorridos complejos con varias ramas, use [modo de prueba](../using/building-journeys/testing-the-journey.md) para probar diferentes condiciones de entrada y atributos de perfil y validar todas las rutas posibles. Disponible para recorridos de borrador que utilizan un espacio de nombres.

1. **Compruebe los indicadores de entregabilidad**: revise [puntuaciones de correo no deseado](../using/content-management/spam-report.md), estado de autenticación y métricas de estado de correo electrónico antes de envíos grandes (solo canal de correo electrónico).

1. **Documente los resultados de las pruebas**: mantenga registros de los resultados de las pruebas, los problemas encontrados y las soluciones para mejorar los procesos de pruebas futuros y compartir los conocimientos con su equipo.

1. **Involucre a las partes interesadas desde el principio**: comparta vistas previas y resultados de pruebas con las partes interesadas antes de la [aprobación formal](../using/test-approve/gs-approval.md) para recopilar comentarios y alinear expectativas.

## Flujo de trabajo de pruebas recomendado

Siga este enfoque de 4 fases para validar sus campañas y recorridos antes del lanzamiento:

| Fase | Qué se debe probar | Acciones clave |
|-------|-------------|-------------|
| **1. Validación de contenido** | Personalization, diseño, renderizado | [Vista previa con perfiles de prueba](../using/content-management/preview-test.md), probar [múltiples variaciones](../using/test-approve/simulate-sample-input.md) con CSV/JSON, comprobar [renderizado](../using/content-management/rendering.md) entre dispositivos |
| **2. Comprobaciones técnicas** | Entregabilidad, vínculos, conflictos | Ejecutar [comprobaciones de puntuación de correo no deseado](../using/content-management/spam-report.md), validar vínculos, comprobar [conflictos](../using/conflict-prioritization/conflicts.md) con otras campañas |
| **3. Lógica de recorrido** (solo recorridos) | Condiciones de entrada, flujo, ramificación | Usar [modo de prueba](../using/building-journeys/testing-the-journey.md) para simular la progresión, ejecutar [ensayo](../using/building-journeys/journey-dry-run.md) para las rutas complejas |
| **4. Antes del lanzamiento** | Configuración, aprobaciones, supervisión | Enviar para [aprobación](../using/test-approve/gs-approval.md), comprobar programaciones y públicos, habilitar [alertas](../using/reports/alerts.md) |

**Sugerencia profesional:** comience con la [zona de juegos de personalización](../using/personalization/personalize.md#playground) para probar las expresiones antes de generar contenido y compruebe siempre la [detección de conflictos](../using/conflict-prioritization/conflicts.md) antes del inicio para evitar mensajes excesivos.

## Pruebas en acción: Casos de uso

Consulte cómo se aplican los conceptos de prueba a los casos reales:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/journeys-uc.md">
<img alt="Envío de mensajes multicanal" src="../using/assets/do-not-localize/start-journey.jpeg">
</a>
<div>
<a href="../using/building-journeys/journeys-uc.md"><strong>Envío de mensajes multicanal</strong></a>
</div>
<p>
Pruebe un recorrido que combine Leer público, eventos de reacción y mensajes push/de correo electrónico. Valide todo el flujo desde la segmentación de públicos hasta el envío de mensajes. Céntrese en la coordinación multicanal, los eventos de reacción, la validación de flujo de extremo a extremo y los pasos de prueba/publicación.
</p>
</td>
<td>
<a href="../using/building-journeys/message-to-subscribers-uc.md">
<img alt="Envío de un mensaje a los suscriptores" src="../using/assets/do-not-localize/start-quick.png">
</a>
<div>
<a href="../using/building-journeys/message-to-subscribers-uc.md"><strong>Envío de un mensaje a los suscriptores</strong></a>
</div>
<p>
Realice pruebas de recorridos dirigidas a listas de suscripción con direccionamiento de correo electrónico dinámico. Valide expresiones de personalización para la segmentación correcta de suscriptores. Céntrese en las expresiones de personalización, el direccionamiento dinámico y la segmentación de listas de suscripción.
</p>
</td>
<td>
<a href="../using/building-journeys/weekday-email-uc.md">
<img alt="Envíe mensajes con límite de tiempo" src="../using/assets/do-not-localize/calendar.jpeg">
</a>
<div>
<a href="../using/building-journeys/weekday-email-uc.md"><strong>Envío de mensajes con límite de tiempo</strong></a>
</div>
<p>
Recorridos de prueba con condiciones basadas en el tiempo para garantizar que los mensajes se envíen en días específicos. Valide las actividades de espera y la lógica de programación. Céntrese en las condiciones basadas en el tiempo, las actividades de espera y la validación de programación.
</p>
</td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/jo-use-cases.md">
<img alt="Explore más casos de uso de recorridos" src="../using/assets/do-not-localize/icon-quick-start.svg">
</a>
<div>
<a href="../using/building-journeys/jo-use-cases.md"><strong>Explorar más casos de uso de recorridos</strong></a>
</div>
<p>
Acceda a una completa colección de ejemplos prácticos que abarcan eventos de experiencia, mensajería multicanal e integraciones de sistemas externos. Explore varios contextos, patrones avanzados y enfoques de prueba de integración.
</p>
</td>
</tr></table>

## Terminología clave

Familiarícese con estos conceptos esenciales de prueba para comprender mejor las capacidades de prueba y aprobación de Journey Optimizer. Cada término vincula a documentación detallada.

**[Perfiles de prueba](../using/content-management/test-profiles.md)**: perfiles de cliente sintéticos (clientes no reales) que se usan para obtener una vista previa del contenido personalizado. Marcado en el servicio de Perfil del cliente en tiempo real. Obligatorio para el modo de prueba y la previsualización de contenido. [Más información sobre cómo crear perfiles de prueba](../using/audience/creating-test-profiles.md)

**[Modo de prueba](../using/building-journeys/testing-the-journey.md)**: característica de simulación de recorrido que envía perfiles de prueba a través de rutas de recorrido. Limitaciones: solo recorridos de borrador, requiere espacio de nombres, solo perfiles de prueba. [Ver documentación del modo de prueba](../using/building-journeys/testing-the-journey.md)

**[Ensayo](../using/building-journeys/journey-dry-run.md)**: herramienta de análisis de ejecución de recorrido que rastrea rutas sin enviar mensajes ni realizar llamadas de API. Caso de uso: validación de la lógica sin consumir recursos. [Más información sobre el ensayo](../using/building-journeys/journey-dry-run.md)

**[Datos de entrada de muestra](../using/test-approve/simulate-sample-input.md)**: archivos CSV o JSON que contienen valores de atributo de perfil para probar la personalización. Admite hasta 30 variantes. Alternativa a la creación de perfiles de prueba. [Cómo simular variaciones de contenido](../using/test-approve/simulate-sample-input.md)

**[Listas semilla](../using/configuration/seed-lists.md)**: las direcciones de correo electrónico de las partes interesadas internas se incluyen automáticamente en los envíos reales (no en los envíos de prueba). Solo canal de correo electrónico. Caso de uso: supervisión de la calidad y cumplimiento normativo. [Configure listas semilla](../using/configuration/seed-lists.md)

**[Experimentos de contenido](../using/content-management/get-started-experiment.md)**: pruebas A/B o experimentos de bandidos multibrazo que comparan variaciones de contenido. Solo campañas, no disponible en recorridos. [Introducción a los experimentos](../using/content-management/get-started-experiment.md) | [Crear experimentos](../using/content-management/content-experiment.md)

**[Pruebas](../using/content-management/proofs.md)**: pruebe los envíos de correo electrónico enviados a direcciones de correo electrónico específicas mediante datos de perfil de prueba. A diferencia de las listas semilla (las pruebas son envíos de prueba manuales, las listas semilla son copias automáticas de las partes interesadas). [Envíe pruebas](../using/content-management/proofs.md)

**[Detección de conflictos](../using/conflict-prioritization/conflicts.md)**: herramienta que identifica campañas y recorridos superpuestos dirigidos a los mismos públicos. Compatibilidad de recorrido limitada: tipos de público unitarios, de calificación de público y de lectura de público solamente. [Más información sobre la gestión de conflictos](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Flujos de trabajo de aprobación](../using/test-approve/gs-approval.md)**: proceso de revisión de varios pasos que requiere la aprobación de las partes interesadas antes de la activación. Requiere la configuración de directiva de aprobación. [Configurar aprobaciones](../using/test-approve/gs-approval.md) | [Crear directivas](../using/test-approve/approval-policies.md)

**[Pruebas de renderizado](../using/content-management/rendering.md)**: validación de visualización de correo electrónico en clientes de correo electrónico (Gmail, Outlook, Apple Mail) y dispositivos. Requiere integración con Litmus. [Pruebe la renderización del correo electrónico](../using/content-management/rendering.md)

**[Zona de juegos de personalización](../using/personalization/personalize.md#playground)**: entorno de aprendizaje interactivo para experimentar con sintaxis de personalización y expresiones de prueba con datos de muestra. No se requieren conjuntos de datos activos. [Acceso a la zona de juegos](../using/personalization/personalize.md#playground)

## Recursos adicionales

>[!BEGINTABS]

>[!TAB Guías esenciales]

* [Simular variaciones de contenido](../using/test-approve/simulate-sample-input.md): pruebe hasta 30 contextos de personalización con archivos CSV o JSON. Ideal para pruebas de contenido multilingües sin crear varios perfiles de prueba. Admite tarjetas de correo electrónico, SMS, push, web, basadas en código, en la aplicación y de contenido.

* [Creación de perfiles de prueba](../using/audience/creating-test-profiles.md): cree y administre perfiles de prueba para simular casos de clientes. Obtenga información sobre cómo marcar perfiles para pruebas, establecer atributos y organizar segmentos de prueba.

* [Informe de correo no deseado](../using/content-management/spam-report.md): compruebe los índices de correo no deseado antes de enviar para mejorar la entregabilidad y la ubicación en la bandeja de entrada. Obtenga recomendaciones procesables para la optimización de contenido.

* [Preguntas frecuentes sobre el recorrido](../using/building-journeys/journey-faq.md): encuentre respuestas rápidas a preguntas comunes sobre las pruebas, la ejecución y la solución de problemas de recorridos.

>[!TAB Dependencias y relaciones]

Aprenda cómo las funciones de prueba se conectan entre sí y con los flujos de trabajo de Journey Optimizer en general. Esta sección asigna requisitos previos, dependencias de subida/bajada y combinaciones de capacidades comunes.

+++**Requisitos previos (necesarios antes de realizar la prueba)**

* Los perfiles de prueba deben crearse antes de utilizar el modo de prueba o la previsualización de contenido
* Las directivas de aprobación deben configurarse antes de enviarlas para su aprobación
* Se deben crear listas semilla antes de añadirlas a campañas/recorridos
* Integración de Litmus obligatoria para las pruebas de renderizado de correo electrónico
* El recorrido debe estar en estado de borrador para utilizar el modo de prueba
* El recorrido debe tener un espacio de nombres configurada para utilizar el modo de prueba

+++

+++**De qué depende la prueba (flujo ascendente)**

* Creación de contenido: necesita campañas o recorridos para realizar pruebas
* Perfiles de prueba: obligatorio para el modo de prueba y la previsualización de contenido
* Políticas de aprobación: obligatorias para flujos de trabajo de aprobación
* Configuración: configuraciones de canal, autenticación de correo electrónico, configuración de dominio

+++

+++**Lo que depende de las pruebas (flujo descendente)**

* Activación de campaña/recorrido: no se puede activar sin resolver errores
* Publicación: es posible que se requiera la aprobación antes de publicar
* Supervisión en directo: supervisión e informes posteriores al lanzamiento
* Optimización: utilice los resultados de las pruebas para refinar las campañas futuras

+++

+++**Funciones relacionadas**

* Flujos de trabajo de Prueba + Aprobación: proceso de garantía de calidad
* Pruebas + Detección de conflictos: prevención del exceso de mensajes de los clientes
* Pruebas + Experimentos de contenido: optimización del rendimiento
* Pruebas + Creación de informes: ciclo de mejora continua
* Perfiles de prueba + Personalization: validación de contenido
* Ensayo + Modo de prueba: validación completa del recorrido

+++

+++**Combinaciones de capacidades comunes**

* Prueba de contenido: Perfiles de prueba + Datos de entrada de muestra + Zona de juegos de personalización
* Validación de correo electrónico: pruebas de renderizado + Puntuaciones de correo no deseado + Perfiles de prueba + Pruebas
* Validación de recorrido: Modo de prueba + Ensayo + Perfiles de prueba
* Lista de comprobación previa al lanzamiento: todas las pruebas técnicas + detección de conflictos + flujos de trabajo de aprobación

+++

>[!TAB Preguntas frecuentes]

+++**P: ¿Qué pruebas se requieren antes de iniciar una campaña?**

**Mínimo:** Vista previa del contenido con perfiles de prueba + comprobación de puntuación de correo no deseado (correo electrónico)
**Recomendado:** + Renderizado de correo electrónico + Detección de conflictos + Flujo de trabajo de aprobación
**Práctica recomendada:** + Prueba de datos de entrada de muestra + Listas semilla + Experimento A/B (si se optimiza)

+++

+++**P: ¿Cómo puedo probar la personalización sin crear muchos perfiles de prueba?**

**Solución principal:** Use [datos de entrada de muestra](../using/test-approve/simulate-sample-input.md) con archivos CSV/JSON (admite hasta 30 variantes)
**Alternativa:** Cree de 3 a 5 [perfiles de prueba](../using/audience/creating-test-profiles.md) representativos que abarquen segmentos clave
**Herramienta de aprendizaje:** Experimente primero en [zona de juegos de personalización](../using/personalization/personalize.md#playground)

+++

+++**Q: ¿Cuál es la diferencia entre el modo de prueba y el ensayo para recorridos?**

**Modo de prueba:** Envía perfiles de prueba a través del recorrido, activa acciones reales y genera mensajes de prueba. Requiere recorrido de borrador + espacio de nombres.
**Ensayo:** rastrea las rutas de ejecución sin enviar nada. Funciona en cualquier estado de recorrido. No se envían mensajes ni se ejecutan acciones.
**Usar juntos:** Modo de prueba para la prueba de mensajes + Ensayo para la validación lógica: cobertura completa.

+++

+++**P: ¿Puedo probar recorridos en estado de producción/activo?**

**Modo de prueba:** No, solo recorridos de borrador
**Ensayo:** Sí, funciona en cualquier estado de recorrido
**Vista previa del contenido:** Sí, vista previa de mensajes individuales en cualquier momento
**Solución alternativa:** recorrido activo duplicado en borrador para validación completa del modo de prueba

+++

+++**P: ¿Qué capacidades de prueba requieren las integraciones externas?**

**Renderizado de correo electrónico:** requiere integración con Litmus (licencia independiente)
**Todas las demás:** integradas en Journey Optimizer, no se requieren integraciones adicionales
**Nota:** Los perfiles de prueba requieren el servicio Perfil del cliente en tiempo real (incluido)

+++

+++**P: ¿Cómo pruebo las campañas activadas por API?**

**Opción 1:** use [API de simulación de campaña](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} para pruebas programáticas
**Opción 2:** vista previa del contenido con perfiles de prueba en la interfaz de usuario
**Opción 3:** enviar pruebas para probar las direcciones de correo electrónico
**Práctica recomendada:** combine los tres para obtener una validación completa

+++

>[!ENDTABS]
