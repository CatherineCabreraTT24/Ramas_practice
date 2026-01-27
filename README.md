# DS Git Webinar

Este repositorio es un espacio práctico para aprender el flujo básico de **Git** en un proyecto de **Data Science**, trabajando con ramas y Pull Requests como en un entorno real de trabajo.

---

## 🧪 Actividad práctica: Flujo básico de Git en Data Science

### 🎯 Objetivo
En esta actividad vas a trabajar como se hace en un equipo real de Data Science:

- Crear tu propia **rama**
- Modificar archivos del proyecto
- Guardar cambios con **commits**
- Enviar tus cambios mediante un **Pull Request**

> ⚠️ Regla de oro  
> **Nunca trabajamos directamente sobre `main`.**

---

### 🟢 Paso 1: Clonar el repositorio

```bash
git clone <URL_DEL_REPO>
cd ds-git-webinar
```

---

### 🟢 Paso 2: Crear tu rama de trabajo

Crea una rama con tu nombre:

```bash
git checkout -b feature/tu-nombre
```

Ejemplo:
```bash
git checkout -b feature/catherine
```

Puedes verificar en qué rama estás con:

```bash
git branch
```

---

### 🟢 Paso 3: Modificar archivos del proyecto

#### ✏️ Archivo 1: `NOMBRES.md`

En la sección **Participantes**, agrega tu nombre:

```md
- Tu Nombre Aquí
```

---

#### ✏️ Archivo 2: `src/utils.py`

Agrega una nueva función con tu nombre.  
**No borres funciones existentes.**

Ejemplo:

```python
def greet_tunombre():
    return "Hola, este cambio viene desde la rama de Tu Nombre"
```

---

### 🟢 Paso 4: Guardar los cambios con Git

Revisa qué archivos cambiaste:

```bash
git status
```

Agrega los cambios:

```bash
git add .
```

Crea el commit:

```bash
git commit -m "Agrega nombre y función de saludo"
```

> 💡 Un commit debe explicar **qué hiciste**, no describir todo el proceso.

---

### 🟢 Paso 5: Subir tu rama al repositorio remoto

```bash
git push origin feature/tu-nombre
```

---

### 🟢 Paso 6: Crear el Pull Request (PR)

Desde GitHub / GitLab:

- **Base branch:** `main`
- **Compare branch:** `feature/tu-nombre`
- **Título del PR:**  
  `Agrega saludo y participante`
- **Descripción:**  
  Agrego mi nombre al README y una función de saludo en utils.py

Luego, crea el Pull Request 🚀

---
### 🟢 Paso 7: Mantener tu rama actualizada con `main` (después del Pull Request)

Una vez tu Pull Request fue aprobado y mergeado en `main`, es buena práctica actualizar tu rama local para que refleje el estado actual del proyecto.

#### 1️⃣ Cambia a la rama `main`
```bash
git checkout main
```
#### 2️⃣ Trae la versión más reciente del repositorio remoto
```bash
git pull origin main
```

3️⃣ Vuelve a tu rama y tráete los cambios de main
```bash
git checkout feature/tu-nombre
git merge main
```

---

### ✅ Actividad completada

Si llegaste hasta aquí, ya:

- Trabajaste con ramas
- Hiciste commits
- Subiste cambios
- Abriste un Pull Request

👉 Así se trabaja Git en proyectos reales de Data Science.


