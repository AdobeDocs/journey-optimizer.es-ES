---
name: ajo-ai-accordion
description: Enriquece las páginas de documentación de Adobe Journey Optimizer con una sección de acordeón del Asistente de IA adjunta al final de cada archivo Markdown. Lee cada página, genera automáticamente contenido relevante del Ayudante de IA en función del tema de la página y lo inserta como un acordeón contraíble. Se utiliza cuando el usuario desea agregar información de IA a documentos de AJO, enriquecer páginas de marcado de AJO con contenido de IA o procesar un archivo o carpeta de archivos de marcado con secciones de acordeón de AI.
disable-model-invocation: true
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---


# Enriquecimiento de acordeón de AJO AI

Adjunta un acordeón del asistente de IA generado automáticamente al final de uno o más archivos de marcado en el repositorio de documentación de Journey Optimizer.

## Repositorio de destino

`/Users/sauviat/GitHub/GHEC/journey-optimizer.en/help/using/`

## Sintaxis de acordeón (Experience League)

```markdown
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Reglas:**
- `+++Title` en una línea — el título sigue inmediatamente a `+++`, sin espacio entre
- `+++` solo en una línea cierra el acordeón
- Línea en blanco antes de `+++` y después de `+++`

---

## Flujo de trabajo

### Paso 1: Preguntar por los destinatarios

Pregunte al usuario:

> ¿Qué archivo o carpeta desea enriquecer?
> - Archivo único: ruta relativa a la raíz del repositorio (p. ej. `help/using/email/get-started-email.md`)
> - Carpeta: procesa de forma recursiva todos los archivos de `.md` dentro de (p. ej. `help/using/email`)
> - Lista de archivos/carpetas

Use `AskQuestion` si está disponible; de lo contrario, pregunte en conversación.

Si se proporciona una carpeta, enumere todos los `.md` archivos encontrados y confirme con el usuario antes de procesar.

### Paso 2: Para cada fichero: leer y generar

Para cada archivo de destino:

1. **Lea el archivo** por completo.
2. **Comprenda el tema de la página**: ¿qué característica, concepto o tarea cubre?
3. **Genere el contenido del acordeón** usando las reglas de generación de contenido siguientes.
4. **Comprueba** si ya existe un acordeón de IA al final del archivo (busca `+++` cerca del final). En caso afirmativo, pregunte al usuario si desea realizar la sustitución o la omisión.

### Paso 3: Añadir el acordeón

Anexe al final del archivo:

```markdown
+++[ACCORDION_TITLE]

[GENERATED_CONTENT]

+++
```

No se debe modificar ningún otro contenido del archivo.

### Paso 4: Informe

Una vez procesados todos los archivos:
- Archivos de lista modificados ✓
- Lista de archivos omitidos y motivo (ya tiene acordeón, archivo vacío, no relevante, etc.)

---

## Reglas de generación de contenido

Genere el contenido del acordeón analizando la página Markdown. Produzca las siguientes secciones **en orden**, con formato de listas de viñetas de markdown. Omita cualquier sección para la que no se pueda extraer contenido significativo de la página.

---

### Título del acordeón

Uso: `+++AI Assistant — Page context`

---

### Secciones que se van a generar (en orden)

**1. TL;DR**

Una frase. ¿Qué enseña o habilita esta página?

```markdown
- **TL;DR:** [one sentence summary]
```

---

**2. Intenciones**

Lista con viñetas de lo que un usuario puede lograr después de leer esta página (de 3 a 6 elementos).

```markdown
**Intents:**
- [action the user can perform]
- [action the user can perform]
```

---

**3. Glosario**

Términos clave específicos de esta página o función, con una definición corta. Marcar términos específicos de productos.

```markdown
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
- **[Term]**: [definition]
```

Incluir solo términos que sean relevantes para el tema de esta página. No rellene con términos de marketing genéricos.

---

**4. Protecciones**

Limitaciones, requisitos previos, permisos o restricciones mencionadas en la página.

```markdown
**Guardrails:**
- [guardrail or prerequisite]
- [guardrail or prerequisite]
```

---

**5. Terminología**

Nombres de productos canónicos, acrónimos, variantes aceptadas, sinónimos y sugerencias de desambiguación. Esta sección está dirigida principalmente a la normalización de canalización de IA.

```markdown
**Terminology:**
- Canonical name: [e.g. Adobe Journey Optimizer]
- Acronym: [e.g. AJO] — variants: [e.g. Journey Optimizer, A-JO]
- Synonyms: [e.g. "brand guidelines" = "brand rules", "branding standards"]
- Do not confuse: [e.g. "AI Assistant" ≠ "Adobe Sensei"]
```

Incluir solo las entradas que estén presentes o implícitas en la página.

---

**6. PREGUNTAS FRECUENTES**

3-6 preguntas que un usuario podría hacer acerca del contenido de esta página, con respuestas cortas.

```markdown
**FAQ:**
- **Q: [question]** — [short answer]
- **Q: [question]** — [short answer]
```

---

### Qué NO incluir

- **no** reescribe o resume el contenido del cuerpo de la página (ya está ahí).
- **no** incluye instrucciones paso a paso (las que se encuentran en la página).
- **no** inventa contenido que no es compatible con la página.

---

### Plantilla de acordeón completa

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
- Canonical name: [name]
- Acronym: [acronym] — variants: [variants]

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

---

## Notas

- Procese los archivos uno por uno, no en lotes, para mantener una alta calidad de generación.
- Si la página es muy corta o simplemente una página de redirección/índice, márquela y pregunte al usuario si desea omitirla.
- No crear nuevos archivos: solo editar los archivos `.md` existentes.
