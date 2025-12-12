---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a Journey Optimizer para expertos en marketing
description: Como profesional en recorridos, obtenga más información sobre cómo trabajar con Journey Optimizer
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: e86fa9f6e62aea9dd1f7e6d35e7cf4b20f79aaa6
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 6%

---

# Introducción para expertos en marketing {#get-started-marketers}

Como **Experto en marketing** o **Profesional en recorridos** es responsable de crear ofertas y recorridos, y diseñar contenido. Puede comenzar a trabajar con [!DNL Adobe Journey Optimizer] una vez que la variable [Administrador del sistema](administrator.md) e [Ingeniero de datos](data-engineer.md) le conceda acceso y prepare su entorno.

## Introducción a lo esencial

Journey Optimizer le permite crear experiencias de cliente personalizadas y conectadas por correo electrónico, SMS, push, en la aplicación, web, tarjetas de contenido y mucho más. Trabaje con sus [administradores](administrator.md) para obtener acceso y con [ingenieros de datos](data-engineer.md) para configurar audiencias y datos.

Siga estos pasos principales para empezar a crear experiencias:

1. **Crear públicos**. Cree audiencias a través de definiciones de segmentos, cargue archivos CSV o utilice la composición de audiencias. Journey Optimizer ofrece varias formas de dirigirse a los clientes adecuados. Más información sobre [audiencias](../../audience/about-audiences.md) y [creación de definiciones de segmento](../../audience/creating-a-segment-definition.md).

1. **Diseñar contenido**. Cree mensajes convincentes en varios canales:
   * Use el **Asistente de IA** para generar contenido de correo electrónico, líneas de asunto e imágenes según las directrices de su marca. [Más información sobre la generación de contenido de IA](../../content-management/gs-generative.md)
   * **Personalice mensajes** con datos de clientes, contenido dinámico y lógica condicional. [Más información sobre la personalización](../../personalization/personalize.md)
   * **Itere en datos contextuales** para mostrar listas dinámicas a partir de eventos, acciones personalizadas y búsquedas de conjuntos de datos. [Obtenga información sobre cómo repetir datos contextuales](../../personalization/iterate-contextual-data.md)
   * Cree **plantillas de contenido** y **fragmentos** reutilizables para mantener la coherencia de la marca. [Trabajar con plantillas](../../content-management/content-templates.md)
   * Administre recursos con la integración de **Adobe Experience Manager Assets**. [Más información sobre los recursos](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **Agregar ofertas y tomar decisiones**. Ofrezca la mejor oferta a cada cliente en el momento adecuado mediante el uso de decisiones con tecnología de IA. Obtenga información acerca de [Administración de decisiones](../../offers/get-started/starting-offer-decisioning.md) y [Experience Decisioning](../../experience-decisioning/gs-experience-decisioning.md).

   ![](../assets/offers-e2e-offers-displayed.png)

1. **Prueba y validación**. Previsualizar y probar contenido antes de enviar:
   * Use **perfiles de prueba** para obtener una vista previa de la personalización y comprobar el procesamiento en todos los dispositivos
   * Realizar prueba con **datos de ejemplo** de archivos CSV/JSON
   * Vista previa de **procesamiento de correo electrónico** en clientes de correo electrónico populares
   * Configurar **flujos de trabajo de aprobación** para campañas y recorridos (requiere licencia adicional)

   Aprenda a [probar y validar mensajes](../../content-management/preview-test.md).

1. **Generar recorridos de cliente**. Cree experiencias personalizadas en tiempo real mediante el lienzo de recorrido:

   * Déclencheur recorridos con **eventos** (acciones del cliente) o **audiencias** (envíos por lotes)
   * Agregue **condiciones** para crear rutas personalizadas basadas en datos de clientes
   * Use **actividades de espera** para crear un tiempo perfecto entre los mensajes
   * Enviar mensajes a través de **varios canales** dentro de un recorrido
   * Aplicar **pruebas A/B** para optimizar la efectividad del recorrido
   * Use **búsqueda de conjuntos de datos** para enriquecer recorridos con datos en tiempo real de Adobe Experience Platform. [Más información sobre la búsqueda de conjuntos de datos](../../building-journeys/dataset-lookup.md)
   * Aproveche **identificadores suplementarios** para permitir que el mismo perfil introduzca varias instancias de recorrido (por ejemplo, pedidos o reservas diferentes). [Más información sobre los identificadores suplementarios](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   Aprenda a [diseñar y ejecutar recorridos](../../building-journeys/journey-gs.md) y a explorar [casos de uso de recorridos](../../building-journeys/jo-use-cases.md). Comprenda [los criterios de entrada y salida](../../building-journeys/entry-exit-criteria-guide.md) para controlar el flujo del perfil.

1. **Supervisar y optimizar**. Rastree el rendimiento y mejore los resultados con el tiempo:
   * Supervise el rendimiento de **live recorrido** e identifique cuellos de botella
   * Analizar **tasas y métricas de participación en la entrega de mensajes**
   * Usar **tableros de informes** con la integración de Customer Journey Analytics
   * Rastrear **conversión** e impacto en la empresa

   Aprenda a [supervisar el rendimiento](../../reports/report-gs-cja.md).

## Aproveche las últimas funciones

Journey Optimizer evoluciona continuamente con nuevas funciones para mejorar su eficacia de marketing:

* **Tarjetas de contenido**: Envíe mensajes persistentes y no intrusivos dentro de aplicaciones móviles y sitios web con los que los usuarios puedan interactuar según les convenga. A diferencia de las notificaciones push, las tarjetas de contenido permanecen visibles hasta que se descartan. [Más información sobre las tarjetas de contenido](../../content-card/create-content-card.md)

* **Administración de conflictos y priorización**: controle la frecuencia de los mensajes y evite la comunicación excesiva con reglas de límite avanzadas. Establezca puntuaciones de prioridad para garantizar que los mensajes más importantes lleguen primero a los clientes. [Más información acerca de la administración de conflictos](../../conflict-prioritization/gs-conflict-prioritization.md)

* **Optimización del tiempo de envío con tecnología de IA**: permita que AI prediga el tiempo de envío óptimo para cada cliente en función de sus patrones de participación históricos, lo que aumenta las tasas de apertura y clics hasta en un 10 %. [Más información acerca de la optimización del tiempo de envío](../../building-journeys/send-time-optimization.md)

* **Experimento multi-armed bandit**: Asigne automáticamente más tráfico a las variaciones ganadoras en tiempo real mientras realiza pruebas, maximizando los resultados sin esperar a que finalicen las pruebas. [Más información sobre experimentación](../../content-management/content-experiment.md)

* **Flujos de trabajo de aprobación**: Implemente procesos de revisión para campañas y recorridos antes de que se activen (disponibles con licencia adicional). [Más información sobre las aprobaciones](../../test-approve/gs-approval.md)

## Prácticas recomendadas para el éxito

### Creación de contenido

* **Comenzar con plantillas**: use plantillas prediseñadas y fragmentos de contenido para acelerar la creación y mantener la coherencia
* **Realice pruebas tempranas y vuelva a probarlas con frecuencia**: Obtenga siempre una vista previa del contenido en todos los dispositivos y utilice perfiles de prueba para validar la personalización
* **Aproveche bien la IA**: use el Asistente para IA para los borradores y las variaciones iniciales, pero siempre revise y perfeccione la voz de su marca
* **Manténgalo simple**: Los mensajes claros y concisos con llamadas a la acción potentes funcionan mejor que los diseños complejos

### diseño de recorrido

* **Definir metas claras**: defina métricas de éxito antes de generar su recorrido
* **Asignar la experiencia del cliente**: Visualice todo el recorrido antes de la implementación
* **Usar las actividades de espera estratégicamente**: dé a los clientes tiempo para interactuar antes de enviar los seguimientos
* **Planear estrategias de salida**: defina cuándo y por qué los clientes deben salir del recorrido
* **Probar en modo borrador**: valide la lógica de recorrido con la ejecución en seco antes de activarla

[Conozca las prácticas recomendadas de recorrido](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### Segmentación de audiencia

* **Segmente cuidadosamente**: cree segmentos de audiencia específicos y procesables basados en criterios claros
* **Actualizar con regularidad**: Asegúrese de que las audiencias estén actualizadas configurando las programaciones de evaluación adecuadas
* **Tamaño y precisión del equilibrio**: las audiencias de destino son lo suficientemente grandes para la relevancia estadística pero lo suficientemente específicas para la relevancia
* **Use atributos de enriquecimiento**: aproveche los atributos calculados y los datos de enriquecimiento para una personalización más profunda

### Administración de frecuencia

* **Respetar las preferencias del cliente**: Respetar las exclusiones y las preferencias de comunicación
* **Definir límites de frecuencia**: utilice conjuntos de reglas para evitar la fatiga de los mensajes entre canales
* **Coordinar campañas**: use la administración de conflictos para asegurarse de que los clientes reciban el mensaje correcto en el momento adecuado
* **Supervisar la participación**: observe si hay signos de fatiga (disminución de las tasas de apertura, aumento de las cancelaciones de suscripción)

[Obtenga información sobre la restricción de frecuencia](../../conflict-prioritization/channel-capping.md)

## Exploración de casos de uso

Aprenda de los ejemplos prácticos que muestran las funcionalidades de Journey Optimizer:

**Casos de uso populares:**

* **Serie de bienvenida**: Incorpore nuevos clientes con recorridos personalizados de varios pasos. [Ver caso de uso](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **Recuperación del carro de compras abandonado**: Vuelva a atraer a los clientes que dejaron artículos en el carro de compras. [Ver caso de uso](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **Campañas de renovación de participación**: Recupere clientes inactivos con ofertas segmentadas. [Ver caso de uso](https://experienceleague.adobe.com/es/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)
* **Campañas de cumpleaños**: envía mensajes de cumpleaños personalizados con ofertas especiales
* **Recomendaciones de productos**: sugiere productos relevantes según el historial de compra y navegación
* **Mensajería impulsada por eventos**: Responder a las acciones de los clientes en tiempo real

**patrones de Recorrido:**

* [Enviar mensajes a los suscriptores](../../building-journeys/message-to-subscribers-uc.md): Listas de suscripción de Target con contenido personalizado
* [Mensajería multicanal](../../building-journeys/journeys-uc.md): Combine correo electrónico y push con eventos de reacción
* [Correos electrónicos solo de día laborable](../../building-journeys/weekday-email-uc.md): programe comunicaciones con condiciones basadas en el tiempo

Examine la [biblioteca de casos de uso de recorrido](../../building-journeys/jo-use-cases.md) para ver más patrones e implementaciones.

## Colaborar con otras funciones

Su trabajo de marketing se conecta con otros equipos:

* **Trabajar con [ingenieros de datos](data-engineer.md)**: solicite nuevos atributos calculados, proporcione comentarios sobre la calidad de la audiencia y coordine los requisitos de datos
* **Trabaje con [Desarrolladores](developer.md)**: Alinee en los déclencheur de eventos, pruebe implementaciones móviles y valide el seguimiento
* **Trabaje con [administradores](administrator.md)**: solicite configuraciones de canal, informe de problemas con permisos y coordine la habilitación de nuevas características

## Manténgase al día

Manténgase al tanto de las últimas funciones y características de marketing de Journey Optimizer:

* **[Notas de la versión](../../rn/release-notes.md)**: revise las nuevas características, las actualizaciones de canal y las mejoras publicadas cada mes
* **[Actualizaciones de documentación](../../rn/documentation-updates.md)**: efectúe el seguimiento de cambios recientes, incluidos nuevos casos de uso, prácticas recomendadas y documentación de características
* **Notificaciones de productos**: habilita las notificaciones en tu [perfil de Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} para recibir alertas sobre:
   * Nuevos canales y funcionalidades disponibles para usted
   * Próximos lanzamientos de funcionalidades y programas beta
   * Prácticas recomendadas y oportunidades de formación
   * Anuncios importantes que afectan a las campañas

  Para habilitar las notificaciones, haz clic en tu icono de perfil en la parte superior derecha de Adobe Experience Cloud, ve a **Preferencias > Notificaciones** y configura tus preferencias de notificaciones de Journey Optimizer.

## Próximos pasos

1. **Empiece pequeño**: cree un recorrido de bienvenida simple o una campaña de un solo mensaje para conocer la plataforma
2. **Aproveche la IA**: use el Asistente para IA para hacer preguntas y acelerar la creación de contenido
3. **Únase a la comunidad**: Conéctese con otros usuarios de Journey Optimizer en la [Comunidad de Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
4. **Explorar tutoriales**: Mira vídeos paso a paso en [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=es){target="_blank"}
