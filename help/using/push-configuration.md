---
title: Configuración de notificaciones push
description: Aprenda a configurar su entorno para enviar notificaciones push con Journey Optimizer
source-git-commit: 364861beb52e5663389a254ba145b31431b696ac
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 1%

---

# Configurar el canal de notificaciones push {#push-notification-configuration}

![](assets/do-not-localize/badge.png)

Antes de empezar a enviar notificaciones push con [!DNL Journey Optimizer], debe definir la configuración en [!DNL Adobe Experience Platform] y [!DNL Adobe Experience Platform Launch].

## Configuración de Adobe Experience Platform {#platform-settings}

Para configurar la aplicación móvil en [!DNL Adobe Experience Platform Launch], siga estos pasos:

1. [Asignación de derechos de propiedad y compañía](#push-rights)
1. [Añada las credenciales push de la aplicación móvil en el Platform launch](#push-credentials-launch).
1. [Cree la ](#edge-configuration) configuración de Edge que utilizará la  **[!UICONTROL Edge]** extensión para enviar datos personalizados desde dispositivos móviles a  [!DNL Adobe Experience Platform].
1. [Configure una propiedad](#launch-property) de Platform launch.
1. [Publique la propiedad](#publish-property).
1. [Configure ProfileDataSource](#configure-profiledatasource).

### Paso 1: Asignar derechos de propiedad y compañía {#push-rights}

Antes de crear una aplicación móvil, primero debe asegurarse de tener o asignar los permisos de usuario correctos.

Para obtener más información sobre la administración de usuarios con [!DNL Adobe Experience Platform Launch], consulte [Documentación del Platform launch](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions).

Para asignar derechos de propiedad y compañía:

1. Acceda a [!DNL Admin Console].

1. En la pestaña **[!UICONTROL Products]**, seleccione la tarjeta **[!UICONTROL Adobe Experience Platform Launch]** .

   ![](assets/push_product_1.png)

1. Seleccione un **[!UICONTROL Product Profile]** existente o cree uno nuevo con el botón **[!UICONTROL New profile]**. Para obtener más información sobre cómo crear un **[!UICONTROL New profile]** nuevo, consulte la [Documentación de la consola de administración](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui).

1. En la pestaña **[!UICONTROL Permissions]**, seleccione **[!UICONTROL Property rights]**.

   ![](assets/push_product_2.png)

1. Haga clic en **[!UICONTROL Add all]**. Esto agregará los siguientes derechos a su perfil de producto:
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   ![](assets/push_product_3.png)

1. A continuación, seleccione **[!UICONTROL Company rights]** en el menú de la izquierda.

   ![](assets/push_product_4.png)

1. Añada los siguientes derechos:

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   ![](assets/push_product_5.png)

1. Haga clic en **[!UICONTROL Save]**.

Para asignar esta **[!UICONTROL Product profile]** a los usuarios:

1. En [!DNL Admin Console], en la pestaña **[!UICONTROL Products]**, seleccione la tarjeta **[!UICONTROL Adobe Experience Platform Launch]** .

1. Seleccione el **[!UICONTROL Product profile]** configurado anteriormente.

1. En la pestaña **[!UICONTROL Users]**, haga clic en **[!UICONTROL Add user]**.

   ![](assets/push_product_6.png)

1. Escriba el nombre o la dirección de correo electrónico del usuario y seleccione el usuario. A continuación, haga clic en **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Si el usuario no se ha creado anteriormente en Admin Console, consulte la [documentación de Agregar usuarios](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)


Ahora tiene los permisos de usuario correctos para crear y configurar una aplicación móvil en [!DNL Adobe Experience Platform Launch].

### Paso 2: Agregue las credenciales push de la aplicación móvil en el Platform launch {#push-credentials-launch}

Después de conceder los permisos de usuario correctos, debe agregar las credenciales push de la aplicación móvil en [!DNL Adobe Experience Platform Launch].

Para obtener más información y procedimientos sobre cómo añadir las credenciales push de la aplicación móvil, consulte los pasos detallados en [Documentación del SDK móvil de Adobe Experience Platform](https://aep-sdks.gitbook.io/docs/beta/adobe-journey-optimizer#configure-the-journey-optimizer-extension-in-launch).

<!--
Note that to add push credentials in [!DNL Adobe Experience Platform Launch], the owner of the mobile app should fetch them from APNs/FCM.
1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. Select the **[!UICONTROL App Configurations]** tab in the left-hand panel and click **[!UICONTROL App Configuration]** to create a new configuration.

1. Enter a **[!UICONTROL Name]** for the configuration.

1. From the **[!UICONTROL Messaging Service Type]** drop-down menu, select the **[!UICONTROL Messaging service type]** to be used for these credentials. Here, we selected **[!UICONTROL Apple Push Notification Service]** since we are working with iOS.

1. Enter the mobile app **[!UICONTROL Bundle Id]** in the **[!UICONTROL App ID (iOS Bundle ID)]** field if you are using Apple push notification service or in the **[!UICONTROL App ID (Android package name)]** field if you are using Firebase Cloud Messaging.

    ![](assets/push_launch_app_configuration.png)

1. Drag and drop the .p8 key file or the .json private key file to the **[!UICONTROL Push Credentials]** field.

1. Enter the **[!UICONTROL Key Id]** and **[!UICONTROL Team Id]** if you are using Apple push notification service.

1. Click **[!UICONTROL Save]** to create your app configuration.
-->

### Paso 3: Crear configuración de Edge {#edge-configuration}

**[!UICONTROL Edge configuration]** se utiliza en  **[!UICONTROL Edge]** extension para enviar datos personalizados desde dispositivos móviles a  [!DNL Adobe Experience Platform].
Para configurar [!DNL Adobe Experience Platform], debe proporcionar el nombre **[!UICONTROL Sandbox]** y **[!UICONTROL Event Dataset]**.

Para obtener más información y procedimientos sobre cómo crear **[!UICONTROL Edge configuration]**, consulte los pasos detallados en [Documentación del SDK de Adobe Experience Platform Mobile](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).


<!--
1. From [!DNL Adobe Experience Platform Launch], select the **[!UICONTROL Edge Configurations]** tab and click **[!UICONTROL Edge Configurations]**.
    
1. Select **[!UICONTROL New Edge Configuration]** to add a new **[!UICONTROL Edge Configuration]**.
1. Enter a **[!UICONTROL Name]** and click **[!UICONTROL Save]**

1. Click the **[!UICONTROL Adobe Experience Platform]** toggle to enable it.

1. Fill in the **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** fields. Then, click **[!UICONTROL Save]**.
    
    ![](assets/push-config-4.png)
-->

### Paso 4: Configurar una propiedad de Platform launch {#launch-property}

La configuración de una propiedad [!DNL Adobe Experience Platform Launch] permite que el desarrollador de aplicaciones móviles o el especialista en marketing configuren atributos de SDK móviles, como Tiempos de espera de sesión, el [!DNL Adobe Experience Platform] simulador de pruebas objetivo y el **[!UICONTROL Adobe Experience Platform Datasets]** que se utilizará para que el SDK móvil envíe datos a .

Para obtener más información y procedimientos sobre cómo configurar un **[!UICONTROL Platform Launch property]**, consulte los pasos detallados en [Documentación del SDK de Adobe Experience Platform Mobile](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property).

Para que los SDK necesarios para que funcione la notificación push, necesitará las siguientes extensiones de SDK, tanto para Android como para iOS:

* **[!UICONTROL Mobile Core]** (instalado automáticamente)
* **[!UICONTROL Profile]** (instalado automáticamente)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, opcional pero recomendado para depurar la implementación móvil.

Para obtener más información sobre las [!DNL Adobe Experience Platform Launch] extensiones, consulte [Documentación del Platform launch](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html).

<!--

1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. select the **[!UICONTROL Properties]** tab and click **[!UICONTROL New Property]**.

    ![](assets/push-config-6.png)

1. Enter a **[!UICONTROL Name]** for your new property.

1. Select **[!UICONTROL Mobile]** as **[!UICONTROL Platform]**.

    ![](assets/push-config-7.png)

1. Click **[!UICONTROL Save]** to create your new property.

To configure **[!UICONTROL Adobe Experience Platform Edge Extension]** to send custom data from mobile devices to [!DNL Adobe Experience Platform].

1. Select your previously created property and select the **[!UICONTROL Extensions]** tab to view the extensions for this property.

    ![](assets/push-config-8.png)

1. Click **[!UICONTROL Configure]** under the **[!UICONTROL Adobe Experience Platform Edge]** Network' extension.

1. From the **[!UICONTROL Edge Configuration]** drop-down list, select the **[!UICONTROL Edge Configuration]** created in the previous steps. For more information on **[!UICONTROL Edge Configuration]**, refer to this [section](#edge-configuration).

1. Click **[!UICONTROL Save]**.

To configure **[!UICONTROL Adobe Experience Platform Messaging]** extension to send push profile and push interactions to the correct datasets, follow the same steps as above. Use **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** created in the [Adobe Experience Platform setup](#edge-configuration).
-->

### Paso 5: Publicar la propiedad {#publish-property}

Ahora debe publicar la propiedad para integrar la configuración y utilizarla en la aplicación móvil.

Para publicar su propiedad, consulte los pasos detallados en [Documentación del SDK de Adobe Experience Platform Mobile](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)

### Paso 6: Configurar ProfileDataSource {#configure-profiledatasource}

Para configurar `ProfileDataSource`, utilice la configuración `ProfileDCInletURL` de [!DNL Adobe Experience Platform] y añada lo siguiente en la aplicación móvil:

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

<!--
## Test your mobile app with custom action {#mobile-app-test}

After configuring your mobile app in both Adobe Experience Platform and Adobe Launch, you can now test it before sending push notifications to your profiles. In this use case, we will create a journey to target our mobile app and set a custom action which will trigger the push notification.

You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).

For this journey to work, you need to create an XDM schema. For more information, refer to [XDM documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#schemas-and-data-ingestion).

1. In the left menu, click **[!UICONTROL Data]** then **[!UICONTROL Schemas]** under **[!UICONTROL Data management]** to create your XDM schema.

    ![](assets/test_push_1.png)

1. Click **[!UICONTROL Create schema]** then select **[!UICONTROL XDM Experience event]**.

    ![](assets/test_push_2.png)

1. In the right pane, enter the name of your schema and description. Enable this schema for **[!UICONTROL Profile]**.

1. In the left pane, click **[!UICONTROL Add]** under **[!UICONTROL Mixins]** and select  **[!UICONTROL Create a new Mixin]**. For more information on how to create mixin, refer to [XDM System documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/create-mixin.html?lang=en#api).

    ![](assets/test_push_3.png)

1. Enter a **[!UICONTROL Display Name]** and a **[!UICONTROL Description]**. Click **[!UICONTROL Add mixin]** when done.

    ![](assets/test_push_4.png)

1. In the **[!UICONTROL Field properties]** window, add a **[!UICONTROL Field name]**, **[!UICONTROL Display name]** and select **[!UICONTROL String]** as **[!UICONTROL Type]**.

    ![](assets/test_push_5.png)

1. Check **[!UICONTROL Required]** and click **[!UICONTROL Apply]**.

1. Click **[!UICONTROL Save]**. Your schema is now created and can be used in an **[!UICONTROL Event schema]**.

You then need to set up an **[!UICONTROL Event schema]** where you will set the custom action which you will need to enter in your mobile app to trigger your push notification.

1. From the left menu of the home page, click the **[!UICONTROL Admin]** icon, then click **[!UICONTROL Manage]** from the **[!UICONTROL Events]** card to create your new **[!UICONTROL Event schema]**.

1. Click **[!UICONTROL Add]**, the event configuration pane opens on the right side of the screen.

    ![](assets/test_push_6.png)

1. Enter the name of your event. You can also add a description.

1. In the **[!UICONTROL Event ID type]** field, select **[!UICONTROL Rule Based]**.

1. In the **[!UICONTROL Parameters]**, select your previously created XDM event.

    ![](assets/test_push_7.png)

1. Click **[!UICONTROL Edit]** in the **[!UICONTROL Event ID condition]** field.

1. Drag and your previously added mixin to define the condition that will be used by the system to identify the events that will trigger your journey.

    ![](assets/test_push_8.png)

1. Type in the syntax that you will need to use to trigger your push notification in your test app, in this example **order confirmation**.

    ![](assets/test_push_9.png)

1. Select **[!UICONTROL ECID]** as your **[!UICONTROL Namespace]**.

1. Click **[!UICONTROL Ok]** then **[!UICONTROL Save]**.

Your **[!UICONTROL Event schema]** is now created and can now be used in a journey.

1. In the left menu from [!DNL Journey Optimizer] homepage, click **[!UICONTROL Journeys]**.

1. Click **[!UICONTROL Create]** to create a new journey.

    ![](assets/test_push_10.png)

1. Edit the journey's properties in the configuration pane displayed on the right side. Learn more in this [section](building-journeys/journey-gs.md#change-properties).

1. Start by drag and dropping the **[!UICONTROL Event schema]** created in the previous steps from the **[!UICONTROL Events]** drop-down.

    ![](assets/test_push_11.png)

1. From the **[!UICONTROL Actions]** drop-down, drag and drop a **[!UICONTROL Message]** activity to your journey.

1. Select a previously created message. For more information on how to create push notifications, refer to this [page](create-message.md).

1. Drag and drop an **[!UICONTROL End]** activity to your journey.

1. Activate **[!UICONTROL Test]** to your journey to start testing your push notifications and click **[!UICONTROL Trigger an event]**.

    ![](assets/test_push_12.png)

1. Enter your ECID in the **[!UICONTROL Key]** field then your event that will trigger the push notification in our case **order confirmation**.

    ![](assets/test_push_13.png)

1. Click **[!UICONTROL Send]**.

Your event will be triggered and you will receive your push notification to your mobile app.

![](assets/test_push_14.png)
-->

### Paso 7: Crear un ajuste preestablecido de mensaje {#message-preset}

Una vez configurada la aplicación móvil en [!DNL Adobe Experience Platform Launch], debe crear un ajuste preestablecido de mensaje para poder enviar notificaciones push desde **[!DNL Journey Optimizer]**.

Aprenda a crear y configurar un ajuste preestablecido de mensaje en [esta sección](configuration/message-presets.md).