---
solution: Journey Optimizer
product: journey optimizer
title: Habilitar integraciones externas
description: Integre integraciones externas en el proceso de creación de canales para enriquecer el contenido con información personalizada y dinámica
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: integración
hide: true
exl-id: 104f283e-f6a5-431b-919a-d97b83d19632
source-git-commit: f40e030e7d14120cdbc118a8f93e2f752d713f6b
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 7%

---

# Trabajo con integraciones {#external-sources}

>[!BEGINSHADEBOX]

Tabla de contenido:

* **[Trabajar con integraciones](integrations.md)**
* [Introducción](vendor-integration-gs.md)
* [Proveedores disponibles](vendor-integration.md)
* [Preguntas más frecuentes](vendor-integration-faq.md)

>[!ENDSHADEBOX]

## Información general

La característica **Integraciones** vincula Adobe Journey Optimizer con sistemas de terceros cuyos datos y contenido maquetable ya administra en otro sitio. Puede que aparezca ese material durante la creación y en el momento de envío, lo que admite experiencias más adaptables y personalizadas en los canales que utiliza en Journey Optimizer.

Puede utilizar esta función para acceder a datos externos y extraer contenido de herramientas de terceros, como:

* **Puntos de recompensa** de sistemas de fidelidad.
* **Información de precio** para productos.
* **Recomendaciones de productos** de motores de recomendación.
* A **Actualizaciones de logística** les gusta el estado de entrega.

Para empezar a usar integraciones, es necesario que se concedan a los usuarios los permisos **[!UICONTROL Administrar configuración de integración de AJO]** y **[!UICONTROL Ver integración de AJO]**. [Más información sobre los permisos](../administration/permissions.md)

+++ Obtenga información sobre cómo asignar permisos relacionados con integraciones

1. En el producto **[!UICONTROL Permisos]**, vaya a la pestaña **[!UICONTROL Funciones]** y seleccione la **[!UICONTROL Función]** que desee.

1. Haga clic en **[!UICONTROL Editar]** para modificar los permisos.

1. Agregue el recurso **[!UICONTROL Configuración de la integración de AJO]** y, a continuación, seleccione los permisos de integraciones correspondientes en el menú desplegable.

   ![](assets/external-integration-config-9.png)

1. Haga clic en **[!UICONTROL Guardar]** para aplicar los cambios.

   Los permisos de los usuarios que ya estén asignados a esta función se actualizarán automáticamente.

1. Para asignar esta función a nuevos usuarios, vaya a la pestaña **[!UICONTROL Usuarios]** en el panel de control **[!UICONTROL Funciones]** y haga clic en **[!UICONTROL Añadir usuario]**.

1. Introduzca el nombre del usuario y su dirección de correo electrónico, o selecciónelo en la lista, y haga clic en **[!UICONTROL Guardar]**.

Si el usuario no se creó anteriormente, consulte [esta documentación](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Configuración de la integración {#configure}

>[!AVAILABILITY]
>
> Esta función de integración está restringida a los canales salientes (correo electrónico, SMS y push) y proporciona datos en los formatos JSON o HTML. Tenga en cuenta que la API es de solo lectura, solo admite operaciones de recuperación.

Como administrador, puede configurar integraciones externas siguiendo estos pasos:

1. Vaya a la sección **[!UICONTROL Configuraciones]** del menú de la izquierda y haga clic en **[!UICONTROL Administrar]** desde la tarjeta **[!UICONTROL Integraciones]**.

   A continuación, haga clic en **[!UICONTROL Crear integración]** para iniciar una nueva configuración.

   ![](assets/external-integration-config-1.png)

1. Opcionalmente, pegue un comando **cURL** para rellenar automáticamente la dirección URL, el método HTTP, los encabezados y los parámetros de consulta.

1. Proporcione un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** para su integración.

   >[!NOTE]
   >
   >Estos campos no pueden contener espacios.

1. Escriba el extremo de API **[!UICONTROL URL]**, que puede incluir parámetros de ruta de acceso con variables que se pueden definir mediante etiquetas y valores predeterminados.

1. Configure la **[!UICONTROL plantilla de ruta]** con **[!UICONTROL Nombre]** y **[!UICONTROL Valor predeterminado]**.

   ![](assets/external-integration-config-2.png)

1. Seleccione el **[!UICONTROL método HTTP]** entre GET y POST.

1. Haga clic en **[!UICONTROL Agregar encabezado]** o en **[!UICONTROL Agregar parámetros de consulta]** según sea necesario para la integración. Proporcione los siguientes detalles para cada parámetro:

   * **[!UICONTROL Parámetro]**:: Identificador único usado internamente para hacer referencia al parámetro.

   * **[!UICONTROL Nombre]**: El nombre real del parámetro según lo esperado por la API.

   * **[!UICONTROL Tipo]**: elige **Constante** para un valor fijo o **Variable** para entrada dinámica.

   * **[!UICONTROL Valor]**: escriba el valor directamente para las constantes o seleccione una asignación de variables.

   * **[!UICONTROL Obligatorio]**: especifique si este parámetro es necesario.

   ![](assets/external-integration-config-3.png)

1. Elija un **[!UICONTROL tipo de autenticación]**:

   * **[!UICONTROL Sin autenticación]**: Para las API abiertas que no requieren credenciales.

   * **[!UICONTROL clave de API]**: autentique solicitudes con una clave de API estática. Escriba su **[!UICONTROL Nombre de clave API]**, **[!UICONTROL Valor de clave API]** y especifique su **[!UICONTROL ubicación]**.

   * **[!UICONTROL Autenticación básica]**: use la autenticación básica estándar de HTTP. Escriba **[!UICONTROL Nombre de usuario]** y **[!UICONTROL Contraseña]**.

   * **[!UICONTROL OAuth 2.0]**: realice la autenticación mediante el protocolo OAuth 2.0. Haga clic en el icono ![editar](assets/do-not-localize/Smock_Edit_18_N.svg) para configurar o actualizar la **[!UICONTROL carga útil]**.

   ![](assets/external-integration-config-4.png)

1. Establezca la **[!UICONTROL configuración de directiva]**, como el período de **[!UICONTROL tiempo de espera]** para las solicitudes de API, y elija habilitar la restricción, la caché o reintentar.

   Cuando la restricción está habilitada, las tasas admitidas varían de **50** TPS (mínimo) a **5000** TPS (máximo).
Cuando el reintento está habilitado, se producen otros errores después de **tres** reintentos de forma predeterminada, con **200 ms**, **400 ms** y **800 ms** entre intentos sucesivos.

1. Con el campo **[!UICONTROL Carga de respuesta]**, puede decidir qué campos de la salida de ejemplo se deben utilizar para la personalización de mensajes.

   Haga clic en el icono ![edit](assets/do-not-localize/Smock_Edit_18_N.svg) y pegue una carga útil de respuesta JSON de muestra para detectar automáticamente los tipos de datos.

1. Elija los campos que desea exponer para la personalización y especifique sus tipos de datos correspondientes.

   ![](assets/external-integration-config-5.png)

   >[!NOTE]
   >
   >La configuración **[!UICONTROL Carga de respuesta]** define la respuesta esperada para la creación, incluido cualquier esquema aplicado en ese paso. Los especialistas en marketing solo pueden hacer referencia a campos expuestos, los tokens de otras rutas no superan la validación en el editor.

1. Use **[!UICONTROL Enviar conexión de prueba]** para validar la integración.

   Una vez validado, haga clic en **[!UICONTROL Activar]**.

### Límites y comportamiento del tiempo de envío {#configure-send-time}

En el momento del envío, las respuestas de la API externa pueden ser de hasta **4 MB** de forma predeterminada. Cualquier elemento de mayor tamaño se trata como un error de integración y no se intentan **reintentos** cuando el error se debe al tamaño de la respuesta.

Las llamadas respetan la tasa de regulación **throttling** que configuró: las programaciones de Journey Optimizer intentan alcanzar ese límite incluso cuando el sistema externo está inactivo o devuelve errores. Si **cache** está habilitado, solo se almacenan y reutilizan **las respuestas correctas** hasta que la caché **TTL** que definió caduque; las respuestas con errores nunca se almacenan en caché.

Cada mensaje en cola también lleva un período de validez (TTL). Si el procesamiento se retrasa y un mensaje pasa por esa ventana, el sistema **lo descarta** y emite un evento **`MessageValidityExclusion`**, de modo que el trabajo obsoleto se borra de la cola y los recursos permanecen disponibles.


## Uso de integraciones externas para la personalización {#personalization}

Antes de utilizar integraciones externas para la personalización, tenga en cuenta que la programación y el aislamiento de las llamadas de integración dependen del contexto de ejecución:

* **Ejecución por lotes** (campañas por lotes, campañas orquestadas y campañas de marketing activadas por API): cada ejecución por lotes funciona en un entorno dedicado y aislado. Por lo tanto, las ejecuciones por lotes simultáneas que llaman a sistemas externos no compiten ni se obstruyen entre sí.

* **Ejecución unitaria** (recorridos unitarios, recorridos por lotes y campañas transaccionales activadas por API): el tráfico de integración está aislado por zona protegida de marca, por lo que una API externa lenta para una marca no retrasa a otra. Dentro de la zona protegida, las integraciones simultáneas pueden retrasar brevemente otros mensajes respaldados por integraciones; cada mensaje se intenta durante un máximo de 12 horas antes de la caducidad.

Como experto en marketing, puede utilizar integraciones configuradas para personalizar el contenido. Siga estos pasos:

1. Acceda al contenido de su campaña y haga clic en **[!UICONTROL Agregar personalización]** desde su **[!UICONTROL Componentes]** de texto o HTML.

   [Más información sobre los componentes](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Vaya a la sección **[!UICONTROL Integraciones]** y haga clic en **[!UICONTROL Abrir integraciones]** para ver todas las integraciones activas.

   Tenga en cuenta que los fragmentos de contenido están disponibles con las integraciones, pero solo admiten canales salientes; la publicación entrante no se realizará correctamente. Una vez publicado un fragmento, la adición y el guardado de nuevas integraciones están desactivados para evitar el impacto en los recorridos y campañas existentes.

   ![](assets/external-integration-content-2.png)

1. Seleccione una integración y haga clic en **[!UICONTROL Guardar]**.

   ![](assets/external-integration-content-3.png)

1. Habilite el modo **[!UICONTROL Pills]** para desbloquear el menú de integración avanzada.

   ![](assets/external-integration-content-4.png)

1. Al crear la personalización de la integración, el asistente de integraciones incluye un campo **`required`** que define cómo interactúan los errores o la falta de datos con el contenido predeterminado:

   * **`required=true`** (predeterminado): se detiene el procesamiento de ese mensaje. El envío se excluye con **`ExternalDataLookupExclusion`** y esa exclusión se registra en el **conjunto de datos de comentarios del mensaje**.
   * **`required=false`**: la variable de resultado se establece en **`null`** y el procesamiento continúa. Utilice texto predeterminado, reserva o lógica condicional en la plantilla para que los perfiles no reciban contenido vacío cuando la integración no devuelva datos.

     ![](assets/external-integration-content-8.png)

1. Para completar la configuración de la integración, defina los atributos de la integración, que se especificaron anteriormente durante [configuración](#configure).

   Puede asignar valores a estos atributos mediante valores estáticos, que permanecen constantes, o atributos de perfil, que extraen información de forma dinámica de los perfiles de usuario.

   ![](assets/external-integration-content-5.png)

1. Una vez definidos los atributos de integración, ahora puede usar los campos de integración en el contenido para mensajes personalizados haciendo clic en el icono ![agregar](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >Los tokens de la plantilla solo deben utilizar campos que el administrador exponga en la configuración de la integración. Por ejemplo, `{{weatherResponse.temperature}}` es válido cuando se expone `temperature`; `{{weatherResponse.humidity}}` se rechaza en el editor si `humidity` no se expuso.

1. Haga clic en **[!UICONTROL Guardar]**.

La personalización de la integración ahora se aplica correctamente al contenido, lo que garantiza que cada destinatario reciba una experiencia relevante y adaptada en función de los atributos que haya configurado.

![](assets/external-integration-content-7.png)

