---
title: Introducción a las políticas de decisiones
description: Aprenda a trabajar con políticas de decisiones para entregar ofertas.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: 2dfc9c2db5af1b9b74f7405a68e85563f633a54f
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 26%

---

# Introducción a las políticas de decisión {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="¿Qué es una decisión?"
>abstract="Las políticas de decisión contienen toda la lógica de selección para que el motor de decisión elija el mejor contenido. Las políticas de decisión son específicas de la campaña. Su meta es seleccionar las mejores ofertas para cada perfil, mientras que la creación de campañas le permite indicar cómo se deben presentar los elementos de decisión seleccionados, incluidos los atributos de elemento que se deben incluir en el mensaje."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Acerca de la toma de decisiones"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="Definición de una política de decisión"
>abstract="Una política de decisión le permite elegir los mejores elementos del motor de decisión y enviarlos al público adecuado."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Acerca de la toma de decisiones"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="Política de decisión"
>abstract="Una política de decisión permite elegir los mejores elementos del motor de decisión y enviarlos a cada público."

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="Ubicación"
>abstract="Una ubicación determina dónde aparecen los elementos devueltos por el motor de decisión en un mensaje. Puede realizar un seguimiento de su rendimiento en diferentes ubicaciones en la creación de informes."

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="Seleccionar atributos de decisión del catálogo"
>abstract="Los atributos de decisión se almacenan en el esquema del catálogo. Seleccione un atributo que desee utilizar aquí desde el catálogo seleccionado."

Las políticas de decisión son contenedores para sus ofertas que aprovechan el motor de decisión para devolver dinámicamente el mejor contenido para entregar a cada miembro de la audiencia. Su objetivo es seleccionar las mejores ofertas para cada perfil, mientras que la creación de campañas/recorridos le permite indicar cómo se deben presentar los elementos de decisión seleccionados, incluidos los atributos de elemento que se deben incluir en el mensaje.

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Protecciones y limitaciones

* **Canales compatibles** - Las directivas de decisión están disponibles para estos canales : Experiencia basada en código, Correo electrónico, SMS y Notificaciones push.
* **Requisito de notificaciones push para SDK**: Experience Decisioning con notificaciones push requiere una versión específica de Mobile SDK. Antes de implementar esta característica, compruebe [las notas de la versión](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} para identificar la versión requerida y asegúrese de haber actualizado según corresponda. También puede ver todas las versiones de SDK disponibles para su plataforma en [esta sección](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.
* **Páginas espejo de correo electrónico**: por ahora, los elementos de decisión no se representan en las páginas espejo de correo electrónico.
* **Tipo de seguimiento y vínculos**: para realizar el seguimiento de los vínculos generados por la toma de decisiones, defina estos vínculos en el esquema como &quot;Decisioning Assets&quot;. Los vínculos basados en atributos no se pueden rastrear.
* **Anidado de directivas de decisión en correos electrónicos**: no puede anidar varias directivas de decisión dentro de un componente de correo electrónico principal que ya tenga asociada una directiva de decisión.
* **recorridos/campañas duplicados con toma de decisiones**: si duplica un recorrido o una campaña que incluye una directiva de decisión, la versión duplicada hace referencia al correo electrónico o la experiencia basada en código original, lo que provoca errores. Siempre vuelva a configurar la política de decisión después de la duplicación.
* **Políticas de consentimiento**: las actualizaciones de las políticas de consentimiento tardan hasta 48 horas en surtir efecto. Si una directiva de decisión hace referencia a un atributo vinculado a una directiva de consentimiento actualizada recientemente, los cambios no se aplican inmediatamente.

  Del mismo modo, si se añaden nuevos atributos de perfil sujetos a una directiva de consentimiento a una directiva de decisión, se pueden utilizar, pero la directiva de consentimiento asociada a ellos no se aplicará hasta que haya pasado el retraso.

  Las políticas de consentimiento solo están disponibles para las organizaciones con el complemento Adobe Healthcare Shield o Privacy and Security Shield.

* **Clasificación de IA**: por ahora, la clasificación de IA no es compatible con el canal de correo electrónico en recorridos con toma de decisiones.

* **Plantillas de contenido**: ninguna directiva de decisión configurada en su contenido se guardará en la plantilla. Si aplica la plantilla a otra acción, debe volver a configurar la directiva.

## Pasos clave {#key}

Los pasos principales para aprovechar las políticas de decisión en los mensajes son los siguientes:

1. **Crear una directiva de decisión**

   Añada una política de decisión en el mensaje y configure el número de elementos que desea devolver, la estrategia de selección y las opciones de reserva.

   ➡️ [Aprenda a crear una directiva de decisión](../experience-decisioning/create-decision-policy.md)

1. **Usar la directiva de decisión en el contenido**

   Personalice el contenido con el resultado de la política de decisión insertando los atributos de los elementos de decisión que desee mostrar en el mensaje

   ➡️ [Aprenda a utilizar las directivas de decisión en los mensajes](../experience-decisioning/create-decision-policy.md)

## Vídeotutoriales {#video}

Aprenda a utilizar Decisioning para personalizar correos electrónicos para su audiencia.

>[!VIDEO](https://video.tv.adobe.com/v/3479213?captions=spa&quality=12)

Aprenda a utilizar Decisioning para personalizar las notificaciones push para su audiencia.

>[!VIDEO](https://video.tv.adobe.com/v/3479213?captions=spa&quality=12)

Aprenda a utilizar Decisioning para personalizar los mensajes SMS para su audiencia.

>[!VIDEO](https://video.tv.adobe.com/v/3479532?captions=spa&quality=12)
