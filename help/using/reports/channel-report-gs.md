---
solution: Journey Optimizer
product: journey optimizer
title: Informes de canal
description: Introducción a los informes de canal
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 247b966d-4f84-453b-8178-9c9ebcd494ef
source-git-commit: 0b4af69bcd410d467f7b6a26aa407b1df23a965e
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 2%

---

# Introducción a los informes de canal {#channel-report-gs}

Los informes de canal sirven como una potente herramienta que proporciona una visión general completa de las métricas de tráfico y participación en un informe unificado para cada canal, que incluye todas las acciones de todas las campañas y Recorridos. Se divide en diferentes widgets, cada uno de los cuales proporciona una vista específica del rendimiento de la campaña o del recorrido.

Los informes de canal son totalmente personalizables, por lo que puede cambiar el tamaño de los widgets o eliminarlos para crear un tablero que satisfaga sus necesidades específicas. También puede exportar los datos del informe a un PDF o archivo CSV para su posterior análisis.

Obtenga más información sobre las distintas métricas y widgets disponibles para los informes de canal en esta [página](channel-report.md).

## Antes de empezar {#manage-reports-prereq}

Antes de empezar, compruebe que tiene acceso a **[!UICONTROL Informes]** menú.

Si no puede ver el **[!UICONTROL Informes]** , los derechos de acceso deben ampliarse para incluir el **[!UICONTROL Ver informes de canal]** permiso. Puede ampliar sus propios permisos si tiene acceso a Adobe Experience Platform [Permisos](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=es){target="_blank"} para su organización. Si no es así, póngase en contacto con el administrador de Adobe Journey Optimizer.

+++Obtenga información sobre cómo asignar permisos de informe

Tenga en cuenta que este permiso está incluido en el siguiente complemento integrado **[!UICONTROL Funciones]**: administrador de campañas, aprobador de campañas, visor de campañas y administrador de campañas.

Para asignar el permiso correspondiente a su **[!UICONTROL Rol]**:

1. Desde el [!DNL Permissions] producto, vaya a la **[!UICONTROL Funciones]** y seleccione la función que desea actualizar con el nuevo **[!UICONTROL Ver informes de canal]** permiso.

1. De su **[!UICONTROL Rol]** panel, haga clic en **[!UICONTROL Editar]**.

   ![](assets/channel_permission_1.png)

1. Arrastre y suelte el **[!UICONTROL Informes]** recurso para asignar permiso.

   Desde el **[!UICONTROL Informe]** menú desplegable de recursos, seleccione **[!UICONTROL Ver informes de canal]** permiso.

   ![](assets/channel_permission_2.png)

1. Haga clic en **[!UICONTROL Guardar]**.

Usuarios asignados a esto **[!UICONTROL Rol]** ahora pueden acceder a la **[!UICONTROL Informes]** menú.

+++

## Administrar el tablero de informes {#manage-reports}

Para acceder y administrar los informes de canal, siga estos pasos:

1. Vaya a **[!UICONTROL Informes]** menú dentro de **[!UICONTROL Administración de recorrido]** sección.

   ![](assets/channel_report_1.png)

1. En el tablero, elija una **Inicio** y **[!UICONTROL Hora de finalización]** para segmentar datos específicos.

1. Desde el **[!UICONTROL Acción desde]** , seleccione si quiere segmentar campañas, Recorridos o ambos.

   ![](assets/channel_report_2.png)

1. Clic **[!UICONTROL Modificar]** para cambiar el tamaño o quitar widgets y crear un tablero que satisfaga sus necesidades específicas.

   ![](assets/channel_report_3.png)

1. Cuando esté satisfecho con el orden de visualización y el tamaño de los widgets, haga clic en **[!UICONTROL Guardar]**.

1. Según el widget, puede elegir cambiar de una tabla, un gráfico de barras o un anillo.

1. Haga clic en el icono de porcentaje para mostrar los datos como tasas.

   ![](assets/channel_report_4.png)

## Exportación de informes {#export-reports}

Puede exportar fácilmente los distintos informes a los formatos PDF o CSV, lo que le permite compartirlos, manipularlos o imprimirlos. Los pasos detallados para exportar los informes de canal están disponibles en las siguientes pestañas:

>[!BEGINTABS]

>[!TAB Exportación del informe como archivo de PDF]

1. En el informe, haga clic en **[!UICONTROL Exportar]** y seleccione **[!UICONTROL archivo de PDF]**.

1. En la ventana Imprimir, configure el documento según sea necesario. Tenga en cuenta que las opciones pueden variar según el explorador.

1. Elija imprimir o guardar el informe como PDF.

1. Busque la carpeta en la que desea guardar el archivo, cambie su nombre si es necesario y haga clic en Guardar.

El informe ya está disponible para su visualización o uso compartido en un archivo pdf.

>[!TAB Exportación del informe como archivo CSV]

1. En el informe, haga clic en **[!UICONTROL Exportar]** y seleccione **[!UICONTROL Archivo CSV]** para generar un archivo CSV en el nivel de informe general.

1. También puede elegir exportar datos de un widget específico. Clic **[!UICONTROL Exportar datos de widget a CSV]** situado junto al widget seleccionado.

1. El archivo se descargará automáticamente y se podrá encontrar en los archivos locales.

   Si ha generado el archivo en el nivel de informe, contiene información detallada para cada widget, incluidos su título y datos.

   Si ha generado el archivo en el nivel de widget, proporciona específicamente datos para el widget seleccionado.

>[!ENDTABS]
