---
solution: Journey Optimizer
product: journey optimizer
title: Previsualización, validación y envío del mensaje de LINE
description: Obtenga información sobre cómo obtener una vista previa y validar un mensaje de LINE, resolver advertencias y errores, solicitar la aprobación cuando sea necesario y activarlo o publicarlo en un recorrido o campaña
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: fd8437c6-0052-4116-af60-5624569bda65
TQID: https://experienceleague.adobe.com/Bfu4AL1axI4XUq0PKXuN0PnnxNvq4MB-O7Bzz66mtbU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 94a7cd6e4e89b2c8a4a09cfb4fbfc173ca76c391
workflow-type: tm+mt
source-wordcount: 400
ht-degree: 2%

---


# Previsualización, validación y envío del mensaje de LINE {#send-line}

>[!BEGINSHADEBOX]

**En esta página:** Previsualice y valide su mensaje de LINE, resuelva advertencias y errores, solicite la aprobación cuando sea necesario y complete la configuración de recorrido o campaña para enviar el mensaje.

>[!ENDSHADEBOX]

## Antes de comenzar {#before-you-start}

Antes de empezar, asegúrese de que:

* LINE está habilitado para su organización. Si LINE no está disponible, póngase en contacto con su representante de Adobe para solicitar la activación.
* Una configuración de canal de LINE está disponible en Journey Optimizer. Consulte [Configurar el canal LINE](./line-configuration.md).
* Ha agregado una acción LINE a un recorrido o campaña y ha definido el contenido del mensaje. Consulte [Crear un mensaje de LINE](./create-line.md).

## Previsualización del mensaje de LINE {#preview-line}

Después de definir el contenido del mensaje, use **[!UICONTROL Simular contenido]** para obtener una vista previa del mensaje antes de enviarlo.

Puede utilizar cualquiera de las siguientes opciones:

| Opción de simulación | Úselo para lo siguiente |
| --- | --- |
| **[!UICONTROL Simular contenido]** | Pruebe las variaciones de contenido con datos de entrada de muestra o generación automática de IA. |
| **[!UICONTROL Simular contenido]** > **[!UICONTROL Simular contenido (perfiles de AEP)]** | Vista previa del mensaje con perfiles de prueba. |

Revise cada variación y compruebe que el contenido del mensaje y los valores personalizados se muestran según lo esperado.

Para obtener información detallada sobre la vista previa y la prueba de contenido, consulte [Previsualizar y probar contenido](../content-management/preview-test.md).

## Validación del contenido {#line-validate}

Antes de continuar, revise las alertas que se muestran en la parte superior del editor de mensajes.

Journey Optimizer muestra dos tipos de alertas:

* **Advertencias** son recomendaciones o sugerencias de prácticas recomendadas. No impiden que pruebe o envíe el mensaje.
* **Errores** identifican problemas que deben resolverse antes de que pueda probar o activar el recorrido o publicar la campaña.

Resuelva todos los errores antes de continuar. Aborde las advertencias cuando indiquen que el mensaje puede no proporcionar la experiencia del cliente deseada.

## Solicitar aprobación cuando sea necesario {#line-approval}

Si la campaña está sujeta a una directiva de aprobación, solicite la aprobación antes de enviar el mensaje.

Ver [Más información sobre cómo solicitar aprobación](../test-approve/gs-approval.md).

## Envío del mensaje de LINE {#line-send}

Cuando el mensaje esté listo, vuelva al recorrido o a la campaña que contiene la acción LINE y complete su configuración:

* **Recorrido:** Complete la configuración del recorrido y, a continuación, active el recorrido.
* **Campaña:** Complete la configuración de la campaña y después publique la campaña.

Si no puede activar el recorrido ni publicar la campaña, vuelva al editor de mensajes y resuelva los errores restantes.

## Tareas relacionadas {#related-tasks}

* [Introducción a LINE](./get-started-line.md)
* [Creación de un mensaje de LINE](./create-line.md)
* [Configuración del canal LINE](./line-configuration.md)

{{$include /help/_includes/do-not-localize/line/ai-augmented-send-line.md}}
