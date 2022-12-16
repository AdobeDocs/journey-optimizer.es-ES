---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 100%

---

# Notas de la versión {#release-notes}

En esta página se enumeran todas las nuevas funciones y mejoras de [!DNL Journey Optimizer]. También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.


## Versión de octubre de 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Mejoras {#oct-2022-improvements}

**Recorridos**

* La opción **Forzar reentrada en repetición** se ha añadido en los parámetros de programación de segmentos de lectura recurrentes. Esta opción le permite hacer que todos los perfiles que aún están presentes en el recorrido se cierren automáticamente en la siguiente ejecución. Cuando la opción está desactivada, los perfiles deben finalizar el recorrido antes de poder volver a entrar en otra ocurrencia. [Más información](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Administración**

* Se ha agregado un mensaje a la interfaz de usuario para advertir que las configuraciones de subdominio, subdominio de página de aterrizaje, registro PTR y grupo de IP son comunes a todas las zonas protegidas, por lo que cualquier modificación en una de estas configuraciones también afectará a las zonas protegidas de producción.
* Se han modificado los pasos para cargar la lista de supresión como archivo CSV desde la interfaz de usuario. [Más información](../configuration/manage-suppression-list.md#download-suppression-list)

**Campañas**

* Ahora puede archivar las campañas completadas y detenidas. [Más información](../campaigns/modify-stop-campaign.md#archive)
