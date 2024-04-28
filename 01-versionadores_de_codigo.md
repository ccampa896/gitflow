# Versionadores de código

São plataformas que possuem estratégias para gerenciar as diferentes versões de um código.

## Contextualizando

Durante o desenvolvimento de um projeto, temos vários membros da equipe trabalhando em partes diferentes do código e algumas vezes em uma mesma parte dele. É muito importante que durante o desenvolvimento do projeto ele seja salvo algumas vezes para que não seja perdida aquela parte que está sendo trabalhada. Antigamente (muito antigamente) a forma que era feito esse processo de salvar o projeto era em algum pen drive ou HD externo e até mesmo em pastas compartilhadas no servidor local.

Cada membro da equipe fazia a “sua parte” no projeto e salvava nesse drive e depois ia juntando com os demais arquivos do time, ou então, caso o projeto fosse pequeno e desenvolvido por apenas 1 pessoa, ele iria salvando a cada pausa no trabalho, uma versão diferente. Só de ouvir isso você já pode imaginar o que acontecia. Eram criadas muitas versões diferentes e era muito fácil se perder em meio a tantas versões diferentes, afinal de contas, não era prudente apagar a versão anterior, imagina se dá um problema depois e essa versão antiga é necessária pra correção!? Então eram mantidas várias versões do projeto. Isso também gerava o acúmulo de arquivos repetidos e desnecessários no projeto, pois eles haviam sido alterados por pessoas diferentes e era prudente manter todas as versões para caso de possíveis correções.

Dentre os problemas comuns, tinha a seguinte dúvida: “Como eu vou saber em que parte do projeto cada uma dessas versões estava?” Era necessário renomear o arquivo para manter o histórico e muitas vezes era ineficiente porque eram dados nomes genéricos que não significavam nada.

E quando era necessário copiar o projeto para um membro novo da equipe ou para algum outro membro? Como saber aonde está a versão mais recente?

Outra questão era que muitas empresas utilizavam um mesmo pendrive para salvar as versões desenvolvidas pelo time. Então a questão era: “Como eu vou saber quem fez esse código?” “Colocar a autoria do arquivo nos comentários?” Eram tantos procedimentos errados que acabavam tomando mais tempo da equipe resolvendo esses problemas do que realmente desenvolvendo o projeto.

## Como os versionadores funcionam

Para resolver esses e outros problemas, foram criados os versionadores de códigos que são plataformas que gerenciam esse processo de armazenamento de versões diferentes de códigos. Eles permitem que todos os códigos armazenados possuam uma identificação de quando foi salvo e quem é o responsável por ele. De forma que fica muito mais rápida e prática essa tarefa de manipular os arquivos do projeto, a utilização de versionadores é importante para armazenar com segurança, considerando que o armazenamento local, na máquina física pode trazer riscos de perda do arquivo caso a máquina seja danificada ou ocorra algum erro no sistema. Além disso existem os riscos de invasão e acesso não autorizado, que podem prejudicar a integridade dos arquivos.

Existem várias plataformas como essas, que podem ser utilizadas para essa finalidade e todas elas trazem em comum as funcionalidades de gerenciamento de versões, porém cada uma delas traz algum diferencial com relação à compatibilidade com os sistemas utilizados ou com o projeto. Muitas vezes a empresa acaba escolhendo aquela que a equipe possui mais familiaridade. Então fica a critério da empresa/equipe escolher a plataforma que se adequa melhor às suas necessidades. As mais utilizadas são: Bitbucket, GitHub, SVN.

## Controle de versão Centralizados e Distribuídos

Os sistemas de controle de versão são classificados de duas formas: Centralizados e Distribuídos.

**Centralizado** funciona como uma arquitetura cliente-servidor, onde existe um servidor central, com diversas áreas de trabalho, então as áreas de trabalho precisam passar primeiro pelo servidor para acessar as informações. Podemos considerar como características desse sistema, um tempo de resposta muito bom e atende muito bem uma equipe pequena trabalhando em uma rede local. O principal sistema que trabalha dessa forma é o Subversion (SVN).

**Distribuído** é mais utilizado quando a equipe é maior e está descentralizada trabalhando em diferentes locais, como o caso de uma equipe remota, por exemplo. Pois não existe um servidor central para a execução das tarefas de subir as versões, cada máquina funciona como se tivesse seu próprio servidor, podendo ser realizadas operações de check-in e check-out do projeto dentro delas mesmas, mas existe um servidor remoto disponível para o armazenamento dos arquivos com segurança. As áreas de trabalho podem se comunicar entre si.
