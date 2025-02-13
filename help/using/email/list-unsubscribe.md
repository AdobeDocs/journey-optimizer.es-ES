---
solution: Journey Optimizer
product: journey optimizer
title: Configurar cancelación de suscripción a lista
description: Obtenga información sobre cómo incluir la URL "Cancelar la suscripción" de un solo clic en el encabezado de los correos electrónicos al establecer la configuración del canal
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: ajustes, correo electrónico, configuración
exl-id: c6c77975-ec9c-44c8-a8d8-50ca6231fea6
source-git-commit: 8e8f2d9fd360438f692a5cf79359d3a64c1220be
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 31%

---

# Cancelar suscripción a lista{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

Al configurar un nuevo canal de correo electrónico, al [seleccionar un subdominio](email-settings.md#subdomains-and-ip-pools) de la lista, se muestra la opción **[!UICONTROL Habilitar cancelación de suscripción a una lista]**.

![](assets/preset-list-unsubscribe.png)

## Habilitar cancelación de suscripción a lista {#enable-list-unsubscribe}

Esta opción está habilitada de forma predeterminada para incluir una URL de cancelación de suscripción con un solo clic en el encabezado del correo electrónico, como por ejemplo:

![](assets/preset-list-unsubscribe-header.png)

>[!NOTE]
>
>Si deshabilita esta opción, no se mostrará la URL de cancelación de suscripción con un solo clic en el encabezado del correo electrónico.

El encabezado Cancelar la suscripción a una lista ofrece dos opciones, que están habilitadas de forma predeterminada a menos que desactive una o ambas:

![](assets/surface-list-unsubscribe.png){width="80%"}

* Una dirección **[!UICONTROL Mailto (cancelar la suscripción)]**, que es la dirección de destino a la que se dirigen las solicitudes de cancelación de suscripción para el procesamiento automático.

  En [!DNL Journey Optimizer], la dirección de correo electrónico para cancelar la suscripción es la dirección predeterminada **[!UICONTROL Mailto (cancelar la suscripción)]** mostrada en la configuración del canal, según el [subdominio seleccionado](#subdomains-and-ip-pools). <!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* La URL **[!UICONTROL Cancelar la suscripción con un solo clic]**, que de forma predeterminada es el encabezado de cancelación de suscripción de lista generado por la URL de exclusión con un solo clic, según el subdominio que haya establecido y configurado en la configuración de canal. <!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

Puede seleccionar **[!UICONTROL Nivel de consentimiento]** en la lista desplegable correspondiente. Puede ser específico del canal o de la identidad del perfil. Según esta configuración, cuando un usuario cancela la suscripción mediante la URL de cancelación de suscripción a la lista en el encabezado de un correo electrónico, el consentimiento se actualiza en [!DNL Adobe Journey Optimizer], ya sea en el nivel de canal o en el nivel de ID.

La función **[!UICONTROL Mailto (cancelar la suscripción)]** y la función **[!UICONTROL URL de cancelación de suscripción de un solo clic]** son opcionales.

Si no desea utilizar la URL de cancelación de suscripción de un solo clic generada predeterminada, puede desactivar la función. En el escenario donde la opción **[!UICONTROL Habilitar cancelación de suscripción a lista]** está activada y la función **[!UICONTROL URL de cancelación de suscripción de un solo clic]** está desactivada, si añade un [vínculo de no participación de un solo clic](../email/email-opt-out.md#one-click-opt-out) a un mensaje creado con esta configuración, el encabezado Cancelación de suscripción a lista recupera el vínculo de no participación de un solo clic que ha insertado en el cuerpo del correo electrónico y lo utiliza como valor de URL de cancelación de suscripción de un solo clic.

![](assets/preset-list-unsubscribe-opt-out-url.png)

>[!NOTE]
>
>Si no añade un vínculo de no participación de un solo clic al contenido del mensaje y la opción predeterminada **[!UICONTROL URL de cancelación de suscripción de un solo clic]** no está marcada en la configuración de canal, no se pasa ninguna dirección URL al encabezado del correo electrónico como parte del encabezado Cancelación de suscripción a lista.

Obtenga más información sobre cómo administrar las capacidades de cancelación de suscripción en sus mensajes en [esta sección](../email/email-opt-out.md#unsubscribe-header).

## Administrar datos de cancelación de suscripción externamente {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Definir cómo se administran los datos de cancelación de suscripción"
>abstract="**Adobe administrado**: usted administra los datos de consentimiento dentro del sistema de Adobe.<br>**Administrado por el cliente**: usted administra los datos de consentimiento en un sistema externo y no se actualiza ninguna sincronización de datos de consentimiento en el sistema de Adobe a menos que usted lo inicie."

>[!AVAILABILITY]
>
>Esta capacidad se lanza con disponibilidad limitada (LA) para un pequeño conjunto de clientes.

Si está administrando el consentimiento fuera de Adobe, seleccione la opción **[!UICONTROL Administrado por el cliente]** para escribir una dirección de correo electrónico de cancelación de suscripción personalizada y su propia URL de cancelación de suscripción con un solo clic.

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

>[!WARNING]
>
>Si usa la opción **[!UICONTROL Administrado por el cliente]**, Adobe no almacena datos de cancelación de suscripción o consentimiento. Con la opción **[!UICONTROL Administrado por el cliente]**, las organizaciones eligen utilizar un sistema externo y serán responsables de administrar sus datos de consentimiento en dicho sistema externo. No hay sincronización automática de datos de consentimiento entre el sistema externo y [!DNL Journey Optimizer]. Cualquier sincronización de datos de consentimiento, originada en el sistema externo para actualizar los datos de consentimiento de usuario en [!DNL Journey Optimizer], debe iniciarla la organización como una transferencia de datos para insertar los datos de consentimiento de nuevo en [!DNL Journey Optimizer].

### Configuración de la API de descifrado {#configure-decrypt-api}

Con la opción **[!UICONTROL Administrado por el cliente]** seleccionada, si introduce puntos de conexión personalizados y los utiliza en una campaña o recorrido, [!DNL Journey Optimizer] adjunta algunos parámetros específicos de perfil predeterminados al evento de actualización de consentimiento <!--sent to the custom endpoint -->cuando los destinatarios hacen clic en el vínculo Cancelar suscripción.

Estos parámetros se envían al extremo de forma cifrada. Por lo tanto, el sistema de consentimiento externo necesita implementar una API específica a través de [Adobe Developer](https://developer.adobe.com){target="_blank"} para descifrar los parámetros enviados por Adobe.

La llamada de GET para recuperar estos parámetros depende de la opción de cancelación de suscripción a List que esté usando: **[!UICONTROL URL de cancelación de suscripción de un clic]** o **[!UICONTROL Mailto (cancelación de suscripción)]**.

<!--To configure the API to send back the information to [!DNL Adobe Journey Optimizer] when a recipient has unsubscribed using the List unsubscribe option with custom endpoints, follow the steps below.-->

+++ URL de cancelación de suscripción de un clic

Con la opción **[!UICONTROL Cancelar la suscripción a la URL]** con un solo clic, al hacer clic en el vínculo Cancelar la suscripción se cancela directamente la suscripción del usuario.

La llamada de GET es la siguiente:

Punto final: https://platform.adobe.io/journey/imp/consent/decrypt

Parámetros de consulta:

* **params**: contiene la carga útil cifrada
* **pid**: ID de perfil cifrado

Estos dos parámetros se incluirán en el evento de actualización de consentimiento enviado a los extremos personalizados.

Requisitos de encabezado:

* x-api-key
* x-gw-ims-org-id
* authorization (token de usuario de su cuenta técnica)

+++

+++ Mailto (cancelar la suscripción)

Con la opción **[!UICONTROL Mailto (cancelar la suscripción)]**, al hacer clic en el vínculo Unsubscribe, se envía un correo electrónico rellenado previamente a la dirección de cancelación de suscripción especificada.

La llamada de GET es la siguiente:

Punto final: https://platform.adobe.io/journey/imp/consent/decrypt

Parámetros de consulta:

* **emailParams**: cadena que contiene los parámetros **params** (carga útil cifrada) y **pid** (ID de perfil cifrado).

Los parámetros **params** y **pid** se incluirán en el evento de actualización de consentimiento enviado a los extremos personalizados.

Requisitos de encabezado:

* x-api-key
* x-gw-ims-org-id
* authorization (token de usuario de su cuenta técnica)

+++
