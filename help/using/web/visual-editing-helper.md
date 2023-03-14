---
title: Extensión Ayuda de edición visual
description: Descubra la extensión de Chrome Ayuda de edición visual que le permite crear y previsualizar páginas web en Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 18%

---

# Extensión Ayuda de edición visual {#visual-editing-helper}

>[!BEGINSHADEBOX]

Lo que encontrará en esta documentación:

* [Introducción al canal web](get-started-web.md)
* [Creación de experiencias web](create-web.md)
* [Creación de páginas web](author-web.md)
* **[Extensión Ayuda de edición visual](visual-editing-helper.md)**
* [Creación de informes web](web-report.md)

>[!ENDSHADEBOX]

Para crear y previsualizar rápidamente sus experiencias web, la extensión del explorador Adobe Experience Cloud Visual Editing Helper para Google Chrome permite cargar sitios web de forma fiable dentro del Adobe [!DNL Journey Optimizer] diseñador web.

## Instale la extensión Ayuda de edición visual {#install-visual-editing-helper}

Para obtener e instalar la extensión de explorador Ayuda de edición visual, siga los pasos a continuación.

1. En Google Chrome Web Store, vaya a [Ayuda de edición visual de Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensión del explorador.

1. Haga clic en **[!UICONTROL Añadir a Chrome]** > **[!UICONTROL Añadir extensión]**.

1. Creación de una campaña de canal web en [!DNL Journey Optimizer]. [Descubra cómo](author-web.md#create-web-campaign)

1. Abra el [!DNL Journey Optimizer] diseñador web para empezar a crear la experiencia web. [Más información](author-web.md)

1. Asegúrese de que la extensión del explorador Ayuda de edición visual esté habilitada en la barra de herramientas del explorador Chrome haciendo clic en el icono correspondiente.

   ![](assets/web-visual-editing-extension.png)

El Asistente de edición visual de Adobe Experience Cloud ahora se habilita automáticamente cuando se abre un sitio web en [!DNL Journey Optimizer] diseñador web para la creación de contenido.

La extensión no tiene ninguna configuración condicional y administra todas las configuraciones automáticamente, incluida la configuración de cookies de SameSite.

>[!NOTE]
>
>Es posible que algunos sitios web no se abran de forma fiable en [!DNL Journey Optimizer] diseñador web debido a una de las siguientes razones:
>
> * El sitio web tiene normas estrictas de seguridad.
> * El sitio web se encuentra en un iframe.
> * El control de calidad o la fase del cliente no están disponibles para el mundo exterior (el sitio es interno).


## Resolución de problemas

Al utilizar el Adobe [!DNL Journey Optimizer] diseñador web, si intenta cargar un sitio web que no se puede cargar, aparece un mensaje sugiriendo que instale el [Extensión de explorador Ayuda de edición visual](#install-visual-editing-helper).

Si el SDK web de Adobe Experience Platform aún no está implementado en el sitio web, aparece un mensaje en el diseñador web sugiriendo que instale la extensión de explorador Ayuda de edición visual e implemente la extensión de [SDK web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"}.

Si el sitio no se carga o se comporta de forma inesperada, una posible solución es aceptar cookies en el sitio web en el explorador antes de intentar cargarlo en un Adobe [!DNL Journey Optimizer].

En el caso de las páginas que se están autenticando, si la página de inicio de sesión no se puede cargar o si, después de intentar iniciar sesión, aún no ha iniciado sesión, intente iniciar sesión primero en una pestaña diferente del explorador y, a continuación, cargue el sitio web en la Adobe [!DNL Journey Optimizer] diseñador web.
