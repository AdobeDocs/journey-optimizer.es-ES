---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los datos en [!DNL Journey Optimizer]
description: Aprenda a trabajar con los datos en [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 2dcfcc8d7006c92e046152db5ac1288bdde8b063
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 3%

---

# Introducción a la administración de datos en [!DNL Journey Optimizer] {#about-data}

La riqueza y la cobertura de los datos del cliente final es lo que define la solidez y el éxito de cualquier solución de experiencia del cliente; y estos datos son sagrados y tienen el mayor valor para un cliente determinado. La selección de tecnología ahora está intrínsecamente integrada con una evaluación estricta de las capacidades de administración de datos.

Con Adobe Journey Optimizer puede administrar, conservar y exportar fácilmente estos datos a plataformas o sistemas que forman parte de su oferta tecnológica.

**Mis datos, mis reglas** : Journey Optimizer crea continuamente (y en tiempo real) un completo conjunto de datos de perfil de cliente, además de todos los datos de recorrido y los datos de oferta inherentes a sus operaciones. Las versiones &quot;Strawman&quot; de los datos de usuario incorporados desde sus bases de datos se enriquecen y transforman en datos de alto valor con cobertura y profundidad. Desea que estos datos sean seguros y al mismo tiempo omnipresentes, de modo que pueda aprovechar su valor en todo su ecosistema de TI.

En general, la flexibilidad que desea de los datos se triplica:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinos" src="assets/do-not-localize/dest.png" /> 
    <br>Disponible en otros destinos : Aunque Journey Optimizer sinergia e integra los datos para una experiencia de cliente hiperpersonalizada, desea que estos datos se compartan con otros sistemas en el panorama tecnológico general, mientras busca otras formas de aprovechar estos datos.
    <div>
     <a href="../start/ajo-integrations.md">Más información</a></div>
    </div>
    <br>
  </td>
</tr>
  <td>
    <div><img alt="retención" src="assets/do-not-localize/retention.png" />  
    <br>Conservados durante un período de tiempo estipulado: las regulaciones del sector o regionales (como el RGPD o la CCPA) o las políticas de control interno de datos estipulan cuánto tiempo o cuánto tiempo de duración deben mantenerse o archivarse los datos en Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Más información</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <div><img alt="directiva" src="assets/do-not-localize/policy.png" /> 
    <br>Se eliminan las bases de una cronología acordada para su política: la eliminación de datos es un aspecto crítico de la protección de datos y es un paso clave en todos los procesos de control de datos. Journey Optimizer puede producir más datos de lo necesario. Además, desea tener el máximo cuidado con lo que sucede después de la duración requerida para un conjunto de datos, ya sea por la utilidad o la regulación. El control que necesita es eliminar datos en un momento dado. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">Obtenga más información sobre la higiene de los datos en la documentación de Adobe Experience Platform</a></div>
  </td>
</tr>
</table>

Adobe Experience Platform, en el que se basa Journey Optimizer, proporciona los niveles más altos de control de datos durante la participación, así como al final de la participación. En Journey Optimizer, tiene control total sobre los datos (introducidos o generados por Journey Optimizer), el control superpuesto a esos datos y los destinos a los que se envían.

Todos los datos se consideran propiedad de los clientes y solo se pueden mantener, encriptar, distribuir o destruir a petición suya. Adobe actúa como su fiduciario, sin ningún derecho a sus datos.

Puede utilizar la flexibilidad de los datos de Journey Optimizer para satisfacer sus requisitos específicos relacionados con la retención, el archivado o la eliminación de datos:

* **Extracción/exportación de datos**: Puede iniciar la extracción de datos de origen en cualquier momento a través de la API de acceso a datos sin penalizaciones ni retrasos en el tiempo. La variable [API de acceso a datos](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target=&quot;_blank&quot;} proporciona a los usuarios una interfaz RESTful centrada en la capacidad de detección y accesibilidad de conjuntos de datos ingestados dentro del Experience Platform. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Tenga en cuenta que el contenido utilizado en recorridos o campañas no se puede extraer mediante los métodos API o Destination mencionados anteriormente.

* **Retención de datos del servicio de perfil**: Para los datos de comportamiento y series temporales adjuntos a cualquier perfil, puede elegir utilizar la configuración predeterminada de Journey Optimizer de retener estos datos durante un máximo de 30 días desde la fecha de su adición a un perfil o hasta un período de tiempo alternativo seleccionado por el usuario. El tiempo que el Adobe mantiene estos datos varía según el contrato y se describe en la política de retención de datos de una organización.

   Obtenga más información sobre las caducidades de los eventos de experiencia en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target=&quot;_blank&quot;}.

* **Purgas y mecanismos de archivado**: La depuración de datos y archivos se puede definir y automatizar libremente en Journey Optimizer para automatizar las políticas de retención de datos. Es posible definir diferentes estrategias de envejecimiento para las diferentes entidades de datos. También se pueden definir mecanismos de exportación para exportar automáticamente los datos de antigüedad antes de depurarlos o archivarlos.

   El espacio de trabajo Higiene de los datos en la interfaz de usuario de Adobe Experience Platform le permite crear y supervisar diversas tareas de higiene de los datos, como la eliminación de identidades de consumidores y la programación de caducidades de conjuntos de datos. Este espacio de trabajo está disponible con el Escudo de seguridad y privacidad y con el Escudo de salud. Obtenga más información en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target=&quot;_blank&quot;}.

* **Lago de datos y eliminaciones**: Journey Optimizer puede conservar los datos del cliente almacenados en el Data Lake:

   * durante 7 días para facilitar la incorporación de los datos del cliente en los servicios de perfil, tras los cuales se pueden eliminar permanentemente, o
   * hasta que usted elija eliminarlo


* **Extracción de datos al finalizar o salir del compromiso**: Cuando finaliza el contrato, los datos se eliminan completamente del espacio de almacenamiento del Adobe. Además, puede extraer extractos de perfil completos antes de finalizar un acuerdo. Esta función no conlleva ningún coste adicional. Esto se puede hacer en cualquier momento y no sólo una vez terminada.

Los métodos anteriores se definen contractualmente y se exponen detalladamente en el acuerdo de procesamiento de datos (DPA) que el Adobe está de acuerdo entre sí al principio de una participación. Las aplicaciones de Adobe, incluido Journey Optimizer, se diseñan según el principio de que los datos de cada cliente se tratan como un recurso de datos propietario de ese cliente.
