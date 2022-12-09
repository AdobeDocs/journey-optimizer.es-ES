---
solution: Journey Optimizer
product: journey optimizer
title: Interfaz de usuario
description: Más información sobre la interfaz de usuario de Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 681532f8-1149-465e-92c8-2b5366abc3aa
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---

# Interfaz de usuario {#cjm-user-interface}

Conectar a [Adobe Experience Cloud](http://experience.adobe.com) y busque [!DNL Journey Optimizer].

Los conceptos clave al examinar la interfaz de usuario son comunes en Adobe Experience Platform. Consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-ui/ui-guide.html#adobe-experience-platform-ui-guide){target=&quot;_blank&quot;} para obtener más información.

Los componentes y las capacidades disponibles en la interfaz de usuario dependen de su [permissions](../administration/permissions.md) y [paquete de licencias](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}. Para cualquier pregunta, póngase en contacto con el administrador de éxito de los clientes de Adobe.

>[!NOTE]
>
>Esta documentación se actualiza con frecuencia para reflejar los cambios más recientes en la interfaz de usuario del producto. Sin embargo, algunas capturas de pantalla pueden diferir ligeramente de la interfaz de usuario.


## Navegación izquierda {#left-nav}

Busque los vínculos de la izquierda para acceder a [!DNL Journey Optimizer] capacidades.

![](assets/ajo-home.png)

>[!NOTE]
>
>Las capacidades disponibles pueden variar según los permisos y el acuerdo de licencia.

A continuación se encuentra la lista completa de servicios y capacidades disponibles en la navegación izquierda y vínculos a páginas de ayuda asociadas.

**Página principal**

[!DNL Journey Optimizer] la página de inicio contiene vínculos clave y recursos para comenzar. La variable **[!UICONTROL Recents]** proporciona accesos directos a los eventos y recorridos creados recientemente. Esta lista muestra sus fechas de creación y modificación y su estado.

**[!UICONTROL JOURNEY MANAGEMENT]**

* **[!UICONTROL Journeys]** : cree, configure y organice sus recorridos de clientes. [Más información](../building-journeys/journey-gs.md#jo-build)

* **[!UICONTROL Landing pages]** : cree, diseñe, pruebe y publique páginas de aterrizaje. [Más información](../landing-pages/get-started-lp.md)

**[!UICONTROL DECISION MANAGEMENT]**

* **[!UICONTROL Offers]** - Acceda a sus fuentes y conjuntos de datos recientes desde este menú. Utilice esta sección para crear nuevas ofertas. [Más información](../offers/offer-library/creating-personalized-offers.md)

* **[!UICONTROL Components]** : cree ubicaciones, reglas y etiquetas. [Más información](../offers/offer-library/key-steps.md)

**[!UICONTROL CONTENT MANAGEMENT]**

* **[!UICONTROL Assets]** - [!DNL Adobe Experience Manager Assets Essentials] es un repositorio centralizado de recursos que puede utilizar para rellenar los mensajes. [Más información](../email/assets-essentials.md)

**[!UICONTROL DATA MANAGEMENT]**

* **[!UICONTROL Schemas]** - Utilice Adobe Experience Platform para crear y administrar esquemas del Modelo de datos de experiencia (XDM) en un lienzo visual interactivo denominado Editor de esquemas. [Más información](../data/get-started-schemas.md)

* **[!UICONTROL Datasets]** : Todos los datos que se incorporan en Adobe Experience Platform se conservan dentro del lago de datos como conjuntos de datos. Un conjunto de datos es una construcción de almacenamiento y administración para una recopilación de datos, normalmente una tabla, que contiene un esquema (columnas) y campos (filas). [Más información](../data/get-started-datasets.md)

* **[!UICONTROL Queries]** - Utilice el servicio de consulta de Adobe Experience Platform para escribir y ejecutar consultas, ver consultas ejecutadas anteriormente y acceder a consultas guardadas por usuarios de su organización. [Más información](../data/get-started-queries.md)

* **[!UICONTROL Monitoring]** - Utilice este menú para controlar la ingesta de datos en la interfaz de usuario de Adobe Experience Platform. [Más información](https://experienceleague.adobe.com/docs/experience-platform/ingestion/quality/monitor-data-ingestion.html){target=&quot;_blank&quot;}

**[!UICONTROL CONNECTIONS]**

* **[!UICONTROL Sources]** : utilice este menú para introducir datos de una variedad de fuentes, como aplicaciones de Adobe, almacenamiento basado en la nube, bases de datos y mucho más, y estructurar, etiquetar y mejorar los datos entrantes. [Más información](get-started-sources.md)

**[!UICONTROL CUSTOMER]**

* **[!UICONTROL Segments]** : cree y administre definiciones de segmentos de Experience Platform y utilícelas en sus recorridos. [Más información](../segment/about-segments.md)

* **[!UICONTROL Profiles]** - Perfil del cliente en tiempo real crea una vista holística de cada uno de sus clientes individuales, combinando datos de varios canales, incluidos datos en línea, sin conexión, CRM y de terceros. [Más información](../segment/get-started-profiles.md)

* **[!UICONTROL Identities]** : El servicio de ID de Adobe Experience Platform administra la identificación entre dispositivos, entre canales y casi en tiempo real de sus clientes en lo que se conoce como gráfico de identidad dentro de Adobe Experience Platform. [Más información](../segment/get-started-identity.md)

**[!UICONTROL ADMINISTRATION]**

* **[!UICONTROL Journey Administration]** - Utilice este menú para configurar [events](../event/about-events.md), [fuentes de datos](../datasource/about-data-sources.md) y [acciones](../action/action.md) para usar en sus recorridos.

* **[!UICONTROL Sandboxes]** : Adobe Experience Platform proporciona entornos limitados que dividen una sola instancia en entornos virtuales independientes para ayudar a desarrollar y desarrollar aplicaciones de experiencia digital. [Más información](../administration/sandboxes.md)

* **[!UICONTROL Alerts]** : La interfaz de usuario le permite ver un historial de alertas recibidas en función de las métricas que revela Adobe Experience Platform Observability Insights. La interfaz de usuario también le permite ver, habilitar y deshabilitar las reglas de alerta disponibles. [Más información](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html){target=&quot;_blank&quot;}


## Casos de uso dentro del producto {#in-product-uc}

Aprovechar [!DNL Adobe Journey Optimizer] casos de uso de la página principal y proporcione algunas entradas rápidas para crear un recorrido del cliente.

![](assets/use-cases-home.png)

Los casos de uso disponibles son:

* **Creación de perfiles de prueba**, para crear perfiles de prueba con nuestra plantilla CSV y probar mensajes y recorridos personalizados. Obtenga información sobre cómo implementar este caso de uso [en esta página](../segment/creating-test-profiles.md#use-case-1).
* **Enviar un mensaje de cumpleaños a los clientes**, para enviar automáticamente un correo electrónico para desear a sus clientes alrededor de su cumpleaños. (próximamente)
* **Enviar correos electrónicos a nuevos clientes incorporados**, para enviar fácilmente hasta dos correos electrónicos para dar la bienvenida a sus clientes recién registrados. (próximamente)
* **Enviar mensajes push a la lista importada de clientes**, para enviar rápidamente una notificación push a una lista de clientes importados desde un archivo CSV. (próximamente)

Haga clic en **[!UICONTROL View details]** para obtener más información sobre cada caso de uso.

Haga clic en el **[!UICONTROL Begin]** para iniciar el caso de uso.

Puede acceder a los casos de uso ejecutados desde la **[!UICONTROL View use case library]** botón.

## Accesibilidad{#accessibility}

Las funciones de accesibilidad de [!DNL Adobe Journey Optimizer] se heredan de Adobe Experience Platform:

* Accesibilidad del teclado
* Contraste de color
* Validación de campos obligatorios

[Más información](https://experienceleague.adobe.com/docs/experience-platform/accessibility/features.html){target=&quot;_blank&quot;} en la documentación de Adobe Experience Platform.

Puede utilizar estos métodos abreviados del teclado comunes en [!DNL Journey Optimizer]:

| Acción | Acceso directo |
| --- | --- |
| Desplazamiento entre elementos, secciones y grupos de menús de la interfaz de usuario | Tabulación |
| Retroceder entre elementos, secciones y grupos de menús de la interfaz de usuario | Mayús + Tab |
| Desplazarse dentro de las secciones para definir el enfoque en elementos individuales | Flecha |
| Seleccionar o borrar un elemento que esté enfocado | Entrar o barra espaciadora |
| Cancelar una selección, contraer un panel o cerrar un cuadro de diálogo | Esc |

[Más información](https://experienceleague.adobe.com/docs/experience-platform/accessibility/custom.html){target=&quot;_blank&quot;} en la documentación de Adobe Experience Platform.

Puede utilizar estos métodos abreviados en partes específicas de Journey Optimizer:

<table>
  <thead>
    <tr>
      <th>Elemento de interfaz</th>
      <th>Acción</th>
      <th>Acceso directo</th>
    </tr>
  </thead>
  <tr>
    <td>Lista de recorridos, acciones, fuentes de datos o eventos</td>
    <td>Crear un recorrido, una acción, una fuente de datos o un evento</td>
    <td>C</td>
  </tr>
  <tr>
    <td rowspan="3">Lienzo del recorrido en estado de borrador</td>
    <td>Añada una actividad de la paleta izquierda en la primera posición disponible, de arriba a abajo</td>
    <td>Haga doble clic en la actividad</td>
  </tr>
  <tr>
    <td>Seleccionar todas las actividades</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
  <tr>
    <td>Eliminar las actividades seleccionadas</td>
    <td>Eliminar o Retroceso, a continuación, Intro para confirmar la eliminación</td>
  </tr>
  <tr>
  <td rowspan="3">

Panel de configuración de estos elementos:

<ul>
  <li>Actividad en un recorrido</li>
  <li>Evento</li>
  <li>Fuente de datos</li>
  <li>Acción</li>
</ul>

</td>
    <td>Mover al campo siguiente que se va a configurar</td>
    <td>Tabulación</td>
  </tr>
  <tr>
    <td>Guarde los cambios y cierre el panel de configuración</td>
    <td>Entrar</td>
  </tr>
  <tr>
    <td>Descartar cambios y cerrar el panel de configuración</td>
    <td>Esc</td>
  </tr>
  <tr>
    <td rowspan="4">Recorrido en modo de prueba</td>
    <td>Habilitar o deshabilitar el modo de prueba</td>
    <td>T</td>
  </tr>
  <tr>
    <td>Activador de un evento en un recorrido basado en eventos</td>
    <td>E</td>
  </tr>
  <tr>
    <td>

Se activa un evento en un recorrido basado en segmentos para el que la variable **[!UICONTROL Single profile at a time]** está activada

</td>
    <td>P</td>
  </tr>
  <tr>
    <td>Mostrar los registros de prueba</td>
    <td>L</td>
  </tr>
<!-- //Ajouter ce raccourci quand il marchera (actuellement, le raccourci Ctrl/Cmd+F du navigateur a priorité sur celui de AJO).//
  <tr>
    <td>Page with a search bar</td>
    <td>Select the search bar</td>
    <td>Ctrl/Command + F</td>
  </tr>
-->
  <tr>
    <td>Campo de texto</td>
    <td>Seleccionar todo el texto del campo seleccionado</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
  <tr>
    <td rowspan="2">Ventana emergente</td>
    <td>Guarde los cambios o confirme la acción</td>
    <td>Entrar</td>
  </tr>
  <tr>
    <td>Cierre la ventana</td>
    <td>Esc</td>
  </tr>
  <tr>
    <td>Editor de expresiones simples</td>
    <td>Seleccionar y añadir un campo</td>
    <td>Hacer doble clic en un campo</td>
  </tr>
  <tr>
    <td>Navegación por campos XDM</td>
    <td>Seleccionar todos los campos de un nodo</td>
    <td>Seleccione el nodo principal</td>
  </tr>
  <tr>
    <td>Vista previa de carga útil</td>
    <td>Seleccione la carga útil</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
</table>

## Buscar ayuda y asistencia {#find-help}

Acceda a las páginas de ayuda clave de Adobe Journey Optimizer desde la sección inferior de la página principal.

Utilice la variable **Ayuda** para acceder a las páginas de ayuda, ponerse en contacto con el servicio de asistencia técnica y compartir comentarios. Puede buscar artículos de ayuda y vídeos desde el campo de búsqueda .

![](assets/ajo-help.png)

## Navegadores admitidos {#browsers}

Adobe [!DNL Journey Optimizer] está diseñada para funcionar de forma óptima en la última versión de Google Chrome. Es posible que tenga problemas al utilizar determinadas funciones en versiones anteriores u otros navegadores.

## Preferencias de idioma {#language-pref}

Actualmente, la interfaz de usuario está disponible en los siguientes idiomas:

* Inglés
* Francés
* Alemán
* Italiano
* Español
* Portugués (Brasil)
* Japonés
* Coreano

El idioma predeterminado de la interfaz está determinado por el idioma preferido especificado en el perfil de usuario.

Para cambiar el idioma:

* Haga clic en **Preferencias** desde tu avatar, en la parte superior derecha.
   ![](assets/preferences.png)
* A continuación, haga clic en el idioma mostrado debajo de su dirección de correo electrónico
* Seleccione el idioma preferido y haga clic en **Guardar**. Puede seleccionar un segundo idioma en caso de que el componente que esté utilizando no esté localizado en su primer idioma.
   ![](assets/select-language.png)

## Buscar{#unified-search}

Desde la interfaz de Adobe Journey Optimizer, utilice la capacidad de búsqueda de Adobe Experience Cloud unificada en el centro de la barra superior para encontrar recursos, recorridos, conjuntos de datos y mucho más en sus entornos limitados.

Empiece a introducir contenido para mostrar los resultados principales. Los artículos de ayuda sobre las palabras clave introducidas también se muestran en los resultados.

![](assets/unified-search.png)

Press **Entrar** para acceder a todos los resultados y filtrar por objeto empresarial.

![](assets/search-and-filter.png)

## Filtrar listas{#filter-lists}

En la mayoría de las listas, una barra de búsqueda le permite buscar un elemento específico y seleccionar criterios de filtrado.

Se puede acceder a los filtros haciendo clic en el icono de filtro en la parte superior izquierda de la lista. El menú de filtro le permite filtrar los elementos mostrados según diferentes criterios. Puede elegir mostrar solo los elementos de un determinado tipo o estado, los que ha creado o los modificados en los últimos 30 días. Las opciones difieren según el contexto.

En la lista de recorridos, puede filtrar los recorridos según su estado, tipo y versión desde el **[!UICONTROL Status and version filters]**. El tipo puede ser: **[!UICONTROL Unitary event]**, **[!UICONTROL Segment qualification]**, **[!UICONTROL Read segment]**, **[!UICONTROL Business event]** o **[!UICONTROL Burst]**. Puede elegir mostrar solo los recorridos que utilizan un evento, un grupo de campos o una acción específicos del **[!UICONTROL Activity filters]** y **[!UICONTROL Data filters]**. La variable **[!UICONTROL Publication filters]** permite seleccionar una fecha de publicación o un usuario. Puede elegir, por ejemplo, mostrar las últimas versiones de recorridos en directo que se publicaron ayer. [Más información](../building-journeys/using-the-journey-designer.md).

>[!NOTE]
>
>Tenga en cuenta que las columnas mostradas se pueden personalizar mediante el botón de configuración en la parte superior derecha de las listas. La personalización se guarda para cada usuario.

Utilice la variable **[!UICONTROL Last update]** y **[!UICONTROL Last update by]** para comprobar cuándo se ha producido la última actualización de los recorridos y quién lo guardó.

![](assets/filter-journeys.png)

En los paneles Evento, Fuente de datos y Configuración de acción, la variable **[!UICONTROL Used in]** muestra el número de recorridos que utilizan ese evento, grupo de campos o acción en particular. Puede hacer clic en el botón **[!UICONTROL View journeys]** para mostrar la lista de recorridos correspondientes.

![](assets/journey3bis.png)

En las listas, puede realizar acciones básicas en cada elemento. Por ejemplo, puede duplicar o eliminar un elemento.

![](assets/journey4.png)
