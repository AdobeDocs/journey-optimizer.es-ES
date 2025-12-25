---
solution: Journey Optimizer
product: Journey Optimizer
title: Prueba y aprobación
description: Prueba y aprobación
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 11%

---

# Prueba y aprobación{#section-overview}

La garantía de calidad es fundamental para ofrecer experiencias de cliente excepcionales. Adobe Journey Optimizer proporciona funciones completas de prueba y aprobación para ayudarle a validar el contenido, comprobar la lógica de recorrido y garantizar que las campañas cumplan los estándares de calidad antes de llegar a su audiencia. Desde la previsualización de mensajes personalizados con perfiles de prueba hasta la simulación de flujos de recorrido complejos, estas herramientas le permiten identificar y resolver problemas de forma temprana, reducir el riesgo y mantener la integridad de la marca. Tanto si desea probar el procesamiento de correo electrónico en varios dispositivos, validar recorridos de varios pasos o establecer flujos de trabajo de aprobación formales, esta sección le guía a través de las prácticas recomendadas y los procesos paso a paso para confiar en sus campañas y recorridos. Al implementar pruebas exhaustivas y aprobaciones estructuradas, minimizará los errores, mejorará la capacidad de entrega y creará experiencias perfectas que resuenen con sus clientes.

## Por qué importan las pruebas y la aprobación

Los procesos de prueba y aprobación sirven como puertas de calidad esenciales que protegen la reputación de su marca y garantizan el éxito de la campaña. He aquí por qué importan:

* **Detecte errores antes de que lleguen a los clientes**: identifique los vínculos rotos, la personalización incorrecta, los problemas de procesamiento y los errores lógicos en un entorno controlado en el que las correcciones sean rápidas y sin riesgos.

* **Mejore la capacidad de envío**: pruebe las puntuaciones de spam, valide la autenticación de correos electrónicos y compruebe el procesamiento en todos los clientes de correo electrónico para maximizar la ubicación de la bandeja de entrada y las tasas de participación.

* **Garantizar la coherencia de la marca**: obtenga una vista previa del contenido con diferentes perfiles de prueba para verificar que la personalización se muestre correctamente para varios segmentos de clientes y mantenga los estándares de marca.

* **Validar recorridos complejos**: simule flujos de recorrido de varios pasos para confirmar que los déclencheur se activan correctamente, que las condiciones se evalúan correctamente y que los clientes reciben los mensajes correctos en el momento adecuado.

* **Establecer la responsabilidad**: Implemente flujos de trabajo de aprobación formales que requieran la firma de las partes interesadas, lo que crea una propiedad clara y reduce los inicios de campaña no autorizados o prematuros.

* **Ahorre tiempo y recursos**: detecte problemas al principio del ciclo de desarrollo cuando las correcciones sean más baratas y rápidas, lo que evitará costosas correcciones posteriores al inicio o escalaciones del servicio de atención al cliente.

## Prácticas recomendadas de prueba

Para maximizar la eficacia de sus esfuerzos de prueba, siga estas prácticas recomendadas:

1. **Realizar pruebas antes y con frecuencia**: no espere hasta que una campaña esté completamente creada. Pruebe el contenido, la personalización y la lógica gradualmente a medida que desarrolla.

1. **Use perfiles de prueba realistas** - [Cree perfiles de prueba](../using/audience/creating-test-profiles.md) que representen con precisión los segmentos de audiencia de destino, incluidos casos extremos y diferentes escenarios de personalización.

1. **Realizar pruebas entre dispositivos y clientes**: compruebe el [procesamiento de correo electrónico](../using/content-management/rendering.md) en clientes de correo electrónico (Gmail, Outlook, Apple Mail) y dispositivos (escritorio, móvil, tableta) populares para garantizar una visualización coherente.

1. **Validar la personalización a fondo**: realice pruebas con varios [perfiles de prueba](../using/content-management/test-profiles.md) que tengan valores de atributo diferentes para confirmar que los tokens de personalización se representen correctamente y que los valores de reserva funcionen.

1. **Simular rutas de recorrido**: para recorridos complejos con varias ramas, use [modo de prueba](../using/building-journeys/testing-the-journey.md) para probar diferentes condiciones de entrada y atributos de perfil y validar todas las rutas posibles.

1. **Comprobar indicadores de entrega**: revise [puntuaciones de correo no deseado](../using/content-management/spam-report.md), estado de autenticación y métricas de estado de correo electrónico antes de envíos grandes.

1. **Documentar resultados de pruebas**: mantenga registros de los resultados de las pruebas, los problemas encontrados y las resoluciones para mejorar los procesos de pruebas futuros y compartir los conocimientos con su equipo.

1. **Involucre a las partes interesadas desde el principio** - Comparta vistas previas y resultados de pruebas con las partes interesadas antes de la [aprobación formal](../using/test-approve/gs-approval.md) para recopilar comentarios y alinear expectativas.

## Flujo de trabajo de pruebas recomendado

Siga este enfoque sistemático para garantizar pruebas exhaustivas y aprobaciones sin problemas:

### &#x200B;1. Desarrollo y previsualización de contenido

Comience creando el contenido y utilizando las funcionalidades de previsualización para verificar el diseño y la personalización iniciales:

* Diseña tu [correo electrónico](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [notificación push](../using/push/create-push.md) u otro contenido del canal
* Usar la característica **[Simular contenido](../using/content-management/preview-test.md)** para obtener una vista previa con perfiles de prueba
* Compruebe [tokens de personalización](../using/personalization/personalization-syntax.md), contenido dinámico y valores de reserva
* Verificar [renderización](../using/content-management/rendering.md) en diferentes tamaños de pantalla y clientes de correo electrónico

### &#x200B;2. Validación técnica

Valide los aspectos técnicos que afectan a la capacidad de entrega y la funcionalidad:

* Ejecute [comprobaciones de puntuación de correo no deseado](../using/content-management/spam-report.md) para identificar posibles problemas de envío
* Pruebe los vínculos para asegurarse de que no están rotos y de que se realiza un seguimiento adecuado
* Validar la configuración de [autenticación por correo electrónico](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC)
* Revise el procesamiento de HTML y compruebe los problemas de compatibilidad con CSS
* Probar [diseño interactivo](../using/email/content-from-scratch.md) en dispositivos móviles y de escritorio

### &#x200B;3. Ensayos de Recorrido

Para los recorridos, valide la lógica de orquestación:

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

* **[Envío de mensajes multicanal](../using/building-journeys/journeys-uc.md)**: este caso de uso muestra cómo probar un recorrido que combina Audiencia de lectura, eventos de reacción y mensajes de correo electrónico/push. Aprenda a validar todo el flujo, desde la segmentación de audiencia hasta la entrega de mensajes, y vea los pasos de prueba y publicación en acción.

* **[Enviar un mensaje a los suscriptores](../using/building-journeys/message-to-subscribers-uc.md)**: descubre cómo probar recorridos dirigidos a listas de suscripción con direccionamiento de correo electrónico dinámico. Este ejemplo muestra cómo validar expresiones de personalización y garantizar que los mensajes llegan a los suscriptores correctos.

* **[Enviar mensajes con tiempo limitado](../using/building-journeys/weekday-email-uc.md)**: aprenda a probar recorridos con condiciones basadas en el tiempo para asegurarse de que los mensajes se envíen en días específicos. Consulte cómo validar las actividades de espera y la lógica de programación.

* **[Explorar más casos de uso de recorrido](../using/building-journeys/jo-use-cases.md)**: acceda a una completa colección de ejemplos prácticos que abarcan eventos de experiencia, mensajería multicanal e integraciones de sistemas externos.

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

Valide el recorrido antes de publicarlo probándolo con perfiles específicos para garantizar que los eventos, las condiciones y las acciones funcionan según lo esperado.

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

::::

## Recursos adicionales

### Guías esenciales de prueba y validación

* [Informe en vivo en su Recorrido](../using/building-journeys/report-journey.md): supervise las métricas de recorrido en tiempo real para rastrear el rendimiento e identificar problemas durante la ejecución. Acceda a desgloses detallados de progresión de perfiles, déclencheur de eventos y tasas de finalización de acciones.

* [Creación de perfiles de prueba](../using/audience/creating-test-profiles.md): cree y administre perfiles de prueba para simular escenarios de clientes reales y validar la personalización. Obtenga información sobre cómo marcar perfiles para pruebas, establecer valores de atributos y organizar segmentos de perfiles de prueba.

* [Informe de correo no deseado](../using/content-management/spam-report.md): compruebe su puntuación de correo no deseado antes de enviarlo para mejorar la entrega y la ubicación en la bandeja de entrada. Comprenda cómo los filtros de correo no deseado evalúan el contenido y obtienen recomendaciones para su mejora.

* [Preguntas frecuentes sobre el Recorrido](../using/building-journeys/journey-faq.md): encuentre respuestas a preguntas comunes sobre la creación de recorridos, las pruebas, la ejecución y la solución de problemas. Referencia rápida para resolver problemas frecuentes y comprender el comportamiento del recorrido.

### Temas relacionados

* [Administración de contenido](content-management-landing-page.md): aprenda a diseñar, previsualizar y administrar contenido mediante plantillas, fragmentos y Designer de correo electrónico. Domine las prácticas recomendadas de creación de contenido para lograr una marca coherente.

* [Informes y análisis](reporting-landing-page.md): Analice el rendimiento de la campaña y del recorrido con informes, paneles y métricas completos. Tome decisiones basadas en datos para optimizar las experiencias de los clientes.

* [Configuración de Recorrido](configure-journeys-landing-page.md): configure las fuentes de datos, los eventos y las acciones personalizadas para habilitar la orquestación de recorrido sofisticada. Establecer las bases técnicas para la creación de recorridos.

* [Administración de campañas](../using/campaigns/get-started-with-campaigns.md): explora diferentes tipos de campañas y aprende a crear, programar y optimizar campañas por lotes y en tiempo real para lograr el máximo impacto.
