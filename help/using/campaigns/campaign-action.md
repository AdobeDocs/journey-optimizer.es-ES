---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de la acción de campaña
description: Obtenga información sobre cómo configurar la acción de campaña.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: crear, optimizador, campaña, superficie, mensajes
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 10%

---


# Configuración de la acción de campaña {#action-campaign-action}

Use la ficha **[!UICONTROL Acciones]** para seleccionar una configuración de canal para el mensaje y establecer opciones adicionales como seguimiento, experimento de contenido o contenido multilingüe.

1. **Elige el canal**

   Vaya a la pestaña **[!UICONTROL Acciones]**, haga clic en el botón **[!UICONTROL Agregar acción]** y seleccione el canal de comunicación.

   ![](assets/create-campaign-add-action.png)

   >[!NOTE]
   >
   >Los canales disponibles varían en función del modelo de licencia y los complementos.

1. **Seleccionar una configuración de canal**

   Un [administrador del sistema](../start/path/administrator.md) define una configuración. Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Aprenda a configurar las configuraciones de canal](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **Crear un experimento de contenido**

   Utilice la sección **[!UICONTROL Experimento de contenido]** para definir varios tratamientos de envío y medir cuál ofrece el mejor rendimiento para la audiencia de destino. Haga clic en el botón **[!UICONTROL Crear experimento]** y siga los pasos detallados en esta sección: [Crear un experimento de contenido](../content-management/content-experiment.md).

1. **Agregar contenido multilingüe**

   Utilice la sección **[!UICONTROL Idiomas]** para crear contenido en varios idiomas dentro de la campaña. Para ello, haga clic en el botón **[!UICONTROL Agregar idiomas]** y seleccione la **[!UICONTROL configuración de idioma]** que desee. Encontrará información detallada sobre cómo configurar y utilizar las funciones multilingües en esta sección: [Introducción al contenido multilingüe](../content-management/multilingual-gs.md)

Hay disponibles ajustes adicionales en función del canal de comunicación seleccionado. Expanda las secciones siguientes para obtener más información.

+++**Aplicar reglas de límite** (correo electrónico, correo directo, push, SMS)

En la lista desplegable **[!UICONTROL Reglas de negocio]**, seleccione un conjunto de reglas para aplicar reglas de límite a su campaña. El uso de conjuntos de reglas de canal le permite establecer límites de frecuencia por tipo de comunicación para evitar sobrecargar a los clientes con mensajes similares. [Descubra cómo trabajar con conjuntos de reglas](../conflict-prioritization/rule-sets.md)

+++

+++**Rastrear participación** (correo electrónico, SMS).

Utilice la sección **[!UICONTROL Seguimiento de acciones]** para rastrear cómo reaccionan sus destinatarios a sus envíos de correo electrónico o SMS. Se puede acceder a los resultados de seguimiento desde el informe de campaña una vez que se ha ejecutado la campaña. [Más información sobre los informes de campaña](../reports/campaign-global-report-cja.md)

+++

+++**Habilitar modo de envío rápido** (push).

El modo de envío rápido es un complemento de [!DNL Journey Optimizer] que permite el envío muy rápido de mensajes push en grandes volúmenes a través de campañas. La entrega rápida se utiliza cuando el retraso en la entrega de mensajes es crítico para la empresa, cuando desea enviar una alerta push urgente en teléfonos móviles, por ejemplo, una noticia de última hora a los usuarios que han instalado su aplicación de canal de noticias. Para obtener más información sobre el rendimiento al usar el modo de envío rápido, consulte [Descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html).

+++

+++**Asignar puntuaciones de prioridad** (web, en la aplicación, basado en código)

Asignar una puntuación de prioridad a la campaña le permite priorizar una entrada y una campaña cuando hay una restricción impuesta, como un límite de frecuencia. Introduzca un valor numérico (de 0 a 100). Tenga en cuenta que, cuanto mayor sea el número, mayor será la prioridad. [Aprenda a asignar puntuaciones de prioridad a recorridos y campañas](../conflict-prioritization/priority-scores.md)

+++

+++**Establecer reglas de envío adicionales** (Tarjetas de contenido)

Para las campañas de tarjeta de contenido, puede habilitar reglas de entrega adicionales para elegir los eventos y criterios que almacenan el mensaje en déclencheur. [Aprenda a crear tarjetas de contenido](../content-card/create-content-card.md)

+++

+++**Definir déclencheur** (en la aplicación)

Para los mensajes en la aplicación, puedes usar el botón **[!UICONTROL Editar déclencheur]** para elegir los eventos y los criterios que almacenan el mensaje en déclencheur. [Aprenda a crear un mensaje en la aplicación](../in-app/create-in-app.md)

+++

## Pasos siguientes {#next}

Una vez que la acción de campaña esté lista, puede diseñar su contenido. [Más información](campaign-content.md)
