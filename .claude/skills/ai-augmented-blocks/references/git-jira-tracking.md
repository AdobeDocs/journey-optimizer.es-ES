---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---
# Seguimiento de Git, PR y JIRA

Cómo aterrizar el cambio de forma segura y rastrearlo. Dos reglas firmes del autor:

1. **Preguntar antes de abrir una PR.** Genere y verifique el bloque independientemente, pero solo abra una extracción
solicitud si el autor dice que sí.
2. **No combinar nunca.** Estas relaciones públicas existen para revisión en humanos. La combinación siempre es decisión del autor.

## Barrido estructural (ejecutar antes de confirmar)

Para cada página procesada en la carpeta:

```bash
cd <repo>
for p in <page1> <page2> ...; do
  f="help/_includes/do-not-localize/<folder>/ai-augmented-$p.md"
  inc="help/using/<folder>/$p.md"
  [ -f "$f" ] || echo "MISSING BLOCK: $f"
  grep -q '^# AI Knowledge Reference' "$f"            || echo "$p: missing H1"
  grep -q '^+++ AI Knowledge Reference' "$f"          || echo "$p: missing accordion open"
  grep -q 'This section contains structured knowledge' "$f" || echo "$p: missing opening para 1"
  grep -q 'ai-section-version' "$f"                   || echo "$p: missing sync comment"
  grep -nEi "\b(isn't|aren't|don't|doesn't|didn't|can't|won't|wouldn't|couldn't|shouldn't|it's|we've|we're|you're|they're|that's|there's|haven't|hasn't|wasn't|weren't)\b" "$f" \
    | grep -vi 'UICONTROL' && echo "  ^ $p contraction"
  grep -q "do-not-localize/<folder>/ai-augmented-$p.md" "$inc" || echo "$p: MISSING include in page"
done
echo "=== sweep done ==="
git status --short
```

Cualquier línea impresa (que no sea &quot;barrido realizado&quot; y la lista `git status`) es un defecto que se debe corregir antes de
comprometiéndose.

## Rama y confirmación (nunca confirmación en principal)

```bash
git checkout main -q && git pull -q origin main
git checkout -q -b DOCAC-<key> origin/main    # branch name = the JIRA task key
# ... generate + verify + sweep ...
git add help/_includes/do-not-localize/<folder>/ help/using/<folder>/*.md
git commit -q -m "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)

<one-line what + the verification result>

Co-Authored-By: Claude <model> <noreply@anthropic.com>"
```

**Verifique que la confirmación aterrizó en la rama, no en`main`** (un arma conocida, si cambió a
`main` para inspeccionar páginas, un compromiso posterior puede aterrizar allí):

```bash
git rev-parse --abbrev-ref HEAD                    # must print DOCAC-<key>
git rev-list --left-right --count origin/main...DOCAC-<key>   # must show  0<TAB>1
```

Si una confirmación aterrizó accidentalmente en `main`: `git branch -f DOCAC-<key> <sha>` para señalar la rama
en ella, `git checkout DOCAC-<key>`, luego `git branch -f main origin/main` para restablecer el main local.
`origin/main` nunca se vio afectado por un error local.

Push: `git push -u origin DOCAC-<key>` (usar `--force-with-lease` si la rama ya existe)
remotamente en una confirmación anterior).

## Pregunte por el PR

Pregunte claramente al autor, por ejemplo: *&quot;Bloques generados y verificados para `<folder>`. ¿Lo desea?
¿Desea que abra una PR para revisión?&quot;* Solo si es así:

```bash
gh pr create --base main --head DOCAC-<key> \
  --title "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)" \
  --body-file <pr-body>.md
```

El cuerpo de PR termina con la línea de atribución requerida
(`🤖 Generated with [Claude Code](https://claude.com/claude-code)`). **No combinar** — deje
PR abierta para revisión.

## Seguimiento JIRA

Rastrear cada cambio en una tarea DOCAC (épica de despliegue: `DOCAC-15582`). Busque o cree la carpeta de
tarea y, a continuación:

1. **Comentario** con lo que cambió y el resultado de la verificación (páginas cubiertas/omitidas, verificador)
limpio/corregido, cualquier llamada grave o predeterminada notable). Incluya el vínculo PR si se ha abierto uno.
2. **Establecer la versión de corrección** (este programa usó `AJO26.9`).
3. **Transición** nueva → en curso → resuelta (resolución &quot;fija&quot;), según el flujo de trabajo. En este
proyecto los id de transición eran `4` (progreso de inicio) y después `5` (resolver, con resolución)
   `{"name":"Fixed"}`); una tarea que aún se encuentra en &quot;Nuevo&quot; debe iniciarse antes de que pueda resolverse.

Usar las herramientas JIRA MCP corporativas (`add_jira_comment`, `update_jira_issue` para `fixVersions`,
`bulk_transition_jira_issues`) o la IU de JIRA. Si no tiene acceso a JIRA, dé este paso a
alguien que lo tenga y anótelo en su informe.

## Una carpeta = una rama = una tarea

No mezcle carpetas no relacionadas en una sola rama o PR. Una nueva página añadida más tarde es su propia página pequeña
puede cambiar (modo CREATE) y compartir la tarea de la carpeta u obtener la suya propia, como prefiera su equipo.
