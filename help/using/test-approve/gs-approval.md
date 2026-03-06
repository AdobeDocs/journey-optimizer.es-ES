---
title: Introducción a la aprobación de recorridos y campañas
description: Aprenda a configurar un proceso de aprobación para sus recorridos y campañas.
role: User
level: Beginner
feature: Approval
exl-id: 92d1439e-5cac-4e7d-85f8-ebf432e9ef7c
source-git-commit: e6cac6aff79b30a308be480319902f478436391d
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 58%

---

# Introducción a la aprobación de recorridos y campañas {#send-proofs}

## Introducción a las políticas de aprobación {#gs}

[!DNL Journey Optimizer] le permite configurar un proceso de aprobación que permite a los equipos de marketing asegurarse de que las campañas y los recorridos sean revisados y firmados por las partes interesadas correspondientes antes de su lanzamiento.

Las políticas de aprobación introducen un flujo de trabajo estructurado directamente en la interfaz de usuario, lo que elimina la necesidad de medios externos, como herramientas de administración de tareas o correo electrónico, y garantiza que todas las aprobaciones se administren y rastreen de forma centralizada.

Además, esta función proporciona un control mejorado sobre la publicación de los recorridos y las campañas: con el proceso de aprobación integrado en Journey Optimizer, las campañas y los recorridos permanecen en estado “bloqueado” durante la revisión, lo que garantiza que no se produzcan cambios ni activaciones no deseados antes de que se establezcan todas las aprobaciones necesarias.

## Requisitos previos {#prerequisites}

Antes de empezar, asegúrese de que se han configurado los permisos siguientes.

Para aprobar y publicar recorridos y campañas, los usuarios necesitan los permisos **Aprobar y publicar campañas** y **Aprobar y publicar Recorridos**. [Más información](../administration/permissions.md)

+++  Obtenga información sobre cómo asignar permisos relacionados con la aprobación

1. En el producto **Permisos**, vaya a la pestaña **Funciones** y seleccione la **Función** que desee.

1. Haga clic en **Editar** para modificar los permisos.

1. Añada el recurso **Campañas** y, a continuación, seleccione **Aprobar y publicar campañas** en el menú desplegable.

   ![Asignar permiso para aprobar y publicar campañas](assets/permissions_approval.png){zoomable="yes"}

1. Añada el recurso **Recorridos** y, a continuación, seleccione **Aprobar y publicar recorridos** en el menú desplegable.

   ![Asignar permiso para aprobar y publicar Recorridos](assets/permissions_approval_2.png){zoomable="yes"}

1. Haga clic en **Guardar** para aplicar los cambios.

Los permisos de los usuarios que ya estén asignados a esta función se actualizarán automáticamente.

1. Para asignar esta función a nuevos usuarios, vaya a la pestaña **Usuarios** en el panel de control **Funciones** y haga clic en **Añadir usuario**.

1. Introduzca el nombre del usuario y su dirección de correo electrónico, o selecciónelo en la lista, y haga clic en **Guardar**.

1. Si el usuario no se creó anteriormente, consulte [esta documentación](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/users).

El usuario recibirá un correo electrónico con instrucciones para acceder a su instancia.

+++

## Información general del proceso de aprobación {#process}

El proceso de aprobación global es el siguiente:

![Flujo del proceso de aprobación](assets/approval-process.png){zoomable="yes"}

1. **Configuración de políticas de aprobación**

   Un usuario administrador crea una política de aprobación y define las condiciones en las que la política debe aplicarse a recorridos o campañas. Por ejemplo, puede crear una directiva de aprobación que requiera que todas las campañas programadas creadas por un usuario determinado se aprueben antes de la activación. [Aprenda a crear políticas de aprobación](approval-policies.md)

1. **Envío de campañas/recorridos para su aprobación**

   Los creadores de campañas/recorridos crean un recorrido o campaña y la envían para su aprobación. La campaña o el recorrido entran en el estado “En revisión”, durante el cual no se pueden realizar ediciones a menos que se cancele la solicitud. [Aprenda a solicitar la aprobación](request-approval.md)

   >[!NOTE]
   >
   >Las campañas y los recorridos solo deben enviarse para su aprobación si se ha implementado una política de aprobación. Si no se aplica ninguna política de este tipo, el creador puede publicar directamente la campaña o el recorrido sin requerir la aprobación.

1. **Revisión y aprobación**

   Los aprobadores definidos en la política de aprobación que se aplica al recorrido o campaña reciben una notificación. Pueden revisar el recorrido o el contenido, el público y la configuración de la campaña. Si es necesario realizar cambios, el aprobador los solicita y devuelve la campaña a “Borrador” para que se revise. Si están listos, pueden activar e iniciar el recorrido o la campaña. [Aprenda a revisar y aprobar una solicitud](review-approve-request.md)

## Monitorizar solicitudes de aprobación {#monitor}

Puede monitorizar todas las solicitudes de aprobación y cambio que se han enviado para un recorrido o campaña determinados. Para ello, haga clic en el icono **[!UICONTROL Mostrar pista de auditoría]** ubicado en la sección superior derecha del lienzo del recorrido o en la pantalla de revisión de la campaña.

![Pista de auditoría de solicitudes de aprobación](assets/monitor-requests.png)

## Preguntas frecuentes {#faq}

+++¿Debo crear una política de aprobación para cada campaña o recorrido?

No. Las políticas de aprobación son condicionales. Solo es necesario crear una directiva si desea aplicar la revisión a un conjunto específico de campañas o recorridos (por ejemplo, todas las campañas programadas creadas por un equipo específico). Si no se aplica ninguna directiva a una campaña o recorrido, el creador puede publicar directamente sin solicitar la aprobación.

+++

+++¿Qué sucede si el aprobador no está disponible?

La solicitud permanece &quot;en revisión&quot; hasta que un aprobador actúe en consecuencia. Puede cancelar la solicitud (devolviendo el elemento a &quot;Borrador&quot;) y volver a enviarla cuando el aprobador adecuado esté disponible. Los administradores también pueden actualizar la directiva de aprobación para agregar aprobadores adicionales.

+++

+++¿Puedo editar una campaña o un recorrido mientras está pendiente de aprobación?

No. Una vez enviada para su aprobación, la campaña o el recorrido está en estado bloqueado &quot;En revisión&quot;. Para realizar cambios, el creador o un aprobador deben cancelar primero la solicitud. El elemento vuelve a &quot;Borrador&quot; y se puede editar antes de volver a enviarlo.

+++

+++No veo el permiso Aprobar y publicar en la lista desplegable. ¿Qué debo comprobar?

Asegúrese de añadir primero el recurso correcto. El permiso **Aprobar y publicar campañas** requiere que se agregue el recurso **Campañas** al rol y **Aprobar y publicar Recorridos** requiere el recurso **Recorridos**. Ambos deben añadirse por separado. [Aprenda a asignar permisos relacionados con la aprobación](#prerequisites)

+++

## Recursos adicionales

* **[Crear directivas de aprobación](approval-policies.md)**: aprenda a configurar las directivas de aprobación para aplicar flujos de trabajo de revisión para campañas y recorridos.
* **[Solicitar aprobación](request-approval.md)**: aprenda cómo enviar contenido para su aprobación y hacer un seguimiento del estado de aprobación.
* **[Revisar y aprobar solicitudes](review-approve-request.md)**: descubra cómo revisar, aprobar o rechazar solicitudes de aprobación como aprobador.
* **[Simule con entradas de ejemplo](simulate-sample-input.md)**: aprenda a probar y validar contenido mediante datos de perfil de muestra.
