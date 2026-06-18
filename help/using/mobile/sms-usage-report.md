---
solution: Journey Optimizer
product: journey optimizer
title: Ver métricas de uso de SMS
description: Obtenga información sobre cómo generar informes de uso de SMS para reconciliar el volumen de mensajería con la facturación del proveedor en Journey Optimizer.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: b519bcd5489c441e7f22cb47783d8b99a58c2442
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 1%

---

# Generar informe de uso de SMS {#sms-usage-report}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_metrics"
>title="Métricas de uso de SMS"
>abstract="Genere informes de uso de SMS para reconciliar el volumen de mensajería con la facturación del proveedor. Los informes enumeran los recuentos terminados en dispositivos móviles (MT) y originados en dispositivos móviles (MO) de cada código corto o número de teléfono, agregados por día."

>[!BEGINSHADEBOX]

**En esta página:** Generar informes de uso de SMS en Adobe Journey Optimizer para reconciliar el volumen completado por móvil (MT) y originado por móvil (MO) con la facturación del proveedor, usando una credencial de API de MMS de Sinch y una salida CSV descargable.

>[!ENDSHADEBOX]

Las métricas de uso de SMS están disponibles al comprar SMS a través de Adobe Journey Optimizer. Los informes resumen el tráfico de envío y recepción por código corto o número de teléfono, agregados por día, durante los últimos **90 días**.

Para ver las métricas de uso, un administrador debe:

1. [Cree una credencial de la API de MMS de Sinch](mobile-configuration-sinch.md#sinch-mms) que solo se use para recuperar datos de uso de Sinch.

   Los informes de uso requieren una credencial de API con **[!UICONTROL proveedor de SMS]** establecido en **Sinch MMS**. Esta credencial conecta Journey Optimizer con Sinch para que se puedan recuperar los datos de uso. Es independiente de las credenciales de Sinch utilizadas para enviar mensajes SMS o MMS, aunque los valores de campo proceden del mismo proyecto de Sinch.

1. [Configurar y recuperar un informe de uso de SMS](#configure-sms-usage-report).

Estos pasos requieren el permiso **[!UICONTROL Administrar configuración de SMS]**. [Obtenga más información sobre permisos](../administration/high-low-permissions.md#administration-permissions).

## Configuración y visualización de informes de uso de SMS {#configure-sms-usage-report}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_report_name"
>title="Nombre del informe"
>abstract="Introduzca una etiqueta que le ayude a reconocer este informe en la lista más adelante; por ejemplo, la revisión de facturación de mayo de 2026."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_credential"
>title="Credenciales de SMS"
>abstract="Seleccione la credencial de la API de Sinch cuyo tráfico de envío y recepción debe aparecer en este informe. Para agregar o actualizar credenciales, ve a **Administración** > **Canales** > **Credenciales de API**, y luego elige **Proveedor de SMS** > **Sinch MMS**."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_start_date"
>title="Fecha de inicio"
>abstract="Primer día del intervalo de fechas que se va a incluir en el informe. Los datos de uso solo están disponibles durante los últimos 90 días."

Los informes de uso de SMS presentan el volumen originado en dispositivos móviles (MO) y terminado en dispositivos móviles (MT) por código corto para admitir la reconciliación entre la facturación del proveedor y la actividad de mensajería en Journey Optimizer.

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de SMS]**.

1. Acceda al menú **[!UICONTROL Ver métricas de uso de SMS]** y haga clic en **[!UICONTROL Configurar nuevo informe]**.

   ![](assets/usage_report_1.png)

1. Configure el informe:

   * **[!UICONTROL Nombre del informe]**: escriba una etiqueta que le ayude a reconocer el informe.
   * **[!UICONTROL Credenciales de SMS]**: seleccione la credencial de la API **Sinch MMS** que creó anteriormente para sus informes de uso de SMS.
   * **[!UICONTROL Fecha de inicio]** y **[!UICONTROL Fecha de finalización]**: establezca el intervalo de fechas para el informe. Los datos de uso solo están disponibles durante los últimos 90 días.

     ![](assets/usage_report_2.png)

1. Haga clic en **[!UICONTROL Configurar informe]** para enviar la solicitud.

1. En la lista **[!UICONTROL Informes enviados]**, busque el informe que configuró y haga clic en **[!UICONTROL Recuperar informe]**.

   El estado cambia a **Pendiente** mientras se genera el informe.

1. Una vez que el estado del informe se haya actualizado a **[!UICONTROL Listo]**, haga clic en **[!UICONTROL Ver]** para abrir el informe. El informe incluye:

   * **Resumen de uso**: total de mensajes originados en dispositivos móviles (MO) y terminados en dispositivos móviles (MT) para las fechas seleccionadas, desglosados por código corto.

   * **Volumen diario de SMS**: volumen de SMS por día, desglosado por código corto.

     ![](assets/usage_report_3.png)

1. Para exportar el informe, haga clic en **[!UICONTROL Descargar CSV]**. Journey Optimizer descarga un archivo CSV para el informe que está viendo.
