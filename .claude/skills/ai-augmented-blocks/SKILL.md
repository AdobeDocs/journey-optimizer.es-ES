---
name: ai-augmented-blocks
description: Generar y mantener bloques de referencia de conocimiento de IA para documentos de Adobe Journey Optimizer (recorrido-optimizer.en). Utilícelo cuando una página nueva bajo ayuda/uso/ necesite un bloque de IA, cuando una página existente haya cambiado y su bloque pueda haberse desplazado o cuando se le pida que añada/actualice/verifique contenido de referencia de conocimiento de IA (aumentada por IA). Produce una inclusión no localizada en help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md, la conecta a la página con {{$include}}, ejecuta una ronda de verificación independiente obligatoria para que el bloque sea verdadero e inequívoco, rastrea el trabajo en una tarea DOCAC JIRA y (solo después de preguntar al autor) abre una PR. NUNCA se combina.
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 0%

---


# Bloques de referencia de conocimientos de AI

Esta aptitud genera y mantiene **Referencia de conocimientos de IA** bloques de acordeón para
Documentación de Adobe Journey Optimizer (`journey-optimizer.en`). Los bloques están estructurados,
contexto no localizado anexado a las páginas de documento para que el asistente de IA responda preguntas sobre
Journey Optimizer con mayor precisión.

Cada bloque se almacena como **no localizar include** (por lo que nunca se traduce) y se extrae
en su página con `{{$include}}`. Un bloque contiene **solamente hechos derivados de su propia página
cuerpo**: nada importado de otras páginas, conocimientos generales del producto o comentarios de HTML.

> **Lea los archivos de referencia antes de generar nada.** Contienen las reglas reales, no
> un resumen:
> - `references/generation-spec.md`: estructura de bloques, apertura fija, sección por sección
>   reglas de contenido, y cada regla de precisión (límites difíciles frente a recomendados, modos de validación,
>   etiquetas de estado, sin contracciones, la lista de palabras prohibidas).
> - `references/verification-round.md`: la comprobación de hechos contradictoria independiente **obligatoria**
>   esa es la puerta de calidad final. No es opcional y no se puede omitir.
> - `references/git-jira-tracking.md` — flujo de rama/compromiso/PR (pregunte al autor antes de abrir un
>   PR; **nunca combinar**) y seguimiento DOCAC JIRA.

## Cuando se aplique esta aptitud

- **La nueva página** creada en `help/using/<folder>/` → un bloque para ella.
- **La página existente cambió** → comprobar si su bloque se desvió del cuerpo de la página y actualizarlo.
- Se le pidió que **agregara, actualizara, verificara o auditara** bloques aumentados con IA/referencia de conocimientos de IA.

## Ámbito y exclusiones

- **En ámbito:** páginas en `help/using/<folder>/`.
- **Fuera del ámbito; no agregue nunca bloques aquí:**
  - `help/rp_landing_pages/` (páginas de inicio/destino) — excluido por la regla de autor.
  - Concentradores de vínculos/navegación delgados, páginas solo de índice y páginas casi vacías. Cuando una página está vacía
    lista de vínculos sin conceptos sustantivos, **omita la lista y diga por qué** — no forzar un bloqueo.
  - Notas de la versión (`help/using/rn/`, páginas de notas de la versión).
- Cuando haya dudas sobre si una página es lo suficientemente sustantiva, juzgue por el contenido: si enseña algo real
los conceptos, restricciones o terminología lo cubren; si solo señala a otra parte, sáltelo.

## Flujo de trabajo

Trabajar **una carpeta (o una página) a la vez**. No agrupe carpetas no relacionadas en una rama.

### 1 — Determinar objetivos y modo

Pregunte al autor (o deduzca de la solicitud/archivos abiertos) qué páginas procesar y detectar el
modo por página:

- **CREATE** — la página no tiene línea `{{$include .../ai-augmented-<page>.md}}` ni existe
bloque `+++ AI Knowledge Reference` en línea → generar un nuevo bloque.
- **ACTUALIZACIÓN** — la página ya tiene un bloque. Calcule el hash del cuerpo de la página y compárelo con el valor
  `source-hash` en el comentario de sincronización de la inclusión (ver a continuación). Si difieren, la página → a la deriva
  regenerar/actualizar el bloque. Si coinciden, el bloque es actual → omitir (informe &quot;actualizado&quot;).
- **MIGRAR** — la página tiene un bloque *inline* `+++ AI Knowledge Reference` (aún no
externalizado) → moverlo a una inclusión no localizada y reemplazarla por la variable `{{$include}}`
línea, conservando la fidelidad del contenido.

Calcule el hash del cuerpo de la página del mismo modo en todas partes (utilizado para el comentario de sincronización y la comprobación de deriva):

```bash
md5 -q help/using/<folder>/<page>.md | cut -c1-8
```

Calcule **antes** de editar la página (el hash cubre el cuerpo tal como está cuando se bloquea)
generadas). En Linux, use `md5sum help/using/<folder>/<page>.md | cut -c1-8`.

### 2 — Generar (o actualizar) el bloque

Seguir `references/generation-spec.md` exactamente en cada página. Invariantes clave:

- Dos **párrafos de apertura fijos**, literalmente, byte a byte (nunca parafraseados).
- Secciones en orden: **TL;DR, intenciones, glosario, protecciones, terminología, preguntas frecuentes**.
- Cada reclamación basada únicamente en el cuerpo de la página. No hay contracciones. Calificar números como
  `(hard limit)` / `(recommended)` **solo** cuando la página utiliza aplicación/recomendación
  texto; de lo contrario, no hay calificador. Utilice las etiquetas de estado y modo de validación exactos de la página.
  Conservar las cadenas `[!UICONTROL ...]` / `[!DNL ...]` textualmente. Nunca use el impreciso prohibido
  términos a menos que aparezcan literalmente en la página.

**Incluir archivo** — `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`
(cree el subdirectorio `<folder>` si es necesario; aplane cualquier ruta de página anidada con `-`):

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening paragraphs + the six sections]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of the page body> -->
```

**Edición de página** — agrega exactamente una línea, como la última línea de contenido, precedida por una línea en blanco
(no toque nada más en la página):

```
{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}
```

En UPDATE, edite solo el archivo de inclusión (y marque `ai-section-version` si desea realizar el seguimiento
revisiones); la línea `{{$include}}` de la página suele ser la misma. Actualizar `source-hash` a
el hash del cuerpo de la página actual una vez que el bloque vuelve a coincidir con la página.

Ejecute la **autocomprobación** en `references/generation-spec.md` (Paso 3: compruebe todas las notificaciones + el
lista de comprobación posterior a la generación) antes de continuar. Esta es la puerta 1 de 2.

### 3 — Ronda de verificación independiente (puerta final obligatoria)

Este es el paso que el autor requiere específicamente: **confirme que cada bloque es válido, true y
sin ambigüedad.** Ejecútelo como un pase *nuevo e independiente*; lo ideal sería un subagente independiente que
solo ve el cuerpo de la página y el bloque, sin memoria de cómo se escribió el bloque: a continuación
`references/verification-round.md`. Vuelve a comprobar cada reclamación, rebaja cualquier límite mal etiquetado,
corrige los errores de Sinónimos frente a No confundir y elimina todo lo que no esté basado en la página. Aplicar
realice todas las correcciones necesarias en el archivo include antes de continuar. Esta es la puerta 2 de 2 y no se puede omitir.

### 4 — Barrido estructural

Antes de comprometerse, barre cada bloque para ver si hay estructura e higiene (consulte el fragmento de barrido en
`references/git-jira-tracking.md`): asunto principal + encabezado `# AI Knowledge Reference`, el
`+++ … +++` vallas, el párrafo de apertura fijo, el comentario de sincronización, sin contracciones (excluyendo
`[!UICONTROL ...]`) y una línea `{{$include}}` coincidente en la página.

### 5 — Rastree en JIRA y luego pregunte por una PR (nunca fusione)

Seguir `references/git-jira-tracking.md`:

1. Confirme en una rama denominada para la tarea JIRA (`DOCAC-<key>`), nunca en `main`. Compruebe el
la confirmación aterrizó en la rama (1 confirmación antes de `origin/main`), no en `main`.
2. Actualizar la tarea DOCAC: comentar con lo que cambió + el resultado de verificación, establecer la corrección
y realice la transición según lo requiera el proceso de su equipo.
3. **Pregunte al autor si desea una solicitud de extracción.** Sólo abre uno si dicen que sí.
4. **No combinar nunca.** Estas relaciones públicas son para revisión humana; la combinación siempre es la llamada del autor.

### 6 — Informe

Informe por página: creado/actualizado/migrado/omitido (+ motivo), el resultado de la verificación
(limpia o corregida, con las correcciones), la tarea JIRA y el vínculo PR si se ha abierto uno.

## Notas para los redactores que tienen esta aptitud

- El bloque es un **derivado del cuerpo de la página en un momento dado**; trátelo como parte del
página. Cuando cambia una página de forma que afecta a una protección, un límite, una etiqueta de estado o
modo de validación, actualice el bloque en el mismo cambio.
- Los pasos de JIRA y PR necesitan acceso a JIRA y GitHub corporativos. Si no tiene eso
Acceda, siga generando + verificando el bloque y abra el cambio localmente; entregue los pasos de JIRA/PR
a alguien que sí.
- Esta aptitud se encuentra en el repositorio, por lo que todo el equipo de redacción comparte un proceso. Mejore la
Haga referencia a los archivos aquí en lugar de mantener copias privadas.
