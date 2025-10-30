---
source-git-commit: 08eaa7ae974c134ea2e920a1fa854dcf6a971e18
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

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

3. El agente hará lo siguiente automáticamente:
   - Prueba del acceso SSH y HTTPS
   - Utilizar el método de trabajo
   - Le guiará por la configuración si es necesario
4. ¡Listo! ✨

**Nota:** El agente detecta automáticamente si tiene acceso SSH o HTTPS a `git.corp.adobe.com` y usa el método apropiado. Si ninguno de los dos funciona, proporciona una configuración guiada.

### Opción 2: usar terminal

1. Abra el terminal en la raíz del repositorio
2. Ejecutar:

   ```bash
   ./setup-agents.sh
   ```

   La secuencia de comandos:
   - Prueba del acceso SSH y HTTPS
   - Utilizar el método de trabajo
   - Mostrar instrucciones de configuración si es necesario

   O manualmente (si sabe que su Git está configurado):

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

Consulte [AGENTS.md](AGENTS.md) para obtener una lista completa de los agentes disponibles.

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
your-repo/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  └── your-content/
```

El submódulo señala a:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Esto garantiza que todos utilicen los mismos agentes actualizados.

## Para responsables

### Adición a un nuevo repositorio

1. Añada el submódulo:

   ```bash
   git submodule add https://git.corp.adobe.com/AdobeDocs/CursorAgents.git .cursor-agents
   ```

2. Copiar archivos de instalación:
   - `setup-agents.sh`
   - `setup-agent.md` (colocar en la raíz, no en el submódulo)
   - `INSTALL.md`

3. Compromiso:

   ```bash
   git add .gitmodules .cursor-agents setup-agents.sh
   git commit -m "Add Cursor Agents submodule"
   ```

### Actualización del repositorio central

Los cambios en los agentes deben realizarse en:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Todos los repositorios recibirán actualizaciones mediante `git submodule update --remote`.

&#x200B;---

**¿Necesita ayuda?** Póngase en contacto con el jefe del equipo de documentación o compruebe la wiki interna.
