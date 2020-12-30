# GIT BASH

#### Verificar configurações
`git config --global`
#### Atualizar/Cadastrar user e email
user | email 
:---| :---
`git config --global user.name “<NomeDeUsuario>”` <br/> |`git config --global user.email “<EmailExemplo@gmail.com>”`
#### Criar repositório local
`git init`
> *Reinicializa o repositório caso possua.*

#### Verificar status dos arquivos
`git status`
#### Adicionar arquivo untrackted ao staged
Um por vez | tudo ao mesmo tempo
:---:|:---:
`git add <NomeDoArquivo>`<br/> |`git add .` <br/>
-|`git --all` <br/>
-|`git -A` <br/>
#### Salvar uma versão, realizar um commit
`git commit -m “mesagem do commit”`
#### Alterar mensagem do último commit realizado
`git commit -m “nova mesagem do commit” --amend` 

