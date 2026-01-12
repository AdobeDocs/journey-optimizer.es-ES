---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a la optimización de contenido
description: Aprenda a utilizar la optimización de contenido para ofrecer contenido personalizado y optimizado en sus campañas y recorridos.
feature: Experimentation, Targeting
topic: Content Management
role: User
level: Beginner
keywords: optimización, segmentación, experimentación, pruebas A/B, campañas, recorridos, personalización
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 8%

---

# Introducción a la optimización de contenido {#message-optimization}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_optimization"
>title="Optimización de contenido"
>abstract="La optimización de contenido en Journey Optimizer le permite probar distintas versiones del contenido y determinar cuál tiene el mejor rendimiento. Puede utilizar la segmentación para ofrecer contenido personalizado a segmentos específicos, la experimentación para probar varias variaciones o combinar ambos enfoques para estrategias de optimización sofisticadas."

La optimización de contenido le ofrece las herramientas necesarias para enviar el mensaje correcto a la audiencia adecuada y en el momento adecuado. Al combinar perspectivas basadas en datos con potentes capacidades de personalización, puede maximizar la participación y las conversiones en sus campañas y recorridos.

La optimización de contenido está disponible tanto en [campañas](../campaigns/create-campaign.md) como en [recorridos](../building-journeys/journey-gs.md), lo que le permite aplicar las mismas estrategias de optimización en todos los puntos de contacto de clientes.

➡️ [Aprenda a aprovechar la optimización de contenido dentro de una campaña en este vídeo](#video)

## Funcionalidades de optimización {#capabilities}

Con la optimización de contenido en Journey Optimizer, puede:

* [Use targeting](optimization-targeting.md) para entregar contenido personalizado a segmentos de audiencia específicos en función de atributos de perfil, datos contextuales o pertenencia a audiencias.

* [Ejecute experimentos](optimization-experimentation.md) para probar varias variaciones de contenido e identificar cuál funciona mejor según las métricas de éxito.

* [Combine ambos enfoques](optimization-combination.md) para crear estrategias de optimización sofisticadas en las que pruebe distintas variaciones para cada segmento de destino.

## Segmentación frente a experimentación {#targeting-vs-experimentation}

Comprender la diferencia entre segmentación y experimentación le ayuda a elegir el enfoque de optimización adecuado para sus objetivos.

**Segmentación** usa reglas deterministas para entregar contenido personalizado a segmentos específicos según atributos de perfil, contexto o pertenencia a audiencias conocidos. Garantiza que el mensaje correcto llegue a la audiencia correcta.

**Experimentación** usa la asignación aleatoria para probar múltiples variaciones de contenido y descubrir cuál funciona mejor. Le ayuda a conocer qué es lo que más resuena en su audiencia a través de pruebas basadas en datos.

En la tabla siguiente se resumen las principales diferencias:

| Capacidad | Direccionamiento | Experimentación |
|--------|-----------|-----------------|
| **Método de asignación** | Determinístico: basado en reglas | Aleatorio: según la asignación de tráfico |
| **Basado en** | Atributos de perfil, contexto, audiencias | Distribución aleatoria |
| **Caso de uso** | Entrega de contenido relevante a segmentos conocidos | Descubra qué contenido tiene el mejor rendimiento |
| **Ejemplo** | Mostrar diferentes promociones por ubicación | Pruebe 2 líneas de asunto para ver qué abre más |
| **Mejor para** | Personalization a escala | Optimización y aprendizaje |

![](../campaigns/assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## Casos de uso comunes {#use-cases}

Estos son algunos escenarios típicos en los que la optimización de contenido puede ayudarle a lograr mejores resultados:

Segmentación:

* **Segmentación geográfica**: envíe ofertas específicas de la ubicación según la ubicación de sus clientes. Por ejemplo, promocione abrigos de invierno en regiones más frías y trajes de baño en climas más cálidos.

* **Optimización de dispositivos**: ofrece contenido específico del dispositivo, como diseños optimizados para escritorio para usuarios de escritorio y diseños optimizados para móviles para usuarios de smartphones.

Experimentación:

* **Pruebas A/B**: prueba diferentes líneas de asunto de correo electrónico, botones de call-to-action u ofertas promocionales para descubrir cuál genera la mayor cantidad de conversiones.

* **Marketing durante el ciclo vital**: Pruebe diferentes mensajes de incorporación para clientes nuevos en comparación con las ofertas de retención para clientes existentes.

Combinación:

* **Segmentación avanzada**: oriente a los clientes según su nivel de fidelidad y pruebe diferentes mensajes de recompensa dentro de cada nivel para maximizar la participación en todos los segmentos.

## Introducción {#get-started}

Para empezar a optimizar el contenido:

1. **Crear una campaña o un recorrido**: configura tu [campaña](../campaigns/create-campaign.md) o [recorrido](../building-journeys/journey-gs.md) y agrega al menos una acción.

1. **Elija su enfoque de optimización**:
   * [Use targeting](optimization-targeting.md) para personalizar el contenido de segmentos específicos.
   * [Use experimentación](optimization-experimentation.md) para probar múltiples variaciones.
   * [Combine ambos](optimization-combination.md) para obtener una optimización avanzada.

1. **Defina su contenido**: Cree las diferentes variaciones de contenido para su estrategia de optimización.

1. **Activar y supervisar**: inicia tu campaña o recorrido optimizado y realiza un seguimiento del rendimiento en los [informes](../reports/campaign-global-report-cja.md).

## Funcionamiento {#how-it-works}

Una vez que el recorrido o la campaña están activos, los perfiles se evalúan según los criterios definidos. En función de estas evaluaciones, cada perfil recibe la versión de contenido más adecuada:

1. **Evaluación del perfil**: cuando un perfil entra en su campaña o recorrido, Journey Optimizer evalúa sus atributos y contexto.

1. **Asignación de contenido** - Según la configuración de optimización:
   * Para **targeting**, los perfiles que coinciden con criterios específicos reciben el contenido personalizado correspondiente.
   * Para **experimentación**, los perfiles se asignan aleatoriamente a diferentes variaciones de contenido según la configuración de asignación de tráfico.
   * Para **combinaciones**, los perfiles primero coinciden con una regla de segmentación y luego se asignan aleatoriamente a una de las variaciones de experimento para ese segmento.

1. **Seguimiento del rendimiento**: Journey Optimizer realiza un seguimiento automático de las métricas de participación y los datos de conversión para ayudarle a identificar qué contenido funciona mejor.

## Vídeo práctico {#video}

Aprenda a aprovechar la optimización de contenido en campañas activadas por acciones o API. Descubra cómo dirigirse a subpúblicos, crear variaciones de mensajes por ubicación, habilitar contenido de reserva y ejecutar varios experimentos dentro de una sola campaña. Este tutorial también explica cómo administrar campañas multicanal y, al mismo tiempo, mantener la coherencia del mensaje.

>[!VIDEO](https://video.tv.adobe.com/v/3470368?quality=12)

**Temas relacionados**

* [Creación de una campaña](../campaigns/create-campaign.md)
* [Crear un recorrido](../building-journeys/journey-gs.md)
* [Experimento del contenido](../content-management/get-started-experiment.md)
