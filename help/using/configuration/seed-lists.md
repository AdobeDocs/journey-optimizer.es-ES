---
solution: Journey Optimizer
product: journey optimizer
title: Listas semilla
description: Aprenda a utilizar las listas semilla en Journey Optimizer
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
keywords: lista de semillas, lista de semillas, semillas, configuración
source-git-commit: 89d2eb94a600af437862aa2ded74d77179a5c3e8
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 8%

---

# Uso de listas semilla {#seed-lists}

Listas semilla en [!DNL Journey Optimizer] permiten incluir automáticamente direcciones semilla específicas en las entregas.

>[!CAUTION]
>
>Actualmente, esta función solo se aplica al canal de correo electrónico.

Las direcciones semilla se utilizan para dirigirse a los destinatarios que no coinciden con los criterios de destino definidos. De este modo, los destinatarios que estén fuera del alcance de la entrega pueden recibirlo como lo haría cualquier otro destinatario.

Las direcciones semilla no son perfiles reales ni perfiles de prueba, ya que no incluyen detalles de perfil. Solo son destinatarios que pertenecen a partes interesadas internas almacenadas en el sistema. Cuando se seleccionan en una campaña o recorrido específico, se incluyen en el momento de la ejecución de la entrega, lo que significa que recibirán una copia de la entrega con fines de garantía.

* Al recibir las entregas al mismo tiempo y en las mismas condiciones que sus clientes, las listas semilla permiten monitorizar las copias de los correos electrónicos enviadas para garantizar que todos los formatos de visualización, imágenes y vínculos sean correctos, así como realizar un seguimiento de los mensajes reales enviados a sus destinatarios.

  Por ejemplo:

+++ Si es administrador de marketing:

  Desea que todos los integrantes del equipo reciban copias de los mensajes enviados al mismo tiempo que los clientes. De este modo, su equipo puede asegurarse de que los mensajes se envíen con el diseño esperado, las direcciones URL activas, el texto correcto y las imágenes, todo ello según lo planificado antes de la ejecución.

+++

+++ Si es el propietario de un producto:

  Debe realizar un seguimiento de los mensajes reales enviados a los clientes. De hecho, es posible que su equipo y liderazgo estén interesados en algunas campañas y deban agregarse según sea necesario para recibir copias del mensaje en el momento de la entrega.

+++

* Otra razón para utilizar listas semilla es la protección de la lista de correo. La inclusión de direcciones semilla en la lista de la campaña de correo le permite recibir una notificación si la está utilizando un tercero, ya que las direcciones que contiene reciben las entregas enviadas a la misma.

## Acceso a las listas semilla {#access-seed-lists}

Para acceder a las listas semilla ya creadas, vaya a **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** y seleccione **[!UICONTROL Lista semilla]**.

>[!CAUTION]
>
>Los permisos para ver, exportar y administrar las listas semilla están restringidos a [Administradores de recorrido](../administration/ootb-product-profiles.md#journey-administrator). Más información sobre la administración de [!DNL Journey Optimizer] derechos de acceso de los usuarios en [esta sección](../administration/permissions-overview.md).

![](assets/seed-list-access.png)

Puede buscar listas semilla por nombre o filtrar por el usuario que ha creado la lista o en la fecha de creación. Una vez seleccionado, puede borrar el filtro mostrado en la parte superior de la lista.

![](assets/seed-list-filtering.png)

Utilice el **[!UICONTROL Eliminar]** para eliminar una entrada de forma permanente.

>[!CAUTION]
>
>No es posible eliminar una lista semilla que se utilice en un activo [campaña](../campaigns/review-activate-campaign.md) o [recorrido](../building-journeys/publishing-the-journey.md). Se debe desactivar la campaña o el recorrido, o editarlo para utilizar otra superficie que no tenga seleccionada la lista semilla. [Más información sobre el uso de una lista semilla](#use-seed-list)

Puede hacer clic en el nombre de una lista semilla para editarla. <!--Use the **[!UICONTROL Edit]** button to edit a seed list.-->

## Creación de una lista semilla {#create-seed-list}

>[!CONTEXTUALHELP]
>id="ajo_seed_list_details"
>title="Definición de una lista semilla"
>abstract="Utilice una lista semilla para añadir automáticamente direcciones internas específicas a la audiencia de envío con fines de garantía. Las listas semilla permiten supervisar las copias de los mensajes enviados para asegurarse de que todos los elementos de visualización son correctos y proteger la lista de correo. Actualmente, esta función solo se aplica al canal de correo electrónico."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html#use-seed-list" text="¿Qué son las listas semilla?"

>[!CONTEXTUALHELP]
>id="ajo_seed_addresses"
>title="Rellene la lista semilla"
>abstract="Seleccione las direcciones que se incluirán en el momento de la ejecución de la entrega y recibirán una copia exacta del mensaje. Puede importar un archivo CSV o introducir direcciones de correo electrónico manualmente."

Para crear una lista semilla, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Lista semilla]** menú.

1. Seleccione el **[!UICONTROL Creación de una lista semilla]** botón.

   ![](assets/seed-list-create-button.png)

1. Complete los detalles. Comience agregando un nombre.

   ![](assets/seed-list-details.png)

   >[!NOTE]
   >
   >Los nombres deben comenzar por una letra (A-Z) e incluir solo caracteres alfanuméricos o caracteres especiales ( _, ., -).

1. Seleccione el canal. Actualmente solo está disponible el canal de correo electrónico.

1. Seleccione un perfil de prueba. Dado que las direcciones semilla no incluyen detalles del perfil, este perfil de prueba solo se utilizará para mostrar los datos de personalización en el mensaje enviado a las direcciones semilla.

   >[!NOTE]
   >
   >Solo se puede seleccionar un perfil de prueba a la vez.

1. Añada las direcciones semilla a las que desee enviar las entregas. Puede importar un archivo CSV o introducir direcciones de correo electrónico manualmente.

   ![](assets/seed-list-email-addresses.png)

   >[!NOTE]
   >
   >Puede combinar ambas opciones, pero el número total de direcciones en una lista semilla no puede superar las 50.

1. Clic **[!UICONTROL Crear]** para confirmar. La lista semilla recién creada se muestra en la variable [Pantalla de lista semilla](#access-seed-lists).

## Uso de una lista semilla en una campaña o recorrido {#use-seed-list}

Ahora que la lista de reasignación se ha creado, puede utilizarla en cualquier campaña o recorrido para incluir las direcciones semilla correspondientes en las entregas. Para ello, siga los pasos que aparecen a continuación.

>[!CAUTION]
>
>Los mensajes enviados a las direcciones semilla no se incluyen en los informes.

1. Cree una superficie y seleccione la **[!UICONTROL Correo electrónico]** canal. [Más información](../email/email-settings.md)

1. Seleccione la lista semilla que desee en la [sección correspondiente](../email/email-settings.md#seed-list).

   >[!NOTE]
   >
   >Solo se puede seleccionar una lista semilla a la vez.

   ![](assets/seed-list-surface.png)

1. Envíe la superficie.

1. Crear un [campaña](../campaigns/create-campaign.md) o una [recorrido](../building-journeys/journey-gs.md).

1. Seleccione el **[!UICONTROL Correo electrónico]** y seleccione la opción [emerger](channel-surfaces.md) incluida la lista semilla que sea relevante para usted.

   ![](assets/seed-list-campaign-email.png)

1. Activar su [campaña](../campaigns/review-activate-campaign.md) o publique su [recorrido](../building-journeys/publishing-the-journey.md).

Ahora, cada vez que se envía un mensaje de correo electrónico a sus clientes a través de esa campaña o recorrido, las direcciones de correo electrónico de la lista semilla seleccionada también lo reciben en las mismas condiciones, al mismo tiempo y con el mismo contenido que los destinatarios objetivo.

>[!NOTE]
>
>En el caso de los recorridos, la entrega por correo electrónico se envía a las direcciones semilla solo en la primera ejecución del recorrido.

