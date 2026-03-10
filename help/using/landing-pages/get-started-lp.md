---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las páginas de destino
description: Obtenga información sobre las páginas de destino en Journey Optimizer
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: destino, página de destino, inicio, introducción
exl-id: 0da96e32-52ad-4cc3-bac4-844b1f39ed16
source-git-commit: 2240a4bf85d3f5f41a12d128afdc15431dbab75b
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 22%

---

# Introducción a las páginas de destino {#get-started-lp}

Una página de destino es una página web independiente a la que se dirige a un usuario después de hacer clic desde un correo electrónico, un sitio web, un anuncio o cualquier otra ubicación digital.

[!DNL Journey Optimizer] le permite crear y diseñar páginas de aterrizaje para dirigir a los usuarios a formularios en línea en los que pueden optar por recibir sus comunicaciones o un servicio específico, como una newsletter, o excluirse de ellos.

➡️ [Obtenga más información sobre la configuración de suscripciones y la creación de páginas de aterrizaje en este vídeo](#video)

## Cuándo usar páginas de aterrizaje {#when-to-use}

Utilice páginas de aterrizaje cuando desee:

* Permite que los clientes **acepten o excluyan** comunicaciones de marketing o un servicio o boletín específico a partir de un vínculo de un correo electrónico o una campaña, incluidas las listas de suscripción para servicios de destino. [Más información](lp-use-cases.md#subscription-to-a-service)
* **Recopile el consentimiento** antes de enviar comunicaciones y envíe un **correo electrónico de confirmación** tras la inclusión o la exclusión. [Más información](lp-use-cases.md#send-confirmation-email)
* Redirigir a los usuarios a un **formulario web dedicado** sin crear una página externa fuera de [!DNL Journey Optimizer]
* Crear **páginas de aterrizaje adaptables** con las capacidades de diseño de contenido de [!DNL Journey Optimizer]

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="Posible cliente" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong>Creación de páginas de destino</strong>
</div>
<p>
</td>
<td>
<a href="subscription-list.md">
<img alt="Poco frecuente" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>Crear listas de suscripción</strong></a>
</div>
<p></td>
<td>
<a href="design-lp.md">
<img alt="Validación" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="design-lp.md"><strong>Diseño de páginas de destino</strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="Validación" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong>Creación de informes</strong></a>
</div>
<p>
</td>
</tr></table>

## Antes de comenzar {#prerequisites}

Antes de crear una página de aterrizaje, complete estos pasos de configuración:

1. [**Configurar un subdominio**](lp-subdomains.md): configure un subdominio dedicado a alojar sus páginas de aterrizaje.
1. [**Crear un ajuste preestablecido de página de aterrizaje**](lp-presets.md#lp-create-preset): un ajuste preestablecido define el subdominio y otras opciones de configuración aplicadas a las páginas de aterrizaje.
1. [**Crear una lista de suscripción**](subscription-list.md) (para casos de uso de suscripción): obligatorio si desea que los clientes se suscriban o cancelen su suscripción a un servicio específico.

## Funcionamiento {#how-it-works}

La creación y la implementación de una página de aterrizaje siguen esta secuencia:

1. [**Crear y configurar la página de aterrizaje**](create-lp.md): seleccione un ajuste preestablecido, configure la página principal y agregue las subpáginas necesarias.
1. [**Diseñar la página**](design-lp.md): cree el contenido de la página y el formulario con el editor de arrastrar y soltar de [!DNL Journey Optimizer].
1. [**Probar**](create-lp.md#test-landing-page) y [**publicar**](create-lp.md#publish-landing-page) su página de aterrizaje: Previsualice la página, pruebe el comportamiento del formulario y, a continuación, publíquelo para activarlo.
1. [**Vínculo en un mensaje o recorrido**](../email/message-tracking.md#insert-links): agregue la dirección URL de la página de aterrizaje a un correo electrónico, una campaña o una acción de recorrido para que los clientes puedan llegar a ella.

## Vídeo práctico{#video}

El siguiente vídeo muestra cómo crear una lista de suscripción, configurar páginas de aterrizaje para la inclusión o exclusión de un servicio, integrar la opción de inclusión/exclusión en un mensaje y configurar recorridos relevantes.

>[!VIDEO](https://video.tv.adobe.com/v/344397?captions=spa&quality=12&learn=on)
