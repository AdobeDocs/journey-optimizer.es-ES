---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del programa de fidelización
description: Aprenda a configurar proveedores de recompensas, definiciones de eventos, inventario de productos, exclusiones y configuraciones de nivel de organización para su programa de fidelidad en Adobe [!DNL Journey Optimizer].
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: 9383220dd57f6a3ebfe67d0d1081b8834b524293
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 1%

---

# Configuración del programa de fidelización {#loyalty-admin}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md)
* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md)
* [Crear desafíos](create-challenges.md)
* [Creación de tareas](create-tasks.md)
* [Monitorización del rendimiento del desafío de fidelidad](loyalty-reporting.md)
* **Configurar el programa de fidelización** ◀︎ **Usted está aquí**
* [Referencia de API de retos de fidelización](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad en [!DNL Journey Optimizer], consulte [ciclo de lanzamiento](../rn/releases.md).

## Información general {#access-loyalty-admin}

La configuración del programa de fidelización conecta a [!DNL Journey Optimizer] con sus sistemas de fidelidad externos mediante la configuración del cumplimiento de recompensas, la asignación de eventos, el inventario de productos y las exclusiones antes de que los especialistas en marketing creen desafíos.

>[!NOTE]
>
>La configuración del programa de fidelización requiere acceso de administrador a su instancia de [!DNL Journey Optimizer], además de los permisos necesarios para los Desafíos de fidelización. Póngase en contacto con el administrador de Adobe para obtener acceso.

Para abrir la interfaz de configuración, vaya a **[!UICONTROL Fidelidad]** y seleccione **[!UICONTROL Administrador fiel]**. La interfaz está organizada en pestañas:

* **Configuración global**: seleccione el área de nombres de Experience Platform para su programa. [Aprenda a configurar las opciones globales](#global-settings)
* **Proveedores de recompensas**: conecte las API que cumplen las recompensas cuando los clientes progresan o completan desafíos. [Aprenda a configurar proveedores de recompensas](#reward-providers)
* **Definiciones de eventos**: asigne los eventos de experiencia entrantes a las actividades utilizadas en las tareas **[!UICONTROL Evento de AEP personalizado]**. [Aprenda a configurar definiciones de eventos](#event-definitions)
* **Inventario de productos** — Cargar asignaciones de artículos a grupos para usarlas en las reglas de elegibilidad de tareas. [Aprenda a configurar el inventario de productos](#product-inventory)
* **Exclusiones** — Cargar exclusiones de grupo y artículo de toda la organización para la configuración de tareas. [Obtenga información sobre cómo configurar exclusiones](#exclusions)

## Configuración global {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Configuración global"
>abstract="Seleccione el área de nombres de identidad de Adobe Experience Platform para su programa de fidelidad."

Abra la pestaña **[!UICONTROL Configuración global]** y seleccione el [área de nombres de identidad](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces) de Adobe Experience Platform para su programa de fidelidad en la lista desplegable **[!UICONTROL Área de nombres]**. Este área de nombres debe coincidir con la forma en que se identifican los perfiles de miembro en los datos.

![](assets/admin-global-settings.png)

➡️ [Aprenda a trabajar con áreas de nombres de identidad](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces){target="_blank"}

## Proveedores de recompensa {#reward-providers}

Un **proveedor de recompensas** le dice a [!DNL Journey Optimizer] a dónde enviar las llamadas de cumplimiento cuando se registra el progreso del desafío o se completa un desafío. Por ejemplo, una API que acredita puntos de lealtad o estrellas a una cuenta de miembro.

Para crear un proveedor de recompensas, siga estos pasos:

1. Abra la pestaña **[!UICONTROL Proveedores de recompensas]** y seleccione **[!UICONTROL Crear proveedor de recompensas]**.

   ![](assets/admin-reward.png)

1. Escriba un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]**.

1. En el campo **[!UICONTROL URL]**, introduzca el extremo de API que recibe las solicitudes de cumplimiento.

1. Agregue **[!UICONTROL encabezados]** según sea necesario para su API (por ejemplo, claves de API o tipos de contenido).

1. Configure los recursos asociados a su proveedor de recompensas. Expanda cada sección siguiente para ver los detalles de los campos:

   +++Definiciones de recompensa

   Añada una entrada por tipo de recompensa que admita su proveedor (por ejemplo, puntos de programa, estrellas o crédito monetario). Para cada definición:

   * Escriba un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]**.
   * Especifique si la definición es **[!UICONTROL Habilitado]**.
   * Cambie **[!UICONTROL Default]** para marcar una definición como predeterminada para este proveedor.
   * Defina la **carga útil** enviada con las llamadas de cumplimiento.

   ![](assets/admin-reward-definition.png)

   +++

   +++Recompensar proxy

   Enrute las llamadas de cumplimiento a través de un servidor intermedio en lugar de enviarlas directamente al extremo. En las pantallas del proveedor de recompensas y **[!UICONTROL Crear proxy]**, use el campo **[!UICONTROL Credenciales]** para la autenticación de proxy.

   * Escriba un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]**.
   * Escriba **[!UICONTROL Host]** y **[!UICONTROL Puerto]**.
   * Especifique si el proxy está **[!UICONTROL Habilitado]**.
   * En **[!UICONTROL Credenciales]**, escriba el nombre de usuario y la contraseña del proxy como JSON. El valor de las credenciales suele tener este aspecto:

     ```json
     { "userName": "test", "password": "xxxx" }
     ```

   ![](assets/admin-reward-proxies.png)

   +++

   +++Generador de tokens de autenticación

   Utilícelo cuando su API requiera un token de portador o una autenticación similar.

   * Escriba un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]**.
   * En **[!UICONTROL Tipo de autenticación]**, escriba el tipo de autenticación (por ejemplo, Portador).
   * Seleccione el método HTTP (por ejemplo, POST).
   * Escriba la dirección URL del extremo del token y la **[!UICONTROL clave de token]** en la respuesta (por ejemplo, `access_token`).
   * Especifique si el generador de tokens de autenticación está **[!UICONTROL habilitado]**.
   * Añada los encabezados que requiera el extremo de token.

   [!DNL Journey Optimizer] utiliza esta configuración para obtener un token nuevo antes de cada llamada a la API de recompensa.

   ![](assets/admin-reward-auth.png)

   +++

1. Seleccione **[!UICONTROL Crear proveedor de recompensas]**. El proveedor y todos los recursos configurados se guardan juntos.

Después de guardar, el proveedor aparece en la lista de proveedores de recompensas. Los especialistas en marketing pueden seleccionarlo al configurar las recompensas por desafío. [Aprenda a configurar las recompensas por desafío](create-challenges.md#rewards)

Para editar un proveedor de recompensas, abra la pestaña **[!UICONTROL Proveedores de recompensas]**, seleccione el proveedor y actualice los campos in situ. Los cambios en las definiciones de recompensa, los proxies y los generadores de tokens de autenticación se guardan automáticamente al actualizarlos.

>[!NOTE]
>
>**[!UICONTROL Trae tus propios datos]** desafíos para lograr recompensas a través de tu propia integración de datos. Los proveedores de recompensas configurados aquí no se aplican a esos desafíos. [Aprenda a crear sus propios desafíos de datos](create-challenges.md#create-the-challenge)

## Definiciones de eventos {#event-definitions}

**[!UICONTROL Las definiciones de eventos]** indican a [!DNL Journey Optimizer] qué eventos de experiencia de Adobe Experience Platform entrantes se deben procesar. Por ejemplo, una compra o un registro de entrada en el hotel. Los especialistas en marketing hacen referencia a estas definiciones cuando crean **[!UICONTROL tareas de evento de AEP personalizado]**. Los eventos que no coinciden con ninguna definición se omiten.

Cuando su organización envía eventos en su propio formato JSON, **[!UICONTROL Esquema]** y **[!UICONTROL Transformador]** ayudan a [!DNL Journey Optimizer] a validar la carga útil, analizarla y decidir si realizar el seguimiento de la actividad.

Para crear una definición de evento, siga estos pasos:

1. Abra la ficha **[!UICONTROL Definiciones de eventos]** y cree una nueva definición.

   ![](assets/admin-event-definition.png)

1. Escriba un **[!UICONTROL Nombre]** para el evento (por ejemplo, `Coffee purchase`). Los especialistas en marketing ven este nombre al configurar una tarea de **[!UICONTROL Custom AEP event]**.

1. Especifique cómo [!DNL Journey Optimizer] reconoce el evento en las cargas entrantes. Proporcione una **[!UICONTROL ruta de identificador]**, un **[!UICONTROL identificador de esquema XDM]** o ambos:

   * **[!UICONTROL Ruta de acceso del identificador]**: ruta de acceso a un campo de la carga útil (por ejemplo, `data.memberId`). Utilícelo cuando haga coincidir eventos por valores en la carga útil.
   * **[!UICONTROL Valores de identificador]**: valores en la ruta de identificador que deben estar presentes para que coincida esta definición.
   * **[!UICONTROL ID de esquema XDM]**: ID del esquema XDM de Experience Platform para este tipo de evento. Utilícelo cuando los eventos se capturan en un esquema conocido.

1. Si es necesario, pegue cadenas en **[!UICONTROL Schema]** y **[!UICONTROL Transformer]**:

   * **[!UICONTROL Esquema]**: cadena de validación para la carga útil entrante.
   * **[!UICONTROL Transformador]**: expresión de transformación (por ejemplo, JSONata) que asigna la carga útil al formato que espera Loyalty Challenges.

1. Guarde la definición del evento. Aparece en la lista **[!UICONTROL Definiciones de eventos]** y está disponible cuando los especialistas en marketing crean **[!UICONTROL eventos personalizados de AEP]** tareas. [Aprenda a crear tareas](create-tasks.md#choose-activity)

## Inventario de productos {#product-inventory}

La pestaña **[!UICONTROL Inventario de productos]** agrupa los elementos del catálogo para que los especialistas en marketing puedan asignarlos a tareas sin especificar cada ID de elemento. Cargue un **archivo CSV** que asigne cada identificador de elemento a uno o más **grupos de productos** (el mismo elemento puede pertenecer a varios grupos). Los grupos importados están disponibles al configurar la idoneidad de la tarea. [Aprenda a crear tareas](create-tasks.md)

Para cargar un archivo de inventario de productos, siga estos pasos:

1. Prepare un archivo CSV que asigne cada identificador de elemento a uno o varios grupos de productos. Expanda la sección siguiente para ver un ejemplo.

   +++Ejemplo de CSV del inventario de productos

   ![](assets/admin-inventory-csv.png)

   +++

1. Abra la ficha **[!UICONTROL Inventario de productos]**.

1. Seleccione **[!UICONTROL Cargar]** y elija su archivo CSV.

   ![](assets/admin-inventory-upload.png)

1. Revise los datos importados en la lista de inventario. La lista muestra una fila por elemento. La columna **[!UICONTROL Grupos incluidos en]** muestra cada grupo de productos para ese artículo como una píldora o varias píldoras cuando el artículo pertenece a varios grupos.

   ![](assets/admin-inventory-imported.png)

1. Para ver todos los elementos de un grupo de productos, selecciona la píldora de ese grupo en la columna **[!UICONTROL Grupos incluidos en]** de cualquier fila. La vista de detalles del grupo enumera todos los elementos del grupo.

   ![](assets/admin-inventory-group.png)

1. Abra **[!UICONTROL Historial de carga]** para ver las cargas de CSV anteriores.

## Exclusiones {#exclusions}

La pestaña **[!UICONTROL Exclusions]** define los elementos y grupos de catálogo que se excluyen en todo el programa, de modo que los especialistas en marketing no tienen que enumerar las mismas exclusiones en cada tarea. Cargue un **archivo CSV** que asigne cada identificador de elemento a uno o más **grupos de exclusión** (el mismo elemento puede pertenecer a varios grupos).

Después de la importación, los elementos y grupos excluidos aparecerán en el generador de tareas cuando los especialistas en marketing configuren **[!UICONTROL artículos y exclusiones aptos]**. [Aprenda a definir elementos aptos y exclusiones en las tareas](create-tasks.md#eligible-items-exclusions)

Para cargar exclusiones, siga estos pasos:

1. Prepare un archivo CSV que asigne cada identificador de elemento a uno o varios grupos de exclusión. Expanda la sección siguiente para ver un ejemplo.

   +++Ejemplo de CSV de exclusiones

   ![](assets/admin-exclusions-csv.png)

   +++

1. Abra la ficha **[!UICONTROL Exclusiones]**.

1. Seleccione **[!UICONTROL Cargar]** y elija su archivo CSV.

   ![](assets/admin-exclusions-upload.png)

1. Revise los datos importados en la lista de exclusiones. La lista muestra una fila por elemento. La columna **[!UICONTROL Grupos incluidos en]** muestra todos los grupos de exclusión de ese artículo en forma de píldora o de varias píldoras cuando el artículo pertenece a varios grupos.

<!-- SCREENSHOT: Exclusions list after CSV upload -->

1. Para ver todos los elementos de un grupo de exclusión, seleccione la píldora de ese grupo en la columna **[!UICONTROL Grupos incluidos en]** de cualquier fila. La vista de detalles del grupo enumera todos los elementos del grupo.

<!-- SCREENSHOT: Exclusion group details -->

1. Abra **[!UICONTROL Historial de carga]** para ver las cargas de CSV anteriores.
