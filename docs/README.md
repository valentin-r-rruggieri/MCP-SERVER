# GitHub MCP Server

MCP Server para interactuar con la API de GitHub.

## Tools disponibles

- list_repositories
- create_issue
- edit_file

## Uso

### 1. Configuración de credenciales
Crea un archivo `.env` en la raíz del proyecto y añade tu token de acceso personal de GitHub:

```env
GITHUB_TOKEN=tu_token_aqui
```

### 2. Instalación y Construcción
Instala las dependencias y compila el proyecto:

```bash
npm install
npm run build
```

### 3. Configuración en Antigravity / Claude Desktop
Para usar este servidor, añade la siguiente configuración a tu archivo de configuración de MCP:

```json
{
  "mcpServers": {
    "github": {
      "command": "node",
      "args": ["C:/ruta/a/tu/proyecto/dist/index.js"],
      "env": {
        "GITHUB_TOKEN": "tu_token_aqui"
      }
    }
  }
}
```
