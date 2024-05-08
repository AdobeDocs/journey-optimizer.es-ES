---
title: Introducción a Experience Decisioning
description: Más información sobre Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilidad limitada"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 19%

---

# Introducción a Experience Decisioning {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>Ahora mismo, la toma de decisiones sobre experiencias solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.
>
>Por ahora, la función no está disponible para los clientes que han comprado el Adobe **Healthcare Shield** y **Escudo de seguridad y privacidad** ofertas de complementos.

## Qué es Experience Decisioning {#about}

La toma de decisiones sobre experiencias simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como “elementos de decisión” y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar a cada persona los elementos de decisión más relevantes.

Estos elementos de decisión se integran perfectamente en una amplia gama de superficies entrantes a través del nuevo canal de experiencia basado en código, ahora accesible dentro de las campañas de Journey Optimizer. Las políticas de decisión de Experience Decisioning solo están disponibles para su uso en campañas de experiencia basadas en código.

## Pasos clave de Experience Decisioning {#steps}

Los pasos principales para trabajar con Experience Decisioning son los siguientes:

1. **Asignar los permisos adecuados**. Experience Decisioning solo está disponible para usuarios con acceso a un informe relacionado con Experience Decisioning **[!UICONTROL función]** como los gestores de decisiones. Si no puede acceder a Experience Decisioning, se deben ampliar los permisos.

   +++Obtenga información sobre cómo asignar la función Administradores de decisiones

   1. Para asignar una función a un usuario en [!DNL Permissions] producto, vaya a la **[!UICONTROL Funciones]** y seleccione Administradores de decisiones.

      ![](assets/decision_permission_1.png)

   1. Desde el **[!UICONTROL Usuarios]** pestaña, haga clic en **[!UICONTROL Agregar usuario]**.

      ![](assets/decision_permission_2.png)

   1. Escriba el nombre o la dirección de correo electrónico del usuario o seleccione el usuario en la lista y haga clic en **[!UICONTROL Guardar]**.

      Si el usuario no se ha creado anteriormente, consulte la [Documentación de Adición de usuarios](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   El usuario debería recibir entonces un correo electrónico que le redirija a su instancia.

+++

1. **Configuración de atributos personalizados**: adapte el catálogo de artículos a sus necesidades específicas configurando atributos personalizados en el esquema del catálogo.

1. **Crear elementos de decisión** para mostrarlo a su audiencia de destino.

1. **Organizar con colecciones**: utilice las colecciones para categorizar los elementos de decisión según las reglas basadas en atributos. Incorpore colecciones en las estrategias de selección para determinar qué colección de elementos de decisión se debe tener en cuenta.

1. **Creación de reglas de decisión**: Las reglas de decisión se utilizan en elementos de decisión o estrategias de selección para determinar a quién se puede mostrar un elemento de decisión.

1. **Implementación de métodos de clasificación**: Cree métodos de clasificación y aplíquelos dentro de las estrategias de decisión para determinar el orden de prioridad para seleccionar los elementos de decisión.

1. **Crear estrategias de selección**: genere estrategias de selección que aprovechen las colecciones, las reglas de decisión y los métodos de clasificación para identificar los elementos de decisión adecuados para mostrarlos a los perfiles.

1. **Incrustar una política de decisión en la campaña basada en código**: las políticas de decisión combinan varias estrategias de selección para determinar los elementos de decisión aptos que se mostrarán a la audiencia objetivo.
