# Branches

Branches são ramificações criadas no repositório. São utilizadas para que cada desenvolvedor possa trabalhar sem alterar a linha principal. Não sendo necessário criar uma cópia do repositório para isso, você pode criar uma nova ramificação, uma linha que diverge da linha principal, onde você pode trabalhar de forma isolada em alguma atualização, sem que isso interfira no fluxo de trabalho principal.

## Como os dados são armazenados

Ao contrário do que muitas vezes imaginamos, o Git não armazena os dados como uma série de mudanças e diferenças, mas ele cria uma espécie de snapshot (que são cópias instantânea de momentos). Todo commit, possui um objeto que contém um ponteiro para o snapshot do conteúdo que você enviou. Ele contém as suas credenciais e as informações do commit, como a data e a mensagem de commit, assim como ponteiros para os “commit pais” que são commits anteriores a esse que você enviou. Significa que o commit inicial não vai ter pai, os outros terão 1 pai e os que resultam da fusão de uma ou mais branches terão vários pais.

Quando você faz um commit, o git verifica o subdiretório e armazena os objetos no repositório do Git, esses objetos contém os metadados e um ponteiro para a raiz do projeto para que ele possa recriar aqueles snapshots quando necessário.

Cada commit armazena um ponteiro para identificar qual commit veio imediatamente antes dele. Isso é o que permite que o Git saiba quais foram as alterações feitas em cada commit.

Suponhamos que você queira enviar 3 arquivos, como na imagem abaixo, então seu repositório terá 5 objetos:

- Um blob para o conteúdo de cada um dos seus três arquivos, (Blob é a abreviação de “binary large object - objeto binário grande”. Quando executamos `git add` em um arquivo, o git cria um blob com o conteúdo do arquivo)
- uma árvore que lista o conteúdo do diretório e especifica quais nomes de arquivo são armazenados e quais seus blobs,
- um commit com o ponteiro para essa árvore com todos os metadados de commit.

Então, quando vários arquivos são enviados de branches diferentes, em cada uma delas temos uma estrutura como essa, que será salva sem interferir no fluxo principal. É como que cada desenvolvedor crie uma branch para cada feature dentro do projeto, para que ele possa trabalhar nela e depois que o código for testado e verificado, pode ser inserido no fluxo principal.

## Branch Master

Quando executamos o comando `git init`, o Git cria uma branch padrão, que é a master, mas a maioria das pessoas utilizam apenas ela durante todo o desenvolvimento do projeto. Não criam novas branches, nem alteram essa. Então é por isso que muitas vezes vemos repositórios com apenas essa branch principal, mas ela não tem nada de especial, é apenas a branch padrão criada pelo Git para que vc possa iniciar o projeto.

Nessa imagem podemos ver como uma branch gerencia o histórico de commits. O branch é um ponteiro móvel para os commits. Cada vez que você faz um commit ele vai avançando para o próximo.

Então você pode criar quantas ramificações forem necessárias para organizar melhor o desenvolvimento do seu projeto.

Para criar uma nova branch, você deve executar: `git branch novabranch` e se quiser saber as branches que já foram criadas, pode executara: `git branch`, que vai mostrar as branches existentes.

Para alternar entre branches, utilize `git checkout nomedabranch`.
