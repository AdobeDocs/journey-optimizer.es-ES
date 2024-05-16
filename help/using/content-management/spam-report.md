---
title: Usar informe de spam
description: Aprenda a utilizar el informe de correo no deseado.
feature: Preview
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 4c1dca7815594bbbf5a2d84682338e8b2d743965
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Informe de correo no deseado {#spam-report}

[!DNL Journey Optimizer] le permite comprobar el rendimiento del contenido frente al filtrado de correo no deseado y asegurarse de que los mensajes se dirijan a las bandejas de entrada de los clientes, no al correo no deseado.

Al editar o previsualizar el contenido del correo electrónico, la variable **[!UICONTROL Informe de spam]** proporciona una puntuación y consejos para mejorar las puntuaciones de cada elemento individual de la lista.

Esto le permite determinar si un mensaje corre el riesgo de que las herramientas de filtrado de correo no deseado utilizadas durante la recepción lo consideren como no deseado, y realizar acciones en caso contrario. Muchos proveedores de bandejas de entrada de correo electrónico utilizan herramientas como parte de su proceso de filtrado de correo no deseado. El envío de correos electrónicos con una mala puntuación puede afectar gravemente a la capacidad de entrega.


>[!CAUTION]
>
>* Actualmente, esta función solo está disponible como una versión beta privada.
>
>* Por ahora, el análisis del informe de correo no deseado solo se puede realizar para el contenido en inglés.
>
>* El informe de correo no deseado es informativo y no impide enviar mensajes con una puntuación incorrecta.

Para acceder a **[!UICONTROL Informe de spam]**, siga los pasos a continuación.

1. Desde el **[!UICONTROL Simular]** , haga clic en **[!UICONTROL Informe de spam]** botón.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Se realiza automáticamente una comprobación de correo no deseado y la variable **[!UICONTROL Informe de spam]** La ventana muestra los resultados. Muestra el rendimiento del contenido en términos de diseño del cuerpo, estructura, tamaño de la imagen, palabras de déclencheur de spam, si las hay, etc.

   ![](assets/spam-report-high-score.png)

1. Compruebe las puntuaciones y descripciones de cada elemento.

   Cuanto más bajo sea el resultado, mejor. Si la puntuación es mayor de 5, se muestra una advertencia: indica que algunos mensajes pueden bloquearse o marcarse como correo no deseado cuando se reciben.

1. En función de esa puntuación, si considera que algunos elementos se pueden mejorar, edite el contenido en [Diseñador de correo electrónico](../email/content-from-scratch.md) y realice las actualizaciones necesarias.

1. Una vez completados los cambios, vuelva a la pestaña **[!UICONTROL Informe de spam]** para garantizar que su puntuación haya mejorado.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
