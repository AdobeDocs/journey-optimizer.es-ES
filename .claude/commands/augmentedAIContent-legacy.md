---
source-git-commit: c81615909e033d52fbed56f0195467a3e346a4be
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

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
3. **Genere el contenido del acordeón** con las reglas siguientes.
4. **Comprueba** si ya existe un acordeón de IA al final (busca `+++AI Assistant` cerca del final). En caso afirmativo, pregunte al usuario: ¿reemplazar o omitir?

### Paso 3: Añadir el acordeón

Anexar al final del archivo. No modifique ningún otro contenido.

### Paso 4: Informe

- Archivos modificados ✓
- Archivos omitidos + motivo (ya tiene página de acordeón / vacía / índice)

&#x200B;---

## Reglas de generación de contenido

Analice la página y produzca las secciones debajo de **en orden** como listas de viñetas de markdown. Omita secciones en las que no se pueda extraer contenido significativo.

### Título del acordeón

`+++AI Assistant — Page context`

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

### &#x200B;4. Mecanismos de protección

Limitaciones, requisitos previos, permisos o restricciones mencionadas en la página.

```
**Guardrails:**
- [guardrail]
```

### &#x200B;5. Terminología

Nombres canónicos, siglas, variantes aceptadas, sinónimos, desambiguación. Principalmente para la normalización de canalización de IA.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

### &#x200B;6. Preguntas frecuentes

3-6 preguntas que un usuario podría hacer, con respuestas cortas.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

### Qué NO incluir

- **no** reescribe o resume el contenido del cuerpo (ya está en la página)
- **no** incluye instrucciones paso a paso
- **no** inventa contenido no admitido por la página

### Plantilla completa

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
- [guardrail]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

&#x200B;---

## Notas

- Procesar archivos uno por uno para mejorar la calidad.
- Marque páginas muy cortas o solo de índice y pregunte al usuario si desea omitir.
- No crear nuevos archivos: solo editar los archivos `.md` existentes.
