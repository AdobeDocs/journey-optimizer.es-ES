---
solution: Journey Optimizer
product: journey optimizer
title: Funciones y responsabilidades de AJO
description: Obtenga información acerca de las diferentes funciones que intervienen en Adobe Journey Optimizer y sus responsabilidades
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: d2cdafef6f2d69ea85d9d042c859a8b1e7654d7d
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---


# Funciones y responsabilidades de AJO

Adobe Journey Optimizer (AJO) permite a las marcas ofrecer recorridos de cliente conectados y contextualizados a lo largo del ciclo de vida del cliente. Permite a los equipos personalizar las interacciones a escala y alinea las expectativas de los clientes con los objetivos comerciales. En esta documentación se explican las funciones clave en el uso eficaz de Journey Optimizer, sus responsabilidades y cómo empezar.

**Nota importante:** Adobe Journey Optimizer define funciones distintas con responsabilidades específicas. Un solo individuo puede desempeñar varias funciones o todas las funciones, según la estructura de su organización.

## Guías de inicio rápido basadas en roles

Para simplificar la implementación, AJO organiza las tareas en funciones específicas en función de su experiencia. Cada función se centra en las tareas esenciales necesarias para ofrecer una experiencia de cliente perfecta.

| Función | Responsabilidades principales | Aptitudes clave | Tareas habituales |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrador** | Configuración del sistema y administración de permisos | Configuración del sistema, administración de usuarios, seguridad | Configuración de zonas protegidas, administración de usuarios, configuración de canales |
| **Ingeniero de datos** | Configuración de la estructura y los flujos de datos | Modelado de datos, diseño de esquemas, integración de API | Configurar esquemas, administrar conjuntos de datos, configurar fuentes de datos |
| **Desarrollador** | Integraciones y personalizaciones técnicas | Desarrollo móvil, implementación de API, codificación | Integración de aplicaciones móviles, implementación de API, creación de acciones personalizadas |
| **Experto en marketing** | Diseñar y ejecutar recorridos de cliente | Estrategia de marketing, creación de contenido, diseño de recorridos | Creación de campañas, diseño de recorridos y análisis de informes |

Cada función aborda una fase específica de la implementación de AJO y garantiza un proceso de implementación estructurado y eficaz.

## Orden de implementación y dependencias de rol

Una implementación correcta de Journey Optimizer suele seguir esta secuencia, que refleja las dependencias entre funciones:

1. **Administrador**: configura el entorno\
   El administrador sienta las bases técnicas del sistema y garantiza el acceso y la configuración adecuados para todos los usuarios.
   * Configuración de zonas protegidas y permisos
   * Configuración del acceso de usuario
   * Configuración técnica y de canales de mensajería

2. **Ingeniero de datos**: crea la base de datos\
   Los ingenieros de datos definen la estructura y el flujo de datos, que son esenciales para las experiencias personalizadas.
   * Diseño e implementación de esquemas
   * Configurar áreas de nombres de identidad
   * Configurar la ingesta de datos
   * Creación de perfiles de prueba

3. **Desarrollador**: administra integraciones técnicas\
   Los desarrolladores permiten que AJO interactúe con aplicaciones móviles, sitios web y sistemas externos mediante la implementación de integraciones técnicas. Las notificaciones push, por ejemplo, dependen de configuraciones basadas en desarrolladores.
   * Integración de aplicaciones móviles para notificaciones push
   * Implementación de SDK web
   * Desarrollar integraciones personalizadas mediante API
   * Creación de acciones personalizadas para sistemas de terceros

4. **Especialista en marketing**: crea e inicia recorridos\
   Los especialistas en marketing utilizan las bases establecidas por otras funciones para diseñar e implementar experiencias de cliente. Se centran en la segmentación de audiencia, el contenido personalizado y la optimización de recorridos.
   * Diseño de segmentos de audiencia
   * Creación de contenido personalizado
   * Generar y probar recorridos
   * Analizar el rendimiento y optimizar

**Nota:** Aunque esta secuencia es típica, algunas actividades pueden ocurrir en paralelo. Por ejemplo, los desarrolladores pueden trabajar en las integraciones de aplicaciones mientras los ingenieros de datos configuran los esquemas.

## Introducción por función

Cada función comienza con tareas específicas adaptadas a su objetivo. Completar estos pasos iniciales garantiza una incorporación y alineación más fluidas con el proceso de implementación general:

1. **Para especialistas en marketing**: Céntrese en la creación de recorridos, el diseño de mensajes y la ejecución de campañas.\
   Ejemplo: Comience creando una campaña de correo electrónico de bienvenida para los clientes nuevos.

2. **Para ingenieros de datos**: establezca la base de datos, configure esquemas e integre orígenes de datos.\
   Ejemplo: Configure un esquema para rastrear el historial de compras de los clientes y obtener recomendaciones personalizadas.

3. **Para administradores**: configure entornos, administre permisos y configure canales de mensajería.\
   Ejemplo: Configuración de entornos de zona protegida para probar diferentes estrategias de mensajería.

4. **Para desarrolladores**: Integre aplicaciones móviles, implemente API y genere integraciones personalizadas.\
   Ejemplo: Utilice la API de AJO para almacenar en déclencheur las notificaciones push en función de las acciones de los clientes dentro de la aplicación móvil.

Haga clic en su función a continuación para acceder a instrucciones específicas adaptadas a sus responsabilidades:

* [Introducción como experto en marketing](path/marketer.md)
* [Introducción como ingeniero de datos](path/data-engineer.md)
* [Introducción como administrador](path/administrator.md)

## Vídeo explicativo {#video}

Para obtener más información acerca de las funcionalidades y personalidades clave de Journey Optimizer, vea el vídeo introductorio. El vídeo muestra la interfaz de usuario y resalta las funciones clave en función de los flujos de trabajo específicos de funciones.

>[!VIDEO](https://video.tv.adobe.com/v/3430317?quality=12&captions=spa)

## Recursos adicionales

Para obtener información y actualizaciones más detalladas, explore los siguientes recursos:
* [Notas de la versión](https://experienceleague.adobe.com/docs/journey-optimizer/using/rn/release-notes.html)
* [Vídeos de tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=es)