---
source-git-commit: 341538e14ef7de012cce89561727bdecb44d8183
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 0%

---
# augmentedAIContent

Genera un acordeón **AI Knowledge Reference** creado automáticamente para una o más páginas de marcado en el repositorio de documentación de Journey Optimizer y lo almacena como **inclusión no localizada** para que no se traduzca.

## Repositorio de destino

`help/using/` (relativo a la raíz del repositorio)

## Sintaxis de acordeón (Experience League)

```
+++ AI Knowledge Reference

Content here — any standard markdown is valid.

+++
```

**Reglas:**

- `+++ AI Knowledge Reference` abre el acordeón (un espacio después de `+++`); `+++` solo en una línea lo cierra
- Línea en blanco antes de `+++` y después de `+++`
- El título siempre es exactamente `AI Knowledge Reference`

## Incluir sintaxis (Experience League)

```
{{$include /help/_includes/do-not-localize/<folder>/<include-file>.md}}
```

El contenido extraído a través de `{{$include}}` desde `help/_includes/do-not-localize/` se ha **excluido de la localización**; así es como el bloque permanece sin traducir.

&#x200B;---

## Flujo de trabajo

### Paso 1: Preguntar por los destinatarios

Pregunte al usuario:
> ¿Qué archivo o carpeta desea enriquecer?
> - Archivo único: ruta relativa a la raíz del repositorio (p. ej. `help/using/email/get-started-email.md`)
> - Carpeta: todos los `.md` archivos de forma recursiva (por ejemplo: `help/using/email`)
> - Lista de archivos/carpetas

Si se proporciona una carpeta, enumere los `.md` archivos encontrados y confirme antes de procesar.

### Paso 2: Para cada fichero: leer y generar

1. **Lea el archivo** por completo.
2. **Comprenda el tema de la página**: ¿qué característica, concepto o tarea cubre?
3. **Genere el contenido del bloque** usando las reglas de generación de contenido siguientes.
4. **Ejecute la lista de comprobación de validación posterior a la generación** (ver a continuación); no la omita.
5. **Compruebe** si ya existe un bloque de referencia de conocimiento de IA, ya sea en línea (`+++ AI Knowledge Reference` cerca del final) o ya externalizado (una línea `{{$include /help/_includes/do-not-localize/.../ai-augmented-...}}`). En caso afirmativo, pregunte al usuario: ¿reemplazar o omitir? Al reemplazar, sobrescriba el archivo de inclusión (y si el bloque seguía dentro de la línea, elimine el bloque dentro de la línea y añada la línea de inclusión en su lugar).

### Paso 3: Verificar todas las reclamaciones contra el cuerpo de la página

Antes de escribir el bloque, vuelva a leer la notificación de contenido generado por notificación. Este paso es **obligatorio y no se puede omitir**, ni siquiera en el caso de archivos cortos. Corrija cualquier error antes de continuar con el paso 4.

**Terminología y etiquetas**

- [ ] Cada término, etiqueta y nombre de interfaz de usuario del bloque aparece en el cuerpo de la página, no importado de otra página ni deducido del conocimiento general del producto
- [ ] No aparece ningún sinónimo a menos que ambos formularios aparezcan en la página
- [ ] Cada entrada &quot;No confundir&quot; hace referencia únicamente a los conceptos mencionados en esta página

**Protecciones y límites**

- [ ] Cada valor numérico coincide exactamente con el cuerpo de la página
- [ ] Se llama a un límite **hard** solo si el cuerpo de la página usa esa palabra o implica claramente que el sistema la aplica (por ejemplo, &quot;no puede exceder&quot;, &quot;máximo ... permitido&quot;, &quot;solo ... admitido&quot;)
- [ ] Se llama a un límite **recomendado** solo si el cuerpo de la página usa esa palabra o un equivalente (&quot;para obtener el mejor rendimiento&quot;, &quot;se recomienda&quot;)
- [ ] Si el cuerpo de la página no da ningún calificador, el bloque no da ninguno; no invente uno
- [ ] No hay ningún metacomentario sobre lo que dice o no la página de origen (por ejemplo, &quot;no se indica un número específico en esta página&quot;)

**Definiciones de glosario**

- [ ]: ninguna definición contiene detalles técnicos ausentes del cuerpo de la página
- [ ] Ninguna entrada elabora con información de otras páginas del conjunto de documentación

**respuestas a preguntas frecuentes**

- [ ] Cada detalle específico (asequibilidad de interfaz de usuario, nombres de botones, nombres de campos, secuencias de pasos) se indica en el cuerpo de la página, no se infiere ni se importa desde otras páginas
- [ ] Ninguna respuesta presenta información que el cuerpo de la página no aborda

**Regla de corrección:** Si falla alguna comprobación, corrija el contenido **antes de** que escriba el bloque. Registre todas las correcciones en el informe del paso 5.

&#x200B;---

### Paso 4: Escriba el bloque en una inclusión no localizada y luego inclúyalo

El bloque generado debe **no estar localizado**, por lo que no se escribe en línea en la página. En su lugar, se encuentra en un archivo de inclusión independiente bajo `help/_includes/do-not-localize/`, que se excluye de la traducción, y la página lo extrae con `{{$include}}`. (Esta es la convención DOCAC-15581).

**a. Derive el nombre de archivo de inclusión** de la ruta de acceso de la página en relación con su carpeta de sección de nivel superior en `help/using/`: elimine la extensión `.md`, reemplace los `/` restantes por `-` y agregue el prefijo `ai-augmented-`. Este acoplamiento mantiene el directorio de inclusión plano libre de colisiones.

Ejemplos (sección `building-journeys`):

| Página | Incluir archivo |
|---|---|
| `help/using/building-journeys/end-journey.md` | `ai-augmented-end-journey.md` |
| `help/using/building-journeys/expression/journey-properties.md` | `ai-augmented-expression-journey-properties.md` |

**b. Escriba el archivo de inclusión** en `help/_includes/do-not-localize/<section-folder>/<include-file>` (cree el subdirectorio `<section-folder>` si no existe; una subcarpeta por sección de AJO de nivel superior, p. ej. `building-journeys/`, `email/`). Use exactamente esta estructura: `title` frontmatter, un encabezado de `# AI Knowledge Reference`, el acordeón completo de **Full template** más abajo y, a continuación, el comentario de sincronización:

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

[complete "+++ AI Knowledge Reference" accordion from the Full template below]

<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of the including page's body, excluding the {{$include}} line] -->
```

**c. Agregue la llamada de inclusión** como la última línea de la página, precedida de una línea en blanco. No modifique ningún otro contenido de la página:

```
{{$include /help/_includes/do-not-localize/<section-folder>/<include-file>}}
```

El comentario de sincronización aún permite la detección de deriva: el hash de origen se calcula sobre el cuerpo de la página incluida, de modo que los futuros escritores y herramientas pueden saber cuándo la página se ha alejado del bloque. Dos archivos cambian por página: el **archivo de inclusión** (creado) y la **página** (se agregó una línea de `{{$include}}`).

### Paso 5: Informe

- Archivos modificados ✓ (incluir archivo creado + línea `{{$include}}` de la página)
- Archivos omitidos + motivo (ya tiene bloque / vacío / página de índice)
- Cualquier advertencia de validación generada durante el paso 2

&#x200B;---

## Reglas de generación de contenido

Analice la página y produzca las secciones debajo de **en orden** dentro del acordeón. Omita una sección por completo si no se puede extraer contenido significativo para ella.

### Apertura fija: textual, no modificar

Cada acordeón de Referencia de conocimiento de IA debe comenzar con este bloque exacto. Cópielo tal cual; no parafrasee, condense ni reordene:

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

Las secciones específicas de página a continuación siguen inmediatamente después de estos dos párrafos, dentro del mismo acordeón. (Todo el acordeón se escribe en el archivo de inclusión do-not-localize, por Paso 4, no alineado en la página).

### 1. TL;DR

Una frase: ¿qué enseña o habilita esta página?

```
* **TL;DR:** [one sentence]
```

### &#x200B;2. Intenciones

De 3 a 6 cosas que un usuario puede hacer después de leer esta página.

```
**Intents:**

* [action]
* [action]
```

### &#x200B;3. Glosario

Términos clave específicos de esta página o función con definiciones cortas. Marcar términos específicos de productos.

```
**Glossary:**

* **[Term]**: [definition] *(product-specific)*
```

Incluya solo términos relevantes para esta página. No rellene con términos de marketing genéricos.

**Regla de precisión del modo de validación — obligatorio:**
Si la página cubre cualquier forma de prueba, previsualización o ejecución simulada, DEBE distinguir entre todos los modos que describe realmente la página. No contraiga los distintos modos en una sola entrada abreviada:
- **Simulación**: procesa el contenido del mensaje sin enviarlo; utiliza perfiles reales
- **Modo de prueba**: envía solo a perfiles de prueba designados; utiliza perfiles de prueba AEP persistentes (no perfiles sintéticos o falsos)
- **Ejecución en seco**: ejecuta la lógica de recorrido completa sin activar acciones; utiliza datos de audiencia reales

Incluya solo los modos presentes en la página. Copie el término preciso del producto desde el cuerpo de la página: no sustituya &quot;perfiles sintéticos&quot;, &quot;datos falsos&quot; ni &quot;sin datos reales&quot; por ninguno de estos términos.

### &#x200B;4. Mecanismos de protección

Limitaciones, requisitos previos, permisos o restricciones mencionadas en la página.

```
**Guardrails:**

* [guardrail]
```

**Reglas de precisión de protección — obligatorio:**

- **Califica cada límite numérico** como recomendado o difícil. Ejemplo: &quot;Máximo 10 búsquedas de conjuntos de datos por mensaje (límite estricto)&quot;, no &quot;Máximo 10 búsquedas de conjuntos de datos&quot;.
- **Califique cada cifra de rendimiento o tasa** con su ámbito. Ejemplo: &quot;Límite de TPS de 150 000 mensajes/hora (por zona protegida)&quot;, no &quot;Límite de TPS de 150 000 mensajes/hora&quot;.
- **Compruebe todas las protecciones del cuerpo de la página** antes de incluirla. Si la página dice 10 y el bloque diría 5, el bloque es incorrecto. El cuerpo de la página es autoritativo.
- **No deduzca protecciones** que no se indiquen en la página. Si existe una restricción pero la página no la indica, omítala.

### &#x200B;5. Terminología

Nombres canónicos, siglas, variantes aceptadas, sinónimos, desambiguación. Principalmente para la normalización de canalización de IA.

```
**Terminology:**

* Canonical name: [name] — Acronym: [acronym] — variants: [list]
* Synonyms: "[term A]" = "[term B]"
* Do not confuse: "[term]" ≠ "[other term]"
```

**Regla de estado y precisión del ciclo vital:**
Cuando en la página se describe un ciclo vital (estados de recorrido, estados de mensajes, estados de campañas, etc.), copie las etiquetas de estado exactas del cuerpo de la página. No parafraseen. Utilice las entradas &quot;No confundir&quot; para desambiguar los estados que comparten una palabra raíz pero tienen un significado distinto. Ejemplo:

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. Preguntas frecuentes

3-6 preguntas que un usuario podría hacer, con respuestas cortas.

```
**FAQ:**

* **Q: [question]** — [short answer]
```

**Regla de precisión de preguntas frecuentes:**
Las respuestas deben utilizar las mismas opciones de verbo y sustantivo que el cuerpo de la página. No introduzca verbos como &quot;revertir&quot;, &quot;restablecer&quot; o &quot;revertir&quot; a menos que la página los utilice. Si una transición finaliza una sesión (por ejemplo, si sale del modo de prueba y el recorrido vuelve a su estado anterior), diga exactamente eso: no diga &quot;el recorrido vuelve a Borrador&quot;.

### Qué NO incluir

- **no** reescribe o resume el contenido del cuerpo (ya está en la página)
- **no** incluye instrucciones paso a paso
- **no** inventa contenido no admitido por la página
- **no** usa los siguientes términos imprecisos a menos que aparezcan textualmente en el cuerpo de la página: &quot;sintético&quot;, &quot;datos falsos&quot;, &quot;sin datos reales&quot;, &quot;revertir&quot;, &quot;revertir&quot; (al describir transiciones de estado del producto)

&#x200B;---

## Lista de comprobación de validación posterior a la generación

Ejecute esta lista de comprobación en cada bloque antes de escribir la inclusión. Marque cualquier error en el usuario antes de continuar.

### Comprobación de seguridad

- [ ]: cada valor numérico del bloque existe literalmente o se deriva del cuerpo de la página
- [ ] Cada límite se califica como recomendado o difícil
- [ ] Cada cifra de rendimiento incluye su ámbito (zona protegida/organización/instancia)

### Comprobación terminológica
- [ ] Todos los modos de validación (Simulación, Modo de prueba, Ejecución en seco) presentes en la página se incluyen y se nombran con términos precisos para la página
- [ ] Todos los estados del ciclo vital utilizan las etiquetas exactas del cuerpo de la página
- [ ] No hay verbos imprecisos en las respuestas a preguntas frecuentes (&quot;revertir&quot;, &quot;sintético&quot;, &quot;datos falsos&quot;, &quot;sin datos reales&quot;) a menos que estén presentes literalmente en la página

### Comprobación del ámbito
- [ ] El glosario no contiene términos de marketing genéricos que no estén relacionados con la página
- [ ] respuestas a preguntas frecuentes no presentan información ausente de la página

Si alguna comprobación falla, corrija el bloque antes de escribir la inclusión. Registre la corrección en el informe Paso 5.

&#x200B;---

## Responsabilidad de sincronización

El bloque Referencia de conocimiento de IA es una derivada del cuerpo de la página en un momento dado. Debe tratarse como parte de la página.

**Cuando se actualice el cuerpo de la página (publicar PR, correcciones, etc.):**

- Si la actualización cambia cualquier protección, límite, etiqueta de estado o modo de validación descrito en el bloque, → regenerar o actualizar manualmente el bloque en la misma PR.
- Si la actualización no está relacionada con el contenido del bloque (por ejemplo, los pasos del procedimiento o las actualizaciones de la captura de pantalla), → el bloque puede permanecer sin cambios, pero revíselo brevemente.

El comentario de sincronización dentro del archivo de inclusión (`<!-- ai-section-version -->`) es la señal: si el cuerpo de la página de inclusión ha cambiado desde que se escribió ese hash, el bloque es candidato para revisión. Al actualizar, edite el archivo de inclusión en `help/_includes/do-not-localize/`, no la página.

&#x200B;---

## Plantilla completa

Incluir archivo (`help/_includes/do-not-localize/<section-folder>/ai-augmented-<page>.md`):

```markdown
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

* **TL;DR:** [one sentence]

**Intents:**

* [intent]

**Glossary:**

* **[Term]**: [definition] *(product-specific)*

**Guardrails:**

* [guardrail — qualify each numeric limit as recommended|hard, each throughput figure with scope sandbox|org]

**Terminology:**

* Canonical name: [name] — Acronym: [acronym] — variants: [variants]
* Synonyms: "[a]" = "[b]"
* Do not confuse: "[x]" ≠ "[y]"

**FAQ:**

* **Q: [question]** — [short answer]

+++

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

Línea añadida a la página:

```
{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-end-journey.md}}
```

## Notas

- Procesar archivos uno por uno para mejorar la calidad.
- Marque páginas muy cortas o solo de índice y pregunte al usuario si desea omitir.
- El único archivo nuevo creado por página es la inclusión de no localizar (Paso 4); la página en sí se edita solo para agregar la línea `{{$include}}` única. De lo contrario, no cree ni reestructure archivos.
- La lista de comprobación de validación posterior a la generación no es opcional. Ejecútelo para cada archivo, incluidas las operaciones por lotes.
