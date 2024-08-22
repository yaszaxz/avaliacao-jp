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