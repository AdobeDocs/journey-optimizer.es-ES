---
solution: Journey Optimizer
product: journey optimizer
title: Examinar y filtrar sus recorridos
description: Examinar y filtrar sus recorridos en Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, primero, inicio, inicio rápido, audiencia, evento, acción
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 32%

---

# Examinar y filtrar sus recorridos {#browse-journeys}

## Acceso a recorridos {#journey-access}

### panel de recorrido {#dashboard-jo}

En la sección de menú ADMINISTRACIÓN DE RECORRIDO, haga clic en **[!UICONTROL Recorridos]**. Hay dos fichas disponibles: **[!UICONTROL Información general]** y **[!UICONTROL Examinar]**.

* La pestaña **[!UICONTROL Información general]** muestra un panel con métricas clave relacionadas con tus recorridos:

   * **Perfiles procesados**: número total de perfiles procesados en las últimas 24 horas.
   * **recorridos activos**: número total de recorridos activos con tráfico durante las últimas 24 horas. Los recorridos activos incluyen **recorridos unitarios** (basados en eventos) y **recorridos por lotes** (lectura de audiencia).
   * **Tasa de error**: proporción de todos los perfiles en error comparada con la cantidad total de perfiles que ingresaron en las últimas 24 horas.
   * **Tasa de descarte**: proporción de todos los perfiles descartados en comparación con la cantidad total de perfiles que ingresaron en las últimas 24 horas. Un perfil descartado representa a alguien que no cumple los requisitos para entrar en el recorrido, por ejemplo, debido a un área de nombres incorrecta o a reglas de reentrada.

  >[!NOTE]
  >
  >Este tablero tiene en cuenta los recorridos con tráfico de las últimas 24 horas. Solo se muestran los recorridos a los que tiene acceso. Las métricas se actualizan cada 30 minutos y solo cuando hay nuevos datos disponibles.

  ![](assets/journeys-dashboard.png)

* La ficha **[!UICONTROL Examinar]** muestra la lista de recorridos existentes. Puede buscar recorridos, utilizarlos y realizar acciones básicas en cada elemento. Por ejemplo, puede duplicar o eliminar un elemento.

  ![](assets/journeys-browse.png)

### Filtrar sus recorridos {#filter}

En la lista de recorridos, puede aprovechar varios filtros para restringir la lista de recorridos y mejorar la legibilidad.

![](assets/filter-journeys.png)

Estas son las distintas operaciones de filtrado que puede realizar:

Filtre los recorridos según su estado, tipo, versión y etiquetas asignadas de **[!UICONTROL Estado y versión de filtros]**.

El tipo puede ser: **[!UICONTROL Evento unitario]**, **[!UICONTROL Calificación de audiencia]**, **[!UICONTROL Leer audiencia]** o **[!UICONTROL Evento empresarial]**.

El estado puede ser el siguiente:

* **Cerrado**: el recorrido se ha cerrado con el botón **Cerca de nuevas entradas**. El recorrido deja de permitir que nuevas personas entren en el recorrido. Las personas que ya están en el recorrido pueden terminar el recorrido normalmente.
* **Borrador**: el recorrido se encuentra en su primera fase. Aún no se ha publicado.
* **Borrador (prueba)**: el modo de prueba se ha activado con el botón **Modo de prueba**.
* **Finalizado**: el recorrido cambia automáticamente a este estado después del tiempo de espera global de [91 días](journey-properties.md#global_timeout). Los perfiles que ya están en el recorrido finalizan el recorrido normalmente. Los nuevos perfiles ya no pueden entrar en el recorrido.
* **Activo**: el recorrido se ha publicado con el botón **Publicar**.
* **Detenido**: el recorrido se ha desactivado con el botón **Detener**. Todos los individuos abandonan el recorrido al instante.

>[!NOTE]
>
>El ciclo de vida de creación de Recorridos también incluye un conjunto de estados intermedios que no están disponibles para el filtrado: &quot;Publicación&quot; (entre &quot;Borrador&quot; y &quot;Activo&quot;), &quot;Activación del modo de prueba&quot; o &quot;Desactivación del modo de prueba&quot; (entre &quot;Borrador&quot; y &quot;Borrador (prueba)&quot;) y &quot;Detención&quot; (entre &quot;Activo&quot; y &quot;Detenido&quot;). Cuando un recorrido está en un estado intermedio, es de solo lectura.

Use **[!UICONTROL filtros de creación]** para filtrar recorridos según su fecha de creación o el usuario que los creó.

Mostrar recorridos que utilizan un evento, un grupo de campos o una acción específicos de **[!UICONTROL Activity Filters]** y **[!UICONTROL Data Filters]**.

Use **[!UICONTROL Filtros de publicación]** para seleccionar una fecha de publicación o un usuario. Puede elegir, por ejemplo, mostrar las versiones más recientes de recorridos en directo que se publicaron ayer.

Para filtrar recorridos según un intervalo de fechas específico, seleccione **[!UICONTROL Personalizado]** de la lista desplegable **[!UICONTROL Publicado]**.

Además, en los paneles Evento, Fuente de datos y Configuración de acciones, el campo **[!UICONTROL Utilizado en]** muestra el número de recorridos que utilizan ese evento, grupo de campos o acción en particular. Puede hacer clic en el botón **[!UICONTROL Ver recorridos]** para mostrar la lista de los recorridos correspondientes.

![](assets/journey3bis.png)


## Versiones de recorridos {#journey-versions}

En la lista de recorridos, todas las versiones del recorrido se muestran con el número de versión. Cuando busca un recorrido, las versiones más recientes aparecen en la parte superior de la lista la primera vez que se abre la aplicación. A continuación, puede definir la clasificación que desee y la aplicación la mantendrá como preferencia del usuario. La versión del recorrido también se muestra en la parte superior de la interfaz de la edición de recorrido, encima del lienzo.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Normalmente, un perfil no puede estar presente varias veces en el mismo recorrido y al mismo tiempo. Si la reentrada está activada, un perfil puede volver a entrar en un recorrido, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido. [Más información](end-journey.md).

Si necesita modificar a un recorrido activo, cree una nueva versión del recorrido.

1. Abra la última versión del recorrido activo, haga clic en **[!UICONTROL Crear una nueva versión]** y confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Solo puede crear una nueva versión a partir de la última versión de un recorrido.

1. Realice las modificaciones necesarias, haga clic en **[!UICONTROL Publicar]** y confirme.

Desde el momento en que se publique el recorrido, las personas empezarán a fluir hacia la última versión del recorrido. Las personas que ya han accedido a una versión anterior permanecerán en ella hasta que finalicen el recorrido. Si más tarde vuelven a entrar en el mismo recorrido, accederán a la versión más reciente.

Las versiones de recorrido se pueden detener individualmente. Todas las versiones de los recorridos tienen el mismo nombre.

Cuando se publica una nueva versión de un recorrido, la versión anterior finaliza automáticamente y cambia al estado **Cerrado.**. No puede haber ninguna entrada en el recorrido. Aunque detenga la versión más reciente, la versión anterior permanecerá cerrada.



## Duplicación de un recorrido {#duplicate-a-journey}

Puede duplicar un recorrido existente de la ficha **Examinar**. Todos los objetos y configuraciones se duplican en la copia de recorrido.

Para ello, siga los pasos a continuación:

1. Vaya al recorrido que desee copiar y haga clic en el icono **Más acciones** (los tres puntos junto al nombre del recorrido).
1. Seleccione **Duplicar**.

   ![Duplicar un recorrido](assets/duplicate-jo.png)

1. Introduzca el nombre del recorrido y confírmelo. También puede cambiar el nombre en la pantalla de propiedades del recorrido. De manera predeterminada, el nombre se establece de la siguiente manera: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. El nuevo recorrido se crea y está disponible en la lista de recorridos.

