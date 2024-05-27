
# Lógica de Programação e Algoritmos com JavaScript

## Capítulo 1: Entrada de Dados com `prompt()`

### 1.7 Entrada de Dados com `prompt()`

Vamos avançar um pouco? Já aprendemos a apresentar uma mensagem na tela em nosso primeiro exemplo. Agora, vamos receber uma informação do usuário e apresentar uma mensagem utilizando essa informação. Para isso, utilizaremos variáveis e aprenderemos um novo comando JavaScript.

### Utilizando o `prompt()`

Uma forma de receber dados do usuário em JavaScript é utilizando o comando (método) `prompt()`, que exibe uma caixa com um texto e um espaço para digitação.

#### Exemplo 1.2 — Entrada de dados e uso de variáveis (ex1_2.html)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Exemplo 1.2</title>
</head>
<body>
  <script>
    const nome = prompt("Qual é o seu nome?");
    alert("Olá " + nome);
  </script>
</body>
</html>
```

### Detalhes do Programa

1. **Meta Tag**: Antes do código JavaScript, adicionamos uma metatag HTML para ajustar os caracteres de acentuação a serem exibidos pela página.

2. **Declaração de Variável e `prompt()`**:
    ```javascript
    const nome = prompt("Qual é o seu nome?");
    ```
    - Esse comando declara a variável `nome` e executa o método `prompt()`.
    - O nome digitado pelo usuário na caixa de diálogo do `prompt` é atribuído à variável `nome`.

3. **Exibição de Mensagem com `alert()`**:
    ```javascript
    alert("Olá " + nome);
    ```
    - O método `alert()` exibe uma mensagem na tela.
    - A mensagem é uma combinação de um texto fixo (`"Olá "`) e o conteúdo da variável `nome`.
    - O resultado será a exibição da palavra "Olá", seguida do nome digitado pelo usuário.

### Template Strings

Outra forma de exibir mensagens que contenham um texto fixo e o conteúdo de uma variável em JavaScript é com o uso de Template Strings. Para isso, delimite a mensagem com crases (\`) e insira o nome das variáveis usando a sintaxe: `${nomeVar}`.

#### Exemplo com Template Strings

```javascript
alert(`Olá ${nome}`);
```

### Pontuação Opcional

O uso do ponto e vírgula (`;`) no final dos comandos em programas JavaScript é opcional, mas é uma boa prática usá-lo para evitar possíveis erros.

