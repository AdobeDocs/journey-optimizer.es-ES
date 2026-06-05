---
title: Introducción a las políticas de decisiones
description: Aprenda a trabajar con políticas de decisiones para entregar ofertas.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/E1BsOCI4d-f7PCFVEzNlWFj6Odh4T-9S3oq295tmCsE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 1b4e12b9433a819a3be34c4f01c489af1d6091ed
workflow-type: tm+mt
source-wordcount: 704
ht-degree: 34%

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

Las políticas de decisión son contenedores para sus ofertas que aprovechan el motor de tomas de decisiones para devolver de forma dinámica el mejor contenido para entregar a cada miembro del público. Su objetivo es seleccionar las mejores ofertas para cada perfil, mientras que la creación de campañas/recorridos le permite indicar cómo se deben presentar los elementos de decisión seleccionados, incluidos los atributos de elemento que se deben incluir en el mensaje.

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Protecciones y limitaciones

* **Canales compatibles**: experiencia basada en código, correo electrónico, SMS, notificaciones push y correo directo.

* **Requisito de notificaciones push para SDK**: Experience Decisioning con notificaciones push requiere una versión específica de Mobile SDK. Antes de implementar esta característica, compruebe [las notas de la versión](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} para identificar la versión requerida y asegúrese de haber actualizado según corresponda. También puede ver todas las versiones de SDK disponibles para su plataforma en [esta sección](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.
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

>[!VIDEO](https://video.tv.adobe.com/v/3476158?quality=12)

Aprenda a utilizar Decisioning para personalizar las notificaciones push para su audiencia.

>[!VIDEO](https://video.tv.adobe.com/v/3479199?quality=12)

Aprenda a utilizar Decisioning para personalizar los mensajes SMS para su audiencia.

>[!VIDEO](https://video.tv.adobe.com/v/3479529?quality=12)
