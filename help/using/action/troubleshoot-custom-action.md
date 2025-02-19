---
solution: Journey Optimizer
product: journey optimizer
title: Solución de problemas de acciones personalizadas
description: Obtenga información sobre cómo solucionar problemas de una acción personalizada
badge: label="Disponibilidad limitada"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: acción, terceros, personalizado, recorrido, API
source-git-commit: d7ef9cb8b74781d5c711bd2958070767735a3b24
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 2%

---


# Solución de problemas de acciones personalizadas {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Esta capacidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.
>

Puede probar las acciones personalizadas enviando llamadas a la API desde la sección de administración de la interfaz de usuario de Journey Optimizer. Esta capacidad le ayuda a solucionar problemas de las acciones personalizadas antes o después de utilizarlas en un recorrido.

Como administrador, use la capacidad **[!UICONTROL Enviar solicitud de prueba]** para validar las configuraciones de acción personalizadas realizando llamadas de API reales directamente desde Adobe Journey Optimizer. Esta función garantiza que la estructura de solicitud, los encabezados, la autenticación y la carga útil tengan el formato correcto antes de utilizarse en un recorrido.

![](assets/send-test-request.png){width="70%" align="left"}

Utilice esta capacidad para optimizar el proceso de prueba y validación, asegurándose de que las acciones personalizadas funcionen correctamente en los recorridos activos.

## Requisitos previos {#troubleshoot-custom-action-prereq}

Para usar la capacidad **[!UICONTROL Enviar solicitud de prueba]**, se debe preconfigurar una **acción personalizada** con una dirección URL, encabezados y configuración de autenticación.

Para que los administradores utilicen esta capacidad, se requieren los siguientes permisos:

* Los usuarios deben tener el permiso **[!DNL Manage journeys events, data sources and actions]**.
* Este permiso está incluido en el rol *Administradores de Recorrido*.
* El permiso **[!DNL View journeys events]** no es suficiente.

Obtenga más información acerca de los permisos de recorrido en [esta sección](../administration/high-low-permissions.md#journey-capability).

## Cómo utilizar la función Enviar solicitud de prueba {#troubleshoot-custom-action-use}

Para probar una acción personalizada, siga estos pasos:

1. Vaya a la pantalla de configuración **Acciones personalizadas** y seleccione una acción personalizada.
1. Haga clic en el botón **[!UICONTROL Enviar solicitud de prueba]** en la parte inferior de la pantalla de configuración de la acción.

![Enviar botón de solicitud de prueba en el panel de configuración de acción](assets/test-request.png){width="70%" align="left"}

1. En la ventana emergente, que permite especificar los parámetros de la solicitud:

   * Si el método de acción personalizada **es GET**, no se requiere carga útil.
   * Si el método de acción personalizada **es POST**, debe proporcionar una carga útil JSON.

     >[!NOTE]
     >
     >Adobe Journey Optimizer generará un error si la estructura de este JSON es incorrecta, pero no lo hará si hay una discrepancia con un tipo de datos. Por ejemplo, no habrá ningún error si se utiliza un parámetro entero para lo que debería ser una cadena.

   * Si se define la autenticación, se le pedirá que introduzca los detalles de autenticación.

1. Haga clic en **Enviar** para ejecutar la solicitud.
1. La respuesta de la API, incluidos los encabezados y los códigos de estado, se muestra en la interfaz.

## Gestión de autenticación {#troubleshoot-custom-action-auth}

Cuando una acción personalizada incluye autenticación, Adobe Journey Optimizer requiere que el usuario introduzca los detalles de autenticación para cada solicitud de prueba:

* **Autenticación básica:** El usuario debe proporcionar la *contraseña*.
* **Autenticación de clave API:** El usuario debe escribir la clave API *value*.
* **Autenticación personalizada:** El usuario debe proporcionar los parámetros de autenticación en la solicitud *bodyParam*. En este caso se agregan dos secciones para completar: **Solicitud de autenticación** y **Respuesta de autenticación**.

## Ventajas principales {#troubleshoot-custom-action-benefits}

Como administrador de Journey Optimizer, también puede utilizar herramientas externas (por ejemplo, Postman) para probar las acciones personalizadas. A continuación se enumeran las ventajas clave de la capacidad de resolución de problemas en el producto en comparación con una prueba externa:

* **Recorrido de AJO** ejecuta la solicitud de prueba, lo que significa que:

   * Se utiliza la estructura exacta de la solicitud (incluidos los encabezados específicos de Adobe Journey Optimizer).
   * La IP de origen y los encabezados coinciden con los utilizados en los recorridos activos.

* La capacidad **[!UICONTROL Enviar solicitud de prueba]** se puede usar para solucionar problemas de **recorridos activos**, ya que la acción personalizada ya está implementada.

* Esta capacidad de prueba en el producto elimina la necesidad de copiar manualmente los detalles de configuración entre las herramientas, lo que reduce el riesgo de errores.

## Resolución de problemas {#troubleshoot-custom-action-check}

Si la solicitud falla, puede comprobar lo siguiente:

* Las credenciales de autenticación introducidas en la prueba.
* El método de solicitud (GET frente a POST) y la carga útil correspondiente.
* El extremo y los encabezados de la API definidos en la acción personalizada.
* Utilice los datos de respuesta para identificar posibles errores de configuración.

