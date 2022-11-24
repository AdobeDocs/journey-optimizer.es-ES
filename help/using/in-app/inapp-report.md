---
title: Informe en la aplicación
description: Obtenga información sobre cómo utilizar los datos del informe en la aplicación
feature: Reporting
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3d496efc-1bf9-4895-906c-3757f92c6fe3
source-git-commit: 6b3207f8da2f022d6094e6a2f321ac1b4f137e83
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 3%

---

# Informe en la aplicación {#inapp-report}

El informe en la aplicación está disponible en el informe Campaña .

La página de informe Campaña se muestra con las siguientes pestañas:

* [Campaign](../reports/campaign-global-report.md#campaign-live)
* [Correo electrónico](../reports/campaign-global-report.md#email-live)
* [Push](../reports/campaign-global-report.md#push-live)
* [SMS](../reports/campaign-global-report.md#sms-live)
* [En la aplicación](#in-app-global)

La campaña **[!UICONTROL Informe global]** se divide en distintas utilidades que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](../reports/global-report.md#list-of-components-global.md)

## Pestaña en la aplicación {#inapp-global}

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL En la aplicación]** La pestaña detalla la información principal relativa a los envíos en la aplicación realizados en la campaña.

![](assets/campaign_report_global_6.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe en la aplicación.

La variable **[!UICONTROL Rendimiento en la aplicación]** Los KPI detallan la información principal relativa a la participación de los visitantes en los mensajes en la aplicación, como por ejemplo:

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se entregó el mensaje en la aplicación.

* **[!UICONTROL Impresiones]**: número total de mensajes en la aplicación entregados a todos los usuarios.

* **[!UICONTROL Tasa de clics]**: porcentaje de usuarios que interactuaron con los botones incluidos en el mensaje en la aplicación en comparación con los usuarios que vieron el mensaje.

* **[!UICONTROL Tasa de rechazo]**: porcentaje de mensajes en la aplicación que descartaron los destinatarios.

La variable **[!UICONTROL Resumen en la aplicación]** en el gráfico se muestra la evolución de las impresiones en la aplicación durante el periodo correspondiente.

La variable **[!UICONTROL Clics por botón]** la tabla y el gráfico contienen los datos disponibles para el comportamiento del destinatario por botón:

* **[!UICONTROL Clics]**: número total de destinatarios que interactuaron con los botones incluidos en el mensaje en la aplicación.

* **[!UICONTROL Tasa de clics]**: porcentaje de usuarios que interactuaron con los botones incluidos en el mensaje en la aplicación en comparación con los usuarios que vieron el mensaje.
+++

**Temas relacionados:**

* [Crear mensaje en la aplicación](../in-app/create-in-app.md)
* [Diseño de mensajes en la aplicación](../in-app/design-in-app.md)
* [Configuración en la aplicación](../in-app/inapp-configuration.md)


>[!BEGINTABS]

>[!TAB Añadir una inserción a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad Push desde la sección Actions de la paleta.

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie del mensaje que desea utilizar.

>[!TAB Adición de una push a una campaña]

1. Cree una nueva campaña programada o activada por la API, seleccione **[!UICONTROL Notificaciones push]** como su acción y elija el **[!UICONTROL Superficie de la aplicación]** para usar.

1. Haga clic en **[!UICONTROL Crear]**.

1. En el **[!UICONTROL Propiedades]** , edite la **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

1. Haga clic en el **[!UICONTROL Seleccionar la audiencia]** para definir la audiencia a la que se dirigirá desde la lista de segmentos de Adobe Experience Platform disponibles.

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o con una frecuencia recurrente. Obtenga información sobre cómo configurar la variable **[!UICONTROL Programación]** de su campaña.

1. En el **[!UICONTROL Déclencheur de acción]** , seleccione **[!UICONTROL Frecuencia]** de la notificación push:

   * Una vez
   * Diario
   * Semanal
   * Mensual

>[!ENDTABS]

Prueba 3:

1. Esta es una prueba

>[!BEGINTABS]

>[!TAB Añadir una inserción a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad Push desde la sección Actions de la paleta.

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie del mensaje que desea utilizar.

>[!TAB Adición de una push a una campaña]

1. Cree una nueva campaña programada o activada por la API, seleccione **[!UICONTROL Notificaciones push]** como su acción y elija el **[!UICONTROL Superficie de la aplicación]** para usar.

1. Haga clic en **[!UICONTROL Crear]**.

1. En el **[!UICONTROL Propiedades]** , edite la **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

1. Haga clic en el **[!UICONTROL Seleccionar la audiencia]** para definir la audiencia a la que se dirigirá desde la lista de segmentos de Adobe Experience Platform disponibles.

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o con una frecuencia recurrente. Obtenga información sobre cómo configurar la variable **[!UICONTROL Programación]** de su campaña.

1. En el **[!UICONTROL Déclencheur de acción]** , seleccione **[!UICONTROL Frecuencia]** de la notificación push:

   * Una vez
   * Diario
   * Semanal
   * Mensual

>[!ENDTABS]

1. Esto forma parte de la prueba
