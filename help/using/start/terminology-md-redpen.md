---
solution: Journey Optimizer
product: journey optimizer
title: Terminología clave
description: Terminología clave en AJO
feature: Get Started
role: Admin, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: d4c968d2-5eae-4fff-9b67-427ac9d9d74c
hide: true
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 2%

---

# Terminología

Le damos la bienvenida a la guía terminológica de Adobe Journey Optimizer. Este recurso proporciona definiciones claras y directas de los términos clave que se encuentran al utilizar la plataforma. La comprensión de estos términos le ayuda a navegar por Adobe Journey Optimizer con seguridad, implementar estrategias de marketing de forma eficaz y colaborar de forma eficaz con los integrantes del equipo y con el servicio de asistencia de Adobe.

## Términos de la plataforma principal

| Término | Definición |
|------|------------|
| **Adobe Journey Optimizer (AJO)** | Herramienta que le permite crear y enviar mensajes personalizados a los clientes entre canales, como correo electrónico, mensajes de texto y notificaciones de aplicaciones móviles. Permite diseñar recorridos de clientes que respondan a las acciones de los clientes en tiempo real. Por ejemplo, un déclencheur de confirmación por correo electrónico se produce inmediatamente después de que un cliente realice una compra en el sitio web. |
| **Adobe Experience Platform (AEP)** | La base de Adobe Journey Optimizer. Recopila y organiza todos los datos de los clientes en un solo lugar, creando perfiles de clientes completos que Adobe Journey Optimizer utiliza para enviar mensajes personalizados. Considere AEP como el centro que impulsa las estrategias de participación de los clientes. |
| **espacio aislado** | Espacio de trabajo independiente en el que probar y experimentar sin afectar a las comunicaciones con los clientes en directo. Una zona protegida funciona como un área de práctica o entorno de prueba. Adobe Journey Optimizer proporciona hasta cinco zonas protegidas, lo que permite a los equipos probar escenarios como recorridos de incorporación o campañas promocionales. |

## Términos de recorrido y campaña

| Término | Definición |
|------|------------|
| **Recorrido** | Una serie de pasos conectados que guían a los clientes a través de las experiencias con su marca. Por ejemplo, un recorrido de bienvenida incluye un correo electrónico de bienvenida, un recordatorio de descarga de la aplicación y recomendaciones de productos personalizadas. Cada paso se produce después de que se complete el anterior, lo que permite interacciones secuenciales y personalizadas. |
| **Campaign** | Una sola comunicación o un conjunto de comunicaciones idénticas enviadas a un grupo específico de clientes al mismo tiempo. A diferencia de los recorridos, que se desarrollan con el tiempo, las campañas envían mensajes simultáneamente, ya sea de inmediato o a una hora programada. Por ejemplo, puede programar una campaña de correo electrónico promocional para una venta de fin de semana. |
| **Canal** | El método utilizado para comunicarse con los clientes, como correo electrónico, mensajes de texto (SMS), notificaciones push (alertas de aplicaciones móviles), mensajes en la aplicación o sitios web. Cada canal requiere una configuración específica, como verificar un dominio de correo electrónico o conectar un proveedor de SMS. |
| **Mensaje** | El contenido enviado a los clientes, incluidos texto, imágenes y elementos personalizados. Puede crear mensajes para varios formatos, como correos electrónicos, mensajes de texto y notificaciones push. Por ejemplo, un mensaje podría ser un correo electrónico de &quot;agradecimiento&quot; con nombres de clientes y detalles de pedidos insertados dinámicamente. |
| **Evento** | Ocurrencia que déclencheur o avanza un recorrido. Los eventos incluyen acciones del cliente, como realizar una compra, o eventos del sistema, como el registro de un nuevo cliente. Los eventos permiten a los recorridos responder a las acciones de los clientes en tiempo real. Por ejemplo, el cumpleaños de un cliente genera un déclencheur para recibir un correo electrónico de descuento especial. |

## Términos de cliente y audiencia

| Término | Definición |
|------|------------|
| **Perfil** | Una vista completa de cada cliente que combina información como detalles de contacto, historial de compras, preferencias y comportamientos. Un &quot;perfil atractivo&quot; se refiere a un cliente contactado mediante Adobe Journey Optimizer en los últimos 12 meses. Los perfiles son esenciales para crear experiencias personalizadas basadas en datos. |
| **Audiencia** | Grupo de clientes que comparten características o comportamientos comunes. Por ejemplo, &quot;clientes que compraron en los últimos 30 días&quot; o &quot;clientes interesados en productos de exterior&quot;. Las audiencias se crean en Adobe Experience Platform y se utilizan en Adobe Journey Optimizer para segmentar segmentos específicos. |
| **Calificación de audiencias** | Proceso que se produce cuando un cliente se une a una audiencia o la abandona. Adobe Journey Optimizer déclencheur las acciones automáticamente cuando alguien entra o sale de una audiencia. Por ejemplo, envía un mensaje de bienvenida a los nuevos miembros del programa de fidelidad, lo que garantiza comunicaciones oportunas y relevantes. |
| **Audiencia a la que se puede dirigir** | Número total de perfiles de clientes a los que puede llegar potencialmente. Su cuenta permite una audiencia direccionable que es un 25 % más grande que la audiencia atractiva contratada, lo que proporciona flexibilidad a medida que aumenta su base de clientes. |
| **Audiencia atractiva** | El número de clientes con los que se comunica activamente a través de Adobe Journey Optimizer en función de su contrato. Esto garantiza que se mantenga dentro de los límites de las licencias y que, al mismo tiempo, se centre en interacciones de alto valor. |
| **Definición de segmento** | Las reglas que determinan qué clientes pertenecen a una audiencia. Estas reglas se basan en atributos, comportamientos u otros criterios. Por ejemplo, una definición de segmento podría incluir &quot;clientes que gastaron más de 500 dólares en los últimos seis meses&quot;. |

## Términos de gestión de decisiones

| Término | Definición |
|------|------------|
| **Gestión de decisiones** | Característica que selecciona automáticamente el mejor contenido u oferta para cada cliente. Por ejemplo, recomienda una oferta de envío gratuito para un cliente que abandone con frecuencia el carro de compras. Esto garantiza interacciones personalizadas y relevantes. |
| **Oferta** | Un mensaje de marketing o una promoción específicos presentados a los clientes. Algunos ejemplos son un descuento del 20 %, una oferta de envío gratuito o una recomendación de producto. Adobe Journey Optimizer incluye hasta 10 ofertas por correo electrónico, lo que permite contenido diverso y personalizado. |
| **API de decisiones** | Una conexión técnica que permite a otros sistemas preguntar a Adobe Journey Optimizer: &quot;¿Cuál es la mejor oferta para este cliente en este momento?&quot; La oferta seleccionada se muestra en sitios web, aplicaciones u otros canales. Esta integración amplía las capacidades de Journey Optimizer más allá del correo electrónico y los SMS. |
| **Biblioteca de ofertas** | Una colección centralizada en la que se almacenan y administran todas las ofertas de marketing. Esto garantiza la coherencia en todos los canales y simplifica las actualizaciones de las estrategias promocionales. |
| **Reglas de elegibilidad** | Condiciones que determinan si un cliente puede recibir una oferta determinada. Por ejemplo: &quot;Mostrar solo este descuento a los clientes que no hayan realizado compras en 60 días&quot;. Estas reglas ayudan a evitar mensajes excesivos u ofertas irrelevantes. |

## Datos y términos técnicos

| Término | Definición |
|------|------------|
| **Zona de aterrizaje de datos** | Área de almacenamiento temporal en la que se colocan los archivos de datos antes de trasladarlos a Adobe Experience Platform. Considérela un área de ensayo para los datos. Por ejemplo, aquí se carga un archivo CSV de transacciones de clientes antes de integrarlo en el sistema. |
| **Servicio de consultas** | Herramienta que permite ejecutar consultas de estilo base de datos para validar datos después de importarlos en Adobe Journey Optimizer. Por ejemplo, consulta &quot;¿Cuántos clientes se registraron la semana pasada?&quot; para garantizar la precisión de la segmentación de audiencia. |
| **Atributo calculado** | Una característica del cliente calculada a partir de su comportamiento. Por ejemplo, &quot;valor de compra promedio&quot; o &quot;visitas totales al sitio web este mes&quot;. Estos atributos le ayudan a personalizar mensajes en función de patrones de clientes, como dirigirse a clientes de alto valor con ofertas exclusivas. |
| **Campos de personalización** | Marcadores de posición en mensajes que se sustituyen por información específica del cliente, como el nombre, las compras recientes o el nivel de pertenencia. Adobe Journey Optimizer admite hasta cinco campos de personalización por mensaje. Por ejemplo: &quot;Hola [Nombre], ¡su reciente compra de [Nombre de producto] está en camino!&quot; |
| **Esquema** | Modelo que define cómo se organizan los datos del cliente. Asigna los tipos de información almacenados y sus relaciones. Un esquema claro garantiza una integración perfecta y un uso preciso de los datos en todos los flujos de trabajo. |
| **Conjunto de datos** | Recopilación de datos relacionados organizados según un esquema. Por ejemplo: puede tener conjuntos de datos independientes para el historial de compras, la actividad del sitio web y las interacciones con el servicio de atención al cliente. Estos conjuntos de datos le permiten analizar y actuar en diferentes aspectos del comportamiento de los clientes. |

## Términos de contenido y recursos

| Término | Definición |
|------|------------|
| **Asistente de IA** | Característica integrada que utiliza inteligencia artificial para ayudar a crear contenido. Genera texto, diseña correos electrónicos o crea variaciones de mensajes para diferentes canales. Por ejemplo, le pide que redacte un correo electrónico promocional basado en las preferencias de audiencia. |
| **Assets Essentials** | Una biblioteca incluida con Adobe Journey Optimizer para almacenar y administrar archivos digitales, como imágenes, logotipos y documentos. Incluye almacenamiento para recursos de marketing y admite hasta cinco usuarios con permisos completos y 100 usuarios con acceso de visualización. Esto simplifica la colaboración y garantiza la coherencia de la marca. |
| **Fragmento de contenido** | Un fragmento de contenido reutilizable utilizado en varios mensajes. Por ejemplo, un pie de página estándar con información de contacto que aparece en todos los correos electrónicos. Esto garantiza la coherencia y reduce el tiempo empleado en recrear elementos compartidos. |
| **Plantilla** | Un diseño de mensaje prediseñado personalizado con contenido específico. Las plantillas ayudan a mantener una apariencia coherente en todas las comunicaciones, como los diseños de correo electrónico de marca o los formatos SMS. |

## Términos de Reporting &amp; Analysis

| Término | Definición |
|------|------------|
| **Informe global** | Una descripción general completa que muestra el rendimiento de todos los recorridos y campañas. Le ayuda a comprender las tendencias en las tasas de participación en todos los canales y a evaluar la eficacia de marketing general. |
| **Informe en vivo** | Datos en tiempo real sobre recorridos y campañas en ejecución. Esto permite realizar ajustes inmediatos si es necesario. Por ejemplo, pone en pausa una campaña con baja participación y revisa su mensajería. |
| **Informe de Recorridos** | Perspectivas de rendimiento detalladas de un recorrido específico. Muestra cómo se mueven los clientes en cada paso e identifica dónde podrían dejar. Esto ayuda a optimizar las experiencias de los clientes. |
| **Informe de mensajes** | Estadísticas sobre un mensaje específico, como cuántos se entregaron, abrieron y pulsaron. Esta información ayuda a refinar las comunicaciones futuras al mostrar la eficacia con la que los clientes responden al contenido. |

## Documentación relacionada

* [Introducción a Adobe Journey Optimizer](get-started.md)
* [Arquitectura y conceptos](architecture-concepts-redpen.md)
* [Guía de áreas funcionales](functional-areas-redpen.md)
