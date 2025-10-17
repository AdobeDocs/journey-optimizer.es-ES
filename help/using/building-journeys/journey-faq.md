---
solution: Journey Optimizer
product: journey optimizer
title: Preguntas más frecuentes sobre Recorrido
description: Preguntas frecuentes sobre Journey Optimizer Recorrido
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: recorrido, preguntas, respuestas, solución de problemas, ayuda, guía
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: d55aff6dd3773ad59ab45d2b6d7ced7b9a64de5d
workflow-type: tm+mt
source-wordcount: '4189'
ht-degree: 0%

---


# Preguntas frecuentes {#faq-journeys}

A continuación, encontrará las preguntas más frecuentes sobre los Recorridos de Adobe Journey Optimizer.

¿Necesita más detalles? Usa las opciones de comentarios de la parte inferior de esta página para plantear tu pregunta o conectar con la [comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

## Conceptos generales

+++ ¿Qué es un recorrido en Adobe Journey Optimizer?

Un recorrido es una orquestación de varios pasos que le permite diseñar y ejecutar experiencias del cliente en tiempo real en varios canales. Recorrido combina eventos, actividades de orquestación, acciones y mensajes para crear experiencias personalizadas y contextuales basadas en el comportamiento del cliente y los eventos comerciales.

Más información sobre [recorridos](journey.md).

+++

+++ ¿Cuáles son los diferentes tipos de recorridos?

Adobe Journey Optimizer admite cuatro tipos de recorridos:

* **recorridos unitarios**: Se activan individualmente mediante un evento (por ejemplo, una compra o el inicio de sesión en la aplicación). Los perfiles introducen el recorrido de uno en uno cuando se produce el evento.
* **Leer recorridos de audiencias**: Comience con una audiencia de Adobe Experience Platform y envíe mensajes en lote a todos los perfiles de esa audiencia.
* **recorridos de calificación de audiencia**: se activa cuando los perfiles cumplen los requisitos para un segmento de audiencia específico o salen de él. Los perfiles introducen el recorrido cuando cumplen los criterios de audiencia.
* **recorridos de eventos empresariales**: desencadenados por eventos empresariales (por ejemplo, actualizaciones de existencias o alertas meteorológicas) que afectan a varios perfiles simultáneamente.

Más información sobre [tipos de recorrido](entry-management.md#types-of-journeys).

+++

+++ ¿Cuál es la diferencia entre un recorrido y una campaña?

Los **Recorridos** son orquestaciones de varios pasos que reaccionan a eventos o audiencias de destino, lo que permite lógicas, condiciones, tiempos de espera y múltiples puntos de contacto complejos en el ciclo de vida del cliente.

**Las campañas** se dividen en tres tipos:

* **Campañas de acción**: las comunicaciones únicas o recurrentes enviadas a una audiencia específica son perfectas para mensajes independientes como anuncios promocionales o boletines informativos.
* **Campañas activadas por API**: campañas activadas a través de llamadas de API, lo que permite la integración con sistemas externos para enviar mensajes basados en eventos en tiempo real o lógica empresarial.
* **Campañas orquestadas**: campañas de varios pasos y basadas en audiencias que se basan en un lienzo que puede incluir condiciones, tiempos de espera y múltiples acciones para crear experiencias programadas y coordinadas.

**Práctica recomendada**: Use recorridos para una participación compleja activada por eventos con orquestación avanzada; campañas de acción para comunicaciones programadas y basadas en audiencias; campañas activadas por API para activación programática desde sistemas externos; y campañas orquestadas para comunicaciones de varios pasos con requisitos específicos de campañas.

+++

+++ ¿Cuáles son los componentes principales de un recorrido?

Un recorrido consta de:

* **Eventos**: puntos de entrada que almacenan en déclencheur el recorrido (por ejemplo, calificación de perfiles, eventos empresariales)
* **Actividades de orquestación**: componentes lógicos como condiciones, esperar, leer audiencia y finalizar
* **Acciones**: actividades que realizan tareas, como enviar mensajes, actualizar perfiles o llamar a API externas
* **Acciones de canal integradas**: Funciones de mensajería nativas para correo electrónico, SMS, push y otros canales
* **Acciones personalizadas**: integración con sistemas de terceros

Más información sobre [actividades de recorrido](about-journey-activities.md).

+++

+++ ¿Cómo puedo elegir entre un recorrido unitario y un recorrido de audiencia de lectura?

Usar **recorridos unitarios** cuando:

* Debe reaccionar ante las acciones individuales de los clientes en tiempo real (por ejemplo, confirmación de compra o abandono del carro de compras)
* Cada cliente debe progresar a su propio ritmo
* Desea almacenar en déclencheur según eventos específicos

Use **leer recorridos de audiencia** cuando:

* Está enviando comunicaciones por lotes a un grupo (por ejemplo, newsletter mensual, campañas promocionales)
* Todos los clientes deben recibir el mensaje aproximadamente a la misma hora
* Se está dirigiendo a un segmento de audiencia predefinido

+++

## Creación de recorridos

+++ ¿Cómo empiezo a construir mi primer recorrido?

Siga estos pasos clave:

1. **Configurar requisitos previos**: configure eventos, fuentes de datos y acciones según sea necesario
2. **Crear el recorrido**: vaya al menú Recorridos y haga clic en &quot;Crear Recorrido&quot;
3. **Definir propiedades de recorrido**: establezca el nombre del recorrido, la descripción, el área de nombres y otras opciones de configuración
4. **Diseñar el recorrido**: arrastre y suelte las actividades de la paleta en el lienzo
5. **Probar el recorrido**: use el modo de prueba para validar la lógica de recorrido
6. **Publicar el recorrido**: active el recorrido para activarlo

Siga la [guía paso a paso](journey-gs.md).

+++

+++ ¿Qué requisitos previos se necesitan antes de crear un recorrido?

Los requisitos previos dependen del tipo de recorrido:

* **recorridos activados por eventos**: configure eventos para definir cuándo los perfiles deben entrar en el recorrido
* **recorridos basados en audiencias**: Cree audiencias en Adobe Experience Platform
* **Enriquecimiento de datos**: configure orígenes de datos para recuperar información adicional
* **Integraciones de terceros**: configure acciones personalizadas si usa sistemas externos

Más información acerca de [configuración del recorrido](../configuration/about-data-sources-events-actions.md).

+++

+++ ¿Puedo utilizar datos de sistemas externos en mi recorrido?

Sí. Puede configurar **fuentes de datos externas** para recuperar información de servicios API de terceros y usarla en sus condiciones de recorrido, personalización o acciones. Esto le permite enriquecer la experiencia del cliente con datos en tiempo real de su CRM, sistemas de fidelidad, servicios meteorológicos u otras plataformas externas.

Más información sobre [orígenes de datos externos](../datasource/external-data-sources.md).

+++

+++ ¿Cómo se agregan condiciones al recorrido?

Puede agregar condiciones utilizando la **actividad de condición** desde la paleta de orquestación. Las condiciones le permiten:

* Cree condiciones simples o avanzadas con el editor de expresiones
* Divida el recorrido en varias rutas en función de atributos de perfil, pertenencia a audiencias, eventos o datos contextuales
* Defina rutas de tiempo de espera para perfiles que no cumplan la condición en un tiempo especificado

Más información sobre [condiciones](condition-activity.md).

+++

+++ ¿Puedo enviar mensajes a perfiles en un recorrido?

Sí. Journey Optimizer incluye **acciones de canal integradas** que le permiten enviar mensajes por correo electrónico, notificaciones push, SMS/MMS/RCS, mensajes en la aplicación, experiencias web, experiencias basadas en código, correo directo, tarjetas de contenido, WhatsApp y LINE. Puede diseñar contenido de mensajes directamente en Journey Optimizer y agregarlo como actividades de acción en el recorrido.

Más información acerca de [mensajes en recorrido](journeys-message.md).

+++

+++ ¿Cómo puedo esperar una hora o un evento específico en un recorrido?

Use la **Actividad de espera** para pausar el recorrido durante un tiempo especificado o hasta una fecha u hora específicas. Las actividades de espera son útiles para lo siguiente:

* Envío de mensajes de seguimiento después de un retraso (por ejemplo, 3 días después de la compra)
* Esperar al horario laboral antes de realizar acciones
* Creación de campañas de goteo con intervalos cronometrados
* Combinación con condiciones para crear escenarios de tiempo de espera

Más información sobre [actividades de espera](wait-activity.md).

+++

+++ ¿Puedo actualizar la información del perfil dentro de un recorrido?

Sí. Utilice la actividad **Actualizar perfil** para modificar los atributos de perfil en Adobe Experience Platform según las condiciones o los eventos de recorrido. Esto resulta útil para actualizar puntos de lealtad, registrar hitos de recorrido, cambiar la configuración de preferencias o rastrear puntuaciones de participación del cliente.

Más información sobre [actualizaciones de perfil](update-profiles.md).

+++

+++ ¿Cómo envío un correo electrónico inmediatamente después de que alguien realice una compra?

Crear un **recorrido activado por evento unitario**:

1. Configure un evento &quot;Purchase&quot; con los detalles del pedido
2. Añada el evento como punto de entrada de recorrido
3. Seguir inmediatamente con una acción de correo electrónico
4. Diseñe su correo electrónico de confirmación de pedido con detalles personalizados del pedido
5. Publicación del recorrido

El recorrido envía automáticamente un déclencheur cada vez que se recibe un evento de compra y envía el correo electrónico de confirmación en tiempo real.

Más información sobre [configuración de eventos](../event/about-events.md) y [acciones de correo electrónico](journeys-message.md).

+++

+++ ¿Puedo reenviar un mensaje si alguien no lo abre o hace clic en él?

Sí. Usar una **actividad de condición** combinada con **actividades de espera**:

1. Agregar una actividad de Wait (por ejemplo, wait 3 days)
2. Agregue una actividad Condición para comprobar si el correo electrónico se ha abierto o se ha hecho clic en él
3. Cree dos rutas:
   * **Si se abre o se hace clic**: finalice el recorrido o continúe con los pasos siguientes
   * **Si no se ha abierto o hecho clic**: envía un correo electrónico de recordatorio con una línea de asunto diferente

**Práctica recomendada**: Limite el número de reenvíos para evitar que aparezcan correos no deseados (normalmente, 1-2 recordatorios como máximo).

Más información sobre [eventos de reacción](reaction-events.md).

+++

+++ ¿Cómo se crea un recorrido de abandono del carro de compras?

Cree un recorrido activado por evento con lógica de espera y condición:

1. **Configurar un evento &quot;Abandonado del carro de compras&quot;**: Se activa cuando se agregan elementos, pero el cierre de compra no se completó dentro de un intervalo de tiempo
2. **Agregar una actividad de espera**: espere de 1 a 2 horas para que el cliente tenga tiempo de finalizar de forma natural
3. **Agregar una condición**: compruebe si la compra se completó durante la espera
4. **Si no se compró**: envía un correo electrónico de recordatorio de abandono con el contenido del carro de compras
5. **Opcional**: agrega otra espera (24 horas) y envía un segundo recordatorio con un incentivo (por ejemplo, 10% de descuento)

Más información sobre [casos de uso de recorrido](jo-use-cases.md).

+++

+++ ¿Cómo divido a los clientes en diferentes rutas en función de su historial de compras?

Usar una **actividad de condición** con atributos de perfil o pertenencia a audiencia:

1. Añada una actividad de Condición al recorrido
2. Cree varias rutas en función de ciertos criterios:
   * **Ruta 1**: Clientes de alto valor (compras totales > $1000)
   * **Ruta 2**: Clientes normales (compras totales de $100 a $1000)
   * **Ruta 3**: Clientes nuevos (compras totales &lt; 100 $)
3. Añadir diferentes mensajes u ofertas para cada ruta

Más información sobre las [condiciones](condition-activity.md) y la [calificación de audiencias](audience-qualification-events.md).

+++

+++ ¿Cómo puedo manejar diferentes zonas horarias en mi recorrido?

Journey Optimizer proporciona varias opciones para la administración de huso horario:

* **Zona horaria del perfil**: los mensajes se envían según la zona horaria de cada individuo almacenada en su perfil
* **Zona horaria fija**: todos los mensajes utilizan una zona horaria específica que usted defina
* **Esperar hasta una hora específica**: utilice la actividad Esperar para enviar mensajes a una hora específica en la zona horaria local del destinatario (por ejemplo, 10 a. m.)

**Ejemplo**: Para enviar un correo electrónico de &quot;Buenos días&quot; a las 9 a. m. en la zona horaria de cada cliente, use una actividad de espera con &quot;Esperar hasta una fecha u hora fijas&quot; y habilite la opción de zona horaria.

Más información sobre [administración de huso horario](timezone-management.md).

+++

+++ ¿Cuánto tiempo debo esperar entre mensajes en el recorrido?

**Prácticas recomendadas para tiempos de espera**:

* **Mensajes transaccionales** (confirmaciones de pedidos): enviar inmediatamente
* **Serie de bienvenida**: 1-3 días entre correos electrónicos
* **Contenido educativo**: de 3 a 7 días entre mensajes
* **Campañas promocionales**: al menos 7 días entre ofertas
* **Nuevo compromiso**: 14-30 días para usuarios inactivos

**Factores a considerar**:

* Estándares del sector y expectativas de los clientes
* Urgencia e importancia del mensaje
* Su frecuencia general de mensajería en todos los canales
* Patrones de participación del cliente

**Sugerencia**: Use reglas de límite de recorrido para limitar el número total de mensajes que un cliente recibe en todos los recorridos.

Más información sobre [actividades de espera](wait-activity.md) y [límite de recorrido](../conflict-prioritization/journey-capping.md).

+++

## Prueba y publicación

+++ ¿Cómo pruebo mi recorrido antes de publicarlo?

Journey Optimizer ofrece dos métodos de prueba:

* **Modo de prueba**: simule perfiles individuales que se mueven por el recorrido paso a paso, lo que le permite comprobar la lógica, las condiciones y las acciones antes de lanzarse.
* **Modo de ejecución en seco**: ejecute el recorrido utilizando datos de producción reales sin ponerse en contacto con los clientes reales ni actualizar la información del perfil. Esto le proporciona confianza en la segmentación de audiencias y en el diseño de recorridos.

**Práctica recomendada**: Pruebe siempre los recorridos antes de publicarlos para asegurarse de que funcionan según lo esperado e identificar cualquier problema antes de tiempo.

Obtenga más información sobre [modo de prueba](testing-the-journey.md) y [ejecución en seco](journey-dry-run.md).

+++

+++ ¿Qué sucede cuando publico un recorrido?

Al publicar un recorrido:

* El recorrido se vuelve **activo** y está listo para aceptar nuevos perfiles
* Los perfiles pueden entrar en función de los criterios de entrada (evento o audiencia)
* Los mensajes y las acciones empiezan a ejecutarse para los perfiles que se mueven a través del recorrido
* No puede editar directamente un recorrido publicado (debe crear una nueva versión)

Más información sobre [recorridos de publicación](publishing-the-journey.md).

+++

+++ ¿Se puede modificar un recorrido que ya se ha publicado?

No puede editar directamente un recorrido activo. Para realizar cambios:

1. **Crear una nueva versión**: duplique el recorrido publicado para crear una versión de borrador
2. **Realice los cambios**: edite la versión de borrador según sea necesario
3. **Probar la nueva versión**: use el modo de prueba para validar los cambios
4. **Publicar la nueva versión**: Esto cierra automáticamente la versión anterior y activa la nueva

Los perfiles que ya están en la recorrido completarán la versión original, mientras que los nuevos perfiles entrarán en la nueva versión.

Más información sobre [versiones de recorrido](journey-ui.md#journey-versions).

+++

+++ ¿Cómo detengo un recorrido?

Puede administrar la ejecución del recorrido de varias formas:

* **Cerca de nuevas entradas**: impida que entren nuevos perfiles y permita que los perfiles existentes completen su recorrido
* **Detener inmediatamente**: Finalice el recorrido y salga de todos los perfiles que hay actualmente en él
* **Pausar**: detenga temporalmente el recorrido y vuelva a reanudarlo más tarde (disponible para tipos de recorrido específicos)

Más información sobre [recorridos finales](end-journey.md).

+++

+++ ¿Cuál es la diferencia entre &quot;Cerca de nuevas entradas&quot; y &quot;Detener&quot;?

**Cerca de nuevas entradas**:

* Los nuevos perfiles no pueden entrar en el recorrido
* Los perfiles que ya están en la recorrido continúan y completan su ruta
* Utilícelo cuando desee reducir un recorrido con precisión
* Ejemplo: una campaña de temporada que ha finalizado pero en la que desea que los clientes existentes completen su experiencia

**Detener**:

* Finaliza inmediatamente el recorrido para todos los perfiles
* Se abandonan todos los perfiles que se encuentran actualmente en la recorrido
* Utilícelo para situaciones urgentes o errores críticos
* Ejemplo: Recuperación de productos que requiere la detención inmediata de los mensajes promocionales

Más información acerca de [opciones de pausa del recorrido](journey-pause.md).

+++

## Ejecución y monitorización del recorrido

+++ ¿Cómo puedo realizar un seguimiento del progreso del perfil a través de un recorrido?

Puede monitorizar la ejecución del recorrido mediante:

* **Informe en vivo de Recorridos**: vea métricas y KPI en tiempo real de su recorrido
* **Informe de Recorrido permanente**: Analice el rendimiento del recorrido con Customer Journey Analytics
* **Eventos de paso de Recorrido**: Acceda a datos de ejecución detallados para informes personalizados
* **Tablero de ejecución en seco de Recorrido**: revise los resultados de la ejecución de pruebas antes de lanzarse

Más información sobre [Informes de recorridos](report-journey.md).

+++

+++ ¿Por qué no ha introducido un perfil en mi recorrido?

Razones comunes por las que los perfiles no pueden introducir un recorrido:

* **Evento no recibido**: el evento de activación no se envió o no se configuró correctamente
* **No se cumplen los criterios de audiencia**: el perfil no cumple los requisitos para la audiencia de entrada
* **Reglas de reentrada**: el perfil que completó recientemente el recorrido y la reentrada está bloqueada
* **Recorrido no publicado**: el recorrido está en estado de borrador
* **Área de nombres no válida**: El área de nombres de recorrido no coincide con la identidad del perfil
* **Recorrido cerrado**: El recorrido ya no acepta nuevas entradas

Más información sobre [administración de entradas](entry-management.md).

+++

+++ ¿Qué son los eventos de paso de recorrido y cómo puedo utilizarlos?

Los eventos de paso de recorrido son conjuntos de datos generados automáticamente que capturan información detallada sobre cada paso que realiza un perfil en un recorrido. Incluyen eventos de entrada y salida, ejecución de acciones (mensajes enviados, acciones personalizadas denominadas), transiciones de recorrido (movimiento entre actividades) y errores y tiempos de espera.

**Casos de uso**:

* Creación de informes personalizados en herramientas de Customer Journey Analytics o BI
* Problemas de ejecución del recorrido Debug
* Seguimiento del comportamiento detallado del perfil
* Creación de análisis avanzados y modelos de atribución

Más información sobre [eventos de paso de recorrido](../reports/sharing-overview.md).

+++

+++ ¿Cómo puedo solucionar problemas de un recorrido que no funciona como se esperaba?

Journey Optimizer proporciona varios recursos para la resolución de problemas:

* **Indicadores de error**: las alertas visuales en el lienzo de recorrido resaltan los problemas de configuración
* **Modo de prueba**: revise el recorrido para identificar dónde se producen los problemas
* **informes de Recorrido**: revise las métricas de ejecución para encontrar cuellos de botella o errores
* **Eventos de paso de Recorrido**: Analice los datos de ejecución detallados para comprender el comportamiento del perfil

**Problemas comunes**:

* Eventos o audiencias configurados incorrectamente
* Faltan conexiones de origen de datos
* Expresiones no válidas en condiciones o personalización
* Configuración de tiempo de espera demasiado corto

Más información sobre [recorridos para solucionar problemas](troubleshooting.md).

+++

+++ ¿Qué sucede si una acción falla en un recorrido?

Cuando falla una acción (por ejemplo, tiempo de espera de llamada de API, error de envío de mensaje), el recorrido continúa de forma predeterminada a menos que se configure lo contrario. Puede definir actividades de condición para gestionar escenarios de error y los errores se registran en los informes de recorrido y en los eventos de paso para su monitorización.

**Práctica recomendada**: establezca valores de tiempo de espera adecuados para acciones externas y defina rutas alternativas para escenarios de error críticos.

Más información sobre [respuestas de acción](../action/action-response.md).

+++

+++ ¿Puedo ver quién está actualmente en mi recorrido en este momento?

Sí. Use el **Informe en vivo de Recorrido** para ver:

* Número de perfiles actualmente en el recorrido
* Número de perfiles en cada actividad
* Perfiles introducidos en las últimas 24 horas
* Métricas de ejecución en tiempo real

Para ver perfiles individuales, use **eventos de paso de recorrido** en Customer Journey Analytics o consulte los conjuntos de datos de evento de paso directamente.

Más información sobre [Informes en vivo de recorrido](report-journey.md).

+++

+++ ¿Por qué no se envían mis mensajes en mi recorrido?

**Razones y soluciones comunes**:

* **Problemas de consentimiento**: los destinatarios no se han suscrito para recibir comunicaciones
Solución: compruebe las políticas de consentimiento y el estado de inclusión

* **Lista de supresión**: las direcciones de correo electrónico están en la lista de supresión
Solución: revise la lista de supresión para ver si hay rechazos o quejas

* **Información de contacto no válida**: faltan direcciones de correo electrónico o números de teléfono incorrectos
Solución: valide la calidad de datos del perfil

* **Recorrido no publicado**: el recorrido sigue en modo de borrador
Solución: publique el recorrido para activarlo

* **Mensaje no aprobado**: el contenido del mensaje requiere aprobación antes de enviarlo
Solución: envíe para su aprobación o compruebe el estado de aprobación

* **Problema de configuración del canal**: La configuración de correo electrónico/SMS es incorrecta
Solución: compruebe las configuraciones de canal y la autenticación

Más información sobre [solución de problemas](troubleshooting.md) y [administración de consentimiento](../action/consent.md).

+++

+++ ¿Cómo puedo personalizar los mensajes en mi recorrido?

Puede personalizar mensajes mediante el **editor de personalización**:

**Datos de personalización disponibles**:

* **Atributos de perfil**: campos personalizados de nombre, apellido, correo electrónico
* **Datos del evento**: detalles de compra, comportamiento de navegación, actividad de la aplicación
* **Datos contextuales**: variables de Recorrido, datos de API externos
* **Pertenencia a audiencia**: Calificaciones del segmento
* **Atributos calculados**: Valores precalculados

**Ejemplo de personalización**:

* &quot;Hola {{profile.firstName}}, gracias por comprar {{event.productName}}&quot;
* &quot;En función de su nivel de fidelidad ({{profile.loyaltyTier}}), esta es una oferta especial&quot;
* Bloques de contenido dinámico que cambian según las preferencias de los clientes

Más información sobre [personalización](../personalization/personalize.md).

+++

+++ ¿Puedo enviar diferentes mensajes según el canal preferido?

Sí. Use una **actividad de condición** para comprobar el canal preferido:

1. Añada un perfil de comprobación de condición.ferredChannel
2. Cree rutas independientes para cada canal:
   * **Ruta de correo electrónico**: enviar mensaje de correo electrónico
   * **Ruta de SMS**: enviar mensaje SMS
   * **Ruta de inserción**: Enviar notificación push
3. Adición de una ruta predeterminada para perfiles sin preferencias

**Método alternativo**: usa **acciones multicanal** en las que Journey Optimizer selecciona automáticamente el mejor canal según las preferencias y disponibilidad del perfil.

Más información sobre [acciones del canal](journeys-message.md).

+++

+++ ¿Puedo excluir a ciertos clientes de mi recorrido?

Sí, hay varias formas de excluir a los clientes:

**En la entrada de recorrido**:

* Uso de definiciones de audiencia con reglas de exclusión
* Añadir condiciones de entrada que filtran perfiles específicos
* Configurar requisitos de área de nombres

**Dentro del recorrido**:

* Añada una actividad Condición al principio del recorrido para salir de perfiles no deseados
* Comprobar atributos de exclusión (por ejemplo, estado de VIP, cuentas de prueba)
* Use la calificación de audiencia para identificar perfiles que excluir

**Ejemplo de escenarios de exclusión**:

* Excluir clientes que compraron recientemente
* Excluir a los clientes de VIP de las promociones estándar
* Excluir empleados y cuentas de prueba
* Excluir clientes de regiones específicas

Más información sobre [administración de entradas](entry-management.md) y [condiciones](condition-activity.md).

+++

## Conceptos avanzados

+++ ¿Qué es un área de nombres de recorrido y por qué importa?

Un **área de nombres** es un tipo de identidad (por ejemplo, correo electrónico, ECID, número de teléfono) que determina cómo se identifican los perfiles en la recorrido. El área de nombres define qué identificador se utiliza para hacer coincidir perfiles, debe ser coherente en todos los eventos, audiencias y datos de perfil, y afecta al comportamiento de entrada y reentrada de recorrido.

**Práctica recomendada**: Elija un área de nombres que identifique de forma fiable a sus clientes en todos los puntos de contacto.

Más información sobre [áreas de nombres de identidad](../audience/get-started-identity.md).

+++

+++ ¿Pueden los perfiles introducir el mismo recorrido varias veces?

Sí, dependiendo de la **configuración de reentrada**:

* **Permitir la reentrada**: los perfiles pueden entrar en la recorrido varias veces después de completarla
* **Período de espera de reentrada**: defina un tiempo mínimo entre las entradas de recorrido (por ejemplo, 7 días)
* **Forzar reentrada en el evento**: almacene en Déclencheur una nueva instancia de recorrido aunque el perfil ya esté en el recorrido

**Práctica recomendada**: Use reglas de reentrada para evitar la fatiga del mensaje y garantizar un ritmo adecuado.

Más información sobre [administración de entradas](entry-management.md).

+++

+++ ¿Qué es la optimización del tiempo de envío?

**Optimización del tiempo de envío (STO)** usa IA para predecir el mejor momento para enviar un mensaje a cada perfil individual, lo que maximiza las tasas de apertura y la participación. STO analiza los patrones de participación históricos para determinar cuándo es más probable que cada destinatario interactúe con el mensaje.

**Beneficios**:

* Tasas de apertura y clics mejoradas
* Mejor experiencia del cliente mediante mensajes oportunos
* Tasas de cancelación de suscripción reducidas

Más información sobre [optimización del tiempo de envío](send-time-optimization.md).

+++

+++ ¿Qué son las reglas de límite de recorrido?

**Límite de Recorrido** le permite limitar la cantidad de veces que un perfil puede ingresar recorridos en un período de tiempo especificado, lo que evita la fatiga del mensaje y garantiza una experiencia óptima para el cliente. Puede establecer el máximo de entradas por perfil en recorridos o recorridos específicos, definir ventanas de tiempo (diaria, semanal, mensual) y priorizar recorridos cuando varios recorridos compitan por el mismo perfil.

Más información sobre [límite de recorrido](../conflict-prioritization/journey-capping.md).

+++

+++ ¿Puedo integrar mi recorrido con sistemas externos?

Sí. Utilice **acciones personalizadas** para llamar a API de terceros (CRM, automatización de marketing, sistemas de fidelidad), enviar datos a sistemas externos, recuperar información en tiempo real para la toma de decisiones y almacenar en déclencheur flujos de trabajo en plataformas externas.

Las acciones personalizadas admiten autenticación (clave de API, OAuth 2.0), personalización de la carga útil de solicitud/respuesta, gestión de errores y tiempos de espera, y parámetros dinámicos desde el contexto de recorrido.

Más información sobre las [acciones personalizadas](using-custom-actions.md).

+++

+++ ¿Cómo puedo usar Adobe Campaign con recorrido?

Journey Optimizer se integra de forma nativa con Adobe Campaign para aprovechar sus funciones avanzadas:

* **Adobe Campaign Standard**: usa acciones de Campaign Standard para enviar mensajes transaccionales
* **Adobe Campaign v7/v8**: los flujos de trabajo de la campaña de Déclencheur y el uso de la infraestructura de entrega de Campaign

**Práctica recomendada**: Utilice esta integración si ya tiene plantillas de Campaign, modelos de datos o necesita características específicas de Campaign.

Más información sobre la [integración de Campaign](ajo-ac.md).

+++

+++ ¿Qué es la actividad de salto?

La **actividad de salto** le permite hacer la transición de perfiles de un recorrido a otro, lo que permite patrones de recorrido reutilizables, orquestación de recorrido en varios recorridos, mantenimiento de recorrido simplificado y estrategias de participación progresiva.

Cuando un perfil alcanza una actividad de salto, sale del recorrido actual e introduce el recorrido de destino en su punto inicial.

Más información sobre [la actividad de salto](jump.md).

+++

+++ ¿Cómo se crea un recorrido de serie de bienvenida?

Una serie de bienvenida típica incluye varios puntos de contacto durante varios días:

**Estructura de ejemplo**:

1. **Entrada**: Audiencia de nuevos suscriptores o evento cuando alguien se registra
2. **Correo electrónico 1 - Bienvenida inmediata**: Gracias e introducción
3. **Esperar**: 2 días
4. **Correo electrónico 2 - Introducción**: Tutorial o guía del producto
5. **Esperar**: 3 días
6. **Condición**: ¿el cliente ha realizado una compra?
   * **Sí**: finalizar o mover al recorrido del cliente
   * **No**: continuar la serie de bienvenida
7. **Correo electrónico 3 - Incentivo**: descuento especial para el primer comprador
8. **Esperar**: 5 días
9. **Correo electrónico 4 - Participación**: Contenidos más vendidos o populares

**Prácticas recomendadas**:

* Manténgalo en 3-5 correos electrónicos durante 2-3 semanas
* Cada correo electrónico debe tener un propósito claro y call-to-action
* Monitorice las tasas de apertura y ajuste el tiempo/contenido en consecuencia
* Salga antes de tiempo de los clientes si convierten o interactúan en profundidad

Más información sobre [casos de uso de recorrido](jo-use-cases.md).

+++

+++ ¿Puedo probar diferentes rutas A/B en mi recorrido?

Sí. Use **Optimizar actividad** (disponible en paquetes específicos de Journey Optimizer) o cree divisiones de prueba de forma manual:

**Usando la actividad de optimización**:

* Divide automáticamente el tráfico entre variantes
* Prueba de diferentes mensajes, ofertas o rutas de recorrido completas
* Mide el rendimiento y declara un ganador

**Pruebas manuales con la condición**:

* Cree una condición que divida aleatoriamente los perfiles (por ejemplo, mediante una función de número aleatorio)
* Enviar diferentes experiencias a cada división
* Medir los resultados mediante informes de recorrido

**Lo que puede probar**:

* Líneas de asunto de correo electrónico diferentes
* Contenido de mensaje alternativo
* Tiempos de espera diferentes
* Varias ofertas o incentivos
* Rutas de recorrido completamente diferentes

Más información sobre [optimizar la actividad](optimize.md) y [experimentos de contenido](../content-management/content-experiment.md).

+++

+++ ¿Cómo se almacena en déclencheur un recorrido cuando el inventario es bajo?

Crear un **recorrido de evento empresarial**:

1. **Configurar un evento empresarial**: configure un evento activado por el sistema de inventario cuando las existencias caigan por debajo de un umbral
2. **Seleccionar audiencia de destino**: elija los perfiles a los que notificar (por ejemplo, clientes que vieron el producto, suscriptores a alertas de reabastecimiento)
3. **Agregar acción de mensaje**: Enviar correo electrónico de notificación o push
4. **Personalizar contenido**: incluya detalles del producto, nivel de inventario actual y mensajes de urgencia

**Ejemplo de eventos empresariales**:

* Alerta de inventario baja
* Notificación de caída de precios
* El producto vuelve a estar disponible
* Anuncio de venta Flash
* Promociones basadas en el tiempo

Más información sobre [eventos empresariales](general-events.md).

+++

+++ ¿Puedo pausar un recorrido para una persona específica sin detener todo el recorrido?

Aunque no puede pausar un recorrido para perfiles individuales directamente, puede lograr resultados similares:

**Opciones**:

* **Agregar a audiencia de exclusión**: cree una audiencia de perfiles para excluir y agregar una comprobación de condición de esta audiencia en puntos estratégicos del recorrido
* **Actualizar atributo de perfil**: establezca una marca de &quot;pausa&quot; en el perfil y use condiciones para omitir acciones en los perfiles marcados
* **Acción personalizada**: use un sistema externo para rastrear perfiles en pausa y comprobar el estado mediante una llamada de API
* **Salida manual**: En casos urgentes, puede quitar manualmente los perfiles de prueba

**Nota**: los cambios de Recorrido solo afectan a los nuevos participantes. Los perfiles que ya están en la recorrido siguen la ruta original a menos que la recorrido se detenga por completo.

+++

+++ ¿Cuál es la diferencia entre una condición y una actividad de espera?

**Actividad de condición**:

* **Propósito**: crea diferentes rutas basadas en lógica (si/entonces)
* **Función**: evalúa los datos y enruta los perfiles en consecuencia
* **Casos de uso**: Segmentar clientes, comprobar el estado, rama en función del comportamiento
* **Ejemplo**: Si el cliente es VIP, envíe una oferta premium; de lo contrario, envíe una oferta estándar

**Actividad de espera**:

* **Propósito**: Pausa la recorrido durante un período de tiempo
* **Función**: contiene perfiles en un punto específico antes de continuar
* **Casos de uso**: Intervalos entre mensajes, espera del horario laboral, creación de retrasos
* **Ejemplo**: espere 3 días después del correo electrónico de bienvenida antes de enviar el siguiente mensaje

**Trabajan juntos**:

* Espere un momento y, a continuación, utilice una Condición para comprobar si se ha producido algo durante la espera
* Ejemplo: Esperar 7 días y comprobar si el cliente realizó una compra

Más información sobre [condiciones](condition-activity.md) y [actividades de espera](wait-activity.md).

+++

## Prácticas recomendadas y limitaciones

+++ ¿Cuáles son las limitaciones clave que debo tener en cuenta?

Las barreras importantes incluyen:

* **Complejidad del Recorrido**: actividades máximas, rutas y niveles de anidación
* **Rendimiento**: tasas de envío de mensajes y límites de llamadas API
* **Tiempo de vida**: recorrido máximo (por ejemplo, 91 días para recorridos unitarios)
* **Tamaño de audiencia**: límites en los tamaños de lotes de audiencia de lectura
* **Complejidad de expresión**: límites de caracteres en condiciones y personalización

Ver [limitaciones y protecciones](../start/guardrails.md) completas.

+++

+++ ¿Cuáles son las prácticas recomendadas para el diseño de recorridos?

**Estructura y organización**:

* Mantenga los recorridos centrados en casos de uso específicos
* Utilice un nombre descriptivo para las actividades
* Agregar notas y etiquetas para una lógica compleja
* Agrupar recorridos relacionados con etiquetas

**Rendimiento**:

* Optimizar los tiempos de espera para equilibrar la participación y el volumen
* Limitar las llamadas de API externas a casos de uso esenciales
* Uso de reglas de límite para evitar la fatiga de mensajes
* Monitorización regular de métricas de recorrido

**Pruebas**:

* Probar siempre las recorridos antes de publicar
* Prueba de todas las rutas y escenarios condicionales
* Uso de perfiles de prueba realistas
* Validación de personalización y contenido dinámico

**Mantenimiento**:

* Revisar regularmente el rendimiento del recorrido
* Archivar o cerrar recorridos no utilizados
* Lógica de recorrido de documentos y reglas empresariales
* Plan de versiones de recorrido

Más información sobre [prácticas recomendadas de diseño de recorrido](using-the-journey-designer.md).

+++

+++ ¿Cuántas actividades puedo añadir a un recorrido?

Aunque no hay un límite estricto en el número de actividades, los recorridos muy complejos (más de 50 actividades) pueden resultar difíciles de mantener y solucionar. Los recorridos grandes con muchas ramas y condiciones pueden afectar al tiempo de procesamiento y a la legibilidad.

**Práctica recomendada**: Si el recorrido se vuelve demasiado complejo, considere la posibilidad de dividirlo en varios recorridos mediante la actividad de salto, la creación de recorridos secundarios reutilizables o la simplificación de la lógica con condiciones más eficientes.

Más información sobre [diseño de recorrido](using-the-journey-designer.md).

+++

+++ ¿Cómo puedo asegurarme de que mi recorrido funcione bien a escala?

**Consideraciones de diseño**:

* Utilice entradas basadas en audiencias para comunicaciones por lotes en lugar de eventos individuales
* Implementar tiempos de espera adecuados para propagar el volumen de mensajes
* Aproveche las reglas de límite para evitar la sobrecarga del sistema
* Optimizar la lógica de condición para reducir la complejidad del procesamiento

**Supervisión**:

* Seguimiento regular de métricas de recorrido
* Monitorización del rendimiento de la API para acciones personalizadas
* Revisar tasas de error y ocurrencias de tiempo de espera
* Configurar alertas para errores críticos de recorrido

**Optimización**:

* Utilice el modo de prueba y la ejecución en seco para validar el rendimiento antes de publicar
* Limitar las llamadas de fuentes de datos externas a escenarios esenciales
* Almacenar en caché los datos a los que se accede frecuentemente cuando es posible
* Revisión y optimización del rendimiento del envío de mensajes

Más información sobre [optimización de recorrido](../start/guardrails.md).

+++

## Recursos adicionales

Para obtener más información y actualizaciones, explore los siguientes recursos:

* [Introducción a los recorridos](journey.md)
* [Creación de su primer recorrido](journey-gs.md)
* [Guías de solución de problemas](troubleshooting.md)
* [Casos de uso de recorrido](jo-use-cases.md)
* [Descripción del producto Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
