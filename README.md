# GIT BASH
 
#### Verificar configurações
```
git config --global
```
#### Atualizar/Cadastrar user e email
```
git config --global user.name “<NomeDeUsuario>”
git config --global user.email “<EmailExemplo@gmail.com>”
```
#### Criar repositório local
```sh
git init 
```
> *Reinicializa o repositório caso possua.*

#### Verificar status dos arquivos
```sh
git status
```
#### Adicionar arquivo untrackted ao staged
```sh
git add <NomeDoArquivo>
git add . 
git -A 
git --all
```
#### Salvar uma versão, realizar um commit
```sh
git commit -m “mesagem do commit”
```
#### Alterar mensagem do último commit realizado
```sh
git commit -m “nova mesagem do commit” --amend 
```
