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
source-git-commit: d11d389259057b20c3803643ca40266b9cb4302c
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Compruebe y envíe su mensaje de LINE {#send-line}

## Previsualización del mensaje de texto {#preview-line}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente para previsualizar su contenido. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje. [Aprenda a probar el contenido con datos de entrada de ejemplo](../test-approve/simulate-sample-input.md)

Para ello, haga clic en **[!UICONTROL Simular contenido]** y compruebe su mensaje con los datos del perfil de prueba.

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
