---
source-git-commit: 80d5f294491b35dcdbfe4976cb3ec4cf14384858
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---
# 🚀 instalando agentes de cursor

Los agentes de cursor son herramientas compartidas que le ayudan a crear y mantener la documentación de forma más eficaz.

## Configuración por primera vez

Solo necesita hacer esto **una vez** por repositorio.

### Opción 1: Usar El Cursor (Recomendado ⭐)

1. Abrir chat de cursor (`Cmd+L` o `Ctrl+L`)
2. Tipo:

   ```
   @setup-agents
   ```

3. Siga las indicaciones
4. ¡Listo! ✨

### Opción 2: usar terminal

1. Abra el terminal en la raíz del repositorio
2. Ejecutar:

   ```bash
   ./setup-agents.sh
   ```

   O manualmente:

   ```bash
   git submodule update --init --recursive
   ```

3. ¡Listo! ✨

## Verificación

Después del programa de instalación, compruebe la instalación:

```bash
ls .cursor-agents/agents/
```

Debería ver lo siguiente:
- `draft-page-generator.md`
- `fix-grammar.md`
- etc.

## Uso

Una vez instalado, puede utilizar agentes en Cursor:

```
@draft-page      # Generate a new documentation page
@fix-grammar     # Fix grammar in current file
```

Consulte `.cursor-agents/AGENTS.md` para obtener una lista completa de los agentes disponibles.

## Actualizando agentes

Para obtener la última versión de todos los agentes:

### Opción 1: usar el cursor

```
@update-agents
```

### Opción 2: usar terminal

```bash
git submodule update --remote
```

## Resolución de problemas

### Error &quot;Agente no encontrado&quot;

Si ve este error, los agentes aún no están instalados. Ejecutar:

```
@setup-agents
```

### El submódulo está vacío

Si `.cursor-agents/` existe pero está vacío:

```bash
git submodule update --init --recursive --remote
```

### Permiso denegado

Asegúrese de que el script de configuración sea ejecutable:

```bash
chmod +x setup-agents.sh
```

### Problemas de red/VPN

- Asegúrese de que está conectado a la VPN de Adobe
- Comprobar conectividad de red
- Verificar el acceso de Git:

  ```bash
  git ls-remote https://git.corp.adobe.com/AdobeDocs/CursorAgents
  ```

## Cómo funciona

Los agentes de cursor se distribuyen como **submódulo git**:

```
journey-optimizer.en/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  ├── setup-agent.md           ← Bootstrap agent
  └── help/                    ← Your documentation
```

El submódulo señala a:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Esto garantiza que todos utilicen los mismos agentes actualizados.

**¿Necesita ayuda?** Póngase en contacto con el jefe del equipo de documentación o compruebe la wiki interna.

