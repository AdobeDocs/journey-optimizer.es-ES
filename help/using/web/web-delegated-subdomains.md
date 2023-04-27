---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de subdominios web
description: Obtenga información sobre cómo configurar subdominios web con Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
keywords: web, subdominios, configuración
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Configuración de subdominios web {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Delegación de un subdominio web"
>abstract="Se configurará el subdominio para su uso en canales web. Elija entre los subdominios que ya están delegados en Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Delegación de un subdominio web"
>abstract="Si agrega contenido procedente de Adobe Experience Manager Assets Essentials a sus experiencias web, debe configurar el subdominio que se utilizará para publicar este contenido. Seleccione entre los subdominios ya delegados en el Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Definir un subdominio predeterminado"
>abstract="Puede crear varios subdominios web, pero solo se utilizará el subdominio predeterminado. Puede cambiar el subdominio web predeterminado, pero solo se puede usar uno a la vez."

Al crear experiencias web, si agrega contenido proveniente del [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) , debe configurar el subdominio que se utilizará para publicar este contenido.

Para ello, debe elegir entre la lista de subdominios ya delegados en Adobe. Obtenga más información sobre la delegación de subdominios al Adobe en [esta sección](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>La configuración del subdominio web es común a todos los entornos. Por lo tanto:
>
>* Para acceder y editar subdominios web, debe tener la variable **[!UICONTROL Administrar subdominios web]** permiso en el simulador de pruebas de producción.
>
> * Cualquier modificación en un subdominio web también afectará a los entornos limitados de producción.


Puede crear varios subdominios web, pero solo los **default** se utilizará el subdominio . Puede cambiar el subdominio web predeterminado, pero solo se puede usar uno a la vez.

1. Acceda a la **[!UICONTROL Administración]** > **[!UICONTROL Canales]** a continuación, seleccione **[!UICONTROL Configuración web]** > **[!UICONTROL Subdominios web]**.

   ![](assets/web-access-subdomains.png)

1. Haga clic en **[!UICONTROL Configurar subdominio]**.

1. Seleccione un subdominio delegado de la lista.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >No se puede seleccionar un subdominio que ya se esté utilizando como subdominio web.

1. Para establecer este subdominio como predeterminado, seleccione la opción correspondiente.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Solo el **default** se utilizará el subdominio . Puede cambiar el subdominio web predeterminado, pero solo se puede usar uno a la vez.

1. Haga clic en **[!UICONTROL Enviar]**. El subdominio obtiene la variable **[!UICONTROL Correcto]** estado. Está listo para utilizarse para sus experiencias web.

1. La variable **[!UICONTROL Predeterminado]** aparece un distintivo junto al subdominio que se utiliza actualmente como predeterminado. Para cambiar el subdominio predeterminado, seleccione **[!UICONTROL Establecer como predeterminado]** de la variable **[!UICONTROL Más acciones]** situado junto al subdominio deseado.

   ![](assets/web-subdomain-default.png)

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.-->

1. Solo puede eliminar un **[!UICONTROL Error]** subdominio para limpiar la lista. Para ello, seleccione **[!UICONTROL Eliminar]** de la variable **[!UICONTROL Más acciones]** situado junto al subdominio deseado.

<!--You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->

