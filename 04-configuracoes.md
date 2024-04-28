# Configurações

Após finalizada a instalação, você pode rodar o comando `git --version` para verificar se foi instalado corretamente. Nesse momento deve aparecer a versão instalada no seu computador.

Agora vamos utilizar um comando para configuração das suas credenciais no git para que toda vez que você enviar arquivos para seu repositório, ele utilizará essas informações para identificar a origem daquele envio.

## Configuração de credenciais

Então primeiro vamos executar: `git config --global user.name “Seu nome”`

Depois vamos configurar o email: `git config --global user.email ”seuemail@gmail.com”`

Pra verificar se as configurações foram realizadas corretamente, podemos utilizar: `git config --list`

Agora suas credenciais foram configuradas e podemos iniciar a utilização do GIT.

`git config --global --unset user.senha` para remover a senha salva
