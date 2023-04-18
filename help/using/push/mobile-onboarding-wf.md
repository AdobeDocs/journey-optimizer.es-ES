---
solution: Journey Optimizer
product: journey optimizer
title: Flujo de trabajo de inicio rápido de la incorporación al dispositivo móvil
description: Descubra cómo utilizar el flujo de trabajo de inicio rápido de la incorporación al dispositivo móvil
topic: Mobile
feature: Push
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
source-git-commit: 145d2a60bc5dbd6e2a92f13afbf2db662f465e36
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 5%

---


# Flujo de trabajo de inicio rápido de la incorporación al dispositivo móvil {#mobile-wf}

El nuevo **flujo de trabajo de inicio rápido de la incorporación móvil** es una nueva función de producto para configurar rápidamente el SDK de Mobile, empezar a recopilar y validar datos de eventos móviles y enviar notificaciones push con [!DNL Journey Optimizer].

Se puede acceder a esta funcionalidad a través de la **[!DNL Adobe Experience Platform Data Collection]** página de inicio para todos los clientes como versión beta pública.

## Introducción {#gs-mobile-wf}

Este nuevo flujo de trabajo automatiza la configuración de la recopilación de datos al reducir el número total de clics y acelerar la configuración móvil para Journey Optimizer. Este flujo de trabajo de inicio rápido le guía por cuatro pasos sencillos para [configurar](##setup-mobile-wf), [implementar](#implement-mobile-wf), [validate](#valid-mobile-wf)y [review](#review-mobile-wf) la configuración móvil.

Para acceder al nuevo flujo de trabajo de inicio rápido de la integración móvil, vaya a **[!DNL Data Collection]** del conmutador de soluciones. A continuación, seleccione la **[!DNL Start Collecting Mobile Data]** en la página principal.

![](assets/mobile-wf-home.png)

A continuación se presentan algunas funciones adicionales:

* Flujo de trabajo de cuatro pasos y interfaz de usuario sencillos.
* Ofrece una configuración básica para empezar a recopilar datos de eventos móviles a través del SDK móvil en minutos.
* Posibilidad de probar y validar un evento push móvil básico mediante Assurance.
* Crea y configura automáticamente todos los recursos necesarios de Recopilación de datos y de Journey Optimizer.
* En la guía del producto y la información sobre herramientas.
* Proporciona una transición natural para una implementación más avanzada si es necesario.

## Configuración {#setup-mobile-wf}

El primer paso de este flujo de trabajo crea y configura automáticamente toda la recopilación de datos necesaria y los recursos de Journey Optimizer, como las propiedades móviles, las extensiones móviles, la extensión de Journey Optimizer, las reglas, los elementos de datos, etc.

Tras aceptar los términos y condiciones de la versión beta, introduzca el nombre de su aplicación móvil y haga clic en **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

Proporcione información para las plataformas iOS y Android, incluido su ID de aplicación y claves de autenticación o archivo clave.

## Implementación{#implement-mobile-wf}

El paso siguiente proporciona instrucciones paso a paso para instalar el código en la aplicación móvil.

![](assets/mobile-wf-add-code.png)


## Validación {#valid-mobile-wf}

Revise y compruebe la implementación para validarla. Puede enviar una notificación push de prueba.

![](assets/mobile-wf-valid.png)


## Consulte {#review-mobile-wf}

La configuración automatizada ha finalizado. Ahora puede visitar la propiedad móvil de la etiqueta y configurar las reglas o el elemento de datos, así como empezar a enviar notificaciones push con Adobe Journey Optimizer.

![](assets/mobile-wf-done.png)


**Temas relacionados**

* [Introducción a las notificaciones push](get-started-push.md)
* [Flujo y componentes de datos de notificaciones push](push-gs.md)
* [Configuración del canal push](push-configuration.md)
* [Informe de notificaciones push](../reports/journey-global-report.md#push-global)
* [Crear una notificación push](create-push.md)
