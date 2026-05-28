---
solution: Journey Optimizer
product: journey optimizer
title: Preguntas más frecuentes sobre campañas organizadas
description: Preguntas frecuentes sobre las campañas orquestadas de Journey Optimizer
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
TQID: https://experienceleague.adobe.com/25WjNcE8jmkqH2TvJnyST510xamIV-seDXTmHj0QEYs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: e42070c4cc1dde06786c4075b1e6e45e8c323c12
workflow-type: tm+mt
source-wordcount: 2765
ht-degree: 11%

---

# Preguntas frecuentes {#faq-oc}

A continuación, encontrará las preguntas más frecuentes sobre campañas organizadas de Adobe Journey Optimizer.

¿Necesita más información? Use las opciones de comentarios situados en la parte inferior de esta página para plantear su pregunta o conecte con la [comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=es){target="_blank"}.

+++ ¿Qué es la orquestación de Campaign?

Campaign Orchestration es una función de Journey Optimizer que admite flujos de trabajo de un solo paso o de varios pasos que aprovechan el almacén de datos relacional para crear y segmentar audiencias con el fin de lograr una participación por lotes.

Lleva un nuevo tipo de campañas a Journey Optimizer: **Campañas orquestadas**. Las campañas organizadas ayudan a las marcas a ejecutar campañas de marketing complejas y de uno a varios a escala. Están diseñadas para la participación iniciada por la marca, como promociones, campañas de temporada o comunicaciones basadas en la cuenta.

En comparación con las campañas de un solo envío/acción, aportan **orquestación y secuenciación** al marketing saliente: las audiencias se mueven juntas a través de un flujo de trabajo de varios pasos, en lugar de recibir una ráfaga única.

**Más información**

* [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)
* [Cree su primera campaña orquestada](gs-campaign-creation.md)

+++

+++ ¿Qué puedo hacer con una campaña orquestada?

Las funcionalidades clave incluyen:

* **Audiencias a petición**: Genere y perfeccione instantáneamente grupos de destino mediante consultas relacionales.
* **Segmentación de varias entidades**: para crear audiencias precisas, conecte los datos del cliente con entidades relacionadas (por ejemplo, cuentas, compras o reservas).
* **Visibilidad previa al envío**: consulte las recuentos de público precisas antes del inicio para optimizar el direccionamiento.
* **Flujos de trabajo de varios pasos**: ejecute campañas secuenciadas, como promociones de temporada, lanzamientos de productos u ofertas de fidelidad.

**Prácticas recomendadas**

* Defina **borrar objetivo de campaña** antes de diseñar los flujos de trabajo.
* Comience con una **audiencia piloto** para validar los recuentos y la lógica antes de escalar.
* Mantenga las reglas de segmentación **tan simples como sea posible** para optimizar el rendimiento y la transparencia.
* Use **convenciones de nomenclatura coherentes** para audiencias y campañas para facilitar la administración.

**Más información**

* [Creación de una campaña organizada](create-orchestrated-campaign.md)
* [Trabajo con actividades de campaña](activities/about-activities.md)
* [Cree la regla con el modelador de consultas](build-query.md)

+++

+++ ¿Cómo se obtiene acceso a la orquestación de Campaign?

Para acceder a Campaign Orchestration, la licencia debe incluir **Journey Optimizer - Campañas y Recorridos** o el paquete **Journey Optimizer - Campañas**. Póngase en contacto con su representante de Adobe para confirmar su licencia y actualizarla si es necesario.

**Más información**

* [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)
* [Descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}

+++

+++ ¿En qué se diferencian las campañas orquestadas de los Recorridos?

* **Campañas orquestadas**: lo mejor para **campañas en lotes, de uno a varios**. Las audiencias progresan de forma masiva, según una programación.
* **Recorridos**: lo mejor para una participación de **uno a uno** en tiempo real. Cada cliente avanza por el recorrido a su propio ritmo, activado por comportamientos o eventos.

**Práctica recomendada**: utilícelos juntos: Recorridos para experiencias activadas, reactivas y campañas organizadas para iniciativas planificadas y basadas en calendarios.

**Más información**

* [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)
* [Creación de su primer recorrido](../building-journeys/journey-gs.md)
* [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)

+++

+++ ¿Qué es la segmentación de varias entidades?

La organización de campañas en Adobe Journey Optimizer utiliza una base de datos relacional. Este tipo de modelo de datos tiene esquemas de datos independientes que están conectados mediante relaciones de tipo 1:1 o 1:many. Esto permite a los usuarios iniciar una consulta en cualquier esquema, no solo a nivel de destinatario, y luego dar la vuelta y volver a otros esquemas relacionados, como compras, productos, reservas o detalles del destinatario, lo que proporciona una gran flexibilidad en la forma de crear y refinar segmentos y audiencias.

**Ejemplo** - Segmentar todos los destinatarios con suscripciones que caduquen en los próximos 30 días. En Campaign Orchestration, la consulta puede comenzar con el esquema Subscriptions, buscar solo la columna de fecha de caducidad de ese esquema y devolver todas las suscripciones que deben caducar y, a continuación, acumular los datos del destinatario relacionados con los ID de suscripciones específicos que devuelven los resultados de forma más rápida y eficaz que los modelos de datos que comienzan cada consulta en el nivel de destinatario.

**Más información**

* [Introducción a esquemas y conjuntos de datos](gs-schemas.md)
* [Configuración de una dimensión de segmentación](target-dimension.md)
* [Cree la regla con el modelador de consultas](build-query.md)

+++

+++ ¿Cómo funciona el modelo de datos?

Las campañas usan una **base de datos relacional**. Esto le permite realizar consultas en diferentes conjuntos de datos (por ejemplo, clientes, productos, suscripciones) y conectarlos de forma flexible para una segmentación avanzada.

**Prácticas recomendadas**

* Organice los conjuntos de datos para que las **relaciones (uniones)** reflejen la lógica empresarial.
* Evite las uniones innecesarias para mantener el rendimiento de las consultas.
* Valide los resultados de la muestra antes de ejecutar extracciones a gran escala.

**Más información**

* [Introducción a esquemas y conjuntos de datos](gs-schemas.md)
* [Creación de un esquema manualmente](manual-schema.md)
* [Ingesta de datos](ingest-data.md)

+++

+++ ¿Puedo personalizar mensajes con datos relacionales?

Sí. En Campaign Orchestration, se puede actualizar un perfil de destinatario conocido como &quot;entidad de personas&quot; y utilizar esos datos para la personalización. Además, los datos enriquecidos de entidades vinculadas en la base de datos relacional también se pueden utilizar para la personalización. Puede utilizar perfiles de clientes junto con datos vinculados (como compras o suscripciones) para personalizar el contenido en todos los canales admitidos.

**Recommendations**

* Use **datos transaccionales y de comportamiento** para hacer que las ofertas sean relevantes.
* Combine **atributos estáticos** (por ejemplo, nivel de lealtad) con **atributos dinámicos** (por ejemplo, fecha de última compra).
* Mantenga la personalización concisa: la sobrecarga de mensajes con datos puede dañar la legibilidad.

**Más información**

* [Uso de la actividad Enriquecimiento](activities/enrichment.md)
* [Añadir una actividad de canal en una campaña organizada](activities/channels.md)

+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  
-->

+++ ¿Cómo pruebo una campaña orquestada activada por señales antes de publicar?

Mientras la campaña esté en **Borrador**, puede probarla definiendo **parámetros** en la programación y proporcionando **valores de prueba** para cada uno. Inicie el flujo de trabajo y, a continuación, llame a la API de déclencheur (utilizando la solicitud de ejemplo de la configuración de programación o su propia solicitud con el mismo punto de conexión) para ejecutar la campaña con esos valores de prueba. [Aprenda a completar y probar una campaña activada por señales](trigger-orchestrated-campaign.md#build-and-test).

+++

+++ ¿Puedo revertir una campaña orquestada en vivo a borrador?

Sí, en situaciones específicas. La opción **[!UICONTROL Volver al borrador]** está diseñada como un mecanismo de recuperación para cancelar la publicación y revertir una campaña al estado de borrador.

Esta opción está disponible para campañas programadas en espera de ejecución o para campañas en directo con errores de ejecución. [Aprenda a revertir una campaña en vivo al borrador](start-monitor-campaigns.md#back-to-draft)

+++

+++ ¿Qué sucede internamente cuando publico una campaña orquestada?

Al hacer clic en **[!UICONTROL Publicar]**, se produce la siguiente secuencia:

1. **Activación del programador**: si se configura una programación, el programador inicia y déclencheur la ejecución en el momento definido.
1. **Guardar actividades de audiencia ejecutadas primero**: todas las actividades Guardar audiencia se ejecutan antes de las actividades de mensajes. El shell de audiencia se crea en Audience Portal y los perfiles cualificados comienzan a realizar la ingesta.
1. **Comienza la ejecución del mensaje** — Las actividades de canal comienzan a procesarse para la primera actividad de mensaje del flujo de trabajo.
1. **Búsqueda de instantáneas de perfil**: los datos de perfil se resuelven con una instantánea tomada en el momento de la publicación, no con el perfil en tiempo real, lo que garantiza la coherencia en toda la ejecución.
1. **Evaluación del consentimiento**: el consentimiento se respeta directamente desde el registro de perfil y no se vuelve a evaluar en el momento del envío.
1. **Reconciliación de perfiles**: los destinatarios se reconcilian con perfiles de Adobe Experience Platform en el momento de la entrega.
1. **Creación del registro de envío**: los eventos de envío se registran en el conjunto de datos `ajo_message_feedback_event`.

**Más información**

* [Secuencia de ejecución de tiempo de publicación](start-monitor-campaigns.md#publication-sequence)
* [Iniciar y monitorizar campañas orquestadas](start-monitor-campaigns.md)

+++

+++ ¿Por qué no se envían mis mensajes después de publicar la campaña?

Varias situaciones pueden impedir que los mensajes se envíen después de la publicación. Compruebe lo siguiente en orden:

1. **Confirmación de envío pendiente (más común)**: para las campañas no recurrentes, el envío de mensajes se detiene de forma predeterminada hasta que confirme explícitamente el envío desde el panel de propiedades de la actividad del canal. La campaña se muestra como **Activo**, pero no se emitirán mensajes hasta que se confirme. [Más información](start-monitor-campaigns.md#confirm-sending)

1. **La campaña está programada para el futuro**: si se ha configurado una programación, la campaña estará Activa pero la ejecución aún no se ha iniciado. Compruebe la configuración de la programación y espere a que llegue la hora de inicio configurada. [Más información](create-orchestrated-campaign.md#schedule)

1. **Guardar actividades de audiencia que aún se están ingiriendo** — Guardar actividades de audiencia ejecutadas antes de actividades de mensaje en el momento de la publicación. Si la ingesta de audiencia aún está en curso, la ejecución del mensaje aún no ha comenzado. Monitorice los indicadores de estado de actividad en el lienzo. [Más información](start-monitor-campaigns.md#activities)

1. **La audiencia está vacía** — La consulta de direccionamiento devolvió cero perfiles. Revise las reglas de segmentación y valide el recuento de público antes de volver a publicar.

1. **Todos los perfiles excluidos** — El consentimiento se evalúa en el momento del envío con cada perfil. Si todos los perfiles de destino se han excluido del canal correspondiente, no se envía ningún mensaje. [Más información](../action/consent.md)

1. **Actividad de canal en estado de error**: un indicador de estado naranja o rojo en la actividad de canal indica un problema de bloqueo. Abra **[!UICONTROL Registros]** para obtener detalles sobre el error y cómo resolverlo. [Más información](start-monitor-campaigns.md#logs-tasks)

1. **Entrega de limitación de control de tarifa**: si el control de tarifa está habilitado en la actividad del canal, la entrega puede ser más lenta de lo esperado. Compruebe la configuración del control de velocidad en el panel de propiedades de actividad del canal. [Más información](activities/channels.md#rate-control)

**Más información**

* [Iniciar y monitorizar campañas orquestadas](start-monitor-campaigns.md)
* [Añadir una actividad de canal en una campaña organizada](activities/channels.md)

+++

+++ ¿La publicación utiliza un perfil en tiempo real o una instantánea?

En el momento de la publicación, los datos del perfil se resuelven en función de una **instantánea tomada en el momento de la publicación**, no del perfil en tiempo real. Esto garantiza la coherencia en toda la ejecución de la campaña: todas las actividades procesan el mismo estado de perfil independientemente del tiempo que se ejecute la campaña.

Sin embargo, el consentimiento siempre se respeta desde el registro de perfil actual y no se vuelve a evaluar en el momento del envío.

Tenga en cuenta que la segmentación en campañas orquestadas se realiza en Destinatarios (almacén relacional), mientras que el envío de mensajes y las comprobaciones de consentimiento se resuelven en el Perfil de Adobe Experience Platform.

**Más información**

* [Secuencia de ejecución de tiempo de publicación](start-monitor-campaigns.md#publication-sequence)
* [¿Cuál es la relación entre las entidades de destinatario y perfil?](#faq-oc)
* [Trabajar con políticas de consentimiento](../action/consent.md)

+++

+++ ¿Qué canales son compatibles?

Puede crear campañas organizadas para enviar **correos electrónicos**, **SMS**, **notificaciones inmediatas** y **correos directos**.

**Más información**

* [Añadir una actividad de canal en una campaña organizada](activities/channels.md)
* [Trabajo con actividades de campaña](activities/about-activities.md)

+++

+++ ¿Se pueden iniciar varias comunicaciones y diferentes canales dentro de la misma campaña orquestada?

Sí, las campañas orquestadas admiten la orquestación entre canales. Puede combinar actividades de correo electrónico, SMS, notificaciones push y correo directo en un lienzo de campaña de varios pasos para crear experiencias de cliente completas.

**Más información**

* [Añadir una actividad de canal en una campaña organizada](activities/channels.md)
* [Trabajo con actividades de campaña](activities/about-activities.md)

+++

+++ ¿Están disponibles las plantillas de campaña organizadas?

No, no puede definir ni utilizar plantillas de campaña, pero puede utilizar plantillas de contenido para sus comunicaciones.

**Más información**

* [Añadir una actividad de canal en una campaña organizada](activities/channels.md)
* [Creación de una campaña organizada](create-orchestrated-campaign.md)

+++

+++ ¿El diseñador de contenido de los mensajes es específico de las campañas orquestadas?

No, el diseñador de contenido, incluido el Designer de correo electrónico, es común en todas las funciones de Journey Optimizer.

**Más información**

* [Añadir una actividad de canal en una campaña organizada](activities/channels.md)
* [Uso de la actividad Enriquecimiento](activities/enrichment.md)

+++

+++ ¿Cómo se conectan los distintos canales en las campañas orquestadas?

El componente de canal y el tiempo de ejecución son comunes a todas las campañas de Journey Optimizer, pero los canales admitidos difieren. Las campañas organizadas admiten correo electrónico, SMS, notificaciones push y correo directo.

**Más información**

* [Añadir una actividad de canal en una campaña organizada](activities/channels.md)
* [Mecanismos de protección y limitaciones](guardrails.md)

+++


+++ ¿Pueden las campañas organizadas conectarse con canales salientes (web, en la aplicación)?

No, los canales entrantes como la web y la aplicación no son compatibles con las campañas orquestadas. Solo se admiten canales salientes (correo electrónico, SMS, notificaciones push y correo postal).

**Más información**

* [Mecanismos de protección y limitaciones](guardrails.md)
* [Añadir una actividad de canal en una campaña organizada](activities/channels.md)

+++

+++ ¿Qué sucede con los permisos y el consentimiento?

Los permisos y el consentimiento para campañas y recorridos organizados se administran de forma centralizada en Adobe Experience Platform. Esta configuración se aplica en ambas soluciones para cada destinatario antes del envío.

**Prácticas recomendadas**

* Aplique **gobernanza centralizada**; evite administrar el consentimiento por separado en el nivel de campaña.
* Auditar periódicamente los datos de consentimiento para detectar incoherencias.
* Respete las **exclusiones específicas del canal**; no dé por hecho que el consentimiento global cubre todos los canales.

**Más información**

* [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)
* [Mecanismos de protección y limitaciones](guardrails.md)

+++


+++ ¿Puedo realizar la segmentación ad-hoc en campañas orquestadas?

En Campaign Orchestration, nos referimos a la segmentación ad hoc como &quot;Segmentación en directo&quot;, donde puede acceder a todos los datos disponibles en el almacén relacional en tiempo real, crear una consulta compleja sobre ella y obtener el resultado de la activación instantánea mediante canales salientes (por ejemplo, correo electrónico + SMS).

**Sugerencias**

* Use la segmentación ad hoc para **necesidades con distinción de tiempo** (por ejemplo, promociones flash).
* Guarde y documente consultas útiles para que se puedan reutilizar en campañas futuras.
* Valide la recuento de público antes de la activación para evitar envíos insuficientes o excesivos.

**Más información**

* [Cree la regla con el modelador de consultas](build-query.md)
* [Uso de la actividad Generar público](activities/build-audience.md)
* [Configuración de una dimensión de segmentación](target-dimension.md)

+++


+++ ¿Campaign Orchestration solo accede a los datos cargados por lotes o también puede consultar tablas actualizadas en tiempo real (como los datos de Analytics)?

Journey Optimizer Campaign Orchestration puede crear consultas ad hoc sobre esquemas relacionales. Los esquemas relacionales solo admiten orígenes de lotes por ahora. Además, admite actividades Leer audiencia de cualquier tipo de audiencia de Adobe Experience Platform.

**Más información**

* [Introducción a esquemas y conjuntos de datos](gs-schemas.md)
* [Ingesta de datos](ingest-data.md)
* [Uso de la actividad Leer público](activities/read-audience.md)

+++

+++ ¿Las campañas organizadas admiten la toma de decisiones?

No, las campañas orquestadas no admiten capacidades de toma de decisiones. Para las funciones de toma de decisiones, utilice recorridos de Journey Optimizer estándar o campañas de acción en su lugar.

**Más información**

* [Introducción a Toma de decisiones sobre experiencias](../experience-decisioning/gs-experience-decisioning.md)
* [Creación de su primer recorrido](../building-journeys/journey-gs.md)
* [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)

+++


+++ ¿Cómo funciona la implementación en todos los entornos?

Los objetos creados en campañas orquestadas (por ejemplo, audiencias y flujos de trabajo) pertenecen a la zona protegida en la que se crearon. Para reutilizar una campaña orquestada en otra zona protegida (por ejemplo, desarrollo, fase o producción), cópiela con **Herramientas para zonas protegidas**: agregue la campaña a un paquete, publique el paquete e impórtelo a la zona protegida de destino. La copia importada se crea en **borrador** y **al volver a importar el mismo paquete, se crea una nueva campaña** en lugar de actualizar una existente. Un movimiento completo suele llevar **más de un paso**: es posible que necesite alinear **configuraciones de canal** (nombres coincidentes en el destino), **esquemas** y **conjuntos de datos** a través del mismo paquete o importaciones de paquete adicionales; las configuraciones de canal no se copian con la campaña. No hay ninguna lista de comprobación previa a la exportación completa en la interfaz de usuario; use el flujo de asignación de importación y **alertas posteriores a la importación** para finalizar la configuración. Para obtener detalles y limitaciones, consulte [Copiar objetos de Journey Optimizer entre zonas protegidas](../configuration/copy-objects-to-sandbox.md).

**Prácticas recomendadas**

* Mantenga **zonas protegidas independientes** para la experimentación, el control de calidad y la producción.
* Justo después de la importación, [duplique la campaña](../campaigns/manage-campaigns.md#duplicate-a-campaign) y trabaje desde el duplicado para que el sistema de informes muestre correctamente los comentarios y los datos de seguimiento.
* Después de cada importación, valide la campaña de principio a fin en la zona protegida de destino antes de publicar.
* Documente las configuraciones y alinéelas con los equipos de gobernanza para reducir la deriva de configuración entre entornos.

**Más información**

* [Copiar objetos de Journey Optimizer entre zonas protegidas](../configuration/copy-objects-to-sandbox.md)
* [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)
* [Mecanismos de protección y limitaciones](guardrails.md)

+++

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->

+++ ¿Cuál es la relación entre las entidades de destinatario y perfil?

La segmentación se realiza en los destinatarios mientras se envían con el perfil de Adobe Experience Platform. La dimensión objetivo del destinatario amplía el perfil unificado con datos adicionales que se utilizan para la segmentación dentro de campañas orquestadas, mientras que el destinatario se concilia con el perfil en tiempo de ejecución para enviar mensajes y comprobar la directiva de consentimiento y las reglas empresariales. Esta reconciliación es útil para unificar las reglas empresariales y la aplicación de consentimiento en el nivel de perfil.

![](assets/recipients-and-profiles.png)

**Más información**

* [Configuración de una dimensión de segmentación](target-dimension.md)
* [Introducción a esquemas y conjuntos de datos](gs-schemas.md)
* [Cree la regla con el modelador de consultas](build-query.md)

+++

+++ ¿En qué casos se recomienda utilizar entidades de destinatario frente a de perfil?

Responder &quot;Sí&quot; sugiere el mejor almacén de datos, pero confirme siempre el mejor enfoque en función de su caso de uso y las restricciones con su representante de Adobe.

| Almacenamiento relacional | Perfil del cliente en tiempo real |
|---------|----------|
| ¿La fuente de los datos ya es relacional? | ¿Es la fuente de la transmisión de datos? |
| ¿Tiene pensado ingerir datos según sea necesario para casos de uso de marketing? | ¿Es la actualización de los datos un requisito importante? |
| ¿Existe un gran volumen de datos históricos (`>` 2 meses) que se necesitan para los casos de uso de activación de marketing? | ¿Hay escenarios en los que la acción o la decisión en el momento requieren datos? |
| ¿Hay necesidades específicas de creación, evaluación y activación de audiencias? | ¿Pueden limitarse los datos de comportamiento a `<` 90 días utilizando acumulados precalculados? |
|  | ¿Se necesitan datos para personalizar los mensajes en tiempo real? |

**Más información**

* [Configuración de una dimensión de segmentación](target-dimension.md)
* [Introducción a esquemas y conjuntos de datos](gs-schemas.md)
* [Cree la regla con el modelador de consultas](build-query.md)

+++

+++ ¿Cuál es el número máximo de actividades por campaña orquestada?

Se aplican dos límites diferentes:

* **Actividades de canal**: un máximo de 10 actividades de canal por campaña orquestada (correo electrónico, SMS, push o correo directo). Las actividades de segmentación y control de flujo no cuentan. Si se supera este límite al guardar o publicar, la operación fallará.

* **Tamaño de lienzo**: hasta **500 actividades** en el lienzo. Para mantener la capacidad de mantenimiento, mantenga los flujos de trabajo en **100 actividades** en la práctica.

**Más información**

* [Mecanismos de protección y limitaciones](guardrails.md)
* [Trabajo con actividades de campaña](activities/about-activities.md)

+++

+++ ¿Es posible realizar enriquecimientos para agregar datos adicionales?

Sí, se pueden enriquecer los datos desde el almacén relacional y desde las audiencias de Adobe Experience Platform. Utilice la actividad Enrichment para mejorar los datos de audiencia con atributos adicionales de esquemas relacionados.

**Más información**

* [Uso de la actividad Enriquecimiento](activities/enrichment.md)
* [Uso de la actividad Reconciliación](activities/reconciliation.md)

+++

+++ ¿Deben definirse todos los filtros mediante audiencias o se puede configurar algún tipo de filtro?

Las campañas orquestadas admiten filtros predefinidos: puede definir y guardar una consulta como filtro, agregarla a sus favoritos y reutilizarla en tareas de segmentación adicionales. Los filtros predefinidos pueden incluir parámetros para que pueda introducir valores en el momento de su uso. [Aprenda a trabajar con filtros predefinidos](predefined-filters.md).

**Más información**

* [Cree la regla con el modelador de consultas](build-query.md)
* [Uso de la actividad Generar público](activities/build-audience.md)
* [Trabajo con filtros predefinidos](orchestrated-rule-builder.md)

+++


## Recursos adicionales

Para obtener más información y actualizaciones, explore los siguientes recursos:

* [Limitaciones y protecciones de campañas organizadas](guardrails.md)
* [Introducción a esquemas y conjuntos de datos en campañas organizadas](gs-schemas.md)
* [Cree su primera campaña orquestada](gs-campaign-creation.md)
* [Descripción del producto de Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
