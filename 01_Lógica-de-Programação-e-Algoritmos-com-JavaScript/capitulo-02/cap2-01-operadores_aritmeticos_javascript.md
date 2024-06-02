# Operadores Aritméticos em JavaScript

## Introdução

Os operadores aritméticos são utilizados para realizar operações matemáticas básicas em JavaScript. Eles são fundamentais para qualquer tipo de cálculo numérico dentro do programa.

## Lista de Operadores Aritméticos

Aqui está uma lista dos operadores aritméticos disponíveis em JavaScript e como eles são usados:

- `+`: Adição. Soma dois valores.

  ```javascript
  let a = 5;
  let b = 3;
  console.log(a + b); // Saída: 8
  ```

- `-`: Subtração. Subtrai o segundo valor do primeiro.

  ```javascript
  let a = 5;
  let b = 3;
  console.log(a - b); // Saída: 2
  ```

- `*`: Multiplicação. Multiplica dois valores.

  ```javascript
  let a = 5;
  let b = 3;
  console.log(a * b); // Saída: 15
  ```

- `/`: Divisão. Divide o primeiro valor pelo segundo, resultando em um float.

  ```javascript
  let a = 5;
  let b = 3;
  console.log(a / b); // Saída: 1.6666666666666667
  ```

- `//`: Divisão inteira. (Não existe um operador específico para divisão inteira em JavaScript, mas podemos usar `Math.floor` para isso).

  ```javascript
  let a = 5;
  let b = 3;
  console.log(Math.floor(a / b)); // Saída: 1
  ```

- `%`: Módulo. Retorna o resto da divisão do primeiro valor pelo segundo.

  ```javascript
  let a = 5;
  let b = 3;
  console.log(a % b); // Saída: 2
  ```

- `**`: Exponenciação. Eleva o primeiro valor à potência do segundo.

  ```javascript
  let a = 5;
  let b = 3;
  console.log(a ** b); // Saída: 125javascript
  ```

Estes operadores são a base para manipulação de números em JavaScript e são utilizados em uma ampla variedade de aplicações matemáticas e algorítmicas.

## Exemplos Práticos

### Adição

A adição é usada para somar dois valores. Pode ser usada com números ou strings (neste caso, ela concatenará as strings).

```javascript
let x = 10;
let y = 20;
let resultado = x + y;
console.log(resultado); // Saída: 30

let str1 = "Hello, ";
let str2 = "World!";
let mensagem = str1 + str2;
console.log(mensagem); // Saída: "Hello, World!"
```

### Subtração

A subtração é usada para subtrair um valor de outro.

```javascript
let x = 10;
let y = 5;
let resultado = x - y;
console.log(resultado); // Saída: 5
```

### Multiplicação

A multiplicação multiplica dois valores.

```javascript
let x = 10;
let y = 5;
let resultado = x * y;
console.log(resultado); // Saída: 50
```

### Divisão

A divisão divide um valor pelo outro.

```javascript
let x = 10;
let y = 2;
let resultado = x / y;
console.log(resultado); // Saída: 5
```

### Divisão Inteira

A divisão inteira pode ser obtida usando `Math.floor` para arredondar o resultado da divisão para baixo.

```javascript
let x = 10;
let y = 3;
let resultado = Math.floor(x / y);
console.log(resultado); // Saída: 3
```

### Módulo

O operador de módulo retorna o resto da divisão de dois valores.

```javascript
let x = 10;
let y = 3;
let resultado = x % y;
console.log(resultado); // Saída: 1
```

### Exponenciação

A exponenciação eleva um valor à potência de outro.

```javascript
let x = 2;
let y = 3;
let resultado = x ** y;
console.log(resultado); // Saída: 8
```

Estes exemplos mostram como usar os operadores aritméticos em JavaScript para realizar cálculos básicos. Esses operadores são essenciais para desenvolver uma variedade de funcionalidades em suas aplicações.

[⬅ Voltar ](README.md)
