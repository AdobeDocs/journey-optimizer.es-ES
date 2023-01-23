---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los datos en Journey Optimizer
description: Obtenga información sobre cómo trabajar con datos en Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: datos, administración, plataforma
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Introducción a la administración de datos en [!DNL Journey Optimizer] {#about-data}

La riqueza y la cobertura de los datos del cliente final es lo que define la solidez y el éxito de cualquier solución de experiencia del cliente; y estos datos son sagrados y tienen el mayor valor para un cliente determinado. La selección de tecnología ahora está intrínsecamente integrada con una evaluación estricta de las capacidades de administración de datos.

con [!DNL Adobe Journey Optimizer], puede administrar, conservar y exportar fácilmente estos datos a plataformas o sistemas que forman parte de su pila de tecnología.

**Mis datos, mis reglas** - [!DNL Adobe Journey Optimizer] continuamente (y en tiempo real) crea un completo conjunto de datos de perfil del cliente, además de todos los datos de recorrido y los datos de oferta inherentes a sus operaciones. Las versiones &quot;Strawman&quot; de los datos de usuario incorporados desde sus bases de datos se enriquecen y transforman en datos de alto valor con cobertura y profundidad. Desea que estos datos sean seguros y al mismo tiempo omnipresentes, de modo que pueda aprovechar su valor en todo su ecosistema de TI.

En general, la flexibilidad que desea con los datos es:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinos" src="assets/do-not-localize/dest.png" /> 
    <br>Disponible en otros destinos: Aunque [!DNL Adobe Journey Optimizer] sinergia e integra los datos para una experiencia de cliente hiperpersonalizada, desea estos datos en otros sistemas del entorno tecnológico general, mientras busca otras formas de aprovechar estos datos.
    <div>
     <a href="../start/ajo-integrations.md">Más información</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="directiva" src="assets/do-not-localize/policy.png" /> 
    <br>Se eliminan las bases de una cronología acordada para su política: la eliminación de datos es un aspecto crítico de la protección de datos y es un paso clave en todos los procesos de control de datos. [!DNL Adobe Journey Optimizer] pueden producir más datos de los necesarios. Además, desea tener el máximo cuidado con lo que sucede después de la duración requerida para un conjunto de datos, ya sea por la utilidad o la regulación. El control que necesita es eliminar datos en un momento dado. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">Obtenga más información sobre la higiene de los datos en la documentación de Adobe Experience Platform</a></div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], sobre el cual [!DNL Adobe Journey Optimizer] está creado, le proporciona los niveles más altos de control de datos durante la participación, así como al final de la participación. Within [!DNL Journey Optimizer], tiene control total sobre los datos (introducidos o generados por, [!DNL Journey Optimizer]), la administración superpuesta a esos datos y los destinos a los que se envían.

Todos los datos se consideran propiedad de los clientes y solo se pueden mantener, encriptar, distribuir o destruir a petición suya. Adobe actúa como su fiduciario, sin ningún derecho a sus datos.

Puede usar la variable [!DNL Journey Optimizer]la flexibilidad de los datos de para satisfacer sus requisitos específicos relacionados con la retención, el archiving o la eliminación de datos:

* **Extracción/exportación de datos**: Puede iniciar la extracción de datos de origen en cualquier momento a través de la API de acceso a datos sin penalizaciones ni retrasos en el tiempo. La variable [API de acceso a datos](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target="_blank"} proporciona a los usuarios una interfaz RESTful centrada en la capacidad de detección y accesibilidad de conjuntos de datos ingestados dentro de [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Tenga en cuenta que el contenido utilizado en recorridos o campañas no se puede extraer mediante los métodos API o Destination mencionados anteriormente.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Purgas y mecanismos de archivado**: La depuración de datos y el archivado se pueden definir y automatizar libremente en [!DNL Adobe Journey Optimizer] para automatizar las políticas de retención de datos. Es posible definir diferentes estrategias de envejecimiento para las diferentes entidades de datos. También se pueden definir mecanismos de exportación para exportar automáticamente los datos de antigüedad antes de depurarlos o archivarlos.

   El espacio de trabajo Higiene de los datos en la interfaz de usuario de Adobe Experience Platform le permite crear y supervisar diversas tareas de higiene de los datos, como la eliminación de identidades de consumidores y la programación de caducidades de conjuntos de datos. Este espacio de trabajo está disponible con el Escudo de seguridad y privacidad y con el Escudo de salud. Obtenga más información en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target="_blank"}.

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Extracción de datos al finalizar o salir del compromiso**: Cuando finaliza el contrato, los datos se eliminan completamente del espacio de almacenamiento del Adobe. Además, puede extraer extractos de perfil completos antes de finalizar un acuerdo. Esta función no conlleva ningún coste adicional. Esto se puede hacer en cualquier momento y no sólo una vez terminada.

Los métodos anteriores se definen contractualmente y se exponen detalladamente en el acuerdo de procesamiento de datos (DPA) que el Adobe está de acuerdo entre sí al principio de una participación. aplicaciones de Adobe, incluidas [!DNL Journey Optimizer], se diseñan según el principio de que los datos de cada cliente se tratan como activos de datos propietarios del cliente.
