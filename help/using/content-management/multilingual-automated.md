---
solution: Journey Optimizer
product: journey optimizer
title: Introducción al contenido multilingüe
description: Obtenga más información sobre el contenido multilingüe en Journey Optimizer
feature: Multilingual
topic: Content Management
role: User
level: Beginner
keywords: introducción, inicio, contenido, experimento
hide: true
hidefromtoc: true
source-git-commit: 3b1acd7ada0637ce22e360e6e1bb35921dde2315
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 1%

---

# Creación de contenido multilingüe {#multilingual-automated}

La función multilingüe le permite crear contenido sin esfuerzo en varios idiomas dentro de una sola campaña. Con esta función, puede cambiar entre idiomas al editar la campaña, lo que optimiza todo el proceso de edición y mejora la capacidad para administrar de forma eficaz el contenido multilingüe.

## Crear configuración regional {#create-locale}

Al configurar los ajustes de idioma, tal como se describe en la sección [Cree la configuración de idioma](#language-settings) , si una configuración regional específica no está disponible para el contenido multilingüe, tiene la flexibilidad de crear tantas configuraciones regionales nuevas como sea necesario utilizando **[!UICONTROL Traducción]** menú.

1. Desde el **[!UICONTROL Administration]** menú, acceso **[!UICONTROL Canal]**.

   El menú de traducciones le permite acceder a la lista de configuraciones regionales activadas.

1. Desde el **[!UICONTROL Diccionario de configuración regional]** pestaña, haga clic en **[!UICONTROL Añadir configuración regional]**.

   ![](assets/locale_1.png)

1. Seleccione el código de configuración regional en la **[!UICONTROL Idioma]** y la lista asociada **[!UICONTROL Región]**.

1. Clic **[!UICONTROL Guardar]** para crear su configuración regional.

   ![](assets/locale_2.png)

## Creación del proyecto de traducción {#translation-project}

1. Desde el **[!UICONTROL Proyectos de traducción]** menú debajo de **[!UICONTROL Gestión de contenido]**, haga clic en **[!UICONTROL Crear proyecto]**.

1. Tipo de entrada a **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]**.

1. Seleccione el **[!UICONTROL Configuración regional de origen]**.

1. Seleccione si las traducciones se publican automáticamente después de la aprobación y si desea habilitar el flujo de trabajo de revisión.

1. Clic **[!UICONTROL Añadir configuración regional]** para acceder al menú y definir los idiomas de su proyecto de traducción.

   Si un **[!UICONTROL Configuración regional]** falta, puede crearlo manualmente de antemano desde el **[!UICONTROL Traducción]** o por API. Consulte [Crear nueva configuración regional](#create-locale).

1. Seleccione en la lista su **[!UICONTROL Configuración regional(es) de destino]** y elija cuál **[!UICONTROL Proveedor de traducción]** que desee utilizar para cada configuración regional.

1. Clic **[!UICONTROL Añadir una configuración regional]** cuando haya terminado de vincular la configuración regional de Target con el proveedor de traducción correcto.

1. Clic **[!UICONTROL Guardar]** cuando se configure el proyecto de traducción.

1. En el menú Avanzadas del proyecto de traducción, puede elegir Editarlo, desactivarlo o eliminarlo.

## Crear configuración de idioma {#language-settings}

En esta sección, puede establecer el idioma principal y sus configuraciones regionales asociadas para administrar el contenido multilingüe. También puede elegir el atributo que desee utilizar para buscar información relacionada con el idioma del perfil

1. Desde el **[!UICONTROL Administration]** menú, acceso **[!UICONTROL Canal]**.

1. En el **[!UICONTROL Configuración de idioma]** , haga clic en **[!UICONTROL Crear configuración de idioma]**.

1. Escriba el nombre de su **[!UICONTROL Configuración de idioma]**.

1. Elija la **[!UICONTROL Proyecto de traducción]** opción.

1. Desde el **[!UICONTROL Proyecto de traducción]** , haga clic en **[!UICONTROL Editar]** y elija el creado anteriormente **[!UICONTROL Proyecto de traducción]**.

   Las configuraciones regionales configuradas anteriormente se importan automáticamente. Si actualiza su **[!UICONTROL Proyecto de traducción]**, haga clic en **[!UICONTROL Actualizar]** para reflejar estos cambios en su **[!UICONTROL Configuración de idioma]**.

1. Desde el **[!UICONTROL Preferencia de envío]** , seleccione el atributo que desea buscar para encontrar información sobre los idiomas del perfil.

1. Clic **[!UICONTROL Editar]** junto a su **[!UICONTROL Configuración regional]** para personalizarlo aún más y para agregar **[!UICONTROL Preferencias de perfil]**.

1. Clic **[!UICONTROL Enviar]** para crear su **[!UICONTROL Configuración de idioma]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Creación de una campaña multilingüe {#create-multilingual-campaign}

1. Comience creando y configurando la campaña según sus necesidades. [Más información](../campaigns/create-campaign.md)

1. Vaya a **[!UICONTROL Acciones]** y seleccione. **[!UICONTROL Editar contenido]**.

1. Cree o importe el contenido original y personalícelo según sea necesario.

1. Una vez creado el contenido principal, haga clic en **[!UICONTROL Guardar]** y vuelva a la pantalla de configuración de la campaña.

1. Clic **[!UICONTROL Añadir idiomas]** y seleccione el creado anteriormente **[!UICONTROL Configuración de idioma]**. [Más información](#create-language-settings)

1. Acceda a la configuración avanzada de **[!UICONTROL Configuraciones regionales]** y seleccione **[!UICONTROL Copiar principal en todas las configuraciones regionales]**.

1. Ahora que el contenido principal está duplicado en el contenido seleccionado  **[!UICONTROL Configuraciones regionales]**, acceda a cada configuración regional y haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para traducir el contenido.

1. Puede optar por deshabilitar o habilitar las configuraciones regionales con el **[!UICONTROL Más acción]** del menú de la Configuración regional seleccionada.

1. Para desactivar la configuración multilingüe, haga clic en **[!UICONTROL Añadir idiomas]** y seleccione el idioma que desee conservar como idioma local.

1. Clic **[!UICONTROL Revisar para activar]** para mostrar un resumen de la campaña.

   El resumen le permite modificar la campaña si es necesario y comprobar si algún parámetro es incorrecto o falta.

1. Examine el contenido multilingüe para ver la renderización en cada idioma.

1. Compruebe que la campaña esté configurada correctamente y haga clic en **[!UICONTROL Activar]**.

La campaña está activada. El mensaje configurado en la campaña se envía inmediatamente o en la fecha especificada. Tenga en cuenta que, tan pronto como la campaña esté activa, no se puede modificar. Para reutilizar contenido, puede duplicar la campaña.

Una vez enviado, puede medir el impacto de las campañas en los informes de campañas.

## Informe de campaña multilingüe {#multilingual-campaign-report}

Informes globales, accesibles desde **Siempre** pestaña, muestra los eventos que se produjeron hace al menos dos horas y cubre los eventos durante un periodo de tiempo seleccionado. Se puede acceder al informe global de Campaign directamente desde la campaña con la variable **[!UICONTROL Ver informe]** botón.

Para obtener más información sobre los datos disponibles en el informe de Campaign, consulte [esta página](../reports/campaign-global-report.md).

+++Obtenga más información sobre las distintas métricas y widgets disponibles para su contenido multilingüe.

![](assets/report_multilingual.png)

El **[!UICONTROL Estadísticas de envío de correos electrónicos por idiomas]** widget detalla el éxito de su envío en función de sus **[!UICONTROL Configuraciones regionales]**:

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Estadísticas de seguimiento de correo electrónico por idiomas]** widget contiene los datos disponibles para la actividad de destinatario de su envío en función de su **[!UICONTROL Configuraciones regionales]**:

* **[!UICONTROL Cancela la suscripción]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido.
+++


<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.


-->
