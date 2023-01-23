---
solution: Journey Optimizer
product: journey optimizer
title: Cambiar las direcciones de correo electrónico principales
description: Aprenda a determinar qué dirección de correo electrónico utilizar desde el servicio de perfil.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: principal, ejecución, correo electrónico, destino, perfil, optimizador
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# Cambiar las direcciones principales {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Defina qué dirección utilizar"
>abstract="Cuando hay varias direcciones de correo electrónico o números de teléfono disponibles en la base de datos (personal, profesional, etc.), puede elegir cuál priorizar para el envío."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Defina qué dirección utilizar"
>abstract="Edite los campos utilizados para determinar la dirección de correo electrónico o el número de teléfono de los perfiles que desea priorizar para el envío."

Cuando se segmenta un perfil, es posible que haya varias direcciones de correo electrónico o números de teléfono disponibles en la base de datos (dirección de correo electrónico profesional, número de teléfono personal, etc.).

con [!DNL Journey Optimizer], puede determinar qué dirección de correo electrónico o número de teléfono utilizar desde el servicio de perfil y priorizar cuándo hay varias direcciones disponibles. Para realizar esto, siga los pasos a continuación.

1. Acceda a la  **[!UICONTROL Canales]** > **[!UICONTROL General]** > **[!UICONTROL Campos de ejecución]** para abrir el Navegador.

   ![](assets/primary-address-execution-fields.png)

1. Los campos que se utilizan actualmente de forma predeterminada para determinar la dirección de correo electrónico y el número de teléfono de los perfiles se muestran en esta pantalla. Haga clic en **[!UICONTROL Editar]** para cambiarlos.

   ![](assets/primary-address.png)

1. Haga clic en el campo actual de su elección o en el icono de edición para seleccionar un nuevo campo.

   ![](assets/primary-address-edit.png)

1. Se muestra la lista de campos XDM de tipo correo electrónico disponibles. Seleccione el campo que desea utilizar.

   ![](assets/primary-address-select-field.png)

1. Haga clic en **[!UICONTROL Guardar]** para confirmar su elección.

El campo de ejecución se actualiza y ahora se utiliza como dirección principal.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
