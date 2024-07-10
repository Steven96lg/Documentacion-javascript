# Documentación Javascript

Este repositorio tiene como fin documentar mis conocimientos para tener un acceso más rápido cuando necesite encontrar una sintaxis o método. Si te es de provecho, siéntete libre de consultarlo y compartirlo.



1. [Metodos de arrays](#array-methods)
2. [Objetos](#objects)
3. [web Workers](#workers)


<div id="array-methods"></div>

## Metodos de arrays

- [Map](#map)
- [Filter](#filter)
- [Find](#find)
- [Includes](#includes)
- [Slice](#slice)
- [Splice](#splice)
- [Concat](#concat)

<div id="map"></div>

### Map

El método map es una función que se aplica a arrays y permite crear un nuevo array con los resultados de aplicar una función a cada uno de los elementos del array original. este método no modifica el array original, retorna un nuevo array.

```javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

const doubleNumbers = numbers.map((num) => num*2);

output: [2,4,6,8,10,12,14,16,18,20]
```

<div id="filter"></div>

### Filter

 crea un nuevo array con todos los elementos que pasan una condicion especifica. Es una forma efectiva de filtrar elementos en un array según ciertos criterios.

```javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// Usamos el método filter para obtener solo los números pares
const evenNumbers = numbers.filter(function(number) {
  return number % 2 === 0;
});

output: [2,4,6,8,10]
```

<div id="find"></div>

### Find

 Devuelve el primer elemento del array que cumple con la condición especificada.
 
 ```javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

const findNumber = numbers.find((num) => {
    // devolvera el primer elemento que cumpla esta condición, en este caso el 6
    return num > 5;
});

output: 6

const names = ["Alice", "Bob", "Charlie", "David", "Eve", "Frank", "Grace", "Hannah"];

const findName = names.find((name) => {
  return name.length < 5;
});

// aunque Eve tambien tiene una longitud menor a 5 el metodo siempre devolvera la primer coincidencia
output: "Bob"
```
<div id="includes"></div>

### Includes

Determina si un array incluye un determinado elemento, devuelve true o false según corresponda.

```javascript
const names = ["Alice", "Bob", "Charlie", "David"];
const getName = names.includes("Charlie");

output: true
```

<div id="slice"></div>

### Slice

Devuelve una copia superficial de una porción del array dentro de un nuevo array desde los indices que le indiquemos, el primer parametro toma desde donde empezara, y el segundo toma un elemento antes del indice indicado.

```javascript
const names = ["Alice", "Bob", "Charlie", "David"];
const getNames = names.slice(1,3);

output: [ 'Bob', 'Charlie' ]
```
<div id="splice"></div>

### Splice

Este metodo modifica el arreglo origial, y nos ayuda a eliminar, añadir o modificar elementos.

```javascript
const names = ["Alice", "Bob", "Charlie", "David"];

/*
    Eliminar elementos
    1er parametro: indice a partir del cual vamos a eliminar elementos.
    2do parametro: cantidad de elementos a eliminar.
*/
names.splice(0,2);
output: ["Charlie", "David"] 

/*
    Añadir elementos
    1er parametro: indice a partir del cual vamos a añadir elementos.
    2do parametro: Lo seteamos a 0 para avitar eliminar elementos.
*/

names.splice(1,0,"Steven", "Ander");
output: [ 'Alice', 'Steven', 'Ander', 'Bob', 'Charlie', 'David' ]

/*
    Reemplazar elementos
    1er parametro: indice a partir del cual vamos a reemplazar los elementos.
    2do parametro: cantidad de elementos que vamos a reemplazar.
*/
names.splice(1,2, "Steven", "Ander");
output: [ 'Alice', 'Steven', 'Ander', 'David']
```

<div id="objects"></div>

### Objetos

```javascript
```

<div id="workers"></div>