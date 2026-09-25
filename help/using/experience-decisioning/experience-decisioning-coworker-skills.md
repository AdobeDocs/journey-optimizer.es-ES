---
solution: Journey Optimizer
product: journey optimizer
title: Compañero de trabajo para decisiones
description: Descubra las aptitudes de CX Enterprise Coworker disponibles para la toma de decisiones en Adobe Journey Optimizer, incluidas las aptitudes de Explicador de decisiones y Reglas y clasificación, con instrucciones detalladas e instrucciones de ejemplo.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 8ac4ba8290929e31cd9f7494b63362bc2613d68c
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 1%
---

# Compañero de trabajo para decisiones {#experience-decisioning-coworker-skills}

>[!BEGINSHADEBOX]

**En esta página:** Descubra las habilidades de CX Enterprise Coworker disponibles para la toma de decisiones en Adobe Journey Optimizer, comprender por qué se mostró o no una oferta en un perfil o segmento, y crear, explicar, simular y optimizar reglas de elegibilidad y fórmulas de clasificación, con instrucciones detalladas, instrucciones de ejemplo y prácticas recomendadas.

Más información:

* [Aptitudes de colaborador para Journey Optimizer](../start/ai-features.md#cx-coworker-skills): información general sobre las aptitudes de colaborador en todos los Recorridos, lealtad, administración de contenido y toma de decisiones en Journey Optimizer.
* [Documentación de los compañeros](https://experienceleague.adobe.co/es/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"}: información general sobre las capacidades de Campañas, Conversaciones y Proyectos de los compañeros.
* [Guía de la interfaz de usuario de Coworker Chat](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"}: cómo acceder y navegar por Coworker Chat.

>[!ENDSHADEBOX]

## Explicador de decisión {#decisioning-explainer}

>[!AVAILABILITY]
>
>El explicador de decisiones está disponible para todos los clientes que tienen acceso a Colaborador y toma de decisiones.

Decisioning Explainer responde, en lenguaje natural, por qué se mostró o no una oferta específica en un perfil determinado o, más ampliamente, por qué un segmento de perfiles no ve una oferta. Recorre la pila completa de toma de decisiones para el perfil (o segmento) solicitado y la ventana de tiempo: qué ofertas eran elegibles, qué regla de elegibilidad incluyó o excluyó cada una, si la restricción de frecuencia o fatiga suprimió la oferta, las puntuaciones de clasificación finales y con qué estrategia o modelo de IA se produjeron, y con qué grupo de candidatos (recopilación de elementos) se evaluó el perfil.

Esto responde a un desafío común de los especialistas en marketing: explicar por qué una oferta se clasifica por encima de otra o por qué una decisión de oferta específica se produjo de la manera que lo hizo. El Explicador de decisiones es de sólo lectura: explica las decisiones, pero no modifica las reglas, las fórmulas de clasificación ni las estrategias de selección.

### Casos de uso clave

* **Por qué se mostró o no una oferta específica**

  Ejemplos de mensajes:
  * &quot;¿Por qué el perfil 12345 ver la Oferta X el 15 de mayo?&quot;
  * &quot;¿El perfil X no reunía los requisitos para esta oferta?&quot;
  * &quot;¿Qué regla de idoneidad excluyó a este cliente?&quot;
  * &quot;Muéstrame para qué ofertas era apto el perfil X el 3 de junio&quot;.

* **Por qué la visibilidad de una oferta cambió con el tiempo**

  Ejemplos de mensajes:
  * &quot;¿Por qué ha dejado de mostrarse la oferta Y a los clientes que regresan en los últimos 7 días?&quot;
  * &quot;¿Cuántas veces ha visto este cliente esta oferta?&quot;
  * &quot;¿Esta oferta estaba limitada al perfil X?&quot;
  * &quot;¿Qué ofertas se están suprimiendo actualmente para el perfil X debido a las restricciones de límite?&quot;

* **Cómo se clasificó o seleccionó una oferta**

  Ejemplos de mensajes:
  * &quot;Explicarme exactamente cómo se seleccionó la oferta Z sobre las demás ofertas aptas para este perfil&quot;.
  * &quot;¿Cuál fue la puntuación de clasificación para cada oferta en esta decisión?&quot;
  * &quot;¿Por qué la oferta A estaba por encima de la oferta B para este perfil?&quot;
  * &quot;¿Qué factores influyeron más en el resultado de la clasificación?&quot;

* **Explicaciones de nivel de segmento**

  Decisioning Explainer puede acumular esta lógica en un segmento en lugar de en un solo perfil, y mostrar la razón principal por la que un grupo de perfiles no ve una oferta.

  Ejemplos de mensajes:
  * &quot;Para los clientes de esta audiencia, ¿cuál es la razón más común por la que se les excluye?&quot;
  * &quot;¿Qué ofertas recibe realmente este segmento?&quot;
  * &quot;¿Por qué no ve esta oferta mi segmento de fidelidad?&quot;

### Impulso de las prácticas recomendadas

* **ID de referencia conocidos**: proporcione el ID de perfil, el nombre de oferta o el nombre del segmento para obtener un seguimiento preciso en lugar de una respuesta general.
* **Incluir una ventana de tiempo**: especifique una fecha o un intervalo de fecha al preguntar por qué ha cambiado la visibilidad de una oferta, de modo que el Compañero pueda analizar el seguimiento correctamente.
* **Pedir el desglose de clasificación directamente**: Si desea obtener detalles de puntuación, pida explícitamente la puntuación de clasificación o los factores que influyeron en el resultado.
* **Utilice preguntas de nivel de segmento para las tendencias**: Cuando investigue por qué un grupo de perfiles no está viendo una oferta, pregunte por el segmento en lugar de por un solo perfil para obtener el motivo dominante.

## Reglas y clasificación {#rules-ranking}

>[!AVAILABILITY]
>
>Rules &amp; Ranking está disponible para todos los clientes que tienen acceso a Coworker y Decisioning.

Reglas y clasificación proporciona a los especialistas en marketing asistencia basada en IA para crear, comprender y probar la lógica de toma de decisiones, sin necesidad de escribir o validar manualmente la sintaxis de PQL. Abarca cuatro funciones principales: creación de reglas en lenguaje natural, regla en inglés sencillo y explicación de la fórmula de clasificación, simulación con hasta 3 perfiles de prueba y optimización de PQL. Tiene ámbitos de reglas de idoneidad y fórmulas de clasificación; no crea ni edita estrategias de selección ni políticas de decisión.

### Casos de uso clave

* **Creación de reglas en lenguaje natural**

  Convierta una descripción en lenguaje sencillo en sintaxis de regla de aceptación de PQL, tanto para reglas nuevas como para ediciones en reglas existentes.

  Ejemplos de mensajes:
  * &quot;¿Se puede crear una regla de idoneidad dirigida a los usuarios que cumplen las condiciones XYZ?&quot;
  * &quot;Cree una regla de elegibilidad dirigida a los miembros socio de nivel 2 o superior.&quot;
  * &quot;Escriba una regla de PQL que excluya a los clientes que hayan realizado una compra en los últimos 7 días&quot;.
  * &quot;Modifique esta regla para excluir también a los clientes de la lista de supresión.&quot;

* **Explicación de fórmula y regla en inglés sin formato**

  Explique lo que hace una regla de idoneidad o una fórmula de clasificación existente (qué incluye o excluye, y qué significa cada condición) sin necesidad de leer la sintaxis de PQL.

  Ejemplos de mensajes:
  * &quot;¿Puedes explicarme esta regla en lenguaje natural?&quot;
  * &quot;¿Qué hace realmente esta fórmula de clasificación?&quot;
  * &quot;¿A quién se dirige esta regla de elegibilidad y a quién excluye?&quot;
  * &quot;Resumir esta regla en una frase.&quot;
  * &quot;¿Por qué la oferta A está por encima de la oferta B para este cliente?&quot;
  * &quot;¿Es esta regla demasiado restrictiva para una amplia campaña de sensibilización?&quot;
  * &quot;¿Qué condición de esta regla es filtrar la mayoría de los perfiles?&quot;

* **Simulación**

  Ejecute una regla de aceptación o fórmula de clasificación con hasta 3 perfiles de prueba (introducidos manualmente o generados por IA, incluidos los casos extremos) y obtenga resultados de aprobación o error con la condición de error específica, o una lista clasificada de ofertas con puntuaciones numéricas.

  Ejemplos de mensajes:
  * &quot;Simular esta regla con perfiles de prueba&quot;.
  * &quot;¿Pasa esta regla para un perfil donde loyalty_tier = gold?&quot;
  * &quot;¿Qué perfiles aprueban esta regla de idoneidad: [perfil A, perfil B, perfil C]?&quot;
  * &quot;¿Por qué este perfil no superó la comprobación de idoneidad?&quot;
  * &quot;Generar perfiles de prueba para esta regla de idoneidad&quot;.
  * &quot;Genere perfiles de casos extremos que pongan a prueba esta condición&quot;.
  * &quot;Simule esta fórmula de clasificación en estas ofertas y perfiles.&quot;
  * &quot;¿Qué oferta tendría la clasificación más alta para este perfil dada esta fórmula?&quot;
  * &quot;Compare cómo se comporta esta regla de elegibilidad para un cliente de nivel oro frente a plata frente a básico&quot;.

* **Optimización de PQL**

  Vuelva a escribir una regla o fórmula existente con una sintaxis más concisa para cumplir los límites de tamaño de PQL de Journey Optimizer, sin cambiar su lógica ni su resultado.

  Ejemplos de mensajes:
  * &quot;Optimizar esta regla de PQL para mí&quot;.
  * &quot;Esta regla está alcanzando los límites de tamaño de PQL, ¿puede abreviarla?&quot;

### Impulso de las prácticas recomendadas

* **Proporcione la condición de destino explícitamente**: Al crear o modificar una regla, indique la audiencia, el atributo o la condición de exclusión exactos que desee.
* **Hacer referencia a la regla o fórmula directamente**: Al solicitar una explicación, simulación u optimización, asegúrese de que la regla o fórmula que desea decir esté abierta o claramente identificada.
* **Pida casos extremos**: al simular, pídale a su compañero que genere perfiles de casos extremos para probar una condición con estrés, no solo las típicas.
* **Revisar antes de publicar**: Compruebe la lógica y los resultados de simulación de una regla generada u optimizada antes de publicarla.

{{$include /help/_includes/do-not-localize/start/ai-augmented-experience-decisioning-coworker-skills.md}}
