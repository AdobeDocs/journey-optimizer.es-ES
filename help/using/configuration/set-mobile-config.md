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
source-git-commit: 8fb87d2e2085d98dd8b014df6aa4d734bab4e997
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 8%

---

# Introducción a la configuración de canales guiados {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Nombre de configuración móvil y web"
>abstract="Introduzca el nombre de la configuración móvil o web. Este nombre se utilizará para cada recurso creado automáticamente con la configuración del canal guiado."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Validar con Assurance"
>abstract="Garantice la calidad de la recopilación de datos de su aplicación móvil y la experiencia del usuario con Assurance. Esta herramienta ofrece un análisis, validación y optimización completos. Además, puede conectar directamente la aplicación para verificar que la integración del SDK sea precisa."
>additional-url="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance" text="Consulte la documentación de Assurance"


Esta configuración facilita la configuración rápida de los canales de marketing, lo que garantiza que todos los recursos necesarios estén fácilmente disponibles en Experience Platform, Journey Optimizer y la recopilación de datos. Esto permite a su equipo de marketing iniciar inmediatamente la creación de campañas y recorridos.

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
