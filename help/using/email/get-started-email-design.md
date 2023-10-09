---
solution: Journey Optimizer
product: journey optimizer
title: Diseño de correos electrónicos
description: Obtenga información sobre cómo diseñar sus correos electrónicos
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: correo electrónico, diseño, stock, activos
exl-id: e4f91870-f06a-4cd3-98b7-4c413233e310
source-git-commit: dd463d36550b53faaffca90691550278498c862a
workflow-type: ht
source-wordcount: '480'
ht-degree: 100%

---

# Introducción al diseño de correo electrónico {#get-started-content-design}

Puede importar un contenido existente en [!DNL Journey Optimizer] o aprovechar las funcionalidades de diseño de contenido:

* Utilice las [!DNL Journey Optimizer]**funcionalidades de diseño de correo electrónico de** para diseñar o importar correos electrónicos adaptables. [Más información](content-from-scratch.md)

* Aproveche **Adobe Experience Manager Assets Essentials** para enriquecer los correos electrónicos, crear y administrar su propia base de datos de activos. [Más información](../content-management/assets-essentials.md)

* Encuentre **fotos de Adobe Stock** para crear su contenido y mejorar su diseño de correo electrónico. [Más información](../content-management/stock.md)

* Mejore la experiencia de los clientes creando mensajes y de correo electrónico personalizados en función de sus atributos de perfil. Más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md).

➡️ [Descubra esta función en vídeo](#video)

## Prácticas recomendadas para el diseño de correo electrónico {#best-practices}

Al enviar correos electrónicos, es importante tener en cuenta que los destinatarios pueden reenviarlos, lo que a veces puede causar problemas con el procesamiento del correo electrónico. Esto es especialmente cierto cuando se utilizan clases CSS que es posible que el proveedor de correo electrónico no admita para el reenvío, por ejemplo, si utiliza la clase CSS &quot;is-desktop-hidden&quot; para ocultar una imagen en dispositivos móviles.

Para minimizar estos problemas de renderización, se recomienda mantener la estructura de diseño del correo electrónico lo más sencilla posible. Intente utilizar un único diseño que funcione bien tanto para dispositivos de escritorio como móviles, y evite utilizar clases CSS complejas u otros elementos de diseño que puedan no ser totalmente compatibles con todos los clientes de correo electrónico. Siguiendo estas prácticas recomendadas, puede ayudar a garantizar que los mensajes de correo electrónico se procesen correctamente, independientemente de cómo los destinatarios los vean o los reenvíen.

## Pasos clave para crear contenido de correo electrónico {#key-steps}

Una vez que haya [añadido un correo electrónico](create-email.md) a un recorrido o a una campaña, podrá empezar a crear su contenido de correo electrónico.

1. Desde la pantalla de configuración de recorrido o de campaña, pase por la pantalla **[!UICONTROL Editar contenido]** para acceder al Diseñador de correo electrónico. [Más información](create-email.md#define-email-content)

   ![](assets/email_designer_edit_email_body.png)

1. En la página de inicio del Diseñador de correo electrónico, elija cómo desea diseñar el correo electrónico desde las opciones siguientes:

   * **Diseñe su correo electrónico desde cero** a través de la interfaz del diseñador de correo electrónico y aproveche las imágenes de [Adobe Experience Manager Assets Essentials](../content-management/assets-essentials.md). Información sobre cómo diseñar el contenido de su correo electrónico en [esta sección](content-from-scratch.md).

   * **Codifique o pegue HTML sin procesar** directamente en el diseñador de correo electrónico. Información sobre cómo codificar su propio contenido en [esta sección](code-content.md).

     >[!NOTE]
     >
     >En una campaña, también puede seleccionar el botón **[!UICONTROL Editor de código]** del **[!UICONTROL Editar contenido]** en el Navegador. [Más información](create-email.md#define-email-content)

   * **Importe contenido de HTML existente** desde un archivo o una carpeta .zip. Obtenga información sobre cómo importar contenido de correo electrónico en [esta sección](existing-content.md).

   * **Seleccione un contenido existente** de una lista de plantillas integradas o personalizadas. Aprenda a trabajar con plantillas de correo electrónico [esta sección](../email/use-email-templates.md).

   ![](assets/email_designer_create_options.png)

1. Una vez definido y personalizado el contenido del correo electrónico, puede exportar el contenido para su validación o para utilizarlo posteriormente. Haga clic en **[!UICONTROL HTML de exportación]** para guardar en su equipo un archivo zip que incluirá su HTML y sus recursos.

   ![](assets/email_designer_export.png)

## Vídeotutoriales {#video}

Aprenda a crear contenido de correo electrónico con el editor de mensajes.

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)

Aprenda a configurar experimentos de contenido para realizar pruebas A/B y explorar el contenido de correo electrónico que mejor impulsa sus objetivos empresariales.

>[!VIDEO](https://video.tv.adobe.com/v/3419893)
