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
source-git-commit: 22a8742bf9000ed1cc8437d7ac89747276284dbf
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 4%

---

# Prueba de plantillas de contenido de correo electrónico {#test-template}

Puede probar la renderización de algunas de las plantillas de correo electrónico, tanto si se crean desde cero como a partir de contenido existente. Para ello, siga los pasos que aparecen a continuación.

1. Acceda a la lista de plantillas de contenido a través del menú **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas de contenido]** y seleccione cualquier plantilla de correo electrónico.

1. Haga clic en **[!UICONTROL Editar contenido]** en las **[!UICONTROL propiedades de la plantilla]**.

1. Haga clic en **[!UICONTROL Simular contenido]** y seleccione un perfil de prueba para comprobar su renderización. [Más información](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

   >[!NOTE]
   >
   >[!DNL Journey optimizer] también le permite probar diferentes variantes de sus plantillas de contenido previsualizándolas y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente. [Aprenda a simular variaciones de contenido](../test-approve/simulate-sample-input.md)

1. Puede enviar una prueba para probar el contenido y que sea aprobado por algunos usuarios internos antes de utilizarlo en un recorrido o una campaña.

   * Para ello, haga clic en el botón **[!UICONTROL Enviar revisión]** y siga los pasos descritos en [esta sección](../content-management/proofs.md).

   * Antes de enviar la prueba, debe seleccionar la [configuración de correo electrónico](../configuration/channel-surfaces.md) que se utilizará para probar el contenido.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Actualmente, el seguimiento no es compatible con las plantillas de contenido de prueba de correo electrónico, lo que significa que el seguimiento de eventos, parámetros de UTM y vínculos de página de aterrizaje no serán efectivos en las pruebas que se envían desde una plantilla. Para probar el seguimiento, [use la plantilla de contenido](../email/use-email-templates.md) en un mensaje de correo electrónico y envíe una prueba usando perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o agregados manualmente. [Obtenga información sobre cómo obtener una vista previa y probar el contenido](../content-management/preview-test.md)
