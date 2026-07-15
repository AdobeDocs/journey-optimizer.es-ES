---
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---
# augmentedAIContent

Adjunta una sección **Referencia rápida** generada automáticamente al final de uno o más archivos Markdown en el repositorio de documentación de Journey Optimizer.

## Repositorio de destino

`help/using/` (relativo a la raíz del repositorio)

## Sintaxis de secciones y pestañas (Experience League)

### Encabezado de sección

```
## Quick reference {#quick-reference}
```

### Fichas

```
>[!BEGINTABS]

>[!TAB Tab name]

Content here — any standard markdown is valid.

>[!TAB Another tab]

Content here.

>[!ENDTABS]
```

**Reglas:**

- `>[!BEGINTABS]` y `>[!ENDTABS]` cada uno en su propia línea, rodeados por líneas en blanco
- `>[!TAB Name]` en su propia línea, seguida de una línea en blanco antes del contenido
- Los nombres de las pestañas son mayúsculas y minúsculas, cortos (de 1 a 3 palabras)
- Línea en blanco antes de `>[!BEGINTABS]` y después de `>[!ENDTABS]`

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
3. **Genere el contenido de la sección** usando las reglas de generación de contenido siguientes.
4. **Ejecute la lista de comprobación de validación posterior a la generación** (ver a continuación); no la omita.
5. **Compruebe** si ya existe una sección de referencia rápida al final (busque `## Quick reference` cerca del final). En caso afirmativo, pregunte al usuario: ¿reemplazar o omitir?

### Paso 3: Verificar todas las reclamaciones contra el cuerpo de la página

Antes de anexar, vuelva a leer la notificación de sección generada por notificación. Este paso es **obligatorio y no se puede omitir**, ni siquiera en el caso de archivos cortos. Corrija cualquier error antes de continuar con el paso 4.

**Terminología y etiquetas**

- [ ] Cada término, etiqueta y nombre de interfaz de usuario de la sección aparece en el cuerpo de la página, no importado de otra página ni deducido del conocimiento general del producto
- [ ] No aparece ningún sinónimo a menos que ambos formularios aparezcan en la página
- [ ] Cada entrada &quot;No confundir&quot; hace referencia únicamente a los conceptos mencionados en esta página

**Protecciones y límites**

- [ ] Cada valor numérico coincide exactamente con el cuerpo de la página
- [ ] Se llama a un límite **hard** solo si el cuerpo de la página usa esa palabra o implica claramente que el sistema la aplica (por ejemplo, &quot;no puede exceder&quot;, &quot;máximo ... permitido&quot;, &quot;solo ... admitido&quot;)
- [ ] Se llama a un límite **recomendado** solo si el cuerpo de la página usa esa palabra o un equivalente (&quot;para obtener el mejor rendimiento&quot;, &quot;se recomienda&quot;)
- [ ] Si el cuerpo de la página no da ningún calificador, la sección no da ninguno: no invente uno
- [ ] No hay ningún metacomentario sobre lo que dice o no la página de origen (por ejemplo, &quot;no se indica un número específico en esta página&quot;)

**Definiciones de glosario**

- [ ]: ninguna definición contiene detalles técnicos ausentes del cuerpo de la página
- [ ] Ninguna entrada elabora con información de otras páginas del conjunto de documentación

**respuestas a preguntas frecuentes**

- [ ] Cada detalle específico (asequibilidad de interfaz de usuario, nombres de botones, nombres de campos, secuencias de pasos) se indica en el cuerpo de la página, no se infiere ni se importa desde otras páginas
- [ ] Ninguna respuesta presenta información que el cuerpo de la página no aborda

**Regla de corrección:** Si falla alguna comprobación, corrija el contenido **antes de** anexando. Registre todas las correcciones en el informe del paso 5.

&#x200B;---

### Paso 4: Añadir la sección

Use el bloque de apertura fijo y la plantilla completa definidos a continuación en **Reglas de generación de contenido**. Añada al final del archivo, seguido inmediatamente por el comentario de sincronización:

```
<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of file content before section] -->
```

Este comentario permite a los futuros escritores y herramientas detectar cuándo el cuerpo de la página se ha desviado de la sección. No modifique ningún otro contenido.

### Paso 5: Informe

- Archivos modificados ✓
- Archivos omitidos + motivo (ya tiene sección / vacío / página de índice)
- Cualquier advertencia de validación generada durante el paso 2

&#x200B;---

## Reglas de generación de contenido

Analice la página y produzca las fichas siguientes **en orden**. Omita una pestaña por completo si no se puede extraer contenido significativo para ella.

### Encabezado de sección y apertura fija: textual, no modificar

Cada sección de Referencia rápida debe comenzar con este bloque exacto. Cópielo tal cual; no parafrasee, condense ni reordene:

```
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

El bloque `>[!BEGINTABS]` sigue inmediatamente después de estos dos párrafos.

### Pestaña 1: Información general

TL de una oración;DR summary de lo que la página enseña o habilita, seguido de 3 a 6 cosas que un usuario puede lograr después de leer esta página.

```
>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [action]
* [action]
```

### Pestaña 2: Glosario

Términos clave específicos de esta página o función con definiciones cortas. Marcar términos específicos de productos.

```
>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*
```

Incluya solo términos relevantes para esta página. No rellene con términos de marketing genéricos.

**Regla de precisión del modo de validación — obligatorio:**
Si la página cubre cualquier forma de prueba, previsualización o ejecución simulada, DEBE distinguir entre todos los modos que describe realmente la página. No contraiga los distintos modos en una sola entrada abreviada:
- **Simulación**: procesa el contenido del mensaje sin enviarlo; utiliza perfiles reales
- **Modo de prueba**: envía solo a perfiles de prueba designados; utiliza perfiles de prueba AEP persistentes (no perfiles sintéticos o falsos)
- **Ejecución en seco**: ejecuta la lógica de recorrido completa sin activar acciones; utiliza datos de audiencia reales

Incluya solo los modos presentes en la página. Copie el término preciso del producto desde el cuerpo de la página: no sustituya &quot;perfiles sintéticos&quot;, &quot;datos falsos&quot; ni &quot;sin datos reales&quot; por ninguno de estos términos.

### Pestaña 3: Terminología

Nombres canónicos, siglas, variantes aceptadas, sinónimos, desambiguación. Principalmente para la normalización de canalización de IA.

```
>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [list]
* **Synonyms:** "[term A]" = "[term B]"
* **Do not confuse:** "[term]" ≠ "[other term]"
```

**Regla de estado y precisión del ciclo vital:**
Cuando en la página se describe un ciclo vital (estados de recorrido, estados de mensajes, estados de campañas, etc.), copie las etiquetas de estado exactas del cuerpo de la página. No parafraseen. Utilice las entradas &quot;No confundir&quot; para desambiguar los estados que comparten una palabra raíz pero tienen un significado distinto. Ejemplo:

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### Pestaña 4: Protecciones y limitaciones

Limitaciones, requisitos previos, permisos o restricciones mencionadas en la página.

```
>[!TAB Guardrails & Limitations]

* [guardrail]
```

**Reglas de precisión de protección — obligatorio:**

- **Califica cada límite numérico** como recomendado o difícil. Ejemplo: &quot;Máximo 10 búsquedas de conjuntos de datos por mensaje (límite estricto)&quot;, no &quot;Máximo 10 búsquedas de conjuntos de datos&quot;.
- **Califique cada cifra de rendimiento o tasa** con su ámbito. Ejemplo: &quot;Límite de TPS de 150 000 mensajes/hora (por zona protegida)&quot;, no &quot;Límite de TPS de 150 000 mensajes/hora&quot;.
- **Compruebe todas las protecciones del cuerpo de la página** antes de incluirla. Si la página indica 10 y la sección 5, la sección es incorrecta. El cuerpo de la página es autoritativo.
- **No deduzca protecciones** que no se indiquen en la página. Si existe una restricción pero la página no la indica, omítala.

### Pestaña 5: Preguntas frecuentes

3-6 preguntas que un usuario podría hacer, con respuestas cortas. Asigne a cada una el formato de un encabezado de pregunta en negrita seguido de una respuesta de párrafo.

```
>[!TAB FAQ]

**Q: [question]**

[short answer]
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

Ejecute esta lista de comprobación en cada sección antes de anexar. Marque cualquier error en el usuario antes de continuar.

### Comprobación de seguridad

- [ ]: cada valor numérico de la sección existe literalmente o se deriva del cuerpo de la página
- [ ] Cada límite se califica como recomendado o difícil
- [ ] Cada cifra de rendimiento incluye su ámbito (zona protegida/organización/instancia)

### Comprobación terminológica
- [ ] Todos los modos de validación (Simulación, Modo de prueba, Ejecución en seco) presentes en la página se incluyen y se nombran con términos precisos para la página
- [ ] Todos los estados del ciclo vital utilizan las etiquetas exactas del cuerpo de la página
- [ ] No hay verbos imprecisos en las respuestas a preguntas frecuentes (&quot;revertir&quot;, &quot;sintético&quot;, &quot;datos falsos&quot;, &quot;sin datos reales&quot;) a menos que estén presentes literalmente en la página

### Comprobación del ámbito
- [ ] El glosario no contiene términos de marketing genéricos que no estén relacionados con la página
- [ ] respuestas a preguntas frecuentes no presentan información ausente de la página

Si alguna comprobación falla, corrija la sección antes de anexar. Registre la corrección en el informe Paso 4.

&#x200B;---

## Responsabilidad de sincronización

La sección Referencia rápida es una derivada del cuerpo de la página en un momento dado. Debe tratarse como parte de la página.

**Cuando se actualice el cuerpo de la página (publicar PR, correcciones, etc.):**

- Si la actualización cambia alguna protección, límite, etiqueta de estado o modo de validación descrito en la sección, → regenerar o actualizar manualmente la sección en la misma PR.
- Si la actualización no está relacionada con el contenido de la sección (por ejemplo, los pasos del procedimiento o las actualizaciones de la captura de pantalla), → la sección puede permanecer sin cambios, pero revísela brevemente.

El comentario de sincronización anexado después de la sección (`<!-- ai-section-version -->`) es la señal: si el contenido del archivo antes de la sección ha cambiado desde que se escribió ese hash, la sección es candidata para revisión.

&#x200B;---

## Plantilla completa

```markdown
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

>[!BEGINTABS]

>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [intent]

>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*

>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [variants]
* **Synonyms:** "[a]" = "[b]"
* **Do not confuse:** "[x]" ≠ "[y]"

>[!TAB Guardrails & Limitations]

* [guardrail — type: recommended|hard — scope: sandbox|org]

>[!TAB FAQ]

**Q: [question]**

[short answer]

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

## Notas

- Procesar archivos uno por uno para mejorar la calidad.
- Marque páginas muy cortas o solo de índice y pregunte al usuario si desea omitir.
- No crear nuevos archivos: solo editar los archivos `.md` existentes.
- La lista de comprobación de validación posterior a la generación no es opcional. Ejecútelo para cada archivo, incluidas las operaciones por lotes.
