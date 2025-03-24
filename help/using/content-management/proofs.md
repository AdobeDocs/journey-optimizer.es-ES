---
title: Envío de pruebas de correo electrónico
description: Obtenga información sobre cómo enviar pruebas de correo electrónico.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: 80935cc31ef88a322c2dd555fc8998935c6e5621
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 15%

---

# Envío de pruebas de correo electrónico {#send-proofs}

Una prueba es un mensaje específico que le permite probar un mensaje antes de enviarlo al público principal. Los destinatarios de la prueba se encargan de aprobar el mensaje: procesamiento, contenido, valores de ajuste de personalización, configuración.

Tenga en cuenta que [!DNL Journey optimizer] también le permite probar diferentes variantes del contenido previsualizándolo y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente. [Aprenda a probar el contenido con datos de entrada de ejemplo](../test-approve/simulate-sample-input.md)

>[!PREREQUISITES]
>
>Para enviar pruebas, debe tener los permisos de **Aprobar y publicar** para el recurso específico (campaña o recorrido) asociado al correo electrónico. Además, para enviar pruebas en un recorrido, también se requiere el permiso **Publicar recorrido**. [Más información sobre los permisos](../administration/ootb-permissions.md).


Para enviar pruebas por correo electrónico, primero debe seleccionar [perfiles de prueba](test-profiles.md). A continuación, siga estos pasos:

1. En la pantalla **[!UICONTROL Simular]**, haga clic en el botón **[!UICONTROL Enviar revisión]**.

   ![](../email/assets/send-proof-button.png)

1. En la ventana **[!UICONTROL Enviar prueba]**, escriba el correo electrónico del destinatario y haga clic en **[!UICONTROL Agregar]** para enviarse la prueba a usted mismo o a los miembros de sus organizaciones.

   Tenga en cuenta que puede añadir hasta diez destinatarios para la entrega de prueba.

   ![](../email/assets/send-proof-add.png)

1. Seleccione los **perfiles de prueba** que se usarán para personalizar el contenido del mensaje.

   Cada destinatario de la prueba recibe tantos mensajes como el número de perfiles de prueba seleccionados. Por ejemplo, si ha añadido cinco correos electrónicos de destinatario y ha seleccionado diez perfiles de prueba, enviará cincuenta mensajes de prueba y cada destinatario recibirá diez de ellos.

1. Si es necesario, puede añadir un prefijo a la línea de asunto de la prueba. Solo caracteres alfanuméricos y caracteres especiales como . - _ ( ) [ ] se permiten como prefijo en la línea de asunto.

1. Haga clic en **[!UICONTROL Enviar revisión]**.

   ![](../email/assets/send-proof-select.png)

1. En la pantalla **[!UICONTROL Simular]**, haga clic en el botón **[!UICONTROL Ver pruebas]** para comprobar el estado.

   ![](../email/assets/send-proof-view.png)

Se recomienda enviar pruebas después de cada modificación al contenido del mensaje.

>[!NOTE]
>
>En la prueba enviada, el vínculo a la página espejo no está activo. Solo se activa en los mensajes finales.
