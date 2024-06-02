# Operadores Lógicos em JavaScript

## Introdução

Operadores lógicos são usados para combinar declarações condicionais em JavaScript. Eles são fundamentais para a construção de expressões lógicas complexas e para o controle de fluxo em programas.

## Lista de Operadores Lógicos

Aqui está uma lista dos operadores lógicos em JavaScript e exemplos de como são utilizados:

- `&&`: O operador `&&` (**E**) retorna `true` se ambas as declarações forem verdadeiras.

```javascript
let a = true;
let b = true;
console.log(a && b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = 5;
let y = 10;
console.log(x > 0 && y > 0); // Saída: true
console.log(x > 0 && y < 0); // Saída: false
```

- `||`: O operador `||` (**OU**) retorna `true` se pelo menos uma das declarações for verdadeira.

```javascript
let a = true;
let b = false;
console.log(a || b); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = -5;
let y = 10;
console.log(x > 0 || y > 0); // Saída: true
console.log(x > 0 || y < 0); // Saída: false
```

- `!`: O operador `!` (**NOT**) inverte o valor booleano da declaração.

```javascript
let a = false;
console.log(!a); // Saída: true
```

#### Exemplos Práticos

```javascript
let x = true;
console.log(!x); // Saída: false

let y = false;
console.log(!y); // Saída: true
```

Estes operadores são usados para avaliar condições em estruturas como `if`, `while` e outras lógicas de decisão.

## Exemplos de Uso em Estruturas Condicionais

### `if` e `else`

```javascript
let age = 20;
if (age > 18 && age < 30) {
  console.log("Você está na faixa etária jovem adulta.");
} else {
  console.log("Você está fora da faixa etária jovem adulta.");
}
```

### `while`

```javascript
let number = prompt("Digite um número entre 1 e 10:");
number = parseInt(number);

let count = 0;

while (count < number && count >= 0) {
  console.log("O contador é: " + count);
  count++;
}
```

### `for`

```javascript
let number = prompt("Digite um número:");
number = parseInt(number); // Converte a entrada para número inteiro

let count = 0;

for (let i = 1; i <= number; i++) {
  if (i % 2 === 0) {
    console.log(i + " é par");
    count++;
  }
}

console.log("O número de números pares até " + number + " é: " + count);
alert("O número de números pares até " + number + " é: " + count);
```

Estes exemplos mostram como usar os operadores lógicos para controlar o fluxo de execução de programas em JavaScript.

[⬅ Voltar ](README.md)
