# GitHub MCP Server

MCP Server para interactuar con la API de GitHub.

## Uso

### 1. Configuración de GITHUB_TOKEN
Para utilizar este servidor, necesitas un Token de Acceso Personal (PAT) de GitHub.
1. Ve a [GitHub Settings > Developer settings > Personal access tokens > Tokens (classic)](https://github.com/settings/tokens).
2. Genera un nuevo token con los permisos necesarios (repo, read:org, etc.).
3. Crea un archivo `.env` en la raíz del proyecto o configura la variable de entorno:
   ```bash
   GITHUB_TOKEN=tu_token_aqui
   ```

### 2. Instalación de dependencias
Ejecuta el siguiente comando para instalar las librerías necesarias:
```bash
npm install
```

### 3. Compilación del proyecto
Para compilar el código TypeScript a JavaScript, usa:
```bash
npm run build
```

### 4. Uso desde Antigravity
Para integrar este MCP Server en Antigravity:
1. Abre la configuración de Antigravity.
2. Agrega una nueva configuración de MCP Server apuntando al archivo compilado:
   - Command: `node`
   - Args: `[path/to/MCP-SERVER/dist/index.js]`
   - Env: `GITHUB_TOKEN=tu_token_aqui`
3. Una vez configurado, Antigravity podrá usar las herramientas de GitHub directamente.
