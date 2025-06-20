# Importar Configuración de VSCode

Este manual explica cómo importar toda mi configuración de Visual Studio Code, en tu máquina incluyendo extensiones, perfiles de usuario, atajos de teclado y snippets.

---

## ✅ Método 1: Usando la Extensión **Settings Sync** (oficial de Microsoft)

1. **Instala la extensión:**
   - Abre la barra lateral de extensiones (`Ctrl+Shift+X`)
   - Busca: `Settings Sync` (autor: *Microsoft* o *Shan Khan*)
   - Haz clic en **Instalar**

2. **Inicia sesión:**
   - Al activar la extensión, inicia sesión con GitHub o Microsoft para sincronizar.

3. **Sincroniza tu configuración:**
   - Abre la paleta de comandos (`Ctrl+Shift+P`)
   - Escribe: `Sync: Turn On`
   - Esto sincroniza automáticamente:
     - `settings.json`
     - `keybindings.json`
     - Extensiones instaladas
     - Snippets creados
     - Configuración del espacio de trabajo

4. **Recuperación en otro equipo:**
   - En el nuevo VS Code, instala la misma extensión e inicia sesión
   - Usa el comando `Sync: Turn On` para importar tu configuración

---

## ✅ Método 2: Importación Manual

### 1. Importar configuración

Para esto debes descargar el archivo comprimido de está en el repositorio con nombre `User.zip`.

1. Descomprima el archivo descargado

2. Peguela la carpeta entera (sin renombrarla) en la siguiente ruta

- **Windows:**  
  `C:\Users\<TuUsuarioLocal>\AppData\Roaming\Code\`

- **Linux:**  
  `~/.config/Code/`

3. Si usa Linux debe renombrar los dos archivos terminados en `-for-linux.json` y eliminar los otros dos

4. Por último instale las tres fuentes para una mejor apariencia

---

### 2. Instalar las extensiones

Ubicado dentro del path `C:\Users\<TuUsuarioLocal>\AppData\Roaming\Code\User` en su terminal debe ejecutar:

```bash
  cat extensiones.txt | xargs -n 1 code --install-extension
```