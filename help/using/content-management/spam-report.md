---
title: Usar informe de spam
description: Aprenda a utilizar el informe de correo no deseado.
feature: Preview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: feae2cb9d0bed35f12eb117cf2969c9290ebc06f
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 3%

---

# Uso del informe de spam {#spam-report}

>[!AVAILABILITY]
>
>Actualmente, la función de informe de correo no deseado está disponible como una versión beta solo para usuarios seleccionados. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.

[!DNL Journey Optimizer] le permite comprobar el rendimiento del contenido frente al filtrado de correo no deseado y asegurarse de que los mensajes se dirijan a las bandejas de entrada de los clientes, no al correo no deseado.

>[!CAUTION]
>
>* Actualmente, esta función solo está disponible para el canal de correo electrónico.
>
>* Por ahora, el análisis del informe de correo no deseado solo se puede realizar para el contenido en inglés.

Al editar o previsualizar el contenido, la variable **[!UICONTROL Informe de spam]** proporciona una puntuación y consejos para mejorar las puntuaciones de cada elemento individual de la lista.

Esto le permite determinar si un mensaje corre el riesgo de que las herramientas de filtrado de correo no deseado utilizadas durante la recepción lo consideren como no deseado, y realizar acciones en caso contrario.

>[!CAUTION]
>
>El informe de correo no deseado solo proporciona indicaciones y advertencias. Tenga en cuenta que no se le impide enviar mensajes si el informe de correo no deseado indica que su contenido se considera correo no deseado. Es su elección actuar según la puntuación y las mejoras sugeridas.

Para usar la variable **[!UICONTROL Informe de spam]** función, siga los pasos a continuación.

<!--For example spam scoring tool can tell that there are too many Images compared to the text. Retailers tend to do this even though the spam score gets worse because the content is more engaging.-->

<!--Michael, who is a marketer with NIKE works along with Tara from testing team to ensure that the emails being sent as part of the campaign/journey don't get categorised as SPAM.

They need an integration within AJO's marketing system to show how the curated content is doing against different SPAM compliance pillars like for SPAM trigger words, HTML Body content and layout, subject line etc.

They should be able to get scores for each individual items as shown by market standard SPAM filtering tools like Spam Assassin, Symantec etc.

They should also get suggestions on how to improve the score better to be confident that the messages don't get categorised as spam.-->

1. Desde el **[!UICONTROL Simular]** , haga clic en **[!UICONTROL Informe de spam]** botón.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Se realiza automáticamente una comprobación de correo no deseado y la variable **[!UICONTROL Informe de spam]** La ventana muestra los resultados. Muestra el rendimiento del contenido en términos de diseño del cuerpo, estructura, tamaño de la imagen, palabras de déclencheur de spam, si las hay, etc.

   ![](assets/spam-report-high-score.png)

1. Compruebe las puntuaciones y descripciones de cada elemento.

   Si la puntuación es mayor de 5, se muestra una advertencia. Indica que algunos mensajes pueden ser bloqueados o marcados como correo no deseado por las herramientas de correo no deseado cuando se reciben.

1. En función de esa puntuación, si considera que algunos elementos se pueden mejorar, vaya al contenido mediante el complemento [Diseñador de correo electrónico](../email/content-from-scratch.md) y realizar las actualizaciones necesarias.

1. Una vez que haya realizado los cambios, vuelva a la **[!UICONTROL Informe de spam]** para garantizar que su puntuación haya mejorado.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
