---
solution: Journey Optimizer
product: journey optimizer
title: Configurar subdominios de página de aterrizaje
description: Obtenga información sobre cómo configurar subdominios de páginas de aterrizaje con Journey Optimizer
role: Admin
level: Intermediate
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 1%

---

# Configurar subdominios de página de aterrizaje {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp_header"
>title="Delegación de un subdominio de página de aterrizaje"
>abstract="Se configurará el subdominio para su uso en una página de aterrizaje. Puede utilizar un subdominio que ya esté delegado en el Adobe o configurar otro subdominio."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="Delegación de un subdominio de página de aterrizaje"
>abstract="Debe configurar un subdominio para utilizarlo en las páginas de aterrizaje, ya que necesitará este subdominio para crear un ajuste preestablecido de página de aterrizaje. Puede utilizar un subdominio ya delegado en el Adobe o configurar un nuevo subdominio."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="Crear ajustes preestablecidos de página de aterrizaje"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Crear un ajuste preestablecido de página de aterrizaje"
>abstract="Para poder crear un ajuste preestablecido de página de aterrizaje, asegúrese de haber configurado previamente al menos un subdominio de página de aterrizaje para seleccionarlo en la lista de nombres de subdominio."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="Crear ajustes preestablecidos de página de aterrizaje"

Para poder [crear ajustes preestablecidos de página de aterrizaje](lp-presets.md), debe configurar los subdominios que desea utilizar para las páginas de aterrizaje.

Puede utilizar un subdominio que ya esté delegado en Adobe o configurar otro subdominio. Obtenga más información sobre la delegación de subdominios al Adobe en [esta sección](delegate-subdomain.md).

>[!CAUTION]
>
>La configuración del subdominio de la página de aterrizaje es común a todos los entornos. Por lo tanto, cualquier modificación en un subdominio de página de aterrizaje también afectará a los entornos limitados de producción.

Tenga en cuenta que las mayúsculas no deben estar permitidas en un subdominio

## Usar un subdominio existente {#lp-use-existing-subdomain}

Para utilizar un subdominio que ya está delegado en Adobe, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Administración]** > **[!UICONTROL Canales]** a continuación, seleccione **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Subdominios de la página de aterrizaje]**.

   ![](assets/lp_access-subdomains.png)

1. Haga clic en **[!UICONTROL Configurar subdominio]**.

   ![](assets/lp_set-up-subdomain.png)

1. Select **[!UICONTROL Usar dominio delegado]** de la variable **[!UICONTROL Tipo de configuración]** para obtener más información.

   ![](assets/lp_use-delegated-subdomain.png)

1. Introduzca el prefijo que se mostrará en la dirección URL de la página de aterrizaje.

   >[!NOTE]
   >
   >Solo se permiten caracteres alfanuméricos y guiones.

1. Seleccione un subdominio delegado de la lista.

   >[!NOTE]
   >
   >No puede seleccionar un subdominio que ya se esté utilizando como subdominio de página de aterrizaje.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/lp_prefix-and-subdomain.png)

   Tenga en cuenta que no se pueden usar varios subdominios delegados del mismo dominio principal. Por ejemplo: si &quot;marketing1.yourcompany.com&quot; ya está delegado a Adobe para sus páginas de aterrizaje, no podrá utilizar &quot;marketing2.yourcompany.com&quot;. Sin embargo, si se admiten subdominios de varios niveles para páginas de aterrizaje, puede continuar usando un subdominio de &quot;marketing1.yourcompany.com&quot; (como &quot;email.marketing1.yourcompany.com&quot;) o un dominio principal diferente.

   >[!CAUTION]
   >
   >Si selecciona un dominio delegado a Adobe mediante la variable [método CNAME](delegate-subdomain.md#cname-subdomain-delegation), debe crear el registro DNS en la plataforma de alojamiento. Para generar el registro DNS, el proceso es el mismo que al configurar un nuevo subdominio de página de aterrizaje. Obtenga información sobre cómo [esta sección](#lp-configure-new-subdomain).

1. Haga clic en **[!UICONTROL Enviar]**.

1. Una vez enviado, el subdominio se muestra en la lista con la variable **[!UICONTROL Procesamiento]** estado. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](access-subdomains.md).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >Antes de poder usar ese subdominio para enviar mensajes, debe esperar hasta que el Adobe realice las comprobaciones necesarias, que pueden tardar hasta 4 horas.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Una vez realizadas las comprobaciones correctamente, el subdominio recibe la variable **[!UICONTROL Correcto]** estado. Está listo para utilizarse para crear ajustes preestablecidos de página de aterrizaje.

## Configuración de un nuevo subdominio {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="Generar el registro DNS correspondiente"
>abstract="Para configurar un nuevo subdominio de página de aterrizaje, debe copiar la información del servidor de nombres de Adobe que se muestra en la interfaz de Journey Optimizer y pegarla en la solución de alojamiento de dominios para generar el registro DNS correspondiente. Una vez realizadas las comprobaciones correctamente, el subdominio está listo para utilizarse para crear ajustes preestablecidos de página de aterrizaje."

Para configurar un nuevo subdominio, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Administración]** > **[!UICONTROL Canales]** a continuación, seleccione **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Subdominios de la página de aterrizaje]**.

1. Haga clic en **[!UICONTROL Configurar subdominio]**.

1. Select **[!UICONTROL Añadir su propio dominio]** de la variable **[!UICONTROL Tipo de configuración]** para obtener más información.

   ![](assets/lp_add-your-own-subdomain.png)

1. Especifique el subdominio que desea delegar.

   >[!CAUTION]
   >
   >No puede utilizar un subdominio de página de aterrizaje existente.
   >
   >Las mayúsculas no están permitidas en los subdominios.

   No se permite delegar un subdominio no válido al Adobe. Asegúrese de introducir un subdominio válido que sea propiedad de su organización, como marketing.yourcompany.com.

   >[!NOTE]
   >
   >En el caso de las páginas de aterrizaje, se admiten subdominios de varios niveles. Por ejemplo, puede utilizar &quot;email.marketing.yourcompany.com&quot;.

1. Se muestra el registro que se va a colocar en los servidores DNS. Copie este registro o descargue un archivo CSV y, a continuación, vaya a la solución de alojamiento de dominios para generar el registro DNS correspondiente.

1. Asegúrese de que el registro DNS se haya generado en la solución de alojamiento de dominios. Si todo está configurado correctamente, marque la casilla &quot;Confirmo...&quot; y luego haga clic en **[!UICONTROL Submit]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Al configurar un nuevo subdominio de página de aterrizaje, siempre señalará a un registro CNAME.

1. Una vez enviada la delegación de subdominios, el subdominio se muestra en la lista con la variable **[!UICONTROL Procesamiento]** estado. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](access-subdomains.md).<!--Same statuses?-->

   >[!NOTE]
   >
   >Antes de poder usar ese subdominio para enviar mensajes, debe esperar hasta que el Adobe realice las comprobaciones necesarias, que pueden tardar hasta 4 horas.<!--Learn more in [this section](#subdomain-validation).-->

1. Una vez realizadas las comprobaciones correctamente, el subdominio recibe la variable **[!UICONTROL Correcto]** estado. Está listo para utilizarse para crear ajustes preestablecidos de página de aterrizaje.

   Tenga en cuenta que el subdominio se marcará como **[!UICONTROL Error]** si no puede crear el registro de validación en la solución de alojamiento.
