---
title: Introducción a la aprobación de recorridos y campañas
description: Obtenga información sobre cómo configurar un proceso de aprobación para sus recorridos y campañas.
role: User
level: Beginner
feature: Approval
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 94114fac56b68aa0940ae9843f672823d64c19df
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 18%

---


# Introducción a la aprobación de recorridos y campañas {#send-proofs}

>[!AVAILABILITY]
>
> Actualmente, las directivas de aprobación solo están disponibles para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

## Introducción a las directivas de aprobación {#gs}

Journey Optimizer le permite configurar un proceso de aprobación que permita a los equipos de marketing asegurarse de que las campañas y los recorridos sean revisados y firmados por las partes interesadas correspondientes antes de su lanzamiento.

Las políticas de aprobación introducen un flujo de trabajo estructurado directamente en la interfaz de usuario, lo que elimina la necesidad de medios externos como herramientas de administración de tareas o correo electrónico, y garantiza que todas las aprobaciones se administren y rastreen de forma centralizada.

Además, esta función proporciona un control mejorado sobre la publicación de los recorridos y las campañas: con el proceso de aprobación integrado en Journey Optimizer, las campañas y los recorridos permanecen en estado &quot;bloqueado&quot; durante la revisión, lo que garantiza que no se produzcan cambios ni activaciones no deseadas antes de que se establezcan todas las aprobaciones necesarias.

## Requisitos previos {#prerequisites}

Antes de empezar, asegúrese de que se han configurado los permisos siguientes.

Para acceder a los recorridos y campañas de aprobación y publicación, los usuarios deben tener los permisos **Aprobar y publicar campañas** y **Aprobar y publicar Recorridos**. [Más información](../administration/permissions.md)

+++  Obtenga información sobre cómo asignar permisos relacionados con la aprobación

1. En el producto **Permisos**, vaya a la pestaña **Funciones** y seleccione la **Función** que desee.

1. Haga clic en **Editar** para modificar los permisos.

1. Agregue el recurso **Campañas** y, a continuación, seleccione **Aprobar y publicar campañas** en el menú desplegable.

   ![](assets/permissions_approval.png){zoomable="yes"}

1. Agregue el recurso **Recorridos** y, a continuación, seleccione **Aprobar y publicar Recorridos** en el menú desplegable.

   ![](assets/permissions_approval_2.png){zoomable="yes"}

1. Haga clic en **Guardar** para aplicar los cambios.

Los permisos de los usuarios que ya estén asignados a esta función se actualizarán automáticamente.

1. Para asignar esta función a nuevos usuarios, vaya a la pestaña **Usuarios** en el panel de control **Funciones** y haga clic en **Añadir usuario**.

1. Introduzca el nombre del usuario y su dirección de correo electrónico, o selecciónelo en la lista, y haga clic en **Guardar**.

1. Si el usuario no estaba ya creado, consulte [esta documentación](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/users).

El usuario recibirá un correo electrónico con instrucciones para acceder a su instancia.

+++

## Resumen del proceso de aprobación {#process}

El proceso de aprobación global es el siguiente:

![](assets/approval-process.png){zoomable="yes"}

1. **Configuración de directivas de aprobación**

   Un administrador crea una directiva de aprobación y define las condiciones en las que la directiva debe aplicarse a recorridos o campañas. Por ejemplo, puede crear una directiva de aprobación que requiera que todas las campañas programadas creadas por un usuario determinado se aprueben antes de activarse. [Aprenda a crear directivas de aprobación](approval-policies.md)

1. **Envío de campaña/recorrido para aprobación**

   Los creadores de campañas/recorridos crean un recorrido o una campaña y la envían para su aprobación. La campaña o el recorrido entran en estado &quot;En revisión&quot;, durante el cual no se pueden realizar ediciones a menos que se cancele la solicitud. [Obtenga información sobre cómo solicitar aprobación](request-approval.md)

   >[!NOTE]
   >
   >Las campañas y los recorridos solo deben enviarse para su aprobación si se ha implementado una directiva de aprobación. Si no se aplica ninguna directiva de este tipo, el creador puede publicar directamente la campaña o el recorrido sin requerir la aprobación.

1. **Revisión y aprobación**

   Los aprobadores definidos en la política de aprobación que se aplica al recorrido o campaña reciben una notificación. Pueden revisar el recorrido o el contenido, la audiencia y la configuración de la campaña. Si es necesario realizar cambios, el aprobador los solicita y devuelve la campaña a &quot;Borrador&quot; para que la revisen. Si está listo, puede activarlo e iniciar el recorrido o la campaña. [Obtenga información sobre cómo revisar y aprobar una solicitud](review-approve-request.md)

## Monitorización de solicitudes de aprobación {#monitor}

Puede monitorizar todas las solicitudes de aprobación y cambio que se han enviado para un recorrido o campaña determinados. Para ello, haga clic en el botón **[!UICONTROL Mostrar pista de auditoría]** ubicado en la sección superior derecha del lienzo de recorrido o en la pantalla de revisión de la campaña.

![](assets/monitor-requests.png)
