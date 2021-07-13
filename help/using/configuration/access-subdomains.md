---
title: Delegar subdominios
description: Obtenga información sobre cómo delegar subdominios
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
source-wordcount: '163'
ht-degree: 6%

---


# Acceder a subdominios delegados

Todos los subdominios delegados se muestran en el menú **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**. Los filtros están disponibles para ayudarle a refinar la lista (fecha de delegación, usuario o estado).

![](../assets/subdomain-list.png)

La columna **[!UICONTROL Status]** proporciona información sobre el proceso de delegación de subdominios:

* **[!UICONTROL Draft]**: La delegación de subdominios se ha guardado como borrador. Haga clic en el nombre del subdominio para reanudar el proceso de delegación.
* **[!UICONTROL Processing]**: El subdominio está pasando por varias comprobaciones de configuración antes de poder utilizarlo,
* **[!UICONTROL Success]**: El subdominio ha pasado por las comprobaciones correctamente y puede utilizarse para enviar mensajes,
* **[!UICONTROL Failed]**: Una o varias comprobaciones han fallado después de enviar la delegación de subdominios.

Para acceder a información detallada sobre un subdominio, ábralo desde la lista. Puede:

* Recupere el nombre de subdominio (solo lectura) configurado durante el proceso de delegación, así como las direcciones URL generadas (recursos, páginas espejo, URL de seguimiento).

* Agregue un registro TXT de verificación de sitio de Google al subdominio para asegurarse de que esté verificado (consulte [Agregar un registro TXT de Google a un subdominio](google-txt.md)).

![](../assets/subdomain-delegated.png)
