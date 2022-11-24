---
solution: Journey Optimizer
product: journey optimizer
title: Interfaz de usuario
description: Más información acerca de la interfaz de usuario de Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 681532f8-1149-465e-92c8-2b5366abc3aa
source-git-commit: 44e87553b5a001414f28a972ec5c61947decdf55
workflow-type: tm+mt
source-wordcount: '1578'
ht-degree: 97%

---

# Interfaz de usuario {#cjm-user-interface}

Conéctese a [Adobe Experience Cloud](http://experience.adobe.com) y busque [!DNL Journey Optimizer].

Los conceptos clave al examinar la interfaz de usuario son habituales en Adobe Experience Platform. Consulte la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-ui/ui-guide.html?lang=es#adobe-experience-platform-ui-guide){target=&quot;_blank&quot;} para obtener más información.

Los componentes y las funciones disponibles en la IU dependen de los [permisos](../administration/permissions.md) y del [paquete de licencias](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html?lang=es){target=&quot;_blank&quot;}. Para cualquier pregunta, póngase en contacto con el Manager de éxito del cliente de Adobe.

>[!NOTE]
>
>Esta documentación se actualiza con frecuencia para reflejar los cambios recientes en la interfaz de usuario del producto. Sin embargo, algunas capturas de pantalla pueden diferir ligeramente de la interfaz de usuario que ve.


## Navegación izquierda {#left-nav}

Examine los vínculos de la izquierda para acceder a las funciones de [!DNL Journey Optimizer].

![](assets/ajo-home.png)

>[!NOTE]
>
>Las capacidades disponibles pueden variar según los permisos y el acuerdo de licencia.

A continuación, hay la lista completa de servicios y capacidades disponibles en la navegación izquierda y vínculos a las páginas de ayuda asociadas.

**Inicio**

La página principal de [!DNL Journey Optimizer] contiene vínculos clave y recursos para comenzar. La lista **[!UICONTROL Recientes]** proporciona accesos directos a los eventos y recorridos creados recientemente. Esta lista muestra sus fechas de creación y modificación, así como el estado.

**[!UICONTROL ADMINISTRACIÓN DE RECORRIDOS]**

* **[!UICONTROL Recorridos]** : cree, configure y organice sus recorridos de cliente. [Más información](../building-journeys/journey-gs.md#jo-build)

* **[!UICONTROL Páginas de aterrizaje]** : cree, diseñe, pruebe y publique páginas de aterrizaje. [Más información](../landing-pages/get-started-lp.md)

**[!UICONTROL GESTIÓN DE DECISIONES]**

* **[!UICONTROL Ofertas]**: acceda a sus fuentes y conjuntos de datos recientes desde este menú. Utilice esta sección para crear nuevas ofertas. [Más información](../offers/offer-library/creating-personalized-offers.md)

* **[!UICONTROL Componentes]**: cree ubicaciones, reglas y etiquetas. [Más información](../offers/offer-library/key-steps.md)

**[!UICONTROL ADMINISTRACIÓN DE CONTENIDO]**

* **[!UICONTROL Recursos]** : [!DNL Adobe Experience Manager Assets Essentials] es un repositorio centralizado de recursos que puede utilizar para rellenar los mensajes. [Más información](../design/assets-essentials.md)

**[!UICONTROL ADMINISTRACIÓN DE DATOS]**

* **[!UICONTROL Esquemas]**: utilice Adobe Experience Platform para crear y administrar esquemas del Modelo de datos de experiencia (XDM) en un lienzo visual interactivo denominado Editor de esquemas. [Más información](../data/get-started-schemas.md)

* **[!UICONTROL Conjuntos de datos]**: todos los datos que se incorporan a Adobe Experience Platform se conservan dentro del lago de datos como conjuntos de datos. Un conjunto de datos es una construcción de almacenamiento y administración para una colección de datos, normalmente una tabla, que contiene un esquema (columnas) y campos (filas). [Más información](../data/get-started-datasets.md)

* **[!UICONTROL Consultas]**: utilice el servicio de consulta de Adobe Experience Platform para escribir y ejecutar consultas, ver consultas ejecutadas anteriormente y acceder a las guardadas por usuarios de su organización. [Más información](../data/get-started-queries.md)

* **[!UICONTROL Monitorización]**: utilice este menú para monitorizar la ingesta de datos en la interfaz de usuario de Adobe Experience Platform. [Más información](https://experienceleague.adobe.com/docs/experience-platform/ingestion/quality/monitor-data-ingestion.html?lang=es){target=&quot;_blank&quot;}

**[!UICONTROL CONEXIONES]**

* **[!UICONTROL Fuentes]**: utilice este menú para introducir datos de una variedad de fuentes, como aplicaciones de Adobe, almacenamiento basado en la nube, bases de datos y mucho más, así como estructurar, etiquetar y mejorar los datos entrantes. [Más información](get-started-sources.md)

**[!UICONTROL CLIENTE]**

* **[!UICONTROL Segmentos]**: cree y administre definiciones de segmentos de Experience Platform para aprovecharlas en sus recorridos. [Más información](../segment/about-segments.md)

* **[!UICONTROL Perfiles]**: el perfil del cliente en tiempo real crea una vista integral de cada uno de sus clientes individuales, combinando datos de varios canales, incluidos datos en línea, sin conexión, CRM y de terceros. [Más información](../segment/get-started-profiles.md)

* **[!UICONTROL Identidades]**: el servicio de identidad de Adobe Experience Platform administra la identificación de sus clientes en varios dispositivos, canales cruzados y casi en tiempo real en lo que se conoce como gráfico de identidad dentro de Adobe Experience Platform. [Más información](../segment/get-started-identity.md)

**[!UICONTROL ADMINISTRACIÓN]**

* **[!UICONTROL Administración de recorridos]**: utilice este menú para configurar [eventos](../event/about-events.md), [fuentes de datos](../datasource/about-data-sources.md) y [acciones](../action/action.md) que se utilizarán en los recorridos.

* **[!UICONTROL Zonas protegidas]**: Adobe Experience Platform proporciona entornos limitados que dividen una sola instancia en entornos virtuales independientes para ayudarle a desarrollar aplicaciones de experiencia digital y hacer que evolucionen. [Más información](../administration/sandboxes.md)

* **[!UICONTROL Alertas]**: la interfaz de usuario le permite ver un historial de alertas recibidas en función de las métricas reveladas por Adobe Experience Platform Observability Insights. La IU también le permite ver, habilitar y deshabilitar las reglas de alerta disponibles. [Más información](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=es){target=&quot;_blank&quot;}


## Casos de uso dentro del producto {#in-product-uc}

Aproveche los casos de uso de [!DNL Adobe Journey Optimizer] de la página de inicio y proporcione información rápida para crear un recorrido del cliente.

![](assets/use-cases-home.png)

Los casos de uso disponibles son:

* **Cree perfiles de prueba**, para crear perfiles de prueba con la plantilla CSV a fin de probar mensajes y recorridos personalizados. Aprenda a implementar este caso de uso [en esta página](../segment/creating-test-profiles.md#use-case-1).
* **Envíe un mensaje de cumpleaños a los clientes** para que envíen automáticamente un correo electrónico a fin de felicitar a sus clientes. (próximamente)
* **Envíe correos electrónicos para incorporar nuevos clientes** y enviar fácilmente hasta dos correos electrónicos para dar la bienvenida a sus clientes recién registrados. (próximamente)
* **Envíe mensajes push a la lista importada de clientes** para enviar rápidamente una notificación push a una lista de clientes importados desde un archivo CSV. (próximamente)

Haga clic en **[!UICONTROL Ver detalles]** para obtener más información acerca de cada caso de uso.

Haga clic en el botón **[!UICONTROL Comenzar]** para iniciar el caso de uso.

Puede acceder a los casos de uso ejecutados desde el botón **[!UICONTROL Ver biblioteca de casos de uso]**.

## Accesibilidad{#accessibility}

Las funciones de accesibilidad de [!DNL Adobe Journey Optimizer] se heredan de Adobe Experience Platform:

* Accesibilidad del teclado
* Contraste de color
* Validación de campos obligatorios

[Más información](https://experienceleague.adobe.com/docs/experience-platform/accessibility/features.html?lang=es){target=&quot;_blank&quot;} en la documentación de Adobe Experience Platform.

Puede utilizar estos métodos abreviados del teclado comunes en [!DNL Journey Optimizer]:

| Acción | Acceso directo |
| --- | --- |
| Desplazamiento entre elementos, secciones y grupos de menús de la interfaz de usuario | Tabulación |
| Retroceder entre elementos, secciones y grupos de menús de la interfaz de usuario | Mayús + Tab |
| Desplazarse dentro de las secciones para definir el enfoque en elementos individuales | Flecha |
| Seleccionar o borrar un elemento que esté enfocado | Intro o barra espaciadora |
| Cancelar una selección, contraer un panel o cerrar un cuadro de diálogo | ESC |

[Más información](https://experienceleague.adobe.com/docs/experience-platform/accessibility/custom.html?lang=es){target=&quot;_blank&quot;} en la documentación de Adobe Experience Platform.

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
    <td rowspan="3">Lienzo de recorrido en estado de borrador</td>
    <td>Añadir una actividad de la paleta izquierda en la primera posición disponible, de arriba a abajo</td>
    <td>Doble clic en la actividad</td>
  </tr>
  <tr>
    <td>Seleccionar todas las actividades</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
  <tr>
    <td>Eliminación de las actividades seleccionadas</td>
    <td>Use la tecla Suprimir o Retroceso y a continuación Intro para confirmar la eliminación</td>
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
    <td>Intro</td>
  </tr>
  <tr>
    <td>Descartar cambios y cerrar el panel de configuración</td>
    <td>ESC</td>
  </tr>
  <tr>
    <td rowspan="4">Recorrido en modo de prueba</td>
    <td>Habilitar o deshabilitar el modo de prueba</td>
    <td>T</td>
  </tr>
  <tr>
    <td>Activa un evento en un recorrido basado en eventos</td>
    <td>E</td>
  </tr>
  <tr>
    <td>

Activar un evento en un recorrido basado en segmentos para el cual la opción **[!UICONTROL Un solo perfil a la vez]** está activada

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
    <td>Guardar los cambios o confirmar la acción</td>
    <td>Intro</td>
  </tr>
  <tr>
    <td>Cerrar la ventana</td>
    <td>ESC</td>
  </tr>
  <tr>
    <td>Editor de expresiones simples</td>
    <td>Seleccionar y añadir un campo</td>
    <td>Doble clic en un campo</td>
  </tr>
  <tr>
    <td>Explorar los campos XDM</td>
    <td>Seleccionar todos los campos de un nodo</td>
    <td>Seleccionar el nodo principal</td>
  </tr>
  <tr>
    <td>Vista previa de carga útil</td>
    <td>Seleccionar la carga útil</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
</table>

## Buscar ayuda y asistencia {#find-help}

Acceda a las páginas de ayuda clave de Adobe Journey Optimizer desde la sección inferior de la página de inicio.

Utilice el icono **Ayuda** para acceder a las páginas de ayuda, ponerse en contacto con el servicio de asistencia técnica y compartir comentarios. Puede buscar artículos de ayuda y vídeos en el campo de búsqueda.

![](assets/ajo-help.png)

## Navegadores admitidos {#browsers}

La interfaz de Adobe [!DNL Journey Optimizer] está diseñada para funcionar de forma óptima en la última versión de Google Chrome. Es posible que tenga problemas al utilizar determinadas funciones en versiones anteriores u otros navegadores.

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

* Haga clic en **Preferencias** desde el avatar, en la parte superior derecha.
   ![](assets/preferences.png)
* A continuación, haga clic en el idioma mostrado debajo de su dirección de correo electrónico
* Seleccione el idioma que prefiera y haga clic en **Guardar**. Puede seleccionar un segundo idioma en caso de que el componente que esté utilizando no esté localizado en su primer idioma.
   ![](assets/select-language.png)

## Buscar{#unified-search}

En cualquier lugar de la interfaz de Adobe Journey Optimizer, utilice la búsqueda unificada de Adobe Experience Cloud en el centro de la barra superior para buscar recursos, recorridos, conjuntos de datos y más en las zonas protegidas.

Empiece a introducir contenido para mostrar los resultados principales. Los artículos de ayuda sobre las palabras clave introducidas también se muestran en los resultados.

![](assets/unified-search.png)

Pulse **Entrar** para acceder a todos los resultados y filtrar por objeto empresarial.

![](assets/search-and-filter.png)

## Filtrar listas{#filter-lists}

En la mayoría de las listas, una barra de búsqueda le permite buscar un elemento específico y seleccionar criterios de filtrado.

Se puede acceder a los filtros haciendo clic en el icono de filtro en la parte superior izquierda de la lista. El menú de filtros permite filtrar los elementos mostrados según diferentes criterios. Puede elegir mostrar únicamente los elementos de un determinado tipo o estado, los que ha creado o los modificados en los últimos 30 días. Las opciones difieren según el contexto.

En la lista de recorridos, puede filtrarlos según su estado, tipo y versión en **[!UICONTROL Estado y versión de filtros]**. El tipo puede ser: **[!UICONTROL Evento unitario]**, **[!UICONTROL Clasificación del segmento]**, **[!UICONTROL Leer segmento]**, **[!UICONTROL Evento empresarial]** o **[!UICONTROL Ráfaga]**. Puede elegir mostrar solo los recorridos que utilizan un evento, un grupo de campos o una acción en **[!UICONTROL Filtros de actividad]** y **[!UICONTROL Filtros de datos]**. Los **[!UICONTROL Filtros de publicaciones]** permiten seleccionar una fecha de publicación o un usuario. Puede elegir, por ejemplo, mostrar las versiones más recientes de recorridos en directo que se publicaron ayer. [Más información](../building-journeys/using-the-journey-designer.md).

>[!NOTE]
>
>Tenga en cuenta que las columnas mostradas se pueden personalizar mediante el botón de configuración en la parte superior derecha de las listas. La personalización se guarda para cada usuario.

Utilice las columnas **[!UICONTROL Última actualización]** y **[!UICONTROL Última actualización hecha por]** para comprobar cuándo se produjo la última actualización de los recorridos y quién los guardó.

![](assets/filter-journeys.png)

En los paneles Evento, Fuente de datos y Configuración de acciones, el campo **[!UICONTROL Utilizado en]** muestra el número de recorridos que utilizan ese evento, grupo de campos o acción en particular. Puede hacer clic en el botón **[!UICONTROL Ver recorridos]** para mostrar la lista de los recorridos correspondientes.

![](assets/journey3bis.png)

En las listas, puede realizar acciones básicas por cada elemento. Por ejemplo, puede duplicar o eliminar un elemento.

![](assets/journey4.png)
