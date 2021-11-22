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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 26%

---

# Añadir un registro TXT de Google a un subdominio

Los registros TXT son un tipo de registros DNS que se utilizan para proporcionar información de texto sobre un dominio y que pueden leer fuentes externas.

Para garantizar una buena entrega y un envío correcto de correos electrónicos a las direcciones de Gmail, la administración de Recorridos de cliente le permite añadir registros TXT de verificación de sitios de Google especiales a sus subdominios para garantizar que se verifiquen.

>[!NOTE]
>
> Esta operación solo se puede realizar una vez que un subdominio tiene la variable **[!UICONTROL Success]** estado. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](access-subdomains.md).

Para agregar un registro TXT de Google al subdominio, siga estos pasos:

1. Abra el subdominio desde el **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** para abrir el Navegador.

1. En la sección Google txt record , introduzca el código de verificación generado en [Herramientas de administración de G Suite](https://support.google.com/a/answer/183895)y haga clic en **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Una vez agregado el registro TXT, Google debe verificarlo. Para ello, vaya a las herramientas de administración de G Suite y, a continuación, inicie el paso de verificación.
