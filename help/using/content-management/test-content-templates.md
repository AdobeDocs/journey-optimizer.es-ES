---
solution: Journey Optimizer
product: journey optimizer
title: Prueba de plantillas de contenido
description: Obtenga información sobre cómo probar el procesamiento de algunas de las plantillas de contenido de correo electrónico
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 4%

---

# Prueba de plantillas de contenido de correo electrónico {#test-template}

Puede probar la renderización de algunas de las plantillas de correo electrónico, tanto si se crean desde cero como a partir de contenido existente. Para ello, siga los pasos que aparecen a continuación.

1. Acceda a la lista de plantillas de contenido a través de **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Plantillas de contenido]** y seleccione cualquier plantilla de correo electrónico.

1. Clic **[!UICONTROL Editar contenido]** desde el **[!UICONTROL Propiedades de plantilla]**.

1. Clic **[!UICONTROL Simular contenido]** y seleccione un perfil de prueba para comprobar la renderización. [Más información](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. Puede enviar una prueba para probar el contenido y que sea aprobado por algunos usuarios internos antes de utilizarlo en un recorrido o una campaña.

   * Para ello, haga clic en el **[!UICONTROL Enviar prueba]** y siga los pasos descritos en [esta sección](../content-management/proofs.md).

   * Antes de enviar la prueba, debe seleccionar [superficie de correo electrónico](../configuration/channel-surfaces.md) que se utilizará para probar el contenido.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Actualmente, el seguimiento no es compatible con las plantillas de contenido de prueba de correo electrónico, lo que significa que el seguimiento de eventos, parámetros de UTM y vínculos de página de aterrizaje no serán efectivos en las pruebas que se envían desde una plantilla. Para probar el seguimiento, [usar la plantilla de contenido](../email/use-email-templates.md) en un correo electrónico y [enviar una prueba](../content-management/preview-test.md#send-proofs).
