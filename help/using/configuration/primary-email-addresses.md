---
title: 'Cambiar las direcciones de correo electrónico principales '
description: Aprenda a determinar qué dirección de correo electrónico utilizar desde el servicio de perfil.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 5071de634c9dbb13908d3190fe1157831c372c7d
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 7%

---

# Cambiar las direcciones de correo electrónico principales {#change-primary-email}

Al segmentar un perfil, es posible que haya varias direcciones de correo electrónico disponibles en la base de datos (personal, dirección de correo electrónico profesional, etc.).

con [!DNL Journey Optimizer], puede determinar qué dirección de correo electrónico utilizar desde el servicio de perfil y priorizar cuándo hay varias direcciones disponibles. Para realizar esto, siga los pasos a continuación.

1. Acceda al menú **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]**.

   ![](assets/primary-address-execution-fields.png)

1. El campo que se utiliza actualmente de forma predeterminada para determinar las direcciones de correo electrónico de los perfiles se muestra en esta pantalla. Haga clic en **[!UICONTROL Edit]** para cambiarlo.

   ![](assets/primary-address.png)

1. Haga clic en el campo actual o en el icono de edición para seleccionar un nuevo campo.

   ![](assets/primary-address-edit.png)

1. Se muestra la lista de campos XDM de tipo correo electrónico disponibles. Seleccione el campo que desea utilizar.

   ![](assets/primary-address-field.png)

1. Haga clic en **[!UICONTROL Save]** para confirmar su elección.

   ![](assets/primary-address-save.png)

   El campo de ejecución se actualiza y ahora se utiliza como dirección principal.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
