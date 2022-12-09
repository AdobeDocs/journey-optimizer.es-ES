---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de una fuente de datos
description: Obtenga información sobre cómo configurar una fuente de datos
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Configuración de una fuente de datos {#configure-data-source}


>[!NOTE]
>
>La configuración de la fuente de datos siempre la realiza un **usuario técnico**.

Para configurar una fuente de datos, siga los pasos a continuación:

1. En la sección del menú ADMINISTRACIÓN , seleccione **[!UICONTROL Configurations]**. En el  **[!UICONTROL Data Sources]** , haga clic en **[!UICONTROL Manage]**. Se muestra la lista de fuentes de datos. Consulte [esta página](../start/user-interface.md) para obtener más información sobre la interfaz.

   ![](assets/journey18.png)

1. A continuación, puede agregar grupos de campos a la fuente de datos integrada (consulte [esta página](../datasource/adobe-experience-platform-data-source.md)) o crear una nueva fuente de datos externa (consulte [esta página](../datasource/external-data-sources.md)) y grupos de campos asociados (consulte [esta página](../datasource/configure-data-sources.md#define-field-groups)).

   ![](assets/journey23.png)

1. Haga clic en **[!UICONTROL Save]**.

   La fuente de datos ya está configurada y lista para utilizarse en sus recorridos.

## Definir grupos de campos {#define-field-groups}

Los grupos de campos son conjuntos de campos que se pueden recuperar de un origen de datos y utilizar en un recorrido.

Para cada fuente de datos, se pueden definir varios grupos de campos.

Por ejemplo, puede crear un grupo de campos con el número de teléfono, el correo electrónico, el nombre y la dirección del perfil. A continuación, podrá utilizar estos datos en su recorrido para crear condiciones. Por ejemplo, puede decidir enviar una notificación push solo si el cliente ha instalado la aplicación móvil. Si está vacío, puede enviar un correo electrónico.

Aunque se añada automáticamente un nombre predeterminado, le recomendamos que asigne un nombre al grupo de campos. De hecho, el nombre del grupo de campos será visible para otros usuarios en [!DNL Journey Optimizer]. Es recomendable asignar un nombre relevante a los grupos de campos.

Cuando se utiliza un campo de fuente de datos en un recorrido, el sistema recupera todos los campos definidos para ese grupo de campos. Por lo tanto, es recomendable seleccionar solo los campos que necesite para sus recorridos. Esto reducirá la latencia de las solicitudes en los recorridos, lo que aumenta el rendimiento. Tenga en cuenta que puede agregar fácilmente más campos en grupos de campos más adelante.

El número de recorridos que utilizan un grupo de campos se muestra en la variable **[!UICONTROL Used in]** campo . Puede hacer clic en el botón **[!UICONTROL View journeys]** para mostrar la lista de recorridos con este grupo de campos.

>[!NOTE]
>
>Tenga en cuenta que si un grupo de campos no tiene ningún campo, no se muestra en el editor de expresiones.

![](assets/journey3bis.png)

## Ciclo de vida del grupo de campos {#field-group-lifecycle}

Puede añadir o eliminar campos de un grupo de campos que no se utilice en ningún recorrido en borrador o activo.

Puede agregar, pero no puede quitar un campo de un grupo de campos utilizado en uno o varios recorridos en borrador o en directo. Esto evitará que se rompan los recorridos.

Para eliminar un campo de un grupo de campos utilizado en uno o varios recorridos, siga estos pasos. Veamos un ejemplo de un grupo de campos denominado &quot;Grupo de campos A&quot;.

1. En la lista de grupos de campos, coloque el cursor en &quot;Grupo de campos A&quot; y haga clic en el **[!UICONTROL Duplicate]** en la parte derecha. Asigne un nombre al grupo de campos duplicado &quot;Grupo de campos B&quot;, por ejemplo.
1. En &quot;Grupo de campos B&quot;, elimine los campos que ya no desee.
1. En &quot;Grupo de campos A&quot;, compruebe dónde se utiliza este grupo de campos. Esta información se muestra en la sección **[!UICONTROL Used in]** campo .
1. Abra todos los recorridos que utilicen &quot;Grupo de campos A&quot;.
1. Cree nuevas versiones de cada uno de estos recorridos. Edite todas las actividades utilizando &quot;Grupo de campos A&quot; y seleccione &quot;Grupo de campos B&quot;.
1. Detenga las versiones anteriores de los recorridos que utilizan &quot;Grupo de campos A&quot;. A continuación, no debe realizar ningún recorrido con el grupo de campos A.
1. Elimine &quot;Grupo de campos A&quot; porque ya no se utiliza.
