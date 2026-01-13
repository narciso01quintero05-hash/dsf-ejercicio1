# BLOQUE 3: COLABORACIÓN EN PAREJAS
Objetivo:
Practicar trabajo colaborativo con Git: Fork, Pull Request, revisión de código.

Emparejamiento:
Estudiante A y Estudiante B trabajarán en los repositorios del otro

ESTUDIANTE A - Proponer cambios al proyecto de B
Paso 1: Fork y Clone

```
# 1. Hacer Fork del repo de tu compañero en GitHub (botón Fork)

# 2. Clonar TU fork (no el original)
git clone https://github.com/tu-usuario/portafolio-git-companero.git
cd portafolio-git-companero

# 3. Agregar upstream (repo original del compañero)
git remote add upstream https://github.com/companero/portafolio-git.git

# 4. Verificar remotos
git remote -v
# Deberías ver: origin (tu fork) y upstream (repo original)
```

Paso 2: Crear rama y hacer cambios

```
# Crear rama para tus cambios
git checkout -b feature/mejoras-desde-A

# Implementar cambios asignados (ver abajo)

# Commits frecuentes
git add .
git commit -m "feat: descripción del cambio"
```

Cambios a Implementar por Estudiante A:
1. Agregar animaciones CSS 
    - Transiciones suaves en botones y tarjetas
    - Animación de entrada en hero section
    - Hover effects mejorados
2. Mejorar el footer
    - Agregar columnas: enlaces rápidos, redes sociales, info contacto
    - Iconos reales o FontAwesome
    - Mejor estética

Paso 3: Push a tu Fork

```
# Subir rama a TU fork
git push origin feature/mejoras-desde-A
```

Paso 4: Crear Pull Request

```
# En GitHub:
# 1. Ir a TU fork
# 2. Aparecerá mensaje "Compare & pull request"
# 3. Click en el botón
# 4. Escribir descripción detallada:
#    - Qué cambios hiciste
#    - Por qué son importantes
#    - Capturas de pantalla (opcional)
# 5. Crear Pull Request hacia el repo original del compañero
```

ESTUDIANTE B - Proponer cambios al proyecto de A
Realizar los mismos pasos 1-4 que Estudiante A, pero con estos cambios:

Cambios a Implementar por Estudiante B:
1. Agregar sección de Testimonios
    - Nueva sección entre Proyectos y Contacto
    - 2-3 testimonios falsos
    - Diseño de tarjetas con foto circular, texto y nombre

2. Dark Mode Toggle
    - Botón para cambiar a modo oscuro
    - Variables CSS para colores
    - Guardar preferencia en localStorage (JS básico)

AMBOS ESTUDIANTES - Revisar y Aceptar Pull Requests
Paso 1: Recibir notificación

```
# En GitHub verás notificación de Pull Request
# Revisar en: Tu Repo > Pull Requests
```

Paso 2: Revisar cambios

```
# En GitHub:
# 1. Click en el Pull Request
# 2. Ver pestaña "Files changed"
# 3. Revisar línea por línea
# 4. Dejar comentarios si hay sugerencias
# 5. Aprobar o solicitar cambios
```

Paso 3: Probar cambios localmente (Opcional)

```
# En tu repo original
git fetch origin

# Crear rama temporal para probar
git checkout -b test-pr-companero

# Traer cambios del PR
git pull https://github.com/companero-fork/portafolio-git.git feature/mejoras-desde-A

# Probar en navegador

# Si todo bien, regresar a main
git checkout main
```

Paso 4: Aceptar (Merge) Pull Request

```
# En GitHub:
# 1. En el Pull Request, click "Merge pull request"
# 2. Elegir tipo de merge:
#    - Create a merge commit (recomendado para principiantes)
#    - Squash and merge (combina todos los commits en uno)
#    - Rebase and merge (mantiene historia lineal)
# 3. Click "Confirm merge"
# 4. Opcionalmente eliminar la rama del PR
```

Paso 5: Actualizar tu repo local
```
# Después de hacer merge, actualizar tu repo local
git checkout main
git pull origin main

# Verificar que los cambios están integrados
git log --oneline -5
```

ENTREGA DEL BLOQUE 3
Capturas requeridas:
1. Fork realizado
    - Captura mostrando el fork en tu cuenta de GitHub
2.  Pull Request creado
    - Captura del PR con descripción completa
    - Debe incluir: título descriptivo, descripción detallada, archivos modificados
3. - Revisión de código
    - Captura mostrando comentarios dejados en el PR del compañero
    - Al menos 2-3 comentarios constructivos
4. PR Mergeado
    - Captura del PR aceptado e integrado
    - Debe mostrar el mensaje "Merged" en color morado
5. Commits integrados
    - Captura de git log --oneline --graph mostrando la historia del proyecto con los commits del compañero integrados


CHECKLIST FINAL - BLOQUE 3
Estudiante A:

- Fork del repositorio de Estudiante B
- Clone del fork y configuración de upstream
- Rama feature/mejoras-desde-A creada
- Animaciones CSS implementadas
- Footer mejorado completado
- Commits descriptivos realizados
- Push a fork personal
- Pull Request creado con descripción detallada
- Revisión del PR de Estudiante B completada
- PR de Estudiante B mergeado
- Repositorio local actualizado

Estudiante B:
- Fork del repositorio de Estudiante A
- Clone del fork y configuración de upstream
- Rama feature/mejoras-desde-B creada
- Sección de Testimonios agregada
- Dark Mode Toggle implementado
- localStorage configurado
- Commits descriptivos realizados
- Push a fork personal
- Pull Request creado con descripción detallada
- Revisión del PR de Estudiante A completada
- PR de Estudiante A mergeado
- Repositorio local actualizado

CONSEJOS PARA BUENA COLABORACIÓN
Al revisar código del compañero:
- é constructivo y específico en tus comentarios
- Sugiere mejoras, no solo señales problemas
- Reconoce lo que está bien hecho
- Haz preguntas para entender el razonamiento

Ejemplos de buenos comentarios en PR:

✅ Bueno:

```
"Excelente implementación de las animaciones. 
Sugerencia: podrías agregar `will-change: transform` 
para mejor performance en la animación del hero."
```

✅ Bueno:

```
"El footer se ve muy bien. Considera agregar 
`aria-label` a los iconos de redes sociales 
para mejor accesibilidad."
```

❌ Evitar:

```
"Esto está mal"
"No me gusta"
```

SOLUCIÓN A PROBLEMAS COMUNES
Problema 1: Conflictos al hacer merge

```
# Si hay conflictos:
# 1. GitHub te avisará que no puede hacer auto-merge
# 2. Debes resolver localmente:

git fetch upstream
git checkout main
git merge upstream/main

# Resolver conflictos en los archivos
# Buscar marcas: <<<<<<, ======, >>>>>>

git add .
git commit -m "fix: resolver conflictos de merge"
git push origin main
```

Problema 2: Olvidaste agregar upstream

```
# Verificar remotos actuales
git remote -v

# Si no está upstream:
git remote add upstream https://github.com/companero/portafolio-git.git

# Verificar que se agregó
git remote -v
```

Problema 3: Hiciste cambios en main en lugar de rama

```
# Crear rama con los cambios actuales
git checkout -b feature/mejoras-desde-A

# Volver main al estado anterior
git checkout main
git reset --hard origin/main
```