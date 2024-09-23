---
solution: Journey Optimizer
product: journey optimizer
title: Prueba del contenido con perfiles personalizados
description: Obtenga información sobre cómo obtener una vista previa del contenido y enviar pruebas mediante perfiles personalizados.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6229f295b961b0535139b64928216e40c3759947
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 1%

---


# Prueba del contenido con perfiles personalizados {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulación mediante perfiles personalizados"
>abstract="En esta pantalla, puede obtener una vista previa del contenido y enviar pruebas al suplantar perfiles personalizados que puede cargar desde un archivo CSV o agregar manualmente directamente desde esta pantalla."

>[!AVAILABILITY]
>
>Actualmente, esta función está disponible como una versión beta solo para usuarios seleccionados.
>
>La renderización de la bandeja de entrada y los informes de spam no están disponibles en la experiencia actual. Para usar estas características, selecciona el botón **[!UICONTROL Simular contenido]** de tu contenido para acceder a la interfaz de usuario heredada.

Recorrido Optimizer le permite previsualizar y probar el contenido mediante perfiles personalizados que puede cargar desde un archivo CSV o añadir manualmente al simular el contenido.

Para acceder a esta experiencia, haga clic en el botón **[!UICONTROL Simular contenido]** y elija **[!UICONTROL Simular con CSV(Beta)]**.

Esta pantalla le permite seleccionar perfiles para utilizarlos para previsualizar el contenido y enviar pruebas. El sistema detecta automáticamente todos los atributos utilizados en el contenido para la personalización y los puede utilizar para sus pruebas.

Los pasos principales para probar el contenido son los siguientes:

1. Añada perfiles personalizados, ya sea cargando un archivo CSV o añadiéndolos uno a uno manualmente. [Aprenda a agregar perfiles personalizados](#profiles)
1. Compruebe la previsualización del contenido con los perfiles añadidos. [Obtenga información sobre cómo obtener una vista previa del contenido](#preview)
1. Envíe hasta 10 pruebas a las direcciones de correo electrónico mientras suplanta los perfiles personalizados deseados. [Aprenda a enviar pruebas](#proofs)


## Añadir perfiles personalizados {#profiles}

Puede añadir perfiles personalizados para probar el contenido mediante un archivo CSV o manualmente:

* Para cargar perfiles desde un archivo CSV, haga clic en el vínculo **[!UICONTROL Descargar plantilla]** para recuperar una plantilla de archivo CSV. Estas plantillas incluyen una columna para cada atributo de personalización utilizado en el contenido.

  Rellene el archivo CSV y, a continuación, haga clic en **[!UICONTROL Cargar perfiles de muestra]** para cargarlo y probar el contenido.

* Para agregar un perfil manualmente, haga clic en el botón **[!UICONTROL Crear perfil de muestra]** y rellene la información del perfil. Se muestra un campo para cada atributo de personalización utilizado en el contenido.

  ![](assets/simulate-custom-add.png)

Una vez seleccionados los perfiles, aparece un cuadro para cada perfil en la parte izquierda de la pantalla. Puede utilizar estos perfiles para previsualizar el contenido y enviar pruebas.

## Previsualización del contenido mediante perfiles personalizados {#preview}

Para obtener una vista previa del contenido mediante uno de los perfiles, seleccione el cuadro correspondiente para actualizar la vista previa del contenido en la sección derecha con la información introducida para este perfil.

Puede quitar un cuadro en cualquier momento con el botón de los tres puntos de la esquina superior derecha y seleccionando **[!UICONTROL Quitar]**. Para editar la información de un perfil, haga clic en el botón de puntos suspensivos y seleccione **[!UICONTROL Editar]**.

![](assets/simulate-custom-boxes.png)

## Envío de pruebas {#proofs}

Journey Optimizer permite enviar pruebas a las direcciones de correo electrónico mientras suplanta uno o varios perfiles personalizados que ha añadido en la pantalla de simulación. Los pasos son los siguientes:

1. Compruebe que se hayan agregado perfiles personalizados para probar el contenido y haga clic en el botón **[!UICONTROL Enviar prueba]**.

1. En el campo **[!UICONTROL Destinatarios]**, escriba la dirección de correo electrónico a la que desea enviar la prueba y haga clic en **[!UICONTROL Agregar]**. Repita la operación para enviar la prueba a direcciones de correo electrónico adicionales. Puede añadir hasta 10 destinatarios de prueba.

1. En la sección inferior de la pantalla, seleccione los perfiles personalizados que desea suplantar en la prueba. Puede seleccionar varios perfiles, en cuyo caso el correo electrónico incluirá tantas pruebas como perfiles seleccionados.

   ![](assets/simulate-custom-proofs.png)

1. Haga clic en el botón **[!UICONTROL Enviar prueba]** para comenzar a enviar la prueba.

Puede hacer un seguimiento del envío en cualquier momento haciendo clic en el botón **[!UICONTROL Ver pruebas]** en la pantalla Simular contenido.

![](assets/simulate-custom-sent-proofs.png)
