# Semana #2

Aquí están las variantes anotadas para que puedas juzgar la legibilidad por ti mismo.

### 😠 Los principiantes a veces hacen eso. ¡Malo! Las llaves no son necesarias:

```javascript
if (n < 0) {alert(`Power ${n} is not supported`);}

if (n < 0)
  alert(`Power ${n} is not supported`);
😏 Una línea sin llaves: aceptable, si es corta:
if (n < 0) alert(`Power ${n} is not supported`);
```

## EStilos:

- [StandardJS](https://standardjs.com/)
- [JavaScript.info - Estructura del código](https://es.javascript.info/structure#semicolon)
- [JSLint](https://www.jslint.com/)
- [ESLint](https://eslint.org/)
- [Guía de estilo de JavaScript de Airbnb](https://github.com/airbnb/javascript)
- [Guía de estilo de JavaScript de Google](https://google.github.io/styleguide/jsguide.html)

## BDD:

1. **[Sinon.js](https://sinonjs.org/)**  
   Sinon.js es una biblioteca de JavaScript utilizada para crear pruebas unitarias. Proporciona herramientas como **stubs**, **spies** y **mocks**, que son útiles para simular comportamientos, interceptar llamadas a funciones y verificar interacciones en pruebas.

2. **[Mocha.js](https://mochajs.org/)**  
   Mocha.js es un framework de pruebas para JavaScript que se ejecuta en Node.js y en el navegador. Es conocido por su flexibilidad, ya que permite usar diferentes bibliotecas de aserciones (como Chai) y reportes personalizados. Es ideal para pruebas asíncronas y ofrece una sintaxis clara y descriptiva.

3. **[Chai.js](https://www.chaijs.com/)**  
   Chai.js es una biblioteca de aserciones para Node.js y el navegador. Proporciona una sintaxis legible y expresiva para realizar afirmaciones en pruebas. Ofrece tres estilos de escritura: `assert`, `expect` y `should`, lo que lo hace muy versátil y compatible con frameworks como Mocha.

Un buen articulo para leer:
https://es.wikipedia.org/wiki/Desarrollo_guiado_por_comportamiento

## Pollyfill , Transpilers:

- [Compatibilidad de ES6+](https://compat-table.github.io/compat-table/es6/) – Para JavaScript puro.
- [Can I Use](https://caniuse.com/) – Para funciones relacionadas al navegador.
- [Babel Loader](https://github.com/babel/babel-loader) – Cargador de Babel para Webpack.
- [Webpack](https://webpack.js.org/) – Documentación oficial de Webpack.

# Practica Objetos:
## Ejercicios de JavaScript: Manipulación de Objetos

## Ejercicio 1: Verificar si un objeto está vacío
## Crea un objeto vacío `obj`.
## Escribe una función `estaVacio(obj)` que devuelva `true` si el objeto no tiene propiedades, y `false` en caso contrario.
# Ejercicios de JavaScript: Manipulación de Objetos

## Ejercicio 3: Crear una copia superficial de un objeto usando `Object.assign`
- Crea un objeto `original` con varias propiedades.
- Usa `Object.assign` para crear una copia superficial del objeto en una nueva variable `copia`.
- Modifica una propiedad en `copia` y verifica si el cambio afecta al objeto `original`.

## Ejercicio 4: Crear una copia profunda de un objeto usando `structuredClone`
- Crea un objeto `original` con propiedades anidadas.
- Usa `structuredClone` para crear una copia profunda del objeto en una nueva variable `copiaProfunda`.
- Modifica una propiedad anidada en `copiaProfunda` y verifica si el cambio afecta al objeto `original`.

## Ejercicio 5: Combinar dos objetos usando `Object.assign`
- Crea dos objetos `obj1` y `obj2` con propiedades diferentes.
- Usa `Object.assign` para combinar ambos objetos en un nuevo objeto `combinado`.
- Imprime el objeto `combinado` para verificar el resultado.

## Ejercicio 6: Verificar si un objeto tiene una propiedad específica
- Crea un objeto `auto` con propiedades como `marca`, `modelo` y `año`.
- Escribe una función `tienePropiedad(obj, prop)` que devuelva `true` si el objeto tiene la propiedad especificada, y `false` en caso contrario.

## Ejercicio 7: Eliminar una propiedad de un objeto
- Crea un objeto `usuario` con propiedades como `nombre`, `email` y `edad`.
- Elimina la propiedad `edad` del objeto.
- Imprime el objeto para verificar que la propiedad ha sido eliminada.

## Ejercicio 8: Crear una copia de un objeto con propiedades adicionales
- Crea un objeto `producto` con propiedades como `nombre` y `precio`.
- Usa `Object.assign` para crear una copia del objeto y añadir una nueva propiedad `stock`.

## Ejercicio 9: Clonar un objeto con métodos
- Crea un objeto `calculadora` con métodos como `sumar` y `restar`.
- Usa `structuredClone` para clonar el objeto y verifica si los métodos se clonan correctamente.

## Ejercicio 10: Crear un objeto a partir de otro con propiedades modificadas
- Crea un objeto `libro` con propiedades como `titulo`, `autor` y `año`.
- Usa `Object.assign` para crear un nuevo objeto `libroActualizado` donde el año sea modificado.


