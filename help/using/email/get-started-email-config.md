---
solution: Journey Optimizer
product: journey optimizer
title: Empezar con la configuración de correo electrónico
description: Obtenga más información sobre la configuración de correo electrónico en [!DNL Journey Optimizer]
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: correo electrónico, configuración, superficie, subdominios
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
TQID: https://experienceleague.adobe.com/mVdk2WGb0rL06j1cmNEh4fj0JC-hwuro8ku-0Yv02N8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: fae48155-b23f-40d2-a252-a25bce350b4d
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 84%

---

# Empezar con la configuración de correo electrónico {#get-starte-email-config}

Para poder enviar correos electrónicos a través de recorridos y campañas en [!DNL Journey Optimizer], debe seguir varios pasos de configuración.

1. Para garantizar una entregabilidad óptima y proteger su reputación, empiece **delegando en Adobe los subdominios** que va a utilizar para enviar sus correos electrónicos con [!DNL Journey Optimizer]. Estos subdominios determinarán elementos como las páginas web de las que se realizará un seguimiento y las direcciones URL de las páginas espejo. [Más información](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Cree grupos de IP para **agrupar conjuntamente las direcciones IP** suministradas con su instancia. [Más información](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Cree **configuraciones de canal** y seleccione el canal de **[!UICONTROL Correo electrónico]**. [Más información](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. En cada configuración de canal de correo electrónico, configure todos los **parámetros técnicos** necesarios para enviar correos electrónicos. [Más información](email-settings.md)

   * Aquí es donde se selecciona el subdominio que se utilizará para enviar los correos electrónicos y los grupos de IP que se asociarán con la configuración. [Más información](email-settings.md#ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * El **[!UICONTROL prefijo del correo electrónico de origen]** y el **[!UICONTROL prefijo del correo electrónico de error]** utilizan el [subdominio delegado seleccionado](../configuration/about-subdomain-delegation.md). Opcionalmente, **[!UICONTROL Nombre del remitente]** y **[!UICONTROL Correo electrónico del remitente]** pueden identificar a una parte transmisora diferente (dirección completa de **Remitente**, no vinculada a ese sufijo de subdominio). [Más información](header-parameters.md#sender-header)

   ![](assets/preset-header.png)

1. Determine qué **campos de ejecución** va a utilizar prioritariamente para los destinatarios cuando haya varias direcciones disponibles en Adobe Experience Platform. [Más información](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Administre el número de días durante los cuales se realizan **reintentos** antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
