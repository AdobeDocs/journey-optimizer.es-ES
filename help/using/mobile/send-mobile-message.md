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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c41e8697-e629-4c38-96b3-564faaa17acfid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a4c92daab69394e6a736517f2e23a941135f7eb4
workflow-type: tm+mt
source-wordcount: 536
ht-degree: 1%

---

# Compruebe y envíe su mensaje móvil {#send-sms}

## Previsualización del mensaje móvil {#preview-sms}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba o datos de entrada de muestra (cargados desde un archivo CSV/JSON o añadidos manualmente) para previsualizar su contenido. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje.

Para ello, haga clic en **[!UICONTROL Simular contenido]** y compruebe su mensaje con los datos del perfil de prueba.

![](assets/sms_preview_2.png)

Encontrará información detallada sobre cómo obtener una vista previa y probar contenido en la sección [Administración de contenido](../content-management/preview-test.md).

### Codificación de caracteres y límites {#sms-character-limits}

Se muestra un recuento de caracteres al acceder al menú **[!UICONTROL Simular contenido]** para ayudar a planificar y administrar los mensajes de Mobile.

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
* [Informes de SMS/MMS](../reports/journey-global-report-cja-sms.md)
* [Creación de un mensaje móvil](create-mobile-message.md)
* [Añadir un mensaje en un recorrido](../building-journeys/journey-action.md)
