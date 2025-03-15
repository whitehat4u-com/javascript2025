# Semana #3

Revisa la lista de console de la clase 6 para tener mas ambito sobre el uso de console:
[Enlace a la Clase 6](https://github.com/whitehat4u-com/javascript2025/tree/main/week%201/Clase%206)

# Ejercicios con Símbolos en JavaScript

En este artículo, exploraremos cómo utilizar símbolos en JavaScript para crear propiedades únicas en objetos, y cómo manipular la salida de estos objetos utilizando el método `toPrimitive`. A continuación, se presentan tres ejercicios que te ayudarán a practicar estos conceptos.

## Ejercicio 1: Creación de un objeto con símbolos como propiedades

### Descripción:
Crea un objeto `persona` que tenga propiedades estándar como `nombre` y `edad`, y también propiedades únicas utilizando símbolos. Luego, utiliza `Symbol.keyFor` para obtener la clave de un símbolo registrado globalmente.

### Pasos:
1. Crea un símbolo registrado globalmente llamado `id`.
2. Crea un objeto `persona` con las propiedades `nombre` y `edad`.
3. Agrega una propiedad al objeto `persona` utilizando el símbolo `id`.
4. Utiliza `Symbol.keyFor` para obtener la clave del símbolo `id`.

## Ejercicio 2: Uso de `toPrimitive` para manipular la salida de un objeto

### Descripción:
Crea un objeto `coche` que tenga propiedades como `marca` y `modelo`. Luego, implementa el método `toPrimitive` para que el objeto se comporte de manera diferente cuando se convierte a un string o a un número.

### Pasos:
1. Crea un objeto `coche` con las propiedades `marca` y `modelo`.
2. Implementa el método `toPrimitive` en el objeto `coche` para que:
   - Cuando se convierta a string, devuelva una descripción del coche.
   - Cuando se convierta a número, devuelva el año de fabricación.


## Ejercicio 3: Función constructora con símbolos (sin `prototype` ni `Math`)

### Descripción:
Crea una función constructora `Animal` que tenga propiedades estándar como `nombre` y `especie`, y también propiedades únicas utilizando símbolos. Luego, implementa el método `toPrimitive` para que el objeto se comporte de manera diferente cuando se convierte a un string o a un número. En este ejercicio, no se utilizará `prototype` ni el método `Math`.

### Pasos:
1. Crea una función constructora `Animal` que acepte `nombre` y `especie` como parámetros.
2. Crea un símbolo registrado globalmente llamado `id`.
3. Agrega una propiedad al objeto `Animal` utilizando el símbolo `id`.
4. Implementa el método `toPrimitive` directamente en el objeto para que:
   - Cuando se convierta a string, devuelva una descripción del animal.
   - Cuando se convierta a número, devuelva un identificador único basado en un contador.






##Soluciones:

### 1. Código de ejemplo:

```javascript
// Paso 1: Crear un símbolo registrado globalmente
const id = Symbol.for('id');

// Paso 2: Crear un objeto persona
const persona = {
    nombre: 'Juan',
    edad: 30
};

// Paso 3: Agregar una propiedad con el símbolo id
persona[id] = 12345;

// Paso 4: Obtener la clave del símbolo id
const claveId = Symbol.keyFor(id);
console.log(claveId); // Debería imprimir 'id'
```

### 2. Codigo:
```javascript
const coche = {
    marca: 'Toyota',
    modelo: 'Corolla',
    año: 2020,
    [Symbol.toPrimitive](hint) {
        if (hint === 'string') {
            return `${this.marca} ${this.modelo}`;
        } else if (hint === 'number') {
            return this.año;
        }
        return null;
    }
};

console.log(String(coche)); // Debería imprimir 'Toyota Corolla'
console.log(Number(coche)); // Debería imprimir 2020
```

### 3. Código de ejemplo:

```javascript
// Paso 1: Crear una función constructora Animal
function Animal(nombre, especie) {
    this.nombre = nombre;
    this.especie = especie;

    // Paso 2: Crear un símbolo registrado globalmente
    const id = Symbol.for('id');

    // Paso 3: Agregar una propiedad con el símbolo id
    let contador = 0; // Contador para generar identificadores únicos
    this[id] = ++contador; // Asignar un identificador único

    // Paso 4: Implementar el método toPrimitive
    this[Symbol.toPrimitive] = function(hint) {
        if (hint === 'string') {
            return `${this.nombre} (${this.especie})`;
        } else if (hint === 'number') {
            return this[id]; // Devolver el identificador único
        }
        return null;
    };
}

// Crear una instancia de Animal
const perro = new Animal('Rex', 'Perro');
console.log(String(perro)); // Debería imprimir 'Rex (Perro)'
console.log(Number(perro)); // Debería imprimir 1 (identificador único)

const gato = new Animal('Mimi', 'Gato');
console.log(String(gato)); // Debería imprimir 'Mimi (Gato)'
console.log(Number(gato)); // Debería imprimir 2 (identificador único)
```
## Métodos (Well-Known Symbols) del objeto `Symbol`

Los **well-known symbols** son símbolos predefinidos en JavaScript que se utilizan para personalizar el comportamiento de objetos. A continuación, se presenta una lista de estos símbolos con una breve descripción de su propósito:

| Símbolo                     | Descripción                                                                                   |
|-----------------------------|-----------------------------------------------------------------------------------------------|
| `Symbol.iterator`           | Define el iterador por defecto de un objeto. Se usa en bucles `for...of` y operaciones similares. |
| `Symbol.asyncIterator`      | Define el iterador asíncrono de un objeto. Se usa en bucles `for await...of`.                 |
| `Symbol.match`              | Personaliza el comportamiento de `String.prototype.match`.                                    |
| `Symbol.replace`            | Personaliza el comportamiento de `String.prototype.replace`.                                  |
| `Symbol.search`             | Personaliza el comportamiento de `String.prototype.search`.                                   |
| `Symbol.split`              | Personaliza el comportamiento de `String.prototype.split`.                                    |
| `Symbol.hasInstance`        | Personaliza el comportamiento del operador `instanceof`.                                      |
| `Symbol.isConcatSpreadable` | Indica si un objeto debe ser "aplanado" al usar `Array.prototype.concat`.                     |
| `Symbol.unscopables`        | Define propiedades que no deben ser incluidas en un bloque `with`.                            |
| `Symbol.species`            | Especifica el constructor que se debe usar para crear objetos derivados (por ejemplo, en métodos como `map` o `slice`). |
| `Symbol.toPrimitive`        | Personaliza la conversión de un objeto a un valor primitivo (string, número, etc.).           |
| `Symbol.toStringTag`        | Define la descripción del objeto cuando se llama a `Object.prototype.toString`.               |
| `Symbol.dispose`            | (Propuesto) Define un método para liberar recursos cuando un objeto se desecha.               |
| `Symbol.asyncDispose`       | (Propuesto) Define un método asíncrono para liberar recursos cuando un objeto se desecha.     |
