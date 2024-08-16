---
solution: Journey Optimizer
product: journey optimizer
title: Creación de contenido multilingüe con traducción automática
description: Obtenga más información sobre el contenido multilingüe en Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: introducción, inicio, contenido, experimento
exl-id: 38e82eb2-67d9-4a7d-8c1f-77dab20bcec4
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 8484c39cf610fc4044e656243eba88deb8c50867
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 4%

---

# Creación de contenido multilingüe con traducción automática {#multilingual-automated}

>[!AVAILABILITY]
>
>Ahora mismo, el contenido multilingüe solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

Con el flujo automatizado, simplemente puede seleccionar el idioma de destino y el proveedor de idioma. A continuación, el contenido se envía directamente a la traducción, listo para una revisión final una vez finalizado.

Siga estos pasos para crear contenido multilingüe mediante traducción automática:

1. [Cree su configuración regional](#create-locale).

1. [Crear un proyecto de idioma](#create-translation-project).

1. [Crear configuración de idioma](#create-language-settings).

1. [Crear contenido multilingüe](#create-a-multilingual-campaign).

1. [Revise su tarea de traducción (opcional)](#review-translation-project).

## Crear configuración regional {#create-locale}

Al configurar los ajustes de idioma, como se describe en la sección [Crear la configuración de idioma](#language-settings), si no hay una configuración regional específica disponible para el contenido multilingüe, tiene la flexibilidad de crear tantas configuraciones regionales nuevas como sea necesario mediante el menú **[!UICONTROL Traducción]**.

1. Desde el menú **[!UICONTROL Administración de contenido]**, accede a **[!UICONTROL Traducción]**.

1. En la ficha **[!UICONTROL Diccionario local]**, haga clic en **[!UICONTROL Agregar configuración regional]**.

   ![](assets/locale_1.png)

1. Seleccione su código de configuración regional de la lista **[!UICONTROL Idioma]** y la **[!UICONTROL Región]** asociada.

1. Haga clic en **[!UICONTROL Guardar]** para crear su configuración regional.

   ![](assets/locale_2.png)

## Crear proyecto de traducción {#translation-project}

Inicie el proyecto de traducción especificando la configuración regional de Target e indicando el idioma o la región específicos para el contenido. A continuación, puede elegir su proveedor de traducción.

1. En el menú **[!UICONTROL Traducción]** de **[!UICONTROL Administración de contenido]**, haga clic en **[!UICONTROL Crear proyecto]** en la pestaña **[!UICONTROL Proyectos]**.

   ![](assets/translation_project_1.png)

1. Escriba un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]**.

1. Seleccione la **[!UICONTROL configuración regional de Source]**.

   ![](assets/translation_project_2.png)

1. Seleccione si desea activar las siguientes opciones:

   * **[!UICONTROL Publicar automáticamente traducciones aprobadas]**: una vez aprobadas las traducciones, se integran automáticamente en la campaña sin necesidad de intervención manual.
   * **[!UICONTROL Habilitar flujo de trabajo de revisión]**: solo aplicable a configuraciones regionales traducidas por humanos. Esto permite a un revisor interno evaluar y aprobar o rechazar de forma eficaz el contenido traducido. [Más información](#review-translation-project)

1. Haga clic en **[!UICONTROL Agregar configuración regional]** para acceder al menú y definir los idiomas de su proyecto de traducción.

   Si falta una **[!UICONTROL configuración regional]**, puede crearla manualmente de antemano desde el menú **[!UICONTROL Traducción]** o por API. Consulte [Crear nueva configuración regional](#create-locale).

   ![](assets/translation_project_3.png)

1. Seleccione en la lista sus **[!UICONTROL configuraciones regionales de destino]** y elija qué **[!UICONTROL proveedor de traducción]** desea usar para cada configuración regional.

   Se puede acceder a la configuración del **[!UICONTROL proveedor de traducción]** desde el menú **[!UICONTROL Traducción]** en la sección de menú **[!UICONTROL Administración]**.

   >[!NOTE]
   >
   >La administración de contratos con el proveedor de traducción está fuera del ámbito de esta función. Asegúrese de tener un contrato válido y activo con el socio de traducción designado.
   >
   ></br>El proveedor de traducción es propietario de la calidad del contenido traducido.

1. Haga clic en **[!UICONTROL Agregar configuración regional]** cuando termine de vincular la configuración regional de Target con el proveedor de traducción correcto. A continuación, haga clic en **[!UICONTROL Guardar]**.

   Tenga en cuenta que si un proveedor está atenuado para una configuración regional de destino, indica que el proveedor no admite esa configuración regional en particular.

   ![](assets/translation_project_4.png)

1. Haga clic en **[!UICONTROL Guardar]** cuando su proyecto de traducción esté configurado.

El proyecto de traducción se ha creado y se puede utilizar en una campaña multilingüe.

## Crear configuración de idioma {#language-settings}

En esta sección, puede establecer el idioma principal y sus configuraciones regionales asociadas para administrar el contenido multilingüe. También puede elegir el atributo que desea utilizar para buscar información relacionada con el idioma del perfil.

1. Desde el menú **[!UICONTROL Administración]**, accede al **[!UICONTROL Canal]**.

1. En el menú **[!UICONTROL Configuración de idioma]**, haga clic en **[!UICONTROL Crear configuración de idioma]**.

   ![](assets/language_settings_1.png)

1. Escriba el nombre de su **[!UICONTROL configuración de idioma]**.

1. Elija la opción **[!UICONTROL Proyecto de traducción]**.

1. En el campo **[!UICONTROL Proyecto de traducción]**, haga clic en **[!UICONTROL Editar]** y elija el **[!UICONTROL proyecto de traducción]** que creó anteriormente.

   Las configuraciones regionales configuradas anteriormente se importan automáticamente.

   ![](assets/language_settings_2.png)

1. En el menú **[!UICONTROL Preferencia de envío]**, seleccione el atributo que desee buscar para encontrar información sobre los idiomas del perfil.

1. Haga clic en **[!UICONTROL Editar]** junto a su **[!UICONTROL configuración regional]** para personalizarla más y agregar **[!UICONTROL preferencias de perfil]**.

   ![](assets/language_settings_3.png)

1. Si tu **[!UICONTROL proyecto de traducción]** se ha actualizado, haz clic en **[!UICONTROL Actualizar]** para reflejar estos cambios en tu **[!UICONTROL configuración de idioma]**.

   ![](assets/language_settings_4.png)

1. Haz clic en **[!UICONTROL Enviar]** para crear tu **[!UICONTROL configuración de idioma]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.


1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Creación de contenido multilingüe {#create-multilingual-campaign}

Una vez que haya configurado el proyecto de traducción y la configuración de idioma, estará listo para crear la campaña o el recorrido y personalizar el contenido para las diferentes configuraciones regionales.

1. Comience creando y configurando su notificación por correo electrónico, SMS o push [campaign](../campaigns/create-campaign.md) o [recorrido](../building-journeys/journeys-message.md) según sus necesidades.

1. Una vez creado el contenido principal, haz clic en **[!UICONTROL Guardar]** y vuelve a la pantalla de configuración de la campaña.

1. Haga clic en **[!UICONTROL Agregar idiomas]**.  [Más información](#create-language-settings)

   ![](assets/multilingual-campaign-automated-1.png)

1. Seleccione la **[!UICONTROL configuración de idioma]** creada anteriormente.

   ![](assets/multilingual-campaign-automated-2.png)

1. Ahora que sus configuraciones regionales están importadas, haga clic en **[!UICONTROL Enviar para traducir]** para reenviar el contenido al proveedor de traducción seleccionado anteriormente.

   ![](assets/multilingual-campaign-automated-3.png)

1. Una vez enviado el contenido para su traducción, ya no se puede editar. Para realizar cambios en el contenido original, haga clic en el icono de candado.

   Tenga en cuenta que si desea realizar alguna modificación en este contenido, debe crear un nuevo proyecto de traducción y reenviarlo para su traducción.

   ![](assets/multilingual-campaign-automated-4.png)

1. Haga clic en **[!UICONTROL Abrir traducción]** para acceder a su proyecto de traducción y revisarlo.

   ![](assets/multilingual-campaign-automated-5.png)

1. En esta página, siga el estado del proyecto de traducción:

   * **[!UICONTROL Traducción en curso]**: su proveedor de servicios está trabajando activamente en la traducción.

     Si seleccionaste **Insourcing** al configurar tu **configuración de idioma**, puedes traducir el contenido directamente en tu proyecto de traducción. [Más información](#manage-ht-project)

   * **[!UICONTROL Listo para revisión]**: el proceso de revisión está listo para comenzar, lo que le permite tener acceso a la traducción y rechazarla o aprobarla.

     Si seleccionó **[!UICONTROL Habilitar flujo de trabajo de revisión]** en su **[!UICONTROL proyecto de traducción]**, puede revisar la traducción directamente en Journey Optimizer después de que el proveedor de traducción seleccionado la haya completado. [Más información](#review-translation-project)

   * **[!UICONTROL Revisado]**: la traducción se aprobó, está lista para publicarse y se enviará a la campaña.

   * **[!UICONTROL Listo para publicar]**: la traducción automática se completó y ahora se puede enviar a su campaña.

   * **[!UICONTROL Completado]**: la traducción ya está disponible en su campaña.

   ![](assets/multilingual-campaign-automated-6.png)

1. Una vez finalizada la traducción, el contenido multilingüe está listo para enviarse.

   ![](assets/translation_review_9.png)

1. Haga clic en **[!UICONTROL Revisar para activar]** y mostrar un resumen de la campaña.

   El resumen le permite modificar la campaña si es necesario y comprobar si algún parámetro es incorrecto o falta.

1. Examine el contenido multilingüe para ver la renderización en cada idioma.

   ![](assets/multilingual-campaign-automated-7.png)

1. Compruebe que la campaña esté configurada correctamente y luego haga clic en **[!UICONTROL Activar]**.

Ahora puede activar la campaña o el recorrido. Una vez enviada, puede medir el impacto del recorrido o la campaña multilingüe dentro de los informes.

## Administrar el abastecimiento de proyectos de traducción {#manage-ht-project}

Si seleccionó la opción Abastecimiento al configurar los ajustes de Idioma, puede traducir el contenido directamente en el proyecto de traducción.

1. Desde tu **[!UICONTROL proyecto de traducción]**, accede al menú **[!UICONTROL Más acciones]** y selecciona **[!UICONTROL Abastecimiento]**.

   ![](assets/inhouse-translation-1.png)

1. Puede exportar el archivo CSV para su traducción mediante un software de traducción externo. También puede volver a importar el archivo CSV en su proyecto de traducción haciendo clic en el botón **[!UICONTROL Importar CSV]**.

   ![](assets/inhouse-translation-3.png)

1. Haga clic en **[!UICONTROL Editar]** para agregar el contenido de la traducción.

   ![](assets/inhouse-translation-2.png)

1. Si está listo para publicar el texto traducido, haga clic en **[!UICONTROL Finalizar]**.

## Revisión del proyecto de traducción {#review-translation-project}

Si seleccionó **[!UICONTROL Habilitar flujo de trabajo de revisión]** en su **[!UICONTROL proyecto de traducción]**, puede revisar la traducción directamente en Journey Optimizer después de que el proveedor de traducción seleccionado la haya completado.

Tenga en cuenta que si esta opción está deshabilitada, una vez que su proveedor haya finalizado la traducción, el estado de la tarea de traducción se establece automáticamente en **[!UICONTROL Revisado]**, lo que le permite continuar rápidamente haciendo clic en **[!UICONTROL Publish]**.

1. Una vez que tu proveedor de servicios haya completado la traducción, puedes acceder a la traducción para revisarla desde tu **[!UICONTROL proyecto de traducción]** o directamente desde tu **[!UICONTROL Campaña]**.

   En el menú **[!UICONTROL Más acciones]**, haga clic en **[!UICONTROL Revisar]**.

   ![](assets/translation_review_1.png)

1. En la ventana Revisar, examine el contenido traducido y acepte o rechace cada cadena de traducción.

   ![](assets/translation_review_3.png)

1. Haga clic en **[!UICONTROL Editar]** para cambiar el contenido de la cadena de traducción.

   ![](assets/translation_review_2.png)

1. Escriba la traducción actualizada y haga clic en **[!UICONTROL Confirmar]** cuando termine.

   ![](assets/translation_review_4.png)

1. También puede elegir **[!UICONTROL Rechazar todo]** o **[!UICONTROL Aprobar todo]** directamente.

   Al seleccionar **[!UICONTROL Rechazar todo]**, agregue un comentario y haga clic en **[!UICONTROL Rechazar]**.

1. Haga clic en **[!UICONTROL Vista previa]** para comprobar la renderización del contenido traducido en cada idioma.

1. Si está listo para publicar el texto traducido, haga clic en **[!UICONTROL Finalizar]**.

   ![](assets/translation_review_5.png)

1. Desde tu **[!UICONTROL proyecto de traducción]**, selecciona uno de tu proyecto para acceder a más detalles. Si rechazó la traducción, puede elegir enviarla de nuevo a la traducción.

   ![](assets/translation_review_6.png)

1. Una vez que el estado de **[!UICONTROL proyecto de traducción]** se haya establecido en Revisado, puede enviarlo a su campaña.

   En el menú **[!UICONTROL Más acciones]**, haga clic en **[!UICONTROL Publish]**.

   ![](assets/translation_review_7.png)

1. En su campaña, compruebe que su estado de traducción haya cambiado a **[!UICONTROL Traducción completada]**. Ahora puede enviar su contenido multilingüe; consulte el paso 10 de [esta sección](#create-multilingual-campaign).

   ![](assets/translation_review_9.png)

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.


-->
