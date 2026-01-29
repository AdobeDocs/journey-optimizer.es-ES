---
solution: Journey Optimizer
product: journey optimizer
title: Panel de control de uso de licencias
description: Obtenga información acerca del tablero de uso de licencias de Journey Optimizer
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 7e91face-c8f4-4e70-9123-9e36bae7e67e
source-git-commit: db1e4ee5b2b4bb3a3d7d9e86aded14ad3c613765
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# Panel de control de uso de licencias {#license-usage}

La [!DNL Adobe Journey Optimizer] [interfaz de usuario](../start/user-interface.md) proporciona un panel que muestra información importante sobre el uso de licencias de su organización, tal como se captura durante una instantánea diaria.

Para acceder a este tablero, ve a **[!UICONTROL Administración]** > **[!UICONTROL Uso de licencias]**. Se abrirá la ficha **[!UICONTROL Información general]**, que muestra el tablero.

![Resumen del tablero de uso de licencias](assets/license-usage-dashboard.png)

>[!NOTE]
>
>* Para ver el tablero, debe tener el permiso [Ver tablero de uso de licencias](https://experienceleague.adobe.com/docs/experience-platform/dashboards/permissions.html?lang=es#available-permissions){target="_blank"}.
>
>* Ciertas métricas (por ejemplo, calcular horas y correos electrónicos) no se muestran para los entornos limitados de desarrollo, como indica `N/A` en la columna de cuota. En el panel solo se muestran valores no nulos: cuando las métricas son cero o están cerca de cero, no se rellenan.


Para [!DNL Adobe Journey Optimizer], el tablero le permite comprobar el número de **perfiles atractivos**.

## ¿Qué es un perfil atractivo? {#what-is-engageable-profile}

Un **perfil atractivo** es un registro de información que representa a un individuo que está almacenado en el servicio de perfil y que ha sido contratado por recorridos o campañas.

Características clave de los perfiles atractivos:

* **Período móvil de 12 meses**: Los perfiles atractivos se cuentan según la participación en los últimos 12 meses. Esta métrica muestra el número de perfiles únicos con los que ha intentado interactuar mediante las capacidades de creación, toma de decisiones, envío, experimentación u orquestación de Journey Optimizer.

* **Recuento único por zona protegida**: Si un perfil introduce varios recorridos o campañas en una zona protegida, se cuenta solo una vez como un único perfil atractivo para esa zona protegida.

* **Según la audiencia a la que se puede dirigir**: los perfiles atractivos se calculan a partir de la audiencia a la que se puede dirigir. El recuento representa la audiencia comprometida en los últimos 12 meses que utiliza cualquiera de las capacidades de Journey Optimizer, de su audiencia total a la que se puede dirigir.

* **Comportamiento de la métrica**: El recuento de perfiles atractivos:
   * Pueden aumentar cuando se comprometen nuevos perfiles a través de recorridos o campañas
   * No puede disminuir a menos que no haya participación con determinados perfiles durante más de 12 meses
   * Puede disminuir cuando los perfiles seudónimos se vinculan a perfiles conocidos

>[!NOTE]
>
>Si observa un pico repentino en su recuento de perfiles atractivos, consulte la [sección Resolución de problemas](#troubleshooting-engageable-profiles) a continuación para obtener instrucciones detalladas sobre cómo comprender y resolver el problema.

## Solución de problemas: aumento significativo en el recuento de perfiles atractivos {#troubleshooting-engageable-profiles}

Si observa un pico repentino en el recuento de Perfiles atractivos (por ejemplo, perfiles que aumentan de cientos de miles a millones en un día), esta sección proporciona instrucciones para comprender y abordar el problema.

### Explicación del aumento

La métrica Perfiles atractivos refleja la cantidad de perfiles únicos comprometidos por recorridos o campañas en los últimos 12 meses. Un aumento repentino puede deberse a:

* Audiencias grandes segmentadas por nuevos recorridos o campañas
* Cambios en los conjuntos de datos habilitados para el servicio de perfil
* Procesamiento por lotes de audiencias que no se han involucrado recientemente

### Pasos de resolución

Para solucionar este problema, siga estos pasos:

1. **Comprenda la lógica de recuento de perfiles:**

   * Los perfiles atractivos se calculan en función de perfiles únicos comprometidos por recorridos o campañas en los últimos 12 meses.
   * Si un perfil introduce varios recorridos, se cuenta como un perfil atractivo para esa zona protegida.
   * La métrica no puede disminuir a menos que no haya participación con determinados perfiles durante más de 12 meses o si los perfiles seudónimos están vinculados a perfiles conocidos.
   * Los perfiles atractivos se calculan mediante la Audiencia a la que se puede dirigir un cliente.
   * La audiencia comprometida en los últimos 12 meses que utiliza cualquiera de las capacidades de Journey Optimizer, de una Audiencia direccionable total, determina el recuento de Perfiles atractivos.

2. **Investigue recorridos, campañas y toma de decisiones dirigidas a grandes audiencias:**

   * Revise los recorridos y campañas recientes dirigidos a un gran número de perfiles mediante [Consultas de perfiles atractivas](../reports/query-examples.md#engageable-profiles-queries) o [Servicio de consultas](https://experienceleague.adobe.com/es/docs/experience-platform/query/home){target="_blank"}.
   * Identifique las versiones de recorridos específicas que contribuyeron al pico en los recuentos de perfiles.
   * Es probable que los recorridos, las campañas y las decisiones que impliquen nuevos perfiles produzcan un aumento en el recuento de eventos en los conjuntos de datos de Recorrido, lo que contribuirá al aumento en el recuento de perfiles atractivos.

3. **Filtrar audiencias a nivel de recorrido y campañas:**

   * Aplique filtros en el nivel de audiencia antes de iniciar recorridos o campañas para evitar aumentos innecesarios en Perfiles atractivos.
   * Asegúrese de que solo las audiencias relevantes estén segmentadas durante las participaciones.

4. **Reducir tamaño de audiencia direccionable:**

   * Elimine los perfiles seudónimos si es necesario. Tenga en cuenta que esta acción afecta tanto a Journey Optimizer como a Real-Time Customer Data Platform.
   * Obtenga más información acerca de la [caducidad de datos de perfil seudónimo](https://experienceleague.adobe.com/es/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"} en la Guía de perfil del cliente en tiempo real.
   * **Nota:** La caducidad de los datos del perfil seudónimo no se puede configurar a través de la interfaz de usuario o las API de Platform. Debe ponerse en contacto con el servicio de asistencia para habilitar esta función.

5. **Supervisar cambios en el conjunto de datos:**

   * Compruebe los conjuntos de datos habilitados para la generación de perfiles y asegúrese de que no contengan un ECID (Experience Cloud ID) excesivo.
   * Si es necesario, elimine conjuntos de datos con recuentos de ECID altos y vuelva a crearlos con registros reducidos.

6. **Desarrollar una estrategia de reducción a largo plazo:**

   * El recuento de Perfiles atractivos disminuirá de forma natural si determinados perfiles permanecen inactivos durante más de 12 meses.

**Ver también:**

* [Ejemplos de consultas de perfiles interactivos](../reports/query-examples.md#engageable-profiles-queries): consultas de muestra para supervisar y analizar sus perfiles interactivos
* [Descripción general del servicio Adobe Experience Platform Query](https://experienceleague.adobe.com/es/docs/experience-platform/query/home){target="_blank"}

## Documentación relacionada {#related-documentation}

Obtenga más información en la documentación de Adobe Experience Platform:

* [Resumen del tablero de uso de licencias](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=es){target="_blank"}
* [Explorando el tablero de uso de licencias](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=es#exploring-the-license-usage-dashboard){target="_blank"}
* [Métricas disponibles](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=es#available-metrics){target="_blank"}
* [Caducidad de datos de perfil seudónimo](https://experienceleague.adobe.com/docs/experience-platform/profile/pseudonymous-profiles.html?lang=es){target="_blank"}
