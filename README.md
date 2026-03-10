# Fundamentos de R para el Análisis Estadístico en Ciencias Sociales

Sitio web del curso, construido con [Quarto](https://quarto.org) y publicado con GitHub Pages.

---

## Estructura del proyecto

```
fundamentos-r-cs/
├── _quarto.yml          # Configuración del sitio
├── styles.css           # Estilos personalizados
├── index.qmd            # Página principal (syllabus)
├── modulos/
│   ├── modulo1.qmd
│   ├── modulo2.qmd
│   ├── modulo3.qmd
│   └── modulo4.qmd
├── practicas/
│   ├── P1.qmd           # Una por sesión
│   ├── P2.qmd
│   └── ...
└── docs/                # Carpeta generada por Quarto (NO editar a mano)
```

---

## Cómo publicar el sitio (primera vez)

### 1. Clonar el repositorio

```bash
git clone https://github.com/TU-ORG/fundamentos-r-cs.git
cd fundamentos-r-cs
```

### 2. Renderizar el sitio

Desde la terminal de RStudio:

```bash
quarto render
```

Esto genera la carpeta `docs/` con el sitio estático.

### 3. Publicar en GitHub Pages

Opción A — Comando directo (más fácil):

```bash
quarto publish gh-pages
```

Opción B — Manual:
1. Ve a tu repo en GitHub → Settings → Pages
2. En "Source" selecciona la rama `main` y la carpeta `/docs`
3. Guarda y espera ~2 minutos

---

## Flujo de trabajo diario

```bash
# 1. Actualizar tu copia local
git pull

# 2. Editar tus archivos .qmd en RStudio

# 3. Renderizar
quarto render

# 4. Subir cambios
git add .
git commit -m "Agrego práctica 3"
git push
```

GitHub Pages actualizará el sitio automáticamente.

---

## Trabajar en colaboración (dos ponentes)

Se recomienda usar una **GitHub Organization**:

1. Crear la org en github.com → New organization
2. Crear el repo dentro de la org
3. Agregar a la co-facilitadora como Admin del repo
4. Cada quien trabaja en su rama y hace Pull Request para revisar antes de publicar

```bash
# Crear una rama para tu módulo
git checkout -b monica/modulo2

# ... editar, guardar, renderizar ...

git add .
git commit -m "Sesión 6 lista"
git push origin monica/modulo2
# Luego hacer Pull Request en GitHub
```

---

## Agregar una nueva práctica

1. Crea el archivo `practicas/P_N_.qmd` copiando la estructura de `P1.qmd`
2. Agrega el link en el módulo correspondiente en `modulos/moduloN.qmd`
3. Renderiza y sube

---

## Requisitos

- R ≥ 4.2
- RStudio (recomendado)
- Quarto CLI (incluido en RStudio ≥ 2022.07)
- Git
