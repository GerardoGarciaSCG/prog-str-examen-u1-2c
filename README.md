# Práctica U1 — Git: ramas, conflicto y merge 

## Reglas obligatorias
1) **PROHIBIDO hacer merge a `main`.**
2) Debes crear exactamente estas ramas (desde `main`):
- `nombre-apellido/develop`
- `nombre-apellido/merge`

> Ejemplo: `juan-perez/develop` y `juan-perez/merge`

## Línea objetivo 
Vas a modificar la **misma línea** en tus dos ramas para provocar el conflicto.

**INSTRUCCIÓN IMPORTANTE:**
- **Edita SOLO esta línea** (sin duplicarla y sin moverla de lugar).
- No cambies el texto alrededor, solo el valor.

**LÍNEA OBJETIVO (NO BORRAR):**
`VERSION_OBJETIVO: PENDIENTE`

## Pasos obligatorios
1) Clona el repositorio y ábrelo en IntelliJ.
2) Verifica que estás en `main`.
3) Crea y cámbiate a: `nombre-apellido/develop`
4) En `nombre-apellido/develop`:
   - Cambia la línea objetivo a: `VERSION_OBJETIVO: develop`
   - Haz commit con mensaje: `develop: cambio para conflicto`
   - Haz push de tu rama al remoto.
5) Regresa a `main`.
6) Crea y cámbiate a: `nombre-apellido/merge`
7) En `nombre-apellido/merge`:
   - Cambia la línea objetivo a: `VERSION_OBJETIVO: merge`
   - Haz commit con mensaje: `merge: cambio para conflicto`
   - Haz push de tu rama al remoto.
8) Estando en `nombre-apellido/merge`, haz merge de:
   - `nombre-apellido/develop` ➜ `nombre-apellido/merge`
9) Debe aparecer un **conflicto**. Resuélvelo y deja el resultado final EXACTO así:
   - `VERSION_OBJETIVO: RESUELTO (develop + merge)`
   - Asegúrate de que no queden marcadores `<<<<<<<`, `=======`, `>>>>>>>`.
10) Finaliza el merge (commit si aplica) y haz **push**.

## Evidencias a entregar
1) Link al repositorio.
2) Evidencia de que existen tus ramas:
   - `nombre-apellido/develop`
   - `nombre-apellido/merge`
3) Evidencia del merge en `nombre-apellido/merge` (historial/commits).
4) Evidencia de que **main NO recibió merges**.
