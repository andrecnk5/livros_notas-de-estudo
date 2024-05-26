# O que é o Node.js

Node.js é um ambiente de execução JavaScript construído sobre o motor JavaScript V8 do Google Chrome. Ele permite que os desenvolvedores executem código JavaScript no lado do servidor, permitindo a criação de aplicações web escaláveis, aplicativos de rede e muito mais.

## Características principais:

1. Orientado a Eventos: Node.js utiliza um loop de eventos e callbacks para gerenciar operações assíncronas, como leitura de arquivos e consultas a bancos de dados, permitindo que um único thread gerencie milhares de conexões simultâneas.

2. Non-blocking I/O: Operações de entrada/saída (I/O) em Node.js são não bloqueantes, o que significa que o servidor pode processar outras requisições enquanto aguarda a conclusão de operações I/O.

3. Single-threaded: Embora o Node.js seja single-threaded, ele usa um modelo baseado em eventos para lidar com múltiplas conexões simultâneas de maneira eficiente.

## Vantagens do Node.js

1. Alta Performance: Graças ao motor V8, o Node.js compila JavaScript para código de máquina, resultando em alta performance.
2. Escalabilidade: A arquitetura orientada a eventos do Node.js permite que ele escale horizontalmente (adicionando mais instâncias de servidor) e verticalmente (adicionando mais recursos a uma instância de servidor).
   3.Ampla Comunidade e Ecosistema: O NPM (Node Package Manager) é o maior repositório de pacotes de software do mundo, permitindo que desenvolvedores integrem facilmente bibliotecas e frameworks em seus projetos.

## Instalação e Configuração do Ambiente

Para começar a usar Node.js, é necessário instalá-lo em seu sistema. O Node.js vem com o NPM, que facilita a gestão de pacotes e módulos.

### Passos para instalação no Windows:

1. Download: Acesse o site oficial do Node.js (https://nodejs.org/) e baixe o instalador adequado para o seu sistema.
2. Instalação: Execute o instalador e siga as instruções na tela.
3. Verificação: Abra o prompt de comando e execute node -v e npm -v para verificar as versões instaladas.

### Executando Scripts Node.js

Node.js permite a execução de scripts JavaScript diretamente no terminal.

#### Exemplo:

1. Crie um arquivo chamado app.js:

   ```javascript
   console.log("Hello, Node.js!");
   ```

2. Para executar o script, abra o terminal e digite:

   ```powershell
   node app.js
   ```

   Isso imprimirá Hello, Node.js! no console.

## Diferença entre Node.js e Outros Ambientes de Runtime

Node.js se diferencia de outros ambientes de runtime de várias maneiras:

1. Event Loop: O loop de eventos é um dos componentes mais importantes do Node.js. Ele permite que o Node.js execute operações assíncronas de maneira eficiente, gerenciando várias operações sem bloquear o thread principal.
2. Non-blocking I/O: Em linguagens tradicionais, operações de I/O bloqueiam o thread até que a operação seja concluída. No Node.js, operações de I/O são assíncronas, permitindo que outras operações continuem enquanto aguardam a conclusão de uma operação I/O.
3. Single-Threaded com Callbacks: Enquanto muitas linguagens utilizam múltiplos threads para lidar com concorrência, o Node.js utiliza um único thread e callbacks para gerenciar múltiplas conexões simultâneas. Isso simplifica o desenvolvimento e reduz a complexidade associada à gestão de múltiplos threads.

## Event Loop em Detalhes

O event loop é o mecanismo que permite ao Node.js realizar operações não bloqueantes, mesmo sendo single-threaded. Ele é dividido em várias fases, cada uma responsável por um tipo específico de operações:

1. Timers: Esta fase processa callbacks agendados por setTimeout e setInterval.
   Pending Callbacks: Executa callbacks adiados por operações de I/O.
2. Idle, prepare: Utilizado internamente apenas.
3. Poll: Recupera novos eventos I/O; executa callbacks de I/O (quase todas).
4. Check: Define callbacks setImmediate.
5. Close Callbacks: Executa callbacks de eventos fechados como socket.on('close').

### Exemplo de Event Loop:

#### Finalidade:

O exemplo do event loop ilustra como o Node.js gerencia operações assíncronas. O setTimeout é uma função utilizada para agendar a execução de uma função após um determinado período de tempo, permitindo a execução assíncrona.

##### Código

```javascript
console.log("Primeiro");

setTimeout(() => {
  console.log("Terceiro");
}, 0);

console.log("Segundo");
```

##### Entendendo o código:

- console.log('Primeiro');: Imprime a string 'Primeiro' no console.
- setTimeout(() => {...}, 0);: Agenda a execução da função passada como argumento após 0 milissegundos.
  - setTimeout é uma função do JavaScript que permite executar uma função após um certo período de tempo. O segundo argumento é o tempo em milissegundos após o qual a função deve ser executada.
- console.log('Segundo');: Imprime a string 'Segundo' no console.
- A função agendada por setTimeout (() => { console.log('Terceiro'); }) é executada depois que todas as operações síncronas são concluídas, mesmo que o tempo especificado seja 0 milissegundos. Esta execução ocorre na próxima iteração do loop de eventos.

##### Explicando o Código:

1. Quando o script é executado, o Node.js começa a processar as operações síncronas na sequência em que aparecem.
2. `console.log('Primeiro');` é executado primeiro, imprimindo 'Primeiro' no console.
3. `setTimeout(() => { console.log('Terceiro'); }, 0);` agenda uma operação assíncrona para ser executada após 0 milissegundos. No entanto, como é uma operação assíncrona, ela é enviada para a fila de tarefas a serem executadas na próxima iteração do loop de eventos.
4. `console.log('Segundo');` é executado imediatamente após o agendamento da operação setTimeout, imprimindo 'Segundo' no console.
5. Após todas as operações síncronas serem concluídas, o loop de eventos do Node.js verifica a fila de tarefas assíncronas. Como a função setTimeout foi agendada para ser executada após 0 milissegundos, ela é agora executada, imprimindo 'Terceiro' no console.

##### Saída do Código

```textplain
Primeiro
Segundo
Terceiro
```

Neste exemplo, setTimeout é adiado e processado após o restante do código ser executado

#### O que é setTimeout?

`setTimeout` é uma função do JavaScript que permite executar uma função após um intervalo de tempo especificado. Ela é amplamente utilizada para operações assíncronas, como temporizadores e atrasos na execução de funções.

##### Sintaxe

```javascript
setTimeout(function, delay, ...args);
```

- `function`: A função a ser executada após o tempo de atraso.
- `delay`: O tempo em milissegundos antes da execução da função. Se delay for 0, a função será executada na próxima iteração do loop de eventos.
- `...args`: Argumentos adicionais a serem passados para a função quando ela for executada (opcional).

**Exemplo:**

```javascript
setTimeout(() => {
  console.log("Esta mensagem será exibida após 2 segundos");
}, 2000);
```

Este exemplo agendará a execução da função que imprime a mensagem após 2000 milissegundos (2 segundos).

### Comportamento Assíncrono:

A função setTimeout não bloqueia o thread principal. Em vez disso, ela agenda a função para ser executada após o tempo especificado, permitindo que o thread principal continue executando outras operações. Isso é particularmente útil em aplicações Node.js para manter a responsividade enquanto realiza operações de I/O ou outras tarefas demoradas de maneira assíncrona.

### Conclusão

O event loop é um dos conceitos fundamentais do Node.js, permitindo a execução eficiente de operações assíncronas. O setTimeout é uma das funções que utilizam o event loop para agendar a execução de funções sem bloquear o thread principal, demonstrando a capacidade do Node.js de gerenciar múltiplas operações de forma eficiente e não bloqueante.

## Asynchronous Programming em Node.js

Node.js é altamente eficiente para operações I/O devido à sua natureza assíncrona. Existem várias maneiras de lidar com operações assíncronas:

1. Callbacks: Funções passadas como argumento para outra função, executadas após a conclusão de uma operação.

   ```javascript
   const fs = require("fs");

   fs.readFile("example.txt", "utf8", (err, data) => {
     if (err) {
       console.error(err);
       return;
     }
     console.log(data);
   });
   ```

2. Promises: Um objeto que representa a eventual conclusão (ou falha) de uma operação assíncrona.

   ```javascript
   const fs = require("fs").promises;

   fs.readFile("example.txt", "utf8")
     .then((data) => console.log(data))
     .catch((err) => console.error(err));
   ```

3. Async/Await: Uma sintaxe mais recente para lidar com Promises de forma síncrona.

   ```javascript
   const fs = require("fs").promises;

   async function readFile() {
     try {
       const data = await fs.readFile("example.txt", "utf8");
       console.log(data);
     } catch (err) {
       console.error(err);
     }
   }

   readFile();
   ```

## CommonJS e Módulos ES6

Node.js suporta dois sistemas de módulos: CommonJS e módulos ES6.

**CommonJS:**

```javascript
// adder.js
function add(a, b) {
  return a + b;
}
module.exports = add;

// app.js
const add = require("./adder");
console.log(add(2, 3)); // 5
```

**Módulos ES6:**

```javascript
// adder.mjs
export function add(a, b) {
  return a + b;
}

// app.mjs
import { add } from "./adder.mjs";
console.log(add(2, 3)); // 5
```

Para utilizar módulos ES6, assegure-se de que o arquivo tenha a extensão `.mjs` ou adicione `"type": "module"` no `package.json`.

# Exemplos

- ## Exemplo 1: Olá, Mundo!

  -_Finalidade_: Este exemplo básico mostra como executar um script Node.js simples que imprime uma mensagem no console. Ele serve como uma introdução para entender como o Node.js executa scripts JavaScript fora do navegador.

  _Código_:

  ```javascript
  // Imprime a mensagem 'Hello, Node.js!' no console
  console.log("Hello, Node.js!");
  ```

  _Comentários_:

  - `console.log('Hello, Node.js!');`: Utiliza a função `console.log` para imprimir a string 'Hello, Node.js!' no console.
    Para executar o script:

  _Para executar o script:_

  ```bash
  node hello.js
  ```

- ## Exemplo 2: Servidor HTTP Simples

  _Finalidade_: Este exemplo demonstra como criar um servidor HTTP básico usando Node.js. Ele é fundamental para entender como Node.js pode ser utilizado para construir servidores web que respondem a requisições HTTP.

  _Código_:

  ```javascript
  // Importa o módulo HTTP do Node.js
  const http = require("http");

  // Cria um servidor HTTP
  const server = http.createServer((req, res) => {
    // Define o status da resposta como 200 (OK)
    res.statusCode = 200;
    // Define o cabeçalho da resposta como 'text/plain'
    res.setHeader("Content-Type", "text/plain");
    // Envia a resposta 'Hello, World!' e encerra a resposta
    res.end("Hello, World!\n");
  });

  // Define o servidor para escutar na porta 3000 no endereço '127.0.0.1'
  server.listen(3000, "127.0.0.1", () => {
    // Imprime uma mensagem no console quando o servidor estiver funcionando
    console.log("Server running at http://127.0.0.1:3000/");
  });
  ```

  _Comentários_:

  - `const http = require('http');`: Importa o módulo HTTP do Node.js para criar o servidor.
  - `const server = http.createServer((req, res) => {...});`: Cria um servidor HTTP que responde a requisições.
  - `res.statusCode = 200;`: Define o status da resposta como 200, indicando sucesso.
  - `res.setHeader('Content-Type', 'text/plain');`: Define o tipo de conteúdo da resposta como texto simples.
  - `res.end('Hello, World!\n');`: Envia a resposta 'Hello, World!' ao cliente e encerra a resposta.
  - `server.listen(3000, '127.0.0.1', () => {...});`: Faz o servidor escutar na porta 3000 e no endereço '127.0.0.1'.
  - `console.log('Server running at http://127.0.0.1:3000/');`: Imprime uma mensagem no console quando o servidor estiver funcionando.

        _Para executar o script_:

        ```bash
        node server.js
        ```

    Abra um navegador e acesse http://127.0.0.1:3000/.

- ## Exemplo 3: Leitura de Arquivo

  Finalidade: Este exemplo demonstra como ler o conteúdo de um arquivo utilizando Node.js. É essencial para entender como o Node.js interage com o sistema de arquivos para realizar operações de entrada e saída (I/O).

  Código:

  ```javascript
  // Importa o módulo 'fs' (File System) do Node.js
  const fs = require("fs");

  // Lê o conteúdo do arquivo 'example.txt' de forma assíncrona
  fs.readFile("example.txt", "utf8", (err, data) => {
    // Verifica se ocorreu um erro durante a leitura do arquivo
    if (err) {
      // Imprime o erro no console se ocorreu um erro
      console.error(err);
      return;
    }
    // Imprime o conteúdo do arquivo no console
    console.log(data);
  });
  ```

  Comentários:

  - `const fs = require('fs');`: Importa o módulo de sistema de arquivos (fs) do Node.js.
  - `fs.readFile('example.txt', 'utf8', (err, data) => {...})`;: Lê o conteúdo do arquivo example.txt de forma assíncrona.
  - `if (err) {...}`: Verifica se ocorreu um erro durante a leitura do arquivo.
  - `console.error(err);`: Imprime o erro no console, se houver.
  - `console.log(data);`: Imprime o conteúdo do arquivo no console.

  Para executar o script:

  ```bash
  node readFile.js
  ```

- ## Exemplo 4: Módulo Personalizado

  Finalidade: Este exemplo mostra como criar e utilizar módulos personalizados em Node.js. Módulos são fundamentais para organizar o código em componentes reutilizáveis e manter a base de código limpa e modular.

  Código do Módulo (adicionar.js):

  ```javascript
  // Define uma função que adiciona dois números
  function adicionar(a, b) {
    return a + b;
  }

  // Exporta a função 'adicionar' para que possa ser utilizada em outros arquivos
  module.exports = adicionar;
  ```

  Código Principal (main.js):

  ```javascript
  // Importa o módulo 'adicionar' do arquivo 'adicionar.js'
  const adicionar = require("./adicionar");

  // Usa a função 'adicionar' para somar 3 e 4 e armazena o resultado na variável 'soma'
  const soma = adicionar(3, 4);

  // Imprime o resultado da soma no console
  console.log(`A soma é: ${soma}`);
  ```

  Comentários do Módulo (`adicionar.js`):

  - `function adicionar(a, b) {...}`: Define uma função que recebe dois parâmetros e retorna a soma deles.
  - `module.exports = adicionar;`: Exporta a função `adicionar` para que possa ser utilizada em outros arquivos.

  Comentários do Código Principal (main.js):

  - `const adicionar = require('./adicionar');`: Importa o módulo adicionar do arquivo adicionar.js.
  - `const soma = adicionar(3, 4);`: Usa a função adicionar para somar os números 3 e 4.
  - `console.log(A soma é: ${soma});`: Imprime o resultado da soma no console.

  Para executar o script:

  ```bash
  node main.js
  ```
