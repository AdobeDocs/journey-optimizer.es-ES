---
solution: Journey Optimizer
product: journey optimizer
title: Configurar el webhook de SMS
description: Obtenga información sobre cómo configurar Webhooks para que capture respuestas entrantes para administrar el consentimiento de inclusión y de exclusión
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 0%

---

# Crear webhook {#webhook}

>[!BEGINSHADEBOX]

Si no se proporcionan las palabras clave de inclusión u exclusión, se utilizan mensajes de consentimiento estándar para respetar la privacidad del usuario. Añadir palabras clave personalizadas anula automáticamente los valores predeterminados.

**Palabras clave predeterminadas:**

* **Inclusión**: SUSCRIBIRSE, SÍ, NO DETENER, INICIAR, CONTINUAR, REANUDAR, INICIAR
* **Exclusión**: DETENER, SALIR, CANCELAR, FINALIZAR, CANCELAR SUSCRIPCIÓN, NO
* **Ayuda**: AYUDA

>[!ENDSHADEBOX]

Una vez que las credenciales de la API se hayan creado correctamente, ahora puede configurar los webhooks para capturar las respuestas entrantes para administrar el consentimiento de inclusión y de exclusión, y para recibir informes de entrega, incluidas las confirmaciones de lectura, cuando estén disponibles.

Al configurar un gancho web, puede definir su propósito según el tipo de datos que desee capturar:

* **[!UICONTROL Entrante]**: utilice esta opción si desea capturar las respuestas de consentimiento, como las inclusiones o las exclusiones, y recopilar las preferencias de usuario.

* **[!UICONTROL Comentarios]**: elija esta opción para realizar un seguimiento de los eventos de entrega y participación, incluidos los recibos de lectura y las interacciones del usuario, con el fin de admitir la creación de informes y el análisis.

Examine las pestañas siguientes en función de sus proveedores de SMS:

>[!BEGINTABS]

>[!TAB Personalizado]

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]**, seleccione el menú **[!UICONTROL Webhooks de SMS]** en **[!UICONTROL Configuración de SMS]** y haga clic en el botón **[!UICONTROL Crear webhook]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Configure las opciones de webhook, tal y como se detalla a continuación:

   * **[!UICONTROL Nombre]**: escribe un nombre para tu webhook.

   * **[!UICONTROL Seleccionar proveedor de SMS]**: personalizado.

   * **[!UICONTROL Tipo]**: Entrante.

   * **[!UICONTROL Credenciales de API]**: elija en la lista desplegable sus [credenciales de API configuradas anteriormente](sms-configuration-custom.md#api-credential).

   * **[!UICONTROL Número de teléfono del remitente]**: escribe el número de teléfono del remitente &#x200B;que quieras usar para tus comunicaciones.

     ![](assets/webhook-inbound.png){zoomable="yes"}

1. Haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar sus categorías de palabras clave y, a continuación, configúrelas según su proveedor de SMS:

   * **[!UICONTROL Categoría de palabras clave entrantes]**: elige las categorías de palabras clave **[!UICONTROL Inclusión]**, **[!UICONTROL Exclusión]**, **[!UICONTROL Inclusión doble]**, **[!UICONTROL Ayuda]** o **[!UICONTROL Personalizada]**.

   * **[!UICONTROL Escriba una palabra clave]**: escriba las palabras clave predeterminadas o personalizadas que almacenarán automáticamente en déclencheur el mensaje. Haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar varias palabras clave.

     Para **[!UICONTROL palabra clave personalizada]**, use palabras clave no relacionadas con el consentimiento para acciones basadas en lotes dentro de un recorrido.

   * **[!UICONTROL Mensaje de respuesta]**: seleccione en la lista desplegable la respuesta personalizada que se enviará automáticamente.

   * **[!UICONTROL Exclusión parcial]**: habilite esta opción para enviar una respuesta automática cuando se detecte una palabra clave de exclusión cercana a la coincidencia.

   ![](assets/sms_byo_6.png){zoomable="yes"}

1. Escriba un **[!UICONTROL mensaje de respuesta predeterminado]** que se enviará automáticamente cuando un mensaje entrante no coincida con ninguna palabra clave o categoría configurada.

1. Haga clic en **[!UICONTROL Ver editor de carga útil]** para validar y personalizar las cargas útiles de solicitud.

   Puede personalizar dinámicamente la carga útil mediante atributos de perfil y garantizar que se envíen datos precisos para el procesamiento y la generación de respuestas con la ayuda de funciones de ayuda integradas.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar su webhook.

1. Para crear un webhook de **[!UICONTROL Comentarios]**, sigue los mismos pasos que arriba y selecciona **[!UICONTROL Comentarios]** como tu webhook **[!UICONTROL Escriba]**.

1. Desde el menú de **[!UICONTROL Webhooks]**, puedes editar o eliminar los webhooks existentes, o acceder y copiar la **[!UICONTROL URL de Webhook]** para la integración con tu proveedor de SMS.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Después de crear y configurar las opciones del webhook, debes crear una [configuración de canal](sms-configuration-surface.md) para los mensajes SMS.

Una vez configuradas, puede aprovechar todas las funcionalidades de canal integradas, como la creación de mensajes, la personalización, el seguimiento de vínculos y la creación de informes.

>[!TAB Infobip]

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]**, seleccione el menú **[!UICONTROL Webhooks de SMS]** en **[!UICONTROL Configuración de SMS]** y haga clic en el botón **[!UICONTROL Crear webhook]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Configure las opciones de webhook, tal y como se detalla a continuación:

   * **[!UICONTROL Nombre]**: escribe un nombre para tu webhook.

   * **[!UICONTROL Seleccionar proveedor de SMS]**: Infobip.

   * **[!UICONTROL Tipo]**: Entrante.

   * **[!UICONTROL Credenciales de API]**: elija en la lista desplegable sus [credenciales de API configuradas anteriormente](sms-configuration-infobip.md#api-credential).

   * **[!UICONTROL Número de teléfono del remitente]**: escribe el número de teléfono del remitente &#x200B;que quieras usar para tus comunicaciones.

     ![](assets/webhook-infobip-1.png){zoomable="yes"}

1. Haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar sus categorías de palabras clave y, a continuación, configúrelas según su proveedor de SMS:

   * **[!UICONTROL Categoría de palabras clave entrantes]**: elige las categorías de palabras clave **[!UICONTROL Inclusión]**, **[!UICONTROL Exclusión]**, **[!UICONTROL Inclusión doble]**, **[!UICONTROL Ayuda]** o **[!UICONTROL Personalizada]**.

   * **[!UICONTROL Escriba una palabra clave]**: escriba las palabras clave predeterminadas o personalizadas que almacenarán automáticamente en déclencheur el mensaje. Haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar varias palabras clave.

     Para **[!UICONTROL palabra clave personalizada]**, use palabras clave no relacionadas con el consentimiento para acciones basadas en lotes dentro de un recorrido.

   * **[!UICONTROL Mensaje de respuesta]**: seleccione en la lista desplegable la respuesta personalizada que se enviará automáticamente.

   * **[!UICONTROL Exclusión parcial]**: habilite esta opción para enviar una respuesta automática cuando se detecte una palabra clave de exclusión cercana a la coincidencia.

   ![](assets/webhook-infobip-2.png){zoomable="yes"}

1. Escriba un **[!UICONTROL mensaje de respuesta predeterminado]** que se enviará automáticamente cuando un mensaje entrante no coincida con ninguna palabra clave o categoría configurada.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar su webhook.

1. Para crear un webhook de **[!UICONTROL Comentarios]**, sigue los mismos pasos que arriba y selecciona **[!UICONTROL Comentarios]** como tu webhook **[!UICONTROL Escriba]**.

1. Desde el menú de **[!UICONTROL Webhooks]**, puedes editar o eliminar los webhooks existentes, o acceder y copiar la **[!UICONTROL URL de Webhook]** para la integración con tu proveedor de SMS.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Después de crear y configurar las opciones de entrada para el webhook, debes crear una [configuración de canal](sms-configuration-surface.md) para los mensajes SMS.

Una vez configuradas, puede aprovechar todas las funcionalidades de canal integradas, como la creación de mensajes, la personalización, el seguimiento de vínculos y la creación de informes.

>[!TAB Sinch]

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]**, seleccione el menú **[!UICONTROL Webhooks de SMS]** en **[!UICONTROL Configuración de SMS]** y haga clic en el botón **[!UICONTROL Crear webhook]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Configure las opciones de webhook, tal y como se detalla a continuación:

   * **[!UICONTROL Nombre]**: escribe un nombre para tu webhook.

   * **[!UICONTROL Seleccionar proveedor de SMS]**: Sinch.

   * **[!UICONTROL Tipo]**: Entrante.

   * **[!UICONTROL Credenciales de API]**: elija en la lista desplegable sus [credenciales de API configuradas anteriormente](sms-configuration-sinch.md#create-api).

   * **[!UICONTROL Número de teléfono del remitente]**: escribe el número de teléfono del remitente &#x200B;que quieras usar para tus comunicaciones.

     ![](assets/webhook-sinch-1.png){zoomable="yes"}

1. Haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar sus categorías de palabras clave y, a continuación, configúrelas según su proveedor de SMS:

   * **[!UICONTROL Categoría de palabras clave entrantes]**: elige las categorías de palabras clave **[!UICONTROL Inclusión]**, **[!UICONTROL Exclusión]**, **[!UICONTROL Inclusión doble]**, **[!UICONTROL Ayuda]** o **[!UICONTROL Personalizada]**.

   * **[!UICONTROL Escriba una palabra clave]**: escriba las palabras clave predeterminadas o personalizadas que almacenarán automáticamente en déclencheur el mensaje. Haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar varias palabras clave.

     Para **[!UICONTROL palabra clave personalizada]**, use palabras clave no relacionadas con el consentimiento para acciones basadas en lotes dentro de un recorrido.

   * **[!UICONTROL Mensaje de respuesta]**: seleccione en la lista desplegable la respuesta personalizada que se enviará automáticamente.

   * **[!UICONTROL Exclusión parcial]**: habilite esta opción para enviar una respuesta automática cuando se detecte una palabra clave de exclusión cercana a la coincidencia.

   ![](assets/webhook-sinch-2.png){zoomable="yes"}

1. Escriba un **[!UICONTROL mensaje de respuesta predeterminado]** que se enviará automáticamente cuando un mensaje entrante no coincida con ninguna palabra clave o categoría configurada.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar su webhook.

1. En el menú de **[!UICONTROL Webhooks]**, haz clic en el ![icono de bin](assets/do-not-localize/Smock_Delete_18_N.svg) para eliminar tu webhook.

1. Para modificar la configuración existente, busque el webhook deseado y haga clic en la opción **[!UICONTROL Editar]** para realizar los cambios necesarios.

1. Acceda y copie su nueva **[!UICONTROL URL de webhook]** desde el **[!UICONTROL webhook]** que envió anteriormente.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Después de crear y configurar las opciones de entrada para el webhook, debes crear una [configuración de canal](sms-configuration-surface.md) para los mensajes SMS.

Una vez configuradas, puede aprovechar todas las funcionalidades de canal integradas, como la creación de mensajes, la personalización, el seguimiento de vínculos y la creación de informes.

>[!TAB Twilio]

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]**, seleccione el menú **[!UICONTROL Webhooks de SMS]** en **[!UICONTROL Configuración de SMS]** y haga clic en el botón **[!UICONTROL Crear webhook]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Configure las opciones de webhook, tal y como se detalla a continuación:

   * **[!UICONTROL Nombre]**: escribe un nombre para tu webhook.

   * **[!UICONTROL Seleccionar proveedor de SMS]**: Twilio.

   * **[!UICONTROL Tipo]**: Entrante.

   * **[!UICONTROL Credenciales de API]**: elija en la lista desplegable sus [credenciales de API configuradas anteriormente](sms-configuration-twilio.md#create-api).

   * **[!UICONTROL Número de teléfono del remitente]**: escribe el número de teléfono del remitente &#x200B;que quieras usar para tus comunicaciones.

1. Haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar sus categorías de palabras clave y, a continuación, configúrelas según su proveedor de SMS:

   * **[!UICONTROL Categoría de palabras clave entrantes]**: elige las categorías de palabras clave **[!UICONTROL Inclusión]**, **[!UICONTROL Exclusión]**, **[!UICONTROL Inclusión doble]**, **[!UICONTROL Ayuda]** o **[!UICONTROL Personalizada]**.

   * **[!UICONTROL Escriba una palabra clave]**: escriba las palabras clave predeterminadas o personalizadas que almacenarán automáticamente en déclencheur el mensaje. Haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar varias palabras clave.

     Para **[!UICONTROL palabra clave personalizada]**, use palabras clave no relacionadas con el consentimiento para acciones basadas en lotes dentro de un recorrido.

   * **[!UICONTROL Mensaje de respuesta]**: seleccione en la lista desplegable la respuesta personalizada que se enviará automáticamente.

   * **[!UICONTROL Exclusión parcial]**: habilite esta opción para enviar una respuesta automática cuando se detecte una palabra clave de exclusión cercana a la coincidencia.

1. Escriba un **[!UICONTROL mensaje de respuesta predeterminado]** que se enviará automáticamente cuando un mensaje entrante no coincida con ninguna palabra clave o categoría configurada.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar su webhook.

1. En el menú de **[!UICONTROL Webhooks]**, haz clic en el ![icono de bin](assets/do-not-localize/Smock_Delete_18_N.svg) para eliminar tu webhook.

1. Para modificar la configuración existente, busque el webhook deseado y haga clic en la opción **[!UICONTROL Editar]** para realizar los cambios necesarios.

1. Acceda y copie su nueva **[!UICONTROL URL de webhook]** desde el **[!UICONTROL webhook]** que envió anteriormente.

Después de crear y configurar las opciones de entrada para el webhook, debes crear una [configuración de canal](sms-configuration-surface.md) para los mensajes SMS.

Una vez configuradas, puede aprovechar todas las funcionalidades de canal integradas, como la creación de mensajes, la personalización, el seguimiento de vínculos y la creación de informes.


>[!ENDTABS]


## Vídeo práctico {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)

