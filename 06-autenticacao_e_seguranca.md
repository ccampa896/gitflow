# Autenticação e Segurança

Para acessar os repositórios, você precisa realizar autenticação por motivo de segurança. Para fazer qualquer operação de clone, pull, push, commit ele exige autenticação de segurança. Anteriormente fizemos uma configuração com seu nome e email, de onde o GIT vai buscar as informações de autoria das operações realizadas, mas para manipular os repositórios, você precisa autenticar no repositório.

Contexto

Em 2020, o Git Hub anunciou que tinha a intenção de modificar a forma de autenticação que era até então utilizada para fazer as operações via terminal e acessar os repositórios. Quando precisávamos fazer um commit ou um clone de repositório, o GIT solicitava email e senha da conta para autenticar.

A partir de 13 de Agosto de 2021, começaram a não aceitar mais senhas de contas para autenticação em operações via terminal. Seria necessário então, gerar um Token para todas as operações de Git autenticadas.

**O que mudou?**

Os fluxo de trabalhos afetados, segundo a empresa foram os seguintes:

Acesso Git através de linha de comando

- Aplicativos de desktop usando Git (o GitHub Desktop não é afetado)
- Quaisquer aplicativos / serviços que acessam repositórios Git em GitHub.com diretamente usando sua senha

E os seguintes clientes não foram afetados:

- Aqueles que tiverem [a autenticação de dois fatores](https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa) habilitada na conta, já será necessário usar a autenticação baseada em token ou SSH.
- Os que utilizam o GitHub Enterprise Server.
- Quem utiliza um [aplicativo GitHub](https://docs.github.com/en/developers/apps/about-apps#about-github-apps), pois eles não oferecem suporte à autenticação de senha.

**Vantagens**

Essa mudança se deve a motivos de segurança, pois utilizando os Tokens, as informações do usuário ficam armazenados nele e não no servidor. Outra vantagem é que ele possui um período de validade, não é um token permanente. Ao gerar um novo Token, é possível escolher o período que ele ficará ativo. Depois disso, será necessário gerar um novo Token.

**Como gerar o Token?**

Para configurar e começar a utilizar o Token em seus projetos, você deve seguir os seguintes passos:

1- Faça login na sua conta Git Hub, e no canto superior direito, clique no menu e em seguida, na opção: “Settings” ou “Configurações”.

2 - Em seguida, acesse a opção “Developer Settings”;

3 - Clique na opção “Personal Access Tokens”;

4 - Em seguida, escolha a opção “Generate New Token”;

5 - O GitHub vai solicitar que você digite novamente sua senha para confirmar a identidade;

6 - Escolha um nome para ele e o tempo de expiração;

7 - Em seguida, na mesma tela, selecione as permissões que você deseja conceder a ele;

8 - Depois de configurar as permissões, clique no botão “Generate Token”;

9 - Após Gerar o token, você receberá uma confirmação.

Você receberá o seu token, mas observe a mensagem acima: Você deve copiar seu token nesse momento, pois você não terá mais acesso à ele. Caso não copie nessa etapa, você terá apenas a opção de Atualizar ou Deletar esse e criar outro, não é possível acessar a qualquer momento essa informação.

Então você pode utilizar o comando: `git config --global credential.helper cache` para salvar as credenciais.
