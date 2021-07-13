---
title: Crear grupos de IP
description: '"Aprenda a administrar ip-pools"'
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Configuración de la aplicación
topic: Administración
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 3%

---


# Crear grupos de IP

## Acerca de los grupos de IP

Con Journey Optimizer, puede crear grupos de IP para agrupar las direcciones IP de los subdominios.

La creación de grupos de IP es muy recomendable para la entrega por correo electrónico. Al hacerlo, puede evitar que la reputación de un subdominio afecte a los demás subdominios.

Por ejemplo, una práctica recomendada es tener un grupo de IP para los mensajes de marketing y otro para los mensajes transaccionales. De este modo, si uno de los mensajes de marketing tiene un rendimiento incorrecto y un cliente los declara como correo no deseado, esto no afectará a los mensajes transaccionales enviados a este mismo cliente, que seguirá recibiendo mensajes transaccionales (confirmaciones de compra, mensajes de recuperación de contraseña, etc.).

## Crear un grupo de IP

Para crear un grupo de IP, siga estos pasos:

1. Acceda al menú **[!UICONTROL Channels]** / **[!UICONTROL IP pools]** y haga clic en **[!UICONTROL Create IP Pool]**.

   ![](../assets/ip-pool-create.png)

1. Proporcione un nombre y una descripción (opcional) para el grupo de IP.

   >[!NOTE]
   >
   >El nombre del subdominio debe comenzar con una letra (A-Z) e incluir solo caracteres alfanuméricos o caracteres especiales ( _, ., - ).

1. Seleccione las direcciones IP que desea incluir en el grupo en la lista desplegable y haga clic en **[!UICONTROL Submit]**.

   ![](../assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Todas las direcciones IP aprovisionadas con su instancia están disponibles en la lista.

El grupo de IP ahora se crea y se muestra en la lista. Puede seleccionarlo para acceder a sus propiedades y mostrar el mensaje preestablecido asociado. Para obtener más información sobre cómo asociar un ajuste preestablecido de mensaje con un grupo de IP, consulte [esta sección](message-presets.md)).

![](../assets/ip-pool-created.png)

Para editar un grupo de IP, ábralo y, a continuación, edite sus propiedades como desee.

>[!NOTE]
>
>Si se ha asociado un ajuste preestablecido de mensaje al grupo de direcciones IP, primero debe eliminarlo antes de editar el grupo de direcciones IP. Una vez que haya realizado las modificaciones, puede asociar de nuevo el ajuste preestablecido de mensaje.
