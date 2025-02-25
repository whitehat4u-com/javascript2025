# Matemáticas

Están soportadas las siguientes operaciones:

- Suma `+`
- Resta `-`
- Multiplicación `*`
- División `/`
- Resto `%`
- Exponenciación `**`

## Asignaciones encadenadas

Otra característica interesante es la habilidad para encadenar asignaciones:

```javascript
let a, b, c;

a = b = c = 2 + 2;

alert(a); // 4
alert(b); // 4
alert(c); // 4
```

## Practicar: ¿Cuáles son los resultados de estas expresiones?

```javascript
"" + 1 + 0;
"" - 1 + 0;
true + false;
6 / "3";
"2" * "3";
4 + 5 + "px";
"$" + 4 + 5;
"4" - 2;
"4px" - 2;
"  -9  " + 5;
"  -9  " - 5;
null + 1;
undefined + 1;
" \t \n" - 2;
```

# Operadores a Nivel de Bit en JavaScript

Los operadores a nivel de bit trabajan directamente con la representación binaria de los números. A continuación, se presentan ejemplos para cada uno:

---

## 1. AND ( `&` )

El operador `&` compara cada bit de dos números y devuelve `1` solo si ambos bits son `1`.

```js
let a = 5; //  0101 en binario
let b = 3; //  0011 en binario
let result = a & b; // 0001 (1 en decimal)

console.log(result); // Output: 1
```

## 2. OR ( `|` )

El operador `|` compara cada bit y devuelve `1` si al menos uno de los bits es `1`.

```js
let a = 5; //  0101 en binario
let b = 3; //  0011 en binario
let result = a | b; // 0111 (7 en decimal)

console.log(result); // Output: 7
```

## 3. XOR ( `^` )

El operador `^` devuelve `1` si los bits son diferentes, y `0` si son iguales.

```js
let a = 5; //  0101 en binario
let b = 3; //  0011 en binario
let result = a ^ b; // 0110 (6 en decimal)

console.log(result); // Output: 6
```
