---
solution: Journey Optimizer
product: journey optimizer
title: Prueba del contenido con datos de entrada de ejemplo (Beta)
description: Obtenga información sobre cómo obtener una vista previa del contenido y enviar una prueba por correo electrónico con datos de entrada de ejemplo de un archivo CSV o JSON o añadidos manualmente.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
source-git-commit: 678a2fbce1b4048aad6a2214bb41ec3722db2b2d
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 1%

---


# Prueba del contenido con datos de entrada de ejemplo (Beta) {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simular mediante entrada de muestra"
>abstract="En esta pantalla, puede probar diferentes variantes del contenido proporcionando valores para los campos de personalización a través de una plantilla CSV o JSON, o introduciendo los valores manualmente."

>[!AVAILABILITY]
>
>Actualmente, esta función está disponible para todos los clientes como una versión beta pública.

Recorrido Optimizer le permite probar diferentes variantes del contenido previsualizándolo y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV o JSON o añadidos manualmente. El sistema detecta automáticamente todos los atributos de perfiles utilizados en el contenido para la personalización y los puede utilizar en las pruebas para crear varias variantes.

>[!NOTE]
>
>Por ahora, la simulación de variaciones de contenido solo está disponible para los canales de correo electrónico, SMS y notificaciones push.

Para tener acceso a esta experiencia, haga clic en el botón **[!UICONTROL Simular contenido]** y elija **[!UICONTROL Simular variaciones de contenido (Beta)]**.

![](assets/simulate-sample.png)

Los pasos principales para probar el contenido son los siguientes:

1. Añada hasta 30 variantes con datos de entrada de ejemplo, ya sea cargando un archivo o agregando datos manualmente. [Aprenda a agregar variantes](#profiles)
1. Compruebe la previsualización del contenido con las diferentes variantes. [Obtenga información sobre cómo obtener una vista previa del contenido](#preview)
1. Para el contenido de correo electrónico, envíe hasta 10 pruebas a las direcciones de correo electrónico utilizando las diferentes variantes. [Aprenda a enviar pruebas](#proofs)


## Mecanismos de protección y limitaciones {#limitations}

Antes de empezar a probar el contenido con datos de entrada de ejemplo, tenga en cuenta las siguientes protecciones y requisitos previos.

* A partir de ahora, las pruebas con datos de entrada de muestra solo están disponibles para los canales de correo electrónico, SMS y notificaciones push. No se puede acceder a la experiencia desde el botón &quot;Simular contenido&quot; dentro de Email Designer.
* Las siguientes funciones no están disponibles en la experiencia actual: Renderización de la bandeja de entrada, informes de correo no deseado, contenido multilingüe y experimento de contenido. Para usar estas características, selecciona el botón **[!UICONTROL Simular contenido]** de tu contenido para acceder a la interfaz de usuario anterior.
* Actualmente solo se admiten atributos de perfil. Si se utilizan atributos contextuales en el contenido para la personalización, no se puede probar el contenido con estos atributos.
* Solo se admiten los siguientes tipos de datos al introducir datos para las variantes: número (entero y decimal), cadena, booleano y tipo de fecha. Cualquier otro tipo de datos mostrará un error.

## Añadir variantes {#profiles}

Puede añadir hasta 30 variantes para probar el contenido, ya sea mediante un archivo o manualmente.

>[!NOTE]
>
>Las variantes agregadas solo sirven como propósitos de prueba para el contenido actual. Los no se almacenan en Adobe Experience Platform, sino en la sesión del explorador del usuario, lo que significa que no se mostrarán al cerrar sesión o al trabajar desde otro dispositivo.

### Añadir variante mediante un archivo {#file}

Para añadir una variante desde un archivo, siga estos pasos:

1. Haga clic en el vínculo **[!UICONTROL descargar ejemplo]** para recuperar una plantilla de archivo y, a continuación, elija el formato de archivo que desee utilizar (CSV, JSON o JSONLINES).

1. Haz clic en **[!UICONTROL Descargar]** y luego almacena la plantilla en la ubicación deseada.

1. Abra el archivo y rellene la plantilla para adaptarla a sus necesidades. La plantilla incluye una columna para cada atributo de perfil utilizado en el contenido para la personalización.

1. Cuando el archivo esté listo, haga clic en **[!UICONTROL Cargar datos de entrada]** para cargarlo y probar el contenido.

1. Una vez cargado el archivo, se agrega una casilla en el panel izquierdo para cada línea del archivo. Cada cuadro contiene todos los atributos de perfil utilizados en el contenido para la personalización. Ahora puede usar las variantes para usarlas para obtener una vista previa del contenido en el panel derecho y enviar pruebas.

   ![](assets/simulate-custom-variants.png)

### Añadir variantes manualmente {#manual}

Para añadir una variante manualmente, siga estos pasos:

1. Haga clic en el botón **[!UICONTROL Crear entrada de ejemplo]**.

   Se agrega un cuadro en el panel izquierdo con todos los atributos de perfil utilizados en el contenido para la personalización.

1. Rellene los datos de entrada de ejemplo de la variante y haga clic en **[!UICONTROL Guardar]**.

   ![](assets/simulate-custom-add.png)

1. Una vez añadidas las variantes, puede utilizarlas para obtener una vista previa del contenido en el panel derecho y enviar pruebas.

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
