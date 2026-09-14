---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 4%

---
# Especificación de generación: bloques de referencia de conocimiento de IA

La única fuente fiable para lo que contiene un bloque de referencia de conocimiento de IA y cómo es
escrito. Síguelo exactamente para cada página. (Esto refleja el legado de
`.claude/commands/augmentedAIContent.md`; la aptitud es la versión canónica.)

## Regla de oro

Un bloque puede contener **solamente lo que se puede derivar de su propio cuerpo de página.** No otras páginas, no
conocimientos generales del producto, no contenido comentado/comentado por HTML. Si la página no indica
Si, el bloque tampoco.

## Acordeón + sintaxis de inclusión

```
+++ AI Knowledge Reference

Content here — standard markdown.

+++
```

- `+++ AI Knowledge Reference` se abre (un espacio después de `+++`); `+++` se cierra solo.
- Línea en blanco antes del `+++` de apertura y después del `+++` de cierre.
- El título siempre es exactamente `AI Knowledge Reference`.
- Todo el acordeón vive en una inclusión no localizada y la página la extrae con
  `{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}`. Contenido en
  `help/_includes/do-not-localize/` se ha excluido de la localización; así es como permanece el bloque
  sin traducir.

## Incluir estructura de archivos

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening — verbatim]

[the six sections in order]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of page body> -->
```

- **Nombre de archivo:** deriva de la ruta de acceso de la página en relación con su nivel superior `help/using/<folder>/`
sección: eliminar `.md`, reemplazar cualquier `/` restante por `-`, prefijo `ai-augmented-`.
  - `help/using/building-journeys/end-journey.md` → `ai-augmented-end-journey.md`
  - `help/using/building-journeys/expression/journey-properties.md` →
    `ai-augmented-expression-journey-properties.md`
- Una subcarpeta por sección de nivel superior (`building-journeys/`, `email/`, `data/`, ...).

## Apertura fija: textual, nunca modificar

Cada bloque comienza con estos dos párrafos exactamente. Copiar byte a byte; no parafrasear,
condensar o reordenar:

```
This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

## Las seis secciones, en orden

Omita una sección solo si la página no produce contenido significativo para ella.

### 1. TL;DR
Una frase: lo que la página enseña o habilita. `* **TL;DR:** [one sentence]`

### &#x200B;2. Intenciones
De 3 a 6 cosas que un usuario puede hacer después de leer la página.

### &#x200B;3. Glosario
Términos clave específicos de la página con definiciones cortas; marcar términos específicos de productos con
`*(product-specific)*`. No hay relleno de marketing genérico.

**Precisión del modo de validación (obligatorio):** si la página abarca pruebas/previsualización/simulación
ejecución, distinga cada modo que la página realmente nombra, no los contraiga. Utilice los botones
término exacto de la página (por ejemplo `Simulate content`, `Simulate content (AEP profiles)`,
`Send proof`, `Test mode`, `Dry run`, `Simulation`, `test profile`, `sample input`). Nunca
sustituya cualquiera de ellos por &quot;perfiles sintéticos&quot;, &quot;datos falsos&quot; o &quot;sin datos reales&quot;.

### &#x200B;4. Mecanismos de protección
Límites, requisitos previos, permisos y restricciones establecidos en la página.

- **Califica cada límite numérico** como `(hard limit)` o `(recommended)` — pero **solo** cuando el
la página utiliza un texto de aplicación (error/rechazado/máximo/no puede superar/solo se admite ...)
o redacción de recomendación (para un mejor rendimiento / se recomienda). Si la página no proporciona
calificador, no dar ninguno. **Nunca etiquete un valor aumentable, predeterminado o configurable como rígido.**
Los valores que se pueden generar &quot;poniéndose en contacto con el representante de Adobe&quot; o a través de una API son los siguientes
  `(default)`, no es difícil.
- **Califique cada cifra de rendimiento/tasa con su ámbito** (por zona protegida/por organización/por instancia).
- **Compruebe todos los números en el cuerpo de la página.** El cuerpo de la página es autoritativo.
- **No deduzca** protecciones que la página no establece. Sin metacomentario (&quot;la página no
especifique ...&quot;).

### &#x200B;5. Terminología
Nombres canónicos, siglas, variantes, sinónimos, desambiguación.

- **Sinónimos** (`"A" = "B"`) solo para **equivalentes verdaderos**; ambos formularios deben aparecer en la página
significa lo mismo. Cualquier cosa que sea un *contraste* pasa por debajo de **No confunda**
(`"X" ≠ "Y"`), no sinónimos.
- **Estado/precisión del ciclo de vida:** copiar etiquetas de estado exactas del cuerpo de la página; no
paráfrasis. Utilice &quot;No confundir&quot; para separar los estados que comparten una palabra raíz.

### &#x200B;6. Preguntas frecuentes
3-6 preguntas probables con respuestas cortas. Las respuestas utilizan los **mismos verbos y sustantivos que la página
cuerpo**. No introduzca &quot;revertir&quot;, &quot;restablecer&quot; o &quot;revertir&quot; a menos que la página los utilice.

## Qué NO incluir

- No reescriba ni resuma contenido del cuerpo ni dé instrucciones paso a paso.
- No invente contenido no compatible con la página.
- No utilice estos términos imprecisos a menos que aparezcan **literalmente** en la página:
&quot;sintético&quot;, &quot;datos falsos&quot;, &quot;sin datos reales&quot;, &quot;revertir&quot;, &quot;revertir&quot;.
- **No hay contracciones** en ninguna parte de la prosa del bloque: escriba &quot;no es&quot;, &quot;no es&quot;, &quot;no puede&quot;,
&quot;es&quot;, etc. (La única excepción es una cadena de interfaz de usuario de producto literal como
  `[!UICONTROL configuration doesn't exist]`, que se conserva exactamente.)

## Paso 3: Verificar cada notificación (comprobación automática, puerta 1)

Antes de escribir la inclusión, vuelva a leer la notificación de contenido generado por notificación. Obligatorio, incluso para
páginas cortas. Corrija los errores antes de escribir y registre la corrección en el informe.

- Cada nombre de término, etiqueta o interfaz de usuario del bloque aparece en el cuerpo de la página.
- No hay sinónimo a menos que ambos formularios aparezcan en la página; cada &quot;No confundir&quot; solo hace referencia a
conceptos en esta página.
- Cada valor numérico coincide exactamente con el cuerpo de la página; cada calificador de límite se justifica con el parámetro
redacción de la página; sin calificador inventado.
- No se han importado detalles de glosarios/preguntas frecuentes de otras páginas o conocimientos generales.
- Ningún término impreciso prohibido a menos que sea textualmente en la página; no hay contracciones.

## Lista de comprobación posterior a la generación (puerta 1, continuación)

- [ ]: cada valor numérico existe literalmente / se deriva del cuerpo de la página.
- [ ]: cada límite se calificó correctamente (duro frente a recomendado frente a ninguno); sin valor predeterminado/aumentable
 etiquetado erróneamente como duro.
- [ ] Cada cifra de rendimiento tiene su ámbito.
- [ ]: todos los modos de validación presentes en la página reciben un nombre con términos precisos para la página.
- [ ] Todos los estados del ciclo vital utilizan etiquetas de página exactas.
- [ ] Los sinónimos son equivalentes verdaderos; los contrastes se encuentran en &quot;No confundir&quot;.
- [ ] Sin palabras prohibidas ni contracciones (fuera de las cadenas literales de la IU).
- [ El glosario ] no tiene términos genéricos; FAQ no presenta nada ausente de la página.

La Puerta 1 es la autora del bloque que comprueba su propio trabajo. No **no** reemplaza el
ronda de verificación independiente (puerta 2) en `verification-round.md`.
