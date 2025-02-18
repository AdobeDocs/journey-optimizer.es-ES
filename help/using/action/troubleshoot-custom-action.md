---
solution: Journey Optimizer
product: journey optimizer
title: Prueba de una acción personalizada
description: Obtenga información sobre cómo solucionar problemas de una acción personalizada
badge: label="Disponibilidad limitada"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: acción, terceros, personalizado, recorrido, API
source-git-commit: 5ce76bd61a61e1ed5e896f8da224fc20fba74b53
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 2%

---


# Solucionar problemas de acciones personalizadas {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Esta capacidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.
>

## Información general

La función **Enviar solicitud de prueba** permite a los administradores validar sus configuraciones de acción personalizadas realizando llamadas de API reales directamente desde Adobe Journey Optimizer (AJO). Esta función garantiza que la estructura de solicitud, los encabezados, la autenticación y la carga útil tengan el formato correcto antes de utilizarse en un recorrido.

![](assets/send-test-request.png){width="70%" align="left"}

## Requisitos previos

- **Se requiere acceso de administrador:**
   - Los usuarios deben tener el permiso **&quot;Administrar eventos de recorridos, fuentes de datos y acciones&quot;**.
   - Este permiso está incluido en el rol *Administradores de Recorrido*.
   - El permiso **&quot;Ver eventos de recorridos...&quot;** por sí solo no es suficiente.
- Se debe preconfigurar una **acción personalizada** con una dirección URL, encabezados y configuración de autenticación.

## Cómo utilizar la función Enviar solicitud de prueba

1. Vaya a la pantalla de configuración de **Acciones personalizadas**.
1. Haga clic en el botón **&quot;Enviar solicitud de prueba&quot;**.
1. Aparece una ventana emergente, que le permite especificar parámetros de solicitud:
   - Si el método de acción personalizada **es GET**, no se requiere carga útil.
   - Si el método de acción personalizada **es POST**, debe proporcionar una carga útil JSON.

     >[!NOTE]
     >
     >AJO generará un error si la estructura de este JSON es incorrecta, pero no lo hará si hay una discrepancia con un tipo de datos. Por ejemplo, no habrá ningún error si se utiliza un parámetro entero para lo que debería ser una cadena.

   - Si se define la autenticación, se le pedirá que introduzca los detalles de autenticación.

1. Haga clic en **Enviar** para ejecutar la solicitud.
1. La respuesta de la API, incluidos los encabezados y los códigos de estado, se muestra en la interfaz.

## Gestión de autenticación

Cuando una acción personalizada incluye autenticación, AJO requiere que el usuario introduzca los detalles de autenticación para cada solicitud de prueba:

- **Autenticación básica:** El usuario debe proporcionar la *contraseña*.
- **Autenticación de clave API:** El usuario debe escribir la clave API *value*.
- **Autenticación personalizada:** El usuario debe proporcionar los parámetros de autenticación en la solicitud *bodyParam*. En este caso se agregan dos secciones para completar: **Solicitud de autenticación** y **Respuesta de autenticación**.

## Diferencias clave de las herramientas de prueba externas (por ejemplo, Postman)

- **Recorrido de AJO** ejecuta la solicitud de prueba, lo que significa que:
   - Se utiliza la estructura exacta de la solicitud (incluidos los encabezados específicos de AJO).
   - La IP de origen y los encabezados coinciden con los utilizados en los recorridos activos.
- Se puede usar para solucionar problemas de **recorridos activos** donde la acción personalizada ya está implementada.
- Elimina la necesidad de copiar manualmente los detalles de configuración entre las herramientas, lo que reduce el riesgo de errores.

## Resolución de problemas

- Si la solicitud falla, compruebe lo siguiente:
   - Las credenciales de autenticación introducidas en la prueba.
   - El método de solicitud (GET frente a POST) y la carga útil correspondiente.
   - El extremo y los encabezados de la API definidos en la acción personalizada.
- Utilice los datos de respuesta para identificar posibles errores de configuración.

Esta función optimiza el proceso de prueba y validación, lo que garantiza que las acciones personalizadas funcionen correctamente en los recorridos de AJO activos.

