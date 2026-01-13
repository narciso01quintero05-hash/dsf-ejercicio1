# BLOQUE 1: REPLICAR DISEÑO
Objetivo:
Igualar el diseño modificando el HTML y CSS base, y subir a GitHub.

Instrucciones:
Paso 1: Configurar Git y GitHub

```
# 1. Crear carpeta del proyecto
mkdir portafolio-git
cd portafolio-git

# 2. Copiar archivos index.html y styles.css base

# 3. Inicializar Git
git init

# 4. Crear .gitignore
echo ".DS_Store" > .gitignore

# 5. Hacer primer commit
git add .
git commit -m "Initial commit: Estructura base HTML y CSS"

# 6. Crear repositorio en GitHub (nombre: portafolio-git)

# 7. Conectar con GitHub
git remote add origin https://github.com/tu-usuario/portafolio-git.git
git branch -M main
git push -u origin main
```

Paso 2: Modificar HTML

- Cambiar el contenido para que coincida con la imagen generada
- Agregar nombre del estudiante en lugar de "Mi Portafolio"
- Actualizar textos de hero section
- Agregar imágenes placeholder a las tarjetas de proyectos
- Incluir iconos de redes sociales en footer

Paso 3: Modificar CSS
Actualizar estilos para lograr:
- Colores según la imagen generada
- Gradientes en hero section
- Sombras en tarjetas (box-shadow)
- Botones con hover effects
- Grid responsivo de 3 columnas en proyectos
- Bordes redondeados (border-radius)
- Espaciado mejorado

Paso 4: Commits Frecuentes

```
# Después de cada cambio importante:
git add .
git commit -m "Descripción del cambio"
git push
```

Entregable Bloque 1:
- Sitio que se vea igual o muy similar a la imagen generada
- Mínimo 5 commits documentados
- Repositorio público en GitHub con URL