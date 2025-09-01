---
solution: Journey Optimizer
product: journey optimizer
title: Preguntas más frecuentes sobre campañas organizadas
description: Preguntas frecuentes sobre las campañas orquestadas de Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 13bc5f91e0e47bf36b9b9921fa926f8a5e2a50d6
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 2%

---

# Preguntas frecuentes {#faq-oc}

A continuación, encontrará las preguntas más frecuentes sobre Adobe Journey Optimizer Orchestrated Campaigns.

¿Necesita más detalles? Utilice las opciones de comentarios en la parte inferior de esta página para plantear su pregunta.

## ¿Qué son las campañas orquestadas? {#what-are-oc}

Las campañas organizadas en Adobe Journey Optimizer ayudan a las marcas a ejecutar campañas de marketing complejas y de uno a varios a escala. Están diseñadas para la participación iniciada por la marca, como promociones, campañas de temporada o comunicaciones basadas en la cuenta.

En comparación con las campañas de un solo envío, aportan **orquestación y secuenciación** al marketing saliente: las audiencias se mueven juntas a través de un flujo de trabajo de varios pasos, en lugar de recibir una ráfaga única.

## ¿Qué puedo hacer con las campañas orquestadas? {#what-can-i-do}

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


## ¿Qué canales son compatibles? {#channels}

Las campañas organizadas admiten **notificaciones push, por correo electrónico y SMS**.

>[!BEGINSHADEBOX]

**Recommendations**

* Haga coincidir el canal con la **naturaleza de su mensaje** (por ejemplo, urgente = SMS, ofertas personalizadas = correo electrónico, contextual = push).
* Valide siempre las preferencias de consentimiento y suscripción antes de activar un canal.
* Pruebe el procesamiento de mensajes en varios dispositivos y clientes para garantizar una experiencia coherente.

>[!ENDSHADEBOX]

## ¿En qué se diferencian las campañas orquestadas de los Recorridos? {#oc-vs-journeys}

* **Campañas orquestadas**: lo mejor para **campañas en lotes, de uno a varios**. Audiencias completas se mueven juntas por el lienzo de la campaña.
* **Recorridos**: lo mejor para una participación de **uno a uno** en tiempo real. Cada cliente avanza por el recorrido a su propio ritmo, activado por comportamientos o eventos.

>[!BEGINSHADEBOX]

**Sugerencia** - Muchas organizaciones usan **ambos juntos**—Recorridos para experiencias activadas, reactivas y campañas orquestadas para iniciativas planificadas y basadas en calendarios.

>[!ENDSHADEBOX]

## ¿Cómo funciona el modelo de datos? {#data-model}

Las campañas usan una **base de datos relacional**. Esto le permite realizar consultas en diferentes conjuntos de datos (por ejemplo, clientes, productos, suscripciones) y conectarlos de forma flexible para una segmentación avanzada.

>[!BEGINSHADEBOX]

**Prácticas recomendadas**

* Organice los conjuntos de datos para que las **relaciones (uniones)** reflejen la lógica empresarial.
* Evite las uniones innecesarias para mantener el rendimiento de las consultas.
* Valide los resultados de la muestra antes de ejecutar extracciones a gran escala.

>[!ENDSHADEBOX]

## ¿Puedo personalizar mensajes con estos datos? {#personalization}

Sí. Puede utilizar perfiles de clientes junto con datos vinculados (como compras o suscripciones) para personalizar el contenido en todos los canales admitidos.

>[!BEGINSHADEBOX]

**Recommendations**

* Use **datos transaccionales y de comportamiento** para hacer que las ofertas sean relevantes.
* Combine **atributos estáticos** (por ejemplo, nivel de lealtad) con **atributos dinámicos** (por ejemplo, fecha de última compra).
* Mantenga la personalización concisa: la sobrecarga de mensajes con datos puede dañar la legibilidad.

>[!ENDSHADEBOX]


## ¿Se integra con otras soluciones de Adobe? {#integrations}

* **Customer Journey Analytics**: Los informes de orquestación de campaña están disponibles.
* **Real-Time CDP**: las audiencias creadas en Campaign se pueden leer en CDP.
* **Composición de audiencias federada (FAC)**: disponible como complemento.

## ¿Qué sucede con los permisos y el consentimiento? {#permissions}

Los permisos y el consentimiento se administran centralmente en Adobe Experience Platform. Las mismas reglas se aplican a todos los Recorridos y campañas orquestadas para garantizar el cumplimiento y la experiencia del cliente coherente.

>[!BEGINSHADEBOX]

**Prácticas recomendadas**

* Aplique **gobernanza centralizada**; evite administrar el consentimiento por separado en el nivel de campaña.
* Auditar periódicamente los datos de consentimiento para detectar incoherencias.
* Respete las **exclusiones específicas del canal**: no dé por hecho que el consentimiento global cubre todos los canales.

>[!ENDSHADEBOX]

## ¿Puedo realizar la segmentación ad hoc? {#ad-hoc}

Sí. Con **Segmentación en vivo**, puedes generar consultas complejas de forma inmediata y activarlas en todos los canales salientes.

>[!BEGINSHADEBOX]

**Sugerencias**

* Use la segmentación ad hoc para **necesidades con distinción de tiempo** (por ejemplo, promociones flash).
* Guarde y documente consultas útiles para que se puedan reutilizar en campañas futuras.
* Valide el recuento de audiencias antes de la activación para evitar envíos insuficientes o excesivos.

>[!ENDSHADEBOX]

## ¿Admite esto la toma de decisiones? {#decisioning}

Actualmente, la toma de decisiones no utiliza datos relacionales de campañas organizadas.

## ¿Cómo funciona la implementación en todos los entornos? {#deployment}

Los objetos creados en campañas orquestadas (por ejemplo, audiencias o flujos de trabajo) están vinculados a la zona protegida en la que se crean. Los flujos de trabajo de empaquetado e implementación estándar en entornos (desarrollo, fase, producción) no están disponibles actualmente para campañas organizadas.

>[!BEGINSHADEBOX]

**Prácticas recomendadas**

* Mantenga **zonas protegidas independientes** para la experimentación, el control de calidad y la producción.
* Documente las configuraciones exhaustivamente para permitir la replicación manual si es necesario.
* Alinee con los equipos de gobernanza para reducir la desviación de la configuración entre entornos.

>[!ENDSHADEBOX]

## ¿Existen prácticas recomendadas para ejecutar campañas a escala? {#scale}

Sí, siga las prácticas recomendadas a continuación:

* **Planifique campañas en torno a calendarios comerciales** (lanzamientos de productos, picos estacionales) para alinear volumen y recursos.
* Use **vistas previas de audiencias** antes de enviar para confirmar el tamaño esperado y evitar sorpresas.
* Siempre que sea posible, **escalone los tiempos de envío** para evitar sobrecargar los sistemas descendentes (por ejemplo, centros de llamadas, sitios web).
* Establezca una **rutina de supervisión**: haga un seguimiento de los registros de envío, las tasas de error y las exclusiones después de cada envío.
* Ejecute **análisis posterior a la campaña** en Customer Journey Analytics para restringir el direccionamiento y la orquestación para el siguiente ciclo.
