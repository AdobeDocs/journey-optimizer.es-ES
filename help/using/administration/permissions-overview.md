---
solution: Journey Optimizer
product: journey optimizer
title: Resumen de administración de usuarios
description: Obtenga información sobre cómo definir y administrar permisos
feature: Access Management
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: permisos, derechos, restricciones, acceso, zona protegida
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 8%

---

# Introducción al control de acceso {#permissions-overview}

[!DNL Journey Optimizer] le permite definir y administrar los permisos asignados a distintos usuarios. Los permisos son un conjunto de derechos y restricciones que autorizan o deniegan el acceso a las funciones y capacidades del producto.

El control de acceso de [!DNL Journey Optimizer] se proporciona mediante **Permisos** en Adobe Experience Cloud. Esta funcionalidad aprovecha las funciones y directivas que vinculan a los usuarios con permisos y zonas protegidas.

Para configurar el control de acceso para Journey Optimizer, debe tener privilegios de administrador de sistemas o productos para su organización. La función mínima que puede conceder o retirar permisos es de administrador de productos. Otros roles de administrador que pueden administrar permisos son administradores del sistema (sin restricciones). Consulte el [artículo del Centro de ayuda de Adobe](https://helpx.adobe.com/es/enterprise/using/admin-roles.html){target="_blank"} sobre funciones administrativas para obtener más información.

<!-- A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.-->


La administración de usuarios en [!DNL Journey Optimizer] se basa en estos conceptos clave:

* **[!UICONTROL Roles]**: Los roles hacen referencia a una colección de usuarios que comparten los mismos permisos y zonas protegidas. Estas funciones le permiten administrar fácilmente el acceso y los permisos para diferentes grupos de usuarios dentro de su organización. Una función viene con un conjunto de derechos unitarios (permisos) que permiten a los usuarios acceder a determinadas funcionalidades u objetos de la interfaz.
Con [!DNL Journey Optimizer], puede elegir entre una serie de **[!UICONTROL roles]** preexistentes, cada uno con diferentes niveles de permisos, para asignarlos a los usuarios. Obtenga más información acerca de las **funciones integradas** disponibles en [esta página](ootb-product-profiles.md).

* **[!UICONTROL Permisos]**: los permisos son derechos unitarios que le permiten definir las autorizaciones asignadas a **[!UICONTROL roles]**. Cada permiso se recopila en recursos como, por ejemplo, Recorrido u Ofertas, que representan las diferentes funcionalidades u objetos de [!DNL Journey Optimizer]. Obtenga más información en la sección [Niveles de permisos](high-low-permissions.md).

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL Zonas protegidas]**: Las zonas protegidas virtuales dividen instancias en entornos virtuales independientes y aislados. Las zonas protegidas se asignan mediante funciones en Permisos. Más información sobre [el uso de zonas protegidas](sandboxes.md).

* **Control de acceso basado en objetos**: Etiquetas para limitar el acceso a un objeto. Este enfoque protege los recursos digitales confidenciales de los usuarios no autorizados y garantiza una mayor protección de los datos personales. Más información sobre [Administración de acceso basado en objetos](object-based-access.md).

* **Control de acceso basado en atributos**: Autorizaciones para administrar el acceso a datos para equipos o grupos de usuarios específicos. El control de acceso basado en atributos permite a los administradores controlar el acceso a objetos específicos o funcionalidades basadas en atributos. Los atributos pueden ser metadatos añadidos a un objeto, como una etiqueta añadida a un campo o segmento de esquema. Un administrador define directivas de acceso que incluyen atributos para administrar permisos de acceso de usuarios. Más información sobre [Administración de acceso basada en atributos](attribute-based-access.md).


## Vamos a profundizar

Ahora que comprende los conceptos de control de acceso en **[!DNL Journey Optimizer]**, es hora de profundizar en estas secciones de documentación para comenzar a configurar permisos.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="permissions.md">
<img alt="Permisos" src="assets/do-not-localize/role.jpg">
</a>
<div>
<a href="permissions.md"><strong>Conceder acceso</strong></a>
</div>
<p>
</td>
<td>
<a href="ootb-permissions.md">
<img alt="Permisos integrados" src="assets/do-not-localize/select.jpg">
</a>
<div>
<a href="ootb-permissions.md"><strong>Permisos integrados</strong></a>
</div>
<p>
</td>
<td>
<a href="sandboxes.md">
<img alt="administrar zonas protegidas" src="assets/do-not-localize/sandboxes.jpg">
</a>
<div>
<a href="sandboxes.md"><strong>Administrar zonas protegidas</strong></a>
</div>
<p></td>
<td>
<a href="attribute-based-access.md">
<img alt="Control de acceso basado en atributos" src="assets/do-not-localize/data-access.jpeg">
</a>
<div>
<a href="attribute-based-access.md"><strong>Control de acceso basado en atributos</strong></a>
</div>
<p>
</td>
</tr></table>