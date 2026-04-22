---
solution: Journey Optimizer
product: journey optimizer
title: Cifrar parámetros de URL
description: Aprenda a cifrar parámetros de consulta de URL confidenciales para que PII no se exponga en texto sin formato en los vínculos de seguimiento y las páginas de aterrizaje de Journey Optimizer.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
badge: label="Disponibilidad limitada" type="Informative"
keywords: cifrado, URL, seguimiento, página de aterrizaje, registro de claves, personalización, seguridad, privacidad, zona protegida
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
source-git-commit: 1039daee3b328828361976513cc4d1ba5ce1169a
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 2%

---

# Cifrar parámetros de URL {#url-parameter-encryption}

>[!AVAILABILITY]
>
>Esta función está disponible con disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.
>
>Actualmente, esta funcionalidad solo está disponible para el canal de correo electrónico.

## ¿Por qué utilizar el cifrado de parámetros de URL? {#why-url-parameter-encryption}

Los vínculos de seguimiento personalizados y las direcciones URL de páginas de aterrizaje suelen incluir atributos de perfil, identificadores, tokens u otros valores en la cadena de consulta. Estos parámetros suelen ser visibles como texto sin formato en el correo electrónico o SMS, y se pueden leer si alguien copia, comparte o marca el vínculo. Esto puede suponer un riesgo para la seguridad y la privacidad cuando los valores de pueden incluir información de identificación personal (PII) u otros datos confidenciales que deban proteger.

[!DNL Journey Optimizer] provides an encryption helper in the personalization editor so you can encrypt any expression value at render time (for example a profile attribute, a token, or a string you built from several fields). Encryption always requires a key from your organization&#39;s registry.

You encrypt only the query parameters you choose, using keys that administrators manage in a sandbox-level registry, so confidential values are not left exposed in clear text when the link is shared or inspected.

### Funcionamiento {#how-it-works}

* **Administrators** use the key registry to [create keys](#create-keys) and [manage keys](#manage-keys) in accordance with your organization&#39;s security policies.
* **Marketers** insert the `Encrypt` helper in the personalization editor and pass the value to protect plus an active key identifier from the registry. For syntax and options, see [this section](functions/helpers.md#url-parameter-encryption-helper).

>[!IMPORTANT]
>
>Decryption is your organization&#39;s responsibility. [!DNL Journey Optimizer] encrypts values when the message is rendered. Your website, app, or API must decrypt parameters using the same cryptographic material and processes you define—consistent with your security model.

### Ejemplo

A landing page URL might use a query parameter such as `token` whose value is a string token (for example a JSON payload with offer or profile identifiers). Without encryption, that string token is visible as plain text in the link. Wrapping that value with the encryption helper replaces the sensitive payload with ciphertext in the URL while leaving the rest of the link unchanged.

## Creación de claves {#create-keys}

Antes de poder utilizar el asistente de cifrado de parámetros de URL, debe crear una clave. Para ello, siga los pasos que aparecen a continuación.

>[!NOTE]
>
>Actualmente no hay permisos específicos para acceder y administrar claves. Las funciones que conceden acceso a la sección **[!UICONTROL Configuraciones]** en **[!UICONTROL Administración]** también conceden acceso al registro de claves. Sin embargo, se han planificado permisos específicos para una versión futura.

<!--
>[!IMPORTANT]
>
>To access and manage keys, you you must have the **View Key Registry** and **Manage Key Registry** permissions granted. [Learn more](../administration/high-low-permissions.md)
-->

1. Go to **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**.

1. Haga clic en el botón **[!UICONTROL Administrar]** para abrir el **[!UICONTROL Registro de claves]**.

   ![Sección de registro de claves en el menú Administración](assets/encryption-key-registry.png){width="80%"}

1. Con el botón específico, cree las claves que sean necesarias para su organización.

   ![Botón Crear clave en la sección Registro de claves](assets/encryption-create-key.png){width="80%"}

1. Asígneles una etiqueta clara o un identificador al que sus equipos puedan hacer referencia en el editor de personalización.

   ![Key details in Key registry section](assets/encryption-key-details.png){width="80%"}

1. Click **[!UICONTROL Submit]** to confirm your changes.

Once a key is created, marketers can use the [URL parameter encryption](functions/helpers.md#url-parameter-encryption-helper) helper in the personalization editor to encrypt specific values that they place in URL query parameters.

## Manage keys {#manage-keys}

To manage keys, follow the steps below.

1. Access the **[!UICONTROL Key registry]**. You can see all the keys created for the current sandbox in a list view.

   ![Key registry list view](assets/encryption-key-registry-list.png){width="100%"}

1. Click a key with the **[!UICONTROL Active]** status to open the key details.

   ![Active key details](assets/encryption-key-active-details.png){width="80%"}

1. Click the **[!UICONTROL Revoke]** button to permanently disable the key for new encryption.

   Once a key is revoked, attempts to use it in the helper should fail at render time. Las entradas revocadas permanecen visibles para la auditoría; es posible que los equipos necesiten el material correspondiente para descifrar cargas útiles antiguas en sus propios sistemas.

1. Haga clic en el botón **[!UICONTROL Rotar]** para proporcionar nuevo material de clave y, al mismo tiempo, mantener un identificador de clave estable donde los recorridos y campañas ya hacen referencia a él.

   El material anterior se conserva en el Registro con un estado revocado y un motivo apropiado (por ejemplo, una marca de tiempo de rotación), y una nueva fila o versión refleja la clave activa.

   >[!NOTE]
   >
   >Solo se deben seleccionar claves activas para cifrar los nuevos valores en el editor de personalización. No utilice claves revocadas para el contenido nuevo.

