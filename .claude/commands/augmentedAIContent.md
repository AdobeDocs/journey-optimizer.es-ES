---
source-git-commit: c81615909e033d52fbed56f0195467a3e346a4be
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 1%

---
# augmentedAIContent

Adjunta un acordeón del asistente de IA generado automáticamente al final de uno o más archivos de marcado en el repositorio de documentación de Journey Optimizer.

## Repositorio de destino

`help/using/` (relativo a la raíz del repositorio)

## Sintaxis de acordeón (Experience League)

```
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Reglas:**
- `+++Title` en una línea: el título sigue inmediatamente a `+++`
- `+++` solo en una línea cierra el acordeón
- Línea en blanco antes de `+++` y después de `+++`

---

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
3. **Genere el contenido del acordeón** usando las reglas de generación de contenido siguientes.
4. **Ejecute la lista de comprobación de validación posterior a la generación** (ver a continuación); no la omita.
5. **Comprueba** si ya existe un acordeón de IA al final (busca `+++AI Knowledge Reference` cerca del final). En caso afirmativo, pregunte al usuario: ¿reemplazar o omitir?

### Paso 3: Añadir el acordeón

Use el bloque de apertura fijo y la plantilla completa definidos a continuación en **Reglas de generación de contenido**. Añada al final del archivo, seguido inmediatamente por el comentario de sincronización:

```
<!-- ai-accordion-version: 1 | source-hash: [first 8 chars of MD5 of file content before accordion] -->
```

Este comentario permite a futuros escritores y herramientas detectar cuándo el cuerpo de la página se ha alejado del acordeón. No modifique ningún otro contenido.

### Paso 4: Informe

- Archivos modificados ✓
- Archivos omitidos + motivo (ya tiene página de acordeón / vacía / índice)
- Cualquier advertencia de validación generada durante el paso 2

---

## Reglas de generación de contenido

Analice la página y produzca las secciones debajo de **en orden** como listas de viñetas de markdown. Omita secciones en las que no se pueda extraer contenido significativo.

### Título del acordeón y apertura fija: textual, no modificar

Cada acordeón debe comenzar con este bloque exacto. Cópielo tal cual; no parafrasee, condense ni reordene:

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

Las secciones de contenido generadas siguen inmediatamente después de estos dos párrafos.

### 1. TL;DR

Resumen de una frase de lo que la página enseña o habilita.

```
- **TL;DR:** [one sentence]
```

### &#x200B;2. Intenciones

De 3 a 6 cosas que un usuario puede hacer después de leer esta página.

```
**Intents:**
- [action]
- [action]
```

### &#x200B;3. Glosario

Términos clave específicos de esta página o función con definiciones cortas. Marcar términos específicos de productos.

```
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
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
- [guardrail]
```

**Reglas de precisión de protección — obligatorio:**

- **Califica cada límite numérico** como recomendado o difícil. Ejemplo: &quot;Máximo 10 búsquedas de conjuntos de datos por mensaje (límite estricto)&quot;, no &quot;Máximo 10 búsquedas de conjuntos de datos&quot;.
- **Califique cada cifra de rendimiento o tasa** con su ámbito. Ejemplo: &quot;Límite de TPS de 150 000 mensajes/hora (por zona protegida)&quot;, no &quot;Límite de TPS de 150 000 mensajes/hora&quot;.
- **Compruebe todas las protecciones del cuerpo de la página** antes de incluirla. Si la página dice 10 y el acordeón dice 5, el acordeón está equivocado. El cuerpo de la página es autoritativo.
- **No deduzca protecciones** que no se indiquen en la página. Si existe una restricción pero la página no la indica, omítala.

### &#x200B;5. Terminología

Nombres canónicos, siglas, variantes aceptadas, sinónimos, desambiguación. Principalmente para la normalización de canalización de IA.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

**Regla de estado y precisión del ciclo vital:**
Cuando en la página se describe un ciclo vital (estados de recorrido, estados de mensajes, estados de campañas, etc.), copie las etiquetas de estado exactas del cuerpo de la página. No parafraseen. Utilice las entradas &quot;No confundir&quot; para desambiguar los estados que comparten una palabra raíz pero tienen un significado distinto. Ejemplo:

```
- Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. Preguntas frecuentes

3-6 preguntas que un usuario podría hacer, con respuestas cortas.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

**Regla de precisión de preguntas frecuentes:**
Las respuestas deben utilizar las mismas opciones de verbo y sustantivo que el cuerpo de la página. No introduzca verbos como &quot;revertir&quot;, &quot;restablecer&quot; o &quot;revertir&quot; a menos que la página los utilice. Si una transición finaliza una sesión (por ejemplo, si sale del modo de prueba y el recorrido vuelve a su estado anterior), diga exactamente eso: no diga &quot;el recorrido vuelve a Borrador&quot;.

### Qué NO incluir

- **no** reescribe o resume el contenido del cuerpo (ya está en la página)
- **no** incluye instrucciones paso a paso
- **no** inventa contenido no admitido por la página
- **no** usa los siguientes términos imprecisos a menos que aparezcan textualmente en el cuerpo de la página: &quot;sintético&quot;, &quot;datos falsos&quot;, &quot;sin datos reales&quot;, &quot;revertir&quot;, &quot;revertir&quot; (al describir transiciones de estado del producto)

---

## Lista de comprobación de validación posterior a la generación

Ejecute esta lista de comprobación en cada acordeón antes de anexar. Marque cualquier error en el usuario antes de continuar.

### Comprobación de seguridad
- [ ]: cada valor numérico del acordeón existe literalmente o se puede derivar del cuerpo de la página
- [ ] Cada límite se califica como recomendado o difícil
- [ ] Cada cifra de rendimiento incluye su ámbito (zona protegida/organización/instancia)

### Comprobación terminológica
- [ ] Todos los modos de validación (Simulación, Modo de prueba, Ejecución en seco) presentes en la página se incluyen y se nombran con términos precisos para la página
- [ ] Todos los estados del ciclo vital utilizan las etiquetas exactas del cuerpo de la página
- [ ] No hay verbos imprecisos en las respuestas a preguntas frecuentes (&quot;revertir&quot;, &quot;sintético&quot;, &quot;datos falsos&quot;, &quot;sin datos reales&quot;) a menos que estén presentes literalmente en la página

### Comprobación del ámbito
- [ ] El glosario no contiene términos de marketing genéricos que no estén relacionados con la página
- [ ] respuestas a preguntas frecuentes no presentan información ausente de la página

Si alguna comprobación falla, corrija el acordeón antes de anexar. Registre la corrección en el informe Paso 4.

---

## Responsabilidad de sincronización

El acordeón es un derivado del cuerpo de la página en un momento dado. Debe tratarse como parte de la página.

**Cuando se actualice el cuerpo de la página (publicar PR, correcciones, etc.):**
- Si la actualización cambia cualquier protección, límite, etiqueta de estado o modo de validación descrito en el acordeón, → regenerar o actualizar manualmente el acordeón en el mismo PR.
- Si la actualización no está relacionada con el contenido del acordeón (por ejemplo, pasos del procedimiento, actualizaciones de la captura de pantalla), → el acordeón puede permanecer sin cambios, pero revíselo brevemente.

El comentario de sincronización anexado después del acordeón (`<!-- ai-accordion-version -->`) es la señal: si el contenido del archivo antes del acordeón ha cambiado desde que se escribió ese hash, el acordeón es un candidato para revisión.

---

## Plantilla completa

```markdown
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail — type: recommended|hard — scope: sandbox|org]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
<!-- ai-accordion-version: 1 | source-hash: [hash] -->
```

---

## Notas

- Procesar archivos uno por uno para mejorar la calidad.
- Marque páginas muy cortas o solo de índice y pregunte al usuario si desea omitir.
- No crear nuevos archivos: solo editar los archivos `.md` existentes.
- La lista de comprobación de validación posterior a la generación no es opcional. Ejecútelo para cada archivo, incluidas las operaciones por lotes.
