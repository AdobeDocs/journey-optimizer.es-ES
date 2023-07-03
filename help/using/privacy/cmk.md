---
solution: Journey Optimizer
product: journey optimizer
title: Claves gestionadas por el cliente
description: Obtenga información sobre cómo configurar y administrar las claves de cliente para Adobe Journey Optimizer.
feature: Monitoring
role: Developer, User, Admin, Leader
level: Intermediate
source-git-commit: 7f905ad1f1afbfc55b27eab8efc0a20b35f183de
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 5%

---

# Configurar y administrar claves administradas por el cliente para Adobe Journey Optimizer {#cmk}

>[!AVAILABILITY]
>
>[!DNL Customer Managed Keys] actualmente, esta funcionalidad solo está disponible para las organizaciones que han adquirido [Healthcare Shield o Privacy &amp; Security Shield](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html) oferta de complementos.

Con Adobe Journey Optimizer, [Healthcare Shield](https://www.adobe.com/trust/compliance/hipaa-ready.html) y los clientes de Privacy &amp; Security Shield pueden aprovechar las claves gestionadas por el cliente de Azure (CMK) y aplicarlas a sus datos.

El proceso de configuración de Journey Optimizer consta de dos partes, que aprovechan la tecnología tanto de Adobe Experience Platform como de Customer Journey Analytics (CJA):

* Siga los pasos descritos en la sección [Claves gestionadas por el cliente en Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys.html?lang=es) documentación.

* Siga los pasos descritos en la sección [Claves gestionadas por el cliente en Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-privacy/cmk.html) documentación.

  Completar este proceso de configuración es necesario, incluso si no ha adquirido Customer Journey Analytics (CJA), ya que ciertos componentes de CJA se utilizan en segundo plano.

Para pasar por el proceso de configuración, puede consultar las instrucciones detalladas paso a paso en [Claves gestionadas por el cliente en Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html) documentación.

Tanto Adobe Experience Platform como las claves gestionadas por el cliente garantizan la seguridad de sus datos cifrándolos en tránsito y en reposo. Los datos permanecen protegidos, independientemente de si utiliza claves gestionadas por el cliente.

Para obtener más información sobre el cifrado de datos en Adobe Experience Platform, consulte la [documentación](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html) en el cifrado de datos.
