# Gerencia Esferas

## Jest

Jest é um poderoso Framework de Testes em JavaScript com um foco na simplicidade.

It works with projects using: Babel, TypeScript, Node, React, Angular, Vue and more!

### zero configuração

Jest visa trabalhar fora da caixa, sem configuração, na maioria dos projetos JavaScript.

### snapshots

Faça testes que tenham objetos grandes com facilidade. Snapshots vivem ao lado de seus testes, ou embutidos.

### isolado

Os testes são paralelos e executados em seus próprios processos para maximizar o desempenho.

### excelente api

De it para expect - Jest tem todo o conjunto de ferramentas em um só lugar. Bem documentado e mantido.

### RÁPIDO E SEGURO

Ao garantir que seus testes têm um estado global único, Jest pode executar testes em paralelo de forma confiável. Para tornar as coisas rápidas, Jest executa testes anteriores falharam primeiro e organiza novamente com base no quanto os arquivos de teste demoram.

### COBERTURA DE CÓDIGO

Generate code coverage by adding the flag --coverage. No additional setup needed. Jest can collect code coverage information from entire projects, including untested files.

### SIMULAÇÕES FÁCEIS

Jest uses a custom resolver for imports in your tests, making it simple to mock any object outside of your test’s scope. You can use mocked imports with the rich Mock Functions API to spy on function calls with readable test syntax.

### EXCEÇÕES CLARAS

Testes falham, quando eles ocorrem o Jest fornece um contexto rico do porque falhou, aqui estão alguns exemplos:

### FILOSOFIA

Jest é um framework de teste em JavaScript projetado para garantir a correção de qualquer código JavaScript. Ele permite que você escreva testes com uma API acessível, familiar e rica em recursos que lhe dá resultados rapidamente.

Jest está bem documentado, requer pouca configuração e pode ser estendido para corresponder aos seus requisitos.

Jest torna os testes agradavéis.

##Iniciando

Instale Jest usando yarn:

yarn add --dev jest

Ou npm:

npm install --save-dev jest

Nota: A documentação do Jest usa comandos do yarn, mas com o npm também funcionará. Você pode comparar comandos yarn e npm aqui.

Vamos começar por escrever um teste para uma função hipotética que soma dois números. Primeiro, crie um arquivo sum.js:

function sum(a, b) {
  return a + b;
}
module.exports = sum;

Em seguida, crie um arquivo chamado sum.test.js. Este irá conter o nosso teste real:

const sum = require('./sum');

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});

Adicione a seguinte seção ao seu package.json:

{
  "scripts": {
    "test": "jest"
  }
}

Por fim, execute yarn test ou npm run test e o Jest irá imprimir esta mensagem:

PASS  ./sum.test.js

✓ adds 1 + 2 to equal 3 (5ms)

Você escreveu com sucesso seu primeiro teste usando Jest!

Este teste usou expect e toBe para testar que dois valores eram exatamente idênticos. Para saber mais sobre as outras coisas que Jest pode testar, consulte Usando Matchers.

Executando a partir da linha de comando#

Você pode executar Jest diretamente da CLI (se ele estiver disponível globalmente em seu PATH, por exemplo: yarn global add jest ou npm install -g jest) com uma variedade de comandos úteis.

Aqui vemos como executar Jest em arquivos que correspondam ao my-test, usando config.json como um arquivo de configuração e exibir uma notificação nativa no Sistema Operacional após a execução:

jest my-test --notify --config=config.json

Se você gostaria de aprender mais sobre como executar jest através da linha de comando, dê uma olhada na página Opções de CLI Jest.

### Configuração adicional#

Gerando um arquivo de configuração básico#

Com base no seu projeto, o Jest fará algumas perguntas e irá criar um arquivo básico de configuração com uma breve descrição para cada opção:

jest --init
Usando Babel#

Para usar Babel, instale as dependências necessárias via yarn:

yarn add --dev babel-jest @babel/core @babel/preset-env

Configure o Babel para marcar a sua versão atual do Node criando um arquivo babel.config.js na raiz do seu projeto:

// babel.config.js
module.exports = {
  presets: [['@babel/preset-env', {targets: {node: 'current'}}]],
};

A configuração ideal para Babel dependerá do seu projeto. Veja Docs do Babel para mais detalhes.

**Making your Babel config jest-aware**
**Babel 6 support**

Usando webpack#

Jest pode ser usado em projetos que usam webpack para gerenciar assets, estilos e compilação. webpack oferece alguns desafios únicos em relação à outras ferramentas. Consulte o guia do webpack para começar.

Usando Parcel#

Jest pode ser usado em projetos que usam parcel-bundler para gerenciar ativos, estilos, e compilação semelhante ao webpack. Parcel requer configuração zero. Consulte a documentação oficial da para começar.

Usando TypeScript#

O Jest suporta TypeScript, via Babel. Primeiro certifique-se que você seguir as instruções em usando o Babel acima. Em seguida, instale o @babel/preset-typescript via yarn:

yarn add --dev @babel/preset-typescript

Então adicione o @babel/preset-typescript à lista de presets em seu babel.config.js.

// babel.config.js
module.exports = {
  presets: [
    ['@babel/preset-env', {targets: {node: 'current'}}],
+ '@babel/preset-typescript',
  ],
};

No entanto, há algumas [ressalvas](https://babeljs. io/docs/en/babel-plugin-transform-typescript#caveats) para usar TypeScript com Babel. Como o suporte para TypeScript em Babel é puramente transpilação, Jest não irá checar seus testes enquanto eles são executados. Se você quiser isso, você pode usar ts-jest em vez disso. ou apenas execute o compilador TypeScript tsc separadamente (ou como parte de seu processo de compilação).

Você também pode querer instalar o módulo @types/jest para a versão do Jest que você está usando. Isso ajudará a fornecer a digitação completa ao escrever seus testes com TypeScript.

Para @types/* módulos, é recomendado tentar corresponder à versão do módulo associado. Por exemplo, se você estiver usando 26.4.0 do jest então usar 26.4.x de @types/jest é ideal. Em geral, tente corresponder à versão principal (26) e com uma versão menor (4) o mais próximo possível.

yarn add --dev @types/jest

[Artigo Original](https://jestjs.io/pt-BR/docs/getting-started)