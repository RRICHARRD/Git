# AprendendoGit
Repositório criado para o aprendizado básico de Git. 

**git config --list** //VE O NOME, O EMAIL E MAIS ALGUMAS COISAS 
**git config --global user.name "Inserir meu nome"** //CONFIGURA O NOME
**git config --global user.email "Inserir o email do meu Github"** //CONFIGURA O EMAIL

**git init** //INICIA UM REPOSITÓRIO LOCAL NA PASTA DO PROJETO (git bash)
**git remote add origin https://github.com/RRICHARRD/meuprojeto.git** //ASSOCIA O REPOSITÓRIO LOCAL COM O REMOTO, USA O APELIDO ORIGIN.
**git pull origin master** //TROCAR O MAIN POR MASTER NAS CONFIGURAÇÕES PRIMEIRO, SÓ FAZER ESSE COMANDO SE O ARQUIVO .gitignore FOR CRIADO DIRETAMENTE PELO GITHUB

**git status** //VERIFICA OS ARQUIVOS
**git add .** //ADICIONA TODOS OS ARQUIVOS AO STAGE

**git commit -m "Projeto criado"** //SALVA UMA NOVA VERSÃO DO PROJETO
**git push -u origin master** //ENVIA O REPOSITÓRIO LOCAL PARA O REPOSITÓRIO REMOTO, DEPOIS É SÓ FAZER O COMANDO **git push**

**git log --oneline** //VERIFICO TODOS OS COMMITS REALIZADOS NO PROMPT, VEJO O TODOS OS NOMES DEFINIDOS, INCLUSIVE QUANDO É REALIZADO UM CLONE. 


# Clonado um repositório

**git clone https://github.com/NomeDoUsuario/NomeProjetoParaClonar.git** //COMANDO PARA CLONAR UM REPOSITÓRIO, SE ELE JÁ EXISTE NA MINHA MÁQUINA NÃO TEM COMO CLONAR, DAR UM GIT BASH NA PASTA ONDE EU VOU QUERER DEIXAR A PASTA DO ARQUIVO CLONADO. VERIFICAR NO **git config --list** SE REALMENTE É MEUS DADOS QUE ESTÃO SENDO UTILIZADOS, NO CASO O EMAIL DO GITHUB E O NOME. APLICAR UM **git add .** DENTRO DA PASTA DO ARQUIVO CLONADO PARA COLOCAR AS COISAS NO STAGED, DEPOIS **git commit -m "mensagem de explicação"** PARA SALVAR AS ALTERAÇÕES E **git push** PARA SALVAR NO REPOSITÓRIO DO GITHUB.


