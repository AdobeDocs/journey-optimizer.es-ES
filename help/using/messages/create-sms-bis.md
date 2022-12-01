---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un mensaje SMS
description: Obtenga información sobre cómo crear un mensaje SMS en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 5e5b078fa61e2c615a2242f50439c2f20ea5216a
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 7%

---

# Creación de un mensaje SMS {#create-sms-bis}

>[!NOTE]
>
>De acuerdo con las normas y los reglamentos del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Para ello, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión.

## Creación de un mensaje SMS en un recorrido o campaña

Para empezar a personalizar el mensaje SMS, siga estos pasos:

>[!BEGINTABS]

>[!TAB Añadir un mensaje SMS a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad SMS desde la sección Acciones de la paleta.

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie del mensaje que desea utilizar.

   Para obtener más información sobre cómo configurar un recorrido, consulte.

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el **[!UICONTROL Editar contenido]** botón.

>[!TAB Añadir un mensaje SMS a una campaña]

1. Cree una nueva campaña programada o activada por la API, seleccione **[!UICONTROL SMS]** como su acción y elija el **[!UICONTROL Superficie de la aplicación]** para usar.

1. Haga clic en **[!UICONTROL Crear]**.

1. En el **[!UICONTROL Propiedades]** , edite la **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

1. En el **[!UICONTROL Seguimiento de acciones]** , especifique si desea rastrear los clics en los vínculos de su mensaje SMS.

1. Haga clic en el **[!UICONTROL Seleccionar la audiencia]** para definir la audiencia a la que se dirigirá desde la lista de segmentos de Adobe Experience Platform disponibles.

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o con una frecuencia recurrente. Obtenga información sobre cómo configurar la variable **[!UICONTROL Programación]** de su campaña en.

1. En el **[!UICONTROL Déclencheur de acción]** , seleccione **[!UICONTROL Frecuencia]** de su mensaje SMS:

   * Una vez
   * Diario
   * Semanal
   * Mes

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el **[!UICONTROL Editar contenido]** botón.

>[!ENDTABS]

## Definir el contenido del SMS

1. En la pantalla de configuración de recorrido o de campaña, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido del SMS.

1. Haga clic en el **[!UICONTROL Mensaje]** para abrir el editor de expresiones.

1. Utilice el editor de expresiones para definir contenido y añadir contenido dinámico. Puede utilizar cualquier atributo, como el nombre del perfil o la ciudad.

1. Haga clic en **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa.

1. Cuando el mensaje SMS esté listo, complete la configuración de su para enviarlo.

## Validar el SMS

>[!NOTE]
>
> Para mejorar la capacidad de envío, siempre debe utilizar los números de teléfono en los formatos admitidos por el proveedor. Por ejemplo, Twilio y Sinch solo admiten números de teléfono en formato E.164.

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo. Si ha insertado, puede comprobar cómo se muestra este contenido en el mensaje mediante los datos de perfil de prueba.

Para visualizar la visualización de su mensaje SMS en dispositivos móviles, haga clic en el botón **[!UICONTROL Simular contenido]** pestaña . Obtenga más información sobre la simulación de contenido en .

También debe comprobar las alertas en la sección superior del editor.  Algunas de ellas son simples advertencias, pero otras pueden impedir que utilice el mensaje. Obtenga más información en.
