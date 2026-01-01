# Resultados: Nivel Intermedio (Trabajo Individual)

> **Nota:** Se mantiene el identificador 'Group-A' en el nombre de la rama para cumplir estricamente con el formato de entrega solicitado (`group-X-outcomes`), pero certifico que este trabajo es **individual**.

## 1. Resumen del Ejercicio
Se ha practicado la fusión de ramas divergentes (`feature/header` y `feature/footer`), la resolución manual de conflictos de código y el uso de etiquetas (tags) para versionado.

## 2. Parte 1: Fusión y Conflictos
**Comandos usados:**
- Creación: `git checkout -b feature/...`
- Conflicto provocado: `git merge feature/footer`
- Resolución: Edición manual de `page.html` limpiando marcadores.

**Experiencia con el conflicto:**
Al hacer el segundo merge, Git se detuvo informando de un conflicto en `page.html`. Abrí el archivo, vi las dos versiones del código separadas por marcadores, eliminé los marcadores y dejé ambas líneas (header y footer) porque esa era la intención del diseño.

## 3. Parte 2: Etiquetas (Tags)
**Comandos usados:**
- Anotada: `git tag -a v1.0 -m "mensaje"`
- Ligera: `git tag v1.0-test`
- Push: `git push origin --tags`

**Diferencia observada:**
La etiqueta anotada (`v1.0`) guarda autor, fecha y mensaje (como un commit completo), ideal para releases oficiales. La ligera (`v1.0-test`) es solo un puntero a un commit, útil para marcas temporales o personales.

## 4. Reflexión
Una de las cosas importantes a comprender es que los conflictos no son errores, solo son situaciones donde Git necesita que analicemos esta diferencia para que podamos decidir qué hacer. También entiendo que los tags los ocupamos como puntos fijos en la historia, así como snapshots de versiones, mientras que las ramas son algo distinto: son punteros móviles que van avanzando en el desarrollo.

## 5. Evidencia Técnica

### Historial Gráfico
* b60e80c docs: Entrega nivel Newbie (Individual)
| * 8b47fff docs: Entrega nivel Intermedio (Merge y Tags)
| *   fe6e21e Merge footer with resolved conflicts
| |\  
| | * 0195b2c Add footer to page
| * | 77b88ea Add header to page
| |/  
| * 994450b refactor: consolidate intermediate exercises into single comprehensive exercise
| * a1c17e7 docs: Add submission instructions to intermediate level
| * 9f25f7a Update README for intermediate level exercises
| | * bd9a10d Add personal information
| |/  
|/|   
* | 1aad82b Add hello.txt with my name
* | 360f4a4 refactor: consolidate newbie exercises into single comprehensive exercise
* | 5eedc97 docs: Add submission instructions to newbie level
* | 45e1c31 Update README for newbie level exercises
|/  
| * 9602351 Adding GenAI guidelines
| * 7ad3af4 docs: update main branch files to reflect consolidated exercise structure (1 per level)

### Detalle de Tag v1.0
tag v1.0
Tagger: Sixto Valdes <sixto@datacultura.org>
Date:   Thu Jan 1 12:39:39 2026 -0300

Primera versión estable con header y footer fusionados

commit fe6e21e8f7fe6c4219404c84d659642227ed940d
Merge: 77b88ea 0195b2c
Author: Sixto Valdes <sixto@datacultura.org>
Date:   Thu Jan 1 12:37:10 2026 -0300

    Merge footer with resolved conflicts
