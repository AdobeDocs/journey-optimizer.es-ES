---
solution: Journey Optimizer
product: journey optimizer
title: Comprobación y prueba de los mensajes de texto
description: Obtenga información sobre cómo comprobar y enviar sus mensajes de LINE en Journey Optimizer
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: fd8437c6-0052-4116-af60-5624569bda65
TQID: https://experienceleague.adobe.com/Bfu4AL1axI4XUq0PKXuN0PnnxNvq4MB-O7Bzz66mtbU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 236
ht-degree: 0%

---

# Compruebe y envíe su mensaje de LINE {#send-line}

## Previsualización del mensaje de texto {#preview-line}

Una vez definido el contenido del mensaje, puede previsualizar su contenido mediante cualquiera de los métodos de simulación:

* Haga clic en **[!UICONTROL Simular contenido]** para probar las variaciones de contenido con datos de entrada de muestra o generación automática de IA. [Aprenda a simular variaciones de contenido](../test-approve/simulate-sample-input.md)
* Haga clic en **[!UICONTROL Simular contenido]** y, a continuación, seleccione **[!UICONTROL Simular contenido (perfiles de AEP)]** en el menú desplegable para previsualizarlo con perfiles de prueba.

Encontrará información detallada sobre cómo obtener una vista previa y probar contenido en la sección [Administración de contenido](../content-management/preview-test.md).

## Validación del contenido {#line-validate}

Debe comprobar las alertas en la sección superior del editor. Algunas son simples advertencias, pero otras pueden impedir que envíe el mensaje. Pueden producirse dos tipos de alertas: advertencias y errores.

* **Advertencias** se refieren a recomendaciones y prácticas recomendadas. Por ejemplo, se muestra un mensaje de advertencia si el mensaje de texto está vacío.

* **Los errores** le impiden probar o activar la recorrido o publicar la campaña, siempre y cuando no se resuelvan. Por ejemplo, un mensaje de error le advierte cuando falta la línea de asunto.

## Envío de los mensajes de LINE {#line-send}

>[!IMPORTANT]
>
> Si la campaña está sujeta a una directiva de aprobación, debe solicitar la aprobación para poder enviar los mensajes de texto. [Más información](../test-approve/gs-approval.md)

Cuando el mensaje de LINE esté listo, completa la configuración de tu [recorrido](../building-journeys/journey-gs.md) o [campaña](../campaigns/create-campaign.md) para enviarlo.
