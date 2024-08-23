# avaliacao-jp
Avaliação curso. 

-----------Comandos de configuração do git-----------
1. git --version
    - Verifica a versão do git instalada no pc.
2. git config --global (user.name/user.email)
    - Configura o nome de usuário e e-mail. Deve ser o mesmo e-mail usado na conta do GitHub.

-----------Comandos de criação de chave SSH-----------
1. ls -al ~/.ssh
    - Este comando irá verificar se existe uma chave SSH no computador.
2. ssh-keygen -t ed25519 -C "emai do github"
    - Vai criar uma chave SSH.
3. eval "$(ssh-agent -s)"
    - Realiza a inicialização do agente-ssh.
4. ssh-add ~/.ssh/id_ed25519
    - Adiciona a chave SSH ao agente criado com o comando anterior.
5. clip < ~/.ssh/id_ed25519.pub
    - Copia a chave SSH criada anteriormente.
6. ssh -T git@github.com
    - Testa a conexão. Mas antes de executar o comando, é importante adicionar a chave SSH ao GitHub. Para isso, vá em "Settings", depois em "SSH and GPG keys", "New SSh key" e cola a chave SSH que foi copiada com o comando anterior.

---------------------Comandos Git---------------------
1. git init
    - Comando usado para configuração inicial de um novo repositório. Cria um novo repositório no diretório selecionado.
2. git status
    - Mostra o estado do repositório, mostrando arquivos modificados, novos arquivos e arquivos preparados para commit.
3. git add <nomeDoArquivo>
    - Cria um novo arquivo no índice atual. Além disso, ele prepara os arquivos selecionados para commit.
4. git rm --cached <arquivo>
    - Remove o arquivo escolhido do índice. Os arquivos selecionados não são removidos do diretório, apenas do índice. Para adicionar o arquivo novamente, use o comando 3.
5. git branch
    - Exibe todas as branches locais.
6. git branch -r
    - Exibe todas as branches online.
7.  git branch -a
    - Mostra as branches locais e online.
8. git checkout <nomeDaBranch>
    - Muda para a branch selecionada. Para retornar à branch anterior, é só usar o mesmo comando, mas com o nome da outra branch.
9. git checkout -b <nomeDaBranch>
    - Cria uma nova branch e entra nela automaticamente. Para voltar para a outra branch é do mesmo jeito de antes.
10. git branch -D <nomeDaBranch>
    - Deleta a branch escolhida.
11. git commit -m "<descrição>
    - Faz um commit de mudanças realizadas no índice com uma mensagem que descreve as mudanças realizadas.
12. git merge <branch>
    - Junta a branch atual com a mencionada.
13. git push
    - Envia os commits feitos para o repositório do github.
14. git fetch
    - Puxa oq tem no repositorio do github pro pc.
15. git pull
    - Mesma coisa do comando de antes, soq esse ai mescla as branches locais e online.
