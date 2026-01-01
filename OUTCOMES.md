# Resultados: Nivel Master (Trabajo Individual)

> **Nota:** Se utiliza el identificador 'Group-A' por compatibilidad con el formato de entrega, pero el trabajo es individual.

## 1. Resumen
Se han aplicado técnicas avanzadas de reescritura de historia: `amend` para correcciones rápidas, `rebase interactivo` para limpieza de commits y `rebase` de rama para mantener un historial lineal.

## 2. Parte 1: Amend
**Caso de uso:** Olvidé incluir una línea de configuración en el último commit.
**Solución:** Modifiqué el archivo, hice `git add` y luego `git commit --amend`. Esto actualizó el commit existente sin crear uno nuevo "sucio".

## 3. Parte 2: Rebase Interactivo
**Limpieza:** Tenía 3 commits, uno de ellos corrigiendo un typo del anterior. Usé `git rebase -i HEAD~3` y marqué el commit de corrección como `fixup`.
**Resultado:** El commit del error desapareció fusionado, dejando una historia limpia y profesional.

## 4. Parte 3: Rebase de Rama
**Escenario:** Mientras trabajaba en `feature/awesome-feature`, la rama `master` avanzó.
**Acción:** En lugar de hacer un merge (que crea un commit de "mergeo" ruidoso), hice `git rebase master`. Esto movió mis cambios a la punta de la nueva historia, creando una línea recta.

## 5. Reflexión sobre Riesgos
Reescribir la historia es poderoso pero peligroso. He aprendido la regla de oro: **Nunca hacer rebase en ramas públicas compartidas**. Si cambio la historia de una rama que otros usan, romperé su trabajo. Solo debo usar estas técnicas en mis ramas locales antes de compartir (push).

## 6. Evidencia Técnica

### Historial Lineal (Post-Rebase)
* e24a111 Add awesome feature implementation
* 64e6e1a Update on master branch with critical fixes
* c9c7a19 Add feature B
* 057b328 Add feature A
* e893490 Add complete configuration file
* b5d8eb6 refactor: consolidate master exercises into single comprehensive exercise on history rewriting
* 960a0a6 docs: Add submission instructions to master level
* f0055a0 Update README for master level exercises
| * f6a93d7 docs: Entrega nivel Intermediate (Individual)
| *   fe6e21e Merge footer with resolved conflicts
| |\  
| | * 0195b2c Add footer to page
| * | 77b88ea Add header to page
| |/  
| * 994450b refactor: consolidate intermediate exercises into single comprehensive exercise
| * a1c17e7 docs: Add submission instructions to intermediate level
| * 9f25f7a Update README for intermediate level exercises
|/  
