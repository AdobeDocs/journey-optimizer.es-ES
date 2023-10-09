---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de subdominios web
description: Obtenga información sobre cómo configurar subdominios web con Journey Optimizer
role: Admin
level: Intermediate
keywords: web, subdominios, configuración
exl-id: 6e00466d-4ce5-4d80-89ff-c7331a5ab158
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 21%

---

# Configuración de subdominios web {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Delegación de un subdominio web"
>abstract="Se configurará el subdominio para el uso del canal web. Puede utilizar un subdominio que ya esté delegado en Adobe o configurar otro subdominio."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Delegación de un subdominio web"
>abstract="Si agrega contenido procedente de Adobe Experience Manager Assets Essentials a sus experiencias web, debe configurar el subdominio que se utilizará para publicar este contenido. Seleccione entre los subdominios ya delegados a Adobe o configure un nuevo subdominio."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Definición de un subdominio web"
>abstract="Seleccione un subdominio de la lista de subdominios delegados en Adobe. Puede establecer este subdominio web como el predeterminado, pero solo se puede utilizar un subdominio predeterminado a la vez."

Al crear experiencias web, si añade contenido procedente de [Adobe Experience Manager Assets Essentials](../content-management/assets-essentials.md) , debe configurar el subdominio que se utilizará para publicar este contenido.

Puede utilizar un subdominio que ya esté delegado al Adobe o puede configurar otro subdominio. Obtenga más información sobre la delegación de subdominios al Adobe en [esta sección](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>La configuración del subdominio web es común a todos los entornos. Por lo tanto:
>
>* Para acceder y editar subdominios web, debe tener el **[!UICONTROL Administrar subdominios web]** en la zona protegida de producción.
>
> * Cualquier modificación en un subdominio web también afectará a los entornos limitados de producción.

Puede crear varios subdominios web, pero solo los siguientes **predeterminado** se utilizará el subdominio. Puede cambiar el subdominio web predeterminado, pero solo se puede utilizar uno a la vez.

## Acceso y administración de subdominios web {#access-web-subdomains}

1. Vaya a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** menú, luego seleccione **[!UICONTROL Configuración web]** > **[!UICONTROL Subdominios web]**. Se muestran todos los subdominios configurados con la zona protegida actual.

   ![](assets/web-access-subdomains.png)

1. Puede filtrar por el usuario que delegó cada subdominio o por uno el estado de delegación (**[!UICONTROL Borrador]**, **[!UICONTROL Procesando]**, **[!UICONTROL Correcto]** o **[!UICONTROL Error]**).

   ![](assets/web-filter-subdomains.png)

1. El **[!UICONTROL Predeterminado]** el distintivo se muestra junto al subdominio que se utiliza actualmente como predeterminado. Para cambiar el subdominio predeterminado, seleccione **[!UICONTROL Establecer como predeterminado]** desde el **[!UICONTROL Más acciones]** junto al subdominio deseado.

   ![](assets/web-subdomain-default.png)

   >[!NOTE]
   >
   >Puede cambiar el subdominio web predeterminado, pero solo se puede utilizar uno a la vez.

## Usar un subdominio existente {#web-use-existing-subdomain}

Para utilizar un subdominio que ya se haya delegado al Adobe, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** menú, luego seleccione **[!UICONTROL Configuración web]** > **[!UICONTROL Subdominios web]**.

1. Clic **[!UICONTROL Configuración del subdominio]**.

1. Seleccione el **[!UICONTROL Usar subdominio delegado]** de la opción **[!UICONTROL Tipo de configuración]** y elija un subdominio delegado de la lista.

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

## Configuración de un nuevo subdominio {#web-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_web_subdomain_dns"
>title="Generar el registro DNS coincidente"
>abstract="Para configurar un nuevo subdominio web, debe copiar la información del servidor de nombres de Adobe que se muestra en la interfaz de Journey Optimizer y pegarla en la solución de alojamiento de dominios para generar el registro DNS coincidente. Una vez realizadas las comprobaciones correctamente, el subdominio está listo para utilizarse para publicar contenido procedente de la biblioteca de Experience Manager Assets Essentials."

Para configurar un nuevo subdominio, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** menú, luego seleccione **[!UICONTROL configuración web]** > **[!UICONTROL subdominios web]**.

1. Clic **[!UICONTROL Configuración del subdominio]**.

1. Seleccionar **[!UICONTROL Añadir su propio dominio]** desde el **[!UICONTROL Tipo de configuración]** sección.

1. Especifique el subdominio que desea delegar.

   >[!CAUTION]
   >
   >No se puede utilizar un subdominio web existente.
   >
   >No se permiten mayúsculas en los subdominios.

   ![](assets/web-add-your-own-domain.png)

   No se permite delegar un subdominio no válido al Adobe. Asegúrese de introducir un subdominio válido que sea propiedad de su organización, como marketing.yourcompany.com.

   >[!NOTE]
   >
   >Se admiten subdominios de varios niveles (del mismo dominio principal). Por ejemplo, puede utilizar &quot;web.marketing.yourcompany.com&quot;.

1. Para establecer este subdominio como predeterminado, seleccione la opción correspondiente.

   >[!NOTE]
   >
   >Solo el **predeterminado** se utilizará el subdominio.

1. Se muestra el registro que se va a colocar en los servidores DNS. Copie este registro o descargue un archivo CSV y, a continuación, vaya a la solución de alojamiento de dominios para generar el registro DNS correspondiente.

1. Asegúrese de que se ha generado un registro DNS en la solución de alojamiento de dominios. Si todo está configurado correctamente, marque la casilla &quot;Confirmo...&quot; y luego haga clic en **[!UICONTROL Enviar]**.

   ![](assets/web-add-your-own-domain-confirm.png)

   >[!NOTE]
   >
   >Al configurar un nuevo subdominio web, siempre señalará a un registro CNAME.

1. Una vez enviada la delegación del subdominio, este se muestra en la lista con el **[!UICONTROL Procesando]** estado. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Antes de poder utilizar ese subdominio para enviar mensajes web, debe esperar hasta que el Adobe realice las comprobaciones necesarias, que pueden tardar hasta cuatro horas.

1. Una vez realizadas las comprobaciones correctamente, el subdominio obtiene el **[!UICONTROL Correcto]** estado. Está listo para utilizarse para crear superficies de canal web.

   Observe que el subdominio se marcará como **[!UICONTROL Error]** si no puede crear el registro de validación en la solución de alojamiento.


<!--
Only a subdomain with the **[!UICONTROL Success]** status can be set as default.
You cannot delete a subdomain with the **[!UICONTROL Processing]** status.
-->
