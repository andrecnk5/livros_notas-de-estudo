# Operadores de Associação em JavaScript

## Introdução

Operadores de associação são usados para testar se um elemento está presente em um objeto. Eles são essenciais para verificar a presença de um elemento dentro de objetos iteráveis como arrays e strings.

## Lista de Operadores de Associação

Aqui está uma lista dos operadores de associação em JavaScript e exemplos de como são utilizados:

- `includes()`: Verifica se o valor ou variável está presente na sequência.

```javascript
let arr = [1, 2, 3];
console.log(arr.includes(1)); // Saída: true
```

#### Exemplos Práticos

```javascript
let fruits = ["apple", "banana", "mango"];
console.log(fruits.includes("banana")); // Saída: true
console.log(fruits.includes("grape")); // Saída: false
```

- `indexOf()`: Retorna o índice da primeira ocorrência do valor especificado na sequência, ou -1 se não for encontrado.

```javascript
let arr = [1, 2, 3];
console.log(arr.indexOf(1) !== -1); // Saída: true
console.log(arr.indexOf(4) === -1); // Saída: true
```

#### Exemplos Práticos

```javascript
let numbers = [10, 20, 30, 40, 50];
console.log(numbers.indexOf(30) !== -1); // Saída: true
console.log(numbers.indexOf(60) === -1); // Saída: true
```

- `includes()` em Strings: Verifica se a string contém a sequência de caracteres especificada.

```javascript
let str = "Hello, world!";
console.log(str.includes("Hello")); // Saída: true
console.log(str.includes("hello")); // Saída: false (case-sensitive)
```

#### Exemplos Práticos

```javascript
let text = "The quick brown fox jumps over the lazy dog.";
console.log(text.includes("quick")); // Saída: true
console.log(text.includes("Quick")); // Saída: false
```

### Uso em Condições e Loops

Estes operadores são muito úteis para condições e loops para verificar a presença de elementos dentro de coleções.

```javascript
let items = [1, 2, 3, 4, 5];
if (items.includes(3)) {
  console.log("O item 3 está presente na lista.");
} else {
  console.log("O item 3 não está presente na lista.");
}
let phrase = "JavaScript é divertido!";
if (phrase.includes("divertido")) {
  console.log("A frase contém a palavra 'divertido'.");
} else {
  console.log("A frase não contém a palavra 'divertido'.");
}
```

[⬅ Voltar ](README.md)
