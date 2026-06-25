---
title: Introducción a la aprobación de recorridos y campañas
description: Aprenda a configurar un proceso de aprobación para sus recorridos y campañas.
role: User
level: Beginner
feature: Approval
exl-id: 92d1439e-5cac-4e7d-85f8-ebf432e9ef7c
TQID: https://experienceleague.adobe.com/dKfstmm0ilHKUATU-sz7c04IZBu2O7Ju-srPPoKJVl4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: []
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
subfeature_v2: id: bf7a266e-e483-42c6-b5bc-09ca6e49900cid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 36b855c6d66a614f4c0374cbd1b4746ec68fde21
workflow-type: ht
source-wordcount: 1037
ht-degree: 100%

---

# Introducción a la aprobación de recorridos y campañas {#send-proofs}

>[!BEGINSHADEBOX]

**En esta página:** un proceso de aprobación incrustado mantiene bloqueados los recorridos y las campañas durante la revisión, de modo que las partes interesadas correctas cierran sesión antes de que se publique cualquier cosa, con cada solicitud administrada y rastreada centralmente.

>[!ENDSHADEBOX]

## Introducción a las políticas de aprobación {#gs}

[!DNL Journey Optimizer] posibilita configurar un proceso de aprobación que permita a los equipos de marketing asegurarse de que las partes interesadas revisan y aprueban las campañas y los recorridos antes de que se pongan en marcha.

Las políticas de aprobación introducen un flujo de trabajo estructurado directamente en la interfaz de usuario, lo que elimina la necesidad de medios externos, como herramientas de administración de tareas o correo electrónico, y garantiza que todas las aprobaciones se administren y rastreen de forma centralizada.

Además, esta función proporciona un control mejorado sobre la publicación de los recorridos y las campañas: con el proceso de aprobación integrado en Journey Optimizer, las campañas y los recorridos permanecen en estado “bloqueado” durante la revisión, lo que garantiza que no se produzcan cambios ni activaciones no deseados antes de que se establezcan todas las aprobaciones necesarias.

## Requisitos previos {#prerequisites}

Antes de empezar, asegúrese de que se han configurado los permisos siguientes.

Para aprobar y publicar recorridos y campañas, los usuarios deben tener los permisos **Aprobar y publicar campañas** y **Aprobar y publicar recorridos**. [Más información](../administration/permissions.md)

+++  Aprenda a asignar permisos relacionados con la aprobación

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

![Flujo de proceso de aprobación](assets/approval-process.png){zoomable="yes"}

1. **Configuración de políticas de aprobación**

   Un administrador crea una política de aprobación y define las condiciones en las que debe aplicarse a recorridos o campañas. Por ejemplo, puede crear una política de aprobación que requiera que todas las campañas programadas creadas por un usuario determinado se aprueben antes de activarse. [Aprenda a crear políticas de aprobación](approval-policies.md)

1. **Envío de campañas/recorridos para su aprobación**

   Los creadores de campañas/recorridos crean un recorrido o una campaña y la envían para su aprobación. La campaña o el recorrido entran en el estado “En revisión”, durante el cual no se pueden realizar ediciones a menos que se cancele la solicitud. [Aprenda a solicitar la aprobación](request-approval.md)

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

No. Las políticas de aprobación son condicionales. Solo es necesario crear una política si desea aplicar la revisión a un conjunto específico de campañas o recorridos (por ejemplo, todas las campañas programadas creadas por un equipo específico). Si no se aplica ninguna política a una campaña o recorrido, el creador puede publicar directamente sin solicitar la aprobación.

+++

+++¿Qué sucede si el aprobador no está disponible?

La solicitud permanece “en revisión” hasta que un aprobador actúe en ella. Usted puede cancelar la solicitud (devolviendo el elemento a “Borrador”) y volver a enviarla cuando el aprobador adecuado esté disponible. Los administradores también pueden actualizar la política de aprobación para añadir aprobadores adicionales.

+++

+++¿Puedo editar una campaña o un recorrido mientras está pendiente de aprobación?

No. Una vez enviada para su aprobación, la campaña o el recorrido está en estado bloqueado “En revisión”. Para realizar cambios, el creador o un aprobador deben cancelar primero la solicitud. El elemento vuelve a “Borrador” y se puede editar antes de volver a enviarlo.

+++

+++No veo el permiso Aprobar y publicar en la lista desplegable, ¿qué debo comprobar?

Asegúrese de añadir primero el recurso correcto. El permiso **Aprobar y publicar campañas** requiere que se añada el recurso **Campañas** a la función y **Aprobar y publicar Recorridos** requiere el recurso **Recorridos**. Ambos deben añadirse por separado. [Aprenda a asignar permisos relacionados con la aprobación](#prerequisites)

+++

+++¿Cómo determina [!DNL Journey Optimizer] qué política de aprobación se aplica si más de una política puede coincidir?

Cuando se pueden aplicar varias políticas de aprobación activas al mismo recorrido o campaña, la política **activada más recientemente** tiene prioridad. Los grupos de usuarios de aprobadores definidos en esa política son los que reciben las notificaciones y los que rigen la solicitud.

[Más información](approval-policies.md#multiple-policies)

+++

+++Si un solicitante pertenece a varios grupos de usuarios, ¿puede este solicitante elegir a qué grupo se envía la solicitud de aprobación?

No. Los solicitantes no pueden seleccionar manualmente qué grupo de usuarios recibe o enruta la solicitud de aprobación. Se notifica automáticamente a los grupos de usuarios especificados en la política de aprobación que se aplica (según la [prioridad de política](approval-policies.md#multiple-policies)).

+++

## Recursos adicionales

* **[Crear directivas de aprobación](approval-policies.md)**: aprenda a configurar las directivas de aprobación para aplicar flujos de trabajo de revisión para campañas y recorridos.
* **[Solicitar aprobación](request-approval.md)**: aprenda cómo enviar contenido para su aprobación y hacer un seguimiento del estado de aprobación.
* **[Revisar y aprobar solicitudes](review-approve-request.md)**: descubra cómo revisar, aprobar o rechazar solicitudes de aprobación como aprobador.
* **[Simular variaciones de contenido](simulate-sample-input.md)**: haga clic en **[!UICONTROL Simular contenido]** para probar las variaciones de contenido con datos de entrada de muestra, generación automática por IA o usuarios simulados. Haga clic en **[!UICONTROL Simular contenido]** y, a continuación, seleccione **[!UICONTROL Simular contenido (perfiles de AEP)]** en el menú desplegable para previsualizarlo con perfiles de prueba.
