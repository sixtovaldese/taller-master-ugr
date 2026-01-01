# Resultados: Nivel Master of the Universe (Trabajo Individual)

> **Nota:** Se utiliza el identificador 'Group-A' por requisitos del formato de entrega, pero certifico que este trabajo es **individual**.

## 1. Resumen Ejecutivo
Se ha implementado una capa de seguridad y gobernanza sobre el repositorio. Esto incluye la protección de ramas críticas, el firmado criptográfico de commits (GPG) y la prevención de fugas de secretos.

## 2. Protección de Ramas (Branch Protection)
**Configuración realizada en GitHub:**
- Rama objetivo: `main`
- Reglas activas:
  - *Require pull request before merging*: Obligatorio para Code Review.
  - *Require signed commits*: Solo commits verificados pueden entrar.
  - *Do not allow bypassing settings*: Ni siquiera los administradores pueden saltarse las reglas.

## 3. Firmado de Commits (GPG)
**Infraestructura:**
- Se generó un par de claves RSA de 4096 bits.
- Se exportó la clave pública a GitHub.
- Se configuró Git local para firmar automáticamente (`commit.gpgsign true`).
**Resultado:** Los commits ahora muestran la etiqueta "Verified" en GitHub, garantizando no repudio e identidad.

## 4. Gestión de Secretos
**Prevención:** Se ha endurecido el archivo `.gitignore` para bloquear extensiones sensibles como `*.pem`, `*.key` y archivos de entorno `.env`.
**Auditoría:** Se incluye un reporte de auditoría en la carpeta `security-artifacts`.

## 5. Reflexión Profesional
En entornos empresariales, la identidad lo es todo. Si un atacante compromete una cuenta pero no tiene la clave privada GPG, no puede suplantar al desarrollador en el historial (Supply Chain Security). La combinación de *Branch Protection* + *Signed Commits* crea una cadena de confianza robusta.

## 6. Evidencia Criptográfica

```text
commit cdcf507d07cdcabd808b4f7da0609dfde8f67146
gpg: Signature made ju.,  1 de ene. de 2026 14:13:30 HSP
gpg:                using RSA key 6BE1A391ABF204685007B7C54C8902BED33F5CC2
gpg: checking the trustdb
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: depth: 0  valid:   1  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 1u
gpg: Good signature from "Sixto Valdes <sixto@datacultura.org>" [ultimate]
Author: Sixto Valdes <sixto@datacultura.org>
Date:   Thu Jan 1 14:13:30 2026 -0300

    chore: Harden repository security configuration

commit b0fb9dc0dfbe8a0cdf9099e70d6ea883e8fc8d14
gpg: Signature made lu., 22 de dic. de 2025  5:51:03 HSP
gpg:                using RSA key 1706CDE4E490D08BBEAD9756063BFCF906BA72B7
gpg: Can't check signature: No public key
Author: Miguel Angel Oltra <miguel.oltra@se.com>
Date:   Mon Dec 22 09:51:02 2025 +0100

    refactor: consolidate master-of-the-universe exercises into single comprehensive exercise

commit d1ef79fc28da80e9a124d2f48449c402f09d2ade
Author: Miguel Angel Oltra <SESA219665@se.com>
Date:   Sat Nov 29 12:11:47 2025 +0100

    docs: Add submission instructions to master-of-the-universe level

commit 5bffa64b86e846199a574a4b92e3009d7bde1492
Author: Miguel Angel Oltra <SESA219665@se.com>
Date:   Sat Nov 29 11:57:02 2025 +0100

    Update README for master-of-the-universe level exercises

commit dc582031fed7a252a3c583fe16f497dbc9dcedd1
Author: Miguel Angel Oltra <SESA219665@se.com>
Date:   Sat Oct 25 12:14:28 2025 +0200

    Revert "Update README.md"
    
    This reverts commit e2db1ca85b4c8eca7b31d883744bd3a6f5e444b3.
```
