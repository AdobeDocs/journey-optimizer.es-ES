---
solution: Journey Optimizer
product: journey optimizer
title: Integración de proveedor
description: Utilice Integraciones de Adobe Journey Optimizer con cualquier plataforma externa que exponga una API válida, además de patrones de proveedor probados por ingeniería para confiar en usted al diseñar su configuración.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: integración, proveedor, terceros
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---


# Integración de proveedores {#vendor-integration}

Puede usar **Integraciones** en Adobe Journey Optimizer para llamar a **sistemas externos a través de HTTP** cuando cada sistema exponga un **extremo de API** que se adapte a su caso de uso y sea compatible con la forma en que las integraciones emiten solicitudes y consumen respuestas. Para ver el flujo de trabajo completo, consulte [Trabajar con integraciones](integrations.md).

La lista de soluciones de terceros descrita es ilustrativa, no exhaustiva. Podrán utilizarse otras plataformas cuando cumplan los requisitos del producto.

## Protecciones operativas {#operational-guardrails}

Al configurar cualquier integración en esta guía o en un proveedor similar, aplique lo siguiente:

* **Formato de respuesta:** Las integraciones asignan campos de **JSON** o **HTML** respuestas. Design llama a para que la API devuelva un JSON o un HTML adecuado para la asignación en el momento de la creación.
* **Campos y carga útil:** Solicite y asigne solo los atributos que necesite. Las respuestas más pequeñas reducen la latencia y limitan la exposición de datos confidenciales.
* **Forma de extremo:** prefiere la recuperación estable de **un solo recurso** (por ejemplo, una entrada, un producto o un miembro) sobre los extremos de paginación o lista amplia cuando el producto espera búsquedas de destino. Ver [Limitaciones y exclusiones](#limitations-exclusions) y [Trabajar con integraciones](integrations.md).
* **Volumen y confiabilidad:** Respeta los **límites de tarifa** del proveedor. Configure las directivas **timeout**, **retry** y **cache** para su canal (por ejemplo, correo electrónico por lotes vs. envíos transaccionales) y valide bajo carga.
* **Seguridad:** Almacena y rota tokens, claves de API y credenciales de OAuth según las políticas de tu organización. No incruste secretos en el contenido del mensaje.


## Limitaciones y exclusiones {#limitations-exclusions}

La lista de soluciones de terceros es **ilustrativa**, no exhaustiva. Las API de proveedor, los hosts, los límites de velocidad y las formas de respuesta JSON o HTML pueden cambiar. Confirme los puntos de conexión, la autenticación y la asignación de campos con la documentación actual del proveedor y su suscripción. Los patrones aquí asumen **llamadas orientadas a la lectura** adecuadas para la personalización. Las integraciones solo admiten la asignación de **JSON** y **HTML** respuestas. No se admiten **devoluciones**, **exportaciones por lotes** ni respuestas en ningún otro formato.

## Navegación rápida {#quick-navigation}

Utilice estos vínculos agrupados para ir rápidamente al patrón de proveedor relevante:

* **Sistema de administración de contenido:** [Contenido](vendor-integration.md#contentful), [Área de sitio](vendor-integration.md#sitecore), [Salsify](vendor-integration.md#salsify), [Contentstack](vendor-integration.md#contentstack), [Akeneo](vendor-integration.md#akeneo), [Magnolia](vendor-integration.md#magnolia)
* **Fidelidad y recompensas:** [Voucherify](vendor-integration.md#voucherify), [Talon.One](vendor-integration.md#talon-one), [Antavo](vendor-integration.md#antavo), [Fidelidad Salesforce](vendor-integration.md#salesforce-loyalty), [Capillary](vendor-integration.md#capillary)
* **Plantillas, personalización y recomendaciones:** [Stensul](vendor-integration.md#stensul), [Marigold](vendor-integration.md#marigold), [Adobe Target Recommendations](vendor-integration.md#adobe-target-recommendations)
* **Datos, tiempo y operaciones:** [AccuWeather](vendor-integration.md#accuweather), [ShipStation](vendor-integration.md#shipstation), [RevenueCat](vendor-integration.md#revenuecat), [Databricks](vendor-integration.md#databricks)
* **Comentarios, consentimiento y asistencia social:** [Bynder](vendor-integration.md#bynder), [Trustpilot](vendor-integration.md#trustpilot), [Bazaarvoice](vendor-integration.md#bazaarvoice), [OneTrust](vendor-integration.md#onetrust), [Meta](vendor-integration.md#meta), [Aprimo](vendor-integration.md#aprimo), [Epsilon (Epsilon3)](vendor-integration.md#epsilon)
