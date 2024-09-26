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
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 20%

---

# Introducción a la configuración de canales guiada {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Nombre de configuración móvil y web"
>abstract="Introduzca el nombre de la configuración móvil o web. Este nombre se utilizará para cada recurso creado automáticamente con la configuración del canal guiado."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Validar con Assurance"
>abstract="Adobe Experience Platform Assurance está integrado en este flujo de trabajo para ayudarle a inspeccionar la implementación del SDK, así como para simular y validar eventos de aplicación."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-platform/assurance/home" text="Información general sobre Adobe Experience Platform Assurance"

Este ajuste facilita la configuración rápida de los canales de marketing, lo que garantiza que todos los recursos necesarios estén disponibles en Experience Platform, Journey Optimizer y la recopilación de datos. Esto permite a su equipo de marketing empezar con la creación de campañas y recorridos.

La configuración de canal guiado es compatible con las siguientes plataformas y canales.

* Plataformas y SDK:

   * Swift de Apple, iOS

   * Kotlin, Android

   * Javascript, Web

* Canales:

   * Mobile In-App

   * Mensaje push móvil

   * Web Basic


Tenga en cuenta que para cada plataforma que desee configurar, es necesario crear una configuración independiente. Esto se debe a que cada aplicación requiere una configuración de canal única y esto proporciona la flexibilidad para determinar qué canales desea para cada plataforma.

## Requisitos previos {#prereq}

* Para implementar esto de forma eficaz, es esencial que un miembro de la organización con la autoridad y la capacidad técnica para modificar el sitio web o el código móvil supervise la configuración.

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

* Si está utilizando la opción de configuración Existente, asegúrese de que está utilizando las siguientes versiones de la extensión del SDK móvil de Adobe Experience Platform. Para obtener más información sobre la configuración del SDK, incluidas las dependencias y el código de inicialización necesarios, consulte la [siguiente documentación](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks?lang=en).

  Para Android

   * Mobile Core v3.1.0 o posterior
   * Adobe Journey Optimizer v3.1.0 o posterior

  Para iOS

   * Mobile Core v5.2.0 o posterior
   * Adobe Journey Optimizer v5.1.1 o posterior

## Recursos creados automáticamente {#auto-create-resources}

La configuración guiada de canales simplifica la configuración rápida de los canales de marketing, lo que facilita la disponibilidad de todos los recursos esenciales en las aplicaciones de Experience Platform, Journey Optimizer y recopilación de datos. Esto permite a su equipo de marketing empezar a crear campañas y recorridos rápidamente. A continuación se muestra una lista de los recursos que se generan y configuran automáticamente como parte de la Configuración guiada de canales.

Examine las pestañas siguientes para acceder a las listas completas de todos los recursos que se generan automáticamente:

>[!BEGINTABS]

>[!TAB iOS]

Para la **configuración inicial**, a continuación se muestra una lista completa de todos los recursos creados en la pantalla **Detalles de configuración** al hacer clic en **Crear recursos automáticamente**.

<table>
  <thead>
  <tr>
  <th><strong>Solución</strong></th>
  <th><strong>Recursos creados automáticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Etiquetas</p>
  </td>
  <td>
  <ul>
  <li>Propiedad de etiqueta móvil</li>
  <li>Reglas</li>
  <li>Elementos de datos</li>
  <li>Biblioteca</li>
  <li>Entornos (ensayo, producción, desarrollo)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Extensiones de etiquetas</p>
  </td>
  <td>
  <ul>
  <li>Edge Network de Adobe Experience Platform</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consentimiento (con las directivas de consentimiento predeterminadas habilitadas)</li>
  <li>Identidad (con ECID predeterminado, con reglas de vinculación predeterminadas)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Sesión de Assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Secuencias de datos</p>
  </td>
  <td>
  <p>Flujo de datos con servicios</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Conjunto de datos</li>
  <li>Esquema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Para la **configuración del canal**, a continuación se muestra una lista completa de todos los recursos creados en la pantalla **Agregar canales**.

<table>
  <thead>
  <tr>
  <th><strong>Solución</strong></th>
  <th><strong>Recursos creados automáticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Configuración de canal</li>
  <li>Cargar credencial push (solo mensaje push móvil)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

Para la **configuración inicial**, a continuación se muestra una lista completa de todos los recursos creados en la pantalla **Detalles de configuración** al hacer clic en **Crear recursos automáticamente**.

<table>
  <thead>
  <tr>
  <th><strong>Solución</strong></th>
  <th><strong>Recursos creados automáticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Etiquetas</p>
  </td>
  <td>
  <ul>
  <li>Propiedad de etiqueta móvil</li>
  <li>Reglas</li>
  <li>Elementos de datos</li>
  <li>Biblioteca</li>
  <li>Entornos (ensayo, producción, desarrollo)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Extensiones de etiquetas</p>
  </td>
  <td>
  <ul>
  <li>Edge Network de Adobe Experience Platform</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consentimiento (con las directivas de consentimiento predeterminadas habilitadas)</li>
  <li>Identidad (con ECID predeterminado, con reglas de vinculación predeterminadas)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Sesión de Assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Secuencias de datos</p>
  </td>
  <td>
  <p>Flujo de datos con servicios</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Conjunto de datos</li>
  <li>Esquema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Para la **configuración del canal**, a continuación se muestra una lista completa de todos los recursos creados en la pantalla **Agregar canales**.

<table>
  <thead>
  <tr>
  <th><strong>Solución</strong></th>
  <th><strong>Recursos creados automáticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Configuración de canal</li>
  <li>Cargar credencial push (solo mensaje push móvil)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Web]

Para la **configuración inicial**, a continuación se muestra una lista completa de todos los recursos creados en la pantalla **Detalles de configuración** al hacer clic en **Crear recursos automáticamente**.

<table>
  <thead>
  <tr>
  <th><strong>Solución</strong></th>
  <th><strong>Recursos creados automáticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Etiquetas</p>
  </td>
  <td>
  <ul>
  <li>Propiedad de etiqueta móvil</li>
  <li>Reglas</li>
  <li>Elementos de datos</li>
  <li>Biblioteca</li>
  <li>Entornos (ensayo, producción, desarrollo)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Extensiones de etiquetas</p>
  </td>
  <td>
  <ul>
  <li>Edge Network de Adobe Experience Platform</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consentimiento (con las directivas de consentimiento predeterminadas habilitadas)</li>
  <li>Identidad (con ECID predeterminado, con reglas de vinculación predeterminadas)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Sesión de Assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Secuencias de datos</p>
  </td>
  <td>
  <p>Flujo de datos con servicios</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Conjunto de datos</li>
  <li>Esquema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]

