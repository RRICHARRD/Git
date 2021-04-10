<p align="center">
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo-Color.png" alt="Git-logo-color" width="250"/>
</p>

***

<p align="justify">
  Esse arquivo tem como objetivo ser uma consulta rápida dos comando do terminal git bash, ele não elimina a verificação da documentação oficial no site https://git-scm.com.         Para as pessoas que não desenvolveram proeficiência na língua inglesa, esse breve documento pode auxiliar no uso da ferramenta.
</p>

<h1> 
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25"> 
  Verificar configurações do git na máquina
</h1> 
  
`$ git config --list`

>*Algum momento pode precisar remover algum login da máquina. Entrar em Painel de Controle e opção Gerenciador de Credenciais.* 
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25"> 
  Atualizar/Cadastrar user e email
</h1>

user | email 
:--- | :---
`$ git config --global user.name “<NomeDeUsuario>”` <br/> |`$ git config --global user.email “<EmailExemplo@gmail.com>”`

>*Essas informações ficam disponíveis para visualização no commit, isso significa que a cada snapshoot (commit) feito no git, sempre vai salvar a pessoa que fez a alteração. Além disso mostra o horário que foi realizada.*
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Criar repositório local
</h1>

`$ git init`

> *Reinicializa o repositório caso possua.*
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25">
  Verificar status dos arquivos
</h1>  
  
`$ git status`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Adicionar arquivo untrackted ao staged
</h1>

Um por vez                       | Tudo
:-------------------------------:|:---:
`$ git add <NomeDoArquivo>`<br/> |`$ git add .` <br/>
-|`$ git --all` <br/>
-|`$ git -A` <br/>

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25">
  Salvar uma versão, realizar um commit
</h1>

`$ git commit -m “mensagem do commit”`

> Verifica se o que você fez realmente foi salvo 
---

<h1>
   <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
   Inserir arquivo do staged no último commit já realizado
</h1>

`$git commit --amend`

> *Vai abrir o editor VIM, muda a mensagem lá em cima se quiser e depois escreve :wq para sair.* </br>
> *O w vem de write e q de quite.*
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25">
  Alterar mensagem do último commit realizado (Não tem na documentação oficial explicitamente) 
</h1>

`$ git commit -m “nova mensagem do commit” --amend` 

> *Se tiver outro arquivo no staged vai salvar junto nesse novo commit.* </br>
> *Para alterar somente a mensagem do commit, resolve o problema da mensagem no exato momento que fez, pois ai não vai ter nada no staged.*
---

<h1>
   <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
   Verificar todos os commits do arquivo
</h1>

sha-1 extenços | sha-1 curtos | sha-1 completos
:-------:|:---: | :---:
`$ git log`|`$ git log --oneline` | `$ git log --pretty=oneline` 

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25"> 
  Associar repositório local com o de origem
</h1>

`$ 	git remote add origin <UrlDoRepositorio>`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Verificar a URL do repositório remoto
</h1>

`$ 	git remote -v`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25"> 
  Trazer para o repositório local os arquivos do servidor 
</h1>

Primeira vez | Demais vezes (--set-upstream)
:---:|:---:
`$ git pull origin master` | `$ git pull`

>*Pode utilizar esse comando em qualquer branck que estiver*

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Enviar commit para o servidor
</h1>  
  
 Primeiro momento| Demais momentos
:---|:---
`$ git push --set-upstream origin master`| `$ git push`

 Comando curto| -
:--:|:---:
`$ git push -u origin master` | -

?| - 
:--:|:---:
`$ git push origin master` | - 

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25"> 
  Apaga os commits de cima para baixo mas não apaga o que foi feito no código, o tanto de commits (esse de cima para baixo), é o número especificado ao em N.    
</h1>
  
`$ git reset --soft HEAD~N`

>*Esse N representa o tanto de commit que será apagado de cima para baixo, lembrando, ele não altera o que foi feito no código.
>Dá para usar esse código para juntar vários commits em um só, mas vai ter que ser em ordem do mais novo para o mais velho sem pular nenhum.*
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Color" width="25"> 
  Juntar commits, amassar dois ou mais commit em um único commit
</h1>
  
Longo | Curto
:-----|:-----
`$ git rebase --interactive HEAD~N `|`$ git rebase -i HEAD~N`

>*O N significa o número de commit que vai querer juntar, é para abrir o vim, se não abrir usa o código abaixo para configurar.
>Vai abrir com umas palavras escritas pick, escreve squash no lugar deixando a primeira lá em cima com pick, aperte : e digite wq! para salvar e sair, vai abrir outra tela do vi para inserir um comentário, apaga todos os comentários que veio e digita o comentário que utilizado para detalhar essa junção.*
>Atenção: Faça isso antes de enviar os commits para o repositório, se já estiver lá e depois tentar juntar e dar push vai dar dor de cabeça.
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Black" width="25">
  + Configurar para abrir o vim
</h1>

`git config --global core.editor "vim"`

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Color" width="25"> 
  + Abortar o rebase
</h1>

`$ git rebase --abort`

>*Caso faça algo no vim e nõo consiga desfazer, MAS NÃO SALVOU, fecha o terminal git a abre novamente para abortar, vai voltar tudo para o que estava antes.*

---


<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25">
  Apaga os commits de cima para baixo até o repositório dado checkout 
</h1>

`$ git reset --hard  <6NumerosDoCommit>` 

>*Cuidado com esse comando. Apaga permantemente.*
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25"> 
  Retira algo do statged 
</h1>

Um por vez | Todos
:--- |:---
`$	git restore --staged <nomeDoArquivoNoStage>` | `$ git restore --staged .`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25"> 
  Clonar um repositório 
</h1>

`$ git clone "<UrlDoRepositorio>"`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25"> 
  Alterarnar versão do commit
</h1>

`$ git checkout <6NumerosDoSha1>`

---


<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-Black" width="25">
  Armazenar últimas alterações na memória do git para posteriormente realizar um commit 
</h1>

`$ git stash`

---


<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Mostrar os stash na memória para serem salvos
</h1>

`$ git statsh list`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-black" width="25"> 
  Verificar a diferença de um arquivo para o outro no terminal do git bash
</h1>

`$ git diff`
>*A comparação ocorre entre as modificações inseridas no documento que não possuem no commit anterior, ou seja, compara o arquivo salvo do último commit com os novos códigos inseridos, é o arquivo salvo no commit contra o mesmo arquivo com alterações. NÃO DÁ PARA VER AS ALTERAÇÕES CASO OS ARQUIVOS ESTEJAM NO STAGED!.*
---


<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Criar uma branch no repositório 
</h1>
  
`$ git branch <NomeDaBranch>`

---


<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-black" width="25"> 
  Listar as branches do repositório
</h1>

`$ git branch`

>*Caso o repositório for clonado, esse comando não vai listar todas as branches existentes, precisaria usar o `$ git checkout <NomeDaBranch>`, vai alterar para ela inclusive, mas dai em diante vai aparecer o nome da branch ao utilizar o comando `$ git branch`* </br>
>*Se tiver em equipe, e alguém realizar a criação da branch e enviar para o repositório, é necessário usar o comando `$git pull` trazer tudo do repositório de origin para o repositório remoto.*

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Enviar branch para o repositório
</h1>

`$ git push --set-upstream origin <NomeDaBranch>`

>*Usar `$ git checkout <NomeDaBranch>` primeiro* </br>
>*Cria uma nova branch no repositório de origin com o <NomeDaBranch> dado, associando essa nova branch criada no repositório remoto com a branch criada no repositório local, é muito importante usar o mesmo nome de branch nessa no comando `$ git --set-upstream origin <NomeDaBranch>` para não confundir, já que fica inviável, além de sem sentido, trabalhar com inúmeras ramificações com diferentes nomes no repositório de origin e remoto.*

---


<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-black" width="25"> 
  Alterar de branch
</h1>
`$ git checkout <NomeDaBranch>`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Alterar o nome da branch local
</h1>

Com checkout na própria | Com checkout em outra
:---:|:---:
`$ git branch -m <NovoNomedaBranch>` | `$ git branch -m <NomeDaBranch> <NovoNomeDessaBranch>`  

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-black" width="25"> 
  Alterar o nome da branch remota
</h1>

**Não há comando específico para fazer isso, segue abaixo um passo a passo para conseguir realizar o feito**
```
1. $ git pull
2. $ git branch -m <NovoNomeDaBranchLocal> 
3. $ git push --delete origin <NomeDaBranchQueVaiApagar>
4. $ git push --set-upstream origin <NomeDaBranch>
```

>*A ideia é renomear a branch local para ter todo o histórico do snapshoot, apagar a branch remota, criar uma nova com o nome desejado e associar essa criação a essa nova branch que foi renomeda no repositório local, tornando assim possível alterar o nome da branch remota, é importante usar o `$ git pull` para trazer todas as informaçoes da branch remota para o repositório local primeiro, além disso, é importe alinhar com a equipe para verificar se não tem ninguém usando ela naquele momento.*

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Criar uma branch e no exato momento alternar para ela
</h1>

`$ git checkout -b <NomeDaBranch>`

---


<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-black" width="25"> 
  Deletar branch local
</h1>

`$ git branch -d <NomeDaBranch>`

>*Não é possível fazer esse ato estando na branch que deseja apagar, significa que é necessário estar em outra branch.*</br>
>*As vezes pode ocorrer do git não deixar apagar, ai precisa utilizar o comando `$ git branch -D <NomeDaBranch>`.*
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Deletar branch remota
</h1>

`$ git push --delete origin <NomeDaBranch>`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-black" width="25"> 
  Fazer merge
</h1>

`$ git merge <NomeDaBranch>`

>*Estar com checkout na branch que gostaria de trazer os commit de outra ramificação.* </br>
>*Todos os commits dessa ramificação que está sendo usada para aplicar o merge ficarão nesse nova branch que foi dado o checkout, pode ser tanto a master como qualquer outra.*
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Criar uma Tag
</h1>

Com mensagem do último commit| Com mensagem específica para essa Tag
:---:|:---:
`$ git tag <NomeDaTag>`|`$ git tag -a <NomeDaTag> -m "Mensagem da tag, aparece no github"`

>*Cria na última versão do commit disponível, se quiser colocar a tag em um commit antigo, use o comando `$ git checkout <NumeroDoSha>` para ir até esse commit, em seguida crie uma tag normalmente, essa tag ficará associada nesse commit, outra maneira mais simples é utilizar o comando `$ git tag -a <NomeDaTag> <NumeroDoSha>`, se abrir o vim escreve uma mensgem aperta `Esc` coloca :wq e preciona enter para salvar e sair.* 
---


<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-black" width="25"> 
  Listar as tags do repositório local
</h1>

`$ git tag`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-color" width="25">
  Deletar tag  
</h1>

Repositório remoto | Repositório local
:---:|:---:
`$ git push --delete origin <NomeDaTag>` | `$ git tag -d <NomeDaTag>`

---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  Eviar tag para o repositório do github
</h1>

`$ git push origin <NomeDaTag>`

>*Ficam na opção tags (página do repositório no github).*
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-black" width="25"> 
  Apagar commit do repositório remoto
</h1>

`$ git push origin +<nomeDaBranch>`

>⚠️ *Antes the fazer essa instrução, remova os commits dos repositório local utilizando o comando `$ git reset --soft HEAD~N`, esse comando não apaga as nenhum arquivo, ele coloca todos os arquivos escolhidos novamente no staged, isso vai ser importante, pois a brach do repositório remoto vai ficar igual a sua branch local, portanto, desfaça os commits do seu repositório local deixando da forma que você deseja que o remote fique. <br />
Quando se tira esses aquivos do seu repositório local e coloca no staged, ao utilizar o comando `$ git push origin +master` o repositório remoto vai atualizar e ficar igual ao seu repostório local (ao pé da letra é como se tivesse apagando), lembresse que foi utilizado o comando `$ git reset --soft HEAD~N` para deixar o repositório sem os commits, mas com todos os arquivos da maneira como estavam, então faz um commit novamente e envia para o servidor.* <br /> 
>+ *O caractere "+" ao lado do nome da brach significa que está forçando uma atualização naquela branch, nesse caso o "master" é o nome da branch, vale lembrar que deve ser a mesma brach do reporitório local.* <br />
<strong>Na verdade esse comando deixa a ramificação remote exatamente igual a local, independente de como esteja um ou outro, usando esse comando faz com que a remota fique exatamente igual a local, cuidado ao fazer isso.<strong>
---

<h1>
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Color.png" alt="Git-logo.Mark-Color" width="25">
  <img src="https://github.com/RRICHARRD/Git/blob/master/git-image/Git-Logo.Mark-Black.png" alt="Git-logo.Mark-black" width="25"> 
  Créditos
</h1>

Git Logo by [Jason Long](https://twitter.com/jasonlong) is licensed under the [Creative Commons Attribution 3.0 Unported License.](https://creativecommons.org/licenses/by/3.0/)
