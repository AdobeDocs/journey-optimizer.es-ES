---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a la configuración de correo electrónico
description: Obtenga más información sobre la configuración de correo electrónico en [!DNL Journey Optimizer]
role: Admin
level: Intermediate
feature: Application Settings
topic: Administration
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Introducción a la configuración de correo electrónico {#get-starte-email-config}

Para poder enviar correos electrónicos a través de recorridos y campañas en [!DNL Journey Optimizer], debe seguir varios pasos de configuración.

1. Para garantizar una entrega óptima y proteger su reputación, comience delegando a Adobe los subdominios que va a utilizar para enviar sus correos electrónicos con [!DNL Journey Optimizer]. Estos subdominios determinarán elementos como las páginas web de las que se realizará un seguimiento y las direcciones URL de las páginas espejo. [Más información](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Mejore su capacidad de envío y reputación de correo electrónico agrupando las direcciones IP aprovisionadas con su instancia. [Más información](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Cree superficies de canal y seleccione la opción **[!UICONTROL Email]** canal. [Más información](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. En cada superficie de canal de correo electrónico, configure todos los parámetros técnicos necesarios para enviar correos electrónicos. [Más información](email-settings.md)

   * Aquí es donde se selecciona el subdominio que se utilizará para enviar los correos electrónicos y los grupos de IP que se asociarán con la superficie. [Más información](email-settings.md#subdomains-and-ip-pools)

   ![](assets/preset-subdomain-ip-pool.png)

   * La variable **[!UICONTROL Sender email]** y **[!UICONTROL Error email]** Las direcciones deben utilizar el subdominio delegado seleccionado actualmente. [Más información](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Determine qué dirección de correo electrónico utilizar con prioridad para los destinatarios cuando haya varias direcciones disponibles en Adobe Experience Platform. [Más información](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Administre el número de días durante los cuales se realizan los reintentos antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
