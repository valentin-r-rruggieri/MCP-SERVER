# GitHub MCP Server

MCP Server para interactuar con la API de GitHub.

## Uso

### 1. Configuración de GITHUB_TOKEN
Para que el servidor pueda interactuar con GitHub, necesitás un Token de Acceso Personal (PAT).
1. Andá a [GitHub Settings > Developer settings > Personal access tokens](https://github.com/settings/tokens).
2. Generá un nuevo token (clásico o de grano fino) con permisos para repositorios e issues.
3. Guardá este token de forma segura.

### 2. Instalación de Dependencias
Ejecutá el siguiente comando en la raíz del proyecto:
```bash
npm install
```

### 3. Compilación del Proyecto
Para compilar el código TypeScript a JavaScript:
```bash
npm run build
```

### 4. Uso desde Antigravity
Para integrar este MCP en Antigravity, debés editar tu archivo `mcp_config.json` (generalmente ubicado en `%USERPROFILE%\.gemini\antigravity\mcp_config.json`) y agregar la configuración del servidor:

```json
{
  "mcpServers": {
    "github-mcp": {
      "command": "node",
      "args": ["C:/ruta/a/tu/repo/MCP-SERVER/build/index.js"],
      "env": {
        "GITHUB_TOKEN": "TU_TOKEN_AQUÍ"
      }
    }
  }
}
```
Asegurate de reemplazar `C:/ruta/a/tu/repo/MCP-SERVER/build/index.js` con la ruta absoluta real y `TU_TOKEN_AQUÍ` con tu token generado.
