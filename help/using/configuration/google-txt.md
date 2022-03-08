---
title: Añadir un registro TXT de Google a un subdominio
description: Aprenda a añadir un registro TXT de Google a un subdominio
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 26%

---

# Añadir un registro TXT de Google a un subdominio {#google-txt-record}

Los registros TXT son un tipo de registros DNS que se utilizan para proporcionar información de texto sobre un dominio y que pueden leer fuentes externas.

Para garantizar una buena entrega y un envío correcto de correos electrónicos a las direcciones de Gmail, [!DNL Journey Optimizer] le permite agregar registros TXT especiales de verificación del sitio de Google a sus subdominios para asegurarse de que estén verificados.

>[!CAUTION]
>
> Esta operación solo se puede realizar una vez que un subdominio tiene la variable **[!UICONTROL Success]** estado. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](access-subdomains.md).

Para agregar un registro TXT de Google al subdominio, siga estos pasos:

1. Abra el subdominio desde el **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** para abrir el Navegador.

1. En el **[!UICONTROL Google txt record]** , introduzca el código de verificación generado a partir de [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->y haga clic en **[!UICONTROL Save]**.

   ![](assets/subdomain-google-txt.png)

1. Una vez agregado el registro TXT, Google debe verificarlo. Para ello, vaya a [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, luego inicie el paso de verificación.
