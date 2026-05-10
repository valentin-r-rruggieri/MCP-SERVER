# GitHub MCP Server

MCP Server para interactuar con la API de GitHub.

## Tools disponibles

- list_repositories
- create_issue
- edit_file

## Uso

### Pasos para la configuración:

1. **Instalación de dependencias**:
   ```bash
   npm install
   ```

2. **Variables de Entorno**:
   Crea un archivo `.env` en la raíz del proyecto y añade tu token de GitHub:
   ```env
   GITHUB_TOKEN=tu_token_aqui
   ```

3. **Compilación**:
   Compila el código TypeScript a JavaScript:
   ```bash
   npm run build
   ```

4. **Ejecución**:
   Para iniciar el servidor:
   ```bash
   npm start
   ```

### Integración con Antigravity

Para usar este MCP en Antigravity, añade la configuración correspondiente apuntando al archivo `dist/index.js` compilado.
