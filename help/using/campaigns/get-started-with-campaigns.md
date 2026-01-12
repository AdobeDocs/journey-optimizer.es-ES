---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las campañas
description: Obtenga más información sobre las campañas en Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: campaña, cómo, inicio, optimizador
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: fec72c63d41a41adce5107082c50a68a7b8c0af2
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 31%

---

# Introducción a las campañas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Programación de campañas"
>abstract="De forma predeterminada, las campañas se inician tras la activación manual y finalizan inmediatamente después de enviar el mensaje una vez. Sin embargo, tiene la flexibilidad de establecer una fecha y hora específicas para que se envíe el mensaje. Además, puede especificar una fecha de finalización para campañas de acción recurrentes. En los Activadores de acción, también puede configurar la frecuencia de envío de mensajes para adaptarla a sus preferencias."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Inicio de campaña"
>abstract="Especifique la fecha y la hora a las que se debe enviar el mensaje."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fin de campaña"
>abstract="Especifique cuándo se debe detener la ejecución de una campaña recurrente."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Activadores de acciones de campaña"
>abstract="Defina una frecuencia a la que se debe enviar el mensaje de la campaña."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Control de velocidad"
>abstract="Defina el Control de velocidad para su campaña especificando los límites de velocidad deseados. Esta función es especialmente útil para evitar sobrecargas en sistemas descendentes, como páginas de aterrizaje o plataformas de servicio de atención al cliente."

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Creación de campañas"
>abstract="Utilice **Adobe Journey Optimizer** para ofrecer contenido único a un público específico mediante varios canales. Cuando se utilizan recorridos, las acciones se ejecutan en secuencia. Con las campañas, las acciones se realizan simultáneamente, ya sea de forma inmediata o en función de una programación especificada."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campañas"
>abstract="Cree campañas para ofrecer contenido de una sola vez a un público específico en varios canales. Antes de crear la campaña, asegúrese de que tiene una configuración de canal y un público de Adobe Experience Platform listos para usar."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campaña"
>abstract="Seleccione el tipo de campaña. Los canales disponibles varían según el tipo seleccionado. <br>**Campañas programadas** (campañas de acción): son ideales para comunicaciones por lotes simples y puntuales que se pueden programar para que se ejecuten a una hora específica.<br>**Campañas activadas por API**: se activan mediante una llamada API, lo que permite la mensajería automatizada basada en eventos directamente desde sistemas externos.<br>**Campañas orquestadas**: proporcionan un lienzo visual de arrastrar y soltar para diseñar y automatizar flujos de trabajo de marketing complejos y de varios pasos, desde la segmentación de públicos hasta el envío personalizado de mensajes en todos los canales."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="Campañas"
>abstract="Cree su flujo de segmentación, cree sus mensajes en canales múltiples y planifique sus campañas. Canales admitidos: correo electrónico, SMS, notificación push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="Campañas"
>abstract="Haga envíos salientes únicos o recurrentes, o acciones entrantes en curso."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="Campañas"
>abstract="Ofrezca acciones transaccionales salientes únicas o recurrentes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="Campañas"
>abstract="Ofrezca comunicaciones de marketing personalizadas a los públicos segmentados. Canales compatibles: correo electrónico, SMS, notificaciones push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="Campañas"
>abstract="Envíe comunicaciones transaccionales a perfiles individuales o conjuntos de perfiles. Canales compatibles: correo electrónico, SMS, notificaciones push."

Adobe Journey Optimizer le permite enviar contenido único y con objetivo a audiencias específicas a través de varios canales. Con las campañas, puede ejecutar acciones de marketing coordinadas simultáneamente, llegando a su audiencia con el mensaje correcto y en el momento adecuado.

Esta guía proporciona una hoja de ruta clara para ayudarle a comprender los aspectos básicos de la campaña, elegir el tipo de campaña adecuado para su caso de uso y diseñar campañas con confianza que ofrezcan experiencias de cliente impactantes.

## ¿Qué son las campañas?

**Campañas** son acciones de marketing coordinadas que envían contenido a una audiencia específica a través de uno o más canales. A diferencia de los recorridos en los que las acciones se ejecutan secuencialmente, las campañas realizan acciones simultáneamente, ya sea de forma inmediata o en una programación definida.

Utilice [!DNL Journey Optimizer] campañas para lo siguiente:

* Enviar **contenido único o recurrente** a los segmentos de audiencia de destino
* Ejecute **comunicaciones multicanal coordinadas** por correo electrónico, push, SMS, en la aplicación, web y mucho más
* Déclencheur **respuestas automatizadas** a través de llamadas API para mensajes en tiempo real impulsados por eventos
* Diseñar **flujos de trabajo de marketing complejos** con herramientas de orquestación visual

![](assets/gs-campaigns.png)

➡️ **¿Listo para empezar a crear?** [Cree su primera campaña](create-campaign.md) en minutos.

## Elija su tipo de campaña {#campaign-types}

**Antes de empezar a crear**, es importante que entienda qué tipo de campaña se ajusta a su caso de uso. Adobe Journey Optimizer admite tres tipos de campañas, cada una diseñada para diferentes escenarios y mecanismos de activación:

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Campañas orquestadas]

**Cuándo usar:** Flujos de trabajo de marketing complejos en varios pasos

**Las campañas orquestadas** proporcionan un lienzo visual de arrastrar y soltar para diseñar y automatizar flujos de trabajo de marketing sofisticados. Desde la segmentación de audiencia hasta la entrega de mensajes personalizados en todos los canales, todo sucede en un entorno intuitivo creado para la velocidad y el control.

**Perfecto para:** programas de participación de clientes en varios pasos, estrategias complejas de segmentación y direccionamiento, orquestación de campañas en canales múltiples, marketing a escala iniciado por la marca y automatización avanzada del flujo de trabajo con varios puntos de decisión.

➡️ [Más información sobre las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md)

>[!TAB Campañas de acción (programadas)]

**Cuándo usar:** comunicaciones por lotes simples y programadas

**Las campañas de acción** (también conocidas como Campañas programadas) son ideales para comunicaciones por lotes directas, únicas o recurrentes que se ejecutan a una hora específica.

**Dos categorías:**

* **Marketing**: ofertas promocionales, campañas de participación, anuncios, avisos legales o actualizaciones de directivas. Requiere que los destinatarios hayan dado su consentimiento.
* **Transaccional**: interrupciones, emergencias y cancelaciones. No requiere la inclusión.

**Perfecto para:** boletines mensuales para segmentos de clientes, anuncios promocionales con plazos específicos, campañas de marketing de temporada, comunicaciones de lanzamiento de productos y notificaciones de interrupción del servicio.

➡️ [Más información sobre las campañas de acción](create-campaign.md)

>[!TAB Campañas activadas mediante API]

**Cuándo usar:** Mensajería en tiempo real basada en eventos con sistemas externos

**Las campañas activadas por API** se activan mediante llamadas a la API, lo que permite la mensajería automatizada directamente desde sistemas externos. Estas campañas admiten la personalización mediante atributos de perfil y datos de contexto en tiempo real desde la carga útil de la API.

**Dos categorías:**

* **Marketing**: comunicaciones de marketing personalizadas para audiencias de destino
* **Transaccional**: mensajes después de acciones individuales (restablecimientos de contraseña, compras en el carro de compras, etc.)

**Perfecto para:** confirmaciones de restablecimiento de contraseña, recuperación de abandono del carro de compras, confirmaciones de pedidos y actualizaciones de envío, notificaciones de actividad de la cuenta y recomendaciones personalizadas en tiempo real.

➡️ [Más información acerca de campañas activadas por API](api-triggered-campaigns.md)

>[!ENDTABS]

>[!NOTE]
>
>¿No está seguro de qué tipo elegir? Comience con **campañas de acción** para comunicaciones por lotes programadas o **campañas activadas por API** para mensajería en tiempo real, que cubren los casos de uso más comunes.

## Requisitos previos {#prerequisites}

Antes de trabajar con campañas, asegúrese de que dispone de lo siguiente:

* **Audiencias**: las audiencias deben estar disponibles en Adobe Experience Platform antes de crear campañas. [Introducción a las audiencias →](../audience/about-audiences.md)

* **Configuraciones de canal**: las configuraciones de canal (ajustes preestablecidos) deben crearse y estar disponibles para los canales que desee utilizar. [Configurar configuraciones de canal →](../configuration/channel-surfaces.md)

* **Permisos**: necesita los permisos adecuados según el tipo de campaña. Póngase en contacto con el administrador si no puede acceder a las funcionalidades de la campaña. [Más información acerca de los roles integrados →](../administration/ootb-product-profiles.md)

  +++Lista de permisos de campañas

  | Tipo de campaña | Permisos |
  |-------------|---------------|
  | **Campañas de acción** y **Campañas activadas por API** | Administrador de campañas<br>Aprobador de campaña<br>Gestor de campañas<br>Visor de campañas |
  | **Campañas orquestadas** | Administrador de campañas orquestadas<br>Aprobador de campañas orquestadas<br>Gestor de campañas orquestadas<br>Visor de campañas orquestadas |

  +++

  +++Asignación de permisos de campaña

   1. Vaya a la ficha **[!UICONTROL Roles]** en el producto [!DNL Permissions] y seleccione uno de los **[!UICONTROL roles]** relacionados con la campaña integrada.

   1. En la pestaña **[!UICONTROL Usuarios]**, haga clic en **[!UICONTROL Añadir usuario]**.

   1. Introduzca el nombre o la dirección de correo electrónico del usuario o seleccione el usuario en la lista y haga clic en **[!UICONTROL Guardar]**.

  Si el usuario no se ha creado previamente, consulte la [documentación de Añadir usuarios](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/ui/users){target="_blank"}.

  El usuario debería recibir entonces un correo electrónico que le redirija a su instancia.

  +++

## Flujo de trabajo de creación de campañas {#workflow}

La creación de campañas exitosas sigue un proceso claro y repetible. Este es su flujo de trabajo paso a paso:

+++&#x200B;1. Planifique su campaña

Antes de empezar, aclare sus objetivos:

* **¿Cuál es el objetivo?** (por ejemplo, dirigir conversiones, aumentar la participación, notificar a los clientes)
* **¿Quién es la audiencia?** (por ejemplo, crear o seleccionar de Adobe Experience Platform)
* **¿Qué tipo de campaña encaja?** (ver [tipos de campaña](#campaign-types) más arriba)
* **¿Qué canales usará?** (correo electrónico, push, SMS, en la aplicación, web, etc.) → [Ver canales admitidos por tipo de campaña](../channels/gs-channels.md#channels)
* **¿Cuándo se debe ejecutar?** (inmediato, programado o activado por API)

+++

+++&#x200B;2. Configurar las propiedades de la campaña

Configure las bases de la campaña:

1. **Nombre y describa** su campaña para facilitar su identificación
2. **Seleccionar tipo de campaña** (activada por acción, activada por API u orquestada)
3. **Elija su audiencia**
4. **Establecer prioridad** si se usa la administración de conflictos
5. **Configurar programación** (para campañas de acción) o detalles de API (para activadas por API)

**Guías específicas del tipo:** [Propiedades de la campaña de acción](campaign-properties.md) | [Propiedades de campaña activadas por API](api-triggered-campaign-properties.md) | [Configuración de campaña orquestada](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;3. Diseñar el contenido

Cree mensajes atractivos para su audiencia:

* Usar **Email Designer** para experiencias de correo electrónico enriquecidas
* Configurar **notificaciones push** con imágenes y vínculos profundos
* Diseñar **mensajes SMS/MMS** con personalización
* Crear experiencias **en la aplicación** y **web**
* Agregar **personalización** mediante atributos de perfil y datos contextuales

**Guías específicas del tipo:** [Contenido de la campaña de acción](campaign-content.md) | [Contenido de campaña activado por API](api-triggered-campaign-content.md) | [Contenido de campaña orquestado](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;4. Revisión y prueba

Revise siempre la campaña antes de la activación:

* **Previsualizar contenido** con perfiles de prueba
* **Compruebe el direccionamiento** para garantizar la audiencia correcta
* **Verificar la programación** y la configuración de activación
* **Solicitar aprobación** si se usa el flujo de trabajo de aprobación
* **Capacidad de entrega de pruebas** con listas semilla

**Guías específicas del tipo:** [Revisar campañas de acción](review-activate-campaign.md) | [Revisar campañas activadas por API](review-activate-api-triggered-campaign.md) | [Revisar campañas orquestadas](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;5. Active la campaña

Una vez completada la revisión, active la campaña:

* **Activación manual** - Activar inmediatamente o a la hora programada
* **Activación de API**: para campañas activadas por API, use el punto de conexión de activación
* **Proceso de aprobación**: si es necesario, espere a que se apruebe la parte interesada

Nota: Las campañas activas no se pueden editar (debe duplicar para realizar cambios)

**Guías específicas del tipo:** [Activar campañas de acción](review-activate-campaign.md) | [Activar campañas activadas por API](review-activate-api-triggered-campaign.md) | [Activar campañas orquestadas](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;6. Monitorización y análisis

Realice un seguimiento del rendimiento de la campaña:

* Ver informes y análisis de campaña
* Monitorización de tasas de entrega y métricas de participación
* Seguimiento de errores y devoluciones
* Analizar la conversión y el ROI
* Uso de perspectivas para la optimización

**Guías específicas del tipo:** [Informes de campañas de acción](../reports/campaign-global-report-cja.md) | [Supervisión de campaña activada por API](api-triggered-campaigns.md#monitor) | [Análisis de campañas orquestadas](../orchestrated/create-orchestrated-campaign.md)

+++

## Vamos a profundizar {#get-started-types}

Ahora que comprende las campañas de [!DNL Journey Optimizer], elija el tipo de campaña para comenzar:

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campañas de acción" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campañas de acción</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campañas activadas por API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campañas orquestadas</a></td>
</tr></table>

A medida que se sienta más cómodo con las campañas, explore estas potentes funcionalidades:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=es)

**Programación y sincronización**

Programe campañas para fechas/horas específicas, establezca envíos recurrentes y optimice los tiempos de envío para lograr el máximo impacto. (Campañas activadas por acciones y API)

[Más información sobre la programación](campaign-schedule.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=es)

**Control de tarifa**

Limite el rendimiento de los mensajes para evitar sobrecargas en sistemas descendentes como páginas de aterrizaje o plataformas de atención al cliente. (Campañas activadas por acciones y API)

[Límites de tasa de control](create-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=es)

**Segmentación de audiencia**

Dirija audiencias de Adobe Experience Platform específicas con precisión y administre cualificaciones de audiencia de forma dinámica.

[Seleccionar audiencia de campaña](campaign-audience.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=es)

**Flujos de trabajo de aprobación**

Implemente procesos de revisión y aprobación antes de que las campañas se publiquen, lo que garantiza la calidad y el cumplimiento. (Campañas activadas por acciones y API)

[Revisar y activar](review-activate-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=es)

**Horas tranquilas**

Respete las preferencias del cliente evitando la entrega de mensajes durante los períodos de tiempo especificados. (Campañas activadas por acciones y API)

[Configurar horas de silencio](quiet-hours.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=es)

**Optimización**

Utilice reglas de segmentación y experimentos de contenido para ofrecer contenido personalizado y maximizar la participación.

[Optimizar campañas](gs-message-optimization.md)
:::

::::
