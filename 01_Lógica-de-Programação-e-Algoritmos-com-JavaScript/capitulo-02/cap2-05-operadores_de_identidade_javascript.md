# Operadores de Identidade em JavaScript

## Introdução

Operadores de identidade são usados em JavaScript para comparar as identidades dos objetos, não apenas se eles são equivalentes, mas se eles realmente compartilham a mesma localização na memória.

## Lista de Operadores de Identidade

Aqui está uma lista dos operadores de identidade em JavaScript e exemplos de como são utilizados:

- `===`: Verifica se duas variáveis são estritamente iguais, tanto em valor quanto em tipo.

```javascript
let a = [1, 2, 3];
let b = a;
console.log(a === b); // Saída: true
```

#### Exemplos Práticos

```javascript
let obj1 = { name: "Alice" };
let obj2 = obj1;
console.log(obj1 === obj2); // Saída: true

let arr1 = [1, 2, 3];
let arr2 = arr1;
console.log(arr1 === arr2); // Saída: true
```

- `!==`: Verifica se duas variáveis não são estritamente iguais, tanto em valor quanto em tipo.

```javascript
let a = [1, 2, 3];
let b = [1, 2, 3];
console.log(a !== b); // Saída: true
```

#### Exemplos Práticos

```javascript
let obj1 = { name: "Alice" };
let obj2 = { name: "Alice" };
console.log(obj1 !== obj2); // Saída: true

let arr1 = [1, 2, 3];
let arr2 = [1, 2, 3];
console.log(arr1 !== arr2); // Saída: true
```

### Comparando Objetos e Arrays

Em JavaScript, mesmo que dois objetos ou arrays tenham os mesmos valores, eles são considerados diferentes se não referenciam o mesmo espaço na memória.

```javascript
let obj1 = { name: "Alice" };
let obj2 = { name: "Alice" };
console.log(obj1 === obj2); // Saída: false

let arr1 = [1, 2, 3];
let arr2 = [1, 2, 3];
console.log(arr1 === arr2); // Saída: false
```

#### Exemplos Práticos

```javascript
let obj1 = { age: 25 };
let obj2 = { age: 25 };
console.log(obj1 === obj2); // Saída: false
console.log(obj1 !== obj2); // Saída: true

let arr1 = [4, 5, 6];
let arr2 = [4, 5, 6];
console.log(arr1 === arr2); // Saída: false
console.log(arr1 !== arr2); // Saída: true
```

Estes operadores são particularmente úteis para verificar se duas variáveis referenciam o mesmo objeto em memória, o que é diferente de ter o mesmo conteúdo.

[⬅ Voltar ](README.md)
