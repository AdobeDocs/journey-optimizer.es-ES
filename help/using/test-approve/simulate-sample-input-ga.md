---
solution: Journey Optimizer
product: journey optimizer
title: Simulación de variaciones de contenido
description: Obtenga información sobre cómo previsualizar variaciones de contenido, generar variantes automáticamente con IA, administrar perfiles de prueba y enviar pruebas desde la experiencia Simular variaciones de contenido.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
hide: true
exl-id: 2744974b-62cc-4d25-acc3-edd4c53a9a58
TQID: https://experienceleague.adobe.com/Y8qsGW8XqSVqag4yqRinnem9w2PYJyKIDIWvuGqAchU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: bf7a266e-e483-42c6-b5bc-09ca6e49900c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 2ec7de841e3d871ad4cfc545d80c5271c4137d2c
workflow-type: tm+mt
source-wordcount: 1313
ht-degree: 2%

---

# Simulación de variaciones de contenido {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simular mediante entrada de muestra"
>abstract="En esta pantalla, puede probar las variantes de contenido generándolas automáticamente con IA, añadiendo valores a través de una plantilla CSV o JSON, introduciéndolos manualmente o utilizando perfiles de prueba."

Cuando el contenido incluye lógica condicional o de personalización, debe comprobar que se representa correctamente para cada tipo de destinatario antes de enviarlo.

La experiencia **[!UICONTROL Simular variaciones de contenido]** en [!DNL Journey Optimizer] resuelve esto al permitirle probar varias variantes de contenido desde una sola pantalla, generadas automáticamente con IA, introducidas manualmente, importadas desde un archivo o basadas en usuarios simulados reutilizables. Puede previsualizar cómo se procesa y envía cada variante de pruebas, todo sin crear previamente perfiles persistentes en Adobe Experience Platform.

Desde el contenido, selecciona **[!UICONTROL Simular contenido]** y luego **[!UICONTROL Simular variaciones de contenido]** para abrir una sola experiencia donde puedas:

* **Variantes generadas automáticamente** que usan IA para cubrir ramas condicionales y de personalización
* **Agregar variantes manualmente** o desde un archivo CSV o JSON
* **Use usuarios simulados** para previsualizar y probar con datos de prueba guardados y reutilizables
* **Vista previa** al procesar y **enviar pruebas por correo electrónico** para las variantes seleccionadas

Todos los atributos utilizados en el contenido para la personalización se detectan automáticamente. Una variante es una versión del contenido con valores diferentes para sus atributos.

>[!NOTE]
>
>Las variantes solo sirven como propósitos de prueba para el contenido actual. No se almacenan en Adobe Experience Platform, sino en la sesión del explorador del usuario, lo que significa que no se muestran al cerrar la sesión o al trabajar desde otro dispositivo.

## Protecciones y limitaciones {#limitations}

Antes de empezar a probar el contenido con datos de entrada de ejemplo, tenga en cuenta las siguientes protecciones y requisitos previos.

* **Canales**: la simulación de variaciones de contenido está disponible para:

   * los canales de correo electrónico, SMS y notificaciones push;
   * todos los canales entrantes (web, experiencia basada en código, aplicación, tarjetas de contenido).

* **Funciones compatibles**: las variaciones de contenido se pueden usar con [!DNL Journey Optimizer] funciones de contenido multilingüe y experimento de contenido. Esto le permite probar mensajes en varios idiomas y optimizar el contenido mediante la experimentación.

  También puede aprovechar las variaciones de contenido para probar las plantillas de contenido.

  >[!NOTE]
  >
  >Por ahora, los informes de procesamiento de bandeja de entrada y correo no deseado no están disponibles en la experiencia actual. Para usar estas características, selecciona el botón **[!UICONTROL Simular contenido]** de tu contenido para acceder a la interfaz de usuario anterior.

* **Atributos**: se admiten atributos contextuales y de perfil.

* **Tipos de datos**: solo se admiten los siguientes tipos de datos al escribir datos para las variantes: número (entero y decimal), cadena, booleano y tipo de fecha. Cualquier otro tipo de datos mostrará un error.

* **Número de variantes**: puede agregar hasta 30 variantes para probar el contenido, ya sea mediante un archivo, manualmente o mediante generación automática.

## Crear variantes de contenido

Para crear variaciones para el contenido, haga clic en el botón **[!UICONTROL Simular contenido]** y elija **[!UICONTROL Simular variaciones de contenido]**.

![Opción Simular variaciones de contenido](assets/simulate-sample.png)

Puede crear variantes de las siguientes maneras:

* [Agregar variantes manualmente o desde un archivo](#profiles).
* [Variantes generadas automáticamente](#auto-generate-variants) con IA.
* [Seleccionar variantes de usuarios simulados existentes](#simulated-users).

Una vez creadas las variantes, puede [obtener una vista previa del contenido y enviar pruebas](#preview-proofs).

### Añadir variantes manualmente o desde un archivo {#profiles}

Al acceder a la experiencia de variaciones de contenido, todos los campos personalizados utilizados en el contenido se detectan automáticamente y se muestran en una variante en blanco.

Por ejemplo, si el correo electrónico contiene dos campos de personalización, &quot;Nombre&quot; y &quot;Ciudad&quot;, aparecen en la lista. Inicialmente, no se introduce ningún valor y no se muestra ningún contenido personalizado en el panel de vista previa.

![Lista de variantes de entrada de muestra](assets/simulate-custom-variants-list.png)

Puede añadir variantes manualmente o cargarlas desde un archivo.

+++ Añadir variantes manualmente

Para editar el valor de la variante predeterminada, haga clic en el botón **[!UICONTROL Editar]** para proporcionar valores personalizados para cada campo de personalización. El panel de vista previa se actualizará para mostrar cómo se procesa el contenido con los valores introducidos.

Para agregar una variante nueva, haga clic en el botón **[!UICONTROL Crear muestra]**. Aparece una nueva variante en blanco que contiene todos los campos personalizados detectados. Puede editar la nueva variante según sea necesario.

![Botón Crear entrada de ejemplo](assets/simulate-custom-add.png)

+++

+++ Adición de variantes de un archivo

Puede cargar un archivo con variantes y valores predefinidos para acelerar el proceso.

1. Haga clic en el botón **[!UICONTROL Cargar datos]** para abrir la pantalla de carga de archivos.
1. Seleccione **[!UICONTROL Descargar muestra]** para descargar una plantilla de archivo CSV, JSON o JSONLINES.
1. Abra el archivo de plantilla y rellene los valores deseados para cada atributo de perfil. La plantilla incluye una columna para cada atributo de perfil utilizado en el contenido para la personalización.

   Ejemplo de sintaxis JSON:

   ```json
   {
   "profile": {
       "attributes": {
       "person": {
           "name": {
               "lastName": "Doe",
               "firstName": "John"
               }
           }
       }
   }
   }
   ```

1. Una vez que el archivo esté listo, selecciona **[!UICONTROL Confirmar]** para cargarlo. Después de la carga, se agrega una nueva variante a la lista para cada entrada del archivo.

+++

### Generar variantes de contenido automáticamente {#auto-generate-variants}

[!DNL Journey Optimizer] puede usar la simulación basada en IA para generar automáticamente una variante de contenido y así validar la lógica de personalización sin necesidad de crear variantes a mano.

Al procesar contenido para simulación o prueba, el sistema analiza el contenido, identifica los campos de personalización y los reemplaza por valores significativos para una previsualización casi realista.

Para generar automáticamente una variante, haga clic en el botón **[!UICONTROL Generar]** y espere a que el sistema genere la variante.

![Botón Generar variantes](assets/simulate-generate-variant.png)

>[!NOTE]
>
>La generación produce una única variante. Al hacer clic en **[!UICONTROL Generar]**, se reemplazarán todas las variantes de contenido existentes en la lista, incluidas las que haya agregado manualmente o desde un archivo, con una variante generada.

Revise la variante generada en la lista de variantes y su renderización.

### Seleccionar variantes de usuarios simulados {#simulated-users}

En **[!UICONTROL Simular variaciones de contenido]**, puede basar sus variantes en **usuarios simulados**. Los usuarios simulados son entidades temporales similares a un perfil creadas para realizar pruebas sin utilizar perfiles persistentes en Adobe Experience Platform. A diferencia de las variantes agregadas solo para la sesión del explorador actual, los usuarios simulados se guardan y se pueden reutilizar en los recorridos y por otros usuarios.

Los usuarios simulados se crean y administran desde la característica **[!UICONTROL Simulación]** del recorrido. Para ver el procedimiento completo para crearlos, guardarlos y reutilizarlos, consulte [Crear y administrar usuarios simulados](../building-journeys/simulate-journey.md#test-users).

Una vez creados los usuarios simulados, puede utilizarlos para previsualizar el contenido. Para ello, siga estos pasos:

1. Haga clic en el botón **[!UICONTROL Seleccionar variantes]**.
1. En la lista de usuarios simulados existentes, seleccione los que desee usar y luego haga clic en **[!UICONTROL Seleccionar]**.

   ![Seleccionar usuarios simulados para usarlos como variantes de contenido](assets/simulate-custom-simulated.png)

1. Los usuarios simulados seleccionados se añaden a la lista de variantes de contenido, donde puede obtener una vista previa del contenido con sus valores de atributo. También puede editar manualmente los valores de una variante para probarlos, pero estos cambios no se guardan de nuevo en el usuario simulado.

## Previsualización de contenido y envío de pruebas {#preview-proofs}

Una vez añadidas las variantes, puede utilizarlas para obtener una vista previa del contenido en el panel derecho y enviar pruebas por correo electrónico.

### Previsualizar variaciones de contenido {#preview}

Para obtener una vista previa del contenido mediante una variante, seleccione la variante correspondiente de la lista para actualizar el contenido en el panel de vista previa con la información introducida para esta variante.

En el ejemplo siguiente, se han añadido dos variantes para la línea de asunto del correo electrónico:

| Selección de variante 1 | Selección de variante 2 |
|----------|-------------|
| ![Selección de variante 1](assets/simulate-custom-boxes.png) | ![Selección de variante 2](assets/simulate-custom-boxes2.png) |

<!--
For multilingual content and experimentation, a dropdown is available to switch between the different language variants or treatments.

![Language or treatment selector](assets/simulate-custom-experiment.png)
-->

### Envío de pruebas {#proofs}

Journey Optimizer le permite enviar pruebas a las direcciones de correo electrónico mientras suplanta una o varias variantes que haya agregado en la pantalla de simulación. Los pasos son los siguientes:

1. Compruebe que se hayan agregado variantes para probar el contenido y haga clic en el botón **[!UICONTROL Enviar prueba]**.

1. En el campo **[!UICONTROL Destinatarios]**, escriba la dirección de correo electrónico a la que desea enviar la prueba y haga clic en **[!UICONTROL Agregar]**. Repita la operación para enviar la prueba a direcciones de correo electrónico adicionales. Puede añadir hasta 10 destinatarios de prueba.

1. En la sección inferior de la pantalla, seleccione la variante que desee utilizar en la prueba. Puede seleccionar varias variantes, en cuyo caso el correo electrónico incluirá tantas pruebas como variantes seleccionadas.

   Para obtener más información sobre una variante, seleccione el vínculo **[!UICONTROL Ver detalles del perfil]**. Esto le permite mostrar la información introducida en la pantalla anterior para las diferentes variantes.

   ![Destinatarios de prueba y selección de variante](assets/simulate-custom-proofs.png)

1. Haga clic en el botón **[!UICONTROL Enviar prueba]** para comenzar a enviar la prueba.

1. Para realizar un seguimiento del envío de prueba, haga clic en el botón **[!UICONTROL Ver pruebas]** en la pantalla de simular contenido.

![Lista de pruebas enviadas](assets/simulate-custom-sent-proofs.png)
