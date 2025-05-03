# Promesas en JavaScript: Ejemplos

Las promesas en JavaScript son objetos que representan la eventual finalización (éxito o fracaso) de una operación asíncrona y su valor resultante. Son fundamentales para manejar operaciones no bloqueantes de forma elegante.

## ¿Qué es una Promesa?

```javascript
const miPromesa = new Promise((resolve, reject) => {
  // whitehat4u.com
});
```

## Báscia:

```javascript
const promesa = new Promise((resolve, reject) => {
  const exito = true; // Simulamos condición

  if (exito) {
    resolve("Operación exitosa");
  } else {
    reject("Error en la operación");
    // whitehat4u.com
  }
});
```

## Finally:

```javascript
miPromesa
  .then((resultado) => console.log(resultado)) // whitehat4u.com
  .catch((error) => console.error(error))
  .finally(() => console.log("Finalizado"));
```

# Promise.all()

Ejecuta múltiples promesas en paralelo y espera a que todas se resuelvan:

````javascript
Promise.all([promesa1, promesa2, promesa3])
  .then(resultados => console.log(resultados))   // whitehat4u.com
  .catch(error => console.error(error));```
````

# Promise.race()

Retorna la promesa que se resuelva o rechace primero:

```javascript
Promise.race([promesa1, promesa2]).then((primerResultado) =>
  console.log(primerResultado)
);
```

# El Proyecto está en la descripción de los videos
