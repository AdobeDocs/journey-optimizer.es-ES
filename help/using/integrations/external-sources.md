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
hidefromtoc: true
exl-id: 104f283e-f6a5-431b-919a-d97b83d19632
source-git-commit: ad5fdefed71d75470dc243310e74372e0b08ba2a
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 1%

---

# Trabajo con integraciones {#external-sources}

## Información general

La característica **Integraciones** permite la integración perfecta de fuentes de datos de terceros en Adobe Journey Optimizer. Esta función optimiza la integración de fuentes de contenido y datos externos en las campañas, lo que le permite ofrecer mensajes dinámicos y altamente personalizados en varios canales.

Puede utilizar esta función para acceder a datos externos y extraer contenido de herramientas de terceros, como:

* **Puntos de recompensa** de sistemas de fidelidad.
* **Información de precio** para productos.
* **Recomendaciones de productos** de motores de recomendación.
* A **Actualizaciones de logística** les gusta el estado de entrega.

## Configuración de la integración {#configure}

Como administrador, puede configurar integraciones externas siguiendo estos pasos:

1. Vaya a la sección **[!UICONTROL Configuraciones]** del menú de la izquierda y haga clic en **[!UICONTROL Administrar]** desde la tarjeta **[!UICONTROL Integraciones]**.

   A continuación, haga clic en **[!UICONTROL Crear integración]** para iniciar una nueva configuración.

   ![](assets/external-integration-config-1.png)

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

1. Con el campo **[!UICONTROL Carga de respuesta]**, puede decidir qué campos de la salida de ejemplo se deben utilizar para la personalización de mensajes.

   Haga clic en el icono ![edit](assets/do-not-localize/Smock_Edit_18_N.svg) y pegue una carga útil de respuesta JSON de muestra para detectar automáticamente los tipos de datos.

1. Elija los campos que desea exponer para la personalización y especifique sus tipos de datos correspondientes.

   ![](assets/external-integration-config-5.png)

1. Use **[!UICONTROL Enviar conexión de prueba]** para validar la integración.

   Una vez validado, haga clic en **[!UICONTROL Activar]**.

## Uso de integraciones externas para la personalización {#personalization}

Como experto en marketing, puede utilizar integraciones configuradas para personalizar el contenido. Siga estos pasos:

1. Acceda al contenido de su campaña y haga clic en **[!UICONTROL Agregar personalización]** desde su **[!UICONTROL Componentes]** de texto o HTML.

[Más información sobre los componentes](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Vaya a la sección **[!UICONTROL Integraciones]** y haga clic en **[!UICONTROL Abrir integraciones]** para ver todas las integraciones activas.

   ![](assets/external-integration-content-2.png)

1. Seleccione una integración y haga clic en **[!UICONTROL Guardar]**.

   ![](assets/external-integration-content-3.png)

1. Habilite el modo **[!UICONTROL Pills]** para desbloquear el menú de integración avanzada.

   ![](assets/external-integration-content-4.png)

1. Para completar la configuración de la integración, defina los atributos de la integración, que se especificaron anteriormente durante [configuración](#configure).

   Puede asignar valores a estos atributos mediante valores estáticos, que permanecen constantes, o atributos de perfil, que extraen información de forma dinámica de los perfiles de usuario.

   ![](assets/external-integration-content-5.png)

1. Una vez definidos los atributos de integración, ahora puede usar los campos de integración en el contenido para mensajes personalizados haciendo clic en el icono ![agregar](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

1. Haga clic en **[!UICONTROL Guardar]**.

La personalización de la integración ahora se aplica correctamente al contenido, lo que garantiza que cada destinatario reciba una experiencia relevante y adaptada en función de los atributos que haya configurado.

![](assets/external-integration-content-7.png)
