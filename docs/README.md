# GitHub MCP Server

Este servidor permite interactuar con la API de GitHub utilizando el Model Context Protocol (MCP). Facilita la gestión de repositorios, issues y archivos directamente desde asistentes de IA compatibles como Antigravity.

## Características

- **Listar Repositorios**: Visualiza todos tus repositorios de GitHub.
- **Crear Issues**: Informa errores o solicita nuevas funcionalidades.
- **Editar Archivos**: Modifica o crea archivos directamente en tus repositorios.

## Requisitos Previos

- [Node.js](https://nodejs.org/) (v18 o superior)
- Un [Personal Access Token de GitHub](https://github.com/settings/tokens) con permisos suficientes (`repo`).

## Uso

Para configurar y utilizar este servidor MCP, seguí estos pasos detallados:

### 1. Configuración de GITHUB_TOKEN
Para que el servidor pueda interactuar con tu cuenta de GitHub, necesitás un Token de Acceso Personal (PAT).
1. Generá un token en [GitHub Settings](https://github.com/settings/tokens).
2. Crea un archivo `.env` en la raíz del proyecto basándote en `.env.example`:
   ```bash
   cp .env.example .env
   ```
3. Agregá tu token al archivo `.env`:
   ```env
   GITHUB_TOKEN=tu_personal_access_token_aqui
   ```

### 2. Instalación de Dependencias
Instalá los paquetes necesarios ejecutando:
```bash
npm install
```

### 3. Compilación del Proyecto
Compilá el código fuente de TypeScript a JavaScript:
```bash
npm run build
```

### 4. Uso desde Antigravity
Para integrar este servidor en Antigravity, agregalo a tu configuración de MCP (`mcp_config.json`) con la siguiente estructura:

```json
{
  "mcpServers": {
    "github-mcp": {
      "command": "node",
      "args": ["C:/ruta/a/tu/proyecto/MCP-SERVER/dist/index.js"],
      "env": {
        "GITHUB_TOKEN": "tu_token_aca"
      }
    }
  }
}
```
> **Importante**: Asegurate de que la ruta en `args` sea la ruta absoluta correcta hacia el archivo `dist/index.js` en tu sistema.

## Tools Disponibles

- `list_repositories`: Lista todos los repositorios accesibles por el token.
- `create_issue`: Permite crear un nuevo issue en un repositorio.
- `edit_file`: Permite editar o crear contenido en archivos de un repositorio.
