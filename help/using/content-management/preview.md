---
title: Vista previa del contenido
description: Obtenga información sobre cómo previsualizar el contenido.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 6477270c-0309-411a-8254-c7ffc4419492
source-git-commit: 03cb3298c905766bc059e82c58969a2111379345
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 3%

---

# Vista previa del contenido mediante perfiles de prueba {#preview}

<!--## Preview your content {#preview-content}-->

Una vez definidos los [perfiles de prueba](test-profiles.md), puede obtener una vista previa del contenido.

>[!NOTE]
>
>[!DNL Journey optimizer] también le permite probar diferentes variantes del contenido previsualizándolo y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV / JSON, o añadidos manualmente. [Aprenda a probar el contenido con datos de entrada de ejemplo](../test-approve/simulate-sample-input.md)

Para obtener una vista previa del contenido mediante perfiles de prueba, siga estos pasos:

1. En la pantalla Editar contenido del mensaje o en el Designer de correo electrónico, haga clic en el botón **[!UICONTROL Simular contenido]**.

1. Seleccione un perfil de prueba. Puede comprobar los valores disponibles en las columnas. Utilice las flechas derecha e izquierda para examinar los datos.

   ![](../email/assets/preview-select-profile.png)

   >[!NOTE]
   >
   >Para agregar más perfiles de prueba, seleccione **[!UICONTROL Administrar perfiles de prueba]**. [Más información](test-profiles.md)

1. Haga clic en el icono **[!UICONTROL Seleccionar datos]** situado encima de la lista para agregar o quitar columnas.

   Al final de la lista se pueden ver campos de personalización específicos del mensaje actual. En este ejemplo, el perfil de ciudad, nombre y apellidos. Seleccione esos campos y asegúrese de que estos valores se rellenen en los perfiles de prueba.

   ![](../email/assets/preview-select-data.png)

1. En la vista previa del mensaje, los elementos personalizados se sustituyen por los datos del perfil de prueba seleccionado. Por ejemplo, para este mensaje, tanto el contenido del correo electrónico como el asunto del correo electrónico están personalizados:

   ![](../email/assets/preview-test-profile.png)

1. Seleccione otros perfiles de prueba para previsualizar el correo electrónico para cada variante del mensaje.

>[!NOTE]
>
>Si se encuentra un error en los detalles de configuración, haga clic en el botón **[!UICONTROL Ver detalles de configuración]**. [Más información](../email/surface-personalization.md#check-configuration)

Al crear experiencias basadas en código, puede obtener una vista previa del contenido personalizado directamente en el explorador o en los dispositivos móviles para una simulación en tiempo real. [Más información](../code-based/create-code-based.md#preview-on-device)

