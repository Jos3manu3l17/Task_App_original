# PROYECTO BASE: Task App - Software Factory SENA

**Metodología:** *"Del Requerimiento al Producto"*

Este repositorio constituye la base técnica y administrativa para el desarrollo del proyecto TaskApp. No es solo un contenedor de código, es una simulación de un entorno profesional donde se aplican estándares de calidad, gestión ágil y flujos de trabajo colaborativos reales mediante GitHub.

---

## INTRODUCCIÓN Y PROPÓSITO

El objetivo de este proyecto es desarrollar una aplicación web de gestión de tareas, priorizando:

- Arquitectura limpia  
- Código organizado y escalable  
- Trazabilidad total del trabajo colaborativo  

### El "Por qué" (Justificación)

Dominar el ciclo de vida del software es tan importante como programar. Esta metodología alinea las habilidades técnicas con las exigencias de la industria, garantizando que cada cambio realizado tenga un propósito claro y verificable mediante Issues, Pull Requests, Milestones y Kanban.
---

## CENTRO DE DOCUMENTACIÓN (WIKI DEL PROYECTO)

Antes de escribir código, se revisaron las guías ubicadas en la carpeta docs/ del repositorio:

### Nivel 1. Sistema  
**Ubicación:** `docs/01-guia-sistema/`  
- Manuales técnicos: creación de Issues y Milestones  

### Nivel 2. Metodología  
**Ubicación:** `docs/02-guia-metodologia/`  
- Reglas para pull request 

### Nivel 3. Formatos  
**Ubicación:** `docs/03-formatos-maestros/`  
- Plantillas oficiales de documentos  

---

## ROLES DE LA CÉLULA ÁGIL

### Líder (Arquitecto)

--- Jose Manuel Carreño Puerta 

- **Responsable de:** 
- **Tareas en GitHub:**
  - Protección de ramas  
  - Gestión de Milestones  
  - Revisión y aprobación de Pull Requests  

---

### Desarrollador (Albañil)

--- Camilo Andres Vanegas 
--- Yilver Duvan Garcia

- **Responsables de:** Construcción de módulos y lógica  
- **Tareas en GitHub:**
  - Desarrollo en ramas `feat/`  
  - Reporte de avances  
  - Solicitud de revisión por PR  

---

### El "Por qué"

La división de roles evita duplicidad de tareas y establece una jerarquía clara de responsabilidad (segregación de funciones), esencial en equipos de alto rendimiento.

---

## CONFIGURACIÓN DEL ENTORNO (LOCAL)

Para estandarizar el desarrollo y evitar errores de compatibilidad, sigue estos pasos en tu terminal:

```bash
# Paso 1. Clonar el repositorio
git clone [URL-del-repositorio-grupal]

# Paso 2. Instalar dependencias
npm install

# Paso 3. Ejecutar el servidor local
npm run dev
```

### El "por que"

Estandarizar el entorno asegura la paridad entre las máquinas de todos los colaboradores, erradicando para siempre la excusa de "en mi máquina sí funciona".

## ARQUITECTURA Y ESTRUCTURA DEL PROYECTO

Mantenemos una organización modular para facilitar el mantenimiento:

```
/
.
├── .github/
│   └── ISSUE_TEMPLATE/
│       ├── bug_report.md
│       └── feature_request.md
│   └── pull_request_template.md
├── Contenido/
│   ├── agrear-tarea.html
│   ├── agregarTarea.css
│   ├── dashboard.html
│   ├── index.html
│   ├── Logo de Task App con lista de verificación.p...
│   ├── registro.css
│   ├── registro.html
│   ├── sin-tarea.html
│   ├── Styles-login.css
│   ├── Styles.css
│   ├── tarea-completada.html
│   └── tarea-pendiente.html
├── docs/
│   ├── 01-guia-sistema/
│   │   ├── blindaje-ramas.md
│   │   ├── creacion_milestones.md
│   │   ├── creacion_issues.md
│   │   └── tablero-kanban.md
│   ├── 02-guia-metodologia/
│   │   ├── conventional-commits.md
│   │   ├── gitflow.md
│   │   ├── GUIA_ISSUES.md
│   │   └── GUIA_PULL_REQUEST.md
│   └── 03-formatos-maestros/
│       └── ISSUE_TEMPLATE/
│           ├── bug_report.md
│           ├── feature_request.md
│           └── pull_request_template.md
                README.md
                TEAM_AGREEMENT.md

```

## VISTAS DE LA APLICACION

La aplicación cuenta con múltiples vistas HTML como:

Registro de usuario
Inicio de sesión (Login)
Lista de tareas
Crear tarea

## Durante el proyecto se aplicó el siguiente flujo

Sincronización con develop
Creación de rama feat/nombre-tarea
Desarrollo aislado
Pull Request con Closes #ID
Revisión obligatoria por el líder
Merge a develop
Release final de develop hacia main

## METODOLOGÍA DE TRABAJO (GITFLOW PROFESIONAL)

El flujo de trabajo es el corazón de nuestra colaboración.  
Está estrictamente prohibido hacer commits directos sobre las ramas `main` o `develop`.

---

### Paso 1. Sincronizar
Trae los últimos cambios aprobados del equipo:

```bash
git checkout develop
git pull origin develop
```
### Paso 2. Rama de Tarea

Crea un espacio aislado para tu requerimiento:

```bash
git checkout -b feat/nombre-tarea
```

### Paso 3. Desarrollo

Escribe código limpio y realiza commits descriptivos.

### Paso 4. Sincronización Final

Antes de entregar, integra los cambios recientes del equipo para resolver conflictos en tu máquina:

```bash
git checkout develop
git pull origin develop
git checkout feat/nombre-tarea
git merge develop
```

### Paso 5. Solicitud de PR

Sube tu rama y solicita la revisión técnica en GitHub:

```bash
git push origin feat/nombre-tarea
```

### El "Por qué"

Este flujo protege la estabilidad del código base. Si tu código falla, solo falla en tu rama, manteniendo el proyecto principal intacto y siempre funcional.

## BLINDAJE DE RAMAS Y SEGURIDAD

Para garantizar la integridad del producto, el repositorio cuenta con candados de seguridad:

main representa producción
develop integración del equipo
Prohibidos commits directos
Revisión obligatoria por PR

- **Restricción de Merge:**
  - El botón de integración está bloqueado para los desarrolladores  
  - Solo el Líder tiene el permiso final tras la revisión  

---

## ESTÁNDARES DE CALIDAD (DEFINITION OF DONE)

Antes de aprobar un PR se verificaba:

Diseño responsive
Código limpio sin pruebas innecesarias
Rama sincronizada sin conflictos
Issue vinculado mediante Closes #ID 

### El "Por qué"

Un control de calidad preventivo reduce la deuda técnica (errores acumulados) y automatiza el proceso administrativo.

---

## CRITERIOS DE ENTREGA Y EVALUACIÓN

La fase del proyecto se considera exitosa, terminada y lista para calificación únicamente cuando:

- El **Milestone** en GitHub marca el **100%** de progreso  
- Todas las **Issues** del hito están cerradas y vinculadas a un PR aprobado  
- El proyecto está desplegado en vivo (ej. Vercel, GitHub Pages) y funciona sin errores  

### El "Por qué"

En la industria, el software que no está publicado no existe. Esto vincula el resultado técnico con la gestión profesional.

---

## CÓMO EJECUTAR EL PROYECTO

Clonar el repositorio:
git clone URL_DEL_REPO

Abrir la carpeta:
Abrir la carpeta

cd Task_App_original


## CRITERIOS DE ENTREGA CUMPLIDOS

Milestones al 100%
Issues cerradas y vinculadas a PR
Proyecto funcional en la rama main
Flujo Git profesional aplicado correctamente


## DIRECCIÓN DEL PROYECTO

- **Instructor:** Jhon Becerra
- **Institución:** Servicio Nacional de Aprendizaje (SENA)  
- **Centro:** Centro cndustrial de mantenimineto integral   
- **Programa:** Análisis y Desarrollo de Software  

---

Este repositorio es propiedad del equipo de desarrollo y se rige por las políticas de formación profesional integral del SENA.