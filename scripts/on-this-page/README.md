---
source-git-commit: f59dc265b0de732b52e9d26b6ee510733d0d760e
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---
# Herramientas de cuadro &quot;En esta página&quot;

Herramientas para agregar y verificar el cuadro sombreado estándar **&quot;En esta página&quot;** en la parte superior de
Páginas de documentación de AJO. Consulte las especificaciones en `.cursor/rules/on-this-page-box.mdc`.
El despliegue se rastrea en la carpeta épica **DOCAC-14936** (una tarea por carpeta de nivel superior).

## Aspecto de la caja

```text
# Page Title {#anchor}

>[!BEGINSHADEBOX]

**On this page:** <one clear sentence describing the page's purpose>

>[!ENDSHADEBOX]
```

## Flujo de trabajo recomendado (por carpeta/tarea Jira)

Ejecute desde la raíz del repositorio (`journey-optimizer.en/`).

1. **Insertar cuadros** (inicio de una frase de primer borrador desde el contenido principal de cada página)
   `description`). Mecánico, idempotente, nunca toca frontmatter:

   ```bash
   python scripts/on-this-page/add_on_this_page.py help/using/reports --seed-from-description
   ```

   Vista previa primero con `--dry-run`.

2. **Refine la redacción.** La semilla es un punto de partida: edite cada frase para que
se lee como una declaración de propósito (una frase, texto sin formato, inglés estadounidense). **Posible cliente
con el por qué**: indique el resultado/beneficio del lector (&quot;...para que pueda <outcome>&quot;), no
solo una lista de lo que cubre la página. Igualar nombres de características de estilo doméstico (p. ej.,
&quot;Campaña organizada&quot;, &quot;En la aplicación&quot;). Ver `.cursor/rules/on-this-page-box.mdc`. Si usted
omitir `--seed-from-description`, en su lugar se inserta un marcador de posición `{{TODO...}}` y
el validador marcará los que queden.

3. **Validar** antes de abrir el PR:

   ```bash
   python scripts/on-this-page/validate_on_this_page.py help/using/reports --require
   ```

   El código de salida es distinto de cero en cualquier error, por lo que puede bloquear el CI.

## Ámbito/exclusiones

Las páginas de referencia y sintaxis se excluyen de forma predeterminada (partes de ruta de acceso `api-reference`,
`expression`, `functions`). Reemplazar con `--exclude ...` si es necesario.

## Comprobación del progreso en todo el repositorio

```bash
python scripts/on-this-page/validate_on_this_page.py help
```

Sin `--require`, las páginas a las que les falta una casilla se registran como `pending` (no como
error), para que pueda rastrear el progreso del despliegue en toda la guía.
