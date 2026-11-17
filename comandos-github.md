# 10 comandos básicos de GitHub (Git)

GitHub funciona con Git, un sistema de control de versiones. Los siguientes comandos se escriben en la terminal (Git Bash, PowerShell, Terminal de macOS o la terminal de VS Code) y son los que más se usan en el día a día.

---

## 1. `git clone`

Descarga a tu computadora un repositorio que está en GitHub.

```bash
git clone https://github.com/usuario/repositorio.git
```

**Cuándo usarlo:** la primera vez que quieres trabajar con un proyecto existente.

---

## 2. `git status`

Muestra qué archivos cambiaron, cuáles están listos para guardarse y en qué rama estás.

```bash
git status
```

**Cuándo usarlo:** antes y después de cada cambio, para saber en qué estado está tu proyecto.

---

## 3. `git add`

Prepara los archivos modificados para el siguiente commit (los pasa al "área de preparación").

```bash
git add archivo.txt      # agrega un archivo específico
git add .                # agrega todos los cambios
```

**Cuándo usarlo:** cuando ya terminaste de editar y quieres elegir qué incluir en tu próximo guardado.

---

## 4. `git commit`

Guarda una "foto" de tus cambios preparados, con un mensaje que describe lo que hiciste.

```bash
git commit -m "Agrega página de inicio"
```

**Cuándo usarlo:** cada vez que completas una tarea pequeña y coherente. Mensajes claros facilitan revisar el historial.

---

## 5. `git push`

Sube tus commits locales al repositorio en GitHub.

```bash
git push origin main
```

**Cuándo usarlo:** cuando quieres que tus cambios queden respaldados en GitHub o compartidos con otros.

---

## 6. `git pull`

Descarga de GitHub los cambios más recientes y los integra en tu copia local.

```bash
git pull origin main
```

**Cuándo usarlo:** antes de empezar a trabajar, sobre todo si otra persona también modifica el proyecto.

---

## 7. `git branch`

Lista las ramas del proyecto o crea una nueva. Una rama es una línea de trabajo independiente.

```bash
git branch                       # lista las ramas
git branch nueva-funcion         # crea una rama nueva
```

**Cuándo usarlo:** para probar una idea o una función sin afectar la rama principal.

---

## 8. `git checkout` / `git switch`

Cambia de una rama a otra. `git switch` es la forma más reciente y clara de hacerlo.

```bash
git switch nueva-funcion         # cambia a la rama indicada
git checkout -b otra-rama        # crea una rama y cambia a ella (forma antigua)
```

**Cuándo usarlo:** cuando necesitas trabajar en otra parte del proyecto.

---

## 9. `git merge`

Une los cambios de una rama con la rama en la que estás actualmente.

```bash
git switch main
git merge nueva-funcion
```

**Cuándo usarlo:** cuando terminaste una función en una rama y quieres incorporarla al proyecto principal.

---

## 10. `git log`

Muestra el historial de commits: quién hizo cada cambio, cuándo y con qué mensaje.

```bash
git log
git log --oneline                # versión resumida, una línea por commit
```

**Cuándo usarlo:** para revisar qué se ha hecho en el proyecto o encontrar un cambio anterior.

---

## Flujo típico de trabajo

1. `git pull` para traer los cambios más recientes.
2. `git switch -c mi-cambio` para crear una rama de trabajo.
3. Editar los archivos.
4. `git status` para revisar los cambios.
5. `git add .` y `git commit -m "Descripción del cambio"`.
6. `git push origin mi-cambio` para subirlo a GitHub.
7. Abrir un *Pull Request* en GitHub para revisar y unir los cambios.
