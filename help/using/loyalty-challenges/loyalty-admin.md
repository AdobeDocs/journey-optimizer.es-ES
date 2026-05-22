---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del programa de fidelización
description: Aprenda a configurar proveedores de recompensas, definiciones de eventos y configuraciones de nivel de organización para su programa de fidelidad en Adobe [!DNL Journey Optimizer].
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: 3d894653dd2ac1ddd10a8772da8d5cee21af9bca
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 0%

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

Use la configuración del programa de fidelización en [!DNL Journey Optimizer] para conectarse a los sistemas de fidelización externos. Los especialistas en marketing utilizan **[!UICONTROL Desafíos de fidelidad (Beta)]** para diseñar desafíos, tareas, contenido y mensajería. La configuración del programa de fidelización es un área independiente y solo de administrador para el cumplimiento de recompensas, la asignación de eventos, el inventario de productos y las exclusiones.

>[!NOTE]
>
>La configuración del programa de fidelización está destinada a administradores. Además de los permisos necesarios para los retos de fidelidad, necesita acceso de administrador a su instancia de [!DNL Journey Optimizer]. Póngase en contacto con el administrador de Adobe para solicitar acceso.

Para abrir la interfaz de configuración, vaya a **[!UICONTROL Fidelidad]** y seleccione **[!UICONTROL Administrador fiel]**. La interfaz está organizada en pestañas:

* **Configuración global**: establezca el área de nombres de identidad de Experience Platform. [Aprenda a configurar las opciones globales](#global-settings)
* **Proveedores de recompensas**: Conecte las API externas que cumplan las recompensas, incluidos los tipos de recompensas, los proxies y la autenticación. [Aprenda a configurar proveedores de recompensas](#reward-providers)
* **Definiciones de eventos**: asigne eventos de experiencia entrantes a actividades que pueda usar en **[!UICONTROL eventos personalizados]** tareas. [Aprenda a configurar definiciones de eventos](#event-definitions)
* **Inventario de productos**: cargue asignaciones de artículos a grupos para que pueda usar grupos de productos en las reglas de elegibilidad de tareas. [Aprenda a configurar el inventario de productos](#product-inventory)
* **Exclusiones**: cargue exclusiones de grupos y artículos de toda la organización que se apliquen cuando los especialistas en marketing configuren tareas. [Obtenga información sobre cómo configurar exclusiones](#exclusions)

## Configuración global {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Configuración global"
>abstract="Seleccione el área de nombres de identidad de Adobe Experience Platform para su programa de fidelidad."

Abra la ficha **[!UICONTROL Configuración global]**. Por ahora, la configuración principal disponible en esta pestaña es seleccionar el área de nombres de identidad de Adobe Experience Platform que usa su programa de fidelidad en la lista desplegable **[!UICONTROL Área de nombres]**.

![](assets/admin-global-settings.png)

➡️ [Aprenda a trabajar con áreas de nombres de identidad](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces){target="_blank"}

## Proveedores de recompensa {#reward-providers}

Un **proveedor de recompensas** indica a [!DNL Journey Optimizer] a dónde enviar las llamadas de cumplimiento cuando se registra el progreso del desafío o se completa un desafío; por ejemplo, una API que acredita puntos de lealtad o estrellas a una cuenta de miembro.
* **[!UICONTROL Definiciones de recompensa]**: los tipos de recompensa que este proveedor puede emitir (por ejemplo, estrellas o millas).
* **[!UICONTROL Proxies de recompensa]**: un proxy intermedio por el que se enrutan las llamadas en lugar del extremo directamente.
* **[!UICONTROL Generadores de tokens de autenticación]**: el mecanismo que usa [!DNL Journey Optimizer] para obtener tokens de acceso antes de llamar a su API.

Para crear un proveedor de recompensas, siga estos pasos:

1. Abra la pestaña **[!UICONTROL Proveedores de recompensas]** y seleccione **[!UICONTROL Crear proveedor de recompensas]**.

   ![](assets/admin-reward.png)

1. Escriba **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]**.

1. En el campo **[!UICONTROL URL]**, ingrese la URL de la API que recibe las solicitudes de cumplimiento.

1. Agregue **[!UICONTROL encabezados]** según sea necesario para su API (por ejemplo, claves de API o tipos de contenido).

1. Configure los siguientes recursos asociados a su proveedor de premios. Expanda cada sección para obtener más información:

   +++Definiciones de recompensa

   Una entrada por premio que es compatible con su proveedor (por ejemplo, puntos o estrellas del programa, crédito monetario). Para cada definición:

   * Proporcione un nombre y una descripción.
   * Especifique si la definición es **[!UICONTROL Habilitado]**.
   * Active la opción **![!UICONTROL Default]** para marcar una definición como predeterminada para este proveedor.
   * Especifique la **carga** enviada con las llamadas de cumplimiento.

   ![](assets/admin-reward-definition.png)

   +++

   +++Recompensar proxy

   Enruta las llamadas de cumplimiento a través de un servidor intermedio en lugar de directamente al extremo.

   * Proporcione un nombre y una descripción.
   * Escriba la información de **[!UICONTROL Host]**, **[!UICONTROL Puerto]**.
   * Especifique si el proxy está **[!UICONTROL Habilitado]**.
   * Agregue el proxy **[!UICONTROL Credential]**.

   ![](assets/admin-reward-proxies.png)

   +++

   +++Auth token generator

   Si la API requiere un token de portador para la autenticación.

   * Introduzca un nombre y una descripción.
   * En el campo Auth type, introduzca el tipo de autenticación (por ejemplo, Bearer).
   * Seleccione el método HTTP que desee utilizar (por ejemplo, POST).
   * Introduzca la URL de extremo de token. y agregue la **[!UICONTROL clave de token]** en la respuesta (por ejemplo, `access_token`).
   * Especifique si el generador de tokens de autenticación está **[!UICONTROL habilitado]**.
   * Añada los encabezados requeridos por el extremo del token si es necesario.

   [!DNL Journey Optimizer] utiliza esta configuración para obtener un token nuevo antes de llamar a su API de recompensa.

   ![](assets/admin-reward-auth.png)

   +++

1. Seleccione **[!UICONTROL Crear proveedor de recompensas]**. El proveedor y todos los recursos configurados se guardan juntos.

Después de guardar, el proveedor aparece en la lista de proveedores de recompensas. Los especialistas en marketing pueden seleccionar este proveedor al configurar las recompensas por desafío. [Aprenda a configurar las recompensas por desafío](create-challenges.md#rewards)

Para editar un proveedor de recompensas existente, abre la pestaña **[!UICONTROL Proveedores de recompensas]**, selecciona el proveedor y actualiza los campos correspondientes. Los cambios en los recursos secundarios (definiciones de recompensa, proxies, generadores de tokens de autenticación) se guardan al actualizarlos.

>[!NOTE]
>
>**[!UICONTROL Trae tus propios datos]** desafíos para lograr recompensas a través de tu propia integración de datos. Los proveedores de recompensas configurados aquí no se aplican a esos desafíos. [Aprenda a crear sus propios desafíos de datos](create-challenges.md#create-the-challenge)

## Definiciones de eventos {#event-definitions}

**[!UICONTROL Definiciones de eventos]** asignan eventos de experiencia de sus sistemas (por ejemplo, compras, registro de llegada en el hotel) a actividades en las que los Desafíos de fidelidad pueden actuar, especialmente **[!UICONTROL eventos personalizados]** tareas. Cuando llegan los eventos, [!DNL Journey Optimizer] utiliza estas definiciones para decidir si se deben procesar o no. Los eventos que no coinciden con ninguna definición se omiten.

Para crear una definición de evento, siga estos pasos:

1. Abra la ficha **[!UICONTROL Definiciones de eventos]** y cree una nueva definición.

   ![](assets/admin-event-definition.png)

1. Escriba un **[!UICONTROL Nombre]** para el evento (por ejemplo, `Coffee purchase`); este es el nombre que ven los especialistas en marketing al configurar una tarea de **[!UICONTROL Custom Event]**.

1. Especifique cómo [!DNL Journey Optimizer] reconoce el evento en las cargas entrantes. Proporcione una **[!UICONTROL ruta de identificador]**, un **[!UICONTROL identificador de esquema XDM]** o ambos:

   * **[!UICONTROL Ruta de acceso del identificador]**: ruta de acceso al campo que identifica el evento o miembro (por ejemplo, `data.memberId`). Utilícelo cuando haga coincidir eventos por valores en la carga útil.
   * **[!UICONTROL Valores de identificador]**: valores en la ruta de identificador que deben estar presentes para que coincida esta definición.
   * **[!UICONTROL ID de esquema XDM]**: ID del esquema XDM de Experience Platform para este tipo de evento. Utilícelo cuando los eventos se capturan en un esquema conocido.

1. Cuando las marcas envíen eventos en su propio formato JSON, pegue cadenas en **[!UICONTROL Esquema]** y **[!UICONTROL Transformador]** para que [!DNL Journey Optimizer] pueda identificar los datos, analizarlos y decidir si desea realizar el seguimiento.

   * **[!UICONTROL Esquema]**: cadena de validación para la carga útil entrante.
   * **[!UICONTROL Transformador]**: expresión de transformación (por ejemplo, JSONata) que asigna la carga útil al formato que espera Loyalty Challenges.

1. Guarde la definición del evento. Aparece en la lista **[!UICONTROL Definiciones de eventos]**. Ahora puede utilizarlo en desafíos. [Aprenda a crear desafíos](create-challenges.md)

## Inventario de productos {#product-inventory}

La pestaña **[!UICONTROL Inventario de productos]** le permite agrupar elementos de catálogo para que pueda segmentarlos en tareas sin enumerar todos los ID de artículo. Sube un **archivo CSV** que asigna cada identificador de elemento a uno o más **grupos de productos** (el mismo elemento puede aparecer en varios grupos). Después de la importación, estos grupos están disponibles cuando se configura la idoneidad de la tarea. [Aprenda a crear tareas](create-tasks.md)

Para cargar un archivo de inventario de productos, siga estos pasos:

1. Prepare un archivo CSV que asigne cada identificador de elemento a uno o varios grupos de productos. Expanda la sección siguiente para ver un ejemplo.

   +++Ejemplo de CSV del inventario de productos

   ![](assets/admin-inventory-csv.png)

   +++

1. Abra la ficha **[!UICONTROL Inventario de productos]**.

1. Haga clic en el botón **[!UICONTROL Cargar]** y seleccione el archivo CSV.

   ![](assets/admin-inventory-upload.png)

1. Revise el archivo importado en la lista de inventario. La lista muestra una fila por elemento. En la columna **[!UICONTROL Grupos incluidos en]**, verá todos los grupos de productos a los que pertenece ese elemento. Cada grupo aparece como una píldora (varias píldoras si el producto está en varios grupos).

   ![](assets/admin-inventory-imported.png)

1. Para ver todos los artículos de un grupo de productos, selecciona la píldora de ese grupo en la columna **[!UICONTROL Grupos incluidos en]** de cualquier fila. La vista de detalles del grupo muestra todos los elementos del grupo, no sólo el elemento de la fila seleccionada.

   ![](assets/admin-inventory-group.png)

1. Use **[!UICONTROL Cargar historial]** para ver cargas anteriores de archivos CSV.

## Exclusiones {#exclusions}

La pestaña **[!UICONTROL Exclusiones]** le permite definir elementos de catálogo y grupos que se excluyen en el programa de fidelidad sin enumerar todos los ID de elemento en cada tarea. Sube un **archivo CSV** que asigna cada identificador de elemento a uno o más **grupos de exclusión** (el mismo elemento puede aparecer en varios grupos). Después de la importación, esos elementos y grupos están disponibles en el generador de tareas: los elementos excluidos se marcan automáticamente y no se pueden incluir en una tarea; los grupos de exclusión solo se pueden agregar a la lista de exclusión de la tarea, no a la lista de inclusión. [Aprenda a definir elementos aptos y exclusiones en las tareas](create-tasks.md#eligible-items-exclusions)

Para cargar un archivo de exclusiones de productos, siga estos pasos:

1. Prepare un archivo CSV que asigne cada identificador de elemento a uno o varios grupos de exclusión. Expanda la sección siguiente para ver un ejemplo.

   +++Ejemplo de CSV de exclusiones

   ![](assets/admin-exclusions-csv.png)

   +++

1. Abra la ficha **[!UICONTROL Exclusiones]**.

1. Haga clic en el botón **[!UICONTROL Cargar]** y seleccione el archivo CSV.

   ![](assets/admin-exclusions-upload.png)

1. Revise el archivo importado en la lista de exclusiones. La lista muestra una fila por elemento. En la columna **[!UICONTROL Grupos incluidos en]**, verá todos los grupos de exclusión a los que pertenece el elemento. Cada grupo aparece como una píldora (varias píldoras si el producto está en varios grupos).

1. Para ver todos los elementos de un grupo de exclusión, seleccione la píldora de ese grupo en la columna **[!UICONTROL Grupos incluidos en]** de cualquier fila. La vista de detalles del grupo muestra todos los elementos del grupo, no sólo el elemento de la fila seleccionada.

1. Use **[!UICONTROL Cargar historial]** para ver cargas anteriores de archivos CSV.
