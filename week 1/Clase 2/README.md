# Clase 2

## Resumen del Hoisting

### Variables:

- **`var`**: La declaración es hoisted, pero no la inicialización.
- **`let` y `const`**: La declaración es hoisted, pero no se puede acceder a ellas antes de su declaración (zona muerta temporal).

### Funciones:

- **Funciones declaradas**: La función completa es hoisted.
- **Funciones expresadas**: Solo la declaración de la variable es hoisted, no la asignación de la función.

## Consejos para Evitar Problemas con el Hoisting

1. Declara siempre las variables y funciones al principio de su ámbito.
2. Usa `let` y `const` en lugar de `var` para evitar comportamientos inesperados.
3. Evita llamar funciones antes de su declaración si son funciones expresadas.

## Tareas

### Trabajando con variables.

**Importancia: 2**

1. Declara dos variables: `admin` y `name`.
2. Asigna el valor `"John"` a `name`.
3. Copia el valor de `name` a `admin`.
4. Muestra el valor de `admin` usando `alert` (debe salir `“John”`).

---

### Dando el nombre correcto

**Importancia: 3**

1. Crea una variable con el nombre de nuestro planeta. ¿Cómo nombrarías a dicha variable?
2. Crea una variable para almacenar el nombre del usuario actual de un sitio web. ¿Cómo nombrarías a dicha variable?
