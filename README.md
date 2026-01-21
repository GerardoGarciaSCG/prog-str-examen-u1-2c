# Examen U1 — Git: ramas, conflicto y merge (SIN tocar main)


## Reglas obligatorias
1) **PROHIBIDO** hacer merge a `main`.
2) Debes crear exactamente estas ramas (desde `main`):
- `nombre-apellido/develop`
- `nombre-apellido/merge`

> Ejemplo: `juan-perez/develop` y `juan-perez/merge`

---

## Proyecto a crear (obligatorio)
Vas a crear un proyecto Java en IntelliJ con el nombre:

**Nombre del proyecto:** `U1GitConflicto`

El proyecto debe contener un archivo **Main** con una constante que usaremos para provocar el conflicto.

---

## Línea objetivo (provoca el conflicto)
Vas a modificar la **misma línea** en tus dos ramas para provocar el conflicto.

**INSTRUCCIÓN IMPORTANTE:**
- Edita **SOLO** esta línea (sin duplicarla y sin moverla de lugar).
- No cambies el texto alrededor, solo el valor (el texto entre comillas).

➡️ **LÍNEA OBJETIVO (NO BORRAR):**
```java
public static final String VERSION_OBJETIVO = "PENDIENTE";
```

---

## Pasos obligatorios

### 1) Clonar y abrir el repo
1. Clona el fork del repositorio proporcionado (Revisa el pizarron).
2. Abre IntelliJ.
3. Selecciona **Open** y abre la carpeta del repositorio clonado.

### 2) Crear el proyecto `U1GitConflicto` dentro del repo (en `main`) -> El nombre es importante, hay penalizacion por no usar el nombre de proyecto indicado


1. Crea la clase `Main` (si no te la crea automáticamente):
   - Ruta sugerida: `U1GitConflicto/src/Main.java`
2. Pega este código base (obligatorio):

```java
public class Main {

    public static final String VERSION_OBJETIVO = "PENDIENTE";

    public static void main(String[] args) {
        System.out.println("Version: " + VERSION_OBJETIVO);
    }
}
```

3. Ejecuta el programa una vez para confirmar que compila y corre.
4. En `main`, realiza un commit inicial:
   - Mensaje: `init: proyecto U1GitConflicto`
5. Haz **push** a tu repositorio remoto.

### 3) Crear rama develop y hacer cambio 1 (conflicto)
1. Verifica que estás en `main`.
2. Crea y cámbiate a: `nombre-apellido/develop`
3. En `Main.java`, cambia la línea objetivo a:

```java
public static final String VERSION_OBJETIVO = "develop";
```

4. Commit con mensaje: `develop: cambio para conflicto`
5. Push de tu rama al remoto.

### 4) Crear rama merge y hacer cambio 2 (conflicto)
1. Regresa a `main`.
2. Crea y cámbiate a: `nombre-apellido/merge`
3. En `Main.java`, cambia la línea objetivo a:

```java
public static final String VERSION_OBJETIVO = "merge";
```

4. Commit con mensaje: `merge: cambio para conflicto`
5. Push de tu rama al remoto.

### 5) Merge hacia la rama merge (NO main) y resolver conflicto
1. Asegúrate de estar en `nombre-apellido/merge`.
2. Haz merge de:
   - `nombre-apellido/develop` ➜ `nombre-apellido/merge`
3. Debe aparecer un conflicto. Resuélvelo y deja el resultado final **EXACTO** así:

```java
public static final String VERSION_OBJETIVO = "RESUELTO (develop + merge)";
```

4. Asegúrate de que NO queden marcadores:
   - `<<<<<<<`, `=======`, `>>>>>>>`
5. Finaliza el merge (commit si aplica) y haz **push**.
6. Verifica en GitHub que:
   - El merge quedó en `nombre-apellido/merge`
   - `main` **NO** recibió merges.

---

## Evidencias a entregar
1) Link a tu repositorio (tu fork o tu repo, según indique el docente).
2) Evidencia de que existen tus ramas:
   - `nombre-apellido/develop`
   - `nombre-apellido/merge`
3) Evidencia del merge en `nombre-apellido/merge` (historial/commits).
4) Evidencia de que `main` NO recibió merges.
5) Evidencia del archivo final `Main.java` con el valor final exacto.

---

## Notas importantes
- No edites el README para provocar el conflicto; el conflicto debe ser en `Main.java`.
- Si tienes errores de autenticación al hacer push, revisa que estés logueado en GitHub desde IntelliJ o que tu token/credenciales estén configurados.
