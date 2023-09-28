---
solution: Journey Optimizer
product: journey optimizer
title: Informe global
description: Aprenda a utilizar los datos del informe global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: 92cf1d4a350359adbbad93c4006ec7a0e3902397
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Introducción al Informe global {#global-report}

>[!NOTE]
>
> Si las consultas personalizadas se realizan mediante API al utilizar el servicio de consulta, espere algún retraso para los informes.

Utilice el **[!UICONTROL Informe global]** para medir el impacto de los recorridos y envíos durante un periodo seleccionado.

* Si desea dirigirse a un recorrido o envíos en el contexto de un recorrido, desde el **[!UICONTROL Recorridos]** , acceda al recorrido y haga clic en el **[!UICONTROL Ver informe]** botón. A continuación, puede encontrar los informes globales Recorrido, Correo electrónico, SMS y Push.

  ![](assets/report_journey.png)

* Si desea dirigirse a una campaña, en el **[!UICONTROL Campañas]** , acceda a la campaña y haga clic en **[!UICONTROL Informes]** botón.

  ![](assets/report_campaign.png)

* Si desea cambiar de la **[!UICONTROL Informe en vivo]** a la **[!UICONTROL Informe global]** para la entrega, haga clic en **[!UICONTROL Siempre]** en el conmutador de pestañas.

  ![](assets/report_5.png)

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](#list-of-components-global)

## Personalizar tablero {#modify-dashboard}

Para modificar cada tablero de informes, cambie el período de tiempo y cambie el tamaño o elimine los widgets. Cambiar los widgets solo afecta al tablero del usuario actual. Otros usuarios verán sus propios tableros o los establecidos de forma predeterminada.

1. En el informe global, seleccione una hora de inicio y otra de finalización para segmentar datos específicos.

   ![](assets/report_modify_1.png)

1. Elija si desea excluir los eventos de prueba de los informes con la barra de alternancia. Para obtener más información sobre los eventos de prueba, consulte [esta página](../building-journeys/testing-the-journey.md).

   Tenga en cuenta que la variable **[!UICONTROL Excluir eventos de prueba]** Esta opción solo está disponible para informes de Recorrido.

   ![](assets/report_modify_2.png)

1. Clic **[!UICONTROL Modificar]** para empezar a personalizar el tablero.

   ![](assets/report_modify_3.png)

1. Ajuste el tamaño de los widgets arrastrando su esquina inferior derecha.

   ![](assets/report_modify_4.png)

1. Clic **[!UICONTROL Eliminar]** para eliminar cualquier widget que no necesite.

   ![](assets/report_modify_5.png)

1. Cuando esté satisfecho con el orden de visualización y el tamaño de los widgets, haga clic en **[!UICONTROL Guardar]**.

1. Para personalizar la forma en que se muestran los datos, puede cambiar entre distintas opciones de visualización, como gráficos, tablas y gráficos circulares.

   ![](assets/report_modify_10.png)

El tablero se ha guardado. Los diferentes cambios se volverán a aplicar para un uso posterior de los informes activos. Si es necesario, utilice el **[!UICONTROL Restablecer]** para restaurar el orden predeterminado de los widgets y widgets.

## Exportación de informes {#export-reports}

Puede exportar fácilmente los distintos informes a los formatos PDF o CSV, lo que le permite compartirlos o imprimirlos.

>[!BEGINTABS]

>[!TAB Exportación del informe como archivo CSV]

1. En el informe, haga clic en **[!UICONTROL Exportar]** y seleccione **[!UICONTROL Archivo CSV]** para generar un archivo CSV en el nivel de informe general.

   ![](assets/export_1.png)

1. También puede elegir exportar datos de un widget específico. Clic **[!UICONTROL Exportar datos de widget a CSV]** situado junto al widget seleccionado.

   ![](assets/export_3.png)

1. El archivo se descargará automáticamente y se podrá encontrar en los archivos locales.

   Si ha generado el archivo en el nivel de informe, contiene información detallada para cada widget, incluidos su título y datos.

   Si ha generado el archivo en el nivel de widget, proporciona específicamente datos para el widget seleccionado.

>[!TAB Exportación del informe como archivo de PDF]

1. En el informe, haga clic en **[!UICONTROL Exportar]** y seleccione **[!UICONTROL archivo de PDF]**.

   ![](assets/export_2.png)

1. En la ventana Imprimir, configure el documento según sea necesario. Tenga en cuenta que las opciones pueden variar según el explorador.

1. Elija imprimir o guardar el informe como PDF.

1. Busque la carpeta en la que desea guardar el archivo, cambie su nombre si es necesario y haga clic en Guardar.

El informe ya está disponible para su visualización o uso compartido en un archivo pdf.



>[!ENDTABS]