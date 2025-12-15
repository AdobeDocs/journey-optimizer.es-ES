---
title: Solicitud de aprobación
description: Obtenga información sobre cómo solicitar la aprobación antes de publicar recorridos y campañas.
role: User
level: Beginner
feature: Approval
exl-id: 75dafecd-805d-4aa2-86c6-99e6da4d378b
source-git-commit: b495462aed9a67ff25c2563288bb2ca57e9b7db7
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Solicitud de aprobación {#request-approval}

El acceso al flujo de trabajo de aprobación viene determinado por el caso de uso específico:

* **No existe ninguna directiva de aprobación activa**

   * **Campañas**: si no hay ninguna directiva de aprobación activa para el objeto de campaña en una zona protegida, las campañas mostrarán el botón **[!UICONTROL Activar]**, que le permitirá activarlas sin necesidad de aprobación.

   * **Recorridos**: si no hay ninguna directiva de aprobación activa para el objeto de Recorrido, recorrido mostrará el botón **[!UICONTROL Publicar]**, que le permitirá publicar directamente.

* **Existen directivas de aprobación activas**

   * **Campañas**: Si existen una o más políticas de aprobación activas para el objeto de campaña en una zona protegida, todas las campañas de dicha zona protegida mostrarán el botón **[!UICONTROL Solicitar aprobación]**.
Si no se aplica ninguna directiva de aprobación al objeto seleccionado cuando se hace clic en el botón **[!UICONTROL Solicitar aprobación]**, se activará el flujo de trabajo de aprobación automática.

   * **Recorridos**: si existen una o más directivas de aprobación activas para el objeto de Recorrido en una zona protegida, todos los recorridos mostrarán el botón **[!UICONTROL Solicitar aprobación]**.
Si no se aplica ninguna directiva de aprobación al objeto seleccionado cuando se hace clic en el botón **[!UICONTROL Solicitar aprobación]**, se activará el flujo de trabajo de aprobación automática.

## Enviar solicitud de aprobación

Después de crear tu campaña o recorrido, haz clic en el botón **[!UICONTROL Solicitar aprobación]**. Esto comprobará si hay una directiva de aprobación activa en la zona protegida que se aplique a la campaña o al recorrido.

* Si se encuentra una directiva de aprobación aplicable, la campaña o el recorrido se enviarán para su revisión.

* Si no se aplica ninguna directiva de aprobación a la campaña o al recorrido después de hacer clic en el botón **[!UICONTROL Solicitar aprobación]**, la campaña o el recorrido se aprobarán automáticamente y se activarán o publicarán.

Se abre el panel **[!UICONTROL Solicitar aprobación]**. Proporcione un mensaje a los aprobadores si es necesario y haga clic en **[!UICONTROL Enviar]** para enviar la solicitud.

![](assets/approval-request.png)

Aunque la campaña o el recorrido tengan el estado **[!UICONTROL En revisión]**, tiene la opción de cancelar la solicitud de aprobación. Al hacer clic en el botón **[!UICONTROL Cancelar solicitud]**, la campaña o el recorrido volverán a la fase de borrador y se enviará una notificación a los revisores para informarles de que la solicitud se ha cancelado. A continuación, puede realizar las ediciones necesarias y volver a enviar la campaña o el recorrido para su aprobación.

![](assets/approval-cancel.png)

## Administrar solicitudes de aprobación

Una vez enviada la solicitud de aprobación a los aprobadores, pueden revisarla y activar el recorrido/campaña para activarla o solicitar cambios si es necesario. [Aprenda a revisar y aprobar una solicitud](review-approve-request.md)

Si los aprobadores solicitan cambios, se le notifica mediante un mensaje de correo electrónico y una alerta de Journey Optimizer, a la que se puede acceder haciendo clic en el icono de campana en la parte superior derecha de la pantalla, en la pestaña **[!UICONTROL Solicitudes]**.

![](assets/changes-requested.png)

Para revisar la solicitud de cambio, ábrala desde el correo electrónico o la alerta para acceder al recorrido o campaña y realice los cambios solicitados. Cuando el recorrido o la campaña estén listos para revisarse nuevamente, envíe una nueva solicitud de aprobación con el botón **[!UICONTROL Solicitar aprobación]**.
