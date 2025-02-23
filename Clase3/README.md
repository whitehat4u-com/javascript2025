# Breve Reseña del Creador de JavaScript

## Brendan Eich

Brendan Eich es el creador del lenguaje de programación JavaScript. Nació en 1961 y es un ingeniero de software estadounidense. Eich desarrolló JavaScript en 1995 mientras trabajaba en Netscape Communications Corporation. Sorprendentemente, creó el lenguaje en solo **10 días**. JavaScript fue diseñado originalmente para agregar interactividad a las páginas web, y desde entonces se ha convertido en uno de los lenguajes de programación más populares del mundo.

---

## El Error de Tipo `null` como `object`

En JavaScript, el valor `null` se considera un tipo primitivo, pero cuando se utiliza el operador `typeof` para verificar su tipo, devuelve `"object"`. Esto es un **error histórico** en el lenguaje que se ha mantenido por razones de compatibilidad.

### ¿Por qué sucede esto?

El error se remonta a las primeras versiones de JavaScript. En la implementación original, los valores en JavaScript se representaban con una etiqueta de tipo y un valor. La etiqueta para objetos era `0`, y casualmente, `null` se representaba como un puntero nulo, que en muchas plataformas era `0x00`. Por lo tanto, `typeof null` devolvía `"object"` porque coincidía con la etiqueta de tipo de los objetos. Este comportamiento se ha mantenido para no romper la compatibilidad con código existente.

### Solución

Para verificar si un valor es `null`, se recomienda usar una comparación estricta:

```javascript
if (valor === null) {
  console.log("Es null");
}
```

## ¿Qué es el DOM en JavaScript?

El DOM (Document Object Model) es una representación en forma de árbol de los elementos de un documento HTML o XML. JavaScript puede interactuar con el DOM para manipular el contenido, la estructura y el estilo de una página web. El DOM permite a los desarrolladores acceder y modificar dinámicamente los elementos de una página, lo que hace posible crear aplicaciones web interactivas.

Ejemplo Básico de Manipulación del DOM:

```
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo DOM</title>
</head>
<body>
    <h1 id="titulo">Hola, Mundo!</h1>
    <button onclick="cambiarTexto()">Cambiar Texto</button>

    <script>
        function cambiarTexto() {
            // Acceder al elemento por su ID
            const titulo = document.getElementById("titulo");
            // Cambiar el contenido del elemento
            titulo.textContent = "¡JavaScript es genial!";
        }
    </script>
</body>
</html>
```

### Explicación

1. **Acceso al DOM**: Se utiliza `document.getElementById` para seleccionar un elemento del DOM por su ID.

2. **Manipulación**: Una vez seleccionado, se puede modificar su contenido, atributos o estilos.

3. **Eventos**: Se pueden agregar eventos (como `onclick`) para realizar acciones cuando el usuario interactúa con la página.

El DOM es una parte fundamental de JavaScript para crear páginas web dinámicas e interactivas.
