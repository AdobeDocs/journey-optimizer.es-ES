---
solution: Journey Optimizer
product: journey optimizer
title: Compruebe y pruebe sus mensajes móviles
description: Obtenga información sobre cómo comprobar y enviar mensajes móviles en Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
TQID: https://experienceleague.adobe.com/JPjBxyZzo13tgSLo0dqd5bFOwn9C6MHkA-DjLzlAdEI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 534
ht-degree: 2%

---

# Compruebe y envíe su mensaje móvil {#send-sms}

## Previsualización del mensaje móvil {#preview-sms}

Una vez definido el contenido del mensaje, puede previsualizar su contenido mediante cualquiera de los métodos de simulación:

* Haga clic en **[!UICONTROL Simular contenido]** para probar las variaciones de contenido con datos de entrada de muestra o generación automática de IA. [Aprenda a simular variaciones de contenido](../test-approve/simulate-sample-input.md)
* Haga clic en **[!UICONTROL Simular contenido]** y, a continuación, seleccione **[!UICONTROL Simular contenido (perfiles de AEP)]** en el menú desplegable para previsualizarlo con perfiles de prueba.

![](assets/sms_preview_2.png)

Encontrará información detallada sobre cómo obtener una vista previa y probar contenido en la sección [Administración de contenido](../content-management/preview-test.md).

### Codificación de caracteres y límites {#sms-character-limits}

Se muestra un recuento de caracteres al acceder a cualquiera de los métodos de simulación desde **[!UICONTROL Simular contenido]** para ayudar a planificar y administrar los mensajes de Mobile.

![](assets/sms_preview_3.png)

Journey Optimizer utiliza la codificación UTF-8 en su editor de SMS, lo que le permite escribir o pegar caracteres de doble byte o Unicode. Estos caracteres se transmiten al proveedor de servicios para su envío. La mayoría de los proveedores de SMS utilizan la codificación de 7 bits GSM para mensajes estándar con un límite de 160 caracteres y cambian a UTF-16 (UCS-2) cuando se detectan caracteres no GSM con un límite de 70 caracteres.

Tenga en cuenta que el recuento de caracteres no refleja las variaciones introducidas por la personalización dinámica o los caracteres especiales de 7 bits no GSM.

>[!IMPORTANT]
>
>Los informes de envío de SMS de Journey Optimizer no tienen en cuenta los mensajes concatenados y la personalización dinámica, por lo que es posible que no reflejen el número real de mensajes enviados desde el proveedor. Para obtener información detallada sobre el uso y la facturación, póngase en contacto con su representante de Adobe.
>
>Para conocer las prácticas recomendadas para minimizar los cargos adicionales por facturación SMS, consulte [Prácticas recomendadas por SMS para la optimización de caracteres](mobile-cost-optimization.md).

## Validación del contenido {#sms-validate}

>[!NOTE]
>
> Para mejorar la capacidad de envío, utilice los números de teléfono en los formatos admitidos por el proveedor. Por ejemplo, Twilio y Sinch solo admiten números de teléfono en formato E.164.

Debe comprobar las alertas en la sección superior del editor. Algunas son simples advertencias, pero otras pueden impedir que envíe el mensaje. Pueden producirse dos tipos de alertas: advertencias y errores.

![](assets/sms-alert-button.png)

* **Advertencias** se refieren a recomendaciones y prácticas recomendadas. Por ejemplo, se muestra un mensaje de advertencia si el mensaje de Mobile está vacío o si se pueden superar los límites de caracteres con contenido dinámico.

  **Límites de caracteres:** 160 caracteres por segmento (GSM de 7 bits), 70 para Unicode/emojis, hasta un total de 1500 caracteres.

* **Los errores** le impiden probar o activar la recorrido o publicar la campaña, siempre y cuando no se resuelvan. Por ejemplo, un mensaje de error le advierte cuando falta la línea de asunto.

La alerta **&quot;Se ha superado el límite de caracteres de texto SMS&quot;** puede aparecer incluso cuando el mensaje simulado sea más corto porque la validación calcula la **longitud máxima posible** mediante la evaluación de todas las ramas condicionales, campos de personalización y contenido dinámico en su mayor longitud.

La validación calcula la longitud máxima de todos los datos de perfil posibles, mientras que la simulación muestra la salida real de un perfil de prueba.

## Envío de mensajes móviles {#sms-send}

>[!IMPORTANT]
>
> Si la campaña está sujeta a una directiva de aprobación, deberá solicitar la aprobación para poder enviar los mensajes de Mobile. [Más información](../test-approve/gs-approval.md)

Cuando el mensaje de Mobile esté listo, completa la configuración de tu [recorrido](../building-journeys/journey-gs.md) o [campaña](../campaigns/create-campaign.md) para enviarlo.

**Temas relacionados**

* [Configuración del canal de SMS](mobile-configuration.md)
* [Informes de SMS/RCS/MMS](../reports/journey-global-report-cja-sms.md)
* [Creación de un mensaje móvil](create-mobile-message.md)
* [Añadir un mensaje en un recorrido](../building-journeys/journey-action.md)
