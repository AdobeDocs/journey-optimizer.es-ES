---
solution: Journey Optimizer
product: journey optimizer
title: Preguntas más frecuentes sobre campañas organizadas
description: Preguntas frecuentes sobre las campañas orquestadas de Journey Optimizer
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: aea8e1bc6f34400070234195f576fa7df59dca7d
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 5%

---

# Preguntas frecuentes {#faq-oc}

A continuación, encontrará las preguntas más frecuentes sobre campañas organizadas de Adobe Journey Optimizer.

¿Necesita más detalles? Usa las opciones de comentarios de la parte inferior de esta página para plantear tu pregunta o conectar con la [comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

## ¿Qué es la orquestación de Campaign? {#what-are-oc}

Campaign Orchestration es una función de Journey Optimizer que admite flujos de trabajo de un solo paso o de varios pasos que aprovechan el almacén de datos relacional para crear y segmentar audiencias con el fin de lograr una participación por lotes.

Lleva un nuevo tipo de campañas a Journey Optimizer: **Campañas orquestadas**. Las campañas organizadas ayudan a las marcas a ejecutar campañas de marketing complejas y de uno a varios a escala. Están diseñadas para la participación iniciada por la marca, como promociones, campañas de temporada o comunicaciones basadas en la cuenta.

En comparación con las campañas de un solo envío/acción, aportan **orquestación y secuenciación** al marketing saliente: las audiencias se mueven juntas a través de un flujo de trabajo de varios pasos, en lugar de recibir una ráfaga única.

## ¿Qué puedo hacer con una campaña orquestada? {#what-can-i-do}

Las funcionalidades clave incluyen:

* **Audiencias a petición**: Genere y perfeccione instantáneamente grupos de destino mediante consultas relacionales.
* **Segmentación de varias entidades**: para crear audiencias precisas, conecte los datos del cliente con entidades relacionadas (por ejemplo, cuentas, compras o reservas).
* **Visibilidad previa al envío**: vea los recuentos de audiencia precisos antes del inicio para optimizar el direccionamiento.
* **Flujos de trabajo de varios pasos**: ejecute campañas secuenciadas, como promociones de temporada, lanzamientos de productos u ofertas de fidelidad.

>[!BEGINSHADEBOX]

**Prácticas recomendadas**

* Defina **borrar objetivo de campaña** antes de diseñar los flujos de trabajo.
* Comience con una **audiencia piloto** para validar los recuentos y la lógica antes de escalar.
* Mantenga las reglas de segmentación **tan simples como sea posible** para optimizar el rendimiento y la transparencia.
* Use **convenciones de nomenclatura coherentes** para audiencias y campañas para facilitar la administración.

>[!ENDSHADEBOX]

## ¿Cómo acceder a la orquestación de Campaign? {#access-oc}

Para acceder a Campaign Orchestration, la licencia debe incluir **Journey Optimizer - Campañas y Recorridos** o el paquete **Journey Optimizer - Campañas**. Póngase en contacto con su representante de Adobe para confirmar su licencia y actualizarla si es necesario.

Obtenga más información acerca del modelo de licencias de Campaign Orchestration en [descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

## ¿Qué canales son compatibles? {#channels}

Puede crear campañas organizadas para enviar **correos electrónicos**, **SMS** y **notificaciones push**.


>[!BEGINSHADEBOX]

**Recommendations**

* Haga coincidir el canal con la **naturaleza de su mensaje** (por ejemplo, urgente = SMS, ofertas personalizadas = correo electrónico, contextual = push).
* Valide siempre las preferencias de consentimiento y suscripción antes de activar un canal.
* Pruebe el procesamiento de mensajes en varios dispositivos y clientes para garantizar una experiencia coherente.

>[!ENDSHADEBOX]


## ¿En qué se diferencian las campañas orquestadas de los Recorridos? {#oc-vs-journeys}

* **Campañas orquestadas**: lo mejor para **campañas en lotes, de uno a varios**. Las audiencias progresan de forma masiva, según una programación.
* **Recorridos**: lo mejor para una participación de **uno a uno** en tiempo real. Cada cliente avanza por el recorrido a su propio ritmo, activado por comportamientos o eventos.

>[!BEGINSHADEBOX]

**Práctica recomendada**: Úsalos juntos: Recorridos para experiencias activadas, reactivas y campañas organizadas para iniciativas planificadas y basadas en calendarios.

>[!ENDSHADEBOX]

## ¿Qué es la segmentación de varias entidades? {#multi-entity}

La organización de campañas en Adobe Journey Optimizer utiliza una base de datos relacional. Este tipo de modelo de datos tiene esquemas de datos independientes que están conectados mediante relaciones de tipo 1:1 o 1:many. Esto permite a los usuarios iniciar una consulta en cualquier esquema, no solo a nivel de destinatario, y luego dar la vuelta y volver a otros esquemas relacionados, como compras, productos, reservas o detalles del destinatario, lo que proporciona una gran flexibilidad en la forma de crear segmentos y audiencias, y
refinado.

>[!BEGINSHADEBOX]

**Ejemplo** - Segmentar todos los destinatarios con suscripciones que caduquen en los próximos 30 días. En Campaign Orchestration, la consulta puede comenzar con el esquema Subscriptions, buscar solo la columna de fecha de caducidad de ese esquema y devolver todas las suscripciones que deben caducar y, a continuación, acumular los datos del destinatario relacionados con los ID de suscripciones específicos que devuelven los resultados de forma más rápida y eficaz que los modelos de datos que comienzan cada consulta en el nivel de destinatario.

>[!ENDSHADEBOX]


## ¿Cómo funciona el modelo de datos? {#data-model}

Las campañas usan una **base de datos relacional**. Esto le permite realizar consultas en diferentes conjuntos de datos (por ejemplo, clientes, productos, suscripciones) y conectarlos de forma flexible para una segmentación avanzada.

>[!BEGINSHADEBOX]

**Prácticas recomendadas**

* Organice los conjuntos de datos para que las **relaciones (uniones)** reflejen la lógica empresarial.
* Evite las uniones innecesarias para mantener el rendimiento de las consultas.
* Valide los resultados de la muestra antes de ejecutar extracciones a gran escala.

>[!ENDSHADEBOX]

## ¿Puedo personalizar mensajes con datos relacionales? {#personalization}

Sí. En Campaign Orchestration, se puede actualizar un perfil de destinatario conocido como &quot;entidad de personas&quot; y utilizar esos datos para la personalización. Además, los datos enriquecidos de entidades vinculadas en la base de datos relacional también se pueden utilizar para la personalización. Puede utilizar perfiles de clientes junto con datos vinculados (como compras o suscripciones) para personalizar el contenido en todos los canales admitidos.

>[!BEGINSHADEBOX]

**Recommendations**

* Use **datos transaccionales y de comportamiento** para hacer que las ofertas sean relevantes.
* Combine **atributos estáticos** (por ejemplo, nivel de lealtad) con **atributos dinámicos** (por ejemplo, fecha de última compra).
* Mantenga la personalización concisa: la sobrecarga de mensajes con datos puede dañar la legibilidad.

>[!ENDSHADEBOX]

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  -->

## ¿Qué sucede con los permisos y el consentimiento? {#permissions}

Los permisos y el consentimiento para campañas y recorridos organizados se administran de forma centralizada en Adobe Experience Platform. Esta configuración se aplica en ambas soluciones para cada destinatario antes del envío.

>[!BEGINSHADEBOX]

**Prácticas recomendadas**

* Aplique **gobernanza centralizada**; evite administrar el consentimiento por separado en el nivel de campaña.
* Auditar periódicamente los datos de consentimiento para detectar incoherencias.
* Respete las **exclusiones específicas del canal**; no dé por hecho que el consentimiento global cubre todos los canales.

>[!ENDSHADEBOX]

## ¿Puedo realizar la segmentación ad-hoc en campañas orquestadas? {#ad-hoc}

En Campaign Orchestration, nos referimos a la segmentación ad hoc como &quot;Segmentación en directo&quot;, donde puede acceder a todos los datos disponibles en el almacén relacional en tiempo real, crear una consulta compleja sobre ella y obtener el resultado de la activación instantánea mediante canales salientes (por ejemplo, correo electrónico + SMS).

>[!BEGINSHADEBOX]

**Sugerencias**

* Use la segmentación ad hoc para **necesidades con distinción de tiempo** (por ejemplo, promociones flash).
* Guarde y documente consultas útiles para que se puedan reutilizar en campañas futuras.
* Valide el recuento de audiencias antes de la activación para evitar envíos insuficientes o excesivos.

>[!ENDSHADEBOX]



## ¿Las campañas organizadas admiten la toma de decisiones? {#decisioning}

Sí. Decisioning puede utilizar datos relacionales de campañas orquestadas. Una vez que el esquema relacional se ha conectado con esquemas XDM, los datos XDM se pueden utilizar en la toma de decisiones.

## ¿Cómo funciona la implementación en todos los entornos? {#deployment}

Los objetos creados en campañas orquestadas (por ejemplo, audiencias o flujos de trabajo) están vinculados a la zona protegida en la que se crean. Los flujos de trabajo de empaquetado e implementación estándar en entornos (desarrollo, fase, producción) no están disponibles actualmente para campañas organizadas.

>[!BEGINSHADEBOX]

**Prácticas recomendadas**

* Mantenga **zonas protegidas independientes** para la experimentación, el control de calidad y la producción.
* Documente las configuraciones exhaustivamente para permitir la replicación manual si es necesario.
* Alinee con los equipos de gobernanza para reducir la desviación de la configuración entre entornos.

>[!ENDSHADEBOX]

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->


>[!MORELIKETHIS]
>
>* [Limitaciones y protecciones de campañas orquestadas](../orchestrated/guardrails.md)
>* [Introducción a esquemas y conjuntos de datos en campañas organizadas](../orchestrated/gs-schemas.md)
>* [Cree su primera campaña organizada](../orchestrated/gs-campaign-creation.md)
>* [Descripción del producto Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
