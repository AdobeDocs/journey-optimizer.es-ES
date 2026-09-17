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
source-git-commit: 85784fbe98b5347f86899ce7811017cd368745ff
workflow-type: tm+mt
source-wordcount: '2511'
ht-degree: 8%
---

# Compañero de trabajo para recorridos {#journeys-coworker-skills}

>[!BEGINSHADEBOX]

**En esta página:** Descubra las habilidades de CX Enterprise Coworker disponibles para los recorridos en Adobe Journey Optimizer (crear recorridos a partir de lenguaje natural, generar contenido de canal y analizar el rendimiento del recorrido) con instrucciones detalladas, indicaciones de ejemplo y prácticas recomendadas para cada habilidad.

Más información:

* [Aptitudes de colaborador para Journey Optimizer](../start/ai-features.md#cx-coworker-skills): información general sobre las aptitudes de colaborador en todos los Recorridos, la lealtad y la administración de contenido en Journey Optimizer.
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

1. **Sea específico**: Proporcione detalles claros sobre sus objetivos de recorrido, audiencia de destinatario y acciones deseadas. Incluya información sobre canales, temporización y condiciones.
1. **Especificar tiempo**: indique claramente los períodos de espera entre las acciones y cuándo debe iniciarse el recorrido.
1. **Definir condiciones**: cuando use la lógica condicional, explique los criterios para cada ruta de bifurcación.
1. **Incluir canales**: especifique qué canales de comunicación desea utilizar (push, correo electrónico, SMS).
1. **Programación de menciones**: para los recorridos programados, proporcione la fecha y la hora de inicio que desee.
1. **Acciones personalizadas**: si usa acciones personalizadas en el flujo de trabajo, debe especificar que usa una acción personalizada junto con el nombre exacto de la acción personalizada. Por ejemplo:
Cuando un usuario entre en mi ubicación de tienda, enviar un mensaje de bienvenida mediante la acción personalizada ExternalPush. Espere 2 días y, a continuación, envíe un mensaje de seguimiento mediante una acción personalizada por correo electrónico externo con una encuesta sobre su visita.
1. **Validar expresiones**: asegúrese de comprobar y validar cualquier expresión que las aptitudes de Recorrido creen para asegurarse de que se utilizan los campos y valores correctos.

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

### Aptitudes en el ámbito

Las siguientes funciones son compatibles con la creación de contenido de canal:

* **Generación de contenido con tecnología de IA**: genera contenido para correo electrónico, push, SMS y otros canales mediante mensajes en lenguaje natural.
* **Administración de plantillas**: busca y selecciona entre las plantillas disponibles con capacidades de vista previa.
* **Edición en contexto**: abra el contenido generado en Content Designer para editarlo y refinarlo.
* **Regeneración de contenido**: Regenera el contenido con diferentes tonos, estilos o mensajes mediante la acción Regenerar.
* **Compatibilidad con varios canales**: genere y administre contenido para varios canales dentro del mismo flujo de trabajo de recorrido.
* **acceso al inventario de Recorridos**: seleccione recorridos del inventario y vea los canales asociados.

### Aptitudes fuera del ámbito

Actualmente no se admiten las siguientes funcionalidades:

* **Alineación de marca y comprobaciones de calidad del contenido**
* **Insertar nodos de contenido directamente en el lienzo de recorrido**
* **Importación de plantilla**

### Impulso de las prácticas recomendadas

1. **Sea específico**: Proporcione detalles claros sobre el tipo de contenido, el tono, la audiencia de destino y los mensajes clave.
1. **Especificar canal**: indique claramente para qué canal está creando contenido (correo electrónico, push, SMS).
1. **Definir tono**: especifique el tono deseado (cordial, formal, informal, urgente).
1. **Iterar y refinar**: use la acción de regeneración para refinar el contenido hasta que cumpla con sus requisitos.

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

1. **Analizar anomalías de Recorrido**

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

### Aptitudes en el ámbito

El análisis de Recorrido admite las siguientes funciones:

* **Consultas reactivas**: permite a los usuarios hacer preguntas específicas sobre el rendimiento del recorrido, el uso del público y los conflictos de programación.
* **Integración con otras habilidades**: colabora con las capacidades de Audience y Data Insights para realizar un análisis más profundo.
* **Estructura de la respuesta**: razonamiento (explicar la lógica), resumen del análisis (resaltar puntos clave), detalles del problema (describir el problema) y recomendación (proponer pasos siguientes).
* **Análisis de errores de acciones personalizadas**: Detecte y diagnostique errores de acciones personalizadas y picos de error dentro de un recorrido.
* **Detección de anomalías**: detecte y confirme los picos, las caídas o las líneas planas estadísticamente significativos en los recuentos de entrada, salida o envío de un recorrido, y detecte una causa probable.

### Aptitudes fuera del ámbito

Actualmente no se admiten las siguientes funcionalidades:

* **Creación automática de recorridos**
* **Los canales se solapan**
* **Análisis de entrada del recorrido**
* **Análisis de problemas técnicos**
* **Análisis de fatiga**

### Impulso de las prácticas recomendadas

Para maximizar la eficacia del análisis de Recorrido, siga estas prácticas recomendadas:

1. **Sea específico**: utilice preguntas claras y concisas para obtener información específica. Por ejemplo, en lugar de preguntar &quot;¿Cuáles son mis recorridos?&quot;, especifique &quot;Enumerar todos los recorridos creados en el último mes&quot;.
1. **Combinar información**: integre información de las capacidades de Audience y Data Insights para obtener una vista integral del rendimiento del recorrido.
1. **Perfeccionamiento iterativo**: utilice el análisis de abandonos y solapamientos para perfeccionar de forma iterativa el diseño y la programación de los recorridos.

### Prácticas recomendadas de configuración

* **Defina objetivos claros**: antes de analizar los recorridos, establezca objetivos claros (por ejemplo, mejorar la retención, aumentar las conversiones).
* **Monitorice de forma periódica**: programe revisiones periódicas del rendimiento de los recorridos para identificar las tendencias y las anomalías.
* **Optimice la segmentación**: asegúrese de que la segmentación del público está equilibrada para evitar la fatiga y maximizar la participación.

{{$include /help/_includes/do-not-localize/start/ai-augmented-journeys-coworker-skills.md}}
