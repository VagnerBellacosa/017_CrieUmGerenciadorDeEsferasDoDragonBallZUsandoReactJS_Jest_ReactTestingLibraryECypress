## O que é o Cypress e porque preciso dele ?
##### Raphael Santos

É uma ferramenta de teste rápido, fácil e confiável para qualquer coisa que seja executada em um navegador, para teste de aceitação ou e2e (end-to-end). Veio com propósito de facilitar o processo de configuração, execução e depuração dos seus testes.

## Não é reinventar a roda!

Cypress não é um framework de automação geral, nem é uma estrutura de teste de unidade para seus serviços de back-end afinal existem ótimas ferramentas por aí que fazem isso. É uma excelente ferramenta que traz uma nova experiência enquanto escreve testes end-to-end para seus aplicativos web.

## Outra ferramenta de teste?

Você deve estar se perguntando "Nossa outra ferramenta de teste, já vi inúmeras e nada resolve meu problema, sempre um mar de configuração e detalhes, será mesmo que devo perder meu tempo?"

Calma jovem realmente existe algo diferente e é bem legal.

Alguns dos principais pontos do Cypress.io

- Free e open source.
- Testes em Javascript.
- Continuous Integration.
- Time Travel.
- Real time reloads.
- Automatic waiting.
- Spies, stubs e clocks.
- Controle do tráfego de rede.
- Screenshots e vídeos.
- Testar responsividade em web apps.

Alguns desses pontos você já pode ter visto em outras ferramentas mas será mesmo que conseguiu utiliza-lá de maneira fácil e colocar em prática tudo o que a ferramenta prometia? Mais pra frente irei explicar alguns desses pontos.

## Arquitetura e funcionamento

A imagem abaixo mostra um conjunto de ferramentas e tecnologias que foram utilizadas na construção do Cypress.io. Motivo pela qual se torna um instrumento tão poderoso e ao mesmo tempo intuitivo.

### Acesse a pasta do seu projeto ou crie uma.

$ mkdir cypress-example

Dentro do diretório criado instale o cypress.

$ npm install cypress --save-dev

Após a instalação execute o cypress.

$ ./node_modules/.bin/cypress open

#### Estrutura de diretórios

Confira dentro da pasta do cypress que existem outros diretórios e que cada um deles tem seu objetivo, veja a imagem abaixo.

- Fixtures: É onde seus mocks são armazenados podendo ser utilizados em qualquer teste.
- Integrations: Aqui é o diretório onde criará seus arquivos de teste exemplo : app_spec.js ou .js .jsx .coffee .cjsx.
- Plugins: Com eles é possível trocar, modificar ou estender o comportamento interno do Cypress.

Exemplos de plugins:

- Trocar variáveis de ambiente durante o processo de execução
- Carregar arquivos utilizando a lib fs
- Support: Neste diretório é possível criar comandos que podem ser executados dentro dos testes ou sobrescrever comandos já existentes.

Exemplo de comandos:

- Comando para login ( Evitar duplicação de código)
- Comando para logout

### Como aprender a criar testes com Cypress

Para começar a entender como os testes funcionam acesse a pasta integration. Lá vários arquivos de testes com exemplos foram criados. Ao instalar o cypress recomendo que análise os arquivos na pasta integration pois todos eles serão muito úteis como guia.

Há, não esqueça de apertar o play e ver o cypress em ação e executando todos os testes, fique a vontade também pra modificar os arquivos e ver na prática o que acontece

[Artigo original](https://blog.novatics.com.br/teste-end-to-end-com-cypress-io-358576dc05c3)