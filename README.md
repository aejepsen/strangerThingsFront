Boas vindas ao repositório do projeto Stranger Things!
Para realizar o projeto, atente-se a cada passo descrito a seguir, e se tiver qualquer dúvida, nos envie por Slack! #vqv rocket

Aqui você vai encontrar os detalhes de como estruturar o desenvolvimento do seu projeto a partir deste repositório, utilizando uma branch específica e um Pull Request para colocar seus códigos.

Termos e acordos
Ao iniciar este projeto, você concorda com as diretrizes do Código de Conduta e do Manual da Pessoa Estudante da Trybe.

Entregáveis
🤷🏽‍♀️ Como entregar
man_technologist O que deverá ser desenvolvido

Você vai adaptar e configurar os projetos descritos nesse README para que seja feito o deploy deles. Você vai colocar os projetos front-end e back-end no ar com o Heroku, utilizando o Docker em ambiente de produção. Além disso, você vai alterar alguns comportamentos aplicando os conceitos vistos no conteúdo.

Desenvolvimento
Adapte e configure os projetos descritos nesse README para que seja feito o deploy utilizando Docker por meio do Heroku.

spiral_calendar Data de Entrega

Este projeto é individual
São 1 dias de projeto
Data para entrega final do projeto: 01/08/2022 - 14:00h
Orientações
bangbang Antes de começar a desenvolver

Clone os dois repositórios:
Clone o repositório de front-end
Clone o repositório de back-end
Navegue entre as pastas dos repositórios que você acabou de clonar:
utilize o comando cd para entrar na pasta criada do projeto
Instale as dependências dos dois projetos:
npm install
Para rodar localmente os projetos, execute o script de start do package.json:
npm start
Crie uma branch a partir da branch master para cada um dos repositórios:
Verifique se você está na branch master
Exemplo: git branch.
Se você não estiver na branch master, mude para a branch master
Exemplo: git checkout master
Agora crie uma branch à qual você vai submeter os commits dos seus projetos:
Você deve criar uma branch no seguinte formato: nome-de-usuario-nome-do-projeto
Exemplo:
git checkout -b joaozinho-sd-0x-stranger-things-backend
git checkout -b joaozinho-sd-0x-stranger-things-frontend
Adicione a sua branch com o novo commit ao repositório remoto:
Usando o exemplo anterior:
git push -u origin joaozinho-sd-0x-stranger-things-backend
git push -u origin joaozinho-sd-0x-stranger-things-frontend
Crie um novo Pull Request (PR):
Vá até a página de Pull Requests dos repositórios no GitHub: Backend | Frontend;

Clique no botão verde "New pull request";

Clique na caixa de seleção "Compare" e escolha a sua branch com atenção;

Clique no botão verde "Create pull request";

Adicione uma descrição para o Pull Request e clique no botão verde "Create pull request";

Não se preocupe em preencher mais nada por enquanto!;

Volte até a página de Pull Requests do repositório e confira se o seu Pull Request está criado;

Volte até a página de Pull Requests do repositório e confira se o seu Pull Request está criado;

warning Observação: Os PRs não devem ser abertos neste repositório, apenas nos outros dois repositórios. warning

keyboard Durante o desenvolvimento

warning PULL REQUESTS COM ISSUES NO LINTER NÃO SERÃO AVALIADAS. ATENTE-SE PARA RESOLVÊ-LAS ANTES DE FINALIZAR O DESENVOLVIMENTO! warning

Faça commits das alterações que você realizar no código regularmente.

Lembre-se de sempre atualizar o repositório remoto após um (ou alguns) commits.

Os comandos que você utilizará com mais frequência são:

git status (para verificar o que está em vermelho - fora do stage - e o que está em verde - no stage);
git add (para adicionar arquivos ao stage do Git);
git commit (para criar um commit com os arquivos que estão no stage do Git);
git push -u nome-da-branch (para enviar o commit para o repositório remoto na primeira vez que fizer o push de uma nova branch);
git push (para enviar o commit para o repositório remoto após o passo anterior).
handshake Depois de terminar o desenvolvimento (opcional)

Para sinalizar que o seu projeto está pronto para o "Code Review" dos seus colegas, faça o seguinte:

Vá até a página DO SEU Pull Request, adicione a label de "code-review" e marque seus colegas:

No menu à direita, clique no link "Labels" e escolha a label code-review;

No menu à direita, clique no link "Assignees" e escolha o seu usuário;

No menu à direita, clique no link "Reviewers" e digite students, selecione o time tryber/students-sd-0x.

Caso tenha alguma dúvida, aqui tem um video explicativo.

warning Lembre-se que garantir que todas as issues comentadas pelo Linter estão resolvidas! warning

🕵🏿 Revisando um pull request

Use o conteúdo sobre Code Review para te ajudar a revisar os Pull Requests.

control_knobs Linter

Usaremos o ESLint para fazer a análise estática do seu código.

Este projeto já vem com as dependências relacionadas ao linter configuradas nos arquivos package.json.

Para poder rodar o ESLint em um projeto basta executar o comando npm install dentro do projeto e depois npm run lint. Se a análise do ESLint encontrar problemas no seu código, tais problemas serão mostrados no seu terminal. Se não houver problema no seu código, nada será impresso no seu terminal.

Você pode também instalar o plugin do ESLint no VSCode. Para isso, basta fazer o download do plugin ESLint e instalá-lo.

hammer_and_wrench Testes

Backend
Todos os requisitos do projeto serão testados automaticamente por meio do Jest. Basta executar o comando abaixo:

npm test
Frontend
Todos os requisitos do projeto serão testados automaticamente por meio do Cypress. Basta executar um dos comandos abaixo:

npm run cypress:open // (Com interface)
npm run cy // (via CLI)
building_construction Deploy - Stranger Things

Esse repositório contém as instruções e os requisitos para o projeto de Deploy com Heroku. O código base para o desenvolvimento do projeto está dividido em duas partes: a)uma API de back-end utilizando Node.js e Express; e b)um front-end com React. Abaixo estão disponíveis os links de acesso aos respectivos repositórios:

Repositório com o back-end [Tribo A] [Tribo B] [Tribo C]

Repositório com o front-end [Tribo A] [Tribo B] [Tribo C]

A seguir, temos algumas explicações sobre a estrutura base e alguns comportamentos dessas aplicações. Você explorará esses pontos durante o projeto, alterando o código preexistente.

Lembre-se de que se tratam de projetos base. Sendo assim, ao longo do desenvolvimento, você vai identificar pontos a serem alterados com o objetivo de aplicar as práticas que vimos durante o curso. Mas não se preocupe, pois no README deste repositório esses pontos estão especificados.

Back-end
O Back-end possui a seguinte estrutura:

├── README.md
├── index.js
├── data
│  ├── dataset
│  │  └── stranger-things-characters.json
│  └── repository
│     └── StrangerThings.js
├── services
│  └── StrangerThings.js
├── package-lock.json
└── package.json
API
A API consiste em um serviço simples com um endpoint / que retorna uma listagem com os personagens da série Stranger Things.

Resposta
A lista de personagem possui os seguintes campos:

name: Nome da personagem;

status: se a personagem está viva ou não na série. Os valores possíveis são alive, deceased ou unknown;

origin: o local de origem da personagem.

A resposta é em formato JSON, e o retorno é sempre um array de objetos. Abaixo, um exemplo:

[
  {
    "name": "Will",
    "status": "Alive",
    "origin": "Byers Family"
  }
]
Filtros
Todos os campos da estrutura de retorno da resposta podem ser utilizados como filtros. Para isso, basta passar na query string o filtro desejado. No exemplo abaixo, estamos filtrando pelo nome do personagem:

localhost:3000?name=el

Os filtros são feitos utilizando uma regex, buscando pelo texto passado na query string em qualquer parte do campo, sem diferenciar maiúsculas de minúsculas.

Nesse caso o retorno seria:

[
  {
    "name":"Russell",
    "status":"Alive",
    "origin":"Hawkings Middle School"
  },
  {
    "name":"Eleven",
    "status":"Alive",
    "origin":"Hopper Family"
  }
]
Modo upside down (dw) - Back-end
Na API, no arquivo index.js, há a seguinte variável de controle:

const hereIsTheUpsideDown = true;
Caso ela seja true, a API ativará o modo "Mundo Invertido", conforme a série, e começará a responder desta forma:

[
  {
    "name":"llǝssnᴚ",
    "origin":"looɥɔS ǝlppᴉW sƃuᴉʞʍɐH",
    "status":"ǝʌᴉl∀"
  },
  {
    "name":"uǝʌǝlƎ",
    "origin":"ʎlᴉɯɐℲ ɹǝddoH",
    "status":"ǝʌᴉl∀"
  }
]
Front-end
O front-end consiste em um projeto simples utilizando React, que renderizará o seguinte layout:


Trata-se de um front-end bem simples que vai se comunicar com a nossa API. Ele possui as seguintes funcionalidades:

Uma tabela para exibição da resposta da nossa API;

Um campo de pesquisa para filtro de nome;

Botões de navegação para paginação;

Um botão para ativar o modo Mundo Invertido no front-end.

Todas essas funcionalidades estão implementadas no componente StrangerThings.

Comunicação com o back-end
Na estrutura do projeto, temos um diretório services. Nesse diretório, há um arquivo charactersAPI.js, onde são feitas as chamadas HTTP para a nossa API, utilizando o axios.

O service é uma classe que espera receber a URL da nossa API e um timeout para a requisição:

{
  url: 'localhost:3003',
  timeout: 30000
}
Esses parâmetros estão pré-programados de maneira fixa no componente (alteraremos esse comportamento durante o projeto):

const strangerThingsConfig = {
  url: 'localhost:3002',
  timeout: 30000,
};

const upsideDownConfig = {
  url: 'localhost:3003',
  timeout: 30000,
};

const charactersService = new CharactersService(strangerThingsConfig);
const charactersUpsideDownService = new CharactersService(upsideDownConfig);
Modo upside down (dw) - Front-end
Assim como no back-end, o front-end também possui um modo "Mundo Invertido". Esse modo é ativado e desativado com o botão "Mudar de Realidade".

A ideia é a seguinte: inicialmente, o front-end possui uma imagem de background e utiliza o service instanciado com a configuração contida na variável strangerThingsConfig. Ao ativar o Mundo Invertido, a imagem de background é alterada e passamos a utilizar o serviço instanciado com a configuração upsideDownConfig.

Desse modo, ao "alternar entre os universos", vamos realizar chamadas a API's diferentes.

No exemplo pré-programado, em um dos "universos", chamamos um serviço na porta 3002 e o outro serviço na porta 3003. Exploraremos esse comportamento durante o projeto.

convenience_store Desenvolvimento

O código não está utilizando variáveis de ambiente. Você vai configurá-lo para utilizar essas variáveis, tornando parametrizáveis a porta e o modo upside down.

Em seguida, você deverá adicionar todas as configurações necessárias para executar o Docker juntamente do Heroku.

Você vai realizar o deploy do projeto (front-end e back-end) no Heroku. Você deverá realizar o deploy do projeto, conforme requisitos, no Heroku. Os comandos utilizados deverão ser adicionados no README.md de cada projeto. Para mais informações revisite o Course.

Todos esses passos estão detalhados nos requisitos abaixo.

atom_symbol Dica

Para publicar seu front-end React, utilize o buildpack [mars/create-react-app](https://elements.Heroku.com/buildpacks/mars/create-react-app-buildpack).
Lembre-se de que é possível testar o comportamento definindo as variáveis de ambiente em sua máquina. Você pode fazer as variáveis apontarem tanto para o back-end, rodando localmente em sua máquina, quanto para as APIs já publicadas nos requisitos anteriores.

warning Dica: Lembre-se que ao importar uma variável de ambiente com process.env.nomeDaVariavel, seu tipo é string. warning

speaking_head Nos dê feedbacks sobre o projeto!

Ao finalizar e submeter o projeto, não se esqueça de avaliar sua experiência preenchendo o formulário. Leva menos de 3 minutos!

FORMULÁRIO DE AVALIAÇÃO DE PROJETO

warning O avaliador automático não necessariamente avalia seu projeto na ordem em que os requisitos aparecem no readme. Isso acontece para deixar o processo de avaliação mais rápido. Então, não se assuste se isso acontecer, ok?

card_index_dividers Compartilhe seu portfólio!

Você sabia que o LinkedIn é a principal rede social profissional e compartilhar o seu aprendizado lá é muito importante para quem deseja construir uma carreira de sucesso? Compartilhe esse projeto no seu LinkedIn, marque o perfil da Trybe (@trybe) e mostre para a sua rede toda a sua evolução.

Requisitos do projeto
warning Lembre-se de que o seu projeto só será avaliado se estiver passando por todos os checks do Linter. Utilize o comando npm run lint no seu terminal para verificar os checks do Linter wink warning

Os requisitos estão agrupados por frontend e backend. Realize as alterações nos respectivos diretórios de cada repositório.

warningIMPORTANTE: Para esse projeto, as variáveis de ambiente devem ser definidas em um arquivo .env e o arquivo deve ser enviando no seu PR(Pull Request). ISSO NÃO É UMA PRÁTICA DE MERCADO, contexto no qual o arquivo .env deve ser sempre incluído no .gitignore, pois contém informações sensíveis. Aqui o arquivo .env será enviado apenas por motivo de avaliação.

O teste no back-end:
1 - Verifica as variáveis de ambiente
Altere o back-end para utilizar variáveis de ambiente para controlar a porta em que API escutará e o modo "upsideDown".

A porta que a API escutará, essa variável deve ter, necessariamente, o nome PORT e o seu valor deve ser 3000.

O modo "upsideDown". Essa variável espera um valor boleano e deverá se chamar UPSIDEDOWN_MODE. Lembre-se de que as variáveis de ambiente são strings. O que será testado:

Se existe a variável de ambiente PORT;
Se a variável de ambiente UPSIDEDOWN_MODE existe e se ela é um boleano.
2 - Verifica se o arquivo Dockerfile está configurado da maneira correta
O teste irá verificar se o arquivo `Dockerfile` existe e está configurado da maneira correta. Ele deve construir a imagem a partir da `node:14-alpine` e usar o comando `npm start` para iniciar a aplicação via `CMD`.

O que será testado:

Se o Dockerfile está utilizando a imagem node:14-alpine, verificando se as camadas dessa imagem estão incluídas no build que esse Dockerfile faz;

Se o Dockerfile usa npm start como CMD.

3 - Verifica se o arquivo heroku.yml está configurado na maneira correta
Adicione e configure o arquivo heroku.yml.

O arquivo deve iniciar um servidor do tipo web;

O run deve executar o servidor utilizando o node.

Execute ambos na sua máquina para validar se o comportamento é o esperado.

O que será testado:

- Se o arquivo `heroku.yml` existe;

- Se o serviço a ser executado é um serviço do tipo `web`;

- Se o `node` é responsável por executar o servidor.
4 - Verifica action de Linter para ser executada no GitHub
Você deverá criar uma Action para ser executada somente em **pull_requests** solicitados em todas as branches de seu repositório.

Atenção: O arquivo de configuração da action deverá ser criado em: ./actions/ com o nome project.yml.

O que será validado:

Se o arquivo project.yml existe na pasta actions;

Se a Action será executada somente em pull requests;

Se que o job foi nomeado como eslint;

Se o job eslint é executado com a versão 20.04 do ubuntu;

Se o primeiro passo do job eslint usa a action de checkout;

Se o segundo passo do job eslint usa a action de setup-node e sua versão é a 12;

Se o terceiro passo que no terceiro passo do job eslint executa a instalação das dependências;

Se o quarto passo do job eslint executa o pacote eslint via npx;

Dica: Dê uma olhada na documentação de actions do github;

5 - Verifica o Deploy no Heroku
Crie dois apps para a API: um para o o app hawkins e outro para o app upside-down.

warningIMPORTANTE: Uma variável de ambiente com o nome GITHUB_USER deverá ser criada em seu .env com o seu nome de pessoa usuária do GitHub.

warningIMPORTANTE:

O Heroku limita o tamanho do nome de uma aplicação para ter no máximo 30 caracteres contendo apenas letras minúsculas:
se o seu nome de pessoa usuária do GitHub possuir mais do que 27 caracteres, ou contenha letras maiúsculas, ou comece com um número, você não conseguirá criar uma aplicação com o nome no padrão solicitado pelo requisito.
você pode usar uma abreviação do seu GITHUB_USER apenas com letras minúsculas na variável de ambiente e criar o app com o mesmo pré-fixo, por exemplo, temos o seguinte nome do github, tryber-com-nome-de-github-maior-que-27-caracteres:
GITHUB_USER=tryber
# E o nome dos apps deveriam ficariam assim:
# tryber-up - para o app hawkins;
# tryber-dw - para o app upside-down.
Crie dois apps do Heroku a partir do mesmo código fonte (código da API). O nome do seu app no Heroku deverá conter o seu nome de pessoa usuária no GitHub seguido de "-up" e "-dw". Por exemplo, se seu nome de pessoa usuária no GitHub for "student", seus apps deverão ter os nomes "student-up" e "student-dw" e as URLs abaixo:
- https://student-up.herokuapp.com/ - para o app hawkins;

- https://student-dw.herokuapp.com/ - para o app upside-down.
Configure a variável de ambiente criada para controlar o modo UPSIDEDOWN. Cada um dos apps deverá ter valores distintos, da seguinte maneira:
- O app `hawkins` deverá ter o valor `false`;

- O app `upside-down` deverá ter o valor `true`.
Utilizando o git, faça o deploy de ambos os apps no Heroku.
Acesse as URLs geradas e valide se ambas as API's estão no ar e funcionando como esperado.

warning IMPORTANTE: As URLs deverão ser geradas pelo Heroku e não devem ser modificadas.

O que será testado: - Se ao fazer uma requisição do tipo GET para o endpoint da API hawkins serão retornadas as informações corretas;

- Se ao fazer uma requisição do tipo GET para o endpoint da API upside-down serão retornadas as informações corretas.
O teste no front-end:
6 - Verifica as variáveis de ambiente do front-end
Altere o front-end para utilizar variáveis de ambiente para controlar as URLs e Timeouts de comunicação com a API.

Perceba que o código está esperando por duas APIs. Uma para o modo upside-down e a outra para o modo normal.

O nome das variáveis deve ser o seguinte:

Para seu back-end hawkins:

REACT_APP_HAWKINS_URL para a URL;

REACT_APP_HAWKINS_TIMEOUT para o timeout.

Para seu back-end UPSIDEDOWN:

REACT_APP_UPSIDEDOWN_URL para a URL;

REACT_APP_UPSIDEDOWN_TIMEOUT para o timeout.

O que será testado:

Se existem as 4 variáveis de ambiente citadas acima.
7 - Verifica se foi feito o deploy do frontend no Heroku
Faça o deploy do front-end.

warningIMPORTANTE: Assim como no Back-end, a variável de ambiente GITHUB_USER deverá ser criada com o seu nome de pessoa usuária do GitHub.

Crie um app do Heroku com o front-end. Vamos deixar o Heroku utilizar as configurações padrão. No momento de criar o app do Heroku, utilize o buildpack descrito abaixo, em Dicas;

O nome do seu app no Heroku deve ser seu nome de pessoa usuária do GitHub seguido de "-ft". Por exemplo, se o seu nome de pessoa usuária do GitHub for "student", o nome do seu app será "student-ft" e a URL precisar ser https://student-ft.herokuapp.com/;

Configure as variáveis de ambiente do app para apontar para as API's publicadas;

Faça o deploy com o git.

Para publicar seu front-end React, utilize o buildpack mars/create-react-app.

Lembre-se de que é possível testar o comportamento definindo as variáveis de ambiente em sua máquina. Você pode fazer as variáveis apontarem tanto para o back-end rodando localmente em sua máquina, quanto para as API's já publicadas nos requisitos anteriores.

O que será testado:

- Se ao visitar sua página no Heroku, o botão de mudar de realidade existe;

- Se a pesquisa funciona como deveria, fazendo chamada a API externa;

- Se o botão de mudar de realidade funciona;

- Se os botões de próxima página e página anterior funcionam.  
Bônus
8 - Verifica os multi-ambientes e modo de desenvolvimento.
Utilize a estratégia de multi-ambientes no front-end.

Para isso:

Renomeie o remote atual para remote-desenvolvimento;

Crie e faça o deploy de um novo app no Heroku, conforme requisito 7. O nome do seu novo app no heroku deve ser seu nome de usuário do github seguido de "-pd" ("pd" se refere à "produção", ou seja, não está em desenvolvimento). Por exemplo, se o seu usuário do github for "student", o nome do seu app será "student-pd" e a url precisa ser https://student-pd.herokuapp.com/;

Adicione um elemento ao frontend que identifique que a aplicação está rodando em modo de "desenvolvimento". Esse elemento deve ser visível e conter o texto "Em desenvolvimento";

Lembre-se de criar uma variável de ambiente para controlar esse comportamento, configurando-a para ter um valor diferente em cada um dos ambientes publicados. Atente-se às regras de nomes para váriáveis de ambiente utilizadas no React.

O que será testado:

Se ao acessar o front-end de desenvolvimento, haverá a tag com o texto "Em desenvolvimento";

Se ao acessar o front-end de produção, não haverá a tag.
