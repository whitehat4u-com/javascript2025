# Funciones

## 3 tipos de declaraciones:

```javascript
// Función regular
function suma(a, b) {
  return a + b;
}

// Expresión de función
const suma = function (a, b) {
  return a + b;
};

// Arrow function
const suma = (a, b) => a + b;
```

## Console y Mensajes

| Método               | Descripción                                                                | Ejemplo de uso                                                             |
| -------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `console.log()`      | Muestra un mensaje en la consola.                                          | `console.log("Hola, Mundo");`                                              |
| `console.info()`     | Similar a `console.log()`, pero se usa para mensajes informativos.         | `console.info("Esto es un mensaje informativo");`                          |
| `console.warn()`     | Muestra un mensaje de advertencia en la consola (normalmente en amarillo). | `console.warn("¡Cuidado! Esto es una advertencia.");`                      |
| `console.error()`    | Muestra un mensaje de error en la consola (normalmente en rojo).           | `console.error("¡Algo salió mal!");`                                       |
| `console.debug()`    | Muestra un mensaje de depuración en la consola.                            | `console.debug("Depurando: valor de x =", x);`                             |
| `console.table()`    | Muestra datos en formato de tabla.                                         | `console.table([{nombre: "Alice", edad: 25}, {nombre: "Bob", edad: 30}]);` |
| `console.group()`    | Crea un grupo de mensajes en la consola (se puede anidar).                 | `console.group("Grupo 1"); console.log("Mensaje 1"); console.groupEnd();`  |
| `console.groupEnd()` | Cierra un grupo de mensajes en la consola.                                 | `console.groupEnd();`                                                      |
| `console.time()`     | Inicia un temporizador para medir el tiempo de ejecución.                  | `console.time("Tiempo"); ... console.timeEnd("Tiempo");`                   |
| `console.timeEnd()`  | Detiene un temporizador y muestra el tiempo transcurrido.                  | `console.timeEnd("Tiempo");`                                               |
| `console.clear()`    | Limpia la consola.                                                         | `console.clear();`                                                         |
| `console.count()`    | Cuenta cuántas veces se ha llamado a este método.                          | `console.count("Contador");`                                               |
| `console.assert()`   | Muestra un mensaje de error si la afirmación es falsa.                     | `console.assert(x === 5, "x no es igual a 5");`                            |
| `console.dir()`      | Muestra una lista interactiva de las propiedades de un objeto.             | `console.dir(document.body);`                                              |
| `console.trace()`    | Muestra una traza de la pila de llamadas.                                  | `console.trace("Seguimiento de la pila");`                                 |

# Depuración en JavaScript usando Chrome DevTools

Depurar código es una parte esencial del desarrollo de software. Chrome DevTools es una herramienta poderosa que permite a los desarrolladores depurar JavaScript de manera eficiente. En este artículo, exploraremos cómo usar las funciones básicas de depuración en Chrome, incluyendo los controles de ejecución como **Pausa**, **Paso a paso**, **Siguiente función**, y más.

---

## **Acceder a Chrome DevTools**

Para abrir Chrome DevTools:

1. Haz clic derecho en cualquier parte de una página web y selecciona **"Inspeccionar"**.
2. O presiona `Ctrl + Shift + I` (Windows/Linux) o `Cmd + Option + I` (Mac).
3. Navega a la pestaña **"Sources"** (Fuentes) para ver y depurar tu código JavaScript.

---

## **Puntos de interrupción (Breakpoints)**

Los puntos de interrupción son lugares en el código donde la ejecución se detiene para que puedas inspeccionar el estado del programa.

### Cómo agregar un punto de interrupción:

1. En la pestaña **Sources**, navega hasta el archivo JavaScript que deseas depurar.
2. Haz clic en el número de línea donde quieras pausar la ejecución. Aparecerá un marcador azul indicando el punto de interrupción.

---

## **Controles de ejecución**

Una vez que la ejecución se detiene en un punto de interrupción, puedes usar los controles de ejecución para avanzar paso a paso por el código.

## **Controles disponibles**

| Nombre                                 | Icono | Descripción                                                                                      | Atajo             |
| -------------------------------------- | ----- | ------------------------------------------------------------------------------------------------ | ----------------- |
| **Resume (Reanudar)**                  | ▶️    | Continúa la ejecución hasta el siguiente punto de interrupción o hasta que finalice el programa. | `F8` o `Ctrl + \` |
| **Step Over (Paso a paso por encima)** | ⏭️    | Ejecuta la línea actual y pasa a la siguiente línea, sin entrar en funciones internas.           | `F10`             |
| **Step Into (Paso a paso por dentro)** | ⏬    | Entra en la función actual para depurar línea por línea dentro de ella.                          | `F11`             |
| **Step Out (Salir de la función)**     | ⏫    | Sale de la función actual y continúa la ejecución desde donde fue llamada.                       | `Shift + F11`     |
| **Pause (Pausar)**                     | ⏸️    | Pausa la ejecución del código en el punto actual.                                                | -                 |

# Depuración en JavaScript usando Chrome DevTools

Depurar código es una parte esencial del desarrollo de software. Chrome DevTools es una herramienta poderosa que permite a los desarrolladores depurar JavaScript de manera eficiente. En este artículo, exploraremos cómo usar las funciones básicas de depuración en Chrome, incluyendo los controles de ejecución como **Pausa**, **Paso a paso**, **Siguiente función**, y más.

---

## **Acceder a Chrome DevTools**

Para abrir Chrome DevTools:

1. Haz clic derecho en cualquier parte de una página web y selecciona **"Inspeccionar"**.
2. O presiona `Ctrl + Shift + I` (Windows/Linux) o `Cmd + Option + I` (Mac).
3. Navega a la pestaña **"Sources"** (Fuentes) para ver y depurar tu código JavaScript.

---

## **Puntos de interrupción (Breakpoints)**

Los puntos de interrupción son lugares en el código donde la ejecución se detiene para que puedas inspeccionar el estado del programa.

### Cómo agregar un punto de interrupción:

1. En la pestaña **Sources**, navega hasta el archivo JavaScript que deseas depurar.
2. Haz clic en el número de línea donde quieras pausar la ejecución. Aparecerá un marcador azul indicando el punto de interrupción.

---

## **Controles de ejecución**

Una vez que la ejecución se detiene en un punto de interrupción, puedes usar los controles de ejecución para avanzar paso a paso por el código. intenta seguir el resultado de las variables a y b en el siguiente codigo:

```javascript
function suma(a, b) {
  return a + b;
}

function calcular() {
  const x = 5;
  const y = 10;
  const resultado = suma(x, y);
  console.log(resultado);
}

calcular();
```

# Practica 2:

## **Inspeccionar variables y estado**

Mientras el código está pausado, puedes inspeccionar el valor de las variables y el estado del programa:

1. En el panel **Scope** (Ámbito), verás las variables locales y globales.
2. También puedes pasar el cursor sobre las variables en el código para ver sus valores.

---

## **Depuración avanzada**

- **Watch Expressions**: Agrega expresiones para monitorear valores específicos durante la ejecución.
- **Call Stack**: Muestra la pila de llamadas, es decir, el orden en que se han llamado las funciones.
- **Breakpoints condicionales**: Establece puntos de interrupción que solo se activan si se cumple una condición específica.

---

## **Ejemplo práctico**

Supongamos que tienes el siguiente código:

```javascript
function suma(a, b) {
  return a + b;
}

function calcular() {
  const x = 5;
  const y = 10;
  const resultado = suma(x, y);
  console.log(resultado);
}

calcular();
```
