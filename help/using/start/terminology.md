---
solution: Journey Optimizer
product: journey optimizer
title: Terminología clave
description: Términos y conceptos esenciales en Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 4ae9e908d259dbd266417242cf9e65d693227061
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 9%

---

# Terminología clave {#key-terminology}

Esta guía de referencia define los términos esenciales que se encontrará al utilizar Adobe Journey Optimizer. Comprender estos conceptos le ayuda a navegar por la plataforma con seguridad y a colaborar eficazmente con su equipo.

>[!TIP]
>
>Para obtener explicaciones detalladas sobre las funciones y los flujos de trabajo, consulte las secciones de documentación específicas vinculadas a través de esta guía.

## Términos de la plataforma principal {#core-terms}

| Término | Definición |
|------|------------|
| **Adobe Journey Optimizer** | Una aplicación para crear y enviar mensajes personalizados a los clientes a través de canales (correo electrónico, SMS, notificaciones push, web). Permite diseñar recorridos de clientes que respondan a las acciones de los clientes en tiempo real. |
| **Adobe Experience Platform** | La base de Adobe Journey Optimizer que recopila y organiza todos los datos de clientes en un solo lugar. Crea perfiles de cliente unificados que Journey Optimizer utiliza para la personalización. [Más información](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=es){target="_blank"} |
| **Perfil del cliente en tiempo real** | Una vista unificada en tiempo real de cada cliente que combina datos de varios canales, incluidos datos en línea, sin conexión, CRM y de terceros. Cada perfil se actualiza dinámicamente a medida que los clientes interactúan con la marca. [Más información](../audience/get-started-profiles.md) |
| **espacio aislado** | Un espacio de trabajo independiente para pruebas y experimentación sin afectar a las comunicaciones con los clientes en directo. Adobe Journey Optimizer proporciona varios entornos limitados para los entornos de desarrollo, prueba y producción. [Más información](../administration/sandboxes.md) |

## Términos de recorrido y campaña {#journey-campaign-terms}

| Término | Definición |
|------|------------|
| **Recorrido** | Una serie de pasos conectados que guían a los clientes a través de las experiencias con su marca a lo largo del tiempo. Cada paso se produce en función de las acciones del cliente o los déclencheur de tiempo, lo que permite interacciones secuenciales y personalizadas. [Más información](../building-journeys/journey.md) |
| **Campaign** | Una sola comunicación o conjunto de comunicaciones enviadas a una audiencia específica. A diferencia de los recorridos que se desarrollan con el tiempo, las campañas envían mensajes según una programación o un déclencheur, ya sea de forma inmediata o a una hora específica. [Más información](../campaigns/get-started-with-campaigns.md) |
| **Evento** | Una acción u ocurrencia que pone en déclencheur o avanza un recorrido. Los eventos pueden ser acciones del cliente (realizar una compra, abandonar un carro de compras) o eventos del sistema (fecha/hora, cambio de datos). [Más información](../event/about-events.md) |
| **Canal** | El método utilizado para comunicarse con los clientes: correo electrónico, SMS, notificaciones push, mensajes en la aplicación, web o correo directo. Cada canal requiere una configuración específica. [Más información](../configuration/get-started-configuration.md) |

## Términos de cliente y audiencia {#customer-audience-terms}

| Término | Definición |
|------|------------|
| **Audiencia** | Un grupo de clientes que comparten características o comportamientos comunes, como &quot;clientes que compraron en los últimos 30 días&quot; o &quot;miembros del programa de fidelidad&quot;. Las audiencias se utilizan para segmentar clientes específicos. [Más información](../audience/about-audiences.md) |
| **Calificación de audiencias** | Proceso automático que se produce cuando un cliente se une a una audiencia o la abandona. Journey Optimizer puede almacenar en déclencheur las acciones que se producen cuando alguien entra o sale de una audiencia, lo que garantiza comunicaciones oportunas y relevantes. [Más información](../building-journeys/audience-qualification-events.md) |
| **Audiencia atractiva** | El número de perfiles de cliente con los que puede ponerse en contacto de forma activa mediante Adobe Journey Optimizer en función del acuerdo de licencia. Esto suele referirse a perfiles contratados en los últimos 12 meses. |
| **Perfil de prueba** | Perfiles ficticios utilizados para probar y previsualizar mensajes antes de enviarlos a clientes reales. Los perfiles de prueba ayudan a comprobar la personalización, el contenido y la lógica de recorrido. [Más información](../audience/creating-test-profiles.md) |

## Contenido y términos de Personalization {#content-terms}

| Término | Definición |
|------|------------|
| **Personalización** | Proceso de adaptar el contenido a clientes individuales mediante el uso de sus datos de perfil, preferencias y comportamientos. Por ejemplo, al insertar el nombre de un cliente o mostrar recomendaciones de productos basadas en el historial de navegación. [Más información](../personalization/personalize.md) |
| **Plantilla de contenido** | Un diseño de mensaje reutilizable que se puede utilizar en varias campañas y recorridos para mantener la coherencia de la marca y acelerar la creación de contenido. [Más información](../content-management/content-templates.md) |
| **Fragmento** | Un bloque de contenido reutilizable (como un encabezado, un pie de página o un banner promocional) que se puede utilizar en varios mensajes para garantizar la coherencia y permitir actualizaciones centralizadas. [Más información](../content-management/fragments.md) |
| **Página de aterrizaje** | Una página web independiente en la que los clientes pueden optar por su inclusión o exclusión de comunicaciones, suscribirse a servicios o proporcionar información a través de formularios en línea. [Más información](../landing-pages/get-started-lp.md) |

## Decisión y condiciones de la oferta {#decision-terms}

| Término | Definición |
|------|------------|
| **Gestión de decisiones** | Característica que selecciona automáticamente el mejor contenido u oferta para cada cliente en función de los datos de perfil en tiempo real, el contexto y las reglas comerciales. [Más información](../offers/get-started/starting-offer-decisioning.md) |
| **Oferta** | Un mensaje de marketing, un descuento o una promoción que se pueden presentar a los clientes. Las ofertas incluyen reglas de idoneidad que determinan qué clientes pueden recibirlas. [Más información](../offers/offer-library/creating-personalized-offers.md) |
| **Directiva de decisión** | Un conjunto de reglas y estrategias que determinan qué oferta mostrar a qué cliente en qué momento, en función de restricciones como elegibilidad, prioridad y reglas de límite. [Más información](../experience-decisioning/create-decision.md) |

## Términos de configuración y datos {#data-config-terms}

| Término | Definición |
|------|------------|
| **Esquema** | Estructura que define cómo se organizan los datos en Adobe Experience Platform, incluidos nombres de campo, tipos de datos y relaciones. Los esquemas garantizan la coherencia de los datos entre sistemas. [Más información](../data/get-started-schemas.md) |
| **Conjunto de datos** | Recopilación de datos (normalmente una tabla) que sigue un esquema específico. Los conjuntos de datos almacenan datos de clientes, eventos de interacción y otra información utilizada para la personalización. [Más información](../data/get-started-datasets.md) |

>[!NOTE]
>
>Para obtener un glosario completo de términos de Adobe Experience Platform, consulte el [glosario de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html){target="_blank"}.

## Temas relacionados {#related-topics}

* [Explicación del funcionamiento de Journey Optimizer](understanding-ajo.md)
* [Introducción a la interfaz de usuario](user-interface.md)
* [Elija su función y ruta de aprendizaje](quick-start.md)

