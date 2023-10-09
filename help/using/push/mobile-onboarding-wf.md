---
solution: Journey Optimizer
product: journey optimizer
title: Flujo de trabajo de inicio rápido de incorporación al dispositivo móvil
description: Aprenda a utilizar el flujo de trabajo de inicio rápido de la incorporación móvil
topic: Mobile
feature: Push
role: Admin
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 364ef926-3f92-4297-acbd-a283668106ac
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 9%

---

# Flujo de trabajo de inicio rápido de incorporación al dispositivo móvil {#mobile-wf}

El nuevo **flujo de trabajo de inicio rápido de incorporación móvil** es una nueva función del producto que permite configurar rápidamente el SDK de Adobe Experience Platform Mobile, empezar a recopilar y validar datos de eventos móviles y enviar notificaciones push con [!DNL Journey Optimizer].

Se puede acceder a esta funcionalidad a través de la **[!DNL Adobe Experience Platform Data Collection]** a todos los clientes como una versión beta pública.

## Introducción {#gs-mobile-wf}

Este nuevo flujo de trabajo automatiza la configuración de la recopilación de datos al reducir el número total de clics y acelerar la configuración móvil de Journey Optimizer. Este flujo de trabajo de inicio rápido le permite seguir cuatro sencillos pasos para lo siguiente [configurar](##setup-mobile-wf), [implementar](#implement-mobile-wf), [validate](#valid-mobile-wf), y [reseña](#review-mobile-wf) su configuración móvil.

Para acceder al nuevo flujo de trabajo de inicio rápido de la incorporación móvil, vaya a **[!DNL Data Collection]** desde el conmutador de soluciones. A continuación, seleccione la **[!DNL Start Collecting Mobile Data]** en la página de inicio.

![](assets/mobile-wf-home.png)

A continuación se muestran algunas funciones adicionales:

* Flujo de trabajo de cuatro pasos e interfaz de usuario sencillos.
* Ofrece una configuración básica para empezar a recopilar datos de evento móviles mediante [SDK de Adobe Experience Platform Mobile](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} en minutos.
* Capacidad para probar y validar un evento push móvil básico [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}.
* Crea y configura automáticamente todos los recursos de recopilación de datos y Journey Optimizer necesarios.
* En la guía del producto y la información sobre herramientas.
* Proporciona una transición natural para una implementación más avanzada si es necesario.

## Configuración de {#setup-mobile-wf}

El primer paso de este flujo de trabajo crea y configura automáticamente todos los recursos de recopilación de datos y Journey Optimizer necesarios, como propiedades móviles, extensiones móviles, extensión de Journey Optimizer, reglas, elementos de datos, etc.

Tras aceptar los Términos y condiciones de la versión beta, introduzca el nombre de su aplicación móvil y haga clic en **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

Proporcione información para las plataformas iOS y Android, incluido su ID de aplicación y las claves de autenticación o archivo de clave.

## Implementación{#implement-mobile-wf}

El siguiente paso proporciona instrucciones paso a paso para instalar el código en la aplicación móvil.

![](assets/mobile-wf-add-code.png)


## Validación {#valid-mobile-wf}

Revise y compruebe la implementación para validarla. Puede enviar una notificación push de prueba.

![](assets/mobile-wf-valid.png)


## Consulte {#review-mobile-wf}

La configuración automatizada ha finalizado. Ahora puede visitar la propiedad móvil de la etiqueta, configurar las reglas o el elemento de datos y empezar a enviar notificaciones push con Adobe Journey Optimizer.

![](assets/mobile-wf-done.png)


**Temas relacionados**

* [Introducción a las notificaciones push](get-started-push.md)
* [Flujo y componentes de datos de notificaciones push](push-gs.md)
* [Configuración del canal push](push-configuration.md)
* [Informe de notificaciones push](../reports/journey-global-report.md#push-global)
* [Crear una notificación push](create-push.md)
