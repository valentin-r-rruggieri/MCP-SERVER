# GitHub MCP Server

MCP Server para interactuar con la API de GitHub.

## Uso

### 1. Configuración de GITHUB_TOKEN
Crea un archivo `.env` en la raíz del proyecto (puedes usar `.env.example` como base) y agrega tu token de acceso personal de GitHub:
```env
GITHUB_TOKEN=tu_token_aqui
```

### 2. Instalación de dependencias
Instala los paquetes necesarios ejecutando:
```bash
npm install
```

### 3. Compilación del proyecto
Para compilar el código TypeScript a JavaScript:
```bash
npm run build
```

### 4. Uso desde Antigravity
Para integrar este servidor en Antigravity, añade la configuración correspondiente en tu archivo de configuración de MCP apuntando al archivo compilado:

```json
{
  "mcpServers": {
    "github-mcp": {
      "command": "node",
      "args": ["PATH_TO_PROJECT/dist/index.js"],
      "env": {
        "GITHUB_TOKEN": "YOUR_GITHUB_TOKEN"
      }
    }
  }
}
```
