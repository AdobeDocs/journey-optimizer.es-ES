---
solution: Journey Optimizer
product: journey optimizer
title: Elegir un método de validación
description: Compare la simulación de Recorrido, el modo de prueba de Recorrido y la ejecución en seco de Recorrido y elija el método de validación adecuado para el recorrido antes de publicar.
feature: Journeys, Get Started, Test Profiles
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: probar, simular, simulación, modo de prueba, ejecución en seco, recorrido, validar, comparar, elegir, guía de decisión
version: Journey Orchestration
source-git-commit: 52f7da843df1b3165aa6064efe893328413a7ad3
workflow-type: tm+mt
source-wordcount: '1621'
ht-degree: 0%

---


# Elegir un método de validación {#choose-validation-method}

>[!BEGINSHADEBOX]

**En esta página:** Comparar simulación de Recorrido, modo de prueba de Recorrido y ejecución en seco de Recorrido. Aprenda cuál se adapta a la fase actual de creación de un recorrido, desde una iteración rápida durante el diseño hasta una comprobación final previa al lanzamiento en comparación con la audiencia en directo.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] le ofrece tres formas de validar un recorrido antes de que se ponga en marcha. No son intercambiables: cada uno utiliza un tipo diferente de datos, se adapta a una fase diferente de la compilación y conlleva diferentes consecuencias en el mundo real. Comprender la diferencia por adelantado le ayuda a evitar dos errores comunes. La primera es dedicar tiempo a crear perfiles de prueba cuando lo haría una simulación rápida. La segunda es suponer que un paso de validación es completamente &quot;seguro&quot; cuando aún puede contactar bandejas de entrada reales o hacer llamadas salientes reales.

Esta página se centra en la validación del flujo de recorrido y la lógica de ramificación. Para obtener una imagen completa de las capacidades de prueba y aprobación, incluida la vista previa de contenido, el procesamiento de correo electrónico y las comprobaciones de correo no deseado, los experimentos A/B y los flujos de trabajo de aprobación, consulte [Probar, validar y aprobar](../../rp_landing_pages/test-landing-page.md).

## ¿Es nuevo en validación? Empiece aquí {#quick-pick}

Si no está seguro de qué método se aplica a usted, responda a esta pregunta:

* **Todavía estoy diseñando mi recorrido y deseo validar rápidamente la lógica de una rama, sin crear perfiles de prueba.** → Usar **[Simulación De Recorrido](simulate-journey-gs.md)**.
* **Quiero validar manualmente la lógica de mi borrador de recorrido paso a paso, usando perfiles reales (pero designados como prueba).** → Usar **[modo de prueba de Recorrido](testing-the-journey.md)**.
* **Estoy a punto de publicar y deseo una comprobación final de los volúmenes esperados con respecto a mi audiencia de producción real, sin ponerme en contacto con nadie.** → Usar **[Recorrido en seco](journey-dry-run.md)**.

¿Todavía no estás seguro, o quieres la imagen completa? Siga leyendo: cada método se explica en detalle a continuación.

## Los tres métodos de validación {#validation-methods}

>[!BEGINTABS]

>[!TAB Simulación de Recorrido]

**Cuándo se debe usar:** Iteración rápida durante el diseño del recorrido, especialmente justo antes de un plazo o al probar nuevas ramas o rutas. También funciona bien como método de validación continuo siempre que no resulta práctico crear un perfil de prueba adecuado para su caso de uso.

[Simulación de Recorrido](simulate-journey-gs.md) valida su recorrido con usuarios simulados temporales, sin necesidad de crear o esperar a que se propaguen los perfiles de prueba reales de Adobe Experience Platform (AEP). Puede crear usuarios simulados manualmente o permitir que AI genere automáticamente los eventos de prueba que necesita su recorrido y los asocie a los usuarios simulados adecuados, lo que activa el recorrido en segundos.

Mecánica clave:

* Los usuarios simulados no son perfiles reales en AEP; también puede guardarlos en el [inventario](simulate-journey.md#test-users) para reutilizarlos en simulaciones futuras en lugar de crearlos desde cero cada vez.
* No se evalúan los criterios de salida, las políticas de consentimiento, la restricción de frecuencia/recorrido, la exclusión/supresión y las horas de inactividad.
* Las acciones personalizadas y las llamadas a fuentes de datos externas siguen realizando llamadas salientes reales, no se burlan de ellas.

>[!IMPORTANT]
>
>La simulación envía mensajes reales a las [direcciones de ejecución](simulate-journey.md#test-users) (correo electrónico, teléfono, token push) configuradas en los usuarios simulados; por ejemplo, su propia dirección de correo electrónico. Utiliza la misma canalización de entrega que la producción. No contacta con clientes reales ni actualiza datos de perfil en directo, pero los mensajes en sí son reales.

**Perfecto para:** Validar una nueva rama (por ejemplo, dos nuevas rutas de directiva de decisión) sin esperar la propagación del perfil de prueba de AEP.

➡️ [Introducción a la simulación de recorrido](simulate-journey-gs.md) | [Simular su recorrido](simulate-journey.md)

>[!TAB Modo de prueba de Recorrido]

**Cuándo se debe usar:** Verificación manual de la rama y la lógica de mensaje paso a paso, con perfiles reales (pero designados como prueba) recorriendo el recorrido de borrador.

[Modo de prueba de Recorrido](testing-the-journey.md) le permite validar un recorrido de borrador usando [perfiles de prueba de AEP](../audience/creating-test-profiles.md) persistentes. Para confirmar que la lógica de ramificación y la mecánica de envío de mensajes funcionan según lo diseñado antes de que cualquier audiencia de producción toque el recorrido, active los eventos manualmente desde la interfaz.

Mecánica clave:

* Solo los perfiles marcados como &quot;perfiles de prueba&quot; en el Perfil del cliente en tiempo real pueden introducir un recorrido en el modo de prueba de Recorrido.
* El modo de prueba de recorrido solo está disponible para recorridos de borrador que utilicen un [espacio de nombres](../audience/get-started-identity.md), ya que debe comprobar en AEP si una persona es un perfil de prueba.
* Un máximo de 100 perfiles de prueba pueden entrar en un recorrido durante una sola sesión de prueba y los eventos solo se pueden activar desde la interfaz, no desde sistemas externos a través de la API.
* Al deshabilitar el modo de prueba de Recorrido se eliminan todos los perfiles que ingresaron a la recorrido y se borran los informes.

>[!IMPORTANT]
>
>El modo de prueba de recorrido envía mensajes reales a las bandejas de entrada reales de los perfiles de prueba, utilizando la misma canalización de entrega que la producción. No se pone en contacto con clientes reales, pero tampoco es una simulación &quot;en seco&quot;: asegúrese de que los perfiles de prueba utilizan direcciones que controla.

**Problema:** La creación y propagación de nuevos perfiles de prueba de AEP lleva tiempo. [Simulación de Recorrido](simulate-journey-gs.md) ofrece una alternativa rápida que no requiere ningún perfil de prueba. Resulta útil no solo mientras espera a que los perfiles se propaguen, sino que, en cualquier momento, la creación de un perfil de prueba adecuado para su caso de uso no es práctica.

➡️ [Prueba tu recorrido](testing-the-journey.md)

>[!TAB Recorrido en seco]

**Cuándo se debe usar:** Una comprobación final y realista de la producción justo antes de publicar.

[Ejecución en seco durante el Recorrido](journey-dry-run.md) es un modo especial de publicación de recorrido que ejecuta el recorrido con datos de segmentación y audiencia de producción real, sin ponerse en contacto con clientes reales ni actualizar información de perfil. El recorrido se activa como un recorrido activo y los perfiles fluyen a través de ramas y nodos exactamente como lo harían en la producción. Sin embargo, se omiten [nodos de acción](about-journey-activities.md), como correo electrónico, SMS y acciones personalizadas.

Mecánica clave:

* Utiliza la audiencia de producción real, para que vea el alcance real y la segmentación a escala (por ejemplo, detectar un error en el que una rama entera recibe inesperadamente cero perfiles).
* En cada activación, para recuperar las métricas más rápido puede deshabilitar las actividades de espera y, para mantener la recorrido en silo completo, puede deshabilitar las llamadas a fuentes de datos externas.
* Actualmente, esta es una característica de **disponibilidad limitada** que se está implementando globalmente a lo largo del tiempo.

**Perfecto para:** Detectar problemas como nodos de condición mal escritos o audiencias que inesperadamente no llegan a una rama, justo antes de activar la recorrido.

➡️ [Recorrido en seco](journey-dry-run.md)

>[!ENDTABS]

## ¿Qué método debería utilizar? {#decision-guide}

Comience con una pregunta sencilla: ¿ya tiene perfiles de prueba que se ajusten a su caso de uso? Si es así, **Modo de prueba de Recorrido** le permite validar paso a paso con ellos. Si no, o si no es práctico crearlos para este caso de uso en particular, **Simulación de Recorrido** te validará en segundos.

Más allá de esta opción, la respuesta suele responder a una pregunta más: *¿hasta dónde se acerca la producción?*

Si todavía **está iterando en el diseño de recorrido** — probando una rama nueva, comparando con un plazo — use **Simulación de Recorrido**. No necesita perfiles reales y se ejecuta en segundos. También sigue siendo una opción válida más adelante en la compilación, siempre que no sea práctico crear perfiles de prueba adecuados para el caso de uso. Recuerde que envía mensajes reales a las direcciones de ejecución configuradas en los usuarios simulados.

Si necesita **comprobar manualmente la bifurcación y la lógica de mensajes paso a paso** y desea crear o reutilizar perfiles de prueba de AEP, use **Modo de prueba de Recorrido**. Solo recuerde que envía mensajes reales a las bandejas de entrada reales de esos perfiles de prueba.

Si está a punto de **publicar** y desea una comprobación final de los volúmenes esperados con respecto a la audiencia de producción real, use **Ejecución en seco del Recorrido**. Nunca se pone en contacto con nadie ni cambia ningún dato de perfil.

>[!TIP]
>
>**¿No está seguro de por dónde empezar?** La mayoría de los equipos usa **Simulación de Recorrido** al generar y luego **Ejecución en seco de Recorrido** justo antes de publicar. Alcance el **modo de prueba de Recorrido** cuando necesite recorrer manualmente la lógica de rama con perfiles de prueba reales en lugar de los simulados.

## Comparación rápida {#quick-comparison}

| Método | Datos utilizados | ¿Envía mensajes reales? | Mejor para |
|---|---|---|---|
| [Simulación de Recorrido](simulate-journey-gs.md) | Usuarios simulados temporales, creados manualmente o autogenerados | Sí: a las direcciones de ejecución configuradas en los usuarios simulados | Iteración rápida en nuevas ramas o rutas, sin esperar a la propagación real del perfil de prueba |
| [Modo de prueba de Recorrido](testing-the-journey.md) | Perfiles de prueba de AEP persistentes | Sí: a las bandejas de entrada reales de los perfiles de prueba, mediante la canalización de entrega de producción | Verificación manual de la lógica de bifurcación/mensaje paso a paso en un borrador de recorrido |
| [Recorrido en seco](journey-dry-run.md) | Audiencia/datos de producción real | No (acciones omitidas) | Comprobación final previa al lanzamiento de alcance de audiencia, segmentación y lógica de rama reales a escala real |

Ninguno de estos métodos contacta con clientes reales. Los datos de perfil tampoco se tocan en todos los casos, excepto en que el modo de prueba de Recorrido actualiza los perfiles de prueba utilizados para ejecutarlos (no los perfiles reales del cliente).

## Errores comunes que se deben evitar {#common-mistakes}

* **Suponiendo que la simulación de Recorrido es completamente &quot;segura&quot;.** Es la forma más rápida de realizar pruebas, pero sigue enviando mensajes reales a la dirección de ejecución configurada en cada usuario simulado, normalmente en su propia bandeja de entrada. No suponga que no se envía nada.
* **Creando perfiles de prueba de AEP cuando la simulación de Recorrido funcionaba.** Si solo necesita validar una nueva rama o ruta de política de decisión rápidamente, la simulación omite la espera de la propagación del perfil de prueba por completo: el modo de prueba Guardar Recorrido para cuando realmente necesite perfiles de prueba reales.
* **Tratando el modo de prueba de Recorrido como &quot;seco&quot;.** Los perfiles del modo de prueba de recorrido reciben mensajes reales a través de la canalización de entrega de producción. Asegúrese de que los perfiles de prueba solo utilicen las direcciones que controla.
* **Se espera que la ejecución en seco del Recorrido detecte problemas de contenido o envío.** La ejecución en seco omite los nodos de acción por completo: valida el alcance de la audiencia y la lógica de rama, no el contenido del mensaje ni la mecánica de envío. Para ello, utilice el modo de simulación o el modo de prueba de Recorrido.
* **Olvidando el requisito del área de nombres para el modo de prueba de Recorrido.** El modo de prueba de recorrido solo funciona en recorridos de borrador que utilizan un área de nombres, ya que Journey Optimizer necesita un área de nombres para comprobar si un perfil está marcado como perfil de prueba.

## Próximos pasos {#next-steps}

* **[Introducción a la simulación de recorrido](simulate-journey-gs.md)** — Ejecute su primera simulación
* **[Probar el recorrido](testing-the-journey.md)** — Activar el modo de prueba de Recorrido con perfiles de prueba de AEP
* **[Ejecución en seco de Recorrido](journey-dry-run.md)**: ejecute una ejecución en seco realista para la producción
* **[Publicar su recorrido](publish-journey.md)**: Requisitos previos y proceso de publicación
* **[Introducción a recorrido](journey.md)**: Información general sobre aspectos básicos y funcionalidades
* **[Preguntas frecuentes sobre Journey Orchestration](journey-faq.md)** — Preguntas frecuentes respondidas
* **[Probar, validar y aprobar](../../rp_landing_pages/test-landing-page.md)**: entorno de prueba y aprobación completo, que incluye vista previa de contenido, comprobaciones de procesamiento/correo no deseado, experimentos y flujos de trabajo de aprobación

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-choose-validation-method.md}}
