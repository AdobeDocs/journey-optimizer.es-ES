---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del programa de fidelización
description: Aprenda a configurar proveedores de recompensas, definiciones de eventos y configuraciones de nivel de organización para su programa de fidelidad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: a4ad533e54f3692eb0483138a8cfd1cee0e77ba1
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 2%

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
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](../rn/releases.md).

En la sección **[!UICONTROL Administrador de fidelidad]** se configura la conexión de Journey Optimizer a los sistemas de fidelidad externos. Los especialistas en marketing utilizan **[!UICONTROL Desafíos de fidelidad (Beta)]** para diseñar desafíos, tareas, contenido y mensajería. **[!UICONTROL Administrador de fidelidad]** es un área separada y de solo administrador para el cumplimiento de recompensas, la asignación de eventos y el inventario de productos.

Cuando un cliente completa un desafío o alcanza un hito de recompensa, Journey Optimizer llama al proveedor de recompensas que configuró para entregar puntos u otras recompensas. La configuración de **[!UICONTROL Administrador de fidelización]** no afecta a la configuración del desafío **[!UICONTROL Contenido]**, **[!UICONTROL Mensajería]** o **[!UICONTROL Audiencia]**, que permanece bajo el control del experto en marketing.

## Lo que configura aquí frente a en Retos de fidelización {#scope}

| Área | Configurado en la administración de fidelización | Configurado en retos de fidelización |
|------|----------------------------|----------------------------------|
| API de satisfacción de recompensas | Sí, proveedores de recompensas | No: seleccionar proveedor e importes solamente |
| Asignación de eventos para actividades personalizadas | Sí: definiciones de eventos | No: seleccionar el nombre del evento en las tareas de eventos personalizados |
| Asignaciones de grupos de productos | Sí: inventario de productos | No: utilizar grupos al crear tareas de compra/gasto |
| Estructura, contenido y audiencia del desafío | No | Sí |

Adobe Journey Optimizer envía llamadas de cumplimiento a su proveedor de recompensas cuando los clientes obtienen recompensas. Su plataforma de fidelización es responsable de abonar la cuenta del miembro.

## Requisitos previos {#prerequisites}

**[!UICONTROL Administrador de fidelización]** está destinado a un número reducido de administradores por organización. Además de los permisos necesarios para [Desafíos de fidelidad](get-started.md#prerequisites), necesita acceso de administrador para su instancia de Journey Optimizer. Póngase en contacto con el administrador de Adobe para solicitar acceso.

## Acceso a administrador de fidelización {#access-loyalty-admin}

Para abrir **[!UICONTROL Administrador de fidelización]**, selecciónelo en el panel de navegación izquierdo de Journey Optimizer.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

**[!UICONTROL Administrador de fidelización]** está organizado en fichas: **[!UICONTROL Configuración global]**, **[!UICONTROL Proveedores de recompensas]**, **[!UICONTROL Definiciones de eventos]** y **[!UICONTROL Inventario de productos]**. Las pestañas disponibles dependen de los permisos de su organización y de la configuración de las funciones.

## Configuración global {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Configuración global"
>abstract="Seleccione el área de nombres de identidad de Adobe Experience Platform para su programa de fidelidad y copie su ID de configuración. Esta configuración a nivel de organización es necesaria para que los proveedores de recompensas puedan entregar las recompensas correctamente."

Use **[!UICONTROL Configuración global]** para configurar las opciones de toda la organización para los Desafíos de fidelidad.

1. Abra la ficha **[!UICONTROL Configuración global]**.

1. En la lista desplegable **[!UICONTROL Área de nombres]**, seleccione el [área de nombres de identidad](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces) que usa su programa de fidelidad.

1. Seleccione **[!UICONTROL Guardar]** para aplicar el área de nombres a la configuración de Retos de fidelidad.

1. Copie el **[!UICONTROL ID de configuración]** cuando necesite compartirlo con su equipo de implementación o sistemas externos; por ejemplo, al configurar la entrega de eventos entrantes.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Proveedores de recompensa {#reward-providers}

Un **proveedor de recompensas** le dice a Journey Optimizer dónde enviar llamadas de cumplimiento cuando se registra el progreso del desafío o se completa un desafío; por ejemplo, una API que acredita puntos de lealtad o estrellas a una cuenta de miembro.

Una configuración de proveedor de recompensas incluye:

* Detalles básicos de conexión (nombre, descripción, dirección URL de la API, encabezados)
* **[!UICONTROL Definiciones de recompensa]**: los tipos de recompensa que este proveedor puede emitir (por ejemplo, estrellas o millas)
* **[!UICONTROL Proxies de recompensa]** (opcional): un proxy intermedio por el que se enrutan las llamadas en lugar del extremo directamente
* **[!UICONTROL Generadores de tokens de autenticación]**: el mecanismo que utiliza Journey Optimizer para obtener tokens de acceso antes de llamar a su API.

### Crear un proveedor de recompensas {#create-reward-provider}

1. Abra la pestaña **[!UICONTROL Proveedores de recompensas]** y seleccione **[!UICONTROL Crear proveedor de recompensas]**.

1. Escriba un **[!UICONTROL Nombre]**, **[!UICONTROL Descripción]** y la **[!UICONTROL URL de la API]** que recibe las solicitudes de cumplimiento.

1. Agregue **[!UICONTROL encabezados]** según sea necesario para su API (por ejemplo, claves de API o tipos de contenido).

1. Configurar **[!UICONTROL definiciones de recompensa]**: una entrada por tipo de recompensa que admite su proveedor (por ejemplo, puntos de programa o estrellas). Para cada definición:

   * Especifique la **carga** enviada con las llamadas de cumplimiento.
   * Opcionalmente, marque una definición como **default** para este proveedor.

1. Si lo desea, configure un **[!UICONTROL proxy de recompensa]** para enrutar las llamadas de cumplimiento a través de un servidor intermedio:

   * **[!UICONTROL Nombre]**, **[!UICONTROL Descripción]** y si el proxy está **habilitado**
   * **[!UICONTROL Host]**, **[!UICONTROL Puerto]** y credenciales

1. Configure un **[!UICONTROL generador de tokens de autenticación]** si su API requiere un token de portador para la autenticación:

   * URL de extremo de token y método HTTP (por ejemplo, **POST** para flujos de estilo OAuth)
   * **[!UICONTROL Clave de token]** en la respuesta (por ejemplo, `access_token`)
   * Encabezados requeridos por el extremo del token

   Journey Optimizer utiliza esta configuración para obtener un token nuevo antes de llamar a su API de recompensa.

1. Seleccione **[!UICONTROL Crear proveedor de recompensas]**. El proveedor y todos los recursos secundarios configurados se guardan juntos.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Después de guardar, el proveedor aparece en la lista de proveedores de recompensas. Los especialistas en marketing seleccionan este proveedor al [configurar las recompensas por desafío](create-challenges.md#rewards).

Para editar un proveedor de recompensas existente, abre la pestaña **[!UICONTROL Proveedores de recompensas]**, selecciona el proveedor y actualiza los campos correspondientes. Los cambios en los recursos secundarios (definiciones de recompensa, proxies, generadores de tokens de autenticación) se guardan al actualizarlos.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>**[!UICONTROL Trae tus propios datos]** desafíos para lograr recompensas a través de tu propia integración de datos. Los proveedores de recompensas configurados aquí no se aplican a esos desafíos. [Más información sobre los desafíos que plantea el incorporar tus propios datos](create-challenges.md#create-the-challenge).

## Definiciones de eventos (opcional) {#event-definitions}

**[!UICONTROL Definiciones de eventos]** asignan eventos de experiencia de sus sistemas (en cualquier formato JSON o XDM que use su marca) a actividades en las que los Desafíos de fidelidad pueden actuar, especialmente **[!UICONTROL eventos personalizados]** tareas. Cuando llegan los eventos, Journey Optimizer utiliza estas definiciones para decidir si los procesa o no. Los eventos que no coinciden con ninguna definición se omiten.

### Creación de una definición de evento {#create-event-definition}

1. Abra la ficha **[!UICONTROL Definiciones de eventos]** y cree una nueva definición.

1. Escriba un **[!UICONTROL Nombre]** para el evento (por ejemplo, `Coffee purchase`); este es el nombre que ven los especialistas en marketing al configurar una tarea de **[!UICONTROL Custom Event]**.

1. Especifique cómo identificar el evento en las cargas útiles entrantes:

   * **[!UICONTROL Ruta de identificador]** — Ruta de acceso JSON al campo que identifica el evento o miembro (por ejemplo, `data.memberId`)
   * **[!UICONTROL Valores de identificador]**: valores que deben estar presentes para que esta definición coincida

1. Opcionalmente, especifique un **[!UICONTROL ID de esquema XDM]** si las cargas de evento se ajustan a un esquema de Experience Platform.

1. Opcionalmente, use los campos **[!UICONTROL Esquema]** y **[!UICONTROL Transformador]** para proporcionar cadenas de transformación y esquema personalizadas para analizar y validar el JSON entrante.

   Puede proporcionar un ID de esquema XDM, una ruta de identificador o ambos, según la estructura de los eventos.

1. Guarde la definición del evento.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

La mayoría de las organizaciones crean varias definiciones de eventos, una por cada actividad que desean rastrear (por ejemplo, compras, registros o visitas al sitio). [Aprenda a utilizar tareas de eventos personalizados en desafíos](create-tasks.md#choose-activity).

## Inventario de productos (opcional) {#product-inventory}

Use la ficha **[!UICONTROL Inventario de productos]** para cargar un archivo CSV que asigne identificadores de productos o artículos (por ejemplo, ID de MPG) a grupos de productos. Los especialistas en marketing pueden hacer referencia a estos grupos en las reglas de idoneidad de tareas en lugar de escribir los SKU individuales.

1. Abra la ficha **[!UICONTROL Inventario de productos]**.

1. Cargue el archivo de asignación.

1. Revise las asignaciones importadas en la lista de inventario. Seleccione un grupo de productos para ver todos los elementos de ese grupo o utilice la búsqueda para buscar elementos por nombre o ID.

1. Use **[!UICONTROL Historial de cargas]** para ver las cargas anteriores.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Exclusiones globales]** para el inventario de productos está planificado para una versión futura y no está documentado aquí.
