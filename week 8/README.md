# Tipos de Error en JavaScript

En JavaScript, los errores son objetos que representan problemas durante la ejecución del código. Estos errores pueden ser capturados y manejados usando bloques `try...catch`. A continuación, se describen los tipos de error más comunes:

## 1. **Error**

- Clase base para todos los errores.
- Ejemplo: `throw new Error("Mensaje genérico")`.

## 2. **SyntaxError**

- Ocurre cuando hay un error en la sintaxis del código.
- Ejemplo: `const x = ;` (falta el valor).

## 3. **ReferenceError**

- Se lanza cuando se intenta acceder a una variable no declarada.
- Ejemplo: `console.log(variableInexistente);`.

## 4. **TypeError**

- Surge cuando un valor no es del tipo esperado.
- Ejemplo: `null.toString()` (intentar llamar un método en `null`).

## 5. **RangeError**

- Ocurre cuando un valor está fuera del rango permitido.
- Ejemplo: `const arr = new Array(-1);` (tamaño negativo).

## 6. **URIError**

- Relacionado con funciones como `encodeURI()` o `decodeURI()`.
- Ejemplo: `decodeURI("%")` (URI malformada).

## 7. **EvalError** (Obsoleto en ES5+)

- Antes se usaba para errores en `eval()`, pero ya no es común.

## 8. **AggregateError** (ES2021)

- Representa múltiples errores agrupados, común en operaciones como `Promise.any()`.

## 9. **Custom Errors**

- Puedes crear tus propios errores extendiendo la clase `Error`.

```javascript
class MiError extends Error {
  constructor(message) {
    super(message);
    this.name = "MiError";
  }
}
throw new MiError("Error personalizado");
```

# El Objeto `Error` en JavaScript: Propiedades Clave

Cuando usas `try...catch` en JavaScript, el bloque `catch` recibe un objeto `Error` que contiene información detallada sobre qué falló. Aquí las propiedades esenciales:

## 🔍 Propiedades Principales

1. **`error.name`**

   - **Qué es**: Tipo de error (ej: `"TypeError"`, `"ReferenceError"`).
   - **Ejemplo**:
     ```javascript
     try {
       null.toString();
     } catch (error) {
       console.log(error.name); // "TypeError"
     }
     ```

2. **`error.message`**

   - **Qué es**: Descripción legible del error.
   - **Ejemplo**:
     ```javascript
     try {
       throw new Error("¡Algo explotó!");
     } catch (error) {
       console.log(error.message); // "¡Algo explotó!"
     }
     ```

3. **`error.stack`** _(No estándar, pero soportado)_
   - **Qué es**: Traza de la pila (stack trace) con la línea donde ocurrió el error.
   - **Ejemplo**:
     ```javascript
     try {
       functionFail();
     } catch (error) {
       console.log(error.stack);
       // "ReferenceError: functionFail is not defined at <archivo>:<línea>"
     }
     ```

## 🛠️ Uso Práctico

```javascript
try {
  // Código peligroso aquí
} catch (error) {
  console.error(`[${error.name}] ${error.message}`);
  console.debug("Stack trace:", error.stack); // Para depuración
}
```

### 📌 **Key Points:**

- **`name`** y **`message`** son propiedades estándar.
- **`stack`** es útil para debuggear _(pero no es parte del estándar ECMAScript)_.
- Todos los errores nativos (`SyntaxError`, `TypeError`, etc.) heredan estas propiedades.

# 📌 Call, Apply y Bind en JavaScript: Ejercicios Prácticos

## 🔹 **Método `call()`**

**¿Para qué sirve?**  
Ejecuta una función inmediatamente cambiando su contexto (`this`) y pasando argumentos **uno por uno**.

### Ejercicios:

1. **Préstamo de método**: Usa `call` para que un objeto `auto` (con método `arrancar`) pueda arrancar un objeto `moto` que no tiene ese método.
2. **Contexto dinámico**: Crea una función `saludar` que use `this.nombre`. Usa `call` para ejecutarla con distintos objetos (`persona1`, `persona2`).
3. **Herencia simulada**: Invoca un método de una clase `Padre` desde un objeto `Hijo` usando `call`.

---

## 🔹 **Método `apply()`**

**¿Para qué sirve?**  
Igual que `call`, pero recibe argumentos como **un array**. Ideal para funciones que trabajan con listas.

### Ejercicios:

1. **Máximo de un array**: Usa `Math.max` con `apply` para encontrar el número mayor en `[3, 5, 1]`.
2. **Concatenar arrays**: Aplica `Array.prototype.push` con `apply` para fusionar dos arrays sin loops.
3. **Función universal**: Crea una función `calcular` que acepte cualquier operación (suma, resta) y un array de números. Usa `apply` para ejecutarla.

---

## 🔹 **Método `bind()`**

**¿Para qué sirve?**  
Crea una **nueva función** con un contexto (`this`) fijo, pero no la ejecuta inmediatamente.

### Ejercicios:

1. **Eventos con contexto**: Fija el contexto de un método `manejarClic` a un objeto `boton` para usarlo en un event listener.
2. **Temporizadores**: Usa `bind` para que `setTimeout` ejecute un método de un objeto `usuario` con su contexto correcto.
3. **Funciones parciales**: Crea una función `multiplicar(a, b)` y usa `bind` para generar una nueva función `duplicar` (con `a = 2` fijo).

---

### 💡 **Conclusión**

- **`call`/`apply`**: Útiles para ejecutar funciones con contexto controlado (diferenciados por la forma de pasar argumentos).
- **`bind`**: Ideal para **guardar contexto** y usarlo después (eventos, callbacks).
