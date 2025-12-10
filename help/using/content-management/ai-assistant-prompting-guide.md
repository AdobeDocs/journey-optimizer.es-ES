---
solution: Journey Optimizer
product: journey optimizer
title: Guía de solicitud de contenido del Ayudante AI
description: Aprenda a crear indicadores eficaces para la generación de contenido con tecnología de IA mediante el marco de trabajo CO-STAR para crear contenido de marketing de alta conversión y alineado con la marca.
topic: Artificial Intelligence
role: User
level: Intermediate
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '2107'
ht-degree: 1%

---

# Prácticas recomendadas rápidas del Asistente de IA {#ai-assistant-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_ai_assistant_prompt"
>title="Ejemplos de indicaciones"
>abstract="Explore la documentación de Journey Optimizer para aprender a crear indicadores eficaces que produzcan contenido de marketing de alta conversión y sin marca."

Esta guía le ayuda a estructurar sus solicitudes, comunicar la intención con claridad y asegurarse de que la IA produzca mensajes que se ajusten a las directrices de marca, las necesidades de audiencia y los objetivos de la campaña.
Aprenda a escribir indicadores eficaces que permitan al asistente de IA generar contenido de marketing de alta calidad y de marca adaptado a sus objetivos.

## Uso del marco CO-STAR {#costar-framework}

Para obtener los mejores resultados con el asistente de IA, organice las indicaciones mediante el marco de trabajo CO-STAR. Este enfoque estructurado garantiza que la IA entienda exactamente lo que necesita.

| Componente | Lo que significa | Por qué importa |
|-|-|-|
| **C - Contexto** | Antecedentes de su campaña, producto o situación | Ayuda a la IA a comprender el panorama general |
| **O - Objetivo** | Su objetivo de marketing específico | Controla lo que el contenido debe lograr |
| **S - Estilo** | Cómo desea comunicarse. | Establece el enfoque |
| **T - Tono** | Estilo emocional y voz | Da forma a cómo se siente el mensaje |
| **A - Audiencia** | Audiencia a la que está dirigiendo | Garantiza que el mensaje resuene con las personas adecuadas |
| **R - Requisitos** | Restricciones específicas o elementos imprescindibles | Define límites y elementos críticos |

## Preguntas frecuentes sobre AI Essentials {#key-takeaways}


### Lo que se hace y lo que no se hace


<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Hacer</th>
<th>No lo hagas</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>Utilice el marco CO-STAR para la estructura</p>
<p>Sea explícito sobre el contenido nuevo frente al existente</p>
<p>Centrar el uso del documento en directrices de extracción específicas</p>
<p>Utilice selecciones desplegables para el tono, la estrategia y la configuración regional</p>
<p>Hacer coincidir los objetivos de marketing con las capacidades de tipo de contenido</p>
<p>Generar varias variantes para las pruebas A/B</p>
</td>
<td>
<p>Solicite cambios estructurales, estilo o edición de imágenes en las solicitudes</p>
<p>Mencione el tono/la estrategia en las indicaciones si está disponible en los menús desplegables</p>
<p>Utilice objetivos vagos como "promocionar nuestro producto"</p>
<p>Solicitar selecciones de elementos condicionales</p>
<p>Esperar modificaciones de diseño mediante mensajes</p>
</td>
</tr>
</tbody>
</table>

### Contenido no admitido en las peticiones de datos

>[!TIP]
>
>Use el **editor de correo electrónico** o **Adobe Express** para realizar modificaciones visuales o de imagen.

Estas solicitudes no son compatibles y deben gestionarse mediante otras herramientas:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>✕ modificaciones de estructura de correo electrónico</th>
<th>✕ Cambios de estilo visuales</th>
<th>✕ operaciones de edición de imágenes</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Selección de secciones específicas para cambiar</li>
<li>Eliminación o clonación de elementos</li>
<li>Selecciones condicionales</li>
<li>Adición o eliminación de secciones de diseño</li>
</ul>
</td>
<td>
<ul>
<li>Formato de texto (negrita, cursiva, tamaño de fuente)</li>
<li>Modificaciones de color</li>
<li>Estilo del diseño (bordes, relleno, márgenes)</li>
<li>Efectos visuales (sombras)</li>
</ul>
</td>
<td>
<ul>
<li>Cambios de fondo</li>
<li>Adición de superposiciones de texto o logotipos</li>
<li>Recorte o cambio de tamaño de imágenes</li>
<li>Ajustes de color</li>
<li>Reemplazo de imagen</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Lista de comprobación de calidad {#quality-checklist}

Antes de generar contenido, asegúrese de lo siguiente:

&check; **Borrar objetivo**: Indica claramente la acción, el producto/servicio, el valor y el contexto.

&check; **Audiencia objetivo definida**: Especifica el segmento, la función o el segmento.

&check; **Alineación de tipo de contenido**: El objetivo coincide con el canal o formato seleccionado.

&check; **Selecciones desplegables configuradas**: se elige el tono, la estrategia y la configuración regional, no los incluya en el mensaje.

&check; **Enfoque del documento especificado**: resalta a qué contenido o secciones hacer referencia.

&check; **Marca aplicada**: se han seleccionado las directrices de marca adecuadas.

&check; **Ámbito realista**: evite solicitudes de cambios de diseño, estilo o ediciones estructurales.

## Escribir objetivos de marketing efectivos {#marketing-objectives}

### Ser específico y estar orientado a la acción

Al diseñar los objetivos de marketing, asegúrese de que sean claros, procesables y mensurables. Evite declaraciones vagas o genéricas.

**Ejemplos de buenos objetivos:**

&check; &quot;Regístrese para disfrutar de la versión de prueba gratuita de 30 días del nuevo panel de análisis con tecnología de IA&quot;

&check; &quot;Generación de posibles clientes para nuestro seminario web B2B sobre &quot;Reducción de los costes de nube en un 40 %&quot;, que se celebrará el 15 de marzo&quot;

&check; &quot;Promocione nuestro descuento de vacaciones del 25% por tiempo limitado en suscripciones premium hasta el 25 de diciembre&quot;

**Ejemplos que se deben evitar:**

✕ &quot;Promocionar nuestro producto&quot; (demasiado vago)

✕ &quot;Hacer que las personas compren cosas&quot; (valor poco claro)

✕ &quot;Enviar correo electrónico sobre nuevas características&quot; (carece de propósito)

### Estructurar el objetivo

Proporcione siempre el contexto y la propuesta de valor para que la IA pueda generar contenido relevante.
Use esta fórmula para escribir objetivos efectivos: **Acción + Producto/Servicio + Valor/Beneficio + Urgencia/Contexto**

**Ejemplos de buenos objetivos:**

&check; &quot;Fomente las descargas de nuestra nueva aplicación móvil que ayude a los usuarios a seguir hábitos de vida sostenibles con recomendaciones personalizadas y respetuosas con el medio ambiente&quot;

&check; &quot;Promocione el registro para nuestro taller exclusivo sobre técnicas avanzadas de visualización de datos para profesionales de marketing&quot;

&check; &quot;Impulse la asistencia a nuestro evento de lanzamiento del producto mostrando el revolucionario asistente de escritura de IA que ahorra más de 5 horas a la semana&quot;

**Ejemplos que se deben evitar:**

✕ &quot;Anunciar nueva aplicación&quot; (falta propuesta de valor y contexto)

✕ &quot;Hacer que las personas se inscriban en el taller&quot; (carece de especificidad acerca de la audiencia y el beneficio)

✕ &quot;Promocionar evento&quot; (sin acción, valor o urgencia claros)

## Creación de contenido nuevo frente a modificación de contenido existente {#new-vs-modify}

Indique claramente si su solicitud implica la generación de contenido nuevo o la actualización de material existente. Esta distinción es importante porque guía a la IA en la selección del enfoque adecuado y garantiza un resultado más preciso y útil.

### Creación de nuevo contenido

Aplique esta estrategia cuando inicie campañas de marketing, revele nuevos productos o inicie cualquier tipo de comunicación actualizada o actualizada. Garantiza que el mensaje comience con fuerza y se ajuste a sus objetivos.

**Cómo preguntar** ➤ Al crear contenido nuevo, céntrese en su objetivo de marketing sin hacer referencia al contenido existente.

>[!BEGINSHADEBOX]

**Ejemplos:**

* **Prueba de SaaS**: &quot;Lance nuestro nuevo software CRM a los propietarios de pequeñas empresas, destacando un ahorro de tiempo del 50%, una calificación de clientes potenciales 90% más rápida y una prueba gratuita de 30 días con incorporación personalizada&quot;
* **Anuncio de características**: &quot;Anuncie nuevas funciones de integración de API que reduzcan el tiempo de desarrollo en un 60 % para los clientes empresariales, dirigiéndose a los responsables técnicos de la toma de decisiones&quot;
* **Promoción de eventos**: &quot;Impulse los registros para nuestro seminario web sobre &#39;Tendencias de marketing digital 2024&#39; con expertos de Google, Meta y Adobe, haciendo hincapié en perspectivas procesables y puestos limitados (500 como máximo)&quot;

>[!ENDSHADEBOX]

### Modificación del contenido existente

>[!TIP]
>
>Para realizar modificaciones estándar como elaborar, resumir o simplificar, use la característica **Refinar** en lugar de escribir avisos personalizados. [Más información](generative-uc.md##refine)

Aplique esto cuando necesite actualizar, actualizar o adaptar sus campañas de marketing actuales. Este método admite mejoras incrementales, lo que garantiza que la mensajería siga siendo relevante sin comenzar desde cero.

**Cómo preguntar** ➤ Al modificar contenido existente, especifique claramente qué desea cambiar y cómo hacerlo.

>[!BEGINSHADEBOX]

**Ejemplos:**

* **Actualización de la campaña**: &quot;Modifique el correo electrónico de lanzamiento del producto para que se centre en las características de seguridad empresarial en lugar de en las ventajas generales de productividad, dirigiéndose a los responsables de la toma de decisiones de TI con certificaciones de cumplimiento&quot;.
* **Giro de audiencia**: &quot;Adapte nuestra invitación de demostración de software para dirigirse específicamente a la atención médica, reemplazando los ejemplos genéricos por casos de uso de atención médica y beneficios de cumplimiento de HIPAA&quot;
* **Actualización estacional**: &quot;Actualice nuestra campaña promocional del tercer trimestre para las compras de las vacaciones del cuarto trimestre, cambiando el enfoque de los regalos de vuelta al colegio a las vacaciones, con énfasis en los envíos rápidos&quot;

>[!ENDSHADEBOX]

## Mejore su mensaje con ajustes avanzados {#personalize-prompt}

### Tipos de estrategias de comunicación

>[!TIP]
>
>Utilice el menú desplegable Estrategia de comunicación del menú de configuración de texto en lugar de mencionarla en la solicitud de procesamiento especializado.

Su estrategia de comunicación determina cómo presentar el mensaje para maximizar el impacto. Las diferentes estrategias funcionan mejor para diferentes objetivos, ya sea que esté generando urgencia, estableciendo confianza o impulsando una acción inmediata. Elija la estrategia que mejor se ajuste a los objetivos de su campaña y a la mentalidad de su audiencia.

| **Estrategia** | **Mejor Para** | **Estilo de mensajería** | **Ejemplos** |
|--------------|--------------|------------------------|--------------|
| **Urgente** | Ofertas con distinción de tiempo, plazos, acción inmediata | Crea presión inmediata con lenguaje basado en el tiempo | &quot;Actuar ahora: la oferta caduca a medianoche&quot; <br> &quot;Regístrese hoy antes de que se llenen los puestos&quot; <br> &quot;La venta flash de 48 horas comienza ahora&quot; |
| **FOMO (Miedo a perderse)** | Ofertas limitadas, eventos, acceso exclusivo | Utiliza señales de urgencia, escasez y presión de tiempo | &quot;¡Solo quedan 24 horas! Existencias limitadas con un descuento del 40 %&quot; <br> &quot;Última oportunidad: el precio por anticipado finaliza mañana&quot; <br> &quot;Solo quedan 100 puntos beta&quot; |
| **Revisión social** | Confianza, testimonios, productos populares | Aprovecha las experiencias y la validación de otros | &quot;Únase a más de 50 000 clientes satisfechos&quot; <br> &quot;Clasificado con 4,9/5 estrellas por profesionales del sector&quot; <br> &quot;Confiado por compañías de Fortune 500&quot; |
| **Escasez** | Inventario limitado, versiones exclusivas, artículos de alta demanda | Destaca la disponibilidad y exclusividad limitadas | &quot;Solo quedan 5 en stock&quot; <br> &quot;Edición limitada: 100 unidades disponibles&quot; <br> &quot;Versión exclusiva: primero en llegar, primero en llegar&quot; |
| **Incentivo** | Promociones, programas de recompensas, ofertas especiales | Destaca beneficios tangibles y recompensas | &quot;Obtenga un 20% de descuento en su primer pedido&quot; <br> &quot;Gane puntos dobles este fin de semana&quot; <br> &quot;Envío gratuito en pedidos superiores a $50&quot; |
| **Exclusividad** | Productos Premium, experiencias de VIP, ofertas solo para miembros | Utiliza un idioma de posicionamiento premium y acceso especial | &quot;Invitación exclusiva a nuestra vista previa privada&quot; <br> &quot;La suscripción Elite desbloquea los análisis avanzados&quot; <br> &quot;Únase a determinadas empresas de la lista Fortune 500 que ya nos utilizan&quot; |
| **Gamification** | Campañas de participación, programas de fidelización y contenido interactivo | Utiliza la mecánica de juegos y el lenguaje de logros | &quot;Desbloquea tu siguiente nivel de recompensa&quot; <br> &quot;Completa los desafíos para ganar insignias&quot; <br> &quot;Sube a la tabla de clasificación para obtener premios exclusivos&quot; |
| **Informativo** | Educación, investigación, productos complejos, liderazgo mental | Utiliza hechos, datos, perspectivas y explicaciones | &quot;5 datos del análisis de más de 10 000 interacciones&quot; <br> &quot;Una nueva investigación revela 3 enfoques innovadores&quot; <br> &quot;Guía completa para implementar la IA en el marketing&quot; |
| **Educación e información** | Contenido de aprendizaje, tendencias del sector, prácticas recomendadas | Proporciona conocimientos valiosos y procedimientos útiles | &quot;Domine las técnicas avanzadas con nuestra guía de expertos&quot; <br> &quot;Descubra 7 estrategias que utilizan los mejores especialistas en marketing&quot; <br> &quot;Aprenda a optimizar su flujo de trabajo en 5 pasos&quot; |

### Establecer el tono correcto {#tone}

>[!TIP]
>
>Utilice el menú desplegable Tono del menú Configuración de texto en lugar de especificarlo en el mensaje.

El tono define cómo la audiencia percibe y responde al mensaje. Seleccione siempre un tono que se ajuste a la voz de su marca y al escenario del recorrido del perfil.

Utilice la tabla siguiente para explorar cada tono en detalle, incluso cuando funcione mejor y ejemplos de contenido que se ajusten a cada estilo.

| Tonalidad | Mejor para | Ejemplo de contenido |
|-|-|-|
| Profesional | Comunicaciones B2B, anuncios formales | &quot;Nos complace anunciar nuestra asociación estratégica...&quot; |
| Empático | Asistencia al cliente, temas confidenciales | &quot;Entendemos lo frustrante que esto debe ser para ti...&quot; |
| Divertido | Campañas atractivas, contenido desenfadado | &quot;Advertencia: ¡Puede causar importantes mejoras en la productividad!&quot; |
| Emocionante | Lanzamientos de productos, promociones de eventos | &quot;¡Este es el momento que has estado esperando!&quot; |
| Inspirador | Campañas de motivación, objetivo de marca | &quot;Juntos, podemos hacer una diferencia en el mundo...&quot; |
| Persuasivo | Campañas de ventas, conversiones | &quot;No pierdas esta oportunidad de tiempo limitado para...&quot; |
| Amistoso | Participación del cliente, mensajes de bienvenida | &quot;¡Nos alegra tanto que estés aquí con nosotros!&quot; |
| Formal | Comunicaciones legales, avisos oficiales | &quot;Por la presente le notificamos los siguientes cambios...&quot; |
| Apologético | Recuperación del servicio, resolución de problemas | &quot;Pedimos disculpas sinceramente por cualquier inconveniente causado...&quot; |
| Asertivo | Contenido de liderazgo, mensajería autorizada | &quot;Esto es lo que tienes que hacer ahora mismo...&quot; |
| Narración | Narrativas de marca, conexiones emocionales | &quot;Todo comenzó con una simple pregunta...&quot; |
| Conversatorio | Nutrir campañas, construir relaciones | &quot;Hablemos de cómo esto puede ayudarte...&quot; |

### Optimizar los recursos de su marca {#brand-assets}

>[!TIP]
>
>Si ya ha cargado un recurso de marca a través del menú **Brand Assets**, no es necesario que haga referencia a él en el mensaje. El sistema utiliza automáticamente los documentos seleccionados.

Los recursos de marca proporcionan información objetiva que enriquece el contenido generado con detalles específicos y precisos.
Cuando cargue documentos generales, como folletos de productos, añada al mensaje en qué partes centrarse:

* **En lugar de** _&quot;Use el folleto del producto&quot;_ **debería usar** _&quot;Céntrese en las características de seguridad avanzadas y las certificaciones de cumplimiento, específicamente en el cumplimiento de SOC 2 y el cifrado de datos&quot;_

* **En lugar de** _&quot;Consulte los estudios de caso&quot;_ **debería usar** _&quot;Resaltar los resultados de retorno de la inversión de los clientes del sector sanitario, específicamente la reducción de costos del 40% en el Centro Médico Regional&quot;_

* **En lugar de** _&quot;Incluir detalles técnicos&quot;_ **debe usar** _&quot;Enfatizar las capacidades de integración de API y los beneficios para desarrolladores, centrándose en los extremos de API de REST y en el tiempo de actividad del 99,9 % de SLA&quot;_

### Refinamiento de contenido

>[!TIP]
>
>Utilice la función Refinar en lugar de preguntar cuando desee elaborar, resumir, simplificar, cambiar el tono o traducir el contenido existente. [Más información](generative-uc.md#refine)

Una vez generado el contenido, use la característica **Refine** para iterarlo y mejorarlo con las siguientes opciones:

| **Acción** | **Caso de uso** | **Ejemplo de mensaje** |
|-|-|-|
| **Elaborar** | Añadir profundidad y detalle al contenido breve | &quot;Conozca los beneficios técnicos de nuestras funciones de seguridad&quot; |
| **Resumir** | Comprimir contenido largo para diferentes formatos | &quot;Resumir esta descripción general del producto para una publicación en medios sociales&quot; |
| **Simplificar** | Hacer que el contenido complejo sea más accesible | &quot;Simplificar esta explicación técnica para una audiencia general&quot; |
| **Cambiar tono** | Adaptación de contenido para diferentes audiencias | &quot;Cambia el tono a más informal para los más jóvenes&quot; |
| **Transcrear** | Adaptación cultural más allá de la traducción | &quot;Transcree esta campaña para el mercado japonés&quot; |

## Ejemplos de mensajes basados en escenarios

### Según el tipo de contenido {#content-type-practices}

<table style="table-layout: fixed; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Canal</th>
<th>Ejemplo</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Correo electrónico</strong></td>
<td>"Fomente las perspectivas empresariales mostrando tres casos de éxito de clientes con métricas detalladas de ROI (IBM: reducción de costes del 45 %, Accenture: aumento del 200 % del posible cliente, Microsoft: ahorro de tiempo del 60 %), dirigiéndose a directores de TI de empresas con más de 1000 empleados".</td>
</tr>
<tr>
<td><strong>SMS</strong></td>
<td>"Alerta a los clientes de VIP sobre la venta flash de 4 horas en productos electrónicos premium con un 40% de descuento, limitado a los primeros 100 clientes"</td>
</tr>
<tr>
<td><strong>Notificaciones push</strong></td>
<td>"Vuelva a atraer a los usuarios que no hayan abierto la aplicación en siete días con recomendaciones de contenido personalizadas basadas en su historial de lectura"</td>
</tr>
<tr>
<td><strong>Páginas de destino</strong></td>
<td>"Convierta a los visitantes B2B en posibles clientes cualificados demostrando cómo nuestra solución de seguridad empresarial evita el 99,9 % de los ataques cibernéticos, con testimonios de Fortune 500 y auditorías de seguridad gratuitas".</td>
</tr>
</tbody>
</table>

### Basado en enfoques específicos del sector {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industria</th>
<th>Mensaje de ejemplo</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Tecnología B2B</strong></td>
<td>"Demuestre el retorno de la inversión y las especificaciones técnicas mientras aborda las preocupaciones de seguridad para los responsables de las decisiones de TI que evalúan nuestra solución de infraestructura en la nube, haciendo hincapié en el 99,9% del tiempo de actividad de SLA, el cumplimiento de SOC 2 y el ahorro de costes del 40%".</td>
</tr>
<tr>
<td><strong>Comercio electrónico minorista</strong></td>
<td>"Cree la urgencia en torno a los artículos de vacaciones de existencias limitadas, al tiempo que destaca el envío gratuito y las devoluciones sencillas para los compradores de último minuto, haciendo hincapié en las cantidades limitadas (quedan menos de 50) y el límite de envío de 24 horas".</td>
</tr>
<tr>
<td><strong>Servicios financieros</strong></td>
<td>"Educar a los clientes sobre las estrategias de diversificación de la cartera de inversiones manteniendo al mismo tiempo el cumplimiento normativo, con información certificada de los asesores financieros y exenciones de responsabilidad de riesgos".</td>
</tr>
<tr>
<td><strong>Salud y bienestar</strong></td>
<td>"Promocione beneficios de atención preventiva y exámenes de salud anuales a la vez que mantiene la precisión médica, con recomendaciones médicas certificadas por la junta y garantías de privacidad del paciente".</td>
</tr>
<tr>
<td><strong>Educación y formación</strong></td>
<td>"Enfatice los resultados de avance profesional y las certificaciones de la industria mientras muestra la experiencia de los instructores, destacando la tasa de colocación laboral del 92% y el currículo basado en proyectos".</td>
</tr>
<tr>
<td><strong>Plataformas SaaS</strong></td>
<td>"Resalte los ahorros de tiempo y las ventajas de la automatización con métricas específicas, al tiempo que aborda los problemas de integración, con un ahorro de tiempo promedio semanal de 25 horas y la integración con más de 200 herramientas populares".</td>
</tr>
</tbody>
</table>
