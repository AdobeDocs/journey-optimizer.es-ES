---
title: Registros de PTR
description: Aprenda a xxxx
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
source-git-commit: 6988a6ab9412e5d27f1ba9d1145cc11c7c06e7b7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# Registros de PTR

## Acerca de los registros PTR

Un registro de puntero (PTR) es un tipo de registro DNS (Sistema de nombres de dominio) que proporciona el nombre de dominio vinculado a una dirección IP.

Con los registros PTR, los servidores de correo receptores pueden comprobar la autenticidad de los servidores de correo electrónico al identificar si sus direcciones IP corresponden a los nombres con los que se conectan los servidores.

## Acceda a los registros PTR de sus subdominios

Una vez delegado un subdominio en Customer Journey Management, se crea automáticamente un registro PTR y se asocia a este subdominio. Puede acceder a él desde el menú **[!UICONTROL Channels]** / **[!UICONTROL PTR records]** .

![](../assets/ptr-records.png)

La lista muestra los registros PTR generados para cada subdominio delegado, utilizando la siguiente sintaxis:

* &quot;r&quot; para registrar,
* &quot;xx&quot; para las dos últimas cifras de la dirección IP,
* nombre de subdominio.

Puede abrir un registro PTR de la lista para mostrar el nombre de subdominio y la dirección IP asociados.

>[!NOTE]
>
>Tenga en cuenta que los registros PTR son de solo lectura y que no se puede modificar el subdominio asociado a una dirección IP.
