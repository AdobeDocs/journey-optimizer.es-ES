---
solution: Journey Optimizer
product: journey optimizer
title: Áreas funcionales
description: Áreas funcionales en AJO
feature: Get Started
role: Admin, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: c9b02ae2-e07b-41f4-90cc-b2c0966f1ed1
hide: true
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Conceptos principales

Adobe Journey Optimizer (AJO) incluye varias áreas funcionales clave que funcionan juntas sin problemas. En esta guía se explica cada área y se describe cómo se combinan estas áreas para crear experiencias de cliente impactantes. Comprender estas áreas funcionales garantiza que puede aprovechar AJO para ofrecer experiencias personalizadas y omnicanal de forma eficaz.

## Información general sobre áreas funcionales

| Área funcional | Beneficio principal | Analogía |
|-------------------------|--------------------------------------------------|------------------------|
| Administración de datos | Organizar los datos de clientes adecuados | La base |
| Administración de clientes | Comprenda quiénes son sus clientes | Conozca su audiencia |
| Administración de contenido | Crear y administrar mensajes coherentes y personalizados | Diseñar el mensaje |
| Gestión de decisiones | Seleccione el mejor mensaje/oferta en tiempo real | Los cerebros |
| Administración de recorridos | Diseñe y automatice experiencias de cliente sin problemas | Director de orquesta |
| Conexiones | Conexión de fuentes de datos y entrega a través de canales de cliente | Las tuberías |
| Administración y privacidad | Controle la configuración, acceda y garantice el cumplimiento de los datos | El libro de reglas |

## Áreas funcionales detalladas

### Administración de datos: The Foundation

**Propósito**: ingerir, estructurar y administrar los datos que alimentan la personalización. Este proceso incluye la definición de estructuras de datos (esquemas), la creación de contenedores de almacenamiento (conjuntos de datos) y la importación de datos de varios sistemas.

Considere la administración de datos como la base de toda la participación de los clientes. Una base de datos bien estructurada garantiza que cada decisión, mensaje y recorrido utilice información precisa y organizada.

**Componentes clave**:

- **Creación y administración de esquemas**: defina la estructura de los datos del cliente.
   - Ejemplo: Crear un esquema que esquematice campos como &quot;Nombre&quot;, &quot;Dirección de correo electrónico&quot; e &quot;Historial de compras&quot;.
- **Configuración del conjunto de datos**: organice los datos en contenedores lógicos.
   - Ejemplo: Agrupar datos de transacciones en un conjunto de datos &quot;Transacciones de ventas&quot; para facilitar el análisis.
- **Flujos de trabajo de ingesta de datos**: importe datos en la plataforma de forma eficaz.
   - Ejemplo: utilice conectores de Source creados previamente para importar datos de clientes desde un sistema de administración de la relación con los clientes (CRM).
- **Herramientas de calidad de datos**: mantenga la precisión y la integridad de los datos.

**Beneficio**: garantiza que los datos de los clientes sean confiables, estén organizados y sean accesibles, lo que sentará las bases para todas las actividades de AJO. Los conectores de Source creados previamente optimizan la ingesta de datos desde plataformas comunes.



### Administración de clientes: conocer a su audiencia

**Propósito**: generar y mantener una comprensión profunda de cada cliente. Esto implica utilizar el Perfil del cliente en tiempo real de Adobe Experience Platform (AEP) para combinar datos de todos los puntos de contacto en una vista unificada. También administra las identidades en dispositivos y canales, lo que permite agrupar personas en audiencias segmentables en función de atributos o comportamientos compartidos.

Las herramientas de administración de clientes conectan puntos de datos dispares para proporcionar una imagen coherente de cada cliente. Esta comprensión garantiza que pueda ofrecer experiencias relevantes y personalizadas.

**Componentes clave**:

- **Perfil del cliente en tiempo real**: vista unificada de cada cliente.
   - Ejemplo: combinar el historial de navegación web, las interacciones de aplicaciones y las compras sin conexión en un solo perfil.
- **Resolución de identidad**: vincule datos de clientes entre dispositivos y canales.
   - Ejemplo: Hacer coincidir la dirección de correo electrónico de un cliente con los datos de uso de su aplicación mediante Identity Graph.
- **Creación y administración de audiencias**: Defina grupos basados en atributos y comportamientos.
   - Ejemplo: Cree una audiencia para &quot;Clientes fieles&quot; que hayan realizado más de cinco compras en el último año.
- **Segmentación**: aplique reglas para la pertenencia a audiencias dinámicas.
   - Ejemplo: Configure un segmento para &quot;Compradores de alto valor&quot; que se actualice automáticamente cuando los clientes gasten más de 500 $.

**Beneficio**: habilita el direccionamiento y la personalización precisos mediante una comprensión dinámica de las preferencias individuales, el historial y las suscripciones a segmentos.



### Gestión de contenido: Diseñe su mensaje

**Propósito**: crear, administrar, personalizar y reutilizar contenido de marketing en varios canales. Esto incluye la administración de recursos digitales, la creación de mensajes con editores visuales o código, el uso de plantillas de contenido y fragmentos reutilizables, la creación de páginas de destino y el uso de inteligencia artificial (IA) para la generación de contenido.

Las herramientas de gestión de contenido garantizan que los equipos creen y entreguen mensajes personalizados de forma eficaz, manteniendo la coherencia y la relevancia en cada punto de contacto.

**Componentes clave**:

- **Editores de contenido**: cree y dé formato a los mensajes visualmente o con código.
   - Ejemplo: Utilice el editor visual para diseñar una campaña de correo electrónico que promocione las ventas de días festivos.
- **Administración de recursos digitales**: Organice y use imágenes y otros medios.
   - Ejemplo: Almacenar imágenes de productos en una biblioteca centralizada para facilitar su reutilización en campañas.
- **Plantillas y fragmentos**: cree componentes de contenido reutilizables.
   - Ejemplo: Cree una plantilla &quot;Mensaje de bienvenida&quot; que inserte dinámicamente nombres de clientes.
- **Herramientas de Personalization**: adapte el contenido de forma dinámica para particulares.
   - Ejemplo: mostrar recomendaciones de productos personalizadas basadas en el historial de navegación.
- **Creador de páginas de aterrizaje**: cree destinos web para las campañas.

**Beneficio**: optimiza la creación de contenido, garantiza la coherencia de la marca y facilita la entrega eficiente de mensajes altamente personalizados.



### Gestión de decisiones: El cerebro de Personalization

**Propósito**: seleccione el mejor mensaje u oferta para cada cliente en el momento adecuado, según su perfil en tiempo real, contexto y reglas empresariales predefinidas o modelos de IA. Gestión de decisiones implica administrar una biblioteca central de ofertas, definir reglas de elegibilidad, aplicar restricciones (como límite de frecuencia) y establecer una lógica de clasificación.

Gestión de decisiones garantiza que la personalización funcione a escala ofreciendo el máximo valor mediante la automatización inteligente.

**Componentes clave**:

- **Biblioteca de ofertas**: Repositorio central de ofertas de marketing.
   - Ejemplo: Ofertas de la tienda como &quot;Cupón con descuento del 20 %&quot; o &quot;Envío gratuito&quot; en una biblioteca compartida.
- **Reglas de decisión**: lógica para seleccionar contenido óptimo.
   - Ejemplo: Mostrar un &quot;Descuento por fidelidad&quot; solo a los clientes del segmento &quot;Clientes fieles&quot;.
- **Restricciones y elegibilidad**: controla quién recibe qué y cuándo.
   - Ejemplo: Aplique un límite de frecuencia para evitar que un cliente reciba la misma oferta dos veces en una semana.
- **Estrategias de clasificación**: dé prioridad a las ofertas según los objetivos comerciales o la IA.
   - Ejemplo: Clasifique ofertas por rentabilidad, mostrando primero los productos con alto margen.
- **Herramientas de simulación**: Pruebe y valide estrategias de decisión.

**Beneficio**: automatiza y optimiza la personalización para garantizar que las experiencias relevantes e impactantes se entreguen en cada punto de contacto.



### Gestión de recorridos: El director de orquesta

**Propósito**: Diseñar, orquestar y automatizar las experiencias de los clientes en varios pasos y canales. Los recorridos reaccionan a los comportamientos y eventos de los clientes en tiempo real, guiando a las personas a través de rutas personalizadas. AJO también admite campañas para enviar mensajes programados y únicos a audiencias específicas.

La administración de recorrido garantiza que las experiencias se sientan adaptables y sin problemas, lo que guía a las personas en función de sus preferencias y acciones.

**Componentes clave**:

- **diseñador de Recorrido**: lienzo visual para crear rutas de acceso de cliente.
   - Ejemplo: Diseño de un recorrido que envíe un correo electrónico de bienvenida cuando un cliente se suscriba.
- **déclencheur de Recorrido**: Eventos que inician o avanzan recorridos.
   - Ejemplo: Déclencheur de un SMS de seguimiento después de que un cliente abandone el carro de compras.
- **Pasos de condición**: utilice la bifurcación basada en lógica.
   - Ejemplo: enviar un mensaje diferente en función de si un cliente abre un correo electrónico.
- **Actividades de espera**: Controle la progresión con retrasos.
   - Ejemplo: espere tres días antes de enviar un correo electrónico de recordatorio.
- **Administración de campañas**: herramientas para mensajes programados de una sola vez.

**Beneficio**: crea experiencias conectadas y sin problemas que se adaptan a las interacciones individuales, nutren las relaciones y conducen a los resultados deseados.



### Conexiones: Las tuberías

**Propósito**: administrar el flujo de datos a AJO (fuentes) y el envío de mensajes o datos desde AJO (canales y destinos). Las fuentes llevan datos a Adobe Experience Platform (AEP). Los canales envían mensajes (por correo electrónico, SMS, push, web, etc.). Los destinos permiten que la información de la audiencia o del conjunto de datos fluya a plataformas externas.

Las conexiones garantizan que los datos entren en AJO de forma eficaz y lleguen a los clientes de forma fiable a través de los puntos de contacto adecuados.

**Componentes clave**:

- **Conectores de Source**: Importe datos en la plataforma.
   - Ejemplo: Utilice un conector para traer datos de compra de una plataforma de comercio electrónico.
- **Configuración del canal**: configure y administre mecanismos de entrega.
   - Ejemplo: Configuración del envío de SMS para mensajes promocionales.
- **Configuración de destino**: conéctese a sistemas de activación externos.
   - Ejemplo: compartir datos de audiencia con una plataforma de publicidad de medios sociales.
- **Administración de flujo de datos**: Controle el movimiento de información.

**Beneficio**: garantiza una ingesta de datos eficiente y una entrega de mensajes confiable en todos los canales, a la vez que habilita la activación en sistemas externos.



### Administración y privacidad: libro de reglas

**Propósito**: establecer la configuración del sistema, administrar el acceso y los permisos de los usuarios, configurar canales de comunicación, definir parámetros de recorrido y garantizar el cumplimiento de las directivas de gobernanza y privacidad de datos. Esto incluye la administración del consentimiento, la aplicación de reglas de uso de datos y la administración de solicitudes de acceso o eliminación de datos.

Las herramientas de administración y privacidad garantizan la protección de la integridad de los datos y el cumplimiento de todas las políticas legales y organizativas.

**Componentes clave**:

- **Administración de usuarios y acceso**: Controle el acceso y los permisos.
   - Ejemplo: Asignación de permisos específicos a equipos de marketing y TI.
- **Configuración de espacio aislado**: Separe los entornos para desarrollo y pruebas.
   - Ejemplo: Utilice una zona protegida para probar nuevos diseños de recorrido antes de implementarlos en tiempo real.
- **Configuración del canal**: configure las opciones técnicas para la entrega.
   - Ejemplo: Configuración de los detalles del servidor de correo electrónico para la mensajería de campaña.
- **Herramientas de privacidad**: administre las preferencias de consentimiento y privacidad.
   - Ejemplo: Gestión eficaz de las solicitudes de eliminación de datos del RGPD (Reglamento General de Protección de Datos).
- **Controles de administración**: Aplicar directivas de uso de datos.

**Beneficio**: garantiza el funcionamiento seguro de la plataforma, el cumplimiento de las regulaciones y la alineación con las directivas de la organización.



## Conectar los puntos: cómo funciona todo junto

Estas áreas funcionales funcionan en un ciclo continuo para ofrecer y optimizar experiencias personalizadas para los clientes:

1. **Ingesta de datos**: Los datos fluyen a AEP, estructurados por la administración de datos.
2. **Comprensión del cliente**: Los perfiles del cliente en tiempo real unifican estos datos, mientras que la administración de clientes mejora la información a través de Perfiles y Audiencias.
3. **Estrategia de contenido y ofertas**: La administración de contenido crea mensajes y recursos. Administración de decisiones define las ofertas y la lógica para seleccionar la mejor.
4. **Orquestación**: Administración de Recorrido asigna las interacciones entre canales, aprovechando la comprensión del cliente, el contenido y las decisiones.
5. **Envío**: las conexiones facilitan la entrega de mensajes a través de canales seleccionados o comparten datos con sistemas externos.
6. **Medición y optimización**: los datos de rendimiento y las interacciones de los clientes devuelven información al sistema para refinar las audiencias, el contenido, las decisiones y los recorridos.
7. **Gobernanza**: los controles de administración y privacidad garantizan el cumplimiento y la correcta configuración del sistema.

Este proceso iterativo permite a las organizaciones aprender y mejorar continuamente sus estrategias de participación de los clientes.
