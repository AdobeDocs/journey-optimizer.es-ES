---
solution: Journey Optimizer
product: journey optimizer
title: Content Credentials en el asistente de IA
description: Descubra cómo Adobe Journey Optimizer aplica automáticamente Content Credentials a las imágenes generadas o editadas con AI Assistant y qué significa esto para su contenido.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
hide: true
source-git-commit: 556502a5c45ad920827785a9950bc5f7bbc4ca8f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# Content Credentials en el asistente de IA {#generative-content-credentials}

>[!BEGINSHADEBOX]

**En esta página:** Conozca qué acciones del Asistente de IA adjuntan Content Credentials, qué significa esto para las imágenes que combinan varias fuentes de IA generativas y qué se transfiere cuando el contenido se mueve entre aplicaciones.

>[!ENDSHADEBOX]

>[!INFO]
>
>Están surgiendo nuevas leyes en torno a la transparencia generativa de la IA, y Adobe está trabajando para cumplir con los requisitos aplicables en todas las jurisdicciones. Content Credentials es la herramienta de procedencia que utiliza Adobe para cumplir los requisitos de estas leyes.

Los Content Credentials son metadatos duraderos e invisibles que registran cómo se creó o editó un fragmento de contenido. Cuando se utiliza un asistente de IA en Adobe Journey Optimizer para generar o editar una imagen con herramientas de IA generativa, Content Credentials se adjunta automáticamente a esa imagen y no es necesario que realice ninguna acción.

## Acciones que adjuntan Content Credentials {#cc-workflows}

La siguiente tabla resume cuándo se adjuntan Content Credentials, en función de la acción de imagen realizada en el asistente de IA.

| Acción | Descripción | ¿Content Credentials adjunto? | Ejemplo de caso de uso |
| --- | --- | --- | --- |
| **Generar una imagen** | Cree una nueva imagen a partir de un mensaje de texto, de una imagen de referencia o genere una imagen similar | Siempre. La imagen se genera mediante IA generativa, por lo que siempre lleva una Content Credential nueva. | Se genera una imagen de titular para una campaña de correo electrónico a partir de un mensaje de texto que describe el elemento visual deseado. |
| **Recortar una imagen** (recorte central o inteligente) | Ajuste de una imagen a las dimensiones solicitadas | Solo si la imagen de origen ya tenía un Content Credential. Al recortar se vuelven a crear los píxeles de la imagen, lo que normalmente borraría esa Content Credential, por lo que el Asistente de IA la lee de la imagen de origen antes de recortarla y, a continuación, la vuelve a crear y a adjuntar al resultado recortado. El recorte en sí no agrega una nueva acción de IA generativa, sino que conserva la existente. | Se recorta una imagen de titular generada para que se ajuste a una página web: la Content Credential se conserva durante el recorte. </br> Una foto de archivo cargada que se utiliza como fondo de notificación push se recorta para ajustarse a la pantalla: como la foto de archivo no lleva ninguna acción de IA generativa, no se crea ningún Content Credential. |
| **Agregar una superposición de texto** | Procesar texto generado sobre una imagen de fondo | Solo si la imagen de fondo ya tenía un Content Credential. Al procesar la superposición, se genera una nueva imagen del fondo más el texto, que normalmente borraría ese Content Credential, por lo que AI Assistant la lee de antemano de la imagen de fondo y luego la reconstruye y la vuelve a adjuntar al resultado. El paso de superposición no agrega una nueva acción de IA generativa. | Un titular promocional se procesa como una superposición de texto en una imagen de fondo generada para una página de aterrizaje: se conserva la Content Credential de la imagen de fondo. |
| **Imágenes de superposición** | Componer dos o más imágenes juntas | Si alguna de las imágenes de origen tiene una Content Credential, la imagen combinada las lleva todas, combinadas en una sola Content Credential. La composición produce una nueva imagen a partir de las fuentes, que normalmente borraría esas Content Credentials, por lo que el asistente de IA lee cada una antes de la composición y luego crea una sola Content Credential combinada que enumera todas las fuentes que contribuyeron con una acción de IA generativa. | Una imagen de producto generada se compone de un fondo generado para un encabezado de correo electrónico: el resultado lleva una Content Credential que refleja ambas fuentes de IA generativas. <br> Dos fotos de marca cargadas se componen en un collage: como ninguna de las fuentes lleva una acción de IA generativa, no se crea ningún Content Credential. |

## Tipos de contenido y su ámbito {#cc-content-types}

* **Imágenes**: Cubiertas. Las Content Credentials se adjuntan cuando las imágenes se generan con IA generativa y se conservan mediante las operaciones de recorte, superposición de texto y superposición de imágenes realizadas por el asistente de IA.
* **Texto**: No aplicable. Las salidas de solo texto del asistente de IA, como la generación de copias, la traducción y las sugerencias de alineación de marca, no requieren Content Credentials.

## Qué sucede a medida que se mueve el contenido {#cc-content-moves}

Content Credentials viajar con el archivo de imagen. Cuando se descarga o exporta una imagen generada o editada con IA generativa desde Adobe Journey Optimizer, se conservan sus Content Credentials. [Más información sobre Content Credentials](https://helpx.adobe.com/es/firefly/using/content-credentials.html){target="_blank"}.

Es posible que algunas formas de introducir imágenes en el contenido, como extraer una imagen de una PDF o de una fuente incrustada (base64), no conserven la Content Credential original. En estos casos, no se puede leer ningún Content Credential del origen y no se crea ninguno para el resultado.

## Recursos adicionales

* [Adobe Content Credentials](https://helpx.adobe.com/es/firefly/using/content-credentials.html){target="_blank"}: Obtenga más información sobre cómo funciona Content Credentials en todos los productos de Adobe.
* [Directrices de usuario de IA generativa de Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [Mecanismos de protección y limitaciones](gs-generative.md#generative-guardrails)
