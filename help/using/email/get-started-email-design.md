---
solution: Journey Optimizer
product: journey optimizer
title: Diseño de correos electrónicos
description: Obtenga información sobre cómo diseñar sus correos electrónicos
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: correo electrónico, diseño, stock, activos
exl-id: e4f91870-f06a-4cd3-98b7-4c413233e310
TQID: https://experienceleague.adobe.com/fyUHQD4jpIUI2KdyrGbgktEhNNc4OWYRJ8AkgZhrIoQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: f550d0f2-143d-4093-9463-467fbec95fcc
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 33c1b3dc43472224da63ea2075ee9cbbc0489f17
workflow-type: tm+mt
source-wordcount: 1325
ht-degree: 57%

---

# Introducción al diseño de correo electrónico {#get-started-content-design}

>[!BEGINSHADEBOX]

**En esta página:** aprenda a diseñar el contenido de su correo electrónico en el diseñador de correo electrónico, los pasos clave para crearlo desde cero, el código o el HTML importado, y las prácticas recomendadas que mantienen el procesamiento de sus correos electrónicos en todos los clientes.

>[!ENDSHADEBOX]

Para acceder al Diseñador de correo electrónico y comenzar a diseñar el contenido de su correo electrónico, primero debe [crear un correo electrónico](create-email.md) en un recorrido o una campaña.

A continuación, puede usar [!DNL Journey Optimizer] **funcionalidades de diseño de correo electrónico** para importar el contenido existente o empezar a crear correos electrónicos adaptables desde cero. [Más información](content-from-scratch.md)

El Diseñador de correo electrónico también le permite lo siguiente:

* Aproveche **Adobe Experience Manager Assets Essentials** para enriquecer los correos electrónicos, crear y administrar su propia base de datos de activos. [Más información](../integrations/assets.md)

* Encuentre **fotos de Adobe Stock** para crear su contenido y mejorar su diseño de correo electrónico. [Más información](../integrations/stock.md)

* Mejore la experiencia de los clientes creando mensajes y de correo electrónico personalizados en función de sus atributos de perfil. Más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md).

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Pasos clave para crear contenido de correo electrónico {#key-steps}

Una vez creado un correo electrónico, puede empezar a diseñar su contenido.

1. Desde la pantalla de configuración de recorrido o de campaña, pase por la pantalla **[!UICONTROL Editar contenido]** para acceder al Diseñador de correo electrónico. [Más información](create-email.md#define-email-content)

   ![](assets/email_designer_edit_email_body.png)

1. En la página de inicio del Diseñador de correo electrónico, elija cómo desea diseñar el correo electrónico desde las opciones siguientes:

   * **Diseñe su correo electrónico desde cero** a través de la interfaz del diseñador de correo electrónico y aproveche las imágenes de [Adobe Experience Manager Assets](../integrations/assets.md). Información sobre cómo diseñar el contenido de su correo electrónico en [esta sección](content-from-scratch.md).

   * **Codifique o pegue el HTML sin procesar** directamente en el diseñador de correo electrónico. Información sobre cómo codificar su propio contenido en [esta sección](code-content.md).

     >[!NOTE]
     >
     >En una campaña, también puede seleccionar el botón **[!UICONTROL Editor de código]** del **[!UICONTROL Editar contenido]** en el Navegador. [Más información](create-email.md#define-email-content)

   * **Importe contenido de HTML existente** desde un archivo o una carpeta .zip. Obtenga información sobre cómo importar contenido de correo electrónico en [esta sección](existing-content.md).

   * **Convierta diseños de imagen en plantillas de HTML** con el conversor de imagen a HTML con tecnología de IA. Aprenda a transformar imágenes estáticas en plantillas de correo electrónico editables en [esta sección](../content-management/image-to-html.md).

   * **Seleccione un contenido existente** de una lista de plantillas integradas o personalizadas. Aprenda a trabajar con plantillas de correo electrónico en [esta sección](../email/use-email-templates.md).

   ![](assets/email_designer_create_options.png)

1. Una vez definido y personalizado el contenido del correo electrónico, puede verificarlo con **comprobaciones de contenido automatizadas** para detectar problemas de HTML y CSS, como etiquetas no admitidas, divs vacíos e infracciones del límite de tamaño, directamente en el panel de creación, antes de enviarlo. [Más información](content-check.md)

   >[!NOTE]
   >
   >El sistema también comprueba la configuración clave mientras diseña y muestra alertas para detectar advertencias (recomendaciones y prácticas recomendadas) y errores (problemas de bloqueo que impiden realizar pruebas o activaciones). [Más información sobre las alertas por correo electrónico](create-email.md#check-email-alerts)

   ![Panel de verificación de contenido en el Designer de correo electrónico con problemas](assets/content-check.png)

1. También puede validar la calidad del contenido para identificar posibles problemas con legibilidad, coherencia del contenido y eficacia. [Más información sobre la validación de calidad del contenido](../content-management/brands-score.md#validate-quality)

   ![](../content-management/assets/brand-score-7.png)

1. Por último, puede exportar el contenido para su validación o uso posterior. Haga clic en **[!UICONTROL HTML de exportación]** para guardar en su equipo un archivo zip que incluirá su HTML y sus recursos.

   ![](assets/email_designer_export.png)

## Prácticas recomendadas para el diseño de correo electrónico {#best-practices}

Al enviar correos electrónicos, es importante tener en cuenta que los destinatarios pueden reenviarlos, lo que a veces puede causar problemas con el procesamiento del correo electrónico. Esto es especialmente cierto cuando se utilizan clases CSS que tal vez el proveedor de correo electrónico no admita para el reenvío, por ejemplo, si utiliza la clase de CSS &quot;is-desktop-hidden&quot; para ocultar una imagen en dispositivos móviles.

Para minimizar estos problemas de renderización, se recomienda mantener la estructura de diseño del correo electrónico lo más sencilla posible. Intente utilizar un único diseño que funcione bien tanto para dispositivos de escritorio como móviles, y evite utilizar clases CSS complejas u otros elementos de diseño que puedan no ser totalmente compatibles con todos los clientes de correo electrónico.

>[!NOTE]
>
>Lo mismo se aplica cuando los correos electrónicos se abren en Gmail o Outlook a través de un explorador web móvil, donde el manejo de CSS difiere significativamente del de las aplicaciones nativas: los diseños simples basados en tablas con estilos totalmente insertados son la opción más segura. [Más información](#mobile-web-limitations)

Siguiendo estas prácticas recomendadas, puede ayudar a garantizar que los mensajes de correo electrónico se procesen correctamente, independientemente de cómo los destinatarios los vean o los reenvíen.

Consulte la tabla siguiente para conocer las prácticas recomendadas sobre el diseño de correo electrónico:

| Recomendado | Uso con cuidado | No recomendado |
|-|-|-|
| <ul><li><b>Diseños estáticos basados en tablas</b> para la estructura</li> <li><b>Tablas HTML y tablas anidadas</b> para mantener la coherencia del diseño</li> <li><b>Anchuras de plantilla</b> entre 600 y 800 píxeles </li> <li><b>CSS en línea simple</b> para diseñar </li> <li><b>Fuentes seguras para la web</b> para compatibilidad universal</li> | <ul><li>Es posible que las <b>imágenes de fondo</b> no aparezcan en ciertas plataformas de correo electrónico.</li><li><b>Las fuentes web personalizadas</b> carecen de compatibilidad universal.</li><li><b>Los diseños anchos</b> pueden visualizarse mal en las pantallas más pequeñas.</li><li><b>Los mapas de imagen</b> ofrecen una funcionalidad limitada.</li><li><b>Un CSS incrustado</b> a veces se elimina durante el envío del correo electrónico.</li> | <ul><li><b>JavaScript</b> generalmente no es compatible en los entornos de correo electrónico.</li> <li> Las etiquetas <b>`<iframe>`</b> se bloquean en la mayoría de las plataformas. </li> <li><b>Flash</b> está obsoleto y ya no es compatible.</li> <li><b>El audio incrustado</b> a menudo no se reproduce.</li> <li><b>El vídeo incrustado</b> no es compatible con muchas plataformas de correo electrónico.</li> <li> <b>Los formularios</b> no funcionan en los correos electrónicos.</li> <li> Las capas `<div>` pueden dar lugar a problemas de renderizado.</li> |

>[!NOTE]
>
>La [Ley de accesibilidad europea](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"} estipula que todas las comunicaciones digitales deben ser accesibles. Además de las prácticas recomendadas de diseño de correo electrónico incluidas en esta sección, asegúrese de seguir las directrices específicas que se indican en [esta página](accessible-content.md) para la creación de contenido accesible con el Diseñador de correo electrónico.

## Limitaciones y protecciones específicas {#email-guardrails}

Incluso los correos electrónicos bien estructurados pueden procesarse de forma diferente en función del cliente o del entorno en el que se abran. Las secciones siguientes documentan las limitaciones conocidas y los comportamientos específicos del cliente que se deben tener en cuenta al diseñar los correos electrónicos.

### Limitaciones del explorador web móvil {#mobile-web-limitations}

El procesamiento del correo electrónico puede diferir cuando los destinatarios abren Gmail o Outlook **a través de un explorador web móvil** (por ejemplo, Chrome en un teléfono), en lugar de usar una aplicación móvil nativa o un cliente de escritorio. Se trata de una limitación conocida de los entornos de correo web móviles y no es específica de Journey Optimizer.

Esta diferencia de procesamiento se debe al comportamiento de los clientes de webmail dentro de un navegador móvil. El explorador procesa primero la interfaz de usuario completa del correo web de escritorio, colocando el correo electrónico a dos capas de profundidad, fuera del alcance de cualquier CSS o consulta de medios adaptable. Gmail Web también elimina los bloques de CSS `<style>` y ajusta el contenido del correo electrónico en su propio `<div>`, lo que puede anular los estilos y crear conflictos de alineación.

Los síntomas habituales incluyen el desplazamiento de la alineación del texto (el texto alineado a la izquierda aparece centrado), líneas de separación blancas adicionales entre secciones de contenido y un diseño general que difiere del diseño de la plantilla.

Estos problemas solo se producen en Gmail Web y Outlook Web cuando se accede a ellas a través de un explorador móvil. Las aplicaciones móviles nativas de Outlook y Gmail, así como todos los clientes de escritorio, no se ven afectados.

>[!TIP]
>
>Para minimizar el impacto:
>
>* Utilice diseños sencillos basados en tablas con CSS totalmente alineado.
>
>* Evite depender de consultas de medios o bloques de `<style>` para propiedades de diseño críticas, como la alineación del texto.

### Consideraciones de procesamiento de Outlook {#outlook-tips}

Outlook tiene varias peculiaridades de procesamiento que pueden afectar al diseño del correo electrónico si no se tienen en cuenta durante el diseño. Para garantizar que los correos electrónicos se representan correctamente en Outlook, siga estas prácticas recomendadas:

* Utilice números pares para el relleno, los tamaños de fuente y los anchos. Outlook convierte los píxeles en puntos internamente, lo que puede introducir espaciado desigual y líneas blancas no deseadas cuando se utilizan números impares.
* Establezca anchos de tabla en píxeles, no porcentajes. Los anchos basados en porcentajes pueden romper el diseño en Outlook. Aplique los valores de anchura directamente en el atributo style de cada tabla.
* Establezca siempre las anchuras de la imagen con el atributo `width`. Outlook ignora las propiedades CSS `width` y `height` de las imágenes y vuelve a las dimensiones nativas del archivo si no hay ningún atributo de HTML presente.
* Incluir texto alternativo en todas las imágenes. Esto evita problemas de visualización y seguridad cuando las imágenes están bloqueadas.
* Aplique bordes a las celdas de la tabla, no al propio elemento de la tabla. Si un borde no se representa como se espera, muévalo del `<table>` al `<td>`.
* Evite las esquinas redondeadas. CSS `border-radius` no se admite de forma fiable en Outlook; las esquinas cuadradas son la opción predeterminada segura.

Para obtener información sobre el diseño en modo oscuro, incluido cómo usar consultas de medios y técnicas de intercambio de imágenes específicas de Outlook.com, consulte [esta página](dark-mode.md).

## Vídeotutoriales {#video}

Aprenda a crear contenido de correo electrónico con el editor de mensajes.

>[!VIDEO](https://video.tv.adobe.com/v/3416231?captions=spa&quality=12)

Aprenda a configurar experimentos de contenido para realizar pruebas A/B y explorar el contenido de correo electrónico que mejor impulsa sus objetivos empresariales.

>[!VIDEO](https://video.tv.adobe.com/v/3447334?captions=spa)
