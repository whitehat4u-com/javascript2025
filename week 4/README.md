# Ejercicios Practica Semana 4

## Objeto de Referencia
```javascript
const Persona = {
  nombre: "Sin nombre",
  edad: 0,
  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
  }
};
```

| **Ejercicios**                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Crear un objeto `usuario` basado en `Persona` y asignarle un nombre y una edad usando `Object.setPrototypeOf`.                                                                                                |
| 2. Usar `Object.getPrototypeOf` para obtener el prototipo del objeto `usuario` y verificar que sea `Persona`.                                                                                                    |
| 3. Modificar el prototipo de `usuario` para agregar un nuevo método `despedirse` que imprima "Adiós".                                                                                                           |
| 4. Crear un nuevo objeto `admin` y establecer su prototipo como `usuario` usando `Object.setPrototypeOf`. Luego, agregar una propiedad `rol` con el valor "Administrador".                                       |
| Usar `Object.getPrototypeOf` para obtener el prototipo de `admin` y verificar que sea `usuario`.                                                                                                             |
| 5. Crear un objeto `estudiante` usando `Object.create` con `Persona` como prototipo. Asignarle un nombre y una edad.                                                                                            |
| 6. Usar `.__proto__` para acceder al prototipo de `estudiante` y verificar que sea `Persona`.                                                                                                                   |
| 7. Crear cuatro objetos (`objeto1`, `objeto2`, `objeto3`, `objeto4`) con referencias entre ellos. Cada objeto debe tener una propiedad `name`. Usar `Object.getPrototypeOf` para identificar cuáles objetos tienen referencias entre sí accediendo a la propiedad `name`. Ejemplo debajo!|

```javascript
const objeto1 = { name: "Objeto 1" };
const objeto2 = { name: "Objeto 2" };
const objeto3 = { name: "Objeto 3" };
const objeto4 = { name: "Objeto 4" };

Object.setPrototypeOf(objeto2, objeto1);
Object.setPrototypeOf(objeto3, objeto2);
Object.setPrototypeOf(objeto4, objeto3);

// Ejemplo de uso:
console.log(Object.getPrototypeOf(objeto4).name); // Debería imprimir "Objeto 3"
```
## Ejercicios Practicos II:
1. Crear un objeto profesor usando Object.create con Persona como prototipo. Luego, crear un objeto asistente que tenga como prototipo a profesor. Verificar la cadena de prototipos usando Object.getPrototypeOf.

2. Ejercicio Complejo: Crear cuatro objetos (a, b, c, d) con referencias circulares entre ellos usando Object.create. Cada objeto debe tener una propiedad name. El usuario debe identificar cuáles objetos tienen referencias entre sí accediendo a la propiedad name usando Object.getPrototypeOf.

```javascript
const a = Object.create(null, { name: { value: "A" } });
const b = Object.create(a, { name: { value: "B" } });
const c = Object.create(b, { name: { value: "C" } });
const d = Object.create(c, { name: { value: "D" } });

// Establecer referencia circular
Object.setPrototypeOf(a, d);

// Ejemplo de uso:
console.log(Object.getPrototypeOf(d).name); // Debería imprimir "C"
console.log(Object.getPrototypeOf(a).name); // Debería imprimir "D"
```
### Buena Suerte!