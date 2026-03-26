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
source-git-commit: d0dd382521aeb2c7e18dc547c2ec55fa1472ab8d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 14%

---

# Introducción a las páginas de destino {#get-started-lp}

Una página de destino es una página web independiente a la que se dirige a un usuario después de hacer clic desde un correo electrónico, un sitio web, un anuncio o cualquier otra ubicación digital.

[!DNL Journey Optimizer] le permite crear y diseñar páginas de aterrizaje para dirigir a los usuarios a formularios en línea en los que pueden optar por recibir sus comunicaciones o un servicio específico, como una newsletter, o excluirse de ellos.

➡️ [Obtenga más información sobre la configuración de suscripciones y la creación de páginas de aterrizaje en este vídeo](#video)

## Cuándo usar páginas de aterrizaje {#when-to-use}

Utilice páginas de aterrizaje cuando desee:

* Permite que los clientes **acepten o excluyan** comunicaciones de marketing o un servicio o boletín específico a partir de un vínculo de un correo electrónico o una campaña, incluidas las listas de suscripción para servicios de destino. [Más información](lp-use-cases.md#subscription-to-a-service)
* **Recopile el consentimiento** antes de enviar comunicaciones y envíe un **correo electrónico de confirmación** tras la inclusión o la exclusión. [Más información](lp-use-cases.md#send-confirmation-email)
* **Captura o actualiza datos de perfil** usando formularios en **[!UICONTROL páginas de aterrizaje de captura de datos]** para generar perfiles progresivos, preferencias, registros y escenarios similares. [Más información](#data-capture-lp)
* Redirigir a los usuarios a un **formulario web dedicado** sin crear una página externa fuera de [!DNL Journey Optimizer]
* Crear **páginas de aterrizaje adaptables** con las capacidades de diseño de contenido de [!DNL Journey Optimizer]

### Captura de datos con páginas de aterrizaje {#data-capture-lp}

Las páginas de aterrizaje de **[!UICONTROL Captura de datos]** le permiten incrustar formularios publicados para que los visitantes puedan enviar atributos escritos en el conjunto de datos de [!DNL Adobe Experience Platform] a través de la conexión de flujo continuo configurada en el ajuste preestablecido de formulario. [Aprenda a crear e incrustar formularios en una página de aterrizaje](lp-forms.md)

>[!NOTE]
>
>Se admite la captura de datos mediante formularios de página de aterrizaje para **perfiles conocidos** (perfiles existentes identificados en [!DNL Adobe Experience Platform]). La página de aterrizaje debe abrirse desde un **vínculo personalizado** (por ejemplo, desde una campaña de correo electrónico) para que la identidad del perfil pueda resolverse cuando se cargue la página.

Los siguientes son ejemplos de uso:

1. **Enriquecimiento progresivo del perfil**: recopile atributos adicionales de clientes conocidos, como número de teléfono, fecha de nacimiento o ubicación, a través de una página de aterrizaje personalizada para enriquecer su perfil de [!DNL Experience Platform] existente para la segmentación y personalización.

2. **Actualización del centro de preferencias**: permite que los suscriptores conocidos administren sus preferencias de comunicación (intereses de canal y tema) a través de una página de aterrizaje, con cambios que normalmente se reflejan en su perfil [!DNL Experience Platform] en un plazo aproximado de 15 minutos.

3. **Registro de evento o seminario web**: capture datos específicos de evento de perfiles conocidos en una página de registro, actualice el perfil con atributos de registro y almacene en déclencheur un recorrido de confirmación.

4. **Inscripción de fidelidad o programa**: permita que los clientes existentes se inscriban en programas de fidelidad o niveles de pertenencia enviando detalles adicionales a través de una página de aterrizaje, enriqueciendo el perfil para la segmentación descendente.

5. **Participantes en concursos o concursos**: permita que los clientes conocidos participen en concursos o sorteos a través de un formulario de página de aterrizaje; capture detalles específicos de la entrada (respuestas, preferencias o declaraciones) y escríbalos en el perfil para apoyar la elegibilidad, la selección de ganadores y los recorridos de seguimiento.

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
<a href="lp-forms.md">
<img alt="Lista de Forms para páginas de aterrizaje en Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Use formularios en sus páginas de aterrizaje</strong></a>
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

1. **Configurar un subdominio**: configure un subdominio dedicado a alojar sus páginas de aterrizaje. [Más información](lp-subdomains.md)
1. **Crear un ajuste preestablecido de página de aterrizaje**: un ajuste preestablecido define el subdominio y otras opciones de configuración aplicadas a las páginas de aterrizaje. [Más información](lp-presets.md#lp-create-preset)
1. **Crear una lista de suscripción** (para casos de uso de suscripción): obligatorio si desea que los clientes se suscriban o cancelen su suscripción a un servicio específico. [Más información](subscription-list.md)
1. **Crear un formulario** (para casos de uso de captura de datos): requerido cuando desee incrustar un formulario en una página de aterrizaje de **[!UICONTROL Captura de datos]** y enviar envíos a [!DNL Experience Platform]. [Más información](lp-forms.md)

## Funcionamiento {#how-it-works}

La creación y la implementación de una página de aterrizaje siguen esta secuencia:

1. **Crear y configurar la página de aterrizaje**: seleccione un ajuste preestablecido, configure la página principal y agregue las subpáginas necesarias. [Más información](create-lp.md#create-landing-page)
1. **Diseñar la página**: cree el contenido de la página y el formulario con el editor de arrastrar y soltar de [!DNL Journey Optimizer]. [Más información](design-lp.md)
1. **Pruebe y publique su página de aterrizaje**: Previsualice la página, pruebe el comportamiento del formulario y, a continuación, publique para activarla. [Más información](create-lp.md#test-landing-page)
1. **Vínculo en un mensaje o recorrido**: agregue la dirección URL de la página de aterrizaje a un correo electrónico, una campaña o una acción de recorrido para que los clientes puedan llegar a ella. [Más información](../email/message-tracking.md#insert-links)

## Vídeo práctico{#video}

El siguiente vídeo muestra cómo crear una lista de suscripción, configurar páginas de aterrizaje para la inclusión o exclusión de un servicio, integrar la opción de inclusión/exclusión en un mensaje y configurar recorridos relevantes.

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)
