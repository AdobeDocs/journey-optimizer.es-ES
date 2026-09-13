---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---
# Ronda de verificación: la puerta de calidad final obligatoria

Esta es la puerta 2 de 2 y el paso que garantiza que cada bloque es **válido, verdadero y libre de errores
ambigüedad&#x200B;**. No es &#x200B;** opcional y no se puede omitir**, incluso para actualizaciones de una sola página.

## Por qué es independiente

El autor del bloque (puerta 1) está demasiado cerca del bloque para detectar sus propios errores de conexión a tierra. Puerta 2
es una **revisión contradictoria independiente**: un revisor nuevo que supone que el bloque puede ser incorrecto
e intenta probarlo, usando **solamente** el cuerpo de la página como verdadero. Ejecutarlo como **subagente independiente**
eso no ha visto cómo se escribió el bloque — esta independencia es lo que lo hace efectivo. Para
Un lote de páginas, un subagente verificador puede cubrir toda la carpeta.

## Lo que hace el verificador, por página

1. Leer la **página de origen completa** `help/using/<folder>/<page>.md`. HTML-comment /
el contenido comentado **no es** un origen válido.
2. Leer **bloque** `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`.
3. Clasifique **cada** notificación como EN TIERRA / INEXACTA / NO EN TIERRA con respecto al cuerpo de la página.
4. **Corrija todos los problemas editando sólo el archivo de bloque**; conserve las dos aperturas fijas
párrafos, las `+++ … +++` vallas y el comentario de sincronización. Nunca modifique la página de origen.
5. Informe por página: `clean` o `N issues` + las correcciones exactas aplicadas.

## La lista de comprobación de confrontación (primero los elementos de mayor riesgo)

- **Números y límites.** Cada valor es exacto. Un límite es `(hard limit)` solo si la página utiliza
cumplimiento/redacción máxima; `(default)` si se puede plantear/predeterminado/configurable (incluida la &quot;solicitud&quot;)
más a través de su representante de Adobe&quot; o &quot;aumentable a través de API&quot;); `(recommended)` para obtener asesoramiento; no
calificador si la página no proporciona ninguno. **Reduzca cualquier límite que el generador haya etiquetado excesivamente como rígido.**
Cada cifra de rendimiento/tasa tiene su alcance.
- **Fechas, ID, nombres de producto/campo, identificadores SQL, enumeraciones de estado, cadenas de error** — textual
en la página. Tolerancia cero en los marcos de tiempo legales/de conformidad: no invente nunca una SLA, retención,
o fecha de aplicación; mantenga cualquier fecha exactamente como la indica la página y etiquetada como página
lo enmarca.
- **Sinónimos frente a No confundir.** Un sinónimo (`"A" = "B"`) requiere ambos formularios en la página
significa lo mismo. Cualquier contraste (`"X" ≠ "Y"`) pertenece a &quot;No confundir&quot;. Mover
etiquetas erróneas.
- **Modos de validación/prueba** con el nombre de los términos exactos de la página, no combinados en
experiencias clásicas o rediseñadas, o entre canales.
- **Conexión a tierra.** No se ha importado nada desde otra página, conocimiento general del producto o un HTML
comentario. Elimine cualquier elemento que el cuerpo de la página no admita.
- **Estilo.** Sin contracciones (fuera de las cadenas literales `[!UICONTROL ...]` / `[!DNL ...]`). Ninguna
de las palabras prohibidas (&quot;sintético&quot;, &quot;datos falsos&quot;, &quot;sin datos reales&quot;, &quot;revertir&quot;, &quot;revertir&quot;)
a menos que aparezca textualmente en la página. Cadenas de interfaz de usuario conservadas exactamente.
- **Estructura.** Dos párrafos de apertura fijos intactos y literales; seis secciones presentes y en
orden en el que la página los admite; sincronización de comentarios presente.

## Mensaje de subagente de verificador reutilizable

Rellene la lista de carpetas y páginas. Inícielo como un subagente independiente de uso general.

```
You are an ADVERSARIAL fact-checker for Adobe Journey Optimizer doc "AI Knowledge Reference"
blocks. Repo: <repo path>. Assume each block MAY contain errors; try hard to find them. This is
the final accuracy gate.

PAGES (basenames): <p1> <p2> ...
SOURCE: help/using/<folder>/<p>.md   BLOCK: help/_includes/do-not-localize/<folder>/ai-augmented-<p>.md

For EACH page:
1. Read the FULL source page body (HTML-comment / commented-out content is NOT valid source).
2. Read the block.
3. Classify EVERY claim GROUNDED / INACCURATE / NOT-GROUNDED against the page body. Scrutinize:
   numeric limits (hard only if the page uses enforcement/maximum wording; downgrade any
   raisable/default/configurable value the block marked hard; every rate figure needs its
   scope); dates/IDs/field names/SQL identifiers/status enums/error strings verbatim and no
   invented SLA/legal timeframes; Synonyms are true equivalents (mislabels -> Do not confuse);
   validation/test modes named with the page's exact terms and not conflated; nothing imported
   from other pages or HTML comments; no contractions (outside verbatim [!UICONTROL ...]); no
   banned words (synthetic / fake data / without real data / revert / roll back) unless verbatim.
4. FIX every issue by editing ONLY the block file. Preserve the two fixed opening paragraphs,
   the +++ ... +++ fences, and the sync comment. Do NOT modify source pages.

Report per page: "<p>: clean" or "<p>: N issues" + the exact fixes applied.
```

## Criterios de salida

La carpeta pasa la puerta 2 únicamente cuando el verificador notifica cada página como `clean` (o se encontró
nada, o se aplicaron correcciones y el bloque ahora está limpio). Si aplicó correcciones, ya están
en los archivos de bloque: inclúyalos en el informe final y continúe con el barrido y la confirmación.
