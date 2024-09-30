---
solution: Journey Optimizer
product: journey optimizer
title: Prueba del contenido con datos de entrada de muestra
description: Obtenga información sobre cómo previsualizar el contenido del correo electrónico y enviar pruebas con datos de entrada de ejemplo.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 100c9ca994199a3b90650ebfbabbf0b7ac8726c2
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 7%

---


# Prueba del contenido con datos de entrada de muestra {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simular mediante entrada de muestra"
>abstract="En esta pantalla, puede probar diferentes variantes del contenido del correo electrónico proporcionando valores para los campos de personalización a través de una plantilla CSV (descargar CSV) o introduciendo manualmente los valores."

>[!AVAILABILITY]
>
>Actualmente, esta función está disponible como una versión beta solo para usuarios seleccionados.

Recorrido Optimizer le permite probar diferentes variantes del contenido del correo electrónico previsualizándolo y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV o añadidos manualmente. El sistema detecta automáticamente todos los atributos de perfiles utilizados en el contenido para la personalización y los puede utilizar en las pruebas para crear varias variantes.

Para acceder a esta experiencia, haga clic en el botón **[!UICONTROL Simular contenido]** y elija **[!UICONTROL Simular con CSV(Beta)]**.

![](assets/simulate-sample.png)

Los pasos principales para probar el contenido son los siguientes:

1. Añada hasta 30 variantes con datos de entrada de ejemplo, ya sea cargando un archivo CSV o añadiendo datos manualmente. [Aprenda a agregar variantes](#profiles)
1. Compruebe la previsualización del contenido con las diferentes variantes. [Obtenga información sobre cómo obtener una vista previa del contenido](#preview)
1. Envíe hasta 10 pruebas a direcciones de correo electrónico utilizando las diferentes variantes. [Aprenda a enviar pruebas](#proofs)


## Mecanismos de protección y limitaciones {#limitations}

Antes de empezar a probar el contenido con datos de entrada de ejemplo, tenga en cuenta las siguientes protecciones y requisitos previos.

* A partir de ahora, las pruebas con datos de entrada de muestra solo están disponibles para el canal de correo electrónico. No se puede acceder a la experiencia desde el botón &quot;Simular contenido&quot; dentro de Email Designer.
* Las siguientes funciones no están disponibles en la experiencia actual: Renderización de la bandeja de entrada, informes de correo no deseado, contenido multilingüe y experimento de contenido. Para usar estas características, selecciona el botón **[!UICONTROL Simular contenido]** de tu contenido para acceder a la interfaz de usuario anterior.
* Actualmente solo se admiten atributos de perfil. Si se utilizan atributos contextuales en el contenido para la personalización, no se puede probar el contenido con estos atributos.
* Solo se admiten los siguientes tipos de datos al introducir datos para las variantes: número (entero y decimal), cadena, booleano y tipo de fecha. Cualquier otro tipo de datos mostrará un error.

## Añadir variantes {#profiles}

Puede añadir hasta 30 variantes para probar el contenido, ya sea mediante un archivo CSV o manualmente:

* Para cargar datos de entrada de ejemplo desde un archivo CSV, haga clic en el vínculo **[!UICONTROL descargar CSV]** para recuperar una plantilla de archivo CSV. Estas plantillas incluyen una columna para cada atributo de perfil utilizado en el contenido para la personalización.

  Rellene el archivo CSV y, a continuación, haga clic en **[!UICONTROL Cargar datos de entrada]** para cargarlos y probar el contenido.

* Para agregar una variante manualmente, haga clic en el botón **[!UICONTROL Crear entrada de ejemplo]** y rellene los datos de entrada de ejemplo para la variante. Se muestra un campo para cada atributo de perfil utilizado en el contenido para la personalización.

  ![](assets/simulate-custom-add.png)

Una vez seleccionados los perfiles, aparece un cuadro para cada variante en la parte izquierda de la pantalla. Puede utilizar estos perfiles para previsualizar el contenido y enviar pruebas.

>[!NOTE]
>
>Las variantes agregadas solo sirven como propósitos de prueba para el contenido actual. Los no se almacenan en Adobe Experience Platform, sino en la sesión del explorador del usuario, lo que significa que no se mostrarán al cerrar sesión o si se trabaja desde otro dispositivo.

## Previsualización de las variantes de contenido {#preview}

Para obtener una vista previa del contenido mediante una de las variantes, seleccione el cuadro correspondiente para actualizar la vista previa del contenido en la sección derecha con la información introducida para esta variante.

Puede quitar una variante en cualquier momento con el botón de los tres puntos de la esquina superior derecha y seleccionando **[!UICONTROL Quitar]**. Para editar la información de una variante, haga clic en el botón de puntos suspensivos y seleccione **[!UICONTROL Editar]**.

![](assets/simulate-custom-boxes.png)

## Envío de pruebas {#proofs}

Journey Optimizer le permite enviar pruebas a las direcciones de correo electrónico mientras suplanta una o varias variantes que haya agregado en la pantalla de simulación. Los pasos son los siguientes:

1. Compruebe que se hayan agregado variantes para probar el contenido y haga clic en el botón **[!UICONTROL Enviar prueba]**.

1. En el campo **[!UICONTROL Destinatarios]**, escriba la dirección de correo electrónico a la que desea enviar la prueba y haga clic en **[!UICONTROL Agregar]**. Repita la operación para enviar la prueba a direcciones de correo electrónico adicionales. Puede añadir hasta 10 destinatarios de prueba.

1. En la sección inferior de la pantalla, seleccione la variante que desee utilizar en la prueba. Puede seleccionar varias variantes, en cuyo caso el correo electrónico incluirá tantas pruebas como variantes seleccionadas.

   Para obtener más información sobre una variante, seleccione el vínculo **[!UICONTROL Ver detalles del perfil]**. Esto le permite mostrar la información introducida en la pantalla anterior para las diferentes variantes.

   ![](assets/simulate-custom-proofs.png)

1. Haga clic en el botón **[!UICONTROL Enviar prueba]** para comenzar a enviar la prueba.

1. Para realizar un seguimiento del envío de prueba, haga clic en el botón **[!UICONTROL Ver pruebas]** en la pantalla de simular contenido.

![](assets/simulate-custom-sent-proofs.png)
