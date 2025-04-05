# Semana 6

## Ejercicios:

### 1. Métodos del Prototype de `Object`

A continuación, se presenta una tabla con algunos métodos importantes del prototipo de `Object` y su descripción:

| Método             | Descripción                                                                                                |
| ------------------ | ---------------------------------------------------------------------------------------------------------- |
| `Object.assign()`  | Copia las propiedades enumerables de uno o más objetos fuente a un objeto destino.                         |
| `Object.create()`  | Crea un nuevo objeto con el prototipo y las propiedades especificadas.                                     |
| `Object.keys()`    | Devuelve un array con las claves enumerables de un objeto.                                                 |
| `Object.values()`  | Devuelve un array con los valores enumerables de un objeto.                                                |
| `Object.entries()` | Devuelve un array de arrays con pares `[clave, valor]` enumerables.                                        |
| `Object.freeze()`  | Congela un objeto, impidiendo modificaciones en sus propiedades.                                           |
| `Object.seal()`    | Sella un objeto, evitando que se añadan o eliminen propiedades.                                            |
| `Object.is()`      | Compara si dos valores son iguales (similar a `===`, pero con diferencias en casos especiales como `NaN`). |

**Ejemplo de práctica:**

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };

// Object.assign
const merged = Object.assign({}, obj1, obj2);
console.log(merged); // { a: 1, b: 2, c: 3, d: 4 }

// Object.keys
console.log(Object.keys(obj1)); // ["a", "b"]

// Object.create
const newObj = Object.create(obj1);
console.log(newObj.a); // 1 (heredado del prototipo obj1)
```

## 2. Ejercicios con new Map y new Set

### new Map

Un Map almacena pares clave-valor y recuerda el orden de inserción

```javascript
const map = new Map();
map.set("nombre", "Juan");
map.set("edad", 30);

console.log(map.get("nombre")); // "Juan"
console.log(map.has("edad")); // true
console.log(map.size); // 2

// Iterar sobre el Map
map.forEach((value, key) => {
  console.log(`${key}: ${value}`);
});
```

### new Set

Un Set almacena valores únicos de cualquier tipo.

```javascript
const set = new Set();
set.add(1);
set.add(2);
set.add(1); // No se añade (duplicado)

console.log(set.has(1)); // true
console.log(set.size); // 2

// Iterar sobre el Set
set.forEach((value) => {
  console.log(value);
});
```

## 3. Método para ver la colección de métodos en el prototipo

El método que permite verificar si un objeto está en la cadena de prototipos de otro es:  
**isPrototypeOf()**

```js
const padre = { nombre: "Padre" };
const hijo = Object.create(padre);

console.log(padre.isPrototypeOf(hijo)); // true
```

## 4. Ejercicio de spread Operator y destructuring:

```javascript
const user = {
  id: 1,
  username: "jsDev2023",
  email: "jsdev@example.com",
  isVerified: true, // Propiedad boolean
  age: 32,
  firstName: "María",
  lastName: "García",
  joinDate: "2022-05-15",
  lastLogin: "2023-11-20T08:30:00Z",
  accountStatus: "active",
  preferences: {
    theme: "dark",
    notifications: true,
    language: "es",
  },
  address: {
    // Objeto anidado
    street: "Calle Principal 123",
    city: "Barcelona",
    postalCode: "08001",
    country: "España",
    coordinates: {
      lat: 41.3851,
      lng: 2.1734,
    },
  },
  skills: ["JavaScript", "React", "Node.js"], // Array
  projects: [
    {
      id: 101,
      name: "E-commerce Platform",
      completed: true,
    },
    {
      id: 102,
      name: "Portfolio Redesign",
      completed: false,
    },
  ],
  isPremium: false, // Otro boolean
  socialMedia: {
    twitter: "@maria_js",
    github: "maria-js-dev",
  },
  twoFactorEnabled: true,
  loginAttempts: 0,
  metadata: {
    lastUpdated: "2023-11-01",
    createdBy: "admin",
  },
};
```

En el siguiente objeto, copia y pegalo en tu editor de codigo y realiza lo siguiente:

1. Extrae la direccion del usuario que simplemente se pueda acceder con una sola referencia, evitando acceso de punto o llaves.

2. Elabora un nuevo arreglo añadiendo esa dirección y un nuevo campo que sea un objeto con la propiedad: "ready", y el valor sea: true

3. Ahora crea un array de referencia y haz un map de ese objeto (incluyelo en un array para iterar), pero que solo contenga los items: preferences, skills y projects.

Si lo hiciste, lograste entender toda la clase, y además te esfuerzas por conseguir la información de tus ejercicios.
