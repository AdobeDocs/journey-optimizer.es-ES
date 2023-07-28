---
title: Introducción al correo directo
description: Obtenga información sobre cómo crear y enviar un mensaje de correo directo en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: correo directo, mensaje, campaña
source-git-commit: 40cd058475b37b8fa7d5c0286ad230422e027cf8
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# Creación de un mensaje de correo directo {#create-direct}

>[!AVAILABILITY]
>
>Por ahora, el canal de correo postal no está disponible para las organizaciones que han adquirido la oferta complementaria Escudo de Adobe Healthcare.

El correo postal es un canal sin conexión que le permite personalizar y generar los archivos de extracción necesarios para que los proveedores de correo postal envíen correo a sus clientes.

Al crear una campaña de correo postal, Journey Optimizer genera automáticamente un archivo que contiene todos los perfiles de destino y los datos seleccionados, como las direcciones postales y los atributos de perfil. Este archivo se envía al servidor de su elección para que el proveedor de correo postal elegido pueda acceder a él, quien se encargará del proceso de envío real.

Los pasos principales para enviar mensajes de correo postal son los siguientes:

![](assets/dm-creation-process.png)

Los mensajes de correo postal solo se pueden crear en el contexto de campañas programadas. No están disponibles para su uso en campañas activadas por API ni en recorridos.

>[!IMPORTANT]
>
>Antes de enviar un mensaje de correo postal, asegúrese de haber configurado:
>
>1. A [configuración de enrutamiento de archivos](../direct-mail/direct-mail-configuration.md#file-routing-configuration) que especifica el servidor en el que se debe cargar y almacenar el archivo de extracción,
>1. A [superficie de mensaje de correo directo](../direct-mail/direct-mail-configuration.md#direct-mail-surface) que hará referencia a la configuración de enrutamiento de archivos.
