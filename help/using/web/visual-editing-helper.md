---
title: Extensión Ayuda de edición visual
description: Descubra la extensión de Chrome de Visual Editing Helper que le permite crear y previsualizar páginas web en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 14%

---

# Extensión Ayuda de edición visual {#visual-editing-helper}

Para crear y previsualizar rápidamente sus experiencias web, la extensión del explorador Adobe Experience Cloud Visual Editing Helper para Google Chrome permite cargar sitios web de forma fiable dentro del Adobe [!DNL Journey Optimizer] diseñador web.

>[!NOTE]
>
>Actualmente, la función de canal web está disponible en versión beta solo para usuarios seleccionados.

## Instalación de la extensión de Visual Editing Helper {#install-visual-editing-helper}

Para obtener e instalar la extensión del explorador de Visual Editing Helper, siga los pasos a continuación.

1. En la tienda web de Google Chrome, vaya a la [Ayuda de edición visual de Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensión del explorador.

1. Haga clic en **[!UICONTROL Añadir a Chrome]** > **[!UICONTROL Añadir extensión]**.

1. Cree una campaña de canales web en [!DNL Journey Optimizer]. [Descubra cómo](author-web.md#create-web-campaign)

1. Abra el [!DNL Journey Optimizer] diseñador web para comenzar a crear su experiencia web. [Más información](author-web.md)

1. Asegúrese de que la extensión del explorador de Visual Editing Helper esté habilitada en la barra de herramientas del explorador Chrome haciendo clic en el icono correspondiente.

   ![](assets/web-visual-editing-extension.png)

El Asistente de edición visual de Adobe Experience Cloud ahora está habilitado automáticamente cuando se abre un sitio web en la [!DNL Journey Optimizer] diseñador web para potenciar la creación de contenido.

La extensión no tiene ninguna configuración condicional y gestiona todos los ajustes automáticamente, incluida la configuración de cookies de SameSite.

>[!NOTE]
>
>Es posible que algunos sitios web no se abran de forma fiable en la variable [!DNL Journey Optimizer] diseñador web por uno de los siguientes motivos:
>
> * El sitio web tiene normas estrictas de seguridad.
> * El sitio web se encuentra en un iframe.
> * El control de calidad o la fase del cliente no están disponibles para el mundo exterior (el sitio es interno).


## Resolución de problemas

Al utilizar el Adobe [!DNL Journey Optimizer] diseñador web, si intenta cargar un sitio web que no se puede cargar, aparece un mensaje sugiriendo que instale el [Extensión del explorador de Visual Editing Helper](#install-visual-editing-helper).

Si el SDK web de Adobe Experience Platform aún no está implementado en el sitio web, se muestra un mensaje en el diseñador web sugiriendo que instale la extensión del explorador Visual Editing Helper e implemente la variable [SDK web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"}.

Si el sitio no se carga o se comporta de forma inesperada, una posible corrección es aceptar cookies en el sitio web del explorador antes de intentar cargarlas en el Adobe [!DNL Journey Optimizer].

En el caso de las páginas bajo autenticación, si la página de inicio de sesión no se carga o si después de intentar iniciar sesión aún no ha iniciado sesión, intente iniciar sesión primero en una pestaña diferente del explorador y luego cargue el sitio web en el Adobe [!DNL Journey Optimizer] diseñador web.
