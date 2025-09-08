---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las campañas
description: Obtenga más información sobre las campañas en Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: campaña, cómo, inicio, optimizador
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 99%

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
>title="Control de tasa"
>abstract="Defina el Control de tasa para su campaña especificando los límites de tasa deseados. Esta función es especialmente útil para evitar sobrecargas en sistemas descendentes, como páginas de aterrizaje o plataformas de servicio de atención al cliente."

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
>abstract="**Las campañas programadas** se ejecutan inmediatamente o en una fecha especificada y están pensadas para enviar mensajes de tipo marketing. Las campañas **activadas por API** se ejecutan mediante el uso de una llamada de API. Están destinadas a enviar mensajes de marketing (mensajes promocionales que requieren el consentimiento del usuario) o mensajes transaccionales (mensajes no comerciales, que también se pueden enviar a perfiles no suscritos en contextos específicos)."

Utilice las campañas de Journey Optimizer para ofrecer contenido único a un público específico mediante varios canales. Cuando se utilizan recorridos, las acciones se ejecutan en secuencia. Con las campañas, las acciones se realizan simultáneamente, ya sea de forma inmediata o en función de una programación especificada.

![](assets/gs-campaigns.png)

Puede crear diferentes tipos de campañas en Journey Optimizer:

* **Campañas de acción**

  Las campañas de acción (o campañas programadas) permiten comunicaciones por lotes ad-hoc sencillas para casos de uso de marketing, como ofertas promocionales, campañas de participación, anuncios, avisos legales o actualizaciones de políticas.

* **Campañas activadas mediante API**

  Las campañas activadas por API permiten que las comunicaciones de marketing lleguen a un público en el momento adecuado o que los mensajes transaccionales/operativos lleguen a una persona, como un restablecimiento de contraseña. Este acto puede implicar una personalización no solo mediante el uso del atributo de perfil, sino también mediante los datos de contexto en tiempo real en el activador, que es una carga útil de API de REST.

* **Campañas orquestadas**

  La orquestación de campañas en Adobe Journey Optimizer impulsa campañas de marketing sofisticadas iniciadas por la marca en todos los canales, lo que le ayuda a fomentar la participación, los ingresos y la lealtad de los clientes a escala.

  Aunque el marketing de múltiples canales es esencial, las campañas orquestadas lo hacen fluido. Con una interfaz visual de arrastrar y soltar, puede diseñar y automatizar flujos de trabajo de marketing complejos, desde la segmentación hasta el envío de mensajes, en varios canales. Todo sucede en un entorno intuitivo, creado para ofrecer velocidad, control y eficacia.

## Requisitos previos {#prerequisites}

Antes de crear la campaña, asegúrese de haber revisado los requisitos previos a continuación.

### Permisos

Las campañas solo están disponibles para los usuarios con los permisos adecuados que se enumeran a continuación. [Más información sobre las funciones integradas de Journey Optimizer](../administration/ootb-product-profiles.md)

>[!BEGINTABS]

>[!TAB Campañas de acción]

Administrador de campañas
Aprobador de campaña
Gestor de campañas
Visualizador de campañas

>[!TAB Campañas activadas mediante API]

Administrador de campañas
Aprobador de campaña
Gestor de campañas
Visualizador de campañas

>[!TAB Campañas orquestadas]

Administrador de campañas orquestadas
Aprobador de campañas orquestadas
Gestor de campañas orquestadas
Visor de campañas orquestadas

>[!ENDTABS]

Si no puede acceder a las funcionalidades de la campaña, póngase en contacto con el administrador para solicitar los permisos necesarios.

+++Obtenga información sobre cómo asignar una función relacionada con la campaña

1. Para asignar una función a un usuario en el producto [!DNL Permissions], vaya a la pestaña **[!UICONTROL Funciones]** y seleccione una de las **[!UICONTROL Funciones]** integradas relacionadas con las campañas anteriores.

1. En la pestaña **[!UICONTROL Usuarios]**, haga clic en **[!UICONTROL Añadir usuario]**.

1. Introduzca el nombre o la dirección de correo electrónico del usuario o selecciónelo de la lista y haga clic en **[!UICONTROL Guardar]**.

   Si el usuario no se ha creado previamente, consulte la [documentación de Añadir usuarios](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/ui/users).

El usuario debería recibir entonces un correo electrónico que le redirija a su instancia.

+++

### Público

Los públicos deben estar disponibles antes de crear la campaña. [Introducción a los públicos](../audience/about-audiences.md).

### Configuración de canal

Para poder seleccionar un canal, debe tener la configuración del canal correspondiente (es decir, preestablecida) creada y disponible. [Aprenda a configurar canales](../configuration/channel-surfaces.md).

## Vamos a profundizar

Ahora que comprende las campañas de [!DNL Journey Optimizer], es hora de profundizar en estas secciones de documentación para empezar a crear sus primeras campañas.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campañas de acción" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campañas de acción</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campañas activadas por API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campañas orquestadas</a></td>
</tr></table>
