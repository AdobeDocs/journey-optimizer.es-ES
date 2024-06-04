---
title: Usar informe de correo no deseado
description: Aprenda a utilizar el informe de correo no deseado.
feature: Preview
role: User
level: Beginner
badge: label="Beta"
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 5f69b252f5812f43b3d0a6fed0aac074ece0d10f
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 6%

---

# Informe de correo no deseado {#spam-report}

>[!CONTEXTUALHELP]
>id="ajo_simulate_spam_report"
>title="Informe de correo no deseado"
>abstract="El informe Spam permite comprobar la puntuación de spam del contenido del correo electrónico. Esta puntuación indica si los ISP o proveedores de buzones de correo considerarán su mensaje como correo no deseado o no. Cuanto más bajo sea el resultado, mejor. Si la puntuación del contenido del correo electrónico es superior a 2, debe considerar la posibilidad de corregir los problemas que causan que las pruebas fallen."

Puede comprobar la puntuación de correo no deseado del contenido del correo electrónico en un informe de correo no deseado específico. Uso de [SpamAssassin](https://spamassassin.apache.org/){target="_blank"}, Adobe Journey Optimizer puede probar el contenido del correo electrónico y asignarle una puntuación para indicar si los ISP o proveedores de buzones de correo lo considerarán como correo no deseado o no.

>[!AVAILABILITY]
>
>Actualmente, esta función está en versión beta y solo se encuentra disponible para los clientes de dicha versión. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.

Al editar o previsualizar el contenido del correo electrónico, la variable **[!UICONTROL Informe de spam]** proporciona una puntuación y consejos para mejorar las puntuaciones de cada elemento individual de la lista.

Esta capacidad le permite determinar si las herramientas de filtrado de correo no deseado utilizadas durante la recepción pueden considerar un mensaje como no deseado y, en ese caso, realizar acciones. Muchos proveedores de bandejas de entrada de correo electrónico utilizan herramientas como parte de su proceso de filtrado de correo no deseado. El envío de correos electrónicos con una mala puntuación puede afectar gravemente a la capacidad de entrega.

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

   Cuanto más bajo sea el resultado, mejor. Si la puntuación es mayor de 5, se muestra una advertencia: indica que algunos mensajes pueden bloquearse o marcarse como correo no deseado cuando se reciben. La práctica recomendada es tener una puntuación inferior a 2.

1. En función de esa puntuación, si considera que algunos elementos se pueden mejorar, edite el contenido en [Diseñador de correo electrónico](../email/content-from-scratch.md) y realice las actualizaciones necesarias.

1. Una vez completados los cambios, vuelva a la pestaña **[!UICONTROL Informe de spam]** para garantizar que su puntuación haya mejorado.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
