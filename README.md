# Comandos do git

Este é um repositório que desenvolvi para colocar os principais comandos do git e algumas informações que devemos saber ao utilizarmos. Espero que ajude você também.

Para inicializar um repositório: 
    git init;
Entendermos o ciclo dos arquivos nos torna mais atentos quando estiver utilizando, então, que possamos lembrar.

   ![alt text](https://git-scm.herokuapp.com/book/en/v2/images/lifecycle.png "Logo Title Text 1")
      

 Sabendo o ciclo, podemos continuar com os comandos.
 Para sabermos os status dos arquivos no ciclo:
     
    git status
  
 Para adicionar um arquivo para o staged:
    
    git add <nome_arquivo.md>
    
 Para enviarmos ao repositorio local (obs- só é enviado aquele arquivo que esta no staged):
    
    git commit -m "descrição sobre o commit" 
    
 Para adicionar e commitar simultaneamente:
    
    git commit -am "observação sobre o commit"
    
Podemos afirmar também, que para cada commit teremos uma identificação para os commit's, possibilitando assim fazer algumas alterações ou saber quando foi feito tal alteração.

Para sabermos o histórico dos commit's:
    
    git log

obs- existem flags que auxiliam na busca por algum commit específico.
Ex:  
        
        git log --author="nome"

Para saber o historico dos commit's mais enxuto, sem muita informação temos:
    
    git shortlog

Encontrando o commit que deseja, e copiando sua hash você tem a opção de apenas visualizar suas informações:
    
    git show <hash_do_commit>
    
Alguns comandos que facilitam a edição ou alterações indevidas:

 - Remove alteração antes de usar o git add:
        
        git checkout nome_arquivo.txt
 - Remove alteração que foi adicionada e não "commitada" ainda:
        
        git reset HEAD
 - Remove alteração depois de ter feito o commit:
        
        git reset --soft (a alteração volta para o estado staged)
        git reset --hard (a alteração volta para 0 estado modified) 
        e temos o git reset --hard (não aconselho usar muito essa pois ao utilizarmos a informação é apagada e não podemos alterar mais, ou seja ,foi perdida)

Aqui também irei repassar comandos de um assunto bem importante - branchs.

Para criar uma branch:
    
    git checkout -b nome_branch
Para excluir uma branch:
    
    git checkout -D nome_branch
Para listar as branch's:
    
    git branch
Para escolher uma branch:
    
    git checkout nome_branch
    

Ao ultilizarmos branch, podemos fazer uso de multiplas partições e após as alterações, unir as branhc's.Para isso temos duas formas de unificá-las:
   Merge: Com esse método, iremos ter um histório de toda a passagem até unir elas e iremos ter que acrescentar um commit:
            
            git merge nome_brach
   Rebase: Nesse método,a união é deixada no mesmo commit, ou seja, não da pra identificar que veio uma alteração de uma branch antiga,ou seja, o histórico fica linear. Então, se não for alguma alteração que precise saber sobre o detalhe da alteração em sí, o melhor é usá-lo:
        
        git rebase nome_branch
        
######Com o uso do git e git hub, espero atualizar esse Readme e fazer algo mais completo para os que estão iniciando, e para que possa ser um tira dúvidas para quem já sabe mas não usa com tanta frequência a ferramenta.        
