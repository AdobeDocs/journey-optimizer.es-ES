---
solution: Journey Optimizer
product: journey optimizer
title: Preguntas más frecuentes sobre campañas organizadas
description: Preguntas frecuentes sobre las campañas orquestadas de Journey Optimizer
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: f82e725b58dbb2fdea70455a203d83b13b0e4a2b
workflow-type: tm+mt
source-wordcount: '1419'
ht-degree: 3%

---

# Preguntas frecuentes {#faq-oc}

A continuación, encontrará las preguntas más frecuentes sobre campañas organizadas de Adobe Journey Optimizer.

¿Necesita más detalles? Usa las opciones de comentarios de la parte inferior de esta página para plantear tu pregunta o conectar con la [comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=es){target="_blank"}.

+++ ¿Qué es la orquestación de Campaign?

Campaign Orchestration es una función de Journey Optimizer que admite flujos de trabajo de un solo paso o de varios pasos que aprovechan el almacén de datos relacional para crear y segmentar audiencias con el fin de lograr una participación por lotes.

Lleva un nuevo tipo de campañas a Journey Optimizer: **Campañas orquestadas**. Las campañas organizadas ayudan a las marcas a ejecutar campañas de marketing complejas y de uno a varios a escala. Están diseñadas para la participación iniciada por la marca, como promociones, campañas de temporada o comunicaciones basadas en la cuenta.

En comparación con las campañas de un solo envío/acción, aportan **orquestación y secuenciación** al marketing saliente: las audiencias se mueven juntas a través de un flujo de trabajo de varios pasos, en lugar de recibir una ráfaga única.

+++

+++ ¿Qué puedo hacer con una campaña orquestada?

Las funcionalidades clave incluyen:

* **Audiencias a petición**: Genere y perfeccione instantáneamente grupos de destino mediante consultas relacionales.
* **Segmentación de varias entidades**: para crear audiencias precisas, conecte los datos del cliente con entidades relacionadas (por ejemplo, cuentas, compras o reservas).
* **Visibilidad previa al envío**: vea los recuentos de audiencia precisos antes del inicio para optimizar el direccionamiento.
* **Flujos de trabajo de varios pasos**: ejecute campañas secuenciadas, como promociones de temporada, lanzamientos de productos u ofertas de fidelidad.

**Prácticas recomendadas**

* Defina **borrar objetivo de campaña** antes de diseñar los flujos de trabajo.
* Comience con una **audiencia piloto** para validar los recuentos y la lógica antes de escalar.
* Mantenga las reglas de segmentación **tan simples como sea posible** para optimizar el rendimiento y la transparencia.
* Use **convenciones de nomenclatura coherentes** para audiencias y campañas para facilitar la administración.

+++

+++ ¿Cómo acceder a la orquestación de Campaign?

Para acceder a Campaign Orchestration, la licencia debe incluir **Journey Optimizer - Campañas y Recorridos** o el paquete **Journey Optimizer - Campañas**. Póngase en contacto con su representante de Adobe para confirmar su licencia y actualizarla si es necesario.

Obtenga más información acerca del modelo de licencias de Campaign Orchestration en [descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

+++ ¿En qué se diferencian las campañas orquestadas de los Recorridos?

* **Campañas orquestadas**: lo mejor para **campañas en lotes, de uno a varios**. Las audiencias progresan de forma masiva, según una programación.
* **Recorridos**: lo mejor para una participación de **uno a uno** en tiempo real. Cada cliente avanza por el recorrido a su propio ritmo, activado por comportamientos o eventos.

**Práctica recomendada**: Úsalos juntos: Recorridos para experiencias activadas, reactivas y campañas organizadas para iniciativas planificadas y basadas en calendarios.


+++

+++ ¿Qué es la segmentación de varias entidades?

La organización de campañas en Adobe Journey Optimizer utiliza una base de datos relacional. Este tipo de modelo de datos tiene esquemas de datos independientes que están conectados mediante relaciones de tipo 1:1 o 1:many. Esto permite a los usuarios iniciar una consulta en cualquier esquema, no solo a nivel de destinatario, y luego dar la vuelta y volver a otros esquemas relacionados, como compras, productos, reservas o detalles del destinatario, lo que proporciona una gran flexibilidad en la forma de crear segmentos y audiencias, y
refinado.


**Ejemplo** - Segmentar todos los destinatarios con suscripciones que caduquen en los próximos 30 días. En Campaign Orchestration, la consulta puede comenzar con el esquema Subscriptions, buscar solo la columna de fecha de caducidad de ese esquema y devolver todas las suscripciones que deben caducar y, a continuación, acumular los datos del destinatario relacionados con los ID de suscripciones específicos que devuelven los resultados de forma más rápida y eficaz que los modelos de datos que comienzan cada consulta en el nivel de destinatario.

+++

+++ ¿Cómo funciona el modelo de datos?

Las campañas usan una **base de datos relacional**. Esto le permite realizar consultas en diferentes conjuntos de datos (por ejemplo, clientes, productos, suscripciones) y conectarlos de forma flexible para una segmentación avanzada.

**Prácticas recomendadas**

* Organice los conjuntos de datos para que las **relaciones (uniones)** reflejen la lógica empresarial.
* Evite las uniones innecesarias para mantener el rendimiento de las consultas.
* Valide los resultados de la muestra antes de ejecutar extracciones a gran escala.


+++

+++ ¿Puedo personalizar mensajes con datos relacionales?

Sí. En Campaign Orchestration, se puede actualizar un perfil de destinatario conocido como &quot;entidad de personas&quot; y utilizar esos datos para la personalización. Además, los datos enriquecidos de entidades vinculadas en la base de datos relacional también se pueden utilizar para la personalización. Puede utilizar perfiles de clientes junto con datos vinculados (como compras o suscripciones) para personalizar el contenido en todos los canales admitidos.


**Recommendations**

* Use **datos transaccionales y de comportamiento** para hacer que las ofertas sean relevantes.
* Combine **atributos estáticos** (por ejemplo, nivel de lealtad) con **atributos dinámicos** (por ejemplo, fecha de última compra).
* Mantenga la personalización concisa: la sobrecarga de mensajes con datos puede dañar la legibilidad.


+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  -->

+++ ¿Qué canales son compatibles?

Puede crear campañas organizadas para enviar **correos electrónicos**, **SMS** y **notificaciones push**.

+++

+++ ¿Se pueden iniciar varias comunicaciones y diferentes canales dentro de la misma campaña orquestada?

Sí, las campañas orquestadas admiten la orquestación entre canales.

+++

+++ ¿Están disponibles las plantillas de campaña organizadas?

No, no puede definir ni utilizar plantillas de campaña, pero puede utilizar plantillas de contenido para sus comunicaciones.

+++

+++ ¿El diseñador de contenido de los mensajes es específico de las campañas orquestadas?

No, el diseñador de contenido, incluido el Designer de correo electrónico, es común en todas las funciones de Journey Optimizer.

+++

+++ ¿Cómo se conectan los distintos canales en las campañas orquestadas?

El componente de canal y el tiempo de ejecución son comunes a todas las campañas de Journey Optimizer, pero los canales admitidos difieren.

+++


+++ ¿Pueden las campañas organizadas conectarse con canales salientes (web, en la aplicación)?

No, los canales salientes no son compatibles con las campañas orquestadas.

+++

+++ ¿Qué sucede con los permisos y el consentimiento?

Los permisos y el consentimiento para campañas y recorridos organizados se administran de forma centralizada en Adobe Experience Platform. Esta configuración se aplica en ambas soluciones para cada destinatario antes del envío.


**Prácticas recomendadas**

* Aplique **gobernanza centralizada**; evite administrar el consentimiento por separado en el nivel de campaña.
* Auditar periódicamente los datos de consentimiento para detectar incoherencias.
* Respete las **exclusiones específicas del canal**; no dé por hecho que el consentimiento global cubre todos los canales.

+++


+++ ¿Puedo realizar la segmentación ad-hoc en campañas orquestadas?

En Campaign Orchestration, nos referimos a la segmentación ad hoc como &quot;Segmentación en directo&quot;, donde puede acceder a todos los datos disponibles en el almacén relacional en tiempo real, crear una consulta compleja sobre ella y obtener el resultado de la activación instantánea mediante canales salientes (por ejemplo, correo electrónico + SMS).


**Sugerencias**

* Use la segmentación ad hoc para **necesidades con distinción de tiempo** (por ejemplo, promociones flash).
* Guarde y documente consultas útiles para que se puedan reutilizar en campañas futuras.
* Valide el recuento de audiencias antes de la activación para evitar envíos insuficientes o excesivos.

+++


+++ ¿Campaign Orchestration solo accede a los datos cargados por lotes o también puede consultar tablas actualizadas en tiempo real (como los datos de Analytics)?

Journey Optimizer Campaign Orchestration puede generar primero consultas ad hoc sobre esquemas relacionales. Los esquemas relacionales solo admiten orígenes de lotes por ahora. Además, admite Leer audiencia de cualquier tipo de Audiencia de Adobe Experience Platform.

+++

+++ ¿Las campañas organizadas admiten la toma de decisiones?

Sí. Decisioning puede utilizar datos relacionales de campañas orquestadas. Una vez que el esquema relacional se ha conectado con esquemas XDM, los datos XDM se pueden utilizar en la toma de decisiones.

+++


+++ ¿Cómo funciona la implementación en todos los entornos?

Los objetos creados en campañas orquestadas (por ejemplo, audiencias o flujos de trabajo) están vinculados a la zona protegida en la que se crean. Los flujos de trabajo de empaquetado e implementación estándar en entornos (desarrollo, fase, producción) no están disponibles actualmente para campañas organizadas.

**Prácticas recomendadas**

* Mantenga **zonas protegidas independientes** para la experimentación, el control de calidad y la producción.
* Documente las configuraciones exhaustivamente para permitir la replicación manual si es necesario.
* Alinee con los equipos de gobernanza para reducir la desviación de la configuración entre entornos.

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

La segmentación se realiza en los destinatarios mientras se envían con el perfil de Adobe Experience Platform. La dimensión objetivo del destinatario amplía el perfil unificado con datos adicionales que se utilizan para la segmentación dentro de campañas orquestadas, mientras que el destinatario se concilia con el perfil en tiempo de ejecución para enviar mensajes y comprobar la directiva de consentimiento y las reglas empresariales. Esta reconciliación es útil para unificar las reglas empresariales y la aplicación de consentimiento en el nivel de perfil

![](assets/recipients-and-profiles.png)

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

+++

+++ ¿Cuál es el número máximo de actividades por campaña orquestada?

El número de actividades en una campaña orquestada está limitado a 500.

+++

+++ ¿Es posible realizar enriquecimientos para agregar datos adicionales?

Sí, se pueden enriquecer los datos desde el almacén relacional y desde las audiencias de Adobe Experience Platform.

+++

+++ ¿Deben definirse todos los filtros mediante audiencias o se puede configurar algún tipo de filtro?

Las campañas orquestadas admiten Filtros predefinidos: puede definir y guardar una consulta como filtro y agregarla a Favoritos para reutilizarla en tareas de segmentación adicionales.

+++




>[!MORELIKETHIS]
>
>* [Limitaciones y protecciones de campañas orquestadas](../orchestrated/guardrails.md)
>* [Introducción a esquemas y conjuntos de datos en campañas organizadas](../orchestrated/gs-schemas.md)
>* [Cree su primera campaña organizada](../orchestrated/gs-campaign-creation.md)
>* [Descripción del producto Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
