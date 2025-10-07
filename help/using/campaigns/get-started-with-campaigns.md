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
source-git-commit: 801b90201c3ffcbfb7b038abac2bf99209a14c7a
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 60%

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
>abstract="Seleccione el tipo de campaña. Los canales disponibles varían según el tipo seleccionado. <br>**Campañas programadas** (campañas de acción): ideal para comunicaciones por lotes simples y puntuales que se pueden programar para que se ejecuten a una hora específica.<br>**Campañas activadas por API**: se activan mediante una llamada de API, lo que permite la mensajería automatizada basada en eventos directamente desde sistemas externos.<br>**Campañas orquestadas**: proporcione un lienzo visual de arrastrar y soltar para diseñar y automatizar flujos de trabajo de marketing complejos y de varios pasos, desde la segmentación de públicos hasta el envío personalizado de mensajes en todos los canales."

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

Utilice [!DNL Journey Optimizer] campañas para entregar contenido de una sola vez a una audiencia específica en varios canales. A diferencia de los recorridos, que ejecutan acciones paso a paso, las campañas realizan acciones simultáneamente, ya sea de forma inmediata o en una programación definida.

![](assets/gs-campaigns.png)

## Tipos de campaña

[!DNL Journey Optimizer] admite tres tipos de campaña. Cada tipo se adapta a diferentes casos de uso y admite diferentes canales.

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Campañas orquestadas]

**Campañas orquestadas** potencia campañas de marketing sofisticadas e iniciadas por la marca en todos los canales, lo que te ayuda a aumentar la participación, los ingresos y la lealtad de los clientes a escala.

Aunque el marketing de múltiples canales es esencial, las campañas orquestadas lo hacen fluido. Con una interfaz visual de arrastrar y soltar, puede diseñar y automatizar flujos de trabajo de marketing complejos, desde la segmentación hasta el envío de mensajes, en varios canales. Todo sucede en un entorno intuitivo, creado para ofrecer velocidad, control y eficacia.

➡️ [Aprenda a trabajar con campañas organizadas](../orchestrated/gs-orchestrated-campaigns.md).

>[!TAB Campañas de acción (o Campañas programadas)]

**Campañas de acción**, también conocidas como Campañas programadas, permiten comunicaciones por lotes simples y específicas.

* **Programado - Marketing** - Para casos de uso de marketing como ofertas promocionales, campañas de participación, anuncios, avisos legales o actualizaciones de directivas. Requiere que los destinatarios se incluyan.
* **Programadas - Transaccionales**: a diferencia de las campañas de marketing, las campañas transaccionales no requieren que se incluyan los destinatarios. Utilice esta categoría para comunicaciones relacionadas con interrupciones, emergencias y cancelaciones. Canales admitidos: correo electrónico, SMS, notificación push.

➡️ [Aprenda a trabajar con campañas de acción](create-campaign.md)

>[!TAB Campañas activadas mediante API]

**Las campañas activadas por API** le permiten almacenar en déclencheur la ejecución de la campaña mediante una llamada de API. Estas comunicaciones se pueden enviar donde la necesidad pueda implicar una personalización no solo mediante un atributo de perfil de restablecimiento de contraseña, sino también mediante los datos de contexto en tiempo real en la déclencheur, que es una carga útil de API de REST.

* **API activada - Marketing** - Envíe comunicaciones de marketing personalizadas a audiencias de destino.
* **API activada - Transaccional** - Enviar mensajes después de una acción realizada por un individuo, como una solicitud de restablecimiento de contraseña, la compra del carro de compras, etc.

➡️ [Aprenda a trabajar con campañas activadas por API](api-triggered-campaigns.md)


>[!ENDTABS]

## Canales admitidos por tipo de campaña {#channels}

La siguiente tabla muestra la disponibilidad de cada canal en diferentes tipos de campaña, indicando dónde se admiten.

| Canal | Acción (Marketing) | Acción (transaccional) | Activado por API (Marketing) | Activado por API (transaccional) | Orquestado |
|----------------------|---------------------|-------------------------|----------------------------|--------------------------------|--------------|
| Correo electrónico | ✅ | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ | ✅ |
| Notificación push | ✅ | ✅ | ✅ | ✅ | ✅ |
| En la aplicación | ✅ | — | — | — | — |
| Correo directo | ✅ | — | — | — | — |
| Web | ✅ | — | — | — | — |
| Exp. basada en código | ✅ | — | — | — | — |
| Tarjetas de contenido | ✅ | — | — | — | — |
| WhatsApp | ✅ | — | — | — | — |
| Línea | ✅ | — | — | — | — |

## Requisitos previos {#prerequisites}

Antes de trabajar con campañas, asegúrese de haber revisado los requisitos previos siguientes.

* Las audiencias de **Audiences** deben estar disponibles antes de crear la campaña. [Introducción a los públicos](../audience/about-audiences.md).

* **Configuraciones de canal**: para poder seleccionar un canal, debe tener la configuración de canal correspondiente (es decir, un ajuste preestablecido) creada y disponible. [Aprenda a configurar canales](../configuration/channel-surfaces.md).

* **Permisos**: las campañas solo están disponibles para los usuarios con los permisos apropiados que se enumeran a continuación. Si no puede acceder a las funcionalidades de la campaña, póngase en contacto con el administrador para solicitar los permisos necesarios. [Más información sobre las funciones integradas de Journey Optimizer](../administration/ootb-product-profiles.md)

  | Tipo de campaña | Permisos |
  |----------------------------|----------------------------------------------------------------------------|
  | **Campañas de acción** | Administrador de campaña<br>Aprobador de campaña<br>Administrador de campaña<br>Visor de campaña |
  | **Campañas activadas mediante API** | Administrador de campaña<br>Aprobador de campaña<br>Administrador de campaña<br>Visor de campaña |
  | **Campañas orquestadas** | Administrador de campañas orquestadas<br>Aprobador de campañas orquestadas<br>Administrador de campañas orquestadas<br>Visor de campañas orquestadas |

  +++Más información sobre cómo asignar una función relacionada con la campaña

   1. Para asignar una función a un usuario en el producto [!DNL Permissions], vaya a la pestaña **[!UICONTROL Funciones]** y seleccione una de las **[!UICONTROL Funciones]** integradas relacionadas con las campañas anteriores.

   1. En la pestaña **[!UICONTROL Usuarios]**, haga clic en **[!UICONTROL Añadir usuario]**.

   1. Introduzca el nombre o la dirección de correo electrónico del usuario o selecciónelo de la lista y haga clic en **[!UICONTROL Guardar]**.

      Si el usuario no se ha creado previamente, consulte la [documentación de Añadir usuarios](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/ui/users).

  El usuario debería recibir entonces un correo electrónico que le redirija a su instancia.

  +++

## Vamos a profundizar

Ahora que comprende las campañas de [!DNL Journey Optimizer], es hora de profundizar en estas secciones de documentación para empezar a crear sus primeras campañas.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campañas de acción" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campañas de acción</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campañas activadas por API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campañas orquestadas</a></td>
</tr></table>
