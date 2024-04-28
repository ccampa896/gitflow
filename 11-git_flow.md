# Git Flow

É um fluxo de trabalho com o GIT, uma estratégia criada para melhorar a organização das branches dentro do repositório permitindo mais fluidez ao processo de novas Features e Releases. É uma solução que permite um gerenciamento mais simples e rápido de equipes e projetos maiores, pois há uma grande quantidade de informações sendo enviadas ao repositório a todo tempo.

## Trabalhando com ramificações

Como dissemos anteriormente, não é correto, do ponto de vista das boas práticas de utilização do Git, que os commits sejam realizados na branch master. Imagine uma equipe grande com 30 à 40 programadores e todos commitando na branch master. Com certeza se tornará uma bagunça! O ideal então é que cada um deles crie branches para cada atualização nova que for desenvolver. Depois que for finalizada a tarefa, é feito um Merge na branch principal, na master.

No GitFlow, funciona dessa forma, mas um pouco mais complexa e organizada e ajuda demais a visualizar melhor as tarefas que estão sendo realizadas.

Veja na imagem abaixo que para cada tipo de atividade realizada, é criada uma branch de desenvolvimento. Após a atividade ser realizada e revisada, é devolvida para a branch principal.

## Começando com o GitFlow

Você pode instalar o gitflow, utilizando esse guia de acordo com seu sistema operacional: https://github.com/nvie/gitflow/wiki/Installation

Depois disso, execute o `git flow init.` Que é uma extensão do git init e não faz alterações nos repositórios, somente cria ramificações.

Então podemos começar criando uma ramificação de desenvolvimento: `git branch develop` depois de criada, podemos criar uma outra, que é filha dessa, chamada feature, então não serão ligadas diretamente à principal, mas à ramificação pai, develop, Vamos criar, utilizando: `git flow feature start feature_branch`, esse procedimento será realizado para a criação das demais ramificações. Ao concluir o desenvolvimento na branch feature, você pode executar: `git flow feature finish feature_branch` que vai mesclar essa ramificação com a de desenvolvimento.

## Resumindo

O fluxo geral do Gitflow é:

1. Uma ramificação `develop` é criada a partir da `main`
2. Uma ramificação de `lançamento` é criada a partir da ramificação de `desenvolvimento`
3. As ramificações de `recurso` são criadas a partir da ramificação de `desenvolvimento`
4. Quando um `recurso` é concluído, ele é mesclado na ramificação de `desenvolvimento`
5. Quando a ramificação `release` é feita, é feito o merge dela na ramificação `develop` e na `principal`
6. Se for detectado um item na `main`, uma ramificação de `hotfix` vai ser criada a partir da `main`
7. Depois que o `hotfix` for concluído, ele passa por merge para a ramificação `develop` e à `main`
