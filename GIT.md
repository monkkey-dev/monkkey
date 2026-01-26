# 🧠 Guía simple de Git

## 📁 Repositorio
git init                // inicializa un repositorio git en la carpeta actual  
git clone URL           // clona un repositorio remoto en local  

## 📊 Estado y cambios
git status              // muestra el estado del repositorio  
git diff                // muestra cambios no añadidos al stage  
git diff --staged       // muestra cambios ya añadidos al stage  

## ➕ Añadir cambios (stage)
git add archivo.txt     // añade un archivo concreto al stage  
git add .               // añade todos los cambios al stage  

## 💾 Commits
git commit -m "mensaje" // crea un commit con mensaje  
git commit --amend      // modifica el último commit  

## 🌿 Ramas
git branch              // lista las ramas locales  
git branch nombre       // crea una nueva rama  
git checkout nombre     // cambia a una rama  
git checkout -b nombre  // crea y cambia a una rama  
git switch nombre       // cambia a una rama (moderno)  

## 🔀 Merge y rebase
git merge rama          // fusiona una rama en la actual  
git rebase rama         // reaplica tus commits sobre otra rama  

## 🌍 Remotos
git remote -v           // muestra repositorios remotos  
git remote add origin URL // añade un remoto llamado origin  

## ⬇️ Descargar cambios
git fetch origin        // descarga cambios del remoto sin tocar tu código  
git pull origin main    // descarga y mezcla cambios del remoto  

## ⬆️ Subir cambios
git push                // sube la rama actual  
git push origin main    // sube main al remoto  

## 🗑️ Eliminar cosas
git rm archivo.txt      // elimina un archivo y lo prepara para commit  
git branch -d rama      // elimina una rama local  

## ⏪ Deshacer (cuidado)
git restore archivo.txt           // descarta cambios en un archivo  
git restore --staged archivo.txt  // quita un archivo del stage  
git reset HEAD~1                  // borra el último commit (mantiene cambios)  
git reset --hard HEAD~1           // borra commit y cambios (peligroso)  

## 🕵️ Historial
git log                 // muestra el historial de commits  
git log --oneline       // historial resumido  

## 🧩 Tags
git tag v1.0.0          // crea un tag  
git push origin v1.0.0  // sube un tag  

## 🧠 Regla de oro
fetch mira  
pull toca  
commit explica  
