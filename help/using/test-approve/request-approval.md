---
title: Solicitud de aprobación
description: Obtenga información sobre cómo solicitar la aprobación antes de publicar recorridos y campañas.
role: User
level: Beginner
feature: Approval
source-git-commit: 8fecd0d4812ba875dba1d47bc32ab08178a13f2c
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---


# Solicitud de aprobación {#request-approval}

Si la funcionalidad de flujo de trabajo de aprobación se ha habilitado para su organización, verá que los botones **[!UICONTROL Activar]** y **[!UICONTROL Publish]** ya no están disponibles en los flujos de trabajo Crear campaña y Crear Recorrido, respectivamente. Estos botones han sido reemplazados por el botón **[!UICONTROL Solicitar aprobación]**.

Después de crear tu campaña o recorrido, debes hacer clic en el botón **[!UICONTROL Solicitar aprobación]**. Esto comprobará si hay una directiva de aprobación activa en la zona protegida que se aplique a la campaña o al recorrido. Si se encuentra una directiva de aprobación relevante, se iniciará el proceso de aprobación. Si no existe ninguna directiva de aprobación aplicable, la campaña o el recorrido se aprueban automáticamente y se activan o publican.

Se abre el panel **[!UICONTROL Solicitar aprobación]**. Proporcione un mensaje a los aprobadores si es necesario y haga clic en **[!UICONTROL Enviar]** para enviar la solicitud.

![](assets/approval-request.png)

Aunque la campaña o el recorrido tengan el estado **[!UICONTROL En revisión]**, tiene la opción de cancelar la solicitud de aprobación. Al hacer clic en el botón **[!UICONTROL Cancelar solicitud]**, la campaña o el recorrido volverán a la fase de borrador y se enviará una notificación a los revisores para informarles de que la solicitud se ha cancelado. A continuación, puede realizar las ediciones necesarias y volver a enviar la campaña o el recorrido para su aprobación.

![](assets/approval-cancel.png)

Una vez enviada la solicitud de aprobación a los aprobadores, pueden revisarla y activar el recorrido/campaña para activarla o solicitar cambios si es necesario. [Aprenda a revisar y aprobar una solicitud](review-approve-request.md)

Si los aprobadores solicitan cambios, se le notifica mediante un mensaje de correo electrónico y una alerta de Journey Optimizer, a la que se puede acceder haciendo clic en el icono de campana en la parte superior derecha de la pantalla, en la pestaña **[!UICONTROL Solicitudes]**.

![](assets/changes-requested.png)

Para revisar la solicitud de cambio, ábrala desde el correo electrónico o la alerta para acceder al recorrido o campaña y realice los cambios solicitados. Cuando el recorrido o la campaña estén listos para revisarse nuevamente, envíe una nueva solicitud de aprobación con el botón **[!UICONTROL Solicitar aprobación]**.
