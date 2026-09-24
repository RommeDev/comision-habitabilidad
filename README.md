<!-- STREAMING_CHUNK:Configurando la estructura del repositorio y descripción general... -->
# Comisión Presidencial para la Evaluación de la Habitabilidad de Infraestructuras

Portal web informativo oficial y repositorio técnico de instrumentos de campo desarrollado para la **Comisión Presidencial para la Evaluación de la Habitabilidad de Infraestructuras** (República Bolivariana de Venezuela), creada con motivo de la contingencia sísmica del 24 de junio.

Este sitio web permite a inspectores, instituciones de gestión de riesgos y a la ciudadanía en general consultar la metodología técnica estandarizada, la matriz de riesgo por etiquetas (Verde, Amarilla y Roja), descargar la documentación oficial y acceder a los módulos de la plataforma digital **HABITABLE**.

---

<!-- STREAMING_CHUNK:Detallando el árbol de archivos y requerimientos de recursos... -->
## Estructura del Repositorio

Para que la página web funcione al 100% y todas las imágenes y enlaces de descarga local operen correctamente, la estructura de carpetas en tu repositorio debe ser la siguiente:

```text
comision-habitabilidad/
├── index.html                                                              # Landing page principal (todo en 1 archivo)
├── logo-comision2.png                                                      # Logotipo oficial del encabezado
├── MANUAL DE USO _Habitable - Modulo Inspector.pdf                         # Documento de descarga 1
├── ANTECEDENTE APLICACION_Coronel et al (2024). App de Eval. Rapida de Daños CONPATVE2024-054-R050.pdf # Documento 2
├── METODOLOGIA_Lopez et al (2023).pdf                                      # Documento de descarga 3
├── PLANILLA EN FISICO_Instrumento de Inspección - Planilla y Manual de Campo- V.8.pdf # Documento 4
└── README.md                                                               # Documentación del proyecto
```

> **Nota importante sobre los nombres de archivo:** Los nombres de los documentos PDF y de la imagen `logo-comision2.png` deben coincidir exactamente como están listados arriba (respetando espacios y mayúsculas) para que los botones de descarga de `index.html` los reconozcan inmediatamente.

---

<!-- STREAMING_CHUNK:Explicando los comandos de Git para inicialización y despliegue... -->
## Guía Rápida: Cómo Subir el Proyecto a GitHub

### Paso 1. Preparar la carpeta local
1. Crea una carpeta en tu computadora llamada `comision-habitabilidad`.
2. Coloca dentro de esa carpeta el archivo `index.html`, la imagen `logo-comision2.png`, los 4 archivos PDF y este `README.md`.

### Paso 2. Inicializar el repositorio Git
Abre tu terminal (Git Bash, Terminal o PowerShell) dentro de esa carpeta y ejecuta:

```bash
# Inicializar repositorio local
git init

# Agregar todos los archivos al seguimiento de Git
git add .

# Crear el primer commit
git commit -m "feat: landing page oficial comision presidencial habitabilidad v1.0"
```

### Paso 3. Crear el repositorio en GitHub y vincular
1. Ingresa a tu cuenta en [GitHub.com](https://github.com/) y haz clic en **New Repository**.
2. Nombre del repositorio sugerido: `comision-habitabilidad` (puedes elegir público o privado).
3. **No** marques la opción de inicializar con README ni .gitignore (ya los tienes localmente).
4. Copia los comandos que te proporciona GitHub y ejecútalos en tu terminal:

```bash
# Renombrar rama a main
git branch -M main

# Vincular tu repositorio remoto (reemplaza TU_USUARIO por tu nombre de usuario en GitHub)
git remote add origin https://github.com/TU_USUARIO/comision-habitabilidad.git

# Subir los archivos
git push -u origin main
```

---

<!-- STREAMING_CHUNK:Detallando la publicación en GitHub Pages y notas técnicas... -->
## Cómo Publicar la Página Web con GitHub Pages (Hosting Gratuito)

GitHub ofrece alojamiento web gratuito sin necesidad de configurar servidores:

1. En tu repositorio en GitHub, ve a la pestaña **Settings** (Configuración).
2. En el menú lateral izquierdo, haz clic en **Pages**.
3. En la sección **Build and deployment**:
   - **Source**: Selecciona `Deploy from a branch`.
   - **Branch**: Selecciona `main` y la carpeta `/ (root)`.
4. Haz clic en **Save** (Guardar).
5. Espera aproximadamente 1 minuto. GitHub te indicará el enlace público de tu página web, por ejemplo:
   ```text
   https://TU_USUARIO.github.io/comision-habitabilidad/
   ```

---

## Características Técnicas de la Landing Page

- **Arquitectura Standalone (Single-File):** Toda la estructura semántica, estilos de interfaz y lógica de interacción (búsqueda en tiempo real de documentos, modales y menú móvil) se encuentran consolidados en `index.html`.
- **Framework de Estilos:** Tailwind CSS mediante CDN oficial (no requiere Node.js, Webpack ni proceso de compilación previo).
- **Tipografías:** Integración de fuentes Google Fonts (*Inter* y *Montserrat*).
- **Diseño Adaptativo:** 100% responsivo para teléfonos móviles, tablets y monitores de escritorio.
- **Seguridad y Enlaces Oficiales:** Conexión directa a los módulos gubernamentales de HABITABLE (`/c`, `/`, `/admin/login`, `/reparaciones/` y `/busqueda`).

---

## Licencia y Uso Institucional

Desarrollado para la Comisión Presidencial para la Evaluación de la Habitabilidad de Infraestructuras. Uso oficial e institucional para la gestión y mitigación del riesgo sísmico.