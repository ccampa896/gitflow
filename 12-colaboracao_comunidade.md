# Colaboração com a comunidade

Existem muitos projetos Open source, ou seja, que possuem o código aberto, onde os membros da comunidade podem participar e contribuir com correção de bugs ou sugerir melhorias. Existem grandes sistemas que utilizam esse modelo de código aberto como o Linux, GitLab, Rails, Node, Django, entre outros.

## Por que contribuir com projetos Open Source

Entre os principais motivos pelos quais você pode contribuir com projetos open source é que você vai estar participando do desenvolvimento de grandes tecnologias que são utilizadas por muitas pessoas no mundo, além de estar praticando suas habilidades técnicas, analisando o código de outra pessoa, propondo melhorias e sugerindo alterações. Quando você começar a participar de projetos diferentes, você vai aprender muitas habilidades e tecnologias diferentes.

Essas contribuições podem ser adicionadas ao seu portfólio e vai fazer com que você tenha mais credibilidade como desenvolvedor.

Você também vai fazer um Networking muito interessante, conhecendo outros programadores que participam da comunidade e poderá trocar experiências com eles.

## Não é apenas código

A contribuição com projetos open sources não envolvem apenas as sugestões de alteração e correção de código em sim, mas você pode contribuir com outras partes do projeto que são geralmente negligenciadas ou esquecidas, como a documentação, por exemplo. Você pode escrever tutoriais para o projeto, uma tradução, reestruturar layouts, entre outras coisas. Se você estiver começando e ainda não tiver muita habilidade com programação ou se você tem facilidade em desenvolver as outras partes do projeto, você já pode começar a contribuir com a comunidade. Isso vai fazer com que você conheça projetos diferentes e entenda como eles funcionem e quem sabe mais tarde pode começar a contribuir com o código.

## Como começar?

Vamos entender como você pode começar a encontrar projetos para contribuir

1- Antes de mais nada, pesquise por projetos open source que você ache interessante e verifique os arquivos dentro dele como o README e CONTRIBUTING, onde você vai encontrar informações sobre aquele projeto. Se você não encontrar informações relevantes no README, já veja como uma oportunidade de contribuir com essa informação no projeto.

Nesses sites você pode encontrar muitos projetos interessantes que você pode contribuir:

https://github.com/MunGell/awesome-for-beginners

https://github.com/explore

https://www.codetriage.com/

2- Veja o projeto, entenda do que ele se trata e identifique pontos que você possa contribuir. Encontrou algum bug? Alguma falha na documentação, na organização dos arquivos?

Dentro do README e do CONTRIBUTING, pode conter informações como orientações para quem deseja contribuir, boas práticas ou algumas regras que devem ser seguidas, mas pode ser que o autor não tenha inserido essa informação.

Quando você identificar o ponto que deseja contribuir, você pode abrir uma Issue (São como o início de uma conversa ou discussão). Quando você abre uma issue, você está interagindo com outras pessoas e falando sobre a sua intenção de colaboração com o projeto, como por exemplo: Você encontrou um bug e gostaria de saber se tem alguém trabalhando nele ou você já tem alguma ideia do que pretende fazer, então você abre uma Issue para abrir uma discussão sobre o assunto.

3- Ao iniciar o trabalho na solução, você faz um FORK do projeto no GITHUB, que vai abrir uma branch pra você submeter sua solução, ele vai fazer uma cópia do projeto para a sua própria conta do GITHUB.

4- Faça o clone do projeto para a sua máquina, `gitclone urldorepositorio`, vocẽ pode sincronizar o seu Fork com o projeto original para que você não fique com ele desatualizado, então cada alteração será sincronizada com ele e você poderá ir trabalhando em uma versão atualizada. Utilize: `git remote add upstream urldoprojeto`

5- Como vimos anteriormente, é importante criar uma branch para o desenvolvimento de novas features, então vamos fazer: `git branch nomedabranch`

6 - Depois que você fizer a alteração no projeto, faça o commit. Começamos com o `git add .` para adicionar todos os arquivos alterados. e depois, o commit: `git commit -m “Mensagem descritiva sobre a alteração realizada”` não se esqueça de utilizar as boas práticas para escrever as mensagens de commit.

7- Agora você pode subir a sua Branch para o Fork, execute: `git push origin nomedabranch`

8- Agora que você já está com as alterações no seu Fork, faça a pull request com a solução que você identificou ser a ideal para aquele bug ou para uma nova feature.

Então você vai no fork do projeto, e clique em NEW PULL REQUEST, vai aparecer um menu mostrando a branch que você criou para o projeto. En seguida vai aparecer a diferença entre a sua branch e o projeto original, onde você precisa verificar se subiu tudo corretamente e clique em “Create Pull Request”. Você precisa escrever uma mensagem que descreva as alterações que você realizou para que os mantenedores do projeto saibam do que se trata.

Quando você enviar o pull request a responsável por ele, ou o autor, vão analisar sua solução proposta e identificar se elas estão de acordo com o que foi planejado para o projeto. Eles podem te enviar perguntas sobre as alterações, podem recusar suas alterações ou incorporá-la ao projeto.
