---
solution: Journey Optimizer
product: journey optimizer
title: Integración de proveedor
description: Utilice Integraciones de Adobe Journey Optimizer con cualquier plataforma externa que exponga una API válida, además de patrones de proveedor probados por ingeniería para confiar en usted al diseñar su configuración.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: integración, proveedor, terceros
source-git-commit: e4c298fb1c47501920a27a93b43878327b6c5861
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---


# Introducción a la integración de proveedores {#vendor-integration}

>[!BEGINSHADEBOX]

Tabla de contenido:

* [Trabajo con integraciones](integrations.md)
* **[Introducción a la integración de proveedores](vendor-integration-gs.md)**
* [Proveedores disponibles](vendor-integration.md)
* [Preguntas más frecuentes](vendor-integration-faq.md)

>[!ENDSHADEBOX]


Puede usar **Integraciones** en Adobe Journey Optimizer para llamar a **sistemas externos a través de HTTP** cuando cada sistema exponga un **extremo de API** que se adapte a su caso de uso y sea compatible con la forma en que las integraciones emiten solicitudes y consumen respuestas. Para ver el flujo de trabajo completo, consulte [Trabajar con integraciones](integrations.md).

La lista de soluciones de terceros descrita es ilustrativa, no exhaustiva. Podrán utilizarse otras plataformas cuando cumplan los requisitos del producto.

## Protecciones operativas {#operational-guardrails}

Al configurar cualquier integración en esta guía o en un proveedor similar, aplique lo siguiente:

* **Formato de respuesta:** Las integraciones asignan campos de **JSON** respuestas. Design llama a para que la API devuelva un JSON adecuado para la asignación en el momento de la creación.
* **Campos y carga útil:** Solicite y asigne solo los atributos que necesite. Las respuestas más pequeñas reducen la latencia y limitan la exposición de datos confidenciales.
* **Forma de extremo:** prefiere la recuperación estable de **un solo recurso** (por ejemplo, una entrada, un producto o un miembro) sobre los extremos de paginación o lista amplia cuando el producto espera búsquedas de destino. Ver [Limitaciones y exclusiones](#limitations-exclusions) y [Trabajar con integraciones](integrations.md).
* **Volumen y confiabilidad:** Respeta los **límites de tarifa** del proveedor. Configure las directivas **timeout**, **retry** y **cache** para su canal (por ejemplo, correo electrónico por lotes vs. envíos transaccionales) y valide bajo carga.
* **Seguridad:** Almacena y rota tokens, claves de API y credenciales de OAuth según las políticas de tu organización. No incruste secretos en el contenido del mensaje.

## Limitaciones y exclusiones {#limitations-exclusions}

La lista de soluciones de terceros es **ilustrativa**, no exhaustiva. Las API de proveedor, los hosts, los límites de velocidad y las formas de respuesta JSON pueden cambiar. Confirme los puntos de conexión, la autenticación y la asignación de campos con la documentación actual del proveedor y su suscripción. Los patrones aquí asumen **llamadas orientadas a la lectura** adecuadas para la personalización. La reescritura, las exportaciones por lotes o las respuestas que no sean JSON pueden estar fuera de ámbito a menos que se indique lo contrario.

## Navegación rápida {#quick-navigation}

Utilice estos vínculos agrupados para ir rápidamente al patrón de proveedor relevante:

* **Contenido y CMS:** [Contenido](#contentful), [Área de sitio](#sitecore), [Salsify](#salsify), [Contentstack](#contentstack), [Akeneo](#akeneo), [Magnolia](#magnolia)
* **Fidelidad y recompensas:** [Voucherify](#voucherify), [Talon.One](#talon-one), [Antavo](#antavo), [Fidelidad Salesforce](#salesforce-loyalty), [Capillary](#capillary)
* **Plantillas y mensajes:** [Stensul](#stensul), [Marigold](#marigold), [Adobe Target Recommendations](#adobe-target-recommendations)
* **Datos, tiempo y operaciones:** [AccuWeather](#accuweather), [ShipStation](#shipstation), [RevenueCat](#revenuecat), [Databricks](#databricks)
* **Comentarios, consentimiento y asistencia social:** [Bynder](#bynder), [Trustpilot](#trustpilot), [Bazaarvoice](#bazaarvoice), [OneTrust](#onetrust), [Meta](#meta), [Aprimo](#aprimo), [Epsilon (Epsilon3)](#epsilon)
