# BLOQUE 2: ITERACIÓN Y MEJORAS
Objetivo:
Implementar cambios incrementales, practicando el flujo Git (add, commit, push).

Instrucciones de Cambios:

Cambio 1: Agregar sección "Sobre Mí"

```
# Crear rama para nueva función
git checkout -b feature/sobre-mi
```

- Agregar nueva sección después de hero con: foto personal, párrafo autobiográfico, lista de habilidades técnicas

```
git add .
git commit -m "feat: agregar sección Sobre Mí con foto y habilidades"
git checkout main
git merge feature/sobre-mi
git push
```

Cambio 2: Mejorar tarjetas de proyectos 
```
git checkout -b feature/mejoras-proyectos
```

- Agregar imágenes reales o placeholder específicos
- Añadir badges de tecnologías con colores
- Incluir enlaces "Demo" y "Código"
- Agregar efecto hover en tarjetas

```
git add .
git commit -m "feat: mejorar tarjetas de proyectos con badges y enlaces"
git push origin feature/mejoras-proyectos
git checkout main
git merge feature/mejoras-proyectos
git push
```

Cambio 3: Hacer diseño responsivo

```
git checkout -b feature/responsive
```
- Agregar media queries para tablet (768px)
- Agregar media queries para móvil (480px)
- Menú hamburguesa para móvil
- Grid de 1 columna en móvil

```
git add .
git commit -m "feat: implementar diseño responsivo para móvil y tablet"
git checkout main
git merge feature/responsive
git push
```

Cambio 4: Validación de formulario 

```
git checkout -b feature/validacion-form
```
- Agregar atributos required
- Agregar pattern para email
- Agregar minlength para textarea
- Estilos para estados :invalid y :valid

```
git add .
git commit -m "feat: agregar validación HTML5 al formulario"
git checkout main
git merge feature/validacion-form
git push
```

Cambio 5: Optimizar rendimiento 

```
git checkout -b fix/performance
```
- Optimizar imágenes (comprimir)
- Minificar CSS (opcional)
- Agregar atributos alt a todas las imágenes
- Mejorar accesibilidad (labels, aria-labels)

```
git add .
git commit -m "fix: optimizar imágenes y mejorar accesibilidad"
git checkout main
git merge fix/performance
git push
```

Entregable Bloque 2:
- Mínimo 10 commits adicionales
- Uso de al menos 3 ramas feature
- Historial claro visible con git log --oneline --graph