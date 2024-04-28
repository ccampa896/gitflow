# Commit e Commit Messages

Commit é um pacote de alterações realizadas no repositório. Nele, podemos encontrar as informações de arquivos alterados, autor e uma mensagem descritiva que indica o que foi realizado naquele pacote de atualizações.

É muito importante manter um padrão nessas mensagens descritivas de commit para que eles fiquem armazenados de forma consistente no repositório e que fique mais claro o objetivo de cada um dos pacotes enviados. Em uma equipe ou em um projeto grande, é ainda mais importante, pois a quantidade de commits enviados ao servidor é bem grande e pode acabar confundindo na hora de reverter alguma alteração ou voltar em algum ponto específico do projeto, pois acaba não sendo possível identificar em que parte do projeto cada commit está.

O objeto de commit é composto pelo metadata do commit+ tree object (snapshot do working directory) + identificador do commit antecessor/ancestral/pai.

## Conventional Commits

Existe uma convenção que especifica tipos de commits que devem ser utilizados em cada situação para deixar mais claro esse processo. A documentação está disponível em: https://www.conventionalcommits.org/pt-br/v1.0.0/#resumo

É interessante a equipe seguir esses padrões para que o projeto fique cada vez mais profissional e o fluxo de alterações e histórico de commits fique muito mais fácil de visualizar e entender. Mas como toda metodologia ou padrão, deve ser adaptado à realidade da empresa e do time para que não se torne mais uma dificuldade no processo de desenvolvimento, mas seja um facilitador.

## Guia de boas práticas de mensagens de commit

Nesse guia, você vai ver algumas regras principais de como você deve escrever sua mensagem de commit, utilizando os verbos corretos e os tipos corretos: https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines

O principal ponto a se considerar, é que independente do tipo utilizado, a mensagem deve ser bastante clara e objetiva, descrevendo exatamente o que aquele commit vai trazer para o repositório, do que se trata aquele pacote de atualizações. Ele veio pra corrigir algum bug? Adicionar uma nova funcionalidade? Inserir um caso de testes? Deve ser especificado que tipo de conteúdo ele traz. Lembrando que não é necessário inserir informações de datas ou autoria de códigos, pois o versionador já insere automaticamente no log do commit.

## .gitignore

O Git possui uma ferramenta que permite criar uma lista de exclusão de arquivos que não devem subir ao repositório remoto. Na raiz, crie um arquivo chamado: .gitignore. Dentro dele, você precisa colocar o nome dos arquivos que não devem subir para o repositório, como por exemplo a pasta node_modules que é uma pasta gigantesca que traz inúmeros arquivos de configuração do node, outro arquivo que deve ser incluído na lista é o .env, que traz configurações locais de credenciais de bancos de dados. Dependendo da tecnologia que você estiver utilizando, você vai colocar outros arquivos nessa lista. Mas a regra principal é: Não subir ao repositório arquivos de configurações locais, principalmente.

## Fazendo o commit

Existe um procedimento para a execução do commit, então não é simplesmente executar o comando. Precisamos seguir os passos: Preparar os arquivos, colocando na staging area, que é uma área de preparação intermediária, onde vamos armazenar de forma temporária os arquivos. Depois podemos executar o commit, propriamente dito, com o `git commit -m “mensagem descritiva”`. Mas não para por aí, pois seus arquivos somente irão subir para o repositório, quando você executar o push para ele. Vou te explicar com detalhes cada uma das etapas, a seguir.

Antes de fazer o commit, precisamos adicionar as alterações no arquivo do diretório local preparando para ele ser entregue para o servidor remoto (staging area), então vamos utilizar: `git add nomedoarquivo` , pois o ideal é que cada commit contenha arquivos relacionados à aquela alteração específica. Então se por exemplo, estou desenvolvendo uma nova feature, e em algum momento acabei alterando algum arquivo que não estava relacionado com ela, se eu subir todos os arquivos de uma vez, utilizando o `git add .` não vou criar um commit limpo, pois esse comando sobe todos os arquivos que foram modificados e que ainda não foram commitados.

O ideal é que sejam enviados todos os arquivos, um por um, para que se tenha um commit coerente, somente com os arquivos relacionados com aquela alteração que foi realizada. É mais trabalhoso, mas vale a pena manter os commits coerentes. No futuro, quando for necessário restaurar algum commit do repositório ou fazer uma busca pelo log, você vai saber exatamente o que foi feito e quais arquivos estava envolvidos. Utilizar o `git add .` não é errado. O errado é você subir um pacote grande com todo tipo de alteração realizada ao mesmo tempo, e depois quando você ou seu time precisar descobrir do que se tratava, terá dificuldades.

Caso você queira desfazer essa inclusão, antes de dar o push para o servidor, utilize: `git reset nome_arquivo` ou `git reset --hard`, que vai remover todas as mudanças que foram para a área de staging. O git reset hard, deve ser utilizado como medida de emergência, caso você tenha subido muita coisa errada e tenha criado uma bagunça no repositório, pois ele apaga tudo o que foi realizado, faz uma verdadeira limpeza na área de staging.

Agora os arquivos estão preparados, então vamos fazer: `git commit -m “Mensagem descritiva do commit”`, com isso enviamos as alterações, mas elas ainda não foram para o servidor. Para isso precisamos fazer o `git push origin nomedabranch` ou `git push -u origin nomedabranch` para criar uma nova branch e subir para o repositório remoto.

## Arquivo README

É um arquivo onde inserimos a informações principais de apresentação do projeto, portanto ele deve ser descritivo e conter a maior quantidade de informações relevantes possível, pois é a documentação do seu projeto.

Uma documentação não é algo que deve ser criado apenas para que outras pessoas possam ver e conhecer seu projeto, mas mesmo que você tenha apenas projetos pessoais, vai te ajudar em algumas questões como manter um histórico para quando precisar utilizar o projeto novamente no futuro e para enriquecer seu projeto como portfólio. É um dos primeiros arquivos, se não o primeiro que um recrutador vai olhar quando quiser conhecer seu trabalho.

Então, um arquivo README, deve conter as seguintes informações, para estar completo e oferecer informações relavantes:

- O que é o projeto? Do que se trata? - Uma descrição do projeto, qual problema ele resolve, qual o propósito dele, vai fazer com que a pessoa que está olhando seu projeto consiga compreender a utilização de determinadas bibliotecas ou a arquitetura. E se for um projeto antigo, no futuro você vai conseguir lembrar essas informações para caso seja necessário refatorá-lo.
- Como o projeto funciona? - Essa é uma informação de ouro para quem deseja implementar seu projeto ou fazer um clone para tentar resolver bugs ou desenvolver novas features. O que precisa ser instalado? Como a pessoa vai executar o projeto? Através do terminal, através da instalação de alguma outra aplicação, rodando algum comando, entre outras informações.
- Quais foram as tecnologias utilizadas e como ele foi implementado? - Aqui você vai descrever as tecnologias e bibliotecas utilizadas, assim como as motivações dessas escolhas.
- Como contribuir com seu projeto? - Nessa parte, você pode colocar algumas “boas práticas” ou regras que as pessoas devem seguir quando forem te enviar pull requests do seu projeto. Algum tipo de formatação específica, deixar informações de contato, você pode pedir para que a pessoa descreva o conteúdo da pull request de forma mais detalhada também.
- Referências - É interessante incluir a página oficial da empresa ou alguns links que podem ajudar a compreender melhor o objetivo do projeto. Nessa área você também pode colocar links úteis como endereço da documentação oficial de alguma tecnologia específica ou algum passo a passo de instalação de tecnologias que serão utilizadas no projeto.
