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

Podemos criar também uma chave de acesso - SSh - que facilita nossa vida para utilizar o git hub.

Verificar chaves SSH existentes.
Abra o Terminal
Digite ls -al ~/.ssh para ver se tem alguma chave SSH presente
$ ls -al ~/.ssh
# Lista os arquivos do seu diretório .ssh, se eles existem
Por padrão, o nome dos arquivos das chaves públicas pode ser um dos seguintes:
id_dsa.pub
id_ecdsa.pub
id_ed25519.pub
id_rsa.pub
Bom se você não tem um par de chave pública e privada, ou não quer conectar as que estão disponíveis no Github, então gere uma chave nova.
Se você viu um par de chave pública e privada listado (por exemplo id_rsa.pub and id_rsa) e gostaria de usá-las para conectar com o Github, você pode adicionar sua chave SSH ao SSH-agent e pular o próximo passo da geração de chave do tutorial.
Gerar uma nova chave SSH
Abra o terminal
Digite isso, substituindo pelo seu email do Github.
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
Isso cria uma nova chave ssh, usando o email como rótulo.
3. Quando aparecer escrito no terminal “Enter a file in which to save the key,” pressione Enter. Isso aceita a localização do arquivo padrão.
Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]
4. No terminal, digite uma senha segura.
Enter passphrase (empty for no passphrase): [Type a passphrase]
Enter same passphrase again: [Type passphrase again]
Adicionando sua chave SSH ao ssh-agent
Antes de adicionar um nova chave SSH no ssh-agent para gerenciar suas chaves, você deveria Verificar chaves SSH existentes e Gerar uma nova chave SSH se for preciso.
Inicie o ssh-agent em background.
$ eval "$(ssh-agent -s)"
Agent pid 59566
2. Adicione sua chave privada SSH no ssh-agent. Se você criou sua chave com um nome diferente, substitua id_rsa no comando com o nome de sua chave privada.
$ ssh-add ~/.ssh/id_rsa

site: https://medium.com/@rgdev/como-adicionar-uma-chave-ssh-na-sua-conta-do-github-linux-e0f19bbc4265



Para adicionar o repositorio no git hub:
git remote add origin git@github.com:login/repositorio.git

atualizar o github do seu repositório:
git push -u origin master


