---
solution: Journey Optimizer
product: journey optimizer
title: Administrar IP permitidas
description: Obtenga información sobre cómo configurar una lista de permitidos IP en Journey Optimizer para garantizar que todo el tráfico entrante a los vínculos alojados en Journey Optimizer fluya exclusivamente a través del cortafuegos de la aplicación web.
feature: Channel Configuration, Deliverability
role: Admin
level: Experienced
keywords: waf, cortafuegos, ip, subdominio, seguridad, tráfico, entrante
source-git-commit: 177baaa49fc173bda3d517d8fb42391bcc22b6c5
workflow-type: tm+mt
source-wordcount: '1095'
ht-degree: 0%

---

# Administrar IP permitidas {#waf-ip-allowlist}

>[!BEGINSHADEBOX]

**En esta página:** Agregue y administre sus direcciones IP de salida de Firewall de aplicaciones web (WAF) por subdominio delegado directamente en [!DNL Journey Optimizer], de modo que solo el tráfico enrutado a través del firewall pueda llegar a los vínculos hospedados en [!DNL Journey Optimizer].

>[!ENDSHADEBOX]


Las organizaciones con requisitos estrictos de seguridad de red, como las del sector financiero, pueden exigir que todas las solicitudes a vínculos alojados por [!DNL Adobe Journey Optimizer] pasen a través de un **firewall de aplicaciones web** (WAF) administrado por el cliente antes de llegar a la red de Adobe. Cualquier solicitud que omita el cortafuegos debe ser rechazada.

[!DNL Journey Optimizer] permite a los administradores configurar, por subdominio delegado, las direcciones IP de salida pública de su WAF. Una vez configurado, solo el tráfico originado en esas IP puede llegar al subdominio correspondiente. Todas las demás solicitudes entrantes, incluidas las solicitudes directas que omiten el cortafuegos, se rechazan.

## Funcionamiento {#waf-ip-allowlist-how-it-works}

Para habilitar el enrutamiento solo de WAF para un subdominio se requieren dos pasos, como se detalla a continuación.

1. **Redireccionamiento de DNS**: los registros DNS del subdominio deben actualizarse para enrutar el tráfico al WAF de su organización en lugar de directamente al perímetro de red de Adobe.
1. **Declaración de IP de salida de WAF**: su organización proporciona las IP de salida pública de su WAF en [!DNL Journey Optimizer]. Estas son las IP desde las que el cortafuegos envía solicitudes a Adobe.

Una vez que ambos están en su lugar, el flujo de tráfico funciona de la siguiente manera:

1. Un destinatario hace clic en un vínculo de una comunicación [!DNL Adobe Journey Optimizer].
1. La solicitud llega al WAF de su organización, que la inspecciona y filtra según sus políticas de seguridad.
1. WAF reenvía la solicitud al perímetro de red de Adobe desde una de sus direcciones IP de salida declaradas.
1. [!DNL Journey Optimizer] comprueba la IP de origen de la solicitud entrante con la lista de permitidos del subdominio.
   - **Coincidencias de IP** → la solicitud pasó por el → de WAF procesado normalmente.
   - **La dirección IP no coincide** → la solicitud omitió el → de WAF **rechazado con un error 403 prohibido**. El destinatario ve un vínculo roto.

Las solicitudes de subdominios sin direcciones IP permitidas configuradas no se ven afectadas y siguen funcionando como antes.

## Protecciones y restricciones {#waf-ip-allowlist-guardrails}

| Control | Detalles |
| --- | --- |
| **Formato de IP** | Se aceptan los rangos IPv4, IPv6 y CIDR. Los valores mal formados se rechazan en línea antes de guardarlos. |
| **Prevención de duplicados** | No hay direcciones IP duplicadas dentro del mismo subdominio. La misma IP se puede utilizar en diferentes subdominios. |
| **Advertencia de intervalo reservado** | Se muestra una advertencia sin bloqueo cuando se introducen intervalos privados/reservados (las direcciones IP de salida de WAF suelen ser públicas). |
| **Solo subdominios delegados** | Solo se pueden seleccionar los subdominios delegados y verificados. |
| **Límite por subdominio** | Máximo de **50 entradas de IP** por subdominio. |
| **Protecciones de bloqueo** | Escriba para confirmar la eliminación completa; advertencias explícitas cada vez que una acción vuelva a abrir un subdominio para todo el tráfico. |

>[!CAUTION]
>
>La configuración incorrecta rompe inmediatamente todos los vínculos del subdominio afectado.

Si se guardan direcciones IP de salida de WAF incorrectas, [!DNL Journey Optimizer] rechazará todas las solicitudes entrantes para ese subdominio, incluidas las legítimas de los destinatarios reales que hacen clic en los vínculos de las comunicaciones, y recibirán una página de error 403.

Confirme siempre las direcciones IP de salida exactas con el equipo de seguridad antes de guardar y pruebe primero en un subdominio que no sea de producción, si es posible.

## Acceso y administración de direcciones IP permitidas {#waf-ip-allowlist-access}

>[!NOTE]
>
>Para acceder y administrar la lista de permitidos IP, debe tener los permisos **[!UICONTROL Ver IP permitidas]** y **[!UICONTROL Administrar IP permitidas]**. [Más información](../administration/ootb-permissions.md)

Para obtener acceso a la lista de subdominios para los que ha permitido IP para el firewall de aplicaciones web, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración general]** y seleccione **[!UICONTROL Lista de permitidos - IP]**.

![Inventario de listas de permitidos IP de WAF](assets/waf-ip-allowlist.png)

La página de inventario enumera todos los subdominios que tienen al menos una IP de WAF permitida, en todos los tipos de canales (correo electrónico, página de aterrizaje, SMS, web). Obtenga más información sobre los subdominios en [esta sección](about-subdomain-delegation.md).

La lista muestra el número de direcciones IP permitidas por subdominio y el autor de la última modificación.

Puede filtrar el inventario por tipo de canal y buscar por nombre de subdominio.

## Añadir direcciones IP a la lista de permitidos {#waf-ip-allowlist-add}

>[!CONTEXTUALHELP]
>id="ajo_waf_allowed_ips"
>title="Introduzca las IP permitidas por WAF para el subdominio seleccionado"
>abstract="Seleccione un subdominio delegado e introduzca las direcciones IP de salida pública del cortafuegos de la aplicación web. Una vez guardado, [!DNL Journey Optimizer] rechazará cualquier solicitud de entrada a ese subdominio que no se origine desde una de las direcciones IP declaradas. Confirme siempre las direcciones IP de salida exactas con el equipo de seguridad antes de guardar."

Para agregar direcciones IP del cortafuegos de aplicaciones web a la lista de permitidos de un subdominio determinado, siga los pasos a continuación.

1. En el inventario de **[!UICONTROL Lista de permitidos - IP]**, haga clic en el botón **[!UICONTROL Agregar IP permitidas]**.

1. Seleccione el subdominio de destino de la lista desplegable **[!UICONTROL Subdominio]**. Solo se muestran [subdominios delegados](delegate-subdomain.md) en todos los tipos de canales admitidos: correo electrónico, página de aterrizaje, SMS y web.

1. En el campo **[!UICONTROL Dirección IP]**, ingrese las direcciones IP de salida pública de su WAF. Se admiten los intervalos IPv4, IPv6 y CIDR (por ejemplo, `203.0.113.42`, `2001:db8::1`, `203.0.113.0/24`).

   Cada entrada válida y no duplicada se valida en línea antes de agregarse. Puede agregar hasta **50 entradas de IP por subdominio**.

   ![Agregar direcciones IP permitidas de WAF para un subdominio](assets/waf-ip-allowlist-add-ip.png)

   >[!IMPORTANT]
   >
   >Se muestra una advertencia cuando se introducen intervalos de IP privados o reservados (RFC 1918, loopback, link-local). Las direcciones IP de salida de WAF suelen ser direcciones públicas.

1. Si es necesario, puede quitar una IP de la lista haciendo clic en el icono **✕** de su chip.

1. Haga clic en **[!UICONTROL Save]**. La lista de permitidos se aplica y se propaga a la arista. El subdominio aparece en el inventario y sus direcciones IP se aplican inmediatamente.

Ahora se rechazarán todas las solicitudes a este subdominio desde cualquier IP que no esté en esta lista.

>[!CAUTION]
>
>Asegúrese de confirmar estas direcciones IP con el equipo de seguridad; los valores incorrectos romperán todos los vínculos de este subdominio.

## Editar direcciones IP permitidas {#waf-ip-allowlist-edit}

Para actualizar las direcciones IP permitidas para un subdominio existente, haga clic en el nombre de subdominio en el inventario.

El campo **Subdominio** es de solo lectura <!--as well as the Channel field-->; no se puede cambiar después de crearlo.

Agregue nuevas direcciones IP mediante el campo de entrada o elimine las direcciones IP existentes haciendo clic en el icono **✕** de cada chip.

![Editar o quitar IP permitidas de WAF](assets/waf-ip-allowlist-edit-ip.png)

>[!IMPORTANT]
>
>Al eliminar la última IP de un subdominio, se vuelve a abrir para todo el tráfico entrante.

## Eliminar direcciones IP permitidas {#waf-ip-allowlist-remove}

Para eliminar todas las IP de la lista de permitidos de un subdominio, utilice el icono Delete de la columna Actions del inventario. Esto elimina completamente la restricción de WAF para ese subdominio.

![Icono Eliminar en la columna Acciones de la lista IP permitidas](assets/waf-ip-allowlist-delete-icon.png)

Se abre una ventana emergente de confirmación. Escriba el nombre exacto del subdominio que desea confirmar y haga clic en **[!UICONTROL Quitar]**.

![Confirmar la eliminación de todas las direcciones IP permitidas por WAF para un subdominio](assets/waf-ip-allowlist-remove.png){width="80%"}

>[!WARNING]
>
>Al confirmar, esta acción elimina todas las direcciones IP de lista de permitidos del subdominio que ha introducido. El tráfico entrante se aceptará una vez más desde cualquier fuente, incluidas las solicitudes que omiten el cortafuegos de su aplicación web. Esto no se puede deshacer: es necesario volver a introducir las direcciones IP para restaurar la restricción.

Después de eliminar todas las direcciones IP, el subdominio ya no aparece en el inventario. Puede volver a configurarlo en cualquier momento volviendo a agregar direcciones IP para este subdominio.
