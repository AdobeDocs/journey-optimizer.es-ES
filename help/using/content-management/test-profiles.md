---
title: Seleccionar perfiles de prueba
description: Obtenga información sobre cómo seleccionar perfiles de prueba para previsualizar y probar contenido.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: c51e4089-7f51-437d-a5ed-de10bab46cf8
source-git-commit: 95a6d032808bc735a27a98dcb61efefa93cf5047
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 16%

---

# Seleccionar perfiles de prueba {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="Utilice perfiles de prueba para comprobar el contenido"
>abstract="Utilice perfiles de prueba para previsualizar y probar el contenido. Si ha añadido campos personalizados, puede comprobar cómo se muestran utilizando los datos del perfil de prueba."

Los perfiles de prueba son destinatarios adicionales que no coinciden con los criterios de objetivo definidos. [Aprenda a crear perfiles de prueba](../audience/creating-test-profiles.md)

Antes de usar perfiles de prueba para probar el contenido, primero debe seleccionarlos. Para ello, siga estos pasos:

1. En la pantalla Editar contenido del mensaje o en el Designer de correo electrónico, haga clic en el botón **[!UICONTROL Simular contenido]** y seleccione **[!UICONTROL Simular contenido]**.

1. Haga clic en el botón **[!UICONTROL Administrar perfiles de prueba]** y, a continuación, seleccione el área de nombres que se utilizará para identificar los perfiles de prueba haciendo clic en el icono de selección **[!UICONTROL Área de nombres de identidad]**. [Obtenga más información acerca de áreas de nombres de identidad de Adobe Experience Platform](../audience/get-started-identity.md).

   En el ejemplo siguiente, utilizamos el área de nombres **Email**.

   ![](../email/assets/previewselect-namespace.png)

1. Utilice el campo de búsqueda para encontrar el área de nombres, selecciónela y haga clic en **[!UICONTROL Seleccionar]**

   ![](../email/assets/preview-email-namespace.png)

1. En el campo **[!UICONTROL Valor de identidad]**, ingrese el valor (aquí la dirección de correo electrónico) para identificar el perfil de prueba y haga clic en **[!UICONTROL Agregar perfil]**.

   <!--![](assets/preview-identity-value.png)-->

1. Si ha añadido personalización al mensaje, agregue otros perfiles para poder probar distintas variantes del mensaje según los datos del perfil. Una vez añadidos, los perfiles se enumeran en los campos seleccionados.

   ![](../email/assets/preview-profile-list.png)

   En función de los elementos de personalización de mensajes, esta lista muestra los datos de cada perfil de prueba en las columnas relacionadas.

>[!NOTE]
>
>Además de los perfiles de prueba, [!DNL Journey optimizer] también le permite probar distintas variantes del contenido mediante la vista previa y el envío de pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV/JSON, o agregados manualmente. [Aprenda a simular variaciones de contenido](../test-approve/simulate-sample-input.md)
