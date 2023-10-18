---
solution: Journey Optimizer
product: journey optimizer
title: Usar fragmentos visuales
description: Aprenda a utilizar fragmentos visuales al crear correos electrónicos en campañas y recorridos de Journey Optimizer
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---

# Añadir fragmentos visuales a los correos electrónicos {#use-visual-fragments}

Puede utilizar un fragmento visual en una [email](get-started-email-design.md) dentro de un recorrido o una campaña, o en una [plantilla de contenido](../content-management/content-templates.md).

>[!NOTE]
>
>Obtenga información sobre cómo crear y administrar fragmentos en [esta sección](../content-management/fragments.md).

➡️ [Aprenda a administrar, crear y utilizar fragmentos en este vídeo](../content-management/fragments.md#video-fragments)

## Usar un fragmento {#use-fragment}

1. Abra cualquier contenido de correo electrónico o plantilla con la variable [Diseñador de correo electrónico](get-started-email-design.md).

1. Seleccione el **[!UICONTROL Fragmentos]** del carril izquierdo.

   ![](assets/fragments-in-designer.png)

1. Se muestra la lista de todos los fragmentos visuales creados en la zona protegida actual. Puede hacer lo siguiente:

   * Busque un fragmento específico escribiendo su etiqueta.
   * Ordene los fragmentos en orden ascendente o descendente.
   * Cambie la forma en que se muestran los fragmentos (tarjetas o vista de lista).

   >[!NOTE]
   >
   >Los fragmentos se ordenan por fecha de creación: los fragmentos visuales añadidos recientemente se muestran primero en la lista.

1. Puede buscar y actualizar la lista.

   >[!NOTE]
   >
   >Si se han modificado o agregado fragmentos mientras edita el contenido, la lista se actualizará con los cambios más recientes.

1. Arrastre y suelte cualquier fragmento de la lista en el área en la que desee insertarlo.

   ![](assets/fragment-insert.png)

1. Al igual que cualquier otro componente, puede mover el fragmento por el contenido.

1. Seleccione el fragmento para mostrar el panel correspondiente a la derecha. Desde allí, puede eliminar el fragmento del contenido o duplicarlo. También puede realizar estas acciones directamente desde el menú contextual que se muestra sobre el fragmento.

   ![](assets/fragment-right-pane.png)

1. Desde el **[!UICONTROL Configuración]** pestaña, puede:

   * Elija los dispositivos en los que desea que se muestre el fragmento.
   * Abra el fragmento en una nueva pestaña para editarlo si es necesario. [Más información](../content-management/fragments.md#edit-fragments)
   * Explore las referencias. [Más información](../content-management/fragments.md#explore-references)

1. Puede personalizar aún más el fragmento mediante el **[!UICONTROL Estilos]** pestaña.

1. Si es necesario, puede romper la herencia con el fragmento original. [Más información](#break-inheritance)

1. Añada tantos fragmentos como desee y **[!UICONTROL Guardar]** sus cambios.

## Romper herencia {#break-inheritance}

Al editar un fragmento visual, los cambios se sincronizan. Se propagan automáticamente a todos los **[!UICONTROL Borrador]** recorridos/campañas y plantillas de contenido que contienen ese fragmento.

>[!NOTE]
>
>Los cambios no se propagan a los correos electrónicos utilizados en **[!UICONTROL Activo]** recorridos o campañas.

Cuando se añaden a un correo electrónico o a una plantilla de contenido, los fragmentos se sincronizan de forma predeterminada.

Sin embargo, puede romper la herencia del fragmento original. En ese caso, el contenido del fragmento se copia en el diseño actual y los cambios ya no se sincronizan.

Para interrumpir la herencia, siga los pasos a continuación:

1. Seleccione el fragmento.

1. Haga clic en el icono de desbloqueo de la barra de herramientas contextual.

   ![](assets/fragment-break-inheritance.png)

1. Ese fragmento se convierte en un elemento independiente que ya no está vinculado al fragmento original. Edítela como cualquier otro componente de contenido en el contenido. [Más información](content-components.md)
