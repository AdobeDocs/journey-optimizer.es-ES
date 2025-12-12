---
solution: Journey Optimizer
product: journey optimizer
title: Funciones y responsabilidades
description: Obtenga información acerca de las diferentes funciones que intervienen en Adobe Journey Optimizer y sus responsabilidades
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: d3765f66beff13aaf77cd585c5da5f93c44fa1df
workflow-type: tm+mt
source-wordcount: '1724'
ht-degree: 13%

---


# Funciones y responsabilidades

Adobe Journey Optimizer permite a las marcas ofrecer experiencias conectadas, contextuales y personalizadas en todo el recorrido del cliente. Journey Optimizer, que se ha creado con un enfoque integral en cuanto a escala, velocidad y flexibilidad, combina tres controladores de valor principales en una aplicación unificada:

* **Datos y participación de clientes en tiempo real** con tecnología del perfil de clientes en tiempo real de Adobe
* **Orquestación omnicanal moderna** a través de lienzos unificados para recorridos en tiempo real y campañas por lotes, además de un diseñador de mensajes moderno
* **Toma de decisiones y personalización inteligentes** mediante la administración de decisiones y las capacidades de IA/ML

Journey Optimizer ofrece dos métodos de orquestación para satisfacer diferentes necesidades de marketing:

* **Recorridos**: la mejor opción para una participación uno a uno en tiempo real por la que cada cliente avanza a su propio ritmo, desencadenada por comportamientos o eventos
* **Campañas orquestadas**: la mejor opción para campañas en lotes y de uno a varios en las que las audiencias progresan juntas a través de flujos de trabajo de varios pasos según una programación. Es ideal para promociones de temporada, lanzamientos de productos y comunicaciones basadas en cuentas

Esta experiencia unificada le permite implementar casos de uso completos en un solo lugar, desde la definición de audiencias y el diseño de recorridos hasta la creación de contenido personalizado y el análisis de resultados. En esta documentación se explican las funciones clave en el uso eficaz de Journey Optimizer, sus responsabilidades y cómo empezar.

**Nota importante:** Adobe Journey Optimizer define funciones distintas con responsabilidades específicas. Un solo individuo puede desempeñar varias funciones o todas las funciones, según la estructura de su organización.

## Guías de inicio rápido basadas en funciones

Para simplificar la implementación, Adobe Journey Optimizer organiza las tareas en funciones específicas en función de su experiencia. Cada función se centra en las tareas esenciales necesarias para ofrecer una experiencia de cliente optimizada.

| Función | Responsabilidades principales | Habilidades clave | Tareas habituales |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrador** | Configuración del entorno y administración de acceso | Configuración del sistema, administración de usuarios, seguridad | Configurar zonas protegidas, administrar permisos de usuario, configurar canales y ajustes preestablecidos de mensajes |
| **Ingeniero de datos** | Datos de perfil del cliente y fuentes de datos | Modelado de datos, esquemas XDM, conectores de origen | Modelar perfiles y datos empresariales en esquemas, configurar conectores de origen, monitorizar la ingesta de datos |
| **Desarrollador** | Implementación técnica e integraciones | SDK móvil/web, API, arquitectura impulsada por eventos | Integrar SDK, implementar eventos, crear extremos de acciones personalizadas |
| **Experto en marketing** | diseño de recorridos y experiencias personalizadas | orquestación de recorrido, creación de contenido, segmentación de audiencia | Diseñar recorridos de clientes, crear y personalizar mensajes, administrar ofertas y componentes de decisión, definir audiencias |

Cada función aborda una fase específica de la implementación de Adobe Journey Optimizer y garantiza un proceso de implementación estructurado y eficaz.

## Orden de implementación y dependencias de función

Una implementación correcta de Journey Optimizer suele seguir esta secuencia, que refleja las dependencias entre funciones:

1. **Administrador**: configura el entorno\
   El administrador establece la base configurando los entornos limitados, los controles de acceso y las configuraciones de canal. Esto debe suceder primero para permitir que funcionen otros equipos.
   * Configurar zonas protegidas de desarrollo, ensayo y producción
   * Configurar funciones, permisos y control de acceso de nivel de objeto (OLAC)
   * Configure las configuraciones de canal (correo electrónico, SMS, push, en la aplicación, web, tarjetas de contenido)
   * Delegación de subdominios y configuración de grupos de IP
   * Configuración de listas de supresión y políticas de consentimiento

2. **Ingeniero de datos**: crea la infraestructura de datos\
   Los ingenieros de datos crean la infraestructura de datos que potencia la personalización y definen cómo los datos de los clientes fluyen hacia y a través del sistema.
   * Crear áreas de nombres de identidad para la identificación de clientes
   * Diseño de esquemas XDM (perfil, eventos de experiencia, relacionales)
   * Configure conjuntos de datos y actívelos para el Perfil del cliente en tiempo real
   * Configuración de la ingesta de datos (por lotes y streaming)
   * Crear atributos calculados para cálculos complejos
   * Configuración de eventos y fuentes de datos para recorridos

3. **Desarrollador**: Implementa integraciones técnicas\
   Los desarrolladores conectan aplicaciones a Journey Optimizer integrando SDK, enviando eventos y creando extremos de API. Estas implementaciones permiten a los recorridos almacenar en déclencheur y ejecutarse.
   * Integración de Mobile SDK (iOS/Android) con la configuración de notificaciones push
   * Implementación de Web SDK para experiencias web
   * Envío de eventos de aplicaciones a recorridos de déclencheur
   * Crear extremos de acción personalizados para integraciones de sistema externas
   * Implementaciones de prueba con Adobe Experience Platform Assurance

4. **Especialista en marketing**: Diseña y ejecuta experiencias de clientes\
   Los especialistas en marketing aprovechan todo el trabajo básico para crear recorridos, crear contenido y optimizar las experiencias de los clientes en todos los canales.
   * Crear audiencias mediante segmentación, carga de CSV o composición de audiencias
   * Diseño de contenido personalizado con el asistente de IA y plantillas
   * Creación de recorridos multicanal con déclencheur de evento y audiencia
   * Probar con flujos de trabajo de aprobación antes del lanzamiento
   * Monitorice el rendimiento y optimice en función de las perspectivas de informes

**Nota:** Aunque esta secuencia es típica, algunas actividades pueden ocurrir en paralelo. Por ejemplo, los desarrolladores pueden trabajar en las integraciones de aplicaciones mientras los ingenieros de datos configuran los esquemas.

## Introducción según función

Cada función comienza con tareas específicas adaptadas a su objetivo. Completar estos pasos iniciales garantiza una incorporación y alineación más fluidas con el proceso de implementación general:

### Para especialistas en marketing {#for-marketers}

Como experto en marketing o profesional del negocio, diseña recorridos de clientes para ofrecer experiencias personales y contextuales en todos los puntos de contacto. Trabajará en una interfaz unificada para implementar casos de uso completos de principio a fin.

**Funcionalidades clave que usará:**

* **Journey Orchestration**: crea una participación de clientes en tiempo real y uno a uno, en la que cada persona se mueve a su propio ritmo, desencadenada por comportamientos o eventos entre canales
* **Orquestación de campaña**: diseñe y automatice campañas complejas en lotes de varios pasos a escala mediante un lienzo visual. Perfecto para campañas iniciadas por la marca, como promociones de temporada, lanzamientos de productos y comunicaciones basadas en cuentas. Aproveche la segmentación de varias entidades para crear audiencias precisas conectando los datos del cliente con entidades relacionadas (cuentas, compras, reservas)
* **Modern Message Designer**: diseñe y personalice mensajes de correo electrónico y móviles con una interfaz de arrastrar y soltar. Edite plantillas listas para usar para acelerar el tiempo de salida al mercado
* **Administración de decisiones**: cree y administre ofertas, reglas de elegibilidad y otros componentes en una biblioteca centralizada que se puede incrustar en correos electrónicos y puntos de contacto de clientes
* **Administración de recursos**: Acceda a Adobe Experience Manager Assets Essentials totalmente integrado en Journey Optimizer para disfrutar de un acceso y una entrega de recursos más sencillos
* **Definición de audiencia**: genere audiencias a petición con refinamiento instantáneo mediante consultas relacionales, con visibilidad previa al envío para obtener recuentos precisos de audiencias
* **Servicios de IA/ML**: aproveche la optimización del tiempo de envío y las puntuaciones de participación predictiva para dirigirse a clientes de alto valor y minimizar el riesgo de pérdida

**Empiece con:** Plantillas de casos de uso y asistentes para crear e implementar fácilmente nuevas recorridos de clientes.

[Introducción como experto en marketing →](path/marketer.md)

### Para ingenieros de datos {#for-data-engineers}

Como arquitecto de datos o ingeniero, puede configurar y mantener los datos de perfil del cliente y otras fuentes de datos que impulsan las experiencias orquestadas por Journey Optimizer.

**Responsabilidades clave:**

* **Datos de perfil del cliente**: Modele datos de perfil del cliente y datos empresariales en esquemas para crear una vista unificada del cliente en 360 grados
* **Modelado de datos relacionales**: para campañas organizadas, diseñe esquemas relacionales para habilitar la segmentación de varias entidades, conectando los datos de los clientes con entidades relacionadas como cuentas, compras, suscripciones y reservas para una creación flexible de audiencias
* **Conectores de Source**: configure conectores de origen para introducir datos de la web, CRM, datos sin conexión y otras fuentes en Adobe Experience Platform
* **Resolución de identidades**: configure áreas de nombres de identidades para actualizar continuamente los perfiles y mover clientes dentro y fuera de segmentos y recorridos en tiempo real
* **Fuentes de datos**: configure las fuentes de datos para que escuchen en tiempo real las señales externas a través del recorrido del cliente
* **Administración de perfiles**: habilite conjuntos de datos para el Perfil del cliente en tiempo real para potenciar las experiencias personalizadas
* **Calidad de los datos**: supervise la ingesta de datos para asegurarse de que todo fluye sin problemas a Journey Optimizer

**Empiece por:** Modele su primer esquema de perfil de cliente y configure un conector de origen para comenzar a ingerir datos.

[Introducción como ingeniero de datos →](path/data-engineer.md)

### Para administradores {#for-administrators}

Como administrador, puede configurar el entorno de Journey Optimizer para permitir que sus equipos trabajen de forma eficaz y segura.

**Responsabilidades clave:**

* **Zonas protegidas**: cree y administre zonas protegidas para dividir datos y recorridos para diferentes grupos de usuarios (desarrollo, pruebas y producción)
* **Administración de usuarios**: configure grupos de usuarios y permisos para controlar el acceso a distintas funcionalidades
* **Configuración del canal**: configure los canales de entrega y los ajustes preestablecidos de mensajes para garantizar una marca coherente en todos los mensajes y recursos entregados a través de Journey Optimizer
* **Seguridad y administración**: aplique el control de acceso de nivel de objeto (OLAC), configure directivas de consentimiento e implemente directivas de control de datos
* **Capacidad de entrega**: delegue subdominios, cree grupos de IP y administre listas de supresión y listas de permitidos
* **Configuración de Recorrido**: configure elementos y configuraciones de recorrido para sus equipos

**Empiece con:** Configure las zonas protegidas y los permisos de usuario y, a continuación, configure las primeras configuraciones de canal y los ajustes preestablecidos de mensaje.

[Introducción como administrador →](path/administrator.md)

### Para desarrolladores {#for-developers}

Implemente integraciones técnicas que conecten Journey Optimizer a sus aplicaciones.

**Responsabilidades clave:**

* Integración de Adobe Experience Platform Mobile SDK (iOS/Android)
* Implementación de Web SDK para experiencias web y notificaciones push web
* Configurar credenciales y certificados de notificaciones push
* Envío de eventos de aplicaciones a recorridos de déclencheur
* Generar extremos de API que Journey Optimizer llame mediante acciones personalizadas
* Implementar experiencias basadas en código para superficies web, móviles y de otro tipo
* Probar y depurar implementaciones con Adobe Experience Platform Assurance
* Trabajo con las API de Journey Optimizer para el acceso mediante programación

**Empiece por:** Integre Mobile o Web SDK e implemente su primer evento para almacenar en déclencheur un recorrido.

[Introducción como desarrollador →](path/developer.md)

## Cross-Role Collaboration

Las implementaciones de Journey Optimizer correctas requieren la colaboración entre todas las funciones. Cada función trabaja con otras para ofrecer experiencias de cliente sin problemas:

>[!BEGINTABS]

>[!TAB Administradores]

**Administradores** habilitan todos los equipos al administrar el acceso y las configuraciones. Trabajan con:

* **Ingenieros de datos**: conceda permisos para la administración de datos, apruebe el acceso a la zona protegida y coordine las directivas de gobernanza
* **Desarrolladores**: Proporcione credenciales de API, configure entornos de prueba y apruebe configuraciones de canal
* **Especialistas en marketing**: asigne permisos para recorridos/campañas, configure canales y admita entornos de prueba

>[!TAB Ingenieros de datos]

**Ingenieros de datos** proporcionan la base de datos para todos. Trabajan con:

* **Administradores**: Solicite permisos para la administración de datos, coordine las directivas de gobernanza y retención
* **Desarrolladores**: Proporcione esquemas XDM y estructuras de eventos, defina formatos de carga útil de eventos y pruebe la ingesta de datos
* **Especialistas en marketing**: cree atributos calculados para la personalización, cree audiencias y configure esquemas relacionales

>[!TAB Desarrolladores]

**Desarrolladores** implementan integraciones técnicas que mejoran los recorridos. Trabajan con:

* **Ingenieros de datos**: obtenga esquemas XDM y estructuras de eventos, alinéense en los requisitos de recopilación de datos y pruebe la entrega de eventos
* **Administradores**: Proporcione especificaciones de API, solicite permisos y credenciales, y coordine la estrategia de prueba
* **Especialistas en marketing**: comprenda los déclencheur de eventos, implemente el seguimiento, admita las pruebas de recorrido y solucione problemas

>[!TAB Especialistas en marketing]

**Los especialistas en marketing** diseñan experiencias para los clientes y proporcionan comentarios. Trabajan con:

* **Ingenieros de datos**: Solicite atributos calculados, coordine los requisitos de audiencia y proporcione comentarios sobre la calidad de los datos
* **Desarrolladores**: Alinee en los déclencheur de eventos, pruebe las implementaciones y valide el seguimiento
* **Administradores**: Solicite configuraciones de canal, confirme el acceso a la función y coordine la habilitación

>[!ENDTABS]

**Práctica recomendada:** Realice reuniones interfuncionales periódicas para alinearse en las prioridades, compartir el progreso y abordar los bloqueadores entre equipos.

## Vídeo práctico {#video}

Para obtener más información acerca de las funcionalidades y personalidades clave de Journey Optimizer, vea el vídeo introductorio. El vídeo muestra la interfaz de usuario y resalta las funciones clave en función de los flujos de trabajo específicos de funciones.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Recursos adicionales

Para obtener información y actualizaciones más detalladas, explore los siguientes recursos:

>[!BEGINTABS]

>[!TAB Aprendizaje y documentación]

* [Vídeos de tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=es){target="_blank"}: tutoriales de vídeo paso a paso para todas las funciones
* [Biblioteca de casos de uso de Recorrido](../building-journeys/jo-use-cases.md): ejemplos prácticos y patrones de implementación
* [Funciones inteligentes y de IA](ai-features.md): obtenga información sobre el asistente de IA, la optimización del tiempo de envío y la generación de contenido
* [Guía de interfaz de usuario](user-interface.md): navegue por Journey Optimizer de forma eficaz

>[!TAB Permanecer actualizado]

* [Notas de la versión](../rn/release-notes.md): últimas funciones, mejoras y correcciones
* [Actualizaciones de documentación](../rn/documentation-updates.md) - Rastrear cambios recientes en la documentación
* [Notificaciones de productos](../rn/releases.md#staying-informed): aprenda a suscribirse a alertas por correo electrónico y en el producto para actualizaciones de Journey Optimizer

>[!TAB Comunidad y asistencia]

* [Comunidad de Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}: conéctese con otros usuarios y expertos
* [Foro de productos](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}: haga preguntas y comparta conocimientos

>[!ENDTABS]
