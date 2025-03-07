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
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 34%

---

# Adición de vínculos y seguimiento de mensajes {#tracking}

Use [!DNL Journey Optimizer] para agregar vínculos al contenido y realizar un seguimiento de los mensajes enviados a fin de supervisar el comportamiento de los destinatarios.

## Habilitar seguimiento {#enable-tracking}

Puede habilitar el seguimiento en el nivel de mensaje de correo electrónico comprobando las opciones **[!UICONTROL Aperturas de correo electrónico]** o **[!UICONTROL Haga clic en el correo electrónico]** al crear su mensaje dentro de un recorrido o una campaña.

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

* **[!UICONTROL Aperturas del correo electrónico]**: Mensajes que se han abierto.
* **[!UICONTROL Clic en el correo electrónico]**: Hace clic en los vínculos de un correo electrónico.

## Inserción de vínculos {#insert-links}

Al diseñar un mensaje, puede agregar vínculos al contenido.

>[!NOTE]
>
>Cuando el seguimiento [está habilitado](#enable-tracking), se realiza un seguimiento de todos los vínculos incluidos en el contenido del mensaje.

Para insertar vínculos en el contenido del correo electrónico, siga los pasos a continuación:

1. Seleccione un elemento y haga clic en **[!UICONTROL Insertar vínculo]** en la barra de herramientas contextual.

   ![](assets/message-tracking-insert-link.png)

1. Elija el tipo de vínculo que desea crear:

   * **[!UICONTROL Vínculo externo]**: inserte un vínculo a una dirección URL externa.

   * **[!UICONTROL Página de aterrizaje]**: inserte un vínculo a una página de aterrizaje. [Más información](../landing-pages/get-started-lp.md)

   * **[!UICONTROL Exclusión en un clic]**: inserte un vínculo para permitir que los usuarios cancelen su suscripción rápidamente a sus comunicaciones sin necesidad de confirmar la exclusión. [Más información](email-opt-out.md#one-click-opt-out).

   * **[!UICONTROL Suscripción/inclusión externa]**: inserte un vínculo para aceptar la recepción de comunicaciones de su marca.

   * **[!UICONTROL Exclusión/baja externa]**: inserte un vínculo para cancelar la suscripción y evitar recibir comunicaciones de su marca. Obtenga más información sobre la administración de exclusiones en [esta sección](email-opt-out.md#opt-out-management).

   * **[!UICONTROL Página espejo]**: agregue un vínculo para mostrar el contenido del correo electrónico en un explorador web. [Más información](#mirror-page)

1. Introduzca la dirección URL deseada en el campo correspondiente o seleccione una página de aterrizaje y defina la configuración y los estilos del vínculo. [Más información](#adjust-links)

   >[!NOTE]
   >
   >Para interpretar las direcciones URL, [!DNL Journey Optimizer] cumple con la sintaxis de URI ([estándar RFC 3986](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}), que deshabilita algunos caracteres internacionales especiales en las direcciones URL. Al intentar enviar la prueba o el correo electrónico, si se le devuelve un error que implica una dirección URL añadida al contenido, puede codificar la cadena como una solución alternativa.

1. Puede personalizar los vínculos. [Más información](../personalization/personalization-syntax.md#perso-urls)

1. Guarde los cambios.

1. Una vez creado el vínculo, puedes modificarlo desde los paneles **[!UICONTROL Configuración]** y **[!UICONTROL Estilos]** de la derecha.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>Los mensajes de correo electrónico de tipo Marketing deben incluir un [vínculo de no participación](../privacy/opt-out.md#opt-out-management), que no es necesario para los mensajes transaccionales. La categoría del mensaje (**[!UICONTROL Marketing]** o **[!UICONTROL Transaccional]**) se define en la [configuración del canal](../configuration/channel-surfaces.md#email-type) al crear el mensaje.

## Ajustar vínculos {#adjust-links}

Puede realizar ajustes en los vínculos mediante los paneles **[!UICONTROL Configuración]** y **[!UICONTROL Estilos]** de la derecha. Puede subrayar un vínculo, editar su color y seleccionar su destino.

1. En un componente de **[!UICONTROL Texto]** donde se inserta un vínculo, seleccione el vínculo.

1. En la pestaña **[!UICONTROL Configuración]**, elige cómo se redirigirá a tu audiencia con la lista desplegable **[!UICONTROL Objetivo]**:

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

Para agregar un vínculo a una página espejo en el correo electrónico, [inserta un vínculo](#insert-links) y selecciona **[!UICONTROL Página espejo]** como tipo de vínculo.

![](assets/message-tracking-mirror-page.png)

La página espejo se crea automáticamente.

>[!IMPORTANT]
>
>Los vínculos de páginas espejo se generan automáticamente y no se pueden editar. Contienen todos los datos personalizados cifrados necesarios para procesar el correo electrónico original. Como resultado, el uso de atributos personalizados con valores grandes puede generar direcciones URL de páginas espejo largas, lo que puede impedir que el vínculo funcione en exploradores web que tengan una longitud máxima de direcciones URL.

Una vez enviado el correo electrónico, cuando los destinatarios hacen clic en el vínculo de la página espejo, el contenido del correo electrónico se muestra en su navegador web predeterminado.

>[!NOTE]
>
>En la [prueba](../content-management/proofs.md) enviada a los perfiles de prueba, el vínculo a la página espejo no está activo. Solo se activa en los mensajes finales.

El período de retención de una página espejo es de 60 días. Después de este retraso, la página espejo ya no estará disponible.

## Administrar seguimiento {#manage-tracking}

El [Diseñador de correo electrónico](content-from-scratch.md) le permite administrar las direcciones URL rastreadas, como editar el tipo de seguimiento para cada vínculo.

1. Haga clic en el icono **[!UICONTROL Vínculos]** del panel izquierdo para mostrar la lista de todas las direcciones URL del contenido de las que se realizará un seguimiento.

   Esta lista permite tener una vista centralizada y localizar cada URL en el contenido del correo electrónico.

1. Para editar un vínculo, haga clic en el icono de lápiz correspondiente.

1. Puede modificar el **[!UICONTROL Tipo de seguimiento]** si es necesario:

   ![](assets/message-tracking-edit-a-link.png)

   Para cada URL individual, puede definir el modo de seguimiento en uno de estos valores:

   * **[!UICONTROL Habilitado]**: activa el seguimiento en esta dirección URL.
   * **[!UICONTROL Exclusión]**: considera esta URL como una de exclusión o de baja.
   * **[!UICONTROL Página espejo]**: considera esta URL como una de página espejo.
   * **[!UICONTROL Nunca]**: Nunca activa el seguimiento de esta dirección URL.

Los informes sobre aperturas y clics están disponibles en [Live Report](../reports/live-report.md) y en [Customer Journey Analytics Report](../reports/report-gs-cja.md).

## Personalizar seguimiento de URL {#url-tracking}

Normalmente [el seguimiento de URL](email-settings.md#url-tracking) se administra en el nivel de configuración, pero no se admiten atributos de perfil. Actualmente, la única manera de hacerlo es [personalizar las direcciones URL](../personalization/personalization-syntax.md#perso-urls) en el diseñador de correo electrónico.

Para añadir parámetros de seguimiento de URL personalizados a los vínculos, siga los pasos a continuación.

1. Seleccione un vínculo y haga clic en **[!UICONTROL Insertar vínculo]** en la barra de herramientas contextual.

1. Seleccione el icono de personalización. Solo está disponible para estos tipos de vínculos: **vínculo externo**, **vínculo de baja** y **exclusión**.

   ![](assets/message-tracking-insert-link-perso.png)

1. Añada el parámetro de seguimiento de URL y seleccione el atributo de perfil que desee en el editor de personalización.

   ![](assets/message-tracking-perso-parameter.png)

1. Guarde los cambios.

1. Repita los pasos anteriores para cada vínculo al que desee agregar este parámetro de seguimiento.

Ahora, cuando se envía el correo electrónico, este parámetro se anexa automáticamente al final de la dirección URL. A continuación, puede capturar este parámetro en las herramientas de análisis web o en los informes de rendimiento.

>[!NOTE]
>
>Para comprobar la dirección URL final, puede [enviar una prueba](../content-management/preview-test.md#send-proofs) y hacer clic en el vínculo del contenido del correo electrónico una vez que reciba la prueba. La dirección URL debe mostrar el parámetro de seguimiento. En el ejemplo anterior, la dirección URL final será: <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>
