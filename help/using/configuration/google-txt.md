---
title: Delegar subdominios
description: Obtenga información sobre cómo delegar subdominios
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Configuración de la aplicación
topic: Administración
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 27%

---


# Añadir un registro TXT de Google a un subdominio

Los registros TXT son un tipo de registros DNS que se utilizan para proporcionar información de texto sobre un dominio y que pueden leer fuentes externas.

Para garantizar una buena entrega y un envío correcto de correos electrónicos a las direcciones de Gmail, la administración de Recorridos de cliente le permite añadir registros TXT de verificación de sitios de Google especiales a sus subdominios para garantizar que se verifiquen.

>[!NOTE]
>
> Esta operación solo se puede realizar una vez que un subdominio tiene el estado **[!UICONTROL Success]**. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](access-subdomains.md).

Para agregar un registro TXT de Google al subdominio, siga estos pasos:

1. Abra el subdominio en el menú **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**.

1. En la sección del registro txt de Google, introduzca el código de verificación generado en [G Suite Admin tools](https://support.google.com/a/answer/183895) y haga clic en **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Una vez agregado el registro TXT, Google debe verificarlo. Para ello, vaya a las herramientas de administración de G Suite y, a continuación, inicie el paso de verificación.
