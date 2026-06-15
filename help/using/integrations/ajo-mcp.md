---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con clientes de MCP (Beta)
description: Obtenga información sobre cómo conectar Adobe Journey Optimizer a clientes MCP mediante el servidor MCP
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 7ced44f92f816d83d9a9ad667b4322dcb5930741
workflow-type: tm+mt
source-wordcount: 1369
ht-degree: 1%

---

# Trabajar con clientes de MCP {#ajo-mcp}

>[!BEGINSHADEBOX]

**En esta página:** Obtenga información general paso a paso del servidor MCP [!DNL Adobe Journey Optimizer], desde los conceptos básicos del Protocolo de contexto de modelo y los clientes admitidos, hasta las herramientas disponibles, las solicitudes de ejemplo, los requisitos previos de configuración, los pasos de conexión y las respuestas a preguntas comunes.

>[!ENDSHADEBOX]

La integración de MCP [!DNL Adobe Journey Optimizer] le permite consultar campañas, recorridos y ofertas utilizando peticiones de datos en lenguaje sencillo, sin necesidad de escribir llamadas a la API ni navegar por las pantallas de productos. Esta página explica cómo funciona la integración, qué puede hacer con ella y cómo empezar.

>[!AVAILABILITY]
>
>El servidor MCP [!DNL Adobe Journey Optimizer] está disponible actualmente en **Claude Web**, **Claude Desktop** y **Cursor**. En futuras versiones se agregará compatibilidad con aplicaciones compatibles con MCP adicionales.

## Beta, seguridad y avisos legales {#mcp-notices}

**Aviso sobre la documentación de Beta:** Esta documentación cubre una función de Beta y no constituye documentación final. El contenido que se describe aquí está relacionado con una versión de Beta y está sujeto a cambios antes de su publicación general. Adobe no realiza ninguna declaración sobre la integridad o precisión de esta documentación.

Al usar Adobe Journey Optimizer MCP Server (Beta) (&quot;Beta&quot;), Usted reconoce por la presente que Beta se proporciona **&quot;tal cual&quot; sin garantía de ningún tipo**. Adobe no tiene obligación de mantener, corregir, actualizar, cambiar, modificar o apoyar de otro modo Beta. Se recomienda tener precaución y no confiar en modo alguno en el correcto funcionamiento o rendimiento de dichos Beta y/o materiales de acompañamiento. Beta se considera información confidencial de Adobe. Cualquier &quot;comentario&quot; (información sobre Beta, incluidos, entre otros, problemas o defectos que encuentre al utilizar Beta, sugerencias, mejoras y recomendaciones) proporcionado por usted a Adobe se asigna a Adobe, incluidos todos los derechos, el título y el interés en y para dichos comentarios.

>[!WARNING]
>
>El Modelo de Protocolo de Contexto (MCP) es un estándar de código abierto emergente y puede presentar riesgos de seguridad o fiabilidad. Las integraciones del servidor de Adobe MCP y la documentación relacionada se proporcionan &quot;tal cual&quot;, sin garantías de ningún tipo.
>
>La conexión de clientes o servidores MCP a productos de Adobe es una configuración seleccionada por el cliente. Los clientes son responsables de evaluar la seguridad y la idoneidad de cualquier integración de MCP. Adobe no se responsabiliza de los problemas que se deriven de una configuración incorrecta, un uso incorrecto del MCP, vulnerabilidades en implementaciones de terceros o acciones no deseadas realizadas a través de flujos de trabajo habilitados para MCP.
>
>Para reducir el riesgo, Adobe recomienda probar las integraciones en un entorno de zona protegida antes de usarlas de forma productiva y revisar y validar cuidadosamente todas las acciones y respuestas iniciadas por MCP antes de confirmarlas o depender de ellas.

## ¿Qué es el protocolo de contexto del modelo? {#mcp-overview}

Los equipos de marketing y de experiencia del cliente dependen cada vez más de las aplicaciones basadas en chat y las herramientas para desarrolladores, como Anthropic Claude, OpenAI ChatGPT, Cursor y Microsoft Copilot Studio, para optimizar su trabajo diario. Estas aplicaciones admiten el **Protocolo de contexto de modelo (MCP)**, un estándar abierto que permite a las aplicaciones exponer las herramientas back-end a modelos de lenguaje de gran tamaño (LLM) de manera uniforme.

[!DNL Adobe Journey Optimizer] ahora proporciona un servidor MCP que muestra las operaciones de campaña y de zona protegida directamente dentro de cualquier aplicación compatible con MCP. Con la integración de MCP [!DNL Adobe Journey Optimizer], distintas personas pueden colaborar en torno a los mismos datos de orquestación, sin necesidad de escribir consultas en la API de REST [!DNL Adobe Journey Optimizer] ni de navegar por varias pantallas de la interfaz de usuario. Los clientes pueden describir su intención de manera conversacional y dejar que el LLM invoque las herramientas de MCP apropiadas.

## Funcionalidades clave {#mcp-capabilities}

El servidor MCP de [!DNL Adobe Journey Optimizer] le permite inspeccionar, resumir y solucionar problemas de campañas, recorridos y ofertas directamente desde su asistente de IA. Todas las operaciones son **de solo lectura** — las superficies del servidor MCP recuperan las API como respuestas en lenguaje sencillo para que pueda:

* **Comprender la lógica de recorrido**: obtenga un resumen legible en lenguaje natural de las ramas, condiciones y acciones de cualquier recorrido.
* **Obtener visibilidad instantánea de la campaña**: pregúntele sobre los estados de campaña y las configuraciones de canal en un lenguaje sencillo y obtenga respuestas al instante, sin navegar por los menús ni extraer informes manualmente.
* **Detectar problemas al principio**: la superficie detuvo campañas, borradores huérfanos y problemas de configuración de canal en el momento en que preguntas para que tu equipo pueda actuar con rapidez.
* **Colabore en torno a datos activos**: los especialistas en marketing, los administradores de campañas y los interesados pueden consultar los mismos datos de [!DNL Adobe Journey Optimizer] activos a través de su asistente de IA, lo que facilita la alineación, la decisión y la movilidad juntas.
* **Auditar el portafolio de orquestación**: revise el estado completo de las campañas sin analizar JSON ni saltar entre las pantallas de producto.

## Herramientas disponibles {#mcp-tools}

El servidor MCP [!DNL Adobe Journey Optimizer] expone las siguientes herramientas:

**Herramientas de campaña**

| Herramienta | Descripción |
|---|---|
| **Enumerar campañas** | Examine sus [!DNL Adobe Journey Optimizer] campañas de marketing. Admite el filtrado por estado (BORRADOR, ACTIVO, DETENIDO, COMPLETADO). |
| **Obtener campaña** | Obtenga información y configuración completas para una campaña específica por ID, incluida la segmentación de audiencia, programación, canal y configuración de contenido. |
| **Enumerar configuraciones de canal** | Vea los ajustes preestablecidos de superficie y la configuración de marca de los canales de correo electrónico, SMS, push o WhatsApp. |

**herramientas de Recorrido**

| Herramienta | Descripción |
|---|---|
| **Obtener todos los Recorridos** | Examine todos los recorridos de su zona protegida [!DNL Adobe Journey Optimizer]. |
| **Obtener Recorrido** | Obtenga detalles completos para un recorrido específico por ID, incluidas su ramificación, condiciones y acciones. |
| **Visualice sus recorridos** | Procese los recorridos con herramientas interactivas para que pueda explorar su estructura y flujo visualmente. |

>[!NOTE]
>
>Todas las herramientas son de solo lectura. Las operaciones de escritura (creación, actualización o eliminación de objetos) no se admiten en la versión actual de Beta.

## Casos de uso {#mcp-use-cases}

Los siguientes ejemplos muestran cómo interactuar con el servidor MCP [!DNL Adobe Journey Optimizer] mediante lenguaje natural:

| Objetivo | Mensaje de ejemplo |
|---|---|
| **Descripción general de la campaña y el recorrido** | Mostrarme todas mis campañas/recorridos de Journey Optimizer / ¿Cuántas campañas/recorridos hay configuradas en Journey Optimizer? |
| **Auditoría de estado** | ¿Qué campañas/recorridos están activos actualmente? / Enumerar cualquier campaña o recorrido pausado o detenido. |
| **Detalles de campaña y recorrido** | Obtenga todos los detalles de la campaña [ID] / Guíame por todo lo configurado en la campaña [ID]. / Obtener todos los detalles del recorrido [ID] / Guíame por todo lo configurado en el recorrido [ID]. |
| **Audiencia y segmentación** | ¿A qué audiencia se dirige la campaña o el recorrido [ID]? / ¿Qué reglas de elegibilidad se establecen en la campaña o el recorrido [ID]? |
| **Programación y horario** | ¿Cuándo está programado que se ejecute la campaña [ID]? / ¿Es la campaña [ID] un envío único o recurrente? |
| **Resolución de problemas** | ¿Por qué no se está enviando la campaña [ID]? / Revise la configuración de la campaña [ID] para detectar cualquier problema. |
| **Configuración de canal** | ¿Qué ajustes preestablecidos de canal hay disponibles en mi zona protegida? / Mostrarme todas mis configuraciones de canal de correo electrónico. |
| **Auditoría de canal** | ¿Qué configuraciones de canal faltan o están incompletas? / ¿Cuántas configuraciones de canal tengo en todos los canales? |

## Requisitos previos {#mcp-prerequisites}

Antes de conectar el servidor MCP [!DNL Adobe Journey Optimizer] a su cliente MCP, asegúrese de lo siguiente:

* Tiene una licencia de [!DNL Adobe Journey Optimizer] activa.
* Tiene acceso a una aplicación compatible con MCP (actualmente Claude Web, Claude Desktop o Cursor).
* Tiene los permisos necesarios en [!DNL Adobe Journey Optimizer] para ver campañas, recorridos y ofertas.

## Conectar el servidor MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Esta integración se realiza en Beta.

Puede conectar el servidor MCP [!DNL Adobe Journey Optimizer] a través de su cliente MCP preferido, entre ellos **Claude Web**, **Claude Desktop** y **Cursor**.

**Conectar mediante un cliente MCP**

Al configurar el servidor MCP en su cliente MCP, utilice la siguiente URL de extremo de servidor:

`https://ajo-mcp.adobe.io/mcp`

**Conectar mediante Claude Web o Claude Desktop**

Para configurar el servidor MCP en Claude Web o Claude Desktop, ve a **Conectores** y selecciona **Adobe Journey Optimizer**.

## Preguntas frecuentes {#mcp-faq}

+++¿Qué clientes MCP son compatibles?

El servidor MCP [!DNL Adobe Journey Optimizer] está disponible actualmente para **Claude Web**, **Claude Desktop** y **Cursor**. En futuras versiones se puede agregar compatibilidad con aplicaciones compatibles con MCP adicionales.
+++

+++¿A qué objetos de [!DNL Adobe Journey Optimizer] puedo acceder a través de MCP?

Puede acceder a campañas, recorridos, ofertas e información de la zona protegida. Las operaciones son de solo lectura (recuperar API); las operaciones de escritura no son compatibles con la versión actual.
+++

+++¿Necesito acceso de desarrollador para usar el servidor MCP [!DNL Adobe Journey Optimizer]?

No. El servidor MCP está diseñado tanto para personalidades técnicas como de marketing. Los especialistas en marketing pueden interactuar con él mediante peticiones de datos en lenguaje natural en cualquier cliente de MCP admitido, mientras que los desarrolladores también pueden utilizarlo en herramientas para desarrolladores compatibles con MCP.
+++

+++¿Se envían mis datos al proveedor del cliente de MCP?

Cuando envía una solicitud, el cliente MCP puede enviar contexto relevante (incluidos [!DNL Adobe Journey Optimizer] datos devueltos por el servidor MCP) a su modelo para su procesamiento. Revise las políticas de privacidad y administración de datos de su proveedor de cliente MCP antes de conectarse a los datos de producción.
+++

+++¿Qué permisos necesito en [!DNL Adobe Journey Optimizer]?

Necesita al menos **permisos de vista** para los objetos que desea consultar: campañas, recorridos u ofertas. No se requieren permisos de escritura porque el servidor MCP solo realiza operaciones de lectura. Póngase en contacto con el administrador de [!DNL Adobe Journey Optimizer] si no está seguro del nivel de acceso actual.
+++

+++¿Puedo utilizar el servidor MCP en entornos de espacio aislado?

Sí. El servidor MCP respeta la configuración de su zona protegida [!DNL Adobe Journey Optimizer]. Puede consultar datos específicos de la zona protegida especificando la zona protegida en la solicitud o conectándose con credenciales con ámbito de una zona protegida en particular.
+++

