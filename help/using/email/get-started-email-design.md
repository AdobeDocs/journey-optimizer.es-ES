---
solution: Journey Optimizer
product: journey optimizer
title: Diseño de correos electrónicos
description: Aprenda a diseñar sus correos electrónicos
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: correo electrónico, diseño, stock, activos
exl-id: e4f91870-f06a-4cd3-98b7-4c413233e310
source-git-commit: 3a9b11b1a4d2159261586394f1595e52c8b749e7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 12%

---

# Introducción al diseño de correo electrónico {#get-started-content-design}

Puede importar un contenido existente en [!DNL Journey Optimizer] o aproveche las capacidades de diseño de contenido:

* Uso [!DNL Journey Optimizer] **capacidades de diseño de correo electrónico** para diseñar o importar correos electrónicos interactivos. [Más información](content-from-scratch.md)

* Aproveche **Adobe Experience Manager Assets Essentials** para enriquecer los correos electrónicos, crear y administrar su propia base de datos de activos. [Más información](assets-essentials.md)

* Encuentre **fotos de Adobe Stock** para crear su contenido y mejorar su diseño de correo electrónico. [Más información](stock.md)

* Mejore la experiencia de los clientes creando mensajes personalizados y dinámicos en función de sus atributos de perfil. Más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md).

➡️ [Descubra esta función en vídeo](#video)

## Prácticas recomendadas para el diseño de correo electrónico {#best-practices}

Al enviar correos electrónicos, es importante tener en cuenta que los destinatarios pueden reenviarlos, lo que a veces puede causar problemas con la renderización del correo electrónico. Esto es especialmente cierto cuando se utilizan clases CSS que puede que no sea compatible con el proveedor de correo electrónico utilizado para el reenvío, por ejemplo, si utiliza la clase CSS &quot;is-desktop-hidden&quot; (está oculta en el escritorio) para ocultar una imagen en dispositivos móviles.

Para minimizar estos problemas de renderización, se recomienda mantener la estructura de diseño del correo electrónico lo más sencilla posible. Intente utilizar un único diseño que funcione bien tanto para dispositivos de escritorio como móviles, y evite utilizar clases CSS complejas u otros elementos de diseño que puedan no ser totalmente compatibles con todos los clientes de correo electrónico. Siguiendo estas prácticas recomendadas, puede ayudar a garantizar que los mensajes de correo electrónico se procesen correctamente, independientemente de cómo los destinatarios los vean o los reenvíen.

## Pasos clave para crear contenido de correo electrónico {#key-steps}

Una vez que haya [se ha añadido un correo electrónico](create-email.md) a un recorrido o a una campaña, puede empezar a crear su contenido de correo electrónico.

1. Desde la pantalla de configuración de recorrido o de campaña, vaya a través de la **[!UICONTROL Editar contenido]** para acceder al Diseñador de correo electrónico. [Más información](create-email.md#define-email-content)

   ![](assets/email_designer_edit_email_body.png)

1. En la página de inicio del Diseñador de correo electrónico, elija cómo desea diseñar el correo electrónico desde las siguientes opciones:

   * **Diseñe su correo electrónico desde cero** a través de la interfaz del diseñador de correo electrónico y aproveche las imágenes de [Adobe Experience Manager Assets Essentials](assets-essentials.md). Aprenda a diseñar el contenido de su correo electrónico en [esta sección](content-from-scratch.md).

   * **HTML sin procesar de código o pegado** directamente en el diseñador de correo electrónico. Aprenda a codificar su propio contenido en [esta sección](code-content.md).

      >[!NOTE]
      >
      >En una campaña, también puede seleccionar la **[!UICONTROL Editor de código]** del **[!UICONTROL Editar contenido]** en el Navegador. [Más información](create-email.md#define-email-content)

   * **Importar contenido de HTML existente** desde un archivo o una carpeta .zip. Obtenga información sobre cómo importar contenido de correo electrónico en [esta sección](existing-content.md).

   * **Seleccionar un contenido existente** de una lista de plantillas integradas o personalizadas. Aprenda a trabajar con plantillas de correo electrónico [esta sección](email-templates.md).

   ![](assets/email_designer_create_options.png)

1. Una vez definido y personalizado el contenido del correo electrónico, puede exportar el contenido para su validación o para utilizarlo posteriormente. Haga clic en **[!UICONTROL HTML de exportación]** para guardar en su equipo un archivo zip que incluirá su HTML y sus recursos.

   ![](assets/email_designer_export.png)

## Vídeo explicativo {#video}

Aprenda a crear contenido de correo electrónico con el editor de mensajes.

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)