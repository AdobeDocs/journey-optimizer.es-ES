---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de dispositivos móviles y web
description: Obtenga información sobre cómo configurar y monitorizar canales móviles y web
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canal, superficie, técnico, parámetros, optimizador
hide: true
hidefromtoc: true
source-git-commit: 4a089308cfc2fa90cc4c0a6baa15a89598e8edd6
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 25%

---

# Introducción a la configuración de canales guiados {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Nombre de configuración móvil y web"
>abstract="Introduzca el nombre de la configuración móvil o web. Este nombre se utilizará para cada recurso creado automáticamente con la configuración del canal guiado."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Validar con Assurance"
>abstract="Adobe Experience Platform Assurance está integrado en este flujo de trabajo para ayudarle a inspeccionar la implementación del SDK, así como para simular y validar eventos de aplicación."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home" text="Información general sobre Adobe Experience Platform Assurance"


Este ajuste facilita la configuración rápida de los canales de marketing, lo que garantiza que todos los recursos necesarios estén disponibles en Experience Platform, Journey Optimizer y la recopilación de datos. Esto permite a su equipo de marketing iniciar inmediatamente la creación de campañas y recorridos.

Para implementar esto de forma eficaz, es esencial que un miembro de la organización con la autoridad y la capacidad técnica para modificar el sitio web o el código móvil supervise la configuración.

A continuación se indican los permisos necesarios para ejecutar la configuración del canal guiado.

+++ Permisos necesarios

<table>
  <thead>
    <tr>
      <th><strong>Solución</strong></th>
      <th><strong>Permisos</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>Recopilación de datos</p>
      </td>
      <td>
        <ul>
          <li>Derechos de compañía &gt; Propiedades</li>
          <li>Derechos de propiedad: desarrollar, publicar, administrar extensiones y entornos</li>
          <li>Superficies de la aplicación: Administrar configuración de aplicación</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <p>Adobe Experience Platform</p>
      </td>
      <td>
        <ul>
          <li>Recopilación de datos: Administrar flujos de datos</li>
          <li>Zona protegida: conceder acceso a las zonas protegidas</li>
          <li>Administrar segmentos: leer, crear, editar y eliminar definiciones de segmentos</li>
          <li>Administrar perfiles: leer, crear, editar y eliminar perfiles</li>
          <li>Leer conjuntos de datos: acceso de solo lectura a conjuntos de datos</li>
          <li>Esquemas de lectura: acceso de solo lectura a esquemas</li>
          <li>Área de nombres de identidad de lectura: acceso de solo lectura al área de nombres de identidad</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <p>Adobe Journey Optimizer</p>
      </td>
      <td>
        <p>Campañas: Administrar y publicar campañas</p>
      </td>
    </tr>
  </tbody>
</table>
+++

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="set-mobile-android.md">
<img alt="Posible cliente" src="assets/do-not-localize/config-android.jpeg">
</a>
<div><a href="set-mobile-android.md"><strong>Configurar la configuración de Android Mobile</strong>
</div>
<p>
</td>
<td>
<a href="set-mobile-ios.md">
<img alt="Poco frecuente" src="assets/do-not-localize/config-ios.jpeg">
</a>
<div>
<a href="set-mobile-ios.md"><strong>Configurar la configuración de iOS Mobile</strong></a>
</div>
<p></td>
<td>
<a href="set-mobile-web.md">
<img alt="Validación" src="assets/do-not-localize/config-web.jpeg">
</a>
<div>
<a href="set-mobile-web.md"><strong>Configurar la configuración web</strong></a>
</div>
<p>
</td>
</tr></table>
