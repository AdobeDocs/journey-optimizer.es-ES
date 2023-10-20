---
title: Seleccionar perfiles de prueba
description: Obtenga información sobre cómo seleccionar perfiles de prueba para previsualizar y probar contenido.
feature: Preview, Proofs
role: User
level: Beginner
source-git-commit: 6da7f4c8caa5a0a6cfda1e90d0c6cd4787c6afca
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 2%

---

# Seleccionar perfiles de prueba {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="Uso de perfiles de prueba para comprobar el contenido"
>abstract="Utilice perfiles de prueba para previsualizar y probar el contenido. Si ha añadido campos personalizados, puede comprobar cómo se muestran utilizando datos de perfil de prueba."

Antes de previsualizar o probar el contenido, primero debe seleccionar perfiles de prueba, que son destinatarios adicionales que no coinciden con los criterios de objetivo definidos. [Obtenga información sobre cómo crear perfiles de prueba](../audience/creating-test-profiles.md)

Para seleccionar perfiles de prueba, siga estos pasos:

1. En la pantalla de edición de contenido del mensaje o en el Diseñador de correo electrónico, haga clic en **[!UICONTROL Simular contenido]** botón.

1. Haga clic en **[!UICONTROL Administración de perfiles de prueba]** a continuación, seleccione el área de nombres que se utilizará para identificar los perfiles de prueba haciendo clic en el **[!UICONTROL Área de nombres de identidad]** icono de selección. [Más información sobre las Áreas de nombres de identidad de Adobe Experience Platform](../audience/get-started-identity.md).

   En el ejemplo siguiente, utilizamos el **Correo electrónico** namespace.

   ![](../email/assets/previewselect-namespace.png)

1. Utilice el campo de búsqueda para encontrar el área de nombres, selecciónela y haga clic en **[!UICONTROL Seleccionar]**

   ![](../email/assets/preview-email-namespace.png)

1. En el **[!UICONTROL Valor de identidad]** , introduzca el valor (aquí la dirección de correo electrónico) para identificar el perfil de prueba y haga clic en **[!UICONTROL Añadir perfil]**.

   <!--![](assets/preview-identity-value.png)-->

1. Si ha añadido personalización al mensaje, agregue otros perfiles para poder probar distintas variantes del mensaje según los datos del perfil. Una vez añadidos, los perfiles se enumeran en los campos seleccionados.

   ![](../email/assets/preview-profile-list.png)

   En función de los elementos de personalización de mensajes, esta lista muestra los datos de cada perfil de prueba en las columnas relacionadas.
