# Merge

Quando mais de um membro do time trabalha em uma mesma atualização e modificam um mesmo arquivo, vão surgir duas versões de um mesmo arquivo, por isso é necessário gerenciar esse conflito e decidir qual das alterações serão mantidas e qual delas serão descartadas.

Então, quando o commit é realizado, o GIT pausa o processo para que você solucione o conflito.

Após você resolver o conflito e decidir qual versão está correta e deve subir para o repositório, será feito então o Merge, que é a mesclagem das duas versões, formando uma unica versão que será enviada para o repositório.

Essa mesclagem é uma forma de unificar branches, pegando linhas de desenvolvimento independentes, e integre em uma unica ramificação. Então na imagem, temos a branch principal (main) e a feature tip que é a outra branch de desenvolvimento.

Se você executar o `git merge`, ele vai unificar as duas branches.

Mas esse processo nem sempre é simples, pois podem aparecer conflitos, onde um arquivo foi modificado por duas pessoas ou você enviou 2 vezes o mesmo arquivo, com informações diferentes. Então quando você executar o `git merge`, vai aparecer uma mensagem de erro com um conflito para você escolher a versão que melhor se adequa ao que você deseja para o projeto.

## “Ferramentas” úteis para lidar com conflitos

Existem alguns comandos do Git que vão te ajudar a resolver conflitos, encontrando mais informações sobre eles:

Quando você fizer um commit e se deparar com um conflito, e utilizar o comando `git status`, você verá as condições do diretório e da área de staging.

Utilizando o `git log --merge`, você conseguirá visualizar a lista de commits com conflitos entre as ramificações.

O `git diff` ajuda a encontrar diferenças entre os estados de repositórios ou arquivos. Ajuda a prevenir conflitos de merge.
