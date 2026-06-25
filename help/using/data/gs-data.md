---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a la gestión de datos en Journey Optimizer
description: Descubra cómo fluyen los datos dentro y fuera de Adobe Journey Optimizer, incluidos los conceptos clave, los pasos de configuración y las protecciones.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
TQID: https://experienceleague.adobe.com/Dq8mzkfuxvcoAPI1vjq9lFHjz4Z5j9s42-kfMy59PeI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2: id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371id: d6e5c7fd-c1d6-4137-98cd-138ccde6752fid: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 79b0c44fffb4297a9a5675200f086c5de544ec88
workflow-type: tm+mt
source-wordcount: 2696
ht-degree: 97%

---

# Introducción a la administración de datos {#about-data}

>[!BEGINSHADEBOX]

**En esta página:** obtenga información general práctica sobre cómo fluyen los datos dentro y fuera de Adobe Journey Optimizer, incluyendo esquemas, conjuntos de datos, identidades, perfiles y fuentes de datos, para que su equipo pueda completar los pasos de preparación de datos antes de crear recorridos y campañas.

>[!ENDSHADEBOX]

Los datos son la base de cada recorrido, decisión y mensaje que entrega con [!DNL Adobe Journey Optimizer].

Esta página le ofrece un punto de partida práctico para comprender lo siguiente:

* Los componentes básicos de datos utilizados por Journey Optimizer (esquemas, conjuntos de datos, identidades, perfiles)
* Cómo utiliza Journey Optimizer los datos de Adobe Experience Platform
* Qué pasos de configuración de datos debe completar su equipo antes de crear recorridos y campañas
* Dónde ir para obtener información detallada sobre la configuración y las prácticas recomendadas

Utilice esta guía junto con sus ingenieros de datos, administradores y especialistas en marketing para que todos compartan una imagen común de cómo los datos fluyen hacia y desde Journey Optimizer.

>[!TIP]
>¿No tiene experiencia en la administración de datos en Journey Optimizer? Vea el [tutorial de Introducción a la configuración de datos](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"} para una guía práctica y sencilla para principiantes acerca de los esquemas, los conjuntos de datos y las fuentes.

## Cómo utiliza Journey Optimizer los datos de Adobe Experience Platform {#aep-data}

[!DNL Adobe Journey Optimizer] se creó en [!DNL Adobe Experience Platform]. No mantiene un almacén de datos separado y aislado. En su lugar, utiliza la misma base de datos que otras [!DNL CX Enterprise] aplicaciones.

Los esquemas y conjuntos de datos se encuentran en Adobe Experience Platform. El servicio de identidad y el servicio de perfil administran las identidades y el [perfil del cliente en tiempo real](../audience/get-started-profiles.md). Journey Optimizer lee datos de perfil y evento de Adobe Experience Platform para evaluar las condiciones del recorrido, personalizar los mensajes y seleccionar ofertas. Escribe datos de interacción (como eventos de envío, apertura, clics y rechazos, y eventos de pasos de recorrido) en conjuntos de datos de Experience Platform. También puede buscar conjuntos de datos adicionales durante la ejecución sin copiar esos datos en el perfil.

>[!TIP]
>Considere Adobe Experience Platform como su capa de datos central y Journey Optimizer como una aplicación que organiza recorridos y mensajes utilizando esa base de datos compartidos.

➡️ [Más información acerca de la arquitectura de Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Conceptos clave de datos en Journey Optimizer {#key-concepts}

Al trabajar con datos en Journey Optimizer, encontrará varios conceptos relacionados. La tabla siguiente le ofrece una descripción general rápida; las secciones siguientes explican cada concepto con más detalle.

| Concepto | Qué es | Uso principal en Journey Optimizer |
|---|---|---|
| Esquema XDM | Reglas que representan, validan y dan formato a los datos (creadas a partir de una clase + grupos de campos) | Atributos de perfil de modelo y eventos de comportamiento |
| Conjunto de datos | Tabla de almacenamiento para datos que se ajustan a un esquema | Mantener datos generados por el sistema, el perfil y el evento |
| Conector de origen | Transmite o procesa por lotes datos de sistemas externos en AEP | Ingesta de datos de CRM, análisis y web |
| Fuente de datos | Expone campos AEP o externos dentro de recorridos | Condiciones del recorrido de energía y personalización de mensajes |
| Identidad | Identificador que representa de forma exclusiva a un cliente individual | Vinculación de perfiles entre canales |
| Conjunto de datos de búsqueda | Referencia en tiempo de ejecución a datos de AEP sin almacenamiento de perfil | Enriquecimiento de los mensajes con datos de referencia activos |

### Esquema (esquema XDM) {#schema}

Un esquema es un conjunto de reglas que representan, validan y dan formato a los datos. Se compone de una **clase** (que define el comportamiento base: registro o serie temporal) y **grupos de campos** opcionales (que añaden campos específicos). Los esquemas se definen utilizando los estándares del Modelo de datos de experiencia (XDM) y se activan en Adobe Experience Platform.

XDM existe para resolver un problema real: el mismo concepto (un cliente, una compra, un producto) se nombra y estructura de forma diferente en los sistemas de origen. XDM proporciona un lenguaje compartido que unifica estos conceptos en una sola definición, independientemente de dónde se originen los datos. Esto es lo que permite que Journey Optimizer funcione de forma coherente con los datos de su CRM, su sitio web, su aplicación móvil y su almacén de datos al mismo tiempo.

En Journey Optimizer, normalmente se trabaja con esquemas de **Perfil individual de XDM** para atributos del cliente (nombre, preferencias, consentimiento) y esquemas de **XDM ExperienceEvent** para eventos de comportamiento (compras, vistas de página, registros).

➡️ [Más información sobre los esquemas](get-started-schemas.md)

### Conjunto de datos {#dataset}

Un conjunto de datos es una construcción de almacenamiento y administración de datos que se ajusta a un esquema; imagíneselo como una tabla con un conjunto definido de columnas y filas. Todos los datos utilizados por Journey Optimizer se almacenan en conjuntos de datos de Adobe Experience Platform. Pueden ser conjuntos de datos de perfil (que contribuyen al Perfil del cliente en tiempo real), conjuntos de datos de evento (que almacenan datos de comportamiento para recorridos y análisis) o conjuntos de datos del sistema creados automáticamente por Journey Optimizer para el seguimiento, los comentarios y los eventos de pasos de recorrido.

➡️ [Más información acerca de los conjuntos de datos](get-started-datasets.md)

### Conector de origen {#source-connector}

Un conector de origen (también conocido como **origen**) le ayuda a introducir datos de varios sistemas, como Adobe Analytics, Adobe Experience Platform Web SDK, almacenamiento en la nube (S3, Azure Blob) o bases de datos CRM, en Adobe Experience Platform. Más allá de la ingesta sin procesar, los conectores permiten la estructuración, el etiquetado y la mejora de los datos mediante servicios de Experience Platform, incluida la asignación de campos a los esquemas XDM y el etiquetado de gobernanza de datos.

➡️ [Obtenga más información acerca de los conectores de origen](../start/get-started-sources.md)

### Fuente de datos (Journey Optimizer) {#data-source}

Una fuente de datos en Journey Optimizer define qué campos de Adobe Experience Platform (o API externas) se exponen dentro de los recorridos y mensajes. Configuradas en la interfaz de usuario de Journey Optimizer, las fuentes de datos suelen incluir la fuente de datos integrada de Adobe Experience Platform (que expone los atributos del perfil del cliente en tiempo real) y fuentes de datos externas o personalizadas opcionales a las que se llama durante el tiempo de ejecución del recorrido para un enriquecimiento adicional. Se utilizan para condiciones de recorrido, acciones personalizadas y personalización de mensajes.

➡️ [Obtenga más información acerca de las fuentes de datos](../datasource/about-data-sources.md)

>[!NOTE]
>El [Glosario de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/glossary){target="_blank"} define “fuente de datos” genéricamente como el origen de los datos (un CRM, una aplicación móvil, etc.). En Journey Optimizer, **fuente de datos** tiene un significado específico: una configuración de interfaz de usuario que controla qué campos se exponen dentro de los recorridos y mensajes.

### Identidad y perfil del cliente en tiempo real {#identity}

Una identidad es un identificador que representa de forma exclusiva a un cliente individual, como un ID de cookie, un ID de dispositivo, una dirección de correo electrónico o un ID de CRM. Las identidades se organizan en espacios de nombres (correo electrónico, ECID, CRMID) y varias identidades para la misma persona se vinculan en un gráfico de identidad unificado. El Perfil del cliente en tiempo real utiliza el gráfico para ver una vista holística de cada cliente individual combinando datos de varios canales, incluidos los canales en línea, sin conexión, CRM y de terceros.

Un concepto clave para los principiantes es el modelo **fragmento de perfil**. Cada vez que un cliente interactúa con su marca en un dispositivo o canal específico (su sitio web, aplicación móvil o tienda), esa interacción se registra como un fragmento de perfil: una vista parcial de ese cliente en función de ese punto de contacto específico. El Perfil del cliente en tiempo real vincula continuamente estos fragmentos en función de valores de identidad compartidos, lo que crea un perfil completo y actualizado. Journey Optimizer lee este perfil ensamblado para evaluar condiciones, seleccionar ofertas y personalizar mensajes en tiempo real.

➡️ [Obtenga más información sobre las identidades en Journey Optimizer](../audience/get-started-identity.md)

### Conjunto de datos de búsqueda {#lookup-dataset}

Un conjunto de datos de consulta permite a Journey Optimizer recuperar datos de referencia o transaccionales en tiempo de ejecución de un conjunto de datos de Adobe Experience Platform, sin almacenar esos datos en el perfil del cliente en tiempo real. Esto resulta útil para datos de referencia que cambian con frecuencia (precios, inventario, horas de almacenamiento) o datos transaccionales que se necesitan en el momento del mensaje pero que no pertenecen al perfil. Journey Optimizer realiza la búsqueda durante el recorrido o la ejecución del mensaje en función de una clave como un ID de producto.

➡️ [Más información acerca de los conjuntos de datos de búsqueda](lookup-aep-data.md)

## Lista de comprobación de preparación de datos {#checklist}

Antes de que los especialistas en marketing empiecen a crear recorridos y campañas, su organización debe completar un conjunto de pasos de preparación de datos. Esto garantiza que Journey Optimizer pueda utilizar los datos adecuados, en el momento adecuado y con conformidad a la normativa.

>[!NOTE]
>Los pasos siguientes implican varias funciones: ingenieros de datos, administradores y profesionales del marketing. Utilice esta lista de comprobación como plan compartido para preparar su entorno. Los pasos 1-4 se llevan a cabo en Adobe Experience Platform; los pasos 5-6 se configuran en Journey Optimizer.

Los seis pasos siguientes le guían a través del proceso completo de configuración de datos, desde la configuración de identidad hasta la verificación de que los datos fluyen correctamente a Journey Optimizer:

1. Defina su estrategia de identidad
1. Diseño de esquemas para datos de perfiles y eventos
1. Creación de conjuntos de datos habilitados para perfiles
1. Integración de datos de sus fuentes
1. Configuración de fuentes de datos en Journey Optimizer
1. Verificar conjuntos de datos de seguimiento, comentarios y recorrido

+++ Defina su estrategia de identidad

Elija una identidad principal para sus clientes (como ECID, correo electrónico o CRMID) y configure los espacios de nombres correspondientes en el servicio de identidad de Adobe Experience Platform. Asegúrese de que los campos de identidad estén presentes en los esquemas habilitados para perfiles y valide que los perfiles estén correctamente vinculados en el gráfico de identidad.

➡️ [Obtenga más información sobre las identidades en Journey Optimizer](../audience/get-started-identity.md)

+++

+++ Diseño de esquemas para datos de perfiles y eventos

Cree esquemas de **XDM Individual Profile** para capturar atributos del cliente, como información de nombre y contacto, preferencias e intereses, y la fase del ciclo vital o el estado de consentimiento. Cree **esquemas XDM ExperienceEvent** para capturar datos de comportamiento y transaccionales, como eventos web y de aplicación, compras e interacciones sin conexión. Marque los campos correctos como identidades y atributos de perfil donde corresponda.

➡️ [Más información sobre los Esquemas](get-started-schemas.md)\
➡️ [Planificación de habilitación de perfil](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"}

+++

+++ Creación de conjuntos de datos habilitados para perfiles

En Adobe Experience Platform, cree conjuntos de datos basados en los esquemas XDM y habilite Perfil en cualquier conjunto de datos que deba contribuir al Perfil del cliente en tiempo real. Confirme que los conjuntos de datos generados por el sistema y creados por Journey Optimizer estén visibles en el espacio de trabajo Conjuntos de datos.

➡️ [Más información acerca de los conjuntos de datos](get-started-datasets.md)\
➡️ [Planificación de habilitación de perfil](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"}\
➡️ [Administrar esquemas habilitados para perfiles](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"}

+++

+++ Integración de datos de sus fuentes

Configure conectores de origen para los sistemas empresariales, como los SDK web de Adobe Analytics, Adobe Experience Platform o las plataformas CRM y POS, y asigne los campos entrantes a los esquemas XDM. Compruebe que los datos aterrizan en los conjuntos de datos correctos y aparecen en el Perfil del cliente en tiempo real donde se espera.

➡️ [Obtenga más información acerca de los conectores de fuentes](../start/get-started-sources.md)

➡️ [Tutorial: Creación de conjuntos e ingesta de datos](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Configuración de fuentes de datos en Journey Optimizer

Las fuentes de datos son un concepto específico de Journey Optimizer: no se encuentran en el lugar donde se alojan los datos, sino en el que se declara qué campos puede leer Journey Optimizer durante el recorrido y la ejecución del mensaje. Antes de que un recorrido pueda evaluar una condición como “¿el cliente es un miembro del programa de fidelización?” o personalizar un mensaje con un nombre, los campos de perfil relevantes deben exponerse a través de una configuración de fuente de datos.

Journey Optimizer incluye una [fuente de datos de Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) integrada que proporciona acceso directo a los atributos del perfil del cliente en tiempo real. Esto incluye la gran mayoría de los casos de uso: lectura de atributos de perfil para la personalización o comprobación de campos de consentimiento y preferencia. También puede configurar [fuentes de datos externas](../datasource/external-data-sources.md) para que llamen a las API de terceros durante el tiempo de ejecución del recorrido; por ejemplo, para recuperar una puntuación de lealtad en tiempo real, una recomendación de producto o un nivel de inventario de tienda que no esté almacenado en Adobe Experience Platform.

>[!NOTE]
>El acceso directo a los datos de evento de experiencia a través de la fuente de datos integrada de Adobe Experience Platform está en desuso y se desactiva progresivamente. [Más información](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

La configuración de fuentes de datos es una tarea administrativa que desbloquea la capa de datos completa para los autores y profesionales de marketing del recorrido. Una vez que un campo se expone a través de una fuente de datos, está disponible en el generador de condiciones de recorrido, en los editores de personalización de mensajes y en las reglas de toma de decisiones sobre ofertas, sin necesidad de realizar ningún trabajo de ingeniería adicional en el momento de la compilación del recorrido.

➡️ [Más información acerca de la configuración de la fuente de datos](../datasource/about-data-sources.md)

+++

+++ Verificar conjuntos de datos de seguimiento, comentarios y recorrido

Confirme que los conjuntos de datos generados por el sistema de Journey Optimizer están disponibles en el espacio de trabajo Conjuntos de datos. Ejecute recorridos y campañas de prueba y, a continuación, utilice el Editor de consultas para comprobar que los eventos de envío, apertura, clic y devolución están registrados y que los eventos y estados de los pasos de recorrido se capturan correctamente. Utilice estos conjuntos de datos para la monitorización continua, la resolución de problemas y la optimización de recorridos.

➡️ [Obtenga más información sobre las consultas en Journey Optimizer](get-started-queries.md)

+++

## Consideraciones sobre barreras de seguridad y diseño de datos {#guardrails}

Algunas barreras de seguridad y limitaciones del producto pueden influir en la forma en que se diseñan el modelo de datos y los recorridos. Es conveniente revisarlas pronto para evitar tener que volver a trabajar sobre ellas más adelante.

>[!IMPORTANT]
>Consulte siempre la página [Limitaciones y barreras de seguridad de Journey Optimizer](../start/guardrails.md) para obtener la información más reciente. Los resúmenes que siguen resaltan elementos clave, pero pueden evolucionar con el tiempo.

### Conjuntos de datos del sistema de Journey Optimizer y TTL {#datasets-ttl}

Journey Optimizer crea varios conjuntos de datos generados por el sistema para el seguimiento, los comentarios y los eventos de pasos de recorrido. A partir de febrero de 2025, se está implementando una barrera de seguridad de tiempo de vida (TTL) para algunos de estos conjuntos de datos, lo que puede afectar a cuánto tiempo se retienen los datos para el análisis y la resolución de problemas.

➡️ [Obtenga más información sobre las barreras de seguridad TTL de los conjuntos de datos](datasets-ttl.md)

### Segmentación de streaming y eventos de Journey Optimizer {#streaming-segmentation}

A partir del 1 de noviembre de 2024, la segmentación de streaming ya no admite eventos de envío y apertura de conjuntos de datos de seguimiento y comentarios de Journey Optimizer. Para casos de uso como restricción de frecuencia y administración de fatiga, use [Reglas empresariales](../conflict-prioritization/rule-sets.md) en lugar de segmentos de streaming basados en eventos de envío/apertura.

➡️ [Más información sobre conjuntos de datos](get-started-datasets.md)

### Búsqueda de conjuntos de datos y toma de decisiones {#lookup-guardrails}

La búsqueda de conjuntos de datos es ideal para atributos que cambian con frecuencia (inventario, precios, tiempo) o datos que no necesitan almacenarse en el perfil del cliente en tiempo real. Revise las barreras de seguridad específicas del producto, como los límites de tamaño del conjunto de datos y los límites de consulta, en la documentación correspondiente antes de diseñar la estrategia de búsqueda.

➡️ [Más información acerca de los conjuntos de datos de búsqueda](lookup-aep-data.md)

## Ejemplo: preparación de datos para un recorrido de bienvenida {#example}

El siguiente ejemplo muestra cómo los conceptos de esta página funcionan juntos en un escenario simple.

1. Un ingeniero de datos crea un [esquema de perfil individual de XDM](get-started-schemas.md) para atributos del cliente (nombre, correo electrónico, nivel de lealtad, consentimiento) y un esquema XDM ExperienceEvent para eventos de registro web.
1. [Se crean conjuntos de datos habilitados para perfiles](get-started-datasets.md) para cada esquema: uno para atributos CRM y otro para eventos de registro.
1. Los equipos móviles y web transmiten eventos de registro a través de los SDK web de Adobe Experience Platform; los datos de CRM se incorporan mediante un [conector de origen](../start/get-started-sources.md).
1. Un administrador configura la [fuente de datos de Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) en Journey Optimizer y expone campos como `profile.person.name.firstName`, `profile.personalEmail.address` y `profile.loyaltyTier`.
1. Un experto en marketing [crea un recorrido de bienvenida](../building-journeys/journey-gs.md) que escucha un evento de registro y usa esos atributos de perfil para [personalizar el correo electrónico de bienvenida](../personalization/personalize.md). Journey Optimizer escribe eventos de envío y apertura para rastrear conjuntos de datos y registros del progreso del recorrido en conjuntos de datos de eventos de paso de recorrido.
1. Un desarrollador usa el [Editor de consultas](get-started-queries.md) para comprobar que los eventos fluyen correctamente y analizar el rendimiento (aperturas, clics, tiempo de envío). El equipo ajusta el recorrido y el contenido en función de estas perspectivas.

Este flujo ilustra cómo los esquemas, conjuntos de datos, fuentes, fuentes de datos y consultas funcionan juntos en un caso de uso completo y fácil de usar para principiantes.

## Recursos relacionados {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Introducción a los esquemas**

Aprenda a crear esquemas XDM en Adobe Experience Platform, elegir la clase y los grupos de campos adecuados y modelar los atributos de perfil y los eventos de comportamiento.

[Más información](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Trabajar con conjuntos de datos**

Obtenga información sobre cómo crear conjuntos de datos de evento y habilitados para perfiles, monitorizar la ingesta de datos y explorar los conjuntos de datos generados por el sistema que Journey Optimizer crea automáticamente para el seguimiento, los comentarios y los eventos de pasos de recorrido.

[Más información](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Configuración de fuentes de datos**

Instrucciones paso a paso sobre la configuración de la fuente de datos integrada de Adobe Experience Platform y las fuentes de datos externas opcionales para exponer los campos de perfil y las respuestas de API externas dentro de los recorridos.

[Más información](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Uso de datos de Adobe Experience Platform**

Descubra cómo enriquecer mensajes en tiempo de ejecución con datos de referencia o transaccionales de conjuntos de datos de AEP, sin almacenar esos datos en el perfil del cliente en tiempo real.

[Más información](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Introducción a las consultas**

Utilice el servicio de consultas para analizar conjuntos de datos de Journey Optimizer, comprobar que los eventos fluyen correctamente y crear consultas de informes sobre los datos de envío, apertura, clics y rechazos.

[Más información](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Introducción a los perfiles**

Explore cómo funciona el perfil del cliente en tiempo real en Journey Optimizer y cómo examinar, inspeccionar y validar perfiles de clientes individuales en la interfaz de usuario de Platform.

[Más información](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Configuración de datos: información general**

Un tutorial en vídeo para principiantes de la configuración de datos en Journey Optimizer, que cubre esquemas, conjuntos de datos y fuentes de principio a fin.

[Ver tutorial](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Creación de conjuntos e ingesta de datos**

Un tutorial práctico que muestra cómo crear conjuntos de datos en Adobe Experience Platform e ingerir datos mediante conectores de origen, con instrucciones paso a paso que puede seguir en su propia zona protegida.

[Ver tutorial](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
