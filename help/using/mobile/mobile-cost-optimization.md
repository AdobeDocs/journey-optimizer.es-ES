---
solution: Journey Optimizer
product: journey optimizer
title: Prácticas recomendadas de SMS para la optimización de costes
description: Aprenda a optimizar los costes de los mensajes SMS administrando los límites de caracteres, la codificación y la personalización en Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: c8c156da-8482-4932-9c15-45ab83c173e7
TQID: https://experienceleague.adobe.com/ccUbyMiVNBULBlaYAb-z6-WFGcWURtmelyKUy7v2g2o
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 1%

---

# Prácticas recomendadas para la optimización del coste de SMS {#sms-cost-optimization}

Los mensajes SMS suelen facturar los proveedores en función de un límite de 160 caracteres por mensaje. El envío de mensajes SMS puede conllevar costes adicionales si los mensajes se dividen en varias partes.

Siga estas directrices para optimizar su estrategia de mensajería y reducir gastos.

## Mantener mensajes cortos {#keep-messages-short}

Journey Optimizer permite hasta 1500 caracteres en el cuerpo de un mensaje SMS. Aparece una advertencia cuando se sobrepasa este límite y los mensajes que superen este umbral generarán un déclencheur de error.

La mayoría de los proveedores de SMS admiten la codificación de 7 bits GSM, donde un solo SMS puede contener hasta 160 caracteres. Los mensajes que superan esta longitud se dividen automáticamente en varias partes del SMS (concatenación):

* **Menos de 160 caracteres**: 1 parte de SMS
* **161-306 caracteres**: 2 partes de SMS
* **307 a 459 caracteres**: 3 partes de SMS

**Para minimizar los costos**, intente mantener los mensajes por debajo de los 160 caracteres para que se cobren como una sola parte de SMS.

Por ejemplo, un mensaje de 1600 caracteres podría consumir 10 créditos SMS, aunque aparezca como un solo mensaje en Journey Optimizer.

## Evite los caracteres especiales que aumentan la longitud {#avoid-special-characters}

Algunos caracteres, como `| ^ &euro; { } [ ] ~ \`, se cuentan como dos caracteres en la codificación GSM. Si incluye estos caracteres, el mensaje podría superar **el límite de 160 caracteres** con mayor rapidez.

## Impedir la codificación UCS-2 {#prevent-ucs2-encoding}

Si el mensaje incluye caracteres que no son GSM, como texto chino o árabe, símbolos de marca comercial o devoluciones graves de herramientas de formato enriquecido, el proveedor codificará el mensaje con UCS-2, que solo admite 70 caracteres por SMS.

El uso de la codificación UCS-2 puede aumentar el recuento de caracteres y, en consecuencia, afectar a la facturación de mensajes con su proveedor de servicios.

Por ejemplo, un mensaje Unicode de 200 caracteres se enviará en 3 partes de SMS.

## Prácticas recomendadas de creación {#authoring-best-practices}

Componga el mensaje SMS final directamente en Journey Optimizer o péguelo desde aplicaciones de texto sin formato.

Evite utilizar aplicaciones de texto enriquecido, ya que pueden introducir caracteres ocultos o saltos de línea que entran en déclencheur con la codificación UCS-2, lo que podría aumentar tanto el número de partes del SMS como los costes asociados.

## Compruebe el recuento de caracteres antes de enviar {#check-character-count}

Use aplicaciones de texto sin formato o cualquier método de simulación en **[!UICONTROL Simular contenido]** para comprobar los recuentos de caracteres.

Aunque Journey Optimizer muestra un recuento de caracteres, incluidos los espacios, durante la simulación de contenido, tenga en cuenta que:

* No incluye **not** caracteres generados a través de la personalización dinámica o ciertos caracteres especiales.

* El **recuento x/1500** sirve como indicador visual del límite técnico de carga útil, no del límite por mensaje; por ejemplo, el límite de 7 bits de GSM de 160 caracteres.

* Adobe admite la codificación UTF-8 en el editor, que difiere de la codificación GSM-7 bits.

## Explicación de los informes {#understanding-reporting}

**Informes de Journey Optimizer** cuenta el mensaje completo como un envío, independientemente de las partes del SMS.

**Informes del proveedor** reflejan el número real de partes de mensajes SMS utilizadas para la entrega y se debe hacer referencia a ellos para confirmar la facturación y cualquier posible sobrecarga. Si Adobe es su proveedor de SMS a través de Sinch, recibirá este informe de facturación por separado mensualmente.

## Consideraciones de Personalization {#personalization-considerations}

La personalización dinámica puede aumentar la longitud de un mensaje. Por ejemplo, sustituir una variable por un nombre largo puede añadir caracteres adicionales.

## Recursos adicionales {#additional-resources}

Revise los caracteres admitidos y las reglas de codificación en [Sinch Character Support Guide](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)
