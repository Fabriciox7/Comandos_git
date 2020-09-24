# git-course
Este é um repositório teste para ensinar como o git funciona.

Inicializar um repositório -- git init;

ciclo de vida dos status dos arquivos:
    untracked -> unmodified -> modified -> staged [commit]

    para adicionar arquivos: git add nomedoarquivo.txt
    para commitar : git commit -m "mensagem sobre o commit" {apenas commitar os que já foram adicionados no staged}

    para adicionar e comitar: git commit -am "descrição sobre o commit"

    Para saber sobre o status dos arquivos: git status;

    Para cada commit a uma identificação na qual podemos trabalhar para desfazer a alteração ou voltar ao um estado que queremos - hash.

    Para saber o histórico de commits, temos o comando: git log , podemos visualizar todos os commits e sua hash's.

    Podemos buscar também com alguns filtros , por exemplo:

    git log --decorate;
    git log --author="nome";

    git shortlog ; É um git log bem resumido.
    git shortlog -sn ; Sabemos o número de commits de cada desenvolvedor contribuinte.
    git log --graph; 
    git show <identificado_hash>

    Alguns comandos  que facilita a edição de alterações indevidas antes de commitar.

    git checkout <nome_arquivo> ; antes do git add {remove alteração} ;

    para remover alteração que já foi adicionada, usamos : git reset HEAD. A informação volta para o estágio de unmodified e podemos usar o git checkout para remover.

    Remover uma alteração depois do commit.Existe três opções:

    git reset --soft <hasH_anterior_a_que_deseja_refazer>  = exclui o commit mas retornar as altterações para o staged,não perdendo informações e possibilidando a edição sem perder dado.

    git reset --mixed hasH_anterior_a_que_deseja_refazer>  = exclui a modificação e ainda retorna os dados para o estado de modified.

    git reset --hard <hash anterior a que exclui> = simplesmente apaga o commit anterior.Deve-se ter cuidado ao usar este método.