---
solution: Journey Optimizer
product: journey optimizer
title: Prueba del contenido mediante perfiles de muestra
description: Obtenga información sobre cómo previsualizar el contenido del correo electrónico y enviar pruebas mediante perfiles de muestra.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6b3518645b9cbfbe6f728011b0889c28fa754496
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Prueba del contenido mediante perfiles de muestra {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulación mediante perfiles de muestra"
>abstract="En esta pantalla, puede obtener una vista previa del contenido del correo electrónico y enviar pruebas mientras suplanta perfiles de muestra que puede cargar desde un archivo CSV o agregar manualmente desde esta pantalla."


<!--ATTENTE CONFIRMATION 

- nom (custom/sample)
- campaigns/journeys ou que campaigns

-->

>[!AVAILABILITY]
>
>Actualmente, esta función está disponible como una versión beta solo para usuarios seleccionados.

Recorrido Optimizer le permite previsualizar y probar el contenido de los correos electrónicos mediante perfiles de muestra que puede cargar desde un archivo CSV o añadir manualmente al simular el contenido. Esta función le permite seleccionar perfiles de muestra para utilizarlos para previsualizar el contenido y enviar pruebas. El sistema detecta automáticamente todos los atributos de perfiles utilizados en el contenido para su personalización y los puede utilizar para sus pruebas.

Para acceder a esta experiencia, haga clic en el botón **[!UICONTROL Simular contenido]** y elija **[!UICONTROL Simular con CSV(Beta)]**.

![](assets/simulate-sample.png)


Los pasos principales para probar el contenido son los siguientes:

1. Añada hasta 30 perfiles de muestra, ya sea cargando un archivo CSV o añadiéndolos uno a uno manualmente. [Aprenda a agregar perfiles de muestra](#profiles)
1. Compruebe la previsualización del contenido con los perfiles añadidos. [Obtenga información sobre cómo obtener una vista previa del contenido](#preview)
1. Envíe hasta 10 pruebas a las direcciones de correo electrónico mientras suplanta los perfiles de muestra deseados. [Aprenda a enviar pruebas](#proofs)


## Mecanismos de protección y limitaciones {#limitations}

Antes de empezar a probar el contenido con perfiles de muestra, tenga en cuenta las siguientes protecciones y requisitos previos.

* Por ahora, la prueba con perfiles de muestra solo está disponible dentro de las campañas y para el canal de correo electrónico.
* Las siguientes funciones no están disponibles en la experiencia actual: Renderización de la bandeja de entrada, informes de correo no deseado, contenido multilingüe y experimento de contenido. Para usar estas características, selecciona el botón **[!UICONTROL Simular contenido]** de tu contenido para acceder a la interfaz de usuario anterior.
* Actualmente solo se admiten atributos de perfil. Si se utilizan atributos contextuales en el contenido para la personalización, no se puede probar el contenido con estos atributos.
* Solo se admiten los siguientes tipos de datos al introducir datos para los perfiles de muestra: número (entero y decimal), cadena, booleano y tipo de fecha. Cualquier otro tipo de datos mostrará un error.

## Añadir perfiles de muestra {#profiles}

Puede añadir hasta 30 perfiles de muestra para probar el contenido mediante un archivo CSV o manualmente:

* Para cargar perfiles desde un archivo CSV, haga clic en el vínculo **[!UICONTROL Descargar plantilla]** para recuperar una plantilla de archivo CSV. Estas plantillas incluyen una columna para cada atributo de perfil utilizado en el contenido para la personalización.

  Rellene el archivo CSV y, a continuación, haga clic en **[!UICONTROL Cargar perfiles de muestra]** para cargarlo y probar el contenido.

* Para agregar un perfil manualmente, haga clic en el botón **[!UICONTROL Crear perfil de muestra]** y rellene la información del perfil. Se muestra un campo para cada atributo de perfil utilizado en el contenido para la personalización.

  ![](assets/simulate-custom-add.png)

Una vez seleccionados los perfiles, aparece un cuadro para cada perfil en la parte izquierda de la pantalla. Puede utilizar estos perfiles para previsualizar el contenido y enviar pruebas.

>[!NOTE]
>
>Los perfiles de muestra agregados solo sirven como propósitos de prueba para el contenido actual. Los no se almacenan en Adobe Experience Platform, sino en la sesión del explorador del usuario, lo que significa que no se mostrarán al cerrar sesión o si se trabaja desde otro dispositivo.

## Previsualización del contenido mediante perfiles de muestra {#preview}

Para obtener una vista previa del contenido mediante uno de los perfiles, seleccione el cuadro correspondiente para actualizar la vista previa del contenido en la sección derecha con la información introducida para este perfil.

Puede quitar un cuadro en cualquier momento con el botón de los tres puntos de la esquina superior derecha y seleccionando **[!UICONTROL Quitar]**. Para editar la información de un perfil, haga clic en el botón de puntos suspensivos y seleccione **[!UICONTROL Editar]**.

![](assets/simulate-custom-boxes.png)

## Envío de pruebas {#proofs}

Journey Optimizer le permite enviar pruebas a las direcciones de correo electrónico mientras suplanta uno o varios perfiles de muestra que haya agregado en la pantalla de simulación. Los pasos son los siguientes:

1. Compruebe que se hayan agregado perfiles de muestra para probar el contenido y haga clic en el botón **[!UICONTROL Enviar prueba]**.

1. En el campo **[!UICONTROL Destinatarios]**, escriba la dirección de correo electrónico a la que desea enviar la prueba y haga clic en **[!UICONTROL Agregar]**. Repita la operación para enviar la prueba a direcciones de correo electrónico adicionales. Puede añadir hasta 10 destinatarios de prueba.

1. En la sección inferior de la pantalla, seleccione los perfiles de muestra que desea suplantar en la prueba. Puede seleccionar varios perfiles, en cuyo caso el correo electrónico incluirá tantas pruebas como perfiles seleccionados.

   Para obtener más información sobre un perfil, selecciona el vínculo **[!UICONTROL Ver detalles del perfil]**. Esto le permite mostrar la información introducida en la pantalla anterior para los distintos atributos de perfil.

   ![](assets/simulate-custom-proofs.png)

1. Haga clic en el botón **[!UICONTROL Enviar prueba]** para comenzar a enviar la prueba.

Puede hacer un seguimiento del envío en cualquier momento haciendo clic en el botón **[!UICONTROL Ver pruebas]** en la pantalla Simular contenido.

![](assets/simulate-custom-sent-proofs.png)
