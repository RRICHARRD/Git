# :desktop_computer: GIT BASH
<p align="justify">
  Esse arquivo tem como objetivo ser uma consulta rápida dos comando do terminal git bash, ele não elimina a verificação da documentação oficial no site https://git-scm.com.         Para as pessoas que não desenvolveram proeficiência na língua inglesa, esse breve documento pode auxiliar no uso da ferramenta.
</p>

## :pushpin: Verificar configurações do git na máquina
`$ git config --list`
>*Algum momento pode precisar remover algum login da máquina. Entrar em Painel de Controle e opção Gerenciador de Credenciais.* 

## :pushpin: Atualizar/Cadastrar user e email
user | email 
:--- | :---
`$ git config --global user.name “<NomeDeUsuario>”` <br/> |`$ git config --global user.email “<EmailExemplo@gmail.com>”`

## :pushpin: Criar repositório local
`$ git init`
> *Reinicializa o repositório caso possua.*

## :pushpin: Verificar status dos arquivos
`$ git status`

## :pushpin: Adicionar arquivo untrackted ao staged
Um por vez                       | Tudo
:-------------------------------:|:---:
`$ git add <NomeDoArquivo>`<br/> |`$ git add .` <br/>
-|`$ git --all` <br/>
-|`$ git -A` <br/>

## :pushpin: Salvar uma versão, realizar um commit
`$ git commit -m “mensagem do commit”`

> Verifica se o que você fez realmente foi salvo 
## :pushpin: Inserir arquivo do staged no último commit já realizado
`$git commit --amend`

> *Vai abrir o editor VIM, muda a mensagem lá em cima se quiser e depois escreve :wq para sair.*
> *o w vem de write e q de quite.*

## :pushpin: Alterar mensagem do último commit realizado (Não tem na documentação oficial explicitamente) 
`$ git commit -m “nova mensagem do commit” --amend` 

> *Se tiver outro arquivo no staged vai salvar junto nesse novo commit.*
> *Para alterar somente a mensagem do commit, resolve o problema da mensagem no exato momento que fez, pois ai não vai ter nada no staged.*

## :pushpin: Verificar todos os commits do arquivo
shas extenços | shas curtos 
:-------:|:---:
`git log`|`git log --oneline` 

## :pushpin: Associar repositório local com o de origem 
`$ 	git remote add origin <UrlDoRepositorio>`

## :pushpin: Trazer para o repositório local os arquivos do servidor 
Primeira vez | Demais vezes
:---:|:---:
`$ git pull origin master` | `$ git pull`

## :pushpin: Empurrar para o servidor 
 Primeiro momento| Demais
:---|:---
`$ git push --set-upstream origin master`| `$ git push`

 ?| -
:--:|:---:
`$ git push -u origin master` | -
`$ git push origin master` | - 

## :pushpin: Apaga os commits de cima para baixo até o repositório dado checkout 
`$ git reset --hard  <6NumerosDoCommit>`  
>*Cuidado com esse comando. Apaga permantemente*

## :pushpin: Retira algo do statged 
Um por vez | Todos
:--- |:---
`$	git restore --staged <nomeDoArquivoNoStage>` | `$ git restore --staged .`

## :pushpin: Clonar um repositório 
`$ git clone <”UrlDoRepositorio”>`

## :pushpin: Mudar a versão atual de salvamente através do commit
`$ git checkout <6NumerosDoCommit >`

## :pushpin: Restaurar versão padrão do commit do último usuário 
`$ git stash`

## :pushpin: Verificar a diferença de um arquivo para o outro no terminal do git bash
`$ git diff`
>*A comparação ocorre entre as modificações inseridas no documento que não possuem no commit anterior, ou seja, compara o arquivo salvo do último commit com os novos códigos >inseridos, é o arquivo salvo no commit contra o mesmo arquivo com alterações. NÃO DÁ PARA VER AS ALTERAÇÕES CASO OS ARQUIVOS ESTEJAM NO STAGED!*

## :pushpin: Listar as branches do repositório 
`$ git branch`

## :pushpin: Criar uma branch no repositório 
`$ git branch <NomeDaBranch>`

## :pushpin: Alterar de branch
`$ git checkout <NomeDaBranch>`

## :pushpin: Criar uma branch e no exato momento alternar para ela
`$ git checkout -b <NomeDaBranch>`

## :pushpin: Criar uma Tag
`$ git tag -a <NomeDaTag> -m"Não tenho certeza, mas acho que seria uma mensagem"`

