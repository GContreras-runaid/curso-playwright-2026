# 🎭 Instalación mínima - Proyecto desde cero

¡Bienvenido al curso de Automation con Playwright!  
En esta guía crearás tu proyecto de Playwright desde cero, sin necesidad de clonar ningún repositorio.

---

## 🚀 Requisitos previos

Antes de empezar, asegúrate de tener instalado en tu computadora:

| Requisito | Windows |
|-----------|---------|
| **Sistema** | Windows 10+ |
| **Node.js** | https://nodejs.org/ (v18+) |
| **Git** | https://git-scm.com/ |
| **Editor** | VS Code recomendado |

---

# 🛠️ Guía de Instalación

---

# 🪟 Windows

## 1. Crear la carpeta del proyecto

Abrir PowerShell o CMD y ejecutar:

```bash
mkdir curso-playwright-2026
cd curso-playwright-2026
```

---

## 2. Inicializar proyecto Node.js

Esto creará el archivo `package.json`.

```bash
npm init -y
```

---

## 3. Crear el proyecto Playwright

Este comando instalará Playwright, descargará los navegadores y creará la estructura base del proyecto.

```bash
npm init playwright@latest
```

Durante la instalación se recomienda:

| Pregunta | Respuesta recomendada |
|---|---|
| TypeScript or JavaScript? | JavaScript |
| Where to put your tests? | tests |
| Add GitHub Actions? | No |
| Install Playwright browsers? | Yes |

---

## 4. Configurar PowerShell (solo si aparece error)

Si Windows bloquea scripts, abrir PowerShell como usuario normal y ejecutar:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

---

## 5. Verificar instalación

Ejecutar los tests de ejemplo:

```bash
npx playwright test
```

---

# 📂 Estructura del Proyecto

Luego de la instalación tendrás algo similar a esto:

```plaintext
curso-playwright-2026/
├── tests/
│   └── example.spec.js
├── playwright.config.js
├── package.json
├── package-lock.json
└── node_modules/
```

---

# 🏃‍♂️ Cómo ejecutar las pruebas

| Acción | Comando |
|--------|---------|
| Correr todos los tests | `npx playwright test` |
| Tests de un archivo | `npx playwright test tests/example.spec.js` |
| Modo visual (headed) | `npx playwright test --headed` |
| Modo interactivo UI | `npx playwright test --ui` |
| Solo en Chromium | `npx playwright test --project=chromium` |
| Ver reporte HTML | `npx playwright show-report` |
| Generar código automáticamente | `npx playwright codegen` |

---

# 🔧 Solución de problemas comunes

## Error de ejecución de scripts

Ejecutar:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

## Node no reconocido

Cerrar y volver a abrir la terminal.

---

# 📚 Recursos adicionales

- https://playwright.dev/
- https://playwright.dev/docs/intro
- https://nodejs.org/