---
solution: Journey Optimizer
product: journey optimizer
title: Trabajar con clientes de MCP
description: Obtenga información sobre cómo conectar Adobe Journey Optimizer a clientes MCP mediante el servidor MCP
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 7ae497e7a0e4d1652413a5a6dbd5d617a3ec31fe
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 1%

---

# Trabajar con clientes de MCP {#ajo-mcp}

>[!AVAILABILITY]
>
>El servidor MCP [!DNL Adobe Journey Optimizer] está disponible actualmente solo en **Claude Web** y **Claude Desktop**. En futuras versiones se agregará compatibilidad con aplicaciones compatibles con MCP adicionales.

La integración de MCP [!DNL Adobe Journey Optimizer] le permite consultar campañas, recorridos y ofertas utilizando peticiones de datos en lenguaje sencillo, sin necesidad de escribir llamadas a la API ni navegar por las pantallas de productos. Esta página explica cómo funciona la integración, qué puede hacer con ella y cómo empezar.

## ¿Qué es el protocolo de contexto del modelo? {#mcp-overview}

Los equipos de marketing y de experiencia del cliente dependen cada vez más de las aplicaciones basadas en chat y las herramientas para desarrolladores, como Anthropic Claude, OpenAI ChatGPT, Cursor y Microsoft Copilot Studio, para optimizar su trabajo diario. Estas aplicaciones admiten el **Protocolo de contexto de modelo (MCP)**, un estándar abierto que permite a las aplicaciones exponer las herramientas back-end a modelos de lenguaje de gran tamaño (LLM) de manera uniforme.

[!DNL Adobe Journey Optimizer] ahora proporciona un servidor MCP que muestra las operaciones de campaña, recorrido, lealtad y espacio aislado directamente dentro de cualquier aplicación compatible con MCP. Con la integración de MCP [!DNL Adobe Journey Optimizer], distintas personas pueden colaborar en torno a los mismos datos de orquestación, sin necesidad de escribir consultas en la API de REST [!DNL Adobe Journey Optimizer] ni de navegar por varias pantallas de la interfaz de usuario. Los clientes pueden describir su intención de manera conversacional y dejar que el LLM invoque las herramientas de MCP apropiadas.

## Funcionalidades clave {#mcp-capabilities}

El servidor MCP [!DNL Adobe Journey Optimizer] le permite inspeccionar, resumir y solucionar problemas de recorridos, campañas y ofertas directamente desde su asistente de IA. Todas las operaciones son **de solo lectura** — las superficies del servidor MCP recuperan las API como respuestas en lenguaje sencillo para que pueda:

* **Comprender la lógica de recorrido**: obtenga un resumen legible en lenguaje natural de las ramas, condiciones y acciones de cualquier recorrido.
* **Comprobar la preparación de la campaña**: identifique los bloqueadores que impiden la publicación de una campaña.
* **Espacios de cobertura puntual**: vea qué canales se cubren en sus recorridos y campañas en directo y dónde existen espacios.
* **Auditar el portafolio de orquestación**: revise el estado completo de las campañas y recorridos sin analizar JSON ni saltar entre las pantallas de productos.

## Casos de uso {#mcp-use-cases}

Los siguientes ejemplos muestran cómo interactuar con el servidor MCP [!DNL Adobe Journey Optimizer] mediante lenguaje natural:

| Objetivo | Mensaje de ejemplo |
|---|---|
| **Resumir detalles de la campaña** | &quot;Obtenga la campaña cmp456 y resuma la audiencia, la programación, el estado y los paquetes&quot;. |
| **Auditoría de inventario y estado** | &quot;¿Qué tenemos y en qué estado está? Mostrar los recuentos en directo frente a los recuentos en borrador frente a los recuentos completados/detenidos/archivados de las campañas.&quot; |
| **Comprobar preparación de publicación** | &quot;¿Por qué la campaña cmp456 no está lista para publicar? Muéstrame los bloqueadores&quot;. |
| **Comparar objetos** | &quot;Comparar las campañas abc123 y xyz789: ¿qué ha cambiado en estado y programación?&quot; |
| **Auditar su portafolio** | &quot;En todos los recorridos y campañas en directo, ¿qué canales se cubren y dónde están los huecos?&quot; |
| **Cobertura y mezcla de canales** | &quot;Muestra el impacto de canal en los recorridos, las campañas y las ubicaciones de ofertas: uso de solo correo electrónico frente a multicanal, push/SMS/en la aplicación y discrepancias entre los canales de recorrido&quot;. |

## Requisitos previos {#mcp-prerequisites}

Antes de conectar el servidor MCP [!DNL Adobe Journey Optimizer] a su cliente MCP, asegúrese de lo siguiente:

* Tiene una licencia de [!DNL Adobe Journey Optimizer] activa.
* Tiene acceso a una aplicación compatible con MCP (actualmente Claude Web o Claude Desktop).
* Tiene los permisos necesarios en [!DNL Adobe Journey Optimizer] para ver campañas, recorridos y ofertas.

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

## Preguntas frecuentes {#mcp-faq}

+++¿Qué clientes MCP son compatibles?

El servidor MCP [!DNL Adobe Journey Optimizer] está disponible actualmente para **Claude Web** y **Claude Desktop**. En futuras versiones se puede agregar compatibilidad con aplicaciones compatibles con MCP adicionales.
+++

+++¿A qué objetos de [!DNL Adobe Journey Optimizer] puedo acceder a través de MCP?

Puede acceder a campañas, recorridos, ofertas, datos de fidelidad e información de la zona protegida. Las operaciones son de solo lectura (recuperar API); las operaciones de escritura no son compatibles con la versión actual.
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
