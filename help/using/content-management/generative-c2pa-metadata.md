---
solution: Journey Optimizer
product: journey optimizer
title: Metadatos de C2PA en el asistente de IA
description: Descubra cómo Adobe Journey Optimizer aplica automáticamente los metadatos de C2PA a las imágenes generadas o editadas con el asistente de IA y qué significa esto para su contenido.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
hide: true
source-git-commit: 22a514528dd9746bbf45da59a20d6fe17feb6e40
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# Metadatos de C2PA en el asistente de IA {#generative-content-credentials}

>[!BEGINSHADEBOX]

**En esta página:** Descubra qué acciones del Asistente de IA adjuntan metadatos de C2PA, qué significa esto para imágenes que combinan varias fuentes de IA generativas y qué se transfiere cuando el contenido se mueve entre aplicaciones.

>[!ENDSHADEBOX]

>[!INFO]
>
>Están surgiendo nuevas leyes en torno a la transparencia generativa de la IA, y Adobe está trabajando para cumplir con los requisitos aplicables en todas las jurisdicciones. Los metadatos de C2PA son la herramienta de procedencia que utiliza Adobe para cumplir los requisitos de estas leyes.

Los metadatos de C2PA son metadatos duraderos e invisibles que registran cómo se creó o editó un fragmento de contenido. Cuando se utiliza el asistente de IA en Adobe Journey Optimizer para generar o editar una imagen con herramientas de IA generativa, los metadatos de C2PA se adjuntan automáticamente a esa imagen y no es necesario que realice ninguna acción.

## Acciones que adjuntan metadatos de C2PA {#cc-workflows}

La siguiente tabla resume cuándo se adjuntan los metadatos de C2PA, en función de la acción de imagen realizada en el asistente de IA.

| Acción | Descripción | ¿Metadatos de C2PA adjuntos? | Ejemplo de caso de uso |
| --- | --- | --- | --- |
| **Generar una imagen** | Cree una nueva imagen a partir de un mensaje de texto, de una imagen de referencia o genere una imagen similar | Siempre. La imagen se genera mediante IA generativa, por lo que siempre lleva metadatos frescos de C2PA. | Se genera una imagen de titular para una campaña de correo electrónico a partir de un mensaje de texto que describe el elemento visual deseado. |
| **Recortar una imagen** (recorte central o inteligente) | Ajuste de una imagen a las dimensiones solicitadas | Solo si la imagen de origen ya tenía metadatos de C2PA. Al recortar se vuelven a crear los píxeles de la imagen, lo que normalmente borraría los metadatos de C2PA, por lo que el Asistente de IA los lee de la imagen de origen antes de recortarlos y, a continuación, los vuelve a crear y a adjuntar al resultado recortado. El recorte en sí no agrega una nueva acción de IA generativa, sino que conserva la existente. | Se recorta una imagen de titular generada para que se ajuste a una página web: los metadatos de C2PA se conservan a través del recorte. </br> Se recorta una foto de archivo cargada que se utiliza como fondo de notificación push para ajustarse a la pantalla: como la foto de archivo no lleva ninguna acción de IA generativa, no se crean metadatos de C2PA. |
| **Agregar una superposición de texto** | Procesar texto generado sobre una imagen de fondo | Solo si la imagen de fondo ya tenía metadatos de C2PA. Al procesar la superposición, se genera una nueva imagen del fondo más el texto, que normalmente borraría esos metadatos de C2PA, por lo que AI Assistant los lee de antemano de la imagen de fondo y luego los reconstruye y vuelve a adjuntar al resultado. El paso de superposición no agrega una nueva acción de IA generativa. | Un titular promocional se procesa como una superposición de texto en una imagen de fondo generada para una página de aterrizaje: se conservan los metadatos de C2PA de la imagen de fondo. |
| **Imágenes de superposición** | Componer dos o más imágenes juntas | Si alguna de las imágenes de origen tiene metadatos de C2PA, la imagen combinada lleva todos ellos, combinados en metadatos de C2PA únicos. La composición produce una nueva imagen a partir de las fuentes, que normalmente borraría esos metadatos de C2PA, por lo que el asistente de IA lee cada uno antes de componer y luego crea un único metadato combinado de C2PA que enumera todas las fuentes que contribuyeron con una acción de IA generativa. | Una imagen de producto generada se compone de un fondo generado para un encabezado de correo electrónico: el resultado lleva metadatos de C2PA que reflejan ambas fuentes de IA generativas. <br> Dos fotos de marca cargadas se componen en un collage: como ninguna de las fuentes lleva una acción de IA generativa, no se crean metadatos de C2PA. |

## Tipos de contenido y su ámbito {#cc-content-types}

* **Imágenes**: Cubiertas. Los metadatos de C2PA se adjuntan cuando las imágenes se generan con IA generativa y se conservan mediante las operaciones de recorte, superposición de texto y superposición de imagen realizadas por el asistente de IA.
* **Texto**: No aplicable. Las salidas de solo texto del asistente de IA, como la generación de copias, la traducción y las sugerencias de alineación de marca, no requieren metadatos de C2PA.

## Qué sucede a medida que se mueve el contenido {#cc-content-moves}

Los metadatos de C2PA viajan con el archivo de imagen. Cuando se descarga o exporta una imagen generada o editada con IA generativa desde Adobe Journey Optimizer, se conservan sus metadatos de C2PA. [Más información acerca de los metadatos de C2PA](https://helpx.adobe.com/es/firefly/using/content-credentials.html){target="_blank"}.

Es posible que algunos métodos para introducir imágenes en el contenido, como extraer una imagen de una PDF o de una fuente incrustada (base64), no conserven los metadatos originales de C2PA. En estos casos, no se pueden leer metadatos de C2PA del origen y no se crea ninguno para el resultado.

## Recursos adicionales

* [Directrices de usuario de IA generativa de Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [Mecanismos de protección y limitaciones](gs-generative.md#generative-guardrails)
* [Transparencia de contenido de IA generativa](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency#related-links)