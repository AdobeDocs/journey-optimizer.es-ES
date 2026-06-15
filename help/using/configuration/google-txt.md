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
TQID: https://experienceleague.adobe.com/FCUB2NeETecjNGYnVhkpkYtEZqgX6y-czXinn2t3J84
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 25%

---

# Añadir un registro TXT de Google a un subdominio {#google-txt-record}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a agregar y actualizar un registro TXT de verificación del sitio de Google en su subdominio para garantizar el envío correcto de correos electrónicos a las direcciones de Gmail.

>[!ENDSHADEBOX]

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
