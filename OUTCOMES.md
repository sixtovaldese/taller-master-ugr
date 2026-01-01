# Resultados: Nivel Principiante (Trabajo Individual)

> **Nota:** Se mantiene el identificador 'Group-A' en el nombre de la rama para cumplir estricamente con el formato de entrega solicitado (`group-X-outcomes`), pero certifico que este trabajo es **individual**.

## 1. Resumen del Ejercicio
He completado los pasos requeridos del nivel Newbie. Configuré mi identidad, practiqué el flujo básico (edit-add-commit) creando el archivo 'hello.txt' y gestioné una rama nueva ('feature/my-info') para simular el trabajo en una funcionalidad.

## 2. Comandos Principales
- **Configuración:** `git config --global user.name "Sixto Valdes"`
- **Creación:** `git add .` seguido de `git commit -m "mensaje"`
- **Ramas:** `git checkout -b feature/my-info` para crear y cambiar.
- **Remoto:** Tuve que usar `git remote set-url origin ...` para apuntar a mi Fork.

## 3. Problemas y Soluciones
- **Bloqueo:** Al intentar el push inicial, recibí un error "403 Permission Denied".
- **Solución:** Entendí que no tengo permisos en el repo del profesor. Hice un "Fork" en GitHub a mi cuenta y cambié la URL del remoto local para poder subir mis cambios.

## 4. Reflexión
Me ha servido para entender que el repositorio local y el remoto están desconectados hasta que haces push/pull. También me queda más claro cómo moverme entre ramas sin perder el trabajo.

## 5. Evidencia del Historial
* 8b47fff docs: Entrega nivel Intermedio (Merge y Tags)
*   fe6e21e Merge footer with resolved conflicts
|\  
| * 0195b2c Add footer to page
* | 77b88ea Add header to page
|/  
* 994450b refactor: consolidate intermediate exercises into single comprehensive exercise
* a1c17e7 docs: Add submission instructions to intermediate level
* 9f25f7a Update README for intermediate level exercises
| * 45487b2 docs: Entrega final Nivel Newbie (Grupo A)
| | * bd9a10d Add personal information
| |/  
| * 1aad82b Add hello.txt with my name
