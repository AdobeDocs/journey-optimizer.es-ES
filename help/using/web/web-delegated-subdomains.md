---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de subdominios web
description: Obtenga información sobre cómo configurar subdominios web con Journey Optimizer
role: Admin
level: Intermediate
keywords: web, subdominios, configuración
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: 39953bb09a699ed4fd07db26a3f2e54f4e2cacd7
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 27%

---

# Configuración de subdominios web {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Delegación de un subdominio web"
>abstract="Se configurará el subdominio para el uso del canal web. Elija entre los subdominios que ya están delegados en Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Delegación de un subdominio web"
>abstract="Si agrega contenido procedente de Adobe Experience Manager Assets Essentials a sus experiencias web, debe configurar el subdominio que se utilizará para publicar este contenido. Seleccione entre los subdominios ya delegados en Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Definición de un subdominio web"
>abstract="Seleccione un subdominio de la lista de subdominios delegados en Adobe. Puede establecer este subdominio web como el predeterminado, pero solo se puede utilizar un subdominio predeterminado a la vez."

Al crear experiencias web, si añade contenido procedente de [Adobe Experience Manager Assets Essentials](../content-management/assets-essentials.md) , debe configurar el subdominio que se utilizará para publicar este contenido.

Para ello, debe elegir de la lista de subdominios ya delegados al Adobe. Obtenga más información sobre la delegación de subdominios al Adobe en [esta sección](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>La configuración del subdominio web es común a todos los entornos. Por lo tanto:
>
>* Para acceder y editar subdominios web, debe tener el **[!UICONTROL Administrar subdominios web]** en la zona protegida de producción.
>
> * Cualquier modificación en un subdominio web también afectará a los entornos limitados de producción.

Puede crear varios subdominios web, pero solo los siguientes **predeterminado** se utilizará el subdominio. Puede cambiar el subdominio web predeterminado, pero solo se puede utilizar uno a la vez.

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** menú, luego seleccione **[!UICONTROL Configuración web]** > **[!UICONTROL Subdominios web]**.

   ![](assets/web-access-subdomains.png)

1. Clic **[!UICONTROL Configuración del subdominio]**.

1. Seleccione un subdominio delegado de la lista.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >No puede seleccionar un subdominio que ya se esté utilizando como subdominio web.

1. El prefijo que se mostrará en la URL web se añade automáticamente. No puede cambiarlo.

1. Para establecer este subdominio como predeterminado, seleccione la opción correspondiente.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Solo el **predeterminado** se utilizará el subdominio.

1. Haga clic en **[!UICONTROL Enviar]**. El subdominio obtiene el **[!UICONTROL Correcto]** estado. Está listo para utilizarse para las experiencias web.

   >[!NOTE]
   >
   >En muy raras ocasiones, la configuración de un subdominio podría fallar. En este caso, puede eliminar la variable **[!UICONTROL Error]** subdominio para limpiar la lista utilizando **[!UICONTROL Eliminar]** del menú contextual **[!UICONTROL Más acciones]** icono.

1. El **[!UICONTROL Predeterminado]** el distintivo se muestra junto al subdominio que se utiliza actualmente como predeterminado. Para cambiar el subdominio predeterminado, seleccione **[!UICONTROL Establecer como predeterminado]** desde el **[!UICONTROL Más acciones]** junto al subdominio deseado.

   ![](assets/web-subdomain-default.png)

   >[!NOTE]
   >
   >Puede cambiar el subdominio web predeterminado, pero solo se puede utilizar uno a la vez.

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.

    You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->
