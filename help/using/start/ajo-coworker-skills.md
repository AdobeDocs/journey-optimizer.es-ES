---
solution: Journey Optimizer
product: journey optimizer
title: Aptitudes de Journey Optimizer en CX Coworker
description: Descubra las habilidades de Adobe Journey Optimizer disponibles en CX Coworker, con instrucciones detalladas y ejemplos de preguntas.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 2
source-git-commit: 46c661740f8a42bcc72c9064e5512b02b1921d71
workflow-type: tm+mt
source-wordcount: '3996'
ht-degree: 6%

---


# Aptitudes de Journey Optimizer en CX Coworker {#ajo-coworker-skills}

>[!BEGINSHADEBOX]

**En esta página:** Descubra las habilidades de Adobe Journey Optimizer disponibles en CX Coworker, desde la creación y el análisis de recorridos hasta la generación de contenido de canal y la administración de recursos de contenido, con instrucciones detalladas, mensajes de ejemplo y prácticas recomendadas para cada habilidad.

>[!ENDSHADEBOX]

## Información general {#overview}

CX Coworker incorpora funciones con tecnología de IA a Adobe Journey Optimizer. [CX Coworker](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home){target="_blank"} es la experiencia de conversación de Adobe que se integra con las aplicaciones de tu empresa para ayudarte a trabajar de manera más eficiente.

Gracias a sus conocimientos con tecnología de IA, CX Coworker permite a los usuarios de Journey Optimizer crear, analizar y optimizar recorridos de marketing mediante una interfaz de lenguaje natural. Con las habilidades de Recorrido, los profesionales pueden crear recorridos rápidamente, detectar y resolver conflictos de programación o audiencia, analizar el rendimiento y los puntos de entrega e identificar recorridos de alto rendimiento para replicarlos en campañas futuras. Permite a los profesionales tomar decisiones basadas en datos, mejorar la participación de los clientes y optimizar la organización de recorridos.

CX Coworker ofrece varias habilidades para gestionar Recorridos y desafíos de fidelidad:

**aptitudes centradas en el Recorrido:**

* **Creación de Recorrido**: cree y configure recorridos de marketing mediante mensajes en lenguaje natural
* **Creación de contenido de canal**: genera, edita y administra contenido específico del canal (correo electrónico, push, SMS) para recorridos mediante la generación de contenido con tecnología de IA
* **Análisis de Recorrido**: Analice recorridos, detecte problemas, descubra información y optimice el rendimiento del recorrido

**Aptitudes centradas en la fidelización:**

* **Administración de retos de fidelidad**: cree y administre desafíos de fidelidad mediante mensajes en lenguaje natural
* **Agente de fidelización - Habilidad de Data Insight**: consulte y analice los datos de rendimiento del programa de fidelización utilizando lenguaje natural

CX Coworker también incluye un conjunto de **herramientas MCP de administración de contenido** para detectar, crear y administrar plantillas de contenido de Journey Optimizer, fragmentos, páginas de aterrizaje y contenido de mensajes en línea de recorrido/campaña. [Más información](#content-management)

<!--
feedback from Ivan: Need to remove Simulate skill from docs until Nico confirms the release timeline.

In addition, **Journey Simulation** is a Journey Optimizer feature that includes [Journey Simulate](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs), an in-product agentic skill, non conversational, with three capabilities: 

* Generating simulated users
* Generating event values
* Quick simulation
-->

## aptitudes de recorrido {#journey-skills}

### Crear recorrido {#journey-create}

Recorrido Crear permite a los usuarios de Journey Optimizer crear y configurar recorridos de marketing mediante una interfaz de lenguaje natural. Con Recorrido Crear, los profesionales pueden crear recorridos rápidamente al describir sus necesidades en mensajes de conversación. La aptitud guía a los usuarios por las diferentes opciones para crear un recorrido, lo que permite a los especialistas en marketing centrarse en la estrategia en lugar de en la configuración técnica.

>[!AVAILABILITY]
>
>Necesita los siguientes permisos para utilizar completamente las funciones de creación de Recorrido:
>
>**Administrar Recorridos**: este permiso le permite crear nuevos recorridos directamente en CX Coworker.
>
>**Ver eventos, fuentes de datos y acciones de Recorrido**: este permiso garantiza que CX Coworker pueda buscar a través de eventos de Recorrido y acciones personalizadas.
>
>**Ver segmentos**: Este permiso garantiza que CX Coworker pueda buscar segmentos de audiencia al crear un Recorrido.
>
>**Administrar segmentos**: Este permiso le permite crear nuevas audiencias directamente en CX Coworker.

#### Casos de uso clave

Recorrido Cree ofertas que se puedan aprovechar para acelerar la ejecución del marketing:

1. **Creación de recorrido desencadenada por eventos**

   * Cree recorridos que se activen en función de eventos de clientes específicos.
   * Diseñar respuestas automatizadas a acciones de clientes en tiempo real.
   * Cree flujos de comunicación personalizados basados en el comportamiento de los clientes.

   **recorrido de visitas a tiendas:**
   &quot;Crear un recorrido que se inicie cuando un usuario entre en mi ubicación de tienda. Envíe una notificación push para dar la bienvenida a los usuarios a la tienda. Espere 2 días y compruebe si el usuario tiene una dirección de correo electrónico válida. Si el usuario tiene una dirección de correo electrónico válida, envíe un sondeo por correo electrónico para preguntar por su experiencia en la tienda. Si el usuario no tiene una dirección de correo electrónico válida, envíe una notificación push para solicitar el registro&quot;.

   **recorridos posteriores a la compra:**
   &quot;Cree un recorrido que se inicie cuando un cliente realice una compra en línea. Envíe una notificación push para agradecerles su compra. A continuación, compruebe si son miembros socio. Si el usuario es un abonado de las recompensas por fidelidad, envíe una segunda notificación push con un código de descuento del 10 %. Si el usuario no es un miembro de las recompensas por fidelidad, envía una notificación push invitándolo a registrarse en el programa de fidelidad. Espere 2 días y envíe una notificación push de seguimiento con una encuesta sobre su experiencia de compra&quot;.

   **Promoción basada en eventos:**
   &quot;Crea un recorrido cuando la puntuación del juego alcance 50. Envíe un mensaje SMS a los miembros de la recompensa de fidelidad diciendo que cumplen los requisitos para una porción gratuita de pizza del patrocinador del socio&quot;.

1. **Creación de recorrido con destino de audiencia**

   * Genere recorridos dirigidos a segmentos de audiencia específicos.
   * Diseñe secuencias de comunicación de varios pasos con sincronización estratégica.

   **Campaña estacional:**
   &quot;Quiero crear un recorrido dirigido a una audiencia de excursionistas. Quiero enviar un correo electrónico alertando a esta audiencia sobre mi próxima venta de vacaciones que incluye una variedad de elementos esenciales para el senderismo. Espere 3 días después de enviar el primer correo electrónico y envíe un segundo correo electrónico que tenga un cupón del 15% con envío gratuito. Espere 1 semana y luego envíe un tercer mensaje de correo electrónico para mostrar nuestro nuevo saco de dormir y la colección de la tienda. Programe el recorrido para que comience el 20/12&quot;.

   **Agradecimiento por la fidelidad:**
   &quot;Cree un recorrido de apreciación de la lealtad para los propietarios de SUV, que incluya una notificación push de agradecimiento con una oferta de lavado de coches gratis y un recordatorio de notificación push de seguimiento si no se interactúa con la primera notificación en el plazo de 1 día&quot;.

1. **Creación de recorrido desencadenada por evento empresarial**

   * Cree recorridos que se activen en función de un evento empresarial determinado y se dirijan a una audiencia específica (por ejemplo, producto disponible o cambio de puntuación de juego)
   * Déclencheur mensajes oportunos y según el contexto cuando cambian las condiciones empresariales.

1. **Creación del recorrido de calificación de audiencia**

   * Cree recorridos que se activen cuando los perfiles entran o salen de una definición de segmento de audiencia.
   * Automatice la mensajería de entrada y salida para lograr los objetivos de incorporación, retención y recuperación.

1. **Flujos de recorrido condicionales**

   * Cree ramas de decisión basadas en atributos del cliente.
   * Diseñe rutas divididas que se adapten a las preferencias de los clientes.

1. **Crear recorrido a partir de la imagen**

   * Cargue una imagen de referencia en su compañero de trabajo y pida crear un recorrido con la imagen como referencia
   * La aptitud para crear recorridos extraerá un mensaje editable de la imagen de referencia

Con esta aptitud, los requisitos del lenguaje natural se traducen en configuraciones de recorrido estructuradas.

#### Aptitudes en el ámbito

Recorrido Crear admite las siguientes funciones:

* **Creación de recorridos en lenguaje natural**: permite a los usuarios describir el flujo de recorrido en lenguaje conversacional.
* **recorridos basados en eventos y en audiencias**: admite tipos de recorridos programados y basados en déclencheur, así como eventos comerciales y calificación de audiencias.
* **Lógica condicional**: administra las divisiones y ramas de decisión en función de los atributos del cliente.
* **Mensajería multicanal**: Admite notificaciones push, correo electrónico y canales SMS.
* **Programación de Recorridos**: Configura las fechas de inicio y el horario de los recorridos programados.

#### Aptitudes fuera del ámbito

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

#### Impulso de las prácticas recomendadas

Para maximizar la eficacia de Creación de Recorridos, siga estas prácticas recomendadas:

1. **Sea específico**: Proporcione detalles claros sobre sus objetivos de recorrido, audiencia de destinatario y acciones deseadas. Incluya información sobre canales, temporización y condiciones.
1. **Especificar tiempo**: indique claramente los períodos de espera entre las acciones y cuándo debe iniciarse el recorrido.
1. **Definir condiciones**: cuando use la lógica condicional, explique los criterios para cada ruta de bifurcación.
1. **Incluir canales**: especifique qué canales de comunicación desea utilizar (push, correo electrónico, SMS).
1. **Programación de menciones**: para los recorridos programados, proporcione la fecha y la hora de inicio que desee.
1. **Acciones personalizadas**: si usa acciones personalizadas en el flujo de trabajo, debe especificar que usa una acción personalizada junto con el nombre exacto de la acción personalizada. Por ejemplo:
Cuando un usuario entre en mi ubicación de tienda, enviar un mensaje de bienvenida mediante la acción personalizada ExternalPush. Espere 2 días y, a continuación, envíe un mensaje de seguimiento mediante una acción personalizada por correo electrónico externo con una encuesta sobre su visita.
1. **Validar expresiones**: asegúrese de comprobar y validar cualquier expresión que las aptitudes de Recorrido creen para asegurarse de que se utilizan los campos y valores correctos.

#### Prácticas recomendadas de configuración

* **Definir objetivos claros**: antes de crear recorridos, establezca objetivos claros (mejorar la retención, impulsar las conversiones y aumentar la participación).
* **Preparar audiencias**: Asegúrese de que las audiencias de destino ya se hayan creado y segmentado correctamente.
* **Planificar contenido del mensaje**: Defina su estrategia de mensajería antes de crear el recorrido.
* **Tenga en cuenta la experiencia del cliente**: Diseñe flujos de recorrido que respeten las preferencias del cliente y eviten la comunicación excesiva.

### Creación de contenido de canal {#channel-content-create}

<!--Ivan : Need to speak with Amar on new options for content generation as this skill has changed. -->

>[!AVAILABILITY]
>
>Esta función está disponible para todos los clientes con disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

La creación de contenido de canal permite a los usuarios de Journey Optimizer generar, editar y administrar contenido específico del canal para recorridos mediante la generación de contenido con tecnología de IA.

#### Casos de uso clave

1. **Generación de contenido específico del canal**: genere contenido para correo electrónico, notificaciones push, SMS y otros canales mediante mensajes en lenguaje natural.

   &quot;Generar contenido de correo electrónico para mi recorrido de bienvenida. Cree un correo electrónico de bienvenida para nuevos clientes con un tono cordial e incluya una oferta de descuento del 10 %&quot;.

   &quot;Generar una notificación push para el recorrido de mi visita a la tienda. Cree un mensaje de bienvenida que anime a los clientes a registrarse y recibir una oferta especial&quot;.

   &quot;Generar contenido SMS para mi recorrido activado por eventos. Cree un mensaje corto para notificar a los clientes sobre una venta flash con un call-to-action&quot;.

1. **Creación de contenido basado en plantillas**: busca y selecciona entre las plantillas disponibles con capacidades de vista previa.

   &quot;Mostrarme las plantillas de correo electrónico disponibles para mi recorrido de campaña de temporada&quot;.

   &quot;Seleccione una plantilla para mi correo electrónico que tenga un diseño moderno y limpio.&quot;

1. **Administración de contenido multicanal**: genera y administra contenido para varios canales dentro del mismo flujo de trabajo de recorrido.

1. **Edición de contenido en contexto**: abra el contenido generado en Content Designer para editarlo y refinarlo.

   &quot;Abra el contenido del correo electrónico en Content Designer para poder personalizar el diseño&quot;.

1. **Refinamiento e iteración del contenido**: Regenera el contenido con diferentes tonos o estilos mediante la acción Regenerar.

   &quot;Regenerar el contenido de las notificaciones push con un tono más informal&quot;.

   &quot;Actualice el contenido del correo electrónico para incluir un código promocional.&quot;

1. **Integración de lienzo de Recorrido**: seleccione recorridos del inventario y vea los canales asociados.

#### Aptitudes en el ámbito

Las siguientes funciones son compatibles con la creación de contenido de canal:

* **Generación de contenido con tecnología de IA**: genera contenido para correo electrónico, push, SMS y otros canales mediante mensajes en lenguaje natural.
* **Administración de plantillas**: busca y selecciona entre las plantillas disponibles con capacidades de vista previa.
* **Edición en contexto**: abra el contenido generado en Content Designer para editarlo y refinarlo.
* **Regeneración de contenido**: Regenera el contenido con diferentes tonos, estilos o mensajes mediante la acción Regenerar.
* **Compatibilidad con varios canales**: genere y administre contenido para varios canales dentro del mismo flujo de trabajo de recorrido.
* **acceso al inventario de Recorridos**: seleccione recorridos del inventario y vea los canales asociados.

#### Aptitudes fuera del ámbito

Actualmente no se admiten las siguientes funcionalidades:

* **Alineación de marca y comprobaciones de calidad del contenido**
* **Insertar nodos de contenido directamente en el lienzo de recorrido**
* **Importación de plantilla**

#### Impulso de las prácticas recomendadas

1. **Sea específico**: Proporcione detalles claros sobre el tipo de contenido, el tono, la audiencia de destino y los mensajes clave.
1. **Especificar canal**: indique claramente para qué canal está creando contenido (correo electrónico, push, SMS).
1. **Definir tono**: especifique el tono deseado (cordial, formal, informal, urgente).
1. **Iterar y refinar**: use la acción de regeneración para refinar el contenido hasta que cumpla con sus requisitos.

### Análisis de recorrido {#journey-analyze}

Las habilidades de recorrido permitirán a los usuarios de Journey Optimizer analizar y optimizar los recorridos mediante una interfaz de lenguaje natural. Con las habilidades de Recorrido, los profesionales pueden identificar y resolver rápidamente conflictos de programación o audiencia, detectar puntos de abandono de usuarios en un recorrido y proporcionar perspectivas o recomendaciones. Permite a los profesionales tomar decisiones basadas en datos, mejorar la participación de los clientes y optimizar la organización de recorridos.

>[!AVAILABILITY]
>
>Las habilidades de recorrido están disponibles para todos los clientes que tienen acceso a CX Coworker. Sin embargo, necesitará los siguientes permisos para utilizar completamente las funciones de Aptitudes de Recorrido:
>
>**Ver Recorridos**: Este permiso le permite ver información sobre el recorrido directamente en CX Coworker.
>
>**Administrar Recorridos**: este permiso le permite crear nuevos recorridos directamente en CX Coworker.
>
>**Ver segmentos**: Este permiso le permite ver información de las audiencias directamente en CX Coworker.
>
>**Administrar segmentos**: Este permiso le permite crear nuevas audiencias directamente en CX Coworker.

#### Casos de uso clave

El análisis de recorrido ofrece una serie de funcionalidades que se pueden aprovechar para optimizar los esfuerzos de marketing:

1. **Análisis del abandono del recorrido**

   * Identifique dónde y por qué abandonan los clientes durante un recorrido.
   * Detecte patrones de comportamiento del cliente que conducen a la desvinculación.
   * Utilice la información para perfeccionar el diseño del recorrido y mejorar la retención.

   Ejemplos de mensajes:
   * &quot;Quiero analizar las visitas en el orden previsto por nodo para la campaña del 4 de julio de recorrido&quot;.
   * &quot;Realizar un análisis de abandonos para la campaña del 4 de julio de recorrido&quot;.
   * &quot;¿Qué es la pérdida de perfil en el transcurso de la campaña del 4 de julio de recorrido?&quot;
   * &quot;Mostrar dónde caen los usuarios en la campaña del 4 de julio de recorrido&quot;.

1. **Análisis de solapamiento de público en los recorridos**

   * Analice el solapamiento de público en múltiples recorridos.
   * Evite la fatiga del público causada por una segmentación excesiva.
   * Optimice la segmentación para garantizar una participación equilibrada.

   Ejemplos de mensajes:
   * &quot;¿Qué audiencias se utilizan en más de X recorridos?&quot;
   * &quot;Enumerar todos los recorridos con la audiencia [audience name]&quot;.
   * &quot;Mostrarme conflictos de superposición de audiencias para el recorrido [Nombre del Recorrido]&quot;.
   * &quot;Mostrar audiencias superpuestas para el recorrido [Nombre del Recorrido] y otros recorridos&quot;.

1. **Análisis del solapamiento de la programación en los recorridos**

   * Detecte conflictos de horarios entre recorridos programados dirigidos al mismo público.
   * Evite el exceso de comunicación y mejore la eficacia de la programación.
   * Maximice el impacto en el público asegurándose de que los viajes se realizan en los momentos óptimos.

   Ejemplos de mensajes:
   * &quot;¿Hay algún conflicto de programación para el recorrido [Nombre de Recorrido]?&quot;
   * &quot;Compruebe si hay conflictos de programación que impliquen el recorrido [Nombre de Recorrido].&quot;
   * &quot;Resaltar las superposiciones de programación entre el recorrido [Nombre del Recorrido] y los recorridos activos.&quot;
   * &quot;¿El recorrido [Nombre de Recorrido] está en conflicto con algún otro recorrido?&quot;

1. **Datos operativos**

   * Perspectivas de Recorrido basadas en mensajes - Perspectivas operativas de la superficie sobre recorridos , es decir, &quot;muéstreme todos los recorridos en directo&quot;.

   Ejemplos de mensajes:
   * &quot;¿Cuándo se publicó [Nombre de Recorrido]?&quot;
   * &quot;¿Cuándo se detuvo [Nombre de Recorrido]?&quot;
   * &quot;Enumerar todos los recorridos que están actualmente en modo de prueba&quot;
   * &quot;¿Cuántos recorridos de vida tengo?&quot;
   * &quot;Dame una lista de todos los recorridos recurrentes programados y sus tiempos de ejecución esperados&quot;.

1. **Análisis de errores de acción personalizada de Recorrido**

   * Identifique cuándo las acciones personalizadas dan error o las tasas de error se disparan dentro de un recorrido.
   * Diagnostique las causas raíz antes de que los errores se propaguen en cascada hasta una interrupción del recorrido más amplia.
   * Utilice pasos de corrección específicos para restaurar rápidamente la fiabilidad de las acciones personalizadas.

   Ejemplos de mensajes:
   * &quot;¿Por qué las acciones personalizadas fallan en el recorrido [Nombre de Recorrido]?&quot;
   * &quot;¿Cuál es la tasa de error para la acción personalizada [Nombre de acción personalizada] en el recorrido [Nombre de Recorrido]?&quot;
   * &quot;Mostrarme la causa raíz de los errores de acciones personalizadas en el recorrido [Nombre de Recorrido]&quot;.
   * &quot;¿Hay algún error de acción personalizada que afecte al recorrido [Nombre de Recorrido] en este momento?&quot;

#### Aptitudes en el ámbito

El análisis de Recorrido admite las siguientes funciones:

* **Consultas reactivas**: permite a los usuarios hacer preguntas específicas sobre el rendimiento del recorrido, el uso del público y los conflictos de programación.
* **Integración con otras habilidades**: colabora con las capacidades de Audience y Data Insights para realizar un análisis más profundo.
* **Estructura de la respuesta**: razonamiento (explicar la lógica), resumen del análisis (resaltar puntos clave), detalles del problema (describir el problema) y recomendación (proponer pasos siguientes).
* **Análisis de errores de acciones personalizadas**: Detecte y diagnostique errores de acciones personalizadas y picos de error dentro de un recorrido.

#### Aptitudes fuera del ámbito

Actualmente no se admiten las siguientes funcionalidades:

* **Creación automática de recorridos**
* **Detección de anomalías en tiempo real**
* **Los canales se solapan**
* **Análisis de entrada del recorrido**
* **Análisis de problemas técnicos**
* **Análisis de fatiga**

#### Impulso de las prácticas recomendadas

Para maximizar la eficacia del análisis de Recorrido, siga estas prácticas recomendadas:

1. **Sea específico**: utilice preguntas claras y concisas para obtener información específica. Por ejemplo, en lugar de preguntar &quot;¿Cuáles son mis recorridos?&quot;, especifique &quot;Enumerar todos los recorridos creados en el último mes&quot;.
1. **Combinar información**: integre información de las capacidades de Audience y Data Insights para obtener una vista integral del rendimiento del recorrido.
1. **Perfeccionamiento iterativo**: utilice el análisis de abandonos y solapamientos para perfeccionar de forma iterativa el diseño y la programación de los recorridos.

#### Prácticas recomendadas de configuración

* **Defina objetivos claros**: antes de analizar los recorridos, establezca objetivos claros (por ejemplo, mejorar la retención, aumentar las conversiones).
* **Monitorice de forma periódica**: programe revisiones periódicas del rendimiento de los recorridos para identificar las tendencias y las anomalías.
* **Optimice la segmentación**: asegúrese de que la segmentación del público está equilibrada para evitar la fatiga y maximizar la participación.

## Aptitudes de fidelización {#loyalty-skills}

>[!AVAILABILITY]
>
>Las habilidades de fidelización están disponibles en CX Coworker para las organizaciones elegibles. Los clientes con una licencia de fidelidad pueden acceder a estas habilidades de fidelidad, incluso si no tienen una licencia adicional de colaborador de CX.

Las habilidades de lealtad permiten a los administradores y analistas de lealtad crear, administrar y analizar programas de lealtad mediante el lenguaje natural. Con estas habilidades impulsadas por IA, puede diseñar rápidamente desafíos de lealtad atractivos, rastrear métricas de rendimiento y tomar decisiones basadas en datos para optimizar la participación de los miembros y la rentabilidad del programa. Tanto si desea crear un nuevo desafío como si desea analizar las tendencias del programa de fidelización, las habilidades de fidelización optimizan todo el flujo de trabajo de gestión de la fidelidad.

### Administración de desafío de fidelización {#loyalty-challenge-management}

La administración de retos de fidelidad permite a los usuarios de Journey Optimizer crear y gestionar retos de fidelidad en CX Coworker utilizando indicaciones en lenguaje natural. Para obtener documentación completa sobre cómo crear, configurar y administrar desafíos de lealtad, incluidas instrucciones de configuración detalladas, consulte la [guía de Desafíos de lealtad](../loyalty-challenges/get-started.md).

#### Casos de uso clave

1. **Desafío de incorporación de varios pasos**

   &quot;Cree un desafío llamado &quot;KickStart de cuenta nueva&quot; para los clientes recién inscritos que les exija completar estos pasos en orden: abra una cuenta corriente, encuéntrela con al menos 500 dólares y descargue la aplicación móvil. Cuando se hayan realizado todos los pasos, recompénselos con 5000 puntos de bonificación. Ejecútelo desde el 1 de septiembre hasta el 31 de octubre, zona horaria del este&quot;.

1. **Desafío del umbral de actividad acumulativa**

   &quot;Cree un desafío llamado &quot;Pasar y ganar verano&quot; para los titulares de tarjetas en el que los miembros ganan un crédito de estado de cuenta de 50 dólares una vez que gastan 1.500 dólares en su tarjeta de crédito durante el tercer trimestre. Comience el 1 de julio, zona horaria del este&quot;.

1. **Desafío de racha de frecuencia**

   &quot;Cree un desafío llamado &quot;Frequent Flyer Sprint&quot; para miembros de nivel elite que requiere 3 vuelos al mes durante dos meses consecutivos. Recompense la finalización con una extensión de estado de nivel y 10.000 millas de bonificación. Empieza el primero del mes que viene, zona horaria del Pacífico&quot;.

1. **Desafío de acción de calificación único**

   &quot;Configure un desafío llamado &quot;Go Paperless&quot; que recompensa a los suscriptores pospago con 500 puntos de bonificación después de que se inscriban en pago automático y cambien a la facturación electrónica dentro de los 30 días. Comience el primero del mes que viene, zona horaria central&quot;.

1. **Desafío de objetivo de participación/consumo**

   &quot;Crea un desafío llamado &quot;Distintivo del explorador&quot; para los miembros que les exige completar 5 actividades en al menos 3 categorías diferentes durante el mes de agosto. Recompénsalos con 1.000 puntos y una insignia &quot;Explorer&quot; al finalizar. Comienza el 1 de agosto, zona horaria de la montaña&quot;.

1. **Desafío de acción diaria**

   &quot;Ayúdame a crear un desafío para los amantes del matcha que requiere que vengan a la tienda todos los días esta semana y compren una bebida de matcha. Su recompensa debería ser de 200 puntos extra si completan el desafío. Llámalo &quot;Loco por Matcha&quot;, usa SKU matcha-001, empieza el lunes de la semana que viene, zona horaria del este&quot;.

#### Aptitudes en el ámbito

La administración de retos de fidelización admite las siguientes funciones:

* **Creación de desafío**: cree una configuración de desafío a partir del lenguaje natural (audiencia, criterios de acción, tiempo, recompensa, nombre).
* **Actualizaciones de desafío**: modifique los detalles del desafío mediante mensajes iterativos.
* **Publicación de desafío**: publique las configuraciones de desafío admitidas directamente desde la conversación.
* **Visibilidad del contexto del desafío**: recupere y revise la información del desafío mientras realiza la iteración.

#### Aptitudes fuera del ámbito

Actualmente no se admiten las siguientes funcionalidades:

* Desafío de eliminación
* Perspectivas de fidelización y habilidades de recomendaciones
* Automatización completa de la creación de contenido para la mensajería de desafío en todos los casos

#### Impulso de las prácticas recomendadas

1. **Asígnele un nombre**: escriba un título claro y fácil de recordar entre comillas.
1. **Especifique la audiencia**: quién califica (por ejemplo, todos los miembros, un nivel, un segmento, nuevos inscritos, titulares de tarjeta y suscriptores).
1. **Defina la acción y cuánto**: Qué deben hacer los miembros, y la frecuencia, umbral o secuencia que cuenta como finalización.
1. **Establecer la ventana de tiempo**: Una fecha de inicio (y de finalización si es de duración fija) más la zona horaria.
1. **Indica la recompensa**: Puntos, millas, créditos de extractos, extensiones de estado, cupones o beneficios otorgados al finalizar.
1. **Haga referencia al evento correspondiente**: indique el SKU, el producto, la acción de la cuenta o el evento de participación específico que rastrea el desafío.

### Agente de fidelización: Data Insight {#loyalty-data-insight}

Agente de fidelización: la aptitud de Data Insight permite a los usuarios de Journey Optimizer analizar y consultar los datos de rendimiento del programa de fidelidad mediante el lenguaje natural. Esta aptitud proporciona perspectivas sobre puntos de fidelidad, niveles de miembros, reembolsos y métricas de ingresos, lo que permite a los administradores y analistas de fidelidad tomar decisiones basadas en datos sobre sus programas de fidelidad.

Casos de uso clave:

1. **Análisis de puntos de fidelización**

   * Analice los puntos de lealtad concedidos, obtenidos y canjeados en períodos específicos.
   * Compare actividades de puntos de fidelidad en diferentes niveles y programas de fidelidad.
   * Rastree el saldo de puntos de lealtad por segmento de miembro.

   Ejemplos de mensajes:
   * &quot;¿Cuántos puntos de lealtad se concedieron durante agosto de 2026?&quot;
   * &quot;¿Cuántos puntos de lealtad obtuvieron los miembros en cada nivel de lealtad durante agosto de 2026?&quot;
   * &quot;Muéstreme el total de puntos de fidelidad canjeados por el estado de fidelidad del miembro (no el nivel de fidelidad) durante agosto de 2026&quot;.
   * &quot;Mostrar el saldo total de puntos de lealtad desglosado por nivel de lealtad durante agosto de 2026&quot;.

1. **Análisis de ingresos y descuentos**

   * Analice los ingresos de los pedidos y las tendencias de descuento por fidelidad por nivel y programa.
   * Compare la generación de ingresos entre programas de fidelización y períodos de tiempo.
   * Rastree el impacto de los descuentos en los ingresos y la participación de los miembros.

   Ejemplos de mensajes:
   * &quot;¿Cuál fue el ingreso total de pedidos para cada nivel de fidelidad durante agosto de 2026?&quot;
   * &quot;¿Cuánto en descuentos por fidelidad se aplicó a cada nivel de fidelidad durante agosto de 2026?&quot;
   * &quot;Mostrar los descuentos de fidelidad totales desglosados por programa de fidelidad durante agosto de 2026&quot;.
   * &quot;¿Cuál fue el ingreso total de pedidos generado por cada programa de fidelidad durante agosto de 2026?&quot;

1. **Perspectivas de rendimiento del programa**

   * Analizar métricas de rendimiento de programas diarias, semanales y mensuales.
   * Compare el rendimiento en diferentes categorías de productos y estrategias de descuento.
   * Identifique las tendencias en los patrones de participación y canje de miembros.

   Ejemplos de mensajes:
   * &quot;Mostrar los ingresos totales del programa de fidelización desglosados por día durante agosto de 2026&quot;.
   * &quot;Mostrar los descuentos de fidelidad totales desglosados por categoría de producto durante agosto de 2026&quot;.
   * &quot;Mostrarme el informe de rendimiento del programa de fidelización para el tercer trimestre de 2026&quot;.

## Herramientas de administración de contenido {#content-management}

>[!AVAILABILITY]
>
>La administración de contenido está disponible para todos los clientes que tengan acceso a CX Coworker.

<!--However, you will need the following permissions in order to fully use the Content Management features:
**Manage Library Items**: This permission lets you list, retrieve, create, and update content templates and fragments directly in CX Coworker.

**Publish Fragment**: This permission lets you publish fragments directly in CX Coworker.-->

Los usuarios de Journey Optimizer pueden descubrir y gestionar recursos de contenido (plantillas de contenido, fragmentos, páginas de aterrizaje y contenido de mensajes en línea de recorrido/campaña) directamente desde CX Coworker con indicaciones en lenguaje natural. Permite pasar de &quot;hablarme sobre mi contenido&quot; a &quot;compilarlo, actualizarlo y publicarlo&quot;, sin abandonar la conversación. Esta capacidad está equipada con 15 herramientas de MCP con capacidad de lectura y escritura para el contenido de Journey Optimizer.

#### Casos de uso clave

1. **Examinar e inspeccionar contenido**

   * Enumere las plantillas de contenido, los fragmentos o las páginas de aterrizaje disponibles y recupere su estructura, metadatos y estado.
   * Recupere el contenido del mensaje en línea configurado en un nodo de recorrido o de acción de campaña.

   Ejemplos de mensajes:
   * &quot;Enumerar mis plantillas de contenido de correo electrónico&quot;.
   * &quot;Mostrarme los fragmentos disponibles para mi campaña de verano&quot;.
   * &quot;Obtenga los detalles de la página de aterrizaje página-123&quot;.
   * &quot;¿Qué contenido está configurado para la variante de correo electrónico del nodo de acción en campaign camp-789?&quot;

1. **Crear plantillas de contenido**

   * Cree una nueva plantilla de contenido para cualquier canal.

   Ejemplos de mensajes:
   * &quot;Cree una plantilla de correo electrónico denominada Rebajas de verano con este contenido de HTML&quot;.
   * &quot;Cree una nueva plantilla de SMS llamada Alerta Flash&quot;.

1. **Actualizar plantillas de contenido**

   * Reemplazar completamente el contenido de una plantilla existente.

   Ejemplos de mensajes:
   * &quot;Actualice la plantilla abc-123 con este nuevo cuerpo de HTML&quot;.

1. **Crear, actualizar, clonar y publicar fragmentos**

   * Cree un nuevo HTML o fragmento de expresión.
   * Actualizar el contenido o los metadatos de un fragmento existente.
   * Clonar un fragmento existente con un nombre nuevo.
   * Envíe un fragmento de borrador para su publicación.

   Ejemplos de mensajes:
   * &quot;Cree un fragmento de HTML llamado Banner de promoción con este marcado&quot;.
   * &quot;Actualice el fragmento frag-456 para cambiar su nombre a Banner promocional V2.&quot;
   * &quot;Clonar el fragmento abc-123 como titular de la promoción - Verano (Variante B).&quot;
   * &quot;Publicar fragmento frag-456&quot;.

1. **Actualizar contenido de mensaje en línea**

   * Reemplace una variante de canal en el mensaje en línea de un nodo de acción de recorrido o campaña.
   * Enumerar las variantes de canal definidas en un nodo de recorrido o de acción de campaña.

   Ejemplos de mensajes:
   * &quot;Actualice la variante de correo electrónico del nodo de acción en campaign camp-789 con este nuevo contenido&quot;.
   * &quot;¿Qué variantes de canal se definen en este nodo de acción?&quot;

#### En ámbito

La administración de contenido admite las siguientes funciones:

* **Enumerar y obtener plantillas de contenido**: Examine las plantillas de contenido y recupere su estructura y metadatos.
* **Enumerar y obtener fragmentos**: Examine fragmentos de contenido y expresión y recupere sus detalles.
* **Enumerar y obtener páginas de aterrizaje**: Examine páginas de aterrizaje y recupere sus metadatos y contenido de página.
* **Obtener contenido en línea de campaña/recorrido**: recupere el contenido del mensaje en línea configurado en un nodo de acción de campaña o recorrido, incluidas las variantes multilingües.
* **Crear plantillas de contenido**: cree una nueva plantilla para cualquier canal.
* **Actualizar plantillas de contenido**: reemplace completamente el contenido de una plantilla existente.
* **Crear, actualizar, clonar y publicar fragmentos**: cree nuevos fragmentos, actualice los existentes, clone un fragmento con un nuevo nombre y envíe un borrador de fragmento para su publicación.
* **Actualizar contenido de mensajes en línea**: reemplace una variante de canal en el mensaje en línea de un nodo de acción de campaña/recorrido, incluidas las variantes multilingües, y enumere las variantes de canal definidas en un nodo de acción.

#### Fuera de ámbito

Actualmente no se admiten las siguientes funcionalidades:

* **Búsqueda de texto completo en plantillas o fragmentos**
* **Validación de plantilla o fragmento** (referencias huérfanas, vínculos rotos, componentes obsoletos)
* **Creando o publicando páginas de aterrizaje**
* **Eliminando plantillas de contenido, fragmentos o páginas de aterrizaje**

#### Impulso de las prácticas recomendadas

1. **ID de referencia conocidos**: proporcione la plantilla, el fragmento, la página de aterrizaje o el ID de campaña/recorrido cuando solicite obtener, actualizar, clonar o publicar un recurso específico.
1. **Sea explícito sobre el canal**: Al crear una plantilla o un fragmento, especifique el canal o el tipo de contenido (correo electrónico, fragmento de HTML, fragmento de expresión).
1. **Confirmar antes de publicar**: revise el contenido de un fragmento después de crearlo o actualizarlo antes de pedir a su compañero que lo publique.
1. **Proporcionar contenido de reemplazo completo**: las operaciones de actualización reemplazan el contenido por completo, de modo que incluya el cuerpo completo de HTML o el contenido de variante en el mensaje.

<!--
Feedback from Ivan: Journey simulate is not ready as a skill

## Journey Simulate: Use Cases, Agentic Skills and User Guide

## Overview

>[!BEGINSHADEBOX]

Journey Simulation is available to all Journey Optimizer customers. Journey Simulate, the in-product agentic skill within Journey Simulation, is available to customers that are a part of the Agent Orchestrator Explorer program and requires at least one of the following permissions:

* **Simulate journeys**: Run simulation workflows from the journey canvas.

* **Publish journeys**: Publish journeys, including flows that use simulation before go-live.

* **Approve and Publish journeys**: Approve and publish journeys when your organization uses approval workflows.

To use AI in **[!UICONTROL Simulation]** (**[!UICONTROL Quick simulation]**, generating simulated users with AI, **[!UICONTROL Generate event values]**), users require **[!UICONTROL Generate Content]** permission from the **[!UICONTROL AI Assistant]** capability. 

[Learn more about permissions](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/administration/permissions).

>[!ENDSHADEBOX]

Journey Simulation is a Journey Optimizer feature that enables Journey Optimizer users to safely test and validate marketing journeys before activation. Within Journey Simulation, Journey Simulate is an in-product agentic skill, not a conversational one, that automates and assists the testing process directly from the journey canvas.

Journey Simulate includes three capabilities:

* Generating simulated users
* Generating event values
* Quick simulation. 

Together, they bridge the gap between journey creation and activation, building confidence in journey logic and reducing the risk of post-launch errors.

## Use cases

### Key use cases for Journey Simulate

Journey Simulate offers three capabilities that can be leveraged to reduce testing time and improve journey quality before go-live:

**Generating simulated users**

* Generate simulated users automatically based on journey paths and required attributes.
* Create simulated users that cover all branches and conditions in a journey, including execution addresses (email, push, SMS).
* Update simulated user attributes on demand to refine test scenarios.
* Ensure all journey branches are covered by assigning the right simulated user to each path.

**Generating event values**

* Generate values for events used in a journey to drive test execution through specific paths.
* Define event attribute values that trigger the desired conditions and branches during simulation.

**Quick simulation**

* Start journey simulation and trigger test executions for all simulated users needed to test all paths of a journey, in a single interaction.
* Visualize how simulated users flow through a journey, step by step, including branching paths and conditional logic.
* Identify which simulated user flows through which path, and why, with detailed node-by-node traversal.
* Review simulation reporting at the end of a run in the Journey Optimizer UI to validate outcomes before activation.

## In scope skills and limitations

### **In scope**

The following capabilities are supported by the Journey Simulation feature:

* **Simulated user management**: View, edit, and update simulated user attributes, including execution addresses and personalization data.
* **Simulation control**: Start and stop journey simulation directly through the Journey Simulation in-product experience.
* **Test execution**: Trigger test executions for one or multiple simulated users.
* **Journey flow visualization**: View step-by-step traversal of simulated users through journey nodes, including branching, splits, and user status.
* **Simulation reporting**: View reporting at the end of a simulation run in the Journey Optimizer UI.
* **Multi-user testing**: Run and visualize tests for multiple simulated users simultaneously, covering all journey branches.

In addition to this, the following capabilities are supported by the Journey Simulate skill:

* **Simulated user generation**: Create simulated users based on journey paths, existing test profiles, or specified attributes.
* **Event value generation**: Generate and assign event attribute values to drive test execution through specific journey paths.
* **Quick simulation**: Run a full end-to-end simulation with minimal intervention. The skill automatically generates simulated users, event values, and pre-filled test settings, then executes the journey and surfaces results for review.

### **Limitations**

Simulation may not support every activity, channel, or integration that Test mode or a live journey supports, and behavior may change as the capability matures.

➡️ Learn more about [Simulation limitations](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs#limitations) in the Journey Optimizer documentation.

-->
