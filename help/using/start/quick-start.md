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
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 20%

---


# Funciones y responsabilidades

Adobe Journey Optimizer permite a las marcas ofrecer recorridos de clientes conectados y contextualizados a lo largo del ciclo de vida del cliente. Permite a los equipos personalizar las interacciones a escala y alinea las expectativas de los clientes con los objetivos comerciales. En esta documentación se explican las funciones clave en el uso eficaz de Journey Optimizer, sus responsabilidades y cómo empezar.

**Nota importante:** Adobe Journey Optimizer define funciones distintas con responsabilidades específicas. Un solo individuo puede desempeñar varias funciones o todas las funciones, según la estructura de su organización.

## Guías de inicio rápido basadas en funciones

Para simplificar la implementación, Adobe Journey Optimizer organiza las tareas en funciones específicas en función de su experiencia. Cada función se centra en las tareas esenciales necesarias para ofrecer una experiencia de cliente optimizada.

| Función | Responsabilidades principales | Habilidades clave | Tareas habituales |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrador** | Configuración del entorno y administración de acceso | Configuración del sistema, administración de usuarios, seguridad | Configuración de zonas protegidas, administración de permisos y configuraciones de canal |
| **Ingeniero de datos** | Fundamento y arquitectura de datos | Modelado de datos, esquemas XDM, calidad de datos | Crear esquemas y conjuntos de datos, configurar la ingesta de datos, administrar el ciclo vital de datos |
| **Desarrollador** | Implementación técnica e integraciones | SDK móvil/web, API, arquitectura impulsada por eventos | Integrar SDK, implementar eventos, crear extremos de acciones personalizadas |
| **Experto en marketing** | Diseño y ejecución de la experiencia del cliente | diseño de recorrido, creación de contenido, análisis de datos | Creación de recorridos, creación de contenido personalizado, optimización de campañas |

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

Concéntrese en crear experiencias de cliente personalizadas en todos los canales.

**Funcionalidades clave que usará:**

* Cree audiencias y segmentos con varios métodos (definiciones de segmentos, carga de CSV, composición de audiencias)
* Diseño de contenido con el asistente de IA para la generación de texto e imágenes
* Cree recorridos de cliente multicanal con el diseñador de arrastrar y soltar
* Aproveche la optimización del tiempo de envío y la administración de conflictos para maximizar la participación
* Prueba de contenido y uso de flujos de trabajo de aprobación antes de publicar
* Monitorización del rendimiento con paneles de informes integrados

**Empiece por:** Cree un recorrido de bienvenida simple o una campaña de recuperación del carro de compras abandonada usando plantillas generadas previamente.

[Introducción como experto en marketing →](path/marketer.md)

### Para ingenieros de datos {#for-data-engineers}

Establezca la base de datos que alimenta las experiencias personalizadas.

**Responsabilidades clave:**

* Crear áreas de nombres de identidad y configurar la resolución de identidades
* Diseño de esquemas XDM para datos de perfil y evento (estándar y relacionales)
* Configure conjuntos de datos y actívelos para el Perfil del cliente en tiempo real
* Configurar conectores de origen para la ingesta de datos por lotes y de flujo continuo
* Creación de atributos calculados para simplificar la segmentación
* Configuración de eventos y fuentes de datos para la ejecución de recorridos
* Administrar la calidad de los datos, la gobernanza y el ciclo vital

**Empiece por:** Configure áreas de nombres de identidad y cree su primer esquema de perfil con los grupos de campos requeridos.

[Introducción como ingeniero de datos →](path/data-engineer.md)

### Para administradores {#for-administrators}

Configure y administre el entorno de Journey Optimizer para su organización.

**Responsabilidades clave:**

* Crear y administrar zonas protegidas para desarrollo, pruebas y producción
* Configurar funciones y permisos mediante funciones predeterminadas o personalizadas
* Aplicar el control de acceso a nivel de objeto (OLAC) a los recursos seguros
* Configure los canales para las tarjetas de correo electrónico, SMS, push, en la aplicación, web y de contenido
* Delegue subdominios y cree grupos de IP para la entrega de correo electrónico
* Administración de listas de supresión y listas de permitidos
* Configurar políticas de consentimiento y administración de datos (con Healthcare/Privacy Shield)

**Empiece con:** Configure zonas protegidas, configure funciones y permisos básicos y, a continuación, trabaje con su equipo en las configuraciones de canal.

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

Las implementaciones correctas de Journey Optimizer requieren la colaboración entre todas las funciones:

* **Administradores** habilitan otras funciones mediante la configuración de zonas protegidas, permisos y configuraciones de canal
* **Ingenieros de datos** proporcionan la base de datos sobre la que se basan los desarrolladores y los especialistas en marketing
* **Desarrolladores** implementan las integraciones técnicas que los especialistas en marketing utilizan para almacenar en déclencheur los recorridos
* **Los especialistas en marketing** proporcionan comentarios a todos los equipos sobre la calidad de los datos, las solicitudes de características y la experiencia del usuario

**Práctica recomendada:** Realice reuniones interfuncionales periódicas para alinearse en las prioridades, compartir el progreso y abordar los bloqueadores entre equipos.

## Vídeo práctico {#video}

Para obtener más información acerca de las funcionalidades y personalidades clave de Journey Optimizer, vea el vídeo introductorio. El vídeo muestra la interfaz de usuario y resalta las funciones clave en función de los flujos de trabajo específicos de funciones.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Recursos adicionales

Para obtener información y actualizaciones más detalladas, explore los siguientes recursos:

**Aprendizaje y documentación:**

* [Vídeos de tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=es){target="_blank"}: tutoriales de vídeo paso a paso para todas las funciones
* [Biblioteca de casos de uso de Recorrido](../building-journeys/jo-use-cases.md): ejemplos prácticos y patrones de implementación
* [Funciones inteligentes y de IA](ai-features.md): obtenga información sobre el asistente de IA, la optimización del tiempo de envío y la generación de contenido
* [Guía de interfaz de usuario](user-interface.md): navegue por Journey Optimizer de forma eficaz

**Permanecer actualizado:**

* [Notas de la versión](../rn/release-notes.md): últimas funciones, mejoras y correcciones
* [Actualizaciones de documentación](../rn/documentation-updates.md) - Rastrear cambios recientes en la documentación
* **Notificaciones de productos** - Habilite alertas en su [perfil de Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} para recibir notificaciones sobre nuevas versiones, ventanas de mantenimiento y anuncios importantes. Haga clic en el icono de perfil > Preferencias > Notificaciones para configurarlas.

**Comunidad y asistencia técnica:**

* [Comunidad de Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=es){target="_blank"}: conéctese con otros usuarios y expertos
* [Foro de productos](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=es){target="_blank"}: haga preguntas y comparta conocimientos
