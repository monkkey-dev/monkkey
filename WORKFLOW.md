# 🚀 RAGE:MP Server – Guía de trabajo con Git

Este repositorio contiene el servidor de RAGE:MP.
Para evitar conflictos y trabajar en equipo de forma ordenada, seguimos este flujo de Git.

--------------------------------------------------

🧠 REGLAS BÁSICAS (OBLIGATORIAS)

- Nunca trabajar directamente en main
- Una rama por feature o fix
- Pull Request obligatorio
- Commits claros (feat:, fix:, etc.)
- main siempre debe funcionar

--------------------------------------------------

🌿 RAMAS

- main → Rama estable (producción)
- feat/* → Nuevas funcionalidades
- fix/* → Corrección de bugs
- refactor/* → Limpieza o cambios internos

Ejemplos:
- feat/login-system
- fix/player-spawn
- refactor/auth-module

--------------------------------------------------

👥 FLUJO DE TRABAJO DEL EQUIPO

1) Clonar el repositorio (una vez)

```git clone https://github.com/ORG/ragemp-server.git```

```cd ragemp-server```

--------------------------------------------------

2) Crear una rama para tu tarea

```git checkout -b feat/nombre-de-la-feature```

--------------------------------------------------

3) Programar y hacer commits

```git add .```
```git commit -m "feat: add login system"```

Commits pequeños y claros.

--------------------------------------------------

4) Actualizar tu rama antes de subir cambios

```git fetch origin```
```git rebase origin/main```

Si hay conflictos:
- Resolverlos manualmente
- Continuar con:
```git rebase --continue```

--------------------------------------------------

5) Subir tu rama a GitHub

```git push origin feat/nombre-de-la-feature```

--------------------------------------------------

6) Crear Pull Request (OBLIGATORIO)

En GitHub:
- Base: main
- Compare: tu rama
- Describir qué hace el cambio
- Otro programador debe revisarlo

Reglas:
- No te apruebes tu propio PR
- Mínimo 1 aprobación

--------------------------------------------------

7) Merge a main

Opciones recomendadas:
- Squash & merge (preferido)
- Rebase & merge

Evitar merges desordenados.

--------------------------------------------------

📁 ESTRUCTURA RECOMENDADA DEL PROYECTO

/server
  /packages
  /client_packages
  /configs
  index.js
.gitignore
README.md

--------------------------------------------------

🚫 ARCHIVOS QUE NO SE SUBEN (.gitignore)

node_modules/
logs/
*.log
.env
.env.local
.cache/

--------------------------------------------------

📝 CONVENCIÓN DE COMMITS

Usamos Conventional Commits:

- feat: nueva funcionalidad
- fix: corrección de bug
- refactor: cambio interno
- docs: documentación
- chore: tareas menores

Ejemplos correctos:
- feat: add vehicle shop
- fix: prevent player spawn crash
- refactor: clean auth logic

--------------------------------------------------

🛑 ERRORES COMUNES (NO HACER)

- Trabajar todos en main
- Commits tipo “muchos cambios”
- Subir configs locales o logs
- Hacer git pull sin pensar

--------------------------------------------------

✅ OBJETIVO FINAL

- Código limpio
- Historial claro
- Conflictos mínimos
- Servidor estable

Si tienes dudas: pregunta antes de hacer push a main.
