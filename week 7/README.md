# Semana #7

# Ejercicios de JavaScript

## 1. Manipulación de funciones y uso de `new Date()`

1. **Fecha personalizada**: Crea una función que reciba día, mes y año como parámetros y devuelva un objeto Date con esa fecha. Luego muestra la fecha en formato "DD/MM/AAAA".

2. **Diferencia de días**: Escribe una función que calcule la diferencia en días entre dos fechas diferentes (pueden ser la fecha actual y una fecha futura).

3. **Reloj digital**: Crea una función que se ejecute cada segundo y muestre por consola la hora actual en formato "HH:MM:SS".

## 2. Manipulación de JSON con `JSON.stringify()` y `JSON.parse()`

1. **Convertir a JSON**: Crea un objeto que represente un libro (con título, autor y año) y conviértelo a formato JSON. Luego convierte ese JSON de vuelta a un objeto JavaScript.

2. **Almacenamiento local**: Crea un objeto con información de usuario (nombre, email, edad) y guárdalo en el localStorage como JSON. Luego recupéralo y conviértelo de nuevo a objeto.

3. **Validación de JSON**: Escribe una función que intente parsear una cadena JSON y maneje los errores adecuadamente si el formato no es válido.

## 3. Ejercicios de recursión

1. **Factorial de 100**:

   ```javascript
   function factorial(n) {
     // Tu código recursivo aquí
   }
   console.log(factorial(100)); // Debe mostrar el factorial de 100
   ```

2. ```javascript
   function sumaDigitos(n) {
     // Función recursiva que sume los dígitos de un número
     // Ej: 1234 → 1+2+3+4 = 10
   }
   console.log(sumaDigitos(1234)); // Debe mostrar 10
   ```

3. Ejercicio:

```js
const persona = {
  nombre: "Ana",
  edad: 30,
  profesion: "Ingeniera",
  ciudad: "Madrid",
  hobbies: ["leer", "viajar", "fotografía"],
};

// 1. Usa destructuración para extraer nombre y edad
// 2. Usa el operador rest para recoger el resto de propiedades en un objeto
// 3. Crea un nuevo objeto que combine algunas propiedades extraídas y el resto

// Ejemplo de solución: ✅
const { nombre, edad, ...resto } = persona;
const nuevaPersona = { nombre, ciudad: resto.ciudad, ...resto };

console.log(nuevaPersona);

const coche = {
  marca: "Toyota",
  modelo: "Corolla",
  año: 2022,
  características: {
    motor: "híbrido",
    potencia: "140cv",
    transmisión: "automática",
  },
  coloresDisponibles: ["blanco", "negro", "gris", "rojo"],
};
```
