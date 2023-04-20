---
solution: Journey Optimizer
product: journey optimizer
title: Añadir un registro TXT de Google a un subdominio
description: Aprenda a añadir un registro TXT de Google a un subdominio
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: subdominio, google, txt, record, gmail, deliverability
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 24%

---

# Añadir un registro TXT de Google a un subdominio {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Registros TXT de Google"
>abstract="Para garantizar un envío correcto de correos electrónicos a las direcciones de Gmail, puede añadir registros TXT de verificación de sitios de Google especiales a su subdominio para asegurarse de que estén verificados."

Los registros TXT son un tipo de registro DNS utilizado para proporcionar información de texto sobre un dominio que pueden leer fuentes externas.

Para garantizar una entrega óptima y un envío correcto de correos electrónicos a las direcciones de Gmail, [!DNL Journey Optimizer] le permite agregar registros TXT especiales de verificación del sitio de Google al subdominio para asegurarse de que estén verificados.

>[!CAUTION]
>
> Esta operación solo se puede realizar una vez que un subdominio tiene la variable **[!UICONTROL Correcto]** estado. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](about-subdomain-delegation.md#access-delegated-subdomains).

Para agregar un registro TXT de Google al subdominio, siga estos pasos:

1. Abra el subdominio desde el **[!UICONTROL Canales]** / **[!UICONTROL Subdominios]** para abrir el Navegador.

1. En el **[!UICONTROL Registro txt de Google]** , introduzca el código de verificación generado a partir de [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->y haga clic en **[!UICONTROL Guardar]**.

   ![](assets/subdomain-google-txt.png)

1. Una vez agregado el registro TXT, Google debe verificarlo. Para ello, vaya a [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->, luego inicie el paso de verificación.
