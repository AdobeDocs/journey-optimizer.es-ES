---
title: Introducción a Experience Decisioning
description: Más información sobre Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: f71795c99157ce43f5250aaf10eb0b97f235b454
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 23%

---

# Introducción a Experience Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX &quot;Lo que encontrará en esta guía de documentación&quot;]

* **[Introducción a Experience Decisioning](gs-experience-decisioning.md)**
* Administrar los elementos de decisión: [Configurar el catálogo de artículos](catalogs.md) - [Crear elementos de decisión](items.md) - [Administrar colecciones de elementos](collections.md)
* Configurar la selección de elementos: [Creación de reglas de decisión](rules.md) - [Crear métodos de clasificación](ranking.md)
* [Creación de estrategias de selección](selection-strategies.md)
* [Creación de políticas de decisión](create-decision.md)

>[!ENDSHADEBOX]

## Qué es Experience Decisioning {#about}

>[!AVAILABILITY]
>
>Actualmente, la función Experience Decisioning está disponible como una versión beta solo para usuarios seleccionados. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.
>
>Las políticas de decisión solo están disponibles para su uso en campañas de experiencia basadas en código.

La toma de decisiones sobre experiencias simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como “elementos de decisión” y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar a cada persona los elementos de decisión más relevantes.

Estos elementos de decisión se integran perfectamente en una amplia gama de superficies entrantes a través del nuevo canal de experiencia basado en código, ahora accesible dentro de las campañas de Journey Optimizer.

## Pasos clave de Experience Decisioning {#steps}

Los pasos principales para trabajar con Experience Decisioning son los siguientes:

1. **Asignar los permisos adecuados**. Las decisiones solo están disponibles para los usuarios con acceso a un informe relacionado con Experience Decisioning **[!UICONTROL función]** como los gestores de decisiones. Si no puede acceder a las decisiones, se deben ampliar los permisos.

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

1. **Configuración de atributos personalizados**: adapte el catálogo de elementos de decisión a sus necesidades específicas configurando atributos personalizados en el esquema del catálogo.

1. **Crear elementos de decisión** para mostrarlo a su audiencia de destino.

1. **Organizar con colecciones**: utilice las colecciones para categorizar los elementos de decisión según las reglas basadas en atributos. Incorpore colecciones en las estrategias de selección para determinar qué colección de elementos de decisión se debe tener en cuenta.

1. **Creación de reglas de decisión**: Las reglas de decisión se utilizan en elementos de decisión o estrategias de selección para determinar a quién se puede mostrar un elemento de decisión.

1. **Implementación de métodos de clasificación**: Cree métodos de clasificación y aplíquelos dentro de las estrategias de decisión para determinar el orden de prioridad para seleccionar los elementos de decisión.

1. **Crear estrategias de selección**: genere estrategias de selección que aprovechen las colecciones, las reglas de decisión y los métodos de clasificación para identificar los elementos de decisión adecuados para mostrarlos a los perfiles.

1. **Incrustar una política de decisión en la campaña basada en código**: las políticas de decisión combinan varias estrategias de selección para determinar los elementos de decisión aptos que se mostrarán a la audiencia objetivo.
