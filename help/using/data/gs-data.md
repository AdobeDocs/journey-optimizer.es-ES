---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a la gestión de datos en Journey Optimizer
description: Obtenga información sobre cómo trabajar con datos en Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: datos, administración, plataforma
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 96%

---

# Introducción a la administración de datos {#about-data}

La riqueza y la cobertura de los datos del cliente final es lo que define la solidez y el éxito de cualquier solución de experiencia del cliente; y estos datos son sagrados y del mayor valor para cualquier cliente. La selección de tecnología está ahora integrada de forma inherente con una evaluación rigurosa de las capacidades de administración de datos.

Con [!DNL Adobe Journey Optimizer] puede administrar, conservar y exportar fácilmente estos datos a plataformas o sistemas que forman parte de su oferta tecnológica. 

**Mis datos, mis reglas**: [!DNL Adobe Journey Optimizer] crea de forma continua (y en tiempo real) un conjunto completo de datos de perfil del cliente, además de todos los datos de recorrido y los datos de ofertas inherentes a sus operaciones. Las versiones de Strawman de los datos de usuario ingeridos desde sus bases de datos se enriquecen y transforman en datos de alto valor con cobertura y profundidad. Desea que estos datos estén seguros y, al mismo tiempo, sean ubicuos, de modo que pueda aprovechar su valor en todo el ecosistema informático.

En general, la flexibilidad que desea de sus datos es la siguiente:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinos" src="assets/do-not-localize/dest.png" /> 
    <br>Disponible en otros destinos: mientras [!DNL Adobe Journey Optimizer] establece una sinergia e integra los datos para lograr una experiencia del cliente hiperpersonalizada; usted desea que estos datos se transmitan a otros sistemas del panorama tecnológico general, mientras busca otras formas de aprovechar estos datos.
    <div>
     <a href="../integrations/ajo-integrations.md">Más información</a></div>
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
    <br>Eliminación de la base de una cronología acordada para la política: la eliminación de datos es un aspecto crítico de la protección de datos y un paso clave en todos los procesos de gobernanza de datos. [!DNL Adobe Journey Optimizer] puede producir más datos de los necesarios. Además, debe tener el máximo cuidado con lo que sucede después de la duración requerida para un conjunto de datos, ya sea por utilidad o por regulación. El control que necesita es eliminar datos en cualquier momento dado. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">Más información</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], en el que [!DNL Adobe Journey Optimizer] se ha creado, proporciona los niveles más altos de control de datos para usted, durante la participación y al final de la misma. En [!DNL Journey Optimizer] tiene control total sobre los datos (que se introducen en o se generan mediante, [!DNL Journey Optimizer]), la gobernanza superpuesta a esos datos y los destinos a los que se envían esos datos.

Todos los datos se consideran propiedad de los clientes y solo pueden mantenerse, cifrarse, distribuirse o destruirse si así lo solicita. Adobe actúa como su fiduciario, sin absolutamente ningún derecho a sus datos.

Puede usar la flexibilidad de datos de [!DNL Journey Optimizer] para satisfacer sus requisitos específicos relacionados con la retención, el archivado o la eliminación de datos:

* **Extracción/exportación de datos**: puede iniciar la extracción de los datos de origen en cualquier momento mediante la API de acceso a datos sin penalizaciones ni retrasos. La [API de acceso a datos](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=es){target="_blank"} proporciona a los usuarios una interfaz RESTful centrada en la detección y accesibilidad de conjuntos de datos ingeridos en [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  Tenga en cuenta que el contenido utilizado en recorridos o campañas no se puede extraer mediante los métodos API o Destino mencionados anteriormente.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer's default setting of retaining this data for up to 91 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization's data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html?lang=es){target="_blank"}.
-->

* **Depuraciones y mecanismos de archivado**: la depuración de datos y el archivado se pueden definir y automatizar libremente en [!DNL Adobe Journey Optimizer] para automatizar las políticas de retención de datos. Es posible definir diferentes estrategias de caducidad para las distintas entidades de datos. También se pueden definir mecanismos de exportación para exportar automáticamente los datos de caducidad antes de depurarlos o archivarlos.

  El espacio de trabajo Ciclo de vida de datos le permite crear y supervisar varias tareas de ciclo de vida de datos, incluida la eliminación de identidades de consumidores y la programación de la caducidad de conjuntos de datos. Este espacio de trabajo está disponible con el Escudo de seguridad y privacidad y con el Escudo de atención sanitaria. Obtenga más información en [esta página](../privacy/data-hygiene.md).

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Extracción de datos al terminar la participación/salida**: cuando se rescinde el contrato, los datos se eliminan por completo del espacio de almacenamiento de Adobe. Además, puede extraer extractos de perfiles completos antes de finalizar un acuerdo. Esta función no tiene costes adicionales. Esto se puede hacer en cualquier momento y no solo tras la finalización.

Los métodos anteriores están definidos contractualmente y expuestos en detalle en el acuerdo de procesamiento de datos (DPA) que Adobe acuerda mutuamente con usted al principio de una participación. Las aplicaciones de Adobe, incluyendo [!DNL Journey Optimizer], se diseñan en torno al principio de que los datos de cada cliente se traten como el recurso de datos propiedad de ese cliente.
