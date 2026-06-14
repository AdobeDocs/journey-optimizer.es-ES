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
TQID: https://experienceleague.adobe.com/wr4XGNostKoN8jZ50VRAQPoGg9tsNhMOyJGEt1mASso
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b19d9237-76be-466d-a869-aacf2d72205f
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2956c3df01f4b2e753111ecf54163ec4084fecf2
workflow-type: tm+mt
source-wordcount: 781
ht-degree: 91%

---

# Introducción a las páginas de destino {#get-started-lp}

>[!BEGINSHADEBOX]

**En esta página:** Las páginas de aterrizaje convierten un clic de un correo electrónico, un anuncio o una campaña en un destino web dedicado en el que los clientes se excluyen o excluyen, administran sus preferencias y comparten datos de perfil, lo que le ayuda a aumentar las audiencias consentidas y a capturar los datos de origen que alimentan la personalización.

>[!ENDSHADEBOX]

Una página de destino es una página web independiente a la que se dirige a un usuario después de hacer clic desde un correo electrónico, un sitio web, un anuncio o cualquier otra ubicación digital.

[!DNL Journey Optimizer] le permite crear y diseñar páginas de destino para dirigir a los usuarios a formularios en línea, donde pueden optar por recibir o rechazar la recepción de comunicaciones, o suscribirse a un servicio específico, como un newsletter.

➡️ [Obtenga más información sobre la configuración de suscripciones y la creación de páginas de destino en este vídeo](#video)

## Cuándo usar páginas de destino {#when-to-use}

Utilice páginas de destino cuando desee:

* Permitir que los clientes **acepten o rechacen** comunicaciones de marketing o un servicio o newsletter específico a partir de un vínculo de un correo electrónico o una campaña, incluidas las listas de suscripción para servicios específicos. [Más información](lp-use-cases.md#subscription-to-a-service)
* **Obtener el consentimiento** antes de enviar comunicaciones y enviar un **correo electrónico de confirmación** al darse de alta o darse de baja. [Más información](lp-use-cases.md#send-confirmation-email)
* **Capturar o actualizar los datos de perfil** usando formularios en páginas de destino de **[!UICONTROL captura de datos]** para generar perfiles progresivos, preferencias, registros y escenarios similares. [Más información](#data-capture-lp)
* Redirigir a los usuarios a un **formulario web específico** sin crear una página externa fuera de [!DNL Journey Optimizer]
* Crear **páginas de destino adaptables** con las capacidades de diseño de contenido de [!DNL Journey Optimizer]

### Captura de datos con páginas de destino {#data-capture-lp}

Las páginas de destino de **[!UICONTROL Captura de datos]** le permiten incrustar formularios publicados para que los visitantes puedan enviar atributos escritos en el conjunto de datos de [!DNL Adobe Experience Platform] a través de la conexión de flujo continuo configurada en el ajuste preestablecido de formulario. [Aprenda a crear e incrustar formularios en una página de destino](lp-forms.md)

>[!NOTE]
>
>Se admite la captura de datos mediante formularios de página de destino para **perfiles conocidos** (perfiles existentes identificados en [!DNL Adobe Experience Platform]). La página de destino debe abrirse desde un **vínculo personalizado** (por ejemplo, desde una campaña de correo electrónico) para que la identidad del perfil pueda resolverse cuando se cargue la página.

Los siguientes son ejemplos de uso:

1. **Enriquecimiento progresivo del perfil**: recopile atributos adicionales de clientes conocidos, como número de teléfono, fecha de nacimiento o ubicación, a través de una página de destino personalizada para enriquecer su perfil de [!DNL Experience Platform] existente para la segmentación y personalización.

2. **Actualización del centro de preferencias**: permite que los suscriptores conocidos administren sus preferencias de comunicación (intereses de canal y tema) a través de una página de destino, con cambios que normalmente se reflejan en su perfil [!DNL Experience Platform] en un plazo aproximado de 15 minutos.

3. **Registro de evento o seminario web**: capture datos específicos de evento de perfiles conocidos en una página de registro, actualice el perfil con atributos de registro y active un recorrido de confirmación.

4. **Inscripción de fidelidad o programa**: permita que los clientes existentes se inscriban en programas de fidelidad o niveles de pertenencia enviando detalles adicionales a través de una página de destino, enriqueciendo el perfil para la segmentación descendente.

5. **Participación en concursos**: permita que los clientes conocidos participen en concursos o sorteos a través de un formulario de página de destino; capture detalles específicos de la entrada (respuestas, preferencias o declaraciones) y escríbalos en el perfil para apoyar la elegibilidad, la selección de ganadores y los recorridos de seguimiento.

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
<img alt="Lista de formularios para páginas de destino en Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Uso de los formularios en las páginas de destino</strong></a>
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

Antes de crear una página de destino, complete estos pasos de configuración:

1. **Configurar un subdominio**: configure un subdominio específico para alojar sus páginas de destino. [Más información](lp-subdomains.md)
1. **Crear un ajuste preestablecido de página de destino**: un ajuste preestablecido define el subdominio y otras opciones de configuración aplicadas a las páginas de aterrizaje. [Más información](lp-presets.md#lp-create-preset)
1. **Crear una lista de suscripción** (para casos de uso de suscripción): obligatorio si desea que los clientes se suscriban o cancelen su suscripción a un servicio específico. [Más información](subscription-list.md)
1. **Crear un formulario** (para casos de uso de captura de datos): requerido cuando desee incrustar un formulario en una página de destino de **[!UICONTROL Captura de datos]** y enviar los datos a [!DNL Experience Platform]. [Más información](lp-forms.md)

## Cómo funciona {#how-it-works}

La creación y la implementación de una página de destino siguen esta secuencia:

1. **Crear y configurar la página de destino**: seleccione un ajuste preestablecido, configure la página principal y añada las subpáginas necesarias. [Más información](create-lp.md#create-landing-page)
1. **Diseñar la página**: cree el contenido de la página y el formulario con el editor de arrastrar y soltar de [!DNL Journey Optimizer]. [Más información](design-lp.md)
1. **Pruebe y publique su página de destino**: previsualice la página, pruebe el comportamiento del formulario y, a continuación, publique para activarla. [Más información](create-lp.md#test-landing-page)
1. **Vínculo en un mensaje o recorrido**: añada la dirección URL de la página de destino a un correo electrónico, una campaña o una acción de recorrido para que los clientes puedan llegar a ella. [Más información](../email/message-tracking.md#insert-links)

## Vídeo tutorial{#video}

El siguiente vídeo muestra cómo crear una lista de suscripción, configurar páginas de destino para ofrecer suscripciones a un servicio o cancelaciones del mismo, integrar la opción de suscripción/cancelación de suscripción en un mensaje y configurar los recorridos relevantes.

>[!VIDEO](https://video.tv.adobe.com/v/344397?captions=spa&quality=12&learn=on)

➡️ **Véalo en la práctica:** Explore [casos de uso de páginas de aterrizaje](lp-use-cases.md) para ver ejemplos paso a paso sobre administración de suscripciones, correos electrónicos de confirmación y escenarios de captura de datos.
