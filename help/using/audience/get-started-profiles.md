---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los perfiles en Journey Optimizer
description: Obtenga información sobre cómo crear y administrar perfiles en Adobe Journey Optimizer
feature: Profiles
role: User
level: Beginner
exl-id: be3936e4-8185-4031-9daf-95eea58077d0
TQID: https://experienceleague.adobe.com/QpLGV-y5qbtmksC-99GU5PtaV-mUA-imew8JDj7-weA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3id: b32bb433-f8c6-4931-8e52-e657230a3bf2id: e95b6013-acbe-46e9-a3b5-b80e14088d7did: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 537
ht-degree: 35%

---

# Introducción a los perfiles {#profiles-gs}

## Acerca de los perfiles

Aproveche el Perfil del cliente en tiempo real en [!DNL Adobe Journey Optimizer] para ver una vista holística de cada cliente individual combinando datos de varios canales, incluidos los canales en línea, sin conexión, CRM y de terceros. **Perfiles** le permite consolidar los datos de sus clientes en una vista unificada que ofrece una cuenta procesable con marca de tiempo de cada interacción del cliente.

➡️ [Descubra esta funcionalidad en vídeo](#video)

**Perfil del cliente en tiempo real&#x200B;**: integre atributos y eventos del cliente desde fuentes en línea, sin conexión y con seudónimo en un único perfil unificado. &#x200B;Utilice el perfil para atraer clientes con experiencias personalizadas en tiempo real en varios puntos de contacto. &#x200B;

**Ingesta de datos**: conéctese a varias fuentes de datos para ingerir datos de comportamiento, transaccionales, financieros y operativos. Introduzca datos en tiempo real o mediante cargas por lotes para mantener los perfiles actualizados constantemente. Los perfiles no se crean directamente en la interfaz de [!DNL Journey Optimizer], sino que se crean o actualizan automáticamente en Adobe Experience Platform cuando se incorporan los datos.

>[!NOTE]
>
>Al introducir datos, los correos electrónicos distinguen entre mayúsculas y minúsculas. Significa que se pueden crear perfiles duplicados (por ejemplo, un perfil para Juan.Greene@luma.com y otro perfil para juan.greene@luma.com) y utilizarse al segmentar el destinatario correspondiente en sus recorridos y campañas de [!DNL Journey Optimizer].

**Gráfico de identidad**: Combine datos de diferentes fuentes usando identidades de clientes, como ID de fidelidad o ID del sistema CRM. &#x200B;Cree una vista completa del cliente asignando relaciones entre distintas identidades dentro de los conjuntos de datos de una marca. &#x200B;

**Participación del cliente**: utilice el perfil del cliente en tiempo real para ofrecer experiencias contextuales y personalizadas, como ofertas y mensajes segmentados. &#x200B;Capte a los clientes en varios canales, incluidas las campañas de marketing, la asistencia al cliente y las actualizaciones transaccionales. &#x200B;

**Uso compartido de datos**: comparte perfiles de clientes con los principales proveedores de almacenamiento en la nube, como Amazon Web Service, Microsoft Azure y Google Cloud. Utilice perfiles compartidos para la creación de informes, el archivado de datos o un análisis más profundo con herramientas de inteligencia empresarial.

>[!MORELIKETHIS]
>
>* [Introducción a la gestión de datos en Journey Optimizer](../data/gs-data.md)
>* [Documentación del perfil del cliente en tiempo real](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=es){target="_blank"}
>* [Protecciones predeterminadas para la segmentación y los datos del perfil del cliente en tiempo real](https://experienceleague.adobe.com/es/docs/experience-platform/profile/guardrails){target="_blank"}
>* [Documentación de ingesta de datos](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home){target="_blank"}

## Panel de perfiles

Para acceder a los perfiles, vaya al menú **[!UICONTROL Cliente]** / **[!UICONTROL Perfiles]** en el panel de navegación izquierdo.

>[!NOTE]
>
>Si su organización es nueva en [!DNL Adobe Journey Optimizer] y aún no tiene conjuntos de datos de perfil activos o políticas de combinación creadas, el panel de control **Perfiles** no está visible. En su lugar, la pestaña **Información general** muestra vínculos a documentación de Adobe Experience Platform para ayudarle a empezar con el Perfil del cliente en tiempo real. Para aprender a trabajar con el **tablero de perfiles** y obtener información detallada sobre las métricas mostradas en el tablero, consulte [esta sección](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es){target="_blank"}.

Puede unir fragmentos de datos de varias fuentes y combinarlos para ver una vista completa de cada uno de sus clientes individuales. Al unir estos datos, las políticas de combinación son las reglas utilizadas para determinar cómo se priorizan los datos y qué datos se combinan para crear la vista unificada. Obtenga más información acerca de **políticas de combinación** en esta [documentación](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=es){target="_blank"}.

![](assets/profiles-home.png)

## Vídeo práctico {#video}

Descubra cómo Adobe Experience Platform organiza y actualiza los perfiles de clientes en tiempo real, y cómo puede acceder a ellos y utilizarlos.

>[!VIDEO](https://video.tv.adobe.com/v/27251?quality=12)
