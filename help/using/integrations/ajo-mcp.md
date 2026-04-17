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
hide: true
source-git-commit: 1e42168a8eb2e5824a4054cced014b6ec57afd7f
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 1%

---

# Trabajo con clientes de MCP (Beta) {#ajo-mcp}

>[!CAUTION]
>
>**Aviso sobre la documentación de Beta:** Esta documentación cubre una función de Beta y no constituye documentación final. El contenido que se describe aquí está relacionado con una versión de Beta y está sujeto a cambios antes de su publicación general. Adobe no realiza ninguna declaración sobre la integridad o precisión de esta documentación.
>
>Al usar Adobe Journey Optimizer MCP Server (Beta) (&quot;Beta&quot;), Usted reconoce por la presente que Beta se proporciona **&quot;tal cual&quot; sin garantía de ningún tipo**. Adobe no tiene obligación de mantener, corregir, actualizar, cambiar, modificar o apoyar de otro modo Beta. Se recomienda tener precaución y no confiar en modo alguno en el correcto funcionamiento o rendimiento de dichos Beta y/o materiales de acompañamiento. Beta se considera información confidencial de Adobe. Cualquier &quot;comentario&quot; (información sobre Beta, incluidos, entre otros, problemas o defectos que encuentre al utilizar Beta, sugerencias, mejoras y recomendaciones) proporcionado por usted a Adobe se asigna a Adobe, incluidos todos los derechos, el título y el interés en y para dichos comentarios.

La integración de MCP [!DNL Adobe Journey Optimizer] le permite consultar campañas y ofertas utilizando peticiones de datos en lenguaje sencillo, sin necesidad de escribir llamadas a la API ni navegar por las pantallas de productos. Esta página explica cómo funciona la integración, qué puede hacer con ella y cómo empezar.

>[!AVAILABILITY]
>
>El servidor MCP [!DNL Adobe Journey Optimizer] está disponible actualmente solo en **Claude Web** y **Claude Desktop**. En futuras versiones se agregará compatibilidad con aplicaciones compatibles con MCP adicionales.

## ¿Qué es el protocolo de contexto del modelo? {#mcp-overview}

Los equipos de marketing y de experiencia del cliente dependen cada vez más de las aplicaciones basadas en chat y las herramientas para desarrolladores, como Anthropic Claude, OpenAI ChatGPT, Cursor y Microsoft Copilot Studio, para optimizar su trabajo diario. Estas aplicaciones admiten el **Protocolo de contexto de modelo (MCP)**, un estándar abierto que permite a las aplicaciones exponer las herramientas back-end a modelos de lenguaje de gran tamaño (LLM) de manera uniforme.

[!DNL Adobe Journey Optimizer] ahora proporciona un servidor MCP que muestra las operaciones de campaña, lealtad y espacio aislado directamente dentro de cualquier aplicación compatible con MCP. Con la integración de MCP [!DNL Adobe Journey Optimizer], distintas personas pueden colaborar en torno a los mismos datos de orquestación, sin necesidad de escribir consultas en la API de REST [!DNL Adobe Journey Optimizer] ni de navegar por varias pantallas de la interfaz de usuario. Los clientes pueden describir su intención de manera conversacional y dejar que el LLM invoque las herramientas de MCP apropiadas.

## Funcionalidades clave {#mcp-capabilities}

El servidor MCP [!DNL Adobe Journey Optimizer] le permite inspeccionar, resumir y solucionar problemas de campañas y ofertas directamente desde su asistente de IA. Todas las operaciones son **de solo lectura** — las superficies del servidor MCP recuperan las API como respuestas en lenguaje sencillo para que pueda:

<!--* **Understand journey logic** — Get a human-readable summary of any journey's branching, conditions, and actions.-->
* **Obtener visibilidad instantánea de la campaña**: pregúntele sobre los estados de campaña y las configuraciones de canal en un lenguaje sencillo y obtenga respuestas al instante, sin navegar por los menús ni extraer informes manualmente.
* **Detectar problemas al principio**: la superficie detuvo campañas, borradores huérfanos y problemas de configuración de canal en el momento en que preguntas para que tu equipo pueda actuar con rapidez.
* **Colabore en torno a datos activos**: los especialistas en marketing, los administradores de campañas y los interesados pueden consultar los mismos datos de [!DNL Adobe Journey Optimizer] activos a través de su asistente de IA, lo que facilita la alineación, la decisión y la movilidad juntas.
* **Auditar el portafolio de orquestación**: revise el estado completo de las campañas sin analizar JSON ni saltar entre las pantallas de producto.

## Herramientas disponibles {#mcp-tools}

El servidor MCP [!DNL Adobe Journey Optimizer] expone las siguientes herramientas:

| Herramienta | Descripción |
|---|---|
| **Enumerar campañas** | Examine sus [!DNL Adobe Journey Optimizer] campañas de marketing. Admite el filtrado por estado (BORRADOR, ACTIVO, DETENIDO, COMPLETADO). |
| **Obtener campaña** | Obtenga información y configuración completas para una campaña específica por ID, incluida la segmentación de audiencia, programación, canal y configuración de contenido. |
| **Enumerar configuraciones de canal** | Vea los ajustes preestablecidos de superficie y la configuración de marca de los canales de correo electrónico, SMS, push o WhatsApp. |

>[!NOTE]
>
>Todas las herramientas son de solo lectura. Las operaciones de escritura (creación, actualización o eliminación de objetos) no se admiten en la versión actual de Beta.

## Casos de uso {#mcp-use-cases}

Los siguientes ejemplos muestran cómo interactuar con el servidor MCP [!DNL Adobe Journey Optimizer] mediante lenguaje natural:

| Objetivo | Mensaje de ejemplo |
|---|---|
| **Descripción general de la campaña** | &quot;Mostrar todas mis campañas de AJO&quot; / &quot;¿Cuántas campañas están configuradas en AJO?&quot; |
| **Auditoría de estado** | &quot;¿Qué campañas están activas actualmente?&quot; / &quot;Enumerar cualquier campaña en pausa o detenida&quot;. |
| **Detalles de la campaña** | &quot;Obtener todos los detalles de la campaña [ID]&quot; / &quot;Guíame por todo lo configurado en la campaña [ID]&quot;.&quot; |
| **Audiencia y segmentación** | &quot;¿A qué audiencia se dirige la campaña [ID]?&quot; / &quot;¿Qué reglas de elegibilidad se establecen en la campaña [ID]?&quot; |
| **Programación y horario** | &quot;¿Cuándo está programado que se ejecute la campaña [ID]?&quot; / &quot;¿Es la campaña [ID] un envío único o recurrente?&quot; |
| **Resolución de problemas** | &quot;¿Por qué no se está enviando la campaña [ID]?&quot; / &quot;Revise la configuración de la campaña [ID] para ver si hay algún problema&quot;. |
| **Configuración de canal** | &quot;¿Qué ajustes preestablecidos de canal hay disponibles en mi zona protegida?&quot; / &quot;Mostrarme todas mis configuraciones de canal de correo electrónico&quot;. |
| **Auditoría de canal** | &quot;¿Qué configuraciones de canal faltan o están incompletas?&quot; / &quot;¿Cuántas configuraciones de canal tengo en todos los canales?&quot; |

## Requisitos previos {#mcp-prerequisites}

Antes de conectar el servidor MCP [!DNL Adobe Journey Optimizer] a su cliente MCP, asegúrese de lo siguiente:

* Tiene una licencia de [!DNL Adobe Journey Optimizer] activa.
* Tiene acceso a una aplicación compatible con MCP (actualmente Claude Web o Claude Desktop).
* Tiene los permisos necesarios en [!DNL Adobe Journey Optimizer] para ver campañas y ofertas.

## Conectar el servidor MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Esta integración se realiza en Beta. Los pasos de configuración detallados se publicarán cuando lleguen a la disponibilidad general. Póngase en contacto con su representante de Adobe para solicitar acceso anticipado y recibir instrucciones de configuración.

Durante la fase de Beta, su representante de Adobe le proporcionará lo siguiente:

* La dirección URL del extremo del servidor MCP específica de su organización.
* Credenciales de autenticación para conectar su asistente de IA a [!DNL Adobe Journey Optimizer].
* Directrices sobre la configuración del servidor MCP en Claude Desktop o Claude Web.

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## Limitaciones conocidas (Beta) {#mcp-limitations}

Las siguientes limitaciones se aplican a la versión actual de Beta del servidor MCP [!DNL Adobe Journey Optimizer]:

| Limitación | Descripción | Solución alternativa |
|---|---|---|
| **Sin métricas de participación o rendimiento** | El servidor MCP no expone datos de informes. Las herramientas no devuelven impresiones, tasas de pulsaciones, conversiones ni estadísticas de envío. | Utilice la interfaz de usuario de informes de AJO, CJA MCP o Adobe Analytics MCP para las métricas. El servicio de consultas de AEP puede consultar datos de evento sin procesar mediante el ID de ejecución de campaña. |
| **La paginación de la lista de campañas está limitada** | `List Campaigns` siempre devuelve la primera página de resultados (hasta 50 campañas, ordenadas alfabéticamente). Los valores de desplazamiento y límite no se aplican, lo que hace que la enumeración completa sea poco práctica para las zonas protegidas grandes. | Use `Get Campaign` directamente si se conoce el nombre o el ID de la campaña. Utilice la interfaz de usuario de AJO para examinar y filtrar la lista completa. |
| **Sin filtrado del lado del servidor por fecha, canal o programación** | `List Campaigns` solo admite el filtrado por estado. El filtrado por fecha de publicación, fecha de programación, canal o tipo de campaña no está disponible en el lado del servidor. | Utilice la lista de campañas de la IU de AJO, que admite el filtrado nativo de fechas y canales. |
| **Recuperación de contenido de mensaje no disponible** | La herramienta de contenido del mensaje devuelve HTTP 502 para todos los tipos de canales (correo electrónico, basado en código y otros). Message HTML, las líneas de asunto, los tokens de personalización y el contenido de las ofertas no se pueden recuperar mediante MCP. | Vea el contenido del mensaje y los tokens de personalización directamente en la interfaz de usuario de AJO en **Campañas > [Campaña] > Contenido**. |

## Preguntas frecuentes {#mcp-faq}

+++¿Qué clientes MCP son compatibles?

El servidor MCP [!DNL Adobe Journey Optimizer] está disponible actualmente para **Claude Web** y **Claude Desktop**. En futuras versiones se puede agregar compatibilidad con aplicaciones compatibles con MCP adicionales.
+++

+++¿A qué objetos de [!DNL Adobe Journey Optimizer] puedo acceder a través de MCP?

Puede acceder a campañas, ofertas, datos de fidelidad e información de la zona protegida. Las operaciones son de solo lectura (recuperar API); las operaciones de escritura no son compatibles con la versión actual.
+++

+++¿Necesito acceso de desarrollador para usar el servidor MCP [!DNL Adobe Journey Optimizer]?

No. El servidor MCP está diseñado tanto para personalidades técnicas como de marketing. Los especialistas en marketing pueden interactuar con él mediante peticiones de datos en lenguaje natural en cualquier cliente de MCP admitido, mientras que los desarrolladores también pueden utilizarlo en herramientas para desarrolladores compatibles con MCP.
+++

+++¿Se envían mis datos al proveedor del cliente de MCP?

Cuando envía una solicitud, el cliente MCP puede enviar contexto relevante (incluidos [!DNL Adobe Journey Optimizer] datos devueltos por el servidor MCP) a su modelo para su procesamiento. Revise las políticas de privacidad y administración de datos de su proveedor de cliente MCP antes de conectarse a los datos de producción.
+++

+++¿Qué permisos necesito en [!DNL Adobe Journey Optimizer]?

Se necesitan al menos **Ver** permisos para los objetos que desea consultar: campañas u ofertas. No se requieren permisos de escritura porque el servidor MCP solo realiza operaciones de lectura. Póngase en contacto con el administrador de [!DNL Adobe Journey Optimizer] si no está seguro del nivel de acceso actual.
+++

+++¿Puedo utilizar el servidor MCP en entornos de espacio aislado?

Sí. El servidor MCP respeta la configuración de su zona protegida [!DNL Adobe Journey Optimizer]. Puede consultar datos específicos de la zona protegida especificando la zona protegida en la solicitud o conectándose con credenciales con ámbito de una zona protegida en particular.
+++
