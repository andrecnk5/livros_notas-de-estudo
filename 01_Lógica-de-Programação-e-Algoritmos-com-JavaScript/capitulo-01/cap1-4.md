
# Lógica de Programação e Algoritmos com JavaScript

## Capítulo 1: Editores de Código em JavaScript

### 1.4 Editores de Código em JavaScript

Para desenvolver com JavaScript de maneira eficiente, é essencial utilizar um editor de código que ofereça recursos avançados para escrita, formatação e depuração do código. Existem diversos editores disponíveis, mas vamos focar no Visual Studio Code (VS Code), um dos mais populares e amplamente usados pelos desenvolvedores.

#### Visual Studio Code

Visual Studio Code é um editor de código-fonte desenvolvido pela Microsoft. Ele é gratuito, de código aberto e funciona em várias plataformas, incluindo Windows, macOS e Linux. VS Code oferece uma vasta gama de funcionalidades que facilitam o desenvolvimento com JavaScript e outras linguagens.

##### Instalação do Visual Studio Code

Para instalar o Visual Studio Code, siga os passos abaixo:

1. **Acesse o site oficial**: Vá até [code.visualstudio.com](https://code.visualstudio.com/).
2. **Baixe o instalador**: Clique no botão de download e escolha a versão adequada para o seu sistema operacional (Windows, macOS ou Linux).
3. **Execute o instalador**: Após o download, execute o instalador e siga as instruções na tela para completar a instalação.

##### Configuração do Ambiente

Uma vez instalado o VS Code, algumas configurações iniciais podem melhorar sua experiência de desenvolvimento:

1. **Extensões**: O VS Code possui um vasto marketplace de extensões que adicionam funcionalidades ao editor. Para JavaScript, algumas extensões recomendadas são:
   - **ESLint**: Ajuda a identificar e corrigir problemas de código JavaScript.
   - **Prettier**: Um formatador de código que ajuda a manter a consistência do estilo do código.
   - **Debugger for Chrome**: Permite depurar código JavaScript diretamente no navegador Google Chrome.

2. **Configurações do Editor**: No menu lateral esquerdo, clique em `File` > `Preferences` > `Settings` para acessar as configurações do editor. Algumas configurações úteis incluem:
   - **Auto Save**: Habilita a salvamento automático do arquivo.
   - **Format on Save**: Formata o código automaticamente ao salvar o arquivo.

##### Utilizando o Visual Studio Code

Vamos criar um exemplo simples para entender como utilizar o VS Code para desenvolver com JavaScript.

1. **Criação de uma Pasta de Projeto**:
   - Crie uma pasta no seu computador chamada `projeto-js`.
   - Abra essa pasta no VS Code clicando em `File` > `Open Folder` e selecionando a pasta `projeto-js`.

2. **Criação de um Arquivo JavaScript**:
   - Dentro da pasta `projeto-js`, crie um novo arquivo chamado `app.js`.
   - Digite o seguinte código no `app.js`:
     ```javascript
     console.log("Hello, World!");
     ```

3. **Executando o Código**:
   - Para executar o código JavaScript, você pode usar o terminal integrado do VS Code.
   - Abra o terminal clicando em `View` > `Terminal`.
   - No terminal, digite `node app.js` e pressione Enter. Você verá a saída `Hello, World!` no terminal.

##### Depuração no Visual Studio Code

Uma das principais vantagens do VS Code é a integração com ferramentas de depuração. Vamos configurar um exemplo básico para depurar código JavaScript.

1. **Configuração do Debugger**:
   - Clique no ícone de `Run and Debug` na barra lateral esquerda.
   - Clique em `create a launch.json file` e selecione `Node.js`.
   - Um arquivo `launch.json` será criado dentro da pasta `.vscode`.

2. **Definindo um Ponto de Interrupção**:
   - No arquivo `app.js`, clique no lado esquerdo do número da linha onde deseja adicionar um ponto de interrupção.
   - Um ponto vermelho aparecerá indicando que o ponto de interrupção foi adicionado.

3. **Iniciando a Depuração**:
   - Clique no botão `Run` (ícone de play) na barra superior.
   - O VS Code iniciará a depuração e parará no ponto de interrupção definido, permitindo inspecionar variáveis e executar comandos linha por linha.

Com essas configurações e exemplos, você estará pronto para começar a desenvolver e depurar seus programas JavaScript de maneira eficiente utilizando o Visual Studio Code.

