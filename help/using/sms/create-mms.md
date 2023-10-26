---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un MMS
description: Obtenga información sobre cómo crear un MMS en Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 9%

---

# Creación de un mensaje MMS {#create-mms}

## Requisitos previos{#sms-prerequisites}

Antes de crear el mensaje SMS, primero debe configurar el proveedor de SMS con Journey Optimizer, siga estos pasos:

* Antes de enviar SMS, debe integrar la configuración del proveedor con Journey Optimizer.

+++ Aprenda a crear una nueva credencial de la API de MMS de Sinch.

   1. En el carril izquierdo, vaya a **[!UICONTROL Administration]** > **[!UICONTROL Canales]** y seleccione la **[!UICONTROL Credenciales de API]** menú. Haga clic en **[!UICONTROL Crear nuevas credenciales de API]** botón.

      ![](assets/sms_6.png)

   1. Configure las credenciales de la API de SMS:

   * En el caso de **[!DNL Sinch MMS]**:

      * **[!UICONTROL Nombre]**: elija un nombre para la credencial de la API.

      * **[!UICONTROL Identificador de proyecto]**, **[!UICONTROL ID de aplicación]** y **[!UICONTROL Token de API]**: en el menú API de conversación, puede encontrar sus credenciales en el menú Aplicación.  [Más información](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html)

     ![](assets/mms_provider.png)

   1. Clic **[!UICONTROL Enviar]** cuando haya terminado de configurar las credenciales de la API.

  Después de crear y configurar las credenciales de la API, debe crear una superficie de canal (es decir, un ajuste preestablecido de mensaje) para los mensajes SMS.

+++

* Una vez finalizado, deberá crear una superficie SMS. Estos pasos debe realizarlos un administrador del sistema de Adobe Journey Optimizer.

+++ Aprenda a crear la superficie de canal.

   1. En el carril izquierdo, vaya a **[!UICONTROL Administration]** > **[!UICONTROL Canales]** y seleccione **[!UICONTROL Marca]** > **[!UICONTROL Superficies de canal]**. Haga clic en **[!UICONTROL Crear superficie de canal]** botón.

      ![](assets/preset-create.png)

   1. Introduzca un nombre y una descripción (opcional) para la superficie y, a continuación, seleccione el canal SMS.

      ![](assets/sms-create-surface.png)

      >[!NOTE]
      >
      > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` y guiones `-` caracteres.

   1. Defina el **Configuración de SMS**.

      ![](assets/sms-surface-settings.png)

      Comience por seleccionar la **[!UICONTROL Tipo de SMS]** que se enviarán con la superficie: **[!UICONTROL Transaccional]** o **[!UICONTROL Marketing]**.

      * Elegir **Marketing** para SMS promocionales: estos mensajes requieren el consentimiento del usuario.
      * Elegir **Transaccional** para mensajes no comerciales, como confirmaciones de pedidos, notificaciones de restablecimiento de contraseña o información de entrega, por ejemplo.

      Al crear un mensaje SMS, debe elegir una superficie de canal válida que coincida con la categoría seleccionada para el mensaje.

      >[!CAUTION]
      >
      >**Transaccional** Los mensajes SMS se pueden enviar a perfiles que cancelaron la suscripción a comunicaciones de marketing. Estos mensajes solo se pueden enviar en contextos específicos.

   1. Seleccione el **[!UICONTROL Configuración de SMS]** para asociarlo con la superficie.

      Para obtener más información sobre cómo configurar su entorno para enviar mensajes SMS, consulte [esta sección](#create-api).

   1. Introduzca el **[!UICONTROL Número de remitente]** &#x200B;desea utilizar para sus comunicaciones.

   1. Seleccione su **[!UICONTROL Campo de ejecución de SMS]** para seleccionar **[!UICONTROL Atributo de perfil]** asociado a los números de teléfono de los perfiles.

   1. Si desea utilizar la función de acortamiento de URL en los mensajes SMS, seleccione un elemento del **[!UICONTROL Subdominio]** lista.

      >[!NOTE]
      >
      >Para poder seleccionar un subdominio, asegúrese de haber configurado previamente al menos un subdominio de SMS. [Descubra cómo](sms-subdomains.md)

   1. Introduzca el **[!UICONTROL Número de exclusión]** que desee utilizar para esta superficie. Cuando los perfiles se excluyen de este número, aún puede enviarles mensajes de otros números que pueda utilizar para enviar mensajes SMS con [!DNL Journey Optimizer].

      >[!NOTE]
      >
      >Entrada [!DNL Journey Optimizer]Por lo tanto, la exclusión de SMS ya no se administra en el nivel de canal. Ahora es específico de un número.

   1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Enviar]** para confirmar. También se puede guardar la superficie de canal como inclinación y reanudar su configuración más adelante.

      ![](assets/sms-submit-surface.png)

   1. Una vez creada la superficie de canal, esta se muestra en la lista con el **[!UICONTROL Procesando]** estado.

      >[!NOTE]
      >
      >Si las comprobaciones no se realizan correctamente, obtenga más información sobre los posibles motivos de error en [esta sección](#monitor-channel-surfaces).

   1. Una vez que las comprobaciones son correctas, la superficie de canal obtiene el **[!UICONTROL Activo]** estado. Está listo para utilizarse para enviar mensajes.

      ![](assets/preset-active.png)


## Creación de un mensaje SMS {#create-sms-journey-campaign}

Examine las pestañas siguientes para aprender a añadir un mensaje SMS en una campaña o un recorrido.

>[!BEGINTABS]

>[!TAB Añadir un mensaje SMS a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad SMS desde el **Acciones** de la paleta.

   ![](assets/sms_create_1.png)

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie de mensaje que desea utilizar.

   ![](assets/sms_create_2.png)

   Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md)

   El **[!UICONTROL Superficie]** de forma predeterminada, el campo está rellenado previamente con la última superficie que el usuario utilizó para ese canal.

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el **[!UICONTROL Editar contenido]** botón. [Definición del contenido de los SMS](#sms-content)

>[!TAB Adición de un mensaje SMS a una campaña]

1. Cree una nueva campaña programada o activada por API, seleccione **[!UICONTROL SMS]** como su acción y elija la **[!UICONTROL Superficie de aplicación]** para usar. [Más información sobre la configuración de SMS](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Haga clic en **[!UICONTROL Crear]**.

1. Desde el **[!UICONTROL Propiedades]** , edite el de la campaña **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

   ![](assets/sms_create_4.png)

1. Haga clic en **[!UICONTROL Seleccionar audiencia]** para definir la audiencia de destino a partir de la lista de audiencias de Adobe Experience Platform disponibles. [Más información](../audience/about-audiences.md).

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a los individuos de la audiencia seleccionada. [Más información](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Clic **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido y crear tratamientos para medir su rendimiento e identificar la mejor opción para la audiencia de destino. [Más información](../campaigns/content-experiment.md)

1. En el **[!UICONTROL Seguimiento de acciones]** , especifique si desea rastrear los clics en los vínculos del mensaje SMS.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o en una frecuencia recurrente. Obtenga información sobre cómo configurar el **[!UICONTROL Programación]** de la campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. Desde el **[!UICONTROL Déclencheur de acción]** , seleccione la opción **[!UICONTROL Frecuencia]** del mensaje SMS:

   * Una vez
   * Diario
   * Semanal
   * Mes

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el **[!UICONTROL Editar contenido]** botón. [Diseño del contenido del SMS](#sms-content)

>[!ENDTABS]

## Definición del contenido de MMS{#mms-content}

1. En la pantalla de configuración del recorrido o la campaña, haga clic en **[!UICONTROL Editar contenido]** para configurar el contenido del SMS.

1. Haga clic en **[!UICONTROL Mensaje]** para abrir el Editor de expresiones.

   ![](assets/sms-content.png)

1. Utilice el Editor de expresiones para definir contenido y agregar contenido dinámico. Puede utilizar cualquier atributo, como el nombre del perfil o la ciudad. Más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md) en el Editor de expresiones.

1. Habilite la opción MMS para añadir contenido multimedia al contenido de SMS.

   >[!NOTE]
   >
   > La opción MMS solo está disponible con Sinch. Debe crear una credencial de API específica para crear MMS. [Más información](sms-configuration.md#create-new-api)

   ![](assets/sms_create_6.png)

1. Añadir un **[!UICONTROL Título]** a sus medios.

1. Introduzca la URL del contenido en la **[!UICONTROL Medios]** field.

   ![](assets/sms_create_7.png)

1. Haga clic en **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa. Puede utilizar **[!UICONTROL Simular contenido]** para previsualizar las direcciones URL abreviadas o el contenido personalizado.

Ahora puede probar y enviar el mensaje SMS a su audiencia. [Más información](send-sms.md)
Una vez enviado, puede medir el impacto de su SMS dentro de los informes de Campaña o Recorrido. Para obtener más información sobre la creación de informes, consulte [esta sección](../reports/campaign-global-report.md#sms-tab).

>[!NOTE]
>
>De acuerdo con las normas y los reglamentos del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Para ello, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. [Obtenga información sobre cómo administrar la exclusión](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Temas relacionados**

* [Previsualización, prueba y envío de su mensaje SMS](send-sms.md)
* [Configuración del canal de SMS](sms-configuration.md)
* [Informe SMS](../reports/journey-global-report.md#sms-global)