# Funciones en JavaScript

En JavaScript, una **función** es un bloque de código reutilizable que realiza una tarea específica. Las funciones pueden recibir datos de entrada (llamados **argumentos** o **parámetros**), procesarlos y devolver un resultado (usando `return`). También pueden ejecutar acciones sin devolver nada.

## Conceptos clave:

1. **Parámetros (args)**: Son variables que se pasan a la función cuando se invoca. Estos permiten que la función trabaje con datos dinámicos.
2. **Return**: Es la palabra clave que devuelve un valor desde la función. Si no se usa `return`, la función devuelve `undefined` por defecto.
3. **Parámetros variables (params)**: En JavaScript, puedes manejar un número variable de argumentos usando `arguments` (obsoleto en modos estrictos) o el operador `...` (rest parameters).

## Ejemplo básico:

```javascript
function sumar(a, b) {
  return a + b;
}

console.log(sumar(2, 3)); // Output: 5
```

## Practica:

1. Elabora un arbol que luzca como este tipo de dibujo impreso en el console.log():

```
    *
   ***
  *****
 *******
*********
```

# Solucion, solo en caso de emergencia:

```
   function imprimirArbol(niveles) {
    // Iteramos desde 1 hasta el número de niveles
    for (let i = 1; i <= niveles; i++) {
        let espacios = "";
        let asteriscos = "";

        // Construir la cadena de espacios
        for (let j = 0; j < niveles - i; j++) {
            espacios += " ";
        }

        // Construir la cadena de asteriscos
        for (let k = 0; k < i * 2 - 1; k++) {
            asteriscos += "*";
        }

        // Mostrar la línea completa
        console.log(espacios + asteriscos);
    }

}

// Ejemplo de uso:
imprimirArbol(5);
```
