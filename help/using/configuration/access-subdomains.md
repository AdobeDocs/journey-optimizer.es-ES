---
title: Acceder a subdominios delegados
description: Obtenga información sobre cómo acceder a los subdominios delegados.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# Acceder a subdominios delegados {#access-delegated-subdomains}

Todos los subdominios delegados se muestran en la sección **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** para abrir el Navegador. Los filtros están disponibles para ayudarle a refinar la lista (fecha de delegación, usuario o estado).

![](assets/subdomain-list.png)

La variable **[!UICONTROL Status]** proporciona información sobre el proceso de delegación de subdominios:

* **[!UICONTROL Draft]**: La delegación de subdominios se ha guardado como borrador. Haga clic en el nombre del subdominio para reanudar el proceso de delegación.
* **[!UICONTROL Processing]**: El subdominio está pasando por varias comprobaciones de configuración antes de poder utilizarlo,
* **[!UICONTROL Success]**: El subdominio ha pasado por las comprobaciones correctamente y puede utilizarse para enviar mensajes,
* **[!UICONTROL Failed]**: Una o varias comprobaciones han fallado después de enviar la delegación de subdominios.

Para acceder a información detallada sobre un subdominio, ábralo desde la lista. Puede:

* Recupere el nombre de subdominio (solo lectura) configurado durante el proceso de delegación, así como las direcciones URL generadas (recursos, páginas espejo, URL de seguimiento).

* Agregue un registro TXT de verificación de sitio de Google al subdominio para asegurarse de que esté verificado (consulte [Añadir un registro TXT de Google a un subdominio](google-txt.md)).

![](assets/subdomain-delegated.png)
