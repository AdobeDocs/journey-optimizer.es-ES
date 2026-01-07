---
solution: Journey Optimizer
product: journey optimizer
title: Añadir un registro TXT de Google a un subdominio
description: Obtenga información sobre cómo agregar un registro TXT de Google a un subdominio
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdominio, google, txt, registro, gmail, envío
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: a23f13bea69d1539cc2cd27a701e20287ddba026
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 24%

---

# Añadir un registro TXT de Google a un subdominio {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Registros TXT de Google"
>abstract="Para garantizar un envío correcto de correos electrónicos a las direcciones de Gmail, puede añadir registros TXT de verificación de sitios de Google especiales a su subdominio para asegurarse de que estén verificados."

Los registros TXT son un tipo de registro DNS que se utiliza para proporcionar información de texto sobre un dominio y que pueden leer fuentes externas.

Para garantizar una entrega óptima y una entrega correcta de correos electrónicos a las direcciones de Gmail, [!DNL Journey Optimizer] le permite agregar registros TXT de verificación de sitios de Google especiales al subdominio para asegurarse de que se ha verificado.

>[!CAUTION]
>
> Esta operación solo se puede realizar una vez que un subdominio tenga el estado **[!UICONTROL Success]**. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](delegate-subdomain.md#access-delegated-subdomains).

## Añadir un registro TXT de Google {#add-google-txt-record}

Para agregar un registro TXT de Google al subdominio, siga estos pasos:

1. Abra el subdominio desde el menú **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Subdominios]**.

1. En la sección **[!UICONTROL registro txt de Google]**, escribe el código de verificación generado desde [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> y luego haz clic en **[!UICONTROL Guardar]**.

   ![](assets/subdomain-google-txt.png)

1. Una vez agregado el registro TXT, Google debe verificarlo. Para ello, vaya a [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools--> y luego inicie el paso de verificación.

## Actualizar un registro TXT de Google {#update-google-txt-record}

Para actualizar un registro TXT de Google existente, siga estos pasos:

1. Abra el subdominio desde el menú **[!UICONTROL Subdominios]**.

1. Borre el valor existente en el campo **[!UICONTROL registro txt de Google]** y haga clic en **[!UICONTROL Guardar]**. Este paso reemplaza el valor de registro TXT de Google anterior por una cadena vacía.

1. A continuación, vuelva a abrir el mismo subdominio e introduzca el nuevo código de verificación.

1. Vuelva a hacer clic en **[!UICONTROL Guardar]**.

1. Compruebe el registro actualizado mediante [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}.
