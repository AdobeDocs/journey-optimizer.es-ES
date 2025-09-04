---
solution: Journey Optimizer
product: journey optimizer
title: Copia de un recorrido en otra zona protegida
description: Obtenga información sobre cómo copiar un recorrido en otra zona protegida
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: zona protegida, recorrido, copiar, entorno
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 21%

---

# Copia de un recorrido en otra zona protegida {#copy-to-sandbox}

<!--
>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copy a journey to another sandbox"
>abstract="Journey Optimizer allows you to copy an entire journey from one sandbox to another. For example, you can copy a journey from the Stage sandbox environment to your Production sandbox. In addition to the Journey itself, Journey Optimizer also copies most of the objects the journey depends on."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox details"
>abstract="Select the destination sandbox you want to copy the journey to. Only sandboxes within your organization are available."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Object details"
>abstract="This is the journey you are going to copy."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Dependent objects"
>abstract="This is the list of associated objects used in the journey. This list displays the name, the object type, as well as the internal Journey Optimizer ID."
-->

Journey Optimizer permite copiar un recorrido completo de una zona protegida a otra. Por ejemplo, puede copiar un recorrido del entorno de zona protegida de ensayo en la zona protegida de producción.

Además del propio recorrido, Journey Optimizer también copia la mayoría de los objetos de los que depende el recorrido: audiencias, esquemas, eventos y acciones.

El proceso de copia se lleva a cabo mediante una **exportación e importación de paquetes** entre las zonas protegidas de origen y destino. Encontrará información detallada sobre cómo exportar objetos e importarlos en una zona protegida de destino en esta sección: [Copiar objetos en otra zona protegida](../configuration/copy-objects-to-sandbox.md)
