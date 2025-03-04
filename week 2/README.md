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

##
