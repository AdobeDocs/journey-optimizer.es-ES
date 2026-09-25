---
solution: Journey Optimizer
product: journey optimizer
title: Compañero de trabajo para recorridos
description: Descubra las habilidades de CX Enterprise Coworker disponibles para crear, generar contenido y analizar recorridos en Adobe Journey Optimizer, con instrucciones detalladas e instrucciones de ejemplo.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 932218c2-64c1-466e-afc4-120b6d8fe37f
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
    internal-label: Journey management
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
    internal-label: Journey design
source-git-commit: ccc5aca071477ef6ba6bd34cf609aeecaaae661c
workflow-type: tm+mt
source-wordcount: '2594'
ht-degree: 7%
---

# Compañero de trabajo para recorridos {#journeys-coworker-skills}

>[!BEGINSHADEBOX]

**En esta página:** Descubra las habilidades de CX Enterprise Coworker disponibles para los recorridos en Adobe Journey Optimizer (crear recorridos a partir de lenguaje natural, generar contenido de canal y analizar el rendimiento del recorrido) con instrucciones detalladas, indicaciones de ejemplo y prácticas recomendadas para cada habilidad.

Más información:

* [Aptitudes de colaborador para Journey Optimizer](../start/ai-features.md#cx-coworker-skills): información general sobre las aptitudes de colaborador en todos los Recorridos, lealtad, administración de contenido y toma de decisiones en Journey Optimizer.
* [Documentación de los compañeros](https://experienceleague.adobe.co/es/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"}: información general sobre las capacidades de Campañas, Conversaciones y Proyectos de los compañeros.
* [Guía de la interfaz de usuario de Coworker Chat](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"}: cómo acceder y navegar por Coworker Chat.

>[!ENDSHADEBOX]

## Crear recorrido {#journey-create}

Recorrido Crear permite a los usuarios de Journey Optimizer crear y configurar recorridos de marketing mediante una interfaz de lenguaje natural. Con Recorrido Crear, los profesionales pueden crear recorridos rápidamente al describir sus necesidades en mensajes de conversación. La aptitud guía a los usuarios por las diferentes opciones para crear un recorrido, lo que permite a los especialistas en marketing centrarse en la estrategia en lugar de en la configuración técnica.

>[!AVAILABILITY]
>
>Necesita los siguientes permisos para utilizar completamente las funciones de creación de Recorrido:
>
>**Administrar Recorridos**: este permiso le permite crear nuevos recorridos directamente en Compañero de trabajo.
>
>**Ver eventos de Recorrido, fuentes de datos y acciones**: este permiso garantiza que el colaborador pueda buscar en eventos de Recorrido y acciones personalizadas.
>
>**Ver segmentos**: Este permiso garantiza que el compañero pueda buscar segmentos de audiencia al crear un Recorrido.
>
>**Administrar segmentos**: Este permiso le permite crear nuevas audiencias directamente en Compañero de trabajo.

### Casos de uso clave

Recorrido Cree ofertas que se puedan aprovechar para acelerar la ejecución del marketing:

* **Creación de recorrido desencadenada por eventos**

  * Cree recorridos que se activen en función de eventos de clientes específicos.
  * Diseñar respuestas automatizadas a acciones de clientes en tiempo real.
  * Cree flujos de comunicación personalizados basados en el comportamiento de los clientes.

  **recorrido de visitas a tiendas:**
  &quot;Crear un recorrido que se inicie cuando un usuario entre en mi ubicación de tienda. Envíe una notificación push para dar la bienvenida a los usuarios a la tienda. Espere 2 días y compruebe si el usuario tiene una dirección de correo electrónico válida. Si el usuario tiene una dirección de correo electrónico válida, envíe un sondeo por correo electrónico para preguntar por su experiencia en la tienda. Si el usuario no tiene una dirección de correo electrónico válida, envíe una notificación push para solicitar el registro&quot;.

  **recorridos posteriores a la compra:**
  &quot;Cree un recorrido que se inicie cuando un cliente realice una compra en línea. Envíe una notificación push para agradecerles su compra. A continuación, compruebe si son miembros socio. Si el usuario es un abonado de las recompensas por fidelidad, envíe una segunda notificación push con un código de descuento del 10 %. Si el usuario no es un miembro de las recompensas por fidelidad, envía una notificación push invitándolo a registrarse en el programa de fidelidad. Espere 2 días y envíe una notificación push de seguimiento con una encuesta sobre su experiencia de compra&quot;.

  **Promoción basada en eventos:**
  &quot;Crea un recorrido cuando la puntuación del juego alcance 50. Envíe un mensaje SMS a los miembros de la recompensa de fidelidad diciendo que cumplen los requisitos para una porción gratuita de pizza del patrocinador del socio&quot;.

* **Creación de recorrido con destino de audiencia**

  * Genere recorridos dirigidos a segmentos de audiencia específicos.
  * Diseñe secuencias de comunicación de varios pasos con sincronización estratégica.

  **Campaña estacional:**
  &quot;Quiero crear un recorrido dirigido a una audiencia de excursionistas. Quiero enviar un correo electrónico alertando a esta audiencia sobre mi próxima venta de vacaciones que incluye una variedad de elementos esenciales para el senderismo. Espere 3 días después de enviar el primer correo electrónico y envíe un segundo correo electrónico que tenga un cupón del 15% con envío gratuito. Espere 1 semana y luego envíe un tercer mensaje de correo electrónico para mostrar nuestro nuevo saco de dormir y la colección de la tienda. Programe el recorrido para que comience el 20/12&quot;.

  **Agradecimiento por la fidelidad:**
  &quot;Cree un recorrido de apreciación de la lealtad para los propietarios de SUV, que incluya una notificación push de agradecimiento con una oferta de lavado de coches gratis y un recordatorio de notificación push de seguimiento si no se interactúa con la primera notificación en el plazo de 1 día&quot;.

* **Creación de recorrido desencadenada por evento empresarial**

  * Cree recorridos que se activen en función de un evento empresarial determinado y se dirijan a una audiencia específica (por ejemplo, producto disponible o cambio de puntuación de juego)
  * Déclencheur mensajes oportunos y según el contexto cuando cambian las condiciones empresariales.

* **Creación del recorrido de calificación de audiencia**

  * Cree recorridos que se activen cuando los perfiles entran o salen de una definición de segmento de audiencia.
  * Automatice la mensajería de entrada y salida para lograr los objetivos de incorporación, retención y recuperación.

* **Flujos de recorrido condicionales**

  * Cree ramas de decisión basadas en atributos del cliente.
  * Diseñe rutas divididas que se adapten a las preferencias de los clientes.

* **Crear recorrido a partir de la imagen**

  * Cargue una imagen de referencia en Coworker y pida crear un recorrido con la imagen como referencia
  * La aptitud para crear recorridos extraerá un mensaje editable de la imagen de referencia

Con esta aptitud, los requisitos del lenguaje natural se traducen en configuraciones de recorrido estructuradas.

### Aptitudes en el ámbito

Recorrido Crear admite las siguientes funciones:

* **Creación de recorridos en lenguaje natural**: permite a los usuarios describir el flujo de recorrido en lenguaje conversacional.
* **recorridos basados en eventos y en audiencias**: admite tipos de recorridos programados y basados en déclencheur, así como eventos comerciales y calificación de audiencias.
* **Lógica condicional**: administra las divisiones y ramas de decisión en función de los atributos del cliente.
* **Mensajería multicanal**: Admite notificaciones push, correo electrónico y canales SMS.
* **Programación de Recorridos**: Configura las fechas de inicio y el horario de los recorridos programados.

### Aptitudes fuera del ámbito

Actualmente no se admiten las siguientes funcionalidades:

* Análisis de recorrido avanzado
* Orquestación entre recorridos
* Configuración de prueba A/B
* Generación de expresiones InAudience
* Nodos de búsqueda de conjuntos de datos
* Configuración de envío de ondas
* Programar opciones de periodicidad
* Selección de área de nombres para audiencias
* Asignación de campos de acción personalizada
* Transformaciones de datos complejas

### Impulso de las prácticas recomendadas

Para maximizar la eficacia de Creación de Recorridos, siga estas prácticas recomendadas:

* **Sea específico**: Proporcione detalles claros sobre sus objetivos de recorrido, audiencia de destinatario y acciones deseadas. Incluya información sobre canales, temporización y condiciones.
* **Especificar tiempo**: indique claramente los períodos de espera entre las acciones y cuándo debe iniciarse el recorrido.
* **Definir condiciones**: cuando use la lógica condicional, explique los criterios para cada ruta de bifurcación.
* **Incluir canales**: especifique qué canales de comunicación desea utilizar (push, correo electrónico, SMS).
* **Programación de menciones**: para los recorridos programados, proporcione la fecha y la hora de inicio que desee.
* **Acciones personalizadas**: si usa acciones personalizadas en el flujo de trabajo, debe especificar que usa una acción personalizada junto con el nombre exacto de la acción personalizada. Por ejemplo:
Cuando un usuario entre en mi ubicación de tienda, enviar un mensaje de bienvenida mediante la acción personalizada ExternalPush. Espere 2 días y, a continuación, envíe un mensaje de seguimiento mediante una acción personalizada por correo electrónico externo con una encuesta sobre su visita.
* **Validar expresiones**: asegúrese de comprobar y validar cualquier expresión que las aptitudes de Recorrido creen para asegurarse de que se utilizan los campos y valores correctos.

### Prácticas recomendadas de configuración

* **Definir objetivos claros**: antes de crear recorridos, establezca objetivos claros (mejorar la retención, impulsar las conversiones y aumentar la participación).
* **Preparar audiencias**: Asegúrese de que las audiencias de destino ya se hayan creado y segmentado correctamente.
* **Planificar contenido del mensaje**: Defina su estrategia de mensajería antes de crear el recorrido.
* **Tenga en cuenta la experiencia del cliente**: Diseñe flujos de recorrido que respeten las preferencias del cliente y eviten la comunicación excesiva.

## Creación de contenido de canal {#channel-content-create}

>[!AVAILABILITY]
>
>Esta función está disponible para todos los clientes con disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

La creación de contenido de canal permite a los usuarios de Journey Optimizer generar, editar y administrar contenido específico del canal para recorridos mediante la generación de contenido con tecnología de IA.

### Casos de uso clave

* **Generación de contenido específico del canal**: genere contenido para correo electrónico, notificaciones push, SMS y otros canales mediante mensajes en lenguaje natural.

  &quot;Generar contenido de correo electrónico para mi recorrido de bienvenida. Cree un correo electrónico de bienvenida para nuevos clientes con un tono cordial e incluya una oferta de descuento del 10 %&quot;.

  &quot;Generar una notificación push para el recorrido de mi visita a la tienda. Cree un mensaje de bienvenida que anime a los clientes a registrarse y recibir una oferta especial&quot;.

  &quot;Generar contenido SMS para mi recorrido activado por eventos. Cree un mensaje corto para notificar a los clientes sobre una venta flash con un call-to-action&quot;.

* **Creación de contenido basado en plantillas**: busca y selecciona entre las plantillas disponibles con capacidades de vista previa.

  &quot;Mostrarme las plantillas de correo electrónico disponibles para mi recorrido de campaña de temporada&quot;.

  &quot;Seleccione una plantilla para mi correo electrónico que tenga un diseño moderno y limpio.&quot;

* **Administración de contenido multicanal**: genera y administra contenido para varios canales dentro del mismo flujo de trabajo de recorrido.

* **Edición de contenido en contexto**: abra el contenido generado en Content Designer para editarlo y refinarlo.

  &quot;Abra el contenido del correo electrónico en Content Designer para poder personalizar el diseño&quot;.

* **Refinamiento e iteración del contenido**: Regenera el contenido con diferentes tonos o estilos mediante la acción Regenerar.

  &quot;Regenerar el contenido de las notificaciones push con un tono más informal&quot;.

  &quot;Actualice el contenido del correo electrónico para incluir un código promocional.&quot;

* **Integración de lienzo de Recorrido**: seleccione recorridos del inventario y vea los canales asociados.

### Impulso de las prácticas recomendadas

* **Sea específico**: Proporcione detalles claros sobre el tipo de contenido, el tono, la audiencia de destino y los mensajes clave.
* **Especificar canal**: indique claramente para qué canal está creando contenido (correo electrónico, push, SMS).
* **Definir tono**: especifique el tono deseado (cordial, formal, informal, urgente).
* **Iterar y refinar**: use la acción de regeneración para refinar el contenido hasta que cumpla con sus requisitos.

## Análisis de recorrido {#journey-analyze}

Las habilidades de recorrido permitirán a los usuarios de Journey Optimizer analizar y optimizar los recorridos mediante una interfaz de lenguaje natural. Con las habilidades de Recorrido, los profesionales pueden identificar y resolver rápidamente conflictos de programación o audiencia, detectar puntos de abandono de usuarios en un recorrido y proporcionar perspectivas o recomendaciones. Permite a los profesionales tomar decisiones basadas en datos, mejorar la participación de los clientes y optimizar la organización de recorridos.

>[!AVAILABILITY]
>
>Las habilidades de recorrido están disponibles para todos los clientes que tienen acceso a Coworker. Sin embargo, necesitará los siguientes permisos para utilizar completamente las funciones de Aptitudes de Recorrido:
>
>**Ver Recorridos**: Este permiso le permite ver información sobre el recorrido directamente en Compañero de trabajo.
>
>**Administrar Recorridos**: este permiso le permite crear nuevos recorridos directamente en Compañero de trabajo.
>
>**Ver segmentos**: Este permiso le permite ver información de las audiencias directamente en Compañero de trabajo.
>
>**Administrar segmentos**: Este permiso le permite crear nuevas audiencias directamente en Compañero de trabajo.

### Casos de uso clave

El análisis de recorrido ofrece una serie de funcionalidades que se pueden aprovechar para optimizar los esfuerzos de marketing:

* **Análisis del abandono del recorrido**

  * Identifique dónde y por qué abandonan los clientes durante un recorrido.
  * Detecte patrones de comportamiento del cliente que conducen a la desvinculación.
  * Utilice la información para perfeccionar el diseño del recorrido y mejorar la retención.

  Ejemplos de mensajes:
  * &quot;Quiero analizar las visitas en el orden previsto por nodo para la campaña del 4 de julio de recorrido&quot;.
  * &quot;Realizar un análisis de abandonos para la campaña del 4 de julio de recorrido&quot;.
  * &quot;¿Qué es la pérdida de perfil en el transcurso de la campaña del 4 de julio de recorrido?&quot;
  * &quot;Mostrar dónde caen los usuarios en la campaña del 4 de julio de recorrido&quot;.

* **Análisis de solapamiento de público en los recorridos**

  * Analice el solapamiento de público en múltiples recorridos.
  * Evite la fatiga del público causada por una segmentación excesiva.
  * Optimice la segmentación para garantizar una participación equilibrada.

  Ejemplos de mensajes:
  * &quot;¿Qué audiencias se utilizan en más de X recorridos?&quot;
  * &quot;Enumerar todos los recorridos con la audiencia [audience name]&quot;.
  * &quot;Mostrarme conflictos de superposición de audiencias para el recorrido [Nombre del Recorrido]&quot;.
  * &quot;Mostrar audiencias superpuestas para el recorrido [Nombre del Recorrido] y otros recorridos&quot;.

* **Análisis del solapamiento de la programación en los recorridos**

  * Detecte conflictos de horarios entre recorridos programados dirigidos al mismo público.
  * Evite el exceso de comunicación y mejore la eficacia de la programación.
  * Maximice el impacto en el público asegurándose de que los viajes se realizan en los momentos óptimos.

  Ejemplos de mensajes:
  * &quot;¿Hay algún conflicto de programación para el recorrido [Nombre de Recorrido]?&quot;
  * &quot;Compruebe si hay conflictos de programación que impliquen el recorrido [Nombre de Recorrido].&quot;
  * &quot;Resaltar las superposiciones de programación entre el recorrido [Nombre del Recorrido] y los recorridos activos.&quot;
  * &quot;¿El recorrido [Nombre de Recorrido] está en conflicto con algún otro recorrido?&quot;

* **Datos operativos**

  * Perspectivas de Recorrido basadas en mensajes - Perspectivas operativas de la superficie sobre recorridos , es decir, &quot;muéstreme todos los recorridos en directo&quot;.

  Ejemplos de mensajes:
  * &quot;¿Cuándo se publicó [Nombre de Recorrido]?&quot;
  * &quot;¿Cuándo se detuvo [Nombre de Recorrido]?&quot;
  * &quot;Enumerar todos los recorridos que están actualmente en modo de prueba&quot;
  * &quot;¿Cuántos recorridos de vida tengo?&quot;
  * &quot;Dame una lista de todos los recorridos recurrentes programados y sus tiempos de ejecución esperados&quot;.

* **Análisis de errores de acción personalizada de Recorrido**

  * Identifique cuándo las acciones personalizadas dan error o las tasas de error se disparan dentro de un recorrido.
  * Diagnostique las causas raíz antes de que los errores se propaguen en cascada hasta una interrupción del recorrido más amplia.
  * Utilice pasos de corrección específicos para restaurar rápidamente la fiabilidad de las acciones personalizadas.

  Ejemplos de mensajes:
  * &quot;¿Por qué las acciones personalizadas fallan en el recorrido [Nombre de Recorrido]?&quot;
  * &quot;¿Cuál es la tasa de error para la acción personalizada [Nombre de acción personalizada] en el recorrido [Nombre de Recorrido]?&quot;
  * &quot;Mostrarme la causa raíz de los errores de acciones personalizadas en el recorrido [Nombre de Recorrido]&quot;.
  * &quot;¿Hay algún error de acción personalizada que afecte al recorrido [Nombre de Recorrido] en este momento?&quot;

* **Analizar anomalías de Recorrido**

  * Detectar picos, caídas o líneas planas inesperados en los recuentos de entrada, salida o envío de mensajes de un recorrido en comparación con las líneas de base históricas, incluso cuando la pregunta se formula en torno al número de perfiles que entran, salen o completan el recorrido.
  * Confirme si un cambio marcado es una anomalía genuina mediante una comprobación estadística determinista, en lugar de depender únicamente del indicador de anomalía sin procesar.
  * Ejecute diagnósticos limitados de solo lectura con datos de ejecución de recorrido para identificar una causa raíz probable, mostrando lo que cada comprobación buscó y encontró junto con la recomendación.
  * Investigue las alertas de anomalías que hagan referencia a una versión de recorrido y una marca de tiempo específicas.

  Ejemplos de mensajes:
  * &quot;¿Por qué se cayeron las entradas para mi recorrido de bienvenida de ayer?&quot;
  * &quot;¿Aumentaron las salidas del recorrido de abandono del carro de compras esta semana?&quot;
  * &quot;Los envíos parecen bajos para el recorrido de recordatorio de renovación de hoy, ¿qué ha pasado?&quot;
  * &quot;¿Por qué ha habido una caída repentina en el número de perfiles que han entrado en mi recorrido de agradecimiento de aniversario de miembro en los últimos 30 días?&quot;
  * &quot;Menos perfiles de los habituales completan este mes mi recorrido de recordatorio de renovación, ¿por qué?&quot;
  * &quot;Se activó una alerta de anomalía para el recorrido [Id. de versión de Recorrido] a las [marcas de tiempo] — investigar&quot;.

* **Comparación de versiones de Recorrido**

  * Compare dos versiones cualquiera del recorrido en el Chat de Coworker.
  * Revise una comparación estructurada de nodos añadidos, eliminados, modificados y movidos con detalles de nivel de campo.
  * Identifique las conexiones cambiadas, los cambios de propiedades en el nivel de recorrido y los recuentos resumidos sin abrir Journey Optimizer.

  >[!NOTE]
  >
  >Actualmente no se admite la comparación a nivel de actividad de acción para contenido de canal. Los cambios en el contenido del canal se marcan como **No verificado** hasta que esta funcionalidad esté disponible.

  Para obtener más información sobre cómo administrar las versiones de recorrido, consulte [Versiones de Recorrido](publish-journey.md#journey-versions).

  Ejemplos de mensajes:
  * &quot;Comparar versiones [Versión A] y [Versión B] del recorrido [Nombre del Recorrido].&quot;
  * &quot;¿Qué ha cambiado entre estas dos versiones del recorrido [Nombre del Recorrido]?&quot;
  * &quot;Mostrarme los nodos y las propiedades de recorrido que cambiaron entre las versiones [Versión A] y [Versión B]&quot;.

### Impulso de las prácticas recomendadas

Para maximizar la eficacia del análisis de Recorrido, siga estas prácticas recomendadas:

* **Sea específico**: utilice preguntas claras y concisas para obtener información específica. Por ejemplo, en lugar de preguntar &quot;¿Cuáles son mis recorridos?&quot;, especifique &quot;Enumerar todos los recorridos creados en el último mes&quot;.
* **Combinar información**: integre información de las capacidades de Audience y Data Insights para obtener una vista integral del rendimiento del recorrido.
* **Perfeccionamiento iterativo**: utilice el análisis de abandonos y solapamientos para perfeccionar de forma iterativa el diseño y la programación de los recorridos.

### Prácticas recomendadas de configuración

* **Defina objetivos claros**: antes de analizar los recorridos, establezca objetivos claros (por ejemplo, mejorar la retención, aumentar las conversiones).
* **Monitorice de forma periódica**: programe revisiones periódicas del rendimiento de los recorridos para identificar las tendencias y las anomalías.
* **Optimice la segmentación**: asegúrese de que la segmentación del público está equilibrada para evitar la fatiga y maximizar la participación.

## Simulación de recorrido {#journey-simulation}

La habilidad de simulación de recorrido incorpora la simulación rápida impulsada por IA en la interfaz de chat, lo que permite a los usuarios validar la lógica de un recorrido en conversación. Con Coworker, los usuarios pueden generar datos de prueba simulados, ejecutar y administrar una simulación y revisar los resultados.

### Casos de uso clave

1. **Generar datos de prueba simulados**

   * Genere el mínimo de usuarios simulados necesarios para ejercer las ramas del recorrido.
   * Generar datos de evento para recorridos activados por eventos, de modo que se active cada rama.

1. **Ejecutar y administrar simulaciones**

   * Inicie una ejecución de simulación.
   * Restablecer una ejecución de simulación.
   * Compruebe el estado de una ejecución de simulación.
   * Enumeración de los usuarios simulados incluidos en una ejecución.
   * Recuperar registros de ejecución.

1. **Revisar resultados de simulación**

   * Devolver resultados detallados, incluido el recorrido de ruta paso a paso.
   * Devolver resultados de rama para la ejecución simulada.

### Limitaciones

Actualmente, esta función solo admite el flujo de simulación rápida y no reemplaza completamente la experiencia de simulación manual de Journey Optimizer.

Utilice la simulación rápida para realizar una comprobación de sanidad rápida y automatizada de la lógica de un recorrido. Para tener un control granular sobre los usuarios y escenarios simulados, usa la [experiencia de simulación manual en Journey Optimizer](simulate-journey-gs.md).

Como parte de esta experiencia de simulación rápida, los usuarios no pueden:

* Elija un usuario simulado guardado existente para una ejecución.
* Edite un usuario simulado antes de volver a ejecutar una simulación.
* Cree, examine, actualice o elimine usuarios simulados persistentes a través del chat.
* Oriente una ruta específica o un caso de prueba personalizado.


{{$include /help/_includes/do-not-localize/start/ai-augmented-journeys-coworker-skills.md}}
