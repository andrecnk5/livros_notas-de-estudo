# Lógica de Programação e Algoritmos com JavaScript

## Entrada de Dados com `prompt()`

### 1.7 Entrada de Dados com `prompt()`

Vamos avançar um pouco? Já aprendemos a apresentar uma mensagem na tela em nosso primeiro exemplo. Agora, vamos receber uma informação do usuário e apresentar uma mensagem utilizando essa informação. Para isso, utilizaremos variáveis e aprenderemos um novo comando JavaScript.

### Utilizando o `prompt()`

Uma forma de receber dados do usuário em JavaScript é utilizando o comando (método) `prompt()`, que exibe uma caixa com um texto e um espaço para digitação.

#### Exemplo 1.2 — Entrada de dados e uso de variáveis (ex1_2.html)

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Exemplo 1.2</title>
  </head>
  <body>
    <script>
      const nome = prompt("Qual é o seu nome?");
      alert("Olá " + nome);
      console.log("Olá " + nome);

      // Utilizando Template Strings
      alert("Olá " + nome + ". Para essa mensagem eu usei Template Strings");
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

## Concatenação

#### Definição

Concatenar significa unir ou ligar coisas em uma sequência. No contexto de programação, concatenar geralmente se refere à operação de unir duas ou mais strings (sequências de caracteres) em uma única string.

#### Concatenar em Programação

Na programação, a concatenação é uma operação comum quando precisamos juntar várias partes de texto em uma só. Isso pode ser útil para criar mensagens dinâmicas, formatar saídas de texto, ou construir URLs e consultas de banco de dados, entre outras aplicações.

#### Concatenar em JavaScript

Em JavaScript, há várias maneiras de concatenar strings. Vamos explorar as principais:

1. **Operador de Concatenação (`+`)**: O operador `+` é a maneira mais simples e direta de concatenar strings em JavaScript.

   ```javascript
   let saudacao = "Olá, ";
   let nome = "Maria";
   let mensagem = saudacao + nome;
   console.log(mensagem); // Saída: "Olá, Maria"
   ```

2. **Método `concat()`**: O método `concat()` pode ser usado para concatenar duas ou mais strings. Embora menos comum que o operador `+`, ainda é uma opção válida.

   ```javascript
   let saudacao = "Olá, ";
   let nome = "João";
   let mensagem = saudacao.concat(nome);
   console.log(mensagem); // Saída: "Olá, João"
   ```

3. **Template Strings (Template Literals)**: Template strings, delimitadas por crases (`), permitem a inclusão de expressões dentro de placeholders (`${}`), oferecendo uma maneira mais legível e conveniente de concatenar strings e incluir variáveis.

   ```javascript
   let saudacao = "Olá";
   let nome = "Ana";
   let mensagem = `${saudacao}, ${nome}!`;
   console.log(mensagem); // Saída: "Olá, Ana!"
   ```

4. **Saudação Personalizada**: Neste exemplo, pedimos ao usuário seu nome e concatenamos com uma mensagem de saudação.

   ```javascript
   <!DOCTYPE html>
   <html>
   <head>
     <meta charset="UTF-8">
     <title>Saudação Personalizada</title>
   </head>
   <body>
     <script>
       // Solicita o nome do usuário
       const nome = prompt("Qual é o seu nome?");
       // Cria uma mensagem de saudação concatenando strings
       const saudacao = "Olá, " + nome + "! Seja bem-vindo!";
       // Exibe a mensagem concatenada
       alert(saudacao);
     </script>
   </body>
   </html>
   ```

5. **Calculando Idade**: Neste exemplo, pedimos ao usuário seu ano de nascimento e calculamos sua idade atual, concatenando o resultado em uma mensagem.

   ```javascript
   <!DOCTYPE html>
   <html>
   <head>
     <meta charset="UTF-8">
     <title>Calculando a Idade</title>
   </head>
   <body>
     <script>
       // Solicita o ano de nascimento do usuário
       const anoNascimento = prompt("Em que ano você nasceu?");
       // Calcula a idade
       const anoAtual = new Date().getFullYear();
       const idade = anoAtual - anoNascimento;
       // Cria uma mensagem informando a idade
       const mensagem = "Você tem " + idade + " anos.";
       // Exibe a mensagem concatenada
       alert(mensagem);
     </script>
   </body>
   </html>
   ```

6. **Informações de Contato**: Neste exemplo, pedimos ao usuário seu nome e seu e-mail e concatenamos essas informações em uma mensagem.

   ```javascript
   <!DOCTYPE html>
   <html>
   <head>
     <meta charset="UTF-8">
     <title>Informações de Contato</title>
   </head>
   <body>
     <script>
       // Solicita o nome do usuário
       const nome = prompt("Qual é o seu nome?");
       // Solicita o e-mail do usuário
       const email = prompt("Qual é o seu e-mail?");
       // Cria uma mensagem concatenando o nome e o e-mail
       const contato = "Nome: " + nome + "\nE-mail: " + email;
       // Exibe a mensagem concatenada
       alert(contato);
     </script>
   </body>
   </html>
   ```

7. **Criação de URL Dinâmica**: Neste exemplo, pedimos ao usuário um ID e concatenamos para formar uma URL dinâmica.

   ```javascript
   <!DOCTYPE html>
   <html>
   <head>
     <meta charset="UTF-8">
     <title>URL Dinâmica</title>
   </head>
   <body>
     <script>
       // Solicita o ID do usuário
       const userID = prompt("Digite seu ID:");
       // Cria uma URL dinâmica concatenando strings
       const url = "https://meusite.com/usuario/" + userID;
       // Exibe a URL concatenada
       alert("Sua URL é: " + url);
     </script>
   </body>
   </html>
   ```

8. **Template Literals com `prompt()`**: Aqui está um exemplo de uso de template literals para a concatenação:

   ```javascript
   <!DOCTYPE html>
   <html>
   <head>
     <meta charset="UTF-8">
     <title>Template Literals com Prompt</title>
   </head>
   <body>
     <script>
       // Solicita o primeiro nome do usuário
       const primeiroNome = prompt("Qual é o seu primeiro nome?");
       // Solicita o sobrenome do usuário
       const sobrenome = prompt("Qual é o seu sobrenome?");
       // Cria uma mensagem usando template literals
       const mensagem = `Olá, ${primeiroNome} ${sobrenome}! Seja bem-vindo!`;
       // Exibe a mensagem concatenada
       alert(mensagem);
     </script>
   </body>
   </html>
   ```

   ## Conclusão

   Concatenar strings é uma operação fundamental em programação, e JavaScript oferece várias maneiras de fazer isso de forma eficiente. Seja usando o operador `+`, o método `concat()`, ou template strings, a concatenação permite criar textos dinâmicos e manipulá-los de maneira flexível.
