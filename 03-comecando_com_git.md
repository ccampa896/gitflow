# Começando com o GIT

Antes de começar a trabalhar com GIT, você precisa saber de alguns conceitos que vão nortear todo o seu trabalho e tudo ficará mais claro quando estiver gerenciando os repositórios.

## Operações locais

A maioria das operações são locais, só precisam de arquivos e recursos locais para operar, não é necessário utilizar nenhuma informação de outros computadores da rede, isso faz com que o tempo de resposta dele seja excelente. Possibilita também o trabalho offline, visto que as informações do projeto estão armazenadas localmente e podem ser enviadas para o repositório online quando você estiver online. Outra vantagem, é que ele pode facilmente acessar o histórico do projeto quando necessário, somente com as informações contidas na própria máquina.

## Integridade

Todas as operações passam por verificações, então não é possível alterar o conteúdo de qualquer arquivo ou pasta sem que esses logs fiquem armazenados no histórico. Da mesma forma, por conta dessas verificações, não há perda de informação durante a transferência de dados, isso significa que não existe possibilidade de haver arquivos corrompidos sem que o Git detecte antes.

Sempre que os arquivos são enviados ao banco de dados do Git ficam armazenados para que seja possível reverter as operações, nunca são removidos quando uma nova versão do arquivo é submetida. Por isso é muito difícil fazer alguma operação que não seja reversível ou apagar dados por engano.

## Três estados

Os arquivos podem estar em tres estados principais dentro do GIT: Commited, Modified (modificado) ou staged (preparado).

**Commited** - significa que os dados já estão armazenados de forma segura no banco de dados local.

**Modified** - Significa que o arquivo foi modificado, não está igual ao enviado ao banco de dados anteriormente e ainda não foi enviado para seu repositório, não foi feito o commit.

**Staged** - Nesse caso, você marcou essa versão atual do arquivo para ser enviado no próximo commit.

## Instalação

Para começar a utilizar o GIT, você precisa instalá-lo em seu sistema operacional, mesmo que esteja utilizando Linux ou Mac OS, onde podemos encontrar o GIT já instalado, é necessário atualizá-lo na máquina.

Vou deixar um link para que você possa instalá-lo de acordo com seu sistema operacional. Acesse: https://git-scm.com/book/pt-br/v2/Começando-Instalando-o-Git
