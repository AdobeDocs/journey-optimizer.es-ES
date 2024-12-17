---
solution: Journey Optimizer
product: journey optimizer
title: AEM Fragmentos de contenido
description: AEM Obtenga información sobre cómo acceder a fragmentos de contenido y administrarlos de forma
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 50b36446ff0e9f4aec9f28056c3c30cc2df3f530
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

---

# Fragmentos de contenido de Adobe Experience Manager {#aem-fragments}

Al integrar Adobe Experience Manager con Adobe Journey Optimizer AEM, ahora puede incorporar sin problemas los fragmentos de contenido de la en el contenido del correo electrónico de Journey Optimizer. AEM Esta conexión optimizada simplifica el proceso de acceso y uso del contenido de la, lo que permite crear campañas y recorridos personalizados y dinámicos.

AEM Para obtener más información sobre el fragmento de contenido de la, consulte [Documentación del Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments).

## Limitaciones {#limitations}

* Solo disponible para el canal de correo electrónico.

* AEM Actualmente, los usuarios no pueden cambiar la instancia de a la que están conectados, ya que cada zona protegida está limitada a una sola instancia.

* Se recomienda limitar el número de usuarios con acceso a los fragmentos de contenido de publicación para reducir el riesgo de errores accidentales en los correos electrónicos.

* Para el contenido multilingüe, solo se admite el flujo manual.

* Actualmente no se admiten variantes.

* Debe crear una etiqueta específica para Journey Optimizer.

+++ Obtenga información sobre cómo crear su etiqueta de Journey Optimizer

   1. Acceda a su entorno de **Experience Manager**.

   1. En el menú **Herramientas**, vaya a la ficha **General** y seleccione **Etiquetado**.

   1. Haga clic en **Crear una etiqueta nueva**.

   1. Asegúrese de que el identificador cumple la siguiente sintaxis: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

   1. Haga clic en **Crear**.

  Ahora puede asignar esta etiqueta de Journey Optimizer a los fragmentos de contenido.
+++

## AEM Añadir fragmentos de contenido {#aem-add}

AEM Después de crear y personalizar sus [Fragmentos de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments), ahora puede importarlos a su campaña o recorrido de Recorrido Optimizer.

1. Después de crear tu [campaña](../email/create-email.md) o [Recorrido](../email/create-email.md) con una acción de correo electrónico, accede al diseñador de correo electrónico para configurar el contenido del correo electrónico. [Más información](../email/get-started-email-design.md)

1. Haga clic dentro de un bloque de texto o en la línea de asunto y seleccione **[!UICONTROL Agregar Personalization]** en la barra de herramientas contextual.

   ![](assets/aem_campaign_2.png)

1. AEM AEM En el menú **[!UICONTROL Fragmento de contenido]** del panel izquierdo, haga clic en **[!UICONTROL Abrir selector de CF de la]**.

   ![](assets/aem_campaign_3.png)

1. Seleccione un **[!UICONTROL fragmento de contenido]** de la lista disponible para importarlo al contenido de Journey Optimizer.

   >[!IMPORTANT]
   >
   >Solo se pueden usar los **[!UICONTROL fragmentos de contenido]** publicados.

1. Haga clic en **[!UICONTROL Mostrar filtros]** para ajustar la lista de fragmentos de contenido.

   El selector Fragmento de contenido incluye filtros preconfigurados:

   * **[!UICONTROL Estado]**: publicado, modificado
   * **[!UICONTROL Etiqueta]**: se define automáticamente en función de su entorno de Journey Optimizer (ID de organización y espacio aislado)

   ![](assets/aem_campaign_4.png)

1. Después de seleccionar su **[!UICONTROL fragmento de contenido]**, haga clic en **[!UICONTROL Seleccionar]** para abrirlo.

   ![](assets/aem_campaign_5.png)

1. Elija los campos que desee de su **[!UICONTROL Fragmento de contenido]** para agregarlos al contenido.

   ![](assets/aem_campaign_6.png)

1. Haz clic en **[!UICONTROL Guardar]** y comprueba tu mensaje en la vista previa. Ahora puede probar y comprobar el contenido del mensaje como se detalla en [esta sección](preview.md).

Una vez que haya realizado las pruebas y validado el contenido, puede enviar su correo electrónico a la audiencia con su [campaña](../campaigns/review-activate-campaign.md) o [Recorrido](../building-journeys/publishing-the-journey.md).

