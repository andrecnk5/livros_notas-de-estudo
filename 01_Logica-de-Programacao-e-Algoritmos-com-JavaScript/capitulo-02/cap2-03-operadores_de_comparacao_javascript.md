# Operadores de Comparação em JavaScript

## Introdução

Operadores de comparação são utilizados em JavaScript para comparar dois valores. Estes operadores retornam um valor booleano: `true` ou `false` dependendo da condição.

## Lista de Operadores de Comparação

Aqui está uma lista dos operadores de comparação em JavaScript e exemplos de como são utilizados:

- `==`: Igualdade. Verifica se dois valores são iguais (com conversão de tipos, se necessário).

```javascript
let a = 5;
let b = "5";
console.log(a == b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = 10;
let y = "10";
console.log(x == y); // Saída: true
```

- `===`: Estritamente igual. Verifica se dois valores são iguais e do mesmo tipo.

```javascript
let a = 5;
let b = 5;
console.log(a === b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = 10;
let y = 10;
console.log(x === y); // Saída: true
```

- `!=`: Diferença. Verifica se dois valores são diferentes (com conversão de tipos, se necessário).

```javascript
let a = 5;
let b = 3;
console.log(a != b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = 10;
let y = "20";
console.log(x != y); // Saída: true
```

- `!==`: Estritamente diferente. Verifica se dois valores são diferentes ou de tipos diferentes.

```javascript
let a = 5;
let b = "5";
console.log(a !== b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = 10;
let y = "10";
console.log(x !== y); // Saída: true
```

- `>`: Maior que. Verifica se o primeiro valor é maior que o segundo.

```javascript
let a = 5;
let b = 3;
console.log(a > b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = 15;
let y = 10;
console.log(x > y); // Saída: true
```

- `<`: Menor que. Verifica se o primeiro valor é menor que o segundo.

```javascript
let a = 2;
let b = 3;
console.log(a < b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = 5;
let y = 10;
console.log(x < y); // Saída: true
```

- `>=`: Maior ou igual. Verifica se o primeiro valor é maior ou igual ao segundo.

```javascript
let a = 5;
let b = 5;
console.log(a >= b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = 10;
let y = 10;
console.log(x >= y); // Saída: true
```

- `<=`: Menor ou igual. Verifica se o primeiro valor é menor ou igual ao segundo.

```javascript
let a = 3;
let b = 5;
console.log(a <= b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = 5;
let y = 10;
console.log(x <= y); // Saída: true
```

Estes operadores são fundamentais para controle de fluxo em programas, permitindo a execução de blocos de código baseados em condições.

[⬅ Voltar ](README.md)
