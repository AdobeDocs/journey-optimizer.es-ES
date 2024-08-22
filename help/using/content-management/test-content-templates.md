---
solution: Journey Optimizer
product: journey optimizer
title: Plantillas de contenido de prueba
description: Obtenga información sobre cómo probar el procesamiento de algunas de las plantillas de contenido de correo electrónico
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 01726ab6-f581-4d19-aedd-2541bc0f27c6
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 6%

---

# Prueba de plantillas de contenido de correo electrónico {#test-template}

Puede probar la renderización de algunas de las plantillas de correo electrónico, tanto si se crean desde cero como a partir de contenido existente. Para ello, siga los pasos que aparecen a continuación.

1. Acceda a la lista de plantillas de contenido a través del menú **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas de contenido]** y seleccione cualquier plantilla de correo electrónico.

1. Haga clic en **[!UICONTROL Editar contenido]** en las **[!UICONTROL propiedades de la plantilla]**.

1. Haga clic en **[!UICONTROL Simular contenido]** y seleccione un perfil de prueba para comprobar su renderización. [Más información](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. Puede enviar una prueba para probar el contenido y que sea aprobado por algunos usuarios internos antes de utilizarlo en un recorrido o una campaña.

   * Para ello, haga clic en el botón **[!UICONTROL Enviar revisión]** y siga los pasos descritos en [esta sección](../content-management/proofs.md).

   * Antes de enviar la prueba, debe seleccionar la [configuración de correo electrónico](../configuration/channel-surfaces.md) que se utilizará para probar el contenido.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Actualmente, el seguimiento no es compatible con las plantillas de contenido de prueba de correo electrónico, lo que significa que el seguimiento de eventos, parámetros de UTM y vínculos de página de aterrizaje no serán efectivos en las pruebas que se envían desde una plantilla. Para probar el seguimiento, [use la plantilla de contenido](../email/use-email-templates.md) en un mensaje de correo electrónico y [envíe una prueba](../content-management/preview-test.md#send-proofs).
