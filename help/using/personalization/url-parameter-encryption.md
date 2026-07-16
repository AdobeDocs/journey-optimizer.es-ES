---
solution: Journey Optimizer
product: journey optimizer
title: Cifrar parámetros de URL
description: Aprenda a cifrar parámetros de consulta de URL confidenciales para que PII no se exponga en texto sin formato en los vínculos de seguimiento y las páginas de aterrizaje de Journey Optimizer.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
keywords: cifrado, URL, seguimiento, página de aterrizaje, registro de claves, personalización, seguridad, privacidad, zona protegida
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1348
ht-degree: 1%

---

# Cifrar parámetros de URL {#url-parameter-encryption}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a cifrar parámetros de consulta de URL confidenciales para que la información de identificación personal no se exponga en texto sin formato, incluido el modo en que los administradores crean, rotan y revocan claves en el registro de claves de zona protegida de Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Actualmente, esta funcionalidad solo está disponible para el canal de correo electrónico.

## ¿Por qué utilizar el cifrado de parámetros de URL? {#why-url-parameter-encryption}

Los vínculos de seguimiento personalizados y las direcciones URL de páginas de aterrizaje suelen incluir atributos de perfil, identificadores, tokens u otros valores en la cadena de consulta. Estos parámetros suelen ser visibles como texto sin formato en el correo electrónico o SMS, y se pueden leer si alguien copia, comparte o marca el vínculo. Esto puede suponer un riesgo para la seguridad y la privacidad cuando los valores de pueden incluir información de identificación personal (PII) u otros datos confidenciales que deban proteger.

[!DNL Journey Optimizer] proporciona un asistente de cifrado en el editor de personalización para que pueda cifrar cualquier valor de expresión en el momento del procesamiento (por ejemplo, un atributo de perfil, un token o una cadena que haya creado a partir de varios campos). El cifrado siempre requiere una clave del registro de su organización.

Solo se cifran los parámetros de consulta que se eligen mediante claves que los administradores administran en un registro de nivel de zona protegida, de modo que los valores confidenciales no quedan expuestos en texto no cifrado cuando se comparte o inspecciona el vínculo.

### Cómo funciona {#how-it-works}

* **Los administradores** utilizan el registro de claves para [crear claves](#create-keys) y [administrar claves](#manage-keys) de acuerdo con las políticas de seguridad de su organización.
* **Los especialistas en marketing** insertan el asistente `Encrypt` en el editor de personalización y pasan el valor que se va a proteger más un identificador de clave activa del Registro. Para ver la sintaxis y las opciones, vea [esta sección](functions/helpers.md#url-parameter-encryption-helper).

>[!IMPORTANT]
>
>El descifrado es responsabilidad de su organización. [!DNL Journey Optimizer] cifra los valores cuando se representa el mensaje. El sitio web, la aplicación o la API deben descifrar parámetros con el mismo material criptográfico y los mismos procesos definidos, de forma coherente con el modelo de seguridad.

### Ejemplo

Una dirección URL de página de aterrizaje puede utilizar un parámetro de consulta como `token`, cuyo valor es un token de cadena (por ejemplo, una carga útil JSON con identificadores de oferta o perfil). Sin cifrado, ese token de cadena es visible como texto sin formato en el vínculo. Al ajustar ese valor con el asistente de cifrado, se sustituye la carga útil confidencial por texto cifrado en la dirección URL, mientras que el resto del vínculo se mantiene sin cambios.

## Creación de claves {#create-keys}

Antes de poder utilizar el asistente de cifrado de parámetros de URL, debe crear una clave. Para ello, siga los pasos que aparecen a continuación.

>[!IMPORTANT]
>
>Para acceder y administrar claves, debe tener concedidos los permisos **Ver registro de claves** y **Administrar registro de claves**. [Más información](../administration/high-low-permissions.md#administration-permissions)

1. Vaya a **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**.

1. Haga clic en el botón **[!UICONTROL Administrar]** para abrir el **[!UICONTROL Registro de claves]**.

   ![Sección de registro de claves en el menú Administración](assets/encryption-key-registry.png){width="80%"}

1. Con el botón específico, cree las claves que sean necesarias para su organización.

   ![Botón Crear clave en la sección Registro de claves](assets/encryption-create-key.png){width="80%"}

1. Asígneles una etiqueta clara o un identificador al que sus equipos puedan hacer referencia en el editor de personalización.

   ![Detalles de clave en la sección de registro de claves](assets/encryption-key-details.png){width="80%"}

1. Haga clic en **[!UICONTROL Enviar]** para confirmar los cambios.

Una vez creada una clave, los especialistas en marketing pueden usar el [cifrado de parámetros de URL](functions/helpers.md#url-parameter-encryption-helper) del editor de personalización para cifrar valores específicos que colocan en parámetros de consulta de URL.

## Administrar claves {#manage-keys}

Para administrar claves, siga los pasos a continuación.

1. Obtenga acceso al **[!UICONTROL Registro de claves]**. Puede ver todas las claves creadas para la zona protegida actual en una vista de lista.

   ![Vista de lista de registro de claves](assets/encryption-key-registry-list.png){width="100%"}

1. Haga clic en una clave con el estado **[!UICONTROL Activo]** para abrir los detalles de la clave.

   ![Detalles de clave activa](assets/encryption-key-active-details.png){width="80%"}

1. Haga clic en el botón **[!UICONTROL Revocar]** para deshabilitar permanentemente la clave para el nuevo cifrado.

   Una vez revocada una clave, los intentos de utilizarla en el asistente deberían fallar en el momento del procesamiento. Las entradas revocadas permanecen visibles para la auditoría; es posible que los equipos necesiten el material correspondiente para descifrar cargas útiles antiguas en sus propios sistemas.

1. Haga clic en el botón **[!UICONTROL Rotar]** para proporcionar nuevo material de clave y, al mismo tiempo, mantener un identificador de clave estable donde los recorridos y campañas ya hacen referencia a él.

   El material anterior se conserva en el Registro con un estado revocado y un motivo apropiado (por ejemplo, una marca de tiempo de rotación), y una nueva fila o versión refleja la clave activa.

   >[!NOTE]
   >
   >Solo se deben seleccionar claves activas para cifrar los nuevos valores en el editor de personalización. No utilice claves revocadas para el contenido nuevo.

## Referencia rápida {#quick-reference}

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

>[!BEGINTABS]

>[!TAB Información general]

**TL;DR**

En esta página se explica cómo los administradores crean, rotan y revocan claves de cifrado en el registro de claves en el nivel de zona protegida de Journey Optimizer, lo que permite a los especialistas en marketing cifrar parámetros de consulta de URL confidenciales para que PII no se exponga en texto sin formato en los vínculos de seguimiento y páginas de aterrizaje.

**Intenciones**

* Comprenda por qué se necesita el cifrado de parámetros de URL (datos confidenciales y PII visibles en cadenas de consulta de texto sin formato)
* Crear claves de cifrado en el registro de claves de zona protegida (tarea de administración que requiere permisos específicos)
* Revocar una clave para deshabilitarla de forma permanente para el nuevo cifrado
* Rotar una clave para proporcionar nuevo material criptográfico manteniendo el mismo identificador
* Utilice el asistente `Encrypt` en el editor de personalización para proteger valores de parámetros de consulta específicos

>[!TAB Glosario]

* **Registro de claves**: Repositorio de nivel de zona protegida en Journey Optimizer (Administración > Configuraciones) donde los administradores crean y administran las claves de cifrado que usa el asistente de cifrado del parámetro de URL. *(específico del producto)*
* **Ayudante de cifrado (`Encrypt`)**: función de ayuda en el editor de personalización que cifra un valor de expresión en el momento del procesamiento y reemplaza PII por texto cifrado en los parámetros de consulta de URL. *(específico del producto)*
* **Revocar (clave)**: Acto de deshabilitar permanentemente una clave para el nuevo cifrado; la entrada de clave permanece visible en el Registro para la auditoría y las cargas más antiguas pueden seguir necesitándola para el descifrado en los sistemas de la organización.
* **Rotar (clave)**: El acto de proporcionar nuevo material criptográfico para una clave manteniendo estable su identificador, de modo que las campañas y recorridos que ya hacen referencia a esa clave no necesitan actualizarse.
* **PII (información de identificación personal)**: datos que pueden identificar a un individuo, como atributos de perfil, tokens o identificadores de oferta, que deben protegerse cuando se incluyen en los parámetros de consulta de URL.

>[!TAB Terminología]

* **Nombre canónico:** Cifrado de parámetro de URL — variantes: Cifrado de URL, cifrado de parámetro de consulta, ofuscación de parámetro de URL
* **Sinónimos:** &quot;Registro de claves&quot; = &quot;Registro de claves&quot; (etiqueta de interfaz de usuario en Administración > Configuraciones)
* **No confundir:** Revocar (deshabilita permanentemente la clave para el nuevo cifrado; la entrada permanece para la auditoría) ≠ Rotar (reemplaza el material criptográfico pero mantiene el mismo identificador de clave activo para el nuevo cifrado)

>[!TAB Protecciones y limitaciones]

* Actualmente, el cifrado de parámetros de URL solo está disponible para el canal de correo electrónico.
* Requiere los permisos de **Ver registro de claves** y **Administrar registro de claves** para obtener acceso a las claves y administrarlas.
* El descifrado es responsabilidad de la organización. Journey Optimizer cifra los valores en el momento del procesamiento; el sitio web, la aplicación o la API deben descifrar los parámetros utilizando el mismo material criptográfico y procesos definidos por la organización.
* Solo se deben utilizar claves activas para cifrar nuevos valores en el editor de personalización; las claves revocadas no se deben utilizar para el nuevo contenido.
* Las claves revocadas siguen estando visibles en el registro a efectos de auditoría; es posible que los sistemas de la organización las necesiten para descifrar cargas útiles antiguas.

>[!TAB Preguntas más frecuentes]

**Q: ¿Quién es el responsable del descifrado?**

El descifrado es responsabilidad de la organización. Journey Optimizer cifra los valores cuando se representa el mensaje. El sitio web, la aplicación o la API deben descifrar los parámetros de consulta utilizando el mismo material criptográfico y procesos que la organización ha definido.

**Q: ¿Cuál es la diferencia entre Revocar y Rotar?**

Revocar deshabilita permanentemente una clave para el nuevo cifrado, al tiempo que mantiene la entrada visible en el registro para auditoría (es posible que las cargas útiles más antiguas necesiten la clave para el descifrado en los sistemas de la organización). Rotate proporciona nuevo material criptográfico para una clave mientras mantiene el mismo identificador de clave, de modo que las campañas y recorridos que hacen referencia a ella siguen funcionando sin actualizaciones.

**Q: ¿Qué permisos se requieren para administrar claves?**

Permisos de **Ver registro de claves** y **Administrar registro de claves**.

**Q: ¿Qué canales admiten el cifrado de parámetros de URL?**

Actualmente solo el canal de correo electrónico.

**Q: ¿Se puede usar una clave revocada para el nuevo cifrado?**

No. Una vez revocada una clave, los intentos de utilizarla en el asistente de cifrado deberían fallar en el momento del procesamiento. No utilice claves revocadas para el contenido nuevo.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: c594ce24 -->
