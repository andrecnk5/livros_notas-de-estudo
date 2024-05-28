# Tipos de Dados e Conversões de Tipos

As variáveis manipuladas em um programa são de tipos específicos. Em JavaScript, os tipos principais de dados são strings (variáveis de texto), números e valores booleanos (true ou false). Conhecer o tipo de uma variável nos permite identificar quais operações são possíveis para essa variável e prever seu comportamento em expressões. Vamos explorar algumas particularidades da linguagem JavaScript relacionadas aos tipos de dados e conversões, utilizando o Exemplo 1.3 para ilustrar.

## Exemplo - Operações Envolvendo Strings e Números (ex1_3.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Exemplo 1.3</title>
</head>
<body>
  <script>
    const a = "20";

    const b = a * 2;  // b = 40
    const c = a / 2;  // c = 10
    const d = a - 2;  // d = 18
    const e = a + 2;  // e = 202 ???

    alert("e: " + e);  // exibe o valor de uma variável
  </script>
</body>
</html>
```



Neste exemplo, temos uma variável do tipo string que recebe "20" (`const a = "20"`). Ela é entendida como uma string por estar delimitada por aspas. Nas operações de multiplicação, divisão e subtração, a linguagem converte automaticamente o texto em número, retornando valores esperados. Contudo, ao realizar a adição, o resultado é diferente do padrão, pois a linguagem concatena (`+`) a string com o número, resultando em "202".

Para resolver este problema, precisamos converter explicitamente a string em número. Isso pode ser feito em JavaScript utilizando os métodos `Number()`, `parseInt()` e `parseFloat()`. Vamos utilizar o método `Number()` para simplificar o processo de aprendizagem:

```javascript
const e = Number(a) + 2;  // e = 22
```

Agora, a variável `a` é convertida para número antes da adição, resultando em 22.

Caso seja necessário converter um número em string, por exemplo, para usar métodos de manipulação de strings, podemos utilizar o método `toString()`. Este método será utilizado em alguns exemplos ao longo deste livro.

Em JavaScript, não é obrigatório definir o tipo da variável na sua declaração. A variável assume um tipo no momento da atribuição de valor. A atribuição de um valor entre aspas (simples ou dupla) cria uma variável do tipo String. Para variáveis numéricas, não devem ser usadas aspas. As variáveis booleanas podem conter os valores `true` ou `false`. Elas serão exploradas em detalhes nos próximos capítulos. As entradas de dados realizadas com o método `prompt()` criam variáveis do tipo String, exceto se hou...

Exibir uma variável que não recebeu um valor atribuído resultará em "undefined". O Exemplo 1.4 demonstra como declarar variáveis e exibir seus tipos usando o comando `typeof`.

## Exemplo 1.4 — Tipos de Variáveis (ex1_4.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Exemplo 1.4</title>
</head>
<body>
  <script>
    const fruta = "Banana";
    const preco = 3.50;
    const levar = true;
    let novoValor;

    console.log(typeof fruta); // string
    console.log(typeof preco); // number
    console.log(typeof levar); // boolean
    console.log(typeof novoValor); // undefined
  </script>
</body>
</html>
```

A declaração de uma variável ou constante com `const` exige uma atribuição de valor, que se manterá fixa durante o programa ou bloco de código onde foi declarada. Além de verificar se uma variável é do tipo `number`, também é possível verificar se o número é inteiro ou possui decimais usando `Number.isInteger()`:

```javascript
console.log(Number.isInteger(12));    // true
console.log(Number.isInteger(3.50));  // false
```

## Conclusão

Compreender os tipos de dados e as conversões em JavaScript é essencial para escrever códigos precisos e eficientes. As conversões automáticas podem ser úteis, mas também podem levar a resultados inesperados se não forem bem compreendidas. Utilize os métodos de conversão adequados para garantir que suas operações aritméticas e de concatenação se comportem conforme o esperado.