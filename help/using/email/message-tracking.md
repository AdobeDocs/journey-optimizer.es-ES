---
solution: Journey Optimizer
product: journey optimizer
title: Seguimiento de mensajes
description: Obtenga información sobre cómo añadir vínculos y rastrear los mensajes enviados
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: vínculos, seguimiento, monitorización, correo electrónico
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: c082d9329949fd8dc68929e3934daf2d9dfdbd46
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 35%

---

# Adición de vínculos y seguimiento de mensajes {#tracking}

Uso [!DNL Journey Optimizer] para añadir vínculos al contenido y realizar un seguimiento de los mensajes enviados para monitorizar el comportamiento de los destinatarios.

## Habilitar seguimiento {#enable-tracking}

Puede habilitar el seguimiento en el nivel de mensaje de correo electrónico comprobando la **[!UICONTROL Aperturas de correo electrónico]** y/o **[!UICONTROL Haga clic en el correo electrónico]** opciones al crear el mensaje dentro de un recorrido o una campaña.

>[!BEGINTABS]

>[!TAB Habilitar el seguimiento en un recorrido]

![](assets/message-tracking-journey.png)

>[!TAB Habilitar el seguimiento en una campaña]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>Ambas opciones están habilitadas de forma predeterminada.

Esto permite rastrear el comportamiento de los destinatarios a través de:

* **[!UICONTROL Aperturas de correo electrónico]**: Mensajes que se han abierto.
* **[!UICONTROL Haga clic en el correo electrónico]**: hace clic en los vínculos de un correo electrónico.

## Inserción de vínculos {#insert-links}

Al diseñar un mensaje, puede agregar vínculos al contenido.

>[!NOTE]
>
>Cuándo [el seguimiento está activado](#enable-tracking), se realiza un seguimiento de todos los vínculos incluidos en el contenido del mensaje.

Para insertar vínculos en el contenido del correo electrónico, siga los pasos a continuación:

1. Seleccione un elemento y haga clic en **[!UICONTROL Insertar vínculo]** en la barra de herramientas contextual.

   ![](assets/message-tracking-insert-link.png)

1. Elija el tipo de vínculo que desea crear:

   * **[!UICONTROL Vínculo externo]**: inserte un vínculo a una dirección URL externa.

   * **[!UICONTROL Página de aterrizaje]**: inserte un vínculo a una página de aterrizaje. [Más información](../landing-pages/get-started-lp.md)

   * **[!UICONTROL Exclusión en un clic]**: inserte un vínculo para permitir a los usuarios cancelar rápidamente la suscripción a sus comunicaciones sin necesidad de confirmar la exclusión. [Más información](email-opt-out.md#one-click-opt-out).

   * **[!UICONTROL Inclusión/suscripción externa]**: inserte un vínculo para aceptar la recepción de comunicaciones de su marca.

   * **[!UICONTROL Exclusión/baja externa]**: inserte un vínculo para cancelar la suscripción y evitar recibir comunicaciones de su marca. Obtenga más información sobre la administración de exclusiones en [esta sección](email-opt-out.md#opt-out-management).

   * **[!UICONTROL Página espejo]**: Añada un vínculo para mostrar el contenido del correo electrónico en un explorador web. [Más información](#mirror-page)

1. Introduzca la dirección URL deseada en el campo correspondiente o seleccione una página de aterrizaje y defina la configuración y los estilos del vínculo. [Más información](#adjust-links)

   >[!NOTE]
   >
   >Para interpretar las direcciones URL, [!DNL Journey Optimizer] cumple con la sintaxis URI ([RFC 3986 estándar](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}), que deshabilita algunos caracteres internacionales especiales en las direcciones URL. Al intentar enviar la prueba o el correo electrónico, si se le devuelve un error que implica una dirección URL añadida al contenido, puede codificar la cadena como una solución alternativa.

1. Puede personalizar los vínculos. [Más información](../personalization/personalization-syntax.md#perso-urls)

1. Guarde los cambios.

1. Una vez creado el vínculo, aún puede modificarlo desde el **[!UICONTROL Configuración]** y **[!UICONTROL Estilos]** paneles a la derecha.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>Los mensajes de correo electrónico de tipo marketing deben incluir un [vínculo de no participación](../privacy/opt-out.md#opt-out-management), que no es necesaria para los mensajes transaccionales. La categoría del mensaje (**[!UICONTROL Marketing]** o **[!UICONTROL Transaccional]**) se define en la [superficie de canal](../configuration/channel-surfaces.md#email-type) al crear el mensaje.

## Ajustar vínculos {#adjust-links}

Puede realizar ajustes en los vínculos utilizando la variable **[!UICONTROL Configuración]** y **[!UICONTROL Estilos]** paneles a la derecha. Puede subrayar un vínculo, editar su color y seleccionar su destino.

1. En un componente de **[!UICONTROL Texto]** donde se inserta un vínculo, seleccione el vínculo.

1. Desde el **[!UICONTROL Configuración]** pestaña, elija cómo se redirigirá la audiencia con el **[!UICONTROL Target]** lista desplegable:

   * **[!UICONTROL Ninguna]**: abre el vínculo en el mismo marco en el que se hizo clic (predeterminado).
   * **[!UICONTROL En blanco]**: abre el vínculo en una nueva ventana o pestaña.
   * **[!UICONTROL Propio]**: abre el vínculo en el mismo marco en el que se hizo clic.
   * **[!UICONTROL Principal]**: abre el vínculo en el marco principal.
   * **[!UICONTROL Superior]**: abre el vínculo en todo el cuerpo de la ventana.

   ![](assets/link_2.png)

1. Marque **[!UICONTROL Subrayar vínculo]** para subrayar el texto de la etiqueta del vínculo.

   ![](assets/link_1.png)

1. Para cambiar el color del vínculo, haga clic en **[!UICONTROL Color del vínculo]** en la pestaña **[!UICONTROL Estilos]**.

   ![](assets/link_3.png)

1. Guarde los cambios.

## Vínculo a una página espejo {#mirror-page}

La página espejo es una página HTML a la que se puede acceder en línea mediante un navegador web. Su contenido es idéntico al contenido del correo electrónico.

Para añadir un vínculo a una página espejo en el correo electrónico, [insertar un vínculo](#insert-links) y seleccione **[!UICONTROL Página espejo]** como tipo de vínculo.

![](assets/message-tracking-mirror-page.png)

La página espejo se crea automáticamente.

>[!IMPORTANT]
>
>Los vínculos de páginas espejo se generan automáticamente y no se pueden editar. Contienen todos los datos personalizados cifrados necesarios para procesar el correo electrónico original. Como resultado, el uso de atributos personalizados con valores grandes puede generar direcciones URL de páginas espejo largas, lo que puede impedir que el vínculo funcione en exploradores web que tengan una longitud máxima de direcciones URL.

Una vez enviado el correo electrónico, cuando los destinatarios hacen clic en el vínculo de la página espejo, el contenido del correo electrónico se muestra en su navegador web predeterminado.

>[!NOTE]
>
>En el [prueba](../content-management/proofs.md) enviado a los perfiles de prueba, el vínculo a la página espejo no está activo. Solo se activa en los mensajes finales.

El período de retención de una página espejo es de 60 días. Después de este retraso, la página espejo ya no estará disponible.

## Administrar seguimiento {#manage-tracking}

El [Diseñador de correo electrónico](content-from-scratch.md) le permite administrar las direcciones URL rastreadas, como editar el tipo de seguimiento para cada vínculo.

1. Haga clic en **[!UICONTROL Vínculos]** del panel izquierdo para mostrar la lista de todas las direcciones URL del contenido de las que se realizará un seguimiento.

   Esta lista permite tener una vista centralizada y localizar cada URL en el contenido del correo electrónico.

1. Para editar un vínculo, haga clic en el icono de lápiz correspondiente.

1. Puede modificar el **[!UICONTROL Tipo de seguimiento]** si es necesario:

   ![](assets/message-tracking-edit-a-link.png)

   Para cada URL individual, puede definir el modo de seguimiento en uno de estos valores:

   * **[!UICONTROL Habilitado]**: activa el seguimiento en esta dirección URL.
   * **[!UICONTROL Exclusión]**: considera esta URL como una de exclusión o de baja.
   * **[!UICONTROL Página espejo]**: considera esta URL como una de página espejo.
   * **[!UICONTROL Nunca]**: nunca se activa el seguimiento de esta URL. <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

Los informes sobre aperturas y clics están disponibles en la [Informe en vivo](../reports/live-report.md) y en el [Informe global](../reports/global-report.md).

## Personalizar seguimiento de URL {#url-tracking}

Normalmente [Seguimiento de URL](email-settings.md#url-tracking) se administra en el nivel de superficie, pero no se admiten atributos de perfil. Actualmente la única manera de hacerlo es [personalizar direcciones URL](../personalization/personalization-syntax.md#perso-urls) en el diseñador de correo electrónico.

Para añadir parámetros de seguimiento de URL personalizados a los vínculos, siga los pasos a continuación.

1. Seleccione un vínculo y haga clic en **[!UICONTROL Insertar vínculo]** en la barra de herramientas contextual.

1. Seleccione el icono de personalización. Solo está disponible para estos tipos de vínculos: **Vínculo externo**, **Vínculo de baja** y **Opción de exclusión**.

   ![](assets/message-tracking-insert-link-perso.png)

1. Añada el parámetro de seguimiento de URL y seleccione el atributo de perfil que desee en el editor de expresiones.

   ![](assets/message-tracking-perso-parameter.png)

1. Guarde los cambios.

1. Repita los pasos anteriores para cada vínculo al que desee agregar este parámetro de seguimiento.

Ahora, cuando se envía el correo electrónico, este parámetro se anexa automáticamente al final de la dirección URL. A continuación, puede capturar este parámetro en las herramientas de análisis web o en los informes de rendimiento.

>[!NOTE]
>
>Para verificar la dirección URL final, puede hacer lo siguiente [enviar una prueba](../content-management/preview-test.md#send-proofs) y haga clic en el vínculo en el contenido del correo electrónico una vez que reciba la prueba. La dirección URL debe mostrar el parámetro de seguimiento. En el ejemplo anterior, la dirección URL final es: <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>
