# relatorioGit



Relatório de aprendizado Git

# Configuração do Ambiente

No começo da trilha 1, aprendemos como configurar o ambiente no geral, como por exemplo a instalação do WSL, configuração de usuário e etc. aqui está um exemplo do manual, onde abrimos para ter uma ajuda extra durante o curso:

 ![image](https://github.com/user-attachments/assets/c0c8c0d8-d0cb-404f-abbc-af8f85f005ff)
![image](https://github.com/user-attachments/assets/86762933-061a-437e-a493-1a006d89c18a)

 
# Comandos Básicos

Algumas perguntas sobre comandos opcionais e necessários, comandos porcelain e plumbing:

  

![image](https://github.com/user-attachments/assets/19b2d090-3add-4cfc-91e5-a1ff398ad302)



# Criação de Pastas e Arquivos

Criação de pastas e arquivos e também iniciar o arquivo .git além de também adicionar conteúdos dentro deles:
 
 ![image](https://github.com/user-attachments/assets/db75ed20-d461-471b-ac59-ed67b8409405)
![image](https://github.com/user-attachments/assets/9943243f-4f03-4734-9775-bf996055c815)
![image](https://github.com/user-attachments/assets/5abb21bd-9a94-4c8f-850d-4a722582df99)

 
# Visualização de Hashs

Ensinou também a ver as hashs únicas de cada arquivo e commit:
 
 ![image](https://github.com/user-attachments/assets/c87a2e06-363f-4344-8283-b235b6d8c7a4)
![image](https://github.com/user-attachments/assets/45c898dc-cccd-4ed4-8a27-ce034f5af06c)


Usamos também comandos como o –unset, o –get <key> e o --list para ver as configurações de um único, vários ou até mesmo mudar um valor

Adicionei vários CEOs com 

`git config --add webflyx.ceo "Warren"`
`git config --add webflyx.ceo "Carson"`
`git config --add webflyx.ceo "Sarah"`


# Branches

usamos –remove-section para remover seções e também vemos os tipos de overrides e o funcionamento das branchs, como por exemplo criar, remover mudar e visualizar:

 ![image](https://github.com/user-attachments/assets/590c5584-6c3f-4590-b564-78973c20dbdd)
![image](https://github.com/user-attachments/assets/048e150a-7940-4bf2-9664-5e5b87d1d0c2)

 
# Merge

Aprendi também sobre o merge, que consiste em subir o conteúdo de uma branch para outra, voltar commits, voltar merges, etc.

# Rebase

Aprendi sobre o Rebase também e as diferenças dele para o merge, um rebase seria basicamente você reescrever o histórico de commits
 
![image](https://github.com/user-attachments/assets/a9bb3731-8040-417c-bf64-149faeb8afef)
![image](https://github.com/user-attachments/assets/65a1f7f9-10db-4185-ad2a-465d6b2b7f46)

 
# Reset de Commits

Aprendi também como resetar o último commit com `git reset --soft COMMITHASH` e também a resetar sem manter as mudanças com `git reset --hard COMMITHASH`, além de também conseguir voltar a um commit específico com `git reset --hard a1b2c3d`, porém esse comando é perigoso, pois paga as coisas que foram feitas na frente.


# Repositório Remoto

Aprendi como criar também um repositório remoto, que consiste em criar um novo repositório porém com os mesmos commits, para que você possa mexer a vontade nele `git remote add <name> <uri>` e para puxar as informações `git fetch`.


# Pull, Push e Pull Requests

Aprendi sobre git pull, git push, pull requests, merge pull requests para transformar a branch remota na main, gitignore, para deixar sua aplicação mais leve como por exemplo ignorar uma boa parte do node_module, que é pesadíssimo.

# Fork

Aprendemi também o “fork”, que é basicamente uma cópia do repositório inteiro onde você pode fazer o que quiser nele sem alterar o principal, fizemos uma cópia da “cópia” e configuramos também.


# Deletar Branch e Recuperar Arquivo

Logo em seguida aprendi a deletar uma branch e a recuperar um arquivo perdido, o que muitas vezes acontece por acidente, nós podemos recuperar pela hash, pois mesmo apagando, a hash continua lá, então pegamos com o `git cat-file -p “nome-do-arquivo”` e depois recriamos.


# Conflitos de Merge

Aprendi também a resolver conflitos de merge, não só em um como em vários arquivos, pois o git não os resolve automaticamente após um commit, após achar o conflito, você deve alterar o arquivo antes de subir, ou forçar o merge, substituindo os dados do merge anterior pelo seu. 


# Conflitos de Rebase

Além de resolver conflitos com merge, resolvi também conflitos de rebase, que consiste basicamente na mesma coisa, entrar no arquivo, modifica-lo para que sumam as diferenças entre os rebases e “commitar” depois.


# Rerere

Entendi como funciona o rerere, que consiste em resolver automaticamente os conflitos e dar uma sugestão para você, ao aceitar, ele meio que junta os dois rebases ou merges e joga uma versão em conjunto para você.


# Reverter Commits

Foi falado também sobre como voltar um commit que foi feito errado ou sem querer com o comando `git reset --soft HEAD~1`, onde o HEAD~1 consiste basicamente onde você estava um “movimento” atrás.


# Squashing

Aprendi sobre Squashing, que consiste em pegar o conteúdo de vários commits e jogar dentro de um único commit com `git rebase -i HEAD~3`, aqui nesse exemplo eu voltei 3 commits e joguei todos dentro de um único commit.


# Stash

No curso eles ensinam também sobre Stash, que consiste em guardar as informações não commitadas para que você possa murdar de branch para fazer algo urgente por exemplo. Os códigos necessários são git stash para guardar e depois quando voltar para a branch você usa git stash pop, onde ele volta os arquivos alterados anteriormente. Obs(Você pode até mesmo fazer mais de um stash ao mesmo tempo, só não é muito recomendado)


# Revert

Sobre o git revert, ele basicamente é um git reset melhorado, pois ele altera um commit anterior sem alterar o histórico ou apagar o commit, ele cria um novo commit, o que ajuda muito se você for trabalhar em uma equipe, você pode usar junto com o git diff, que mostra a diferença entre o commit anterior e a working tree atual.

# Cherry Pick

Explicaram também sobre o Cherry Pick, que consiste basicamente em puxar um commit específico de uma branch ao invés de puxar todas as alterações feitas na branch, útil em algumas ocasiões, mas não é muito utilizado por iniciantes. Código para fazer um cherry pick `git cherry-pick <commit-hash>`.


# Git Bisect

Aprendi também sobre o bisect, um comando muito útil, que consiste em tentar achar um bug a partir de uma vasculha em binário pelo sistema, onde você coloca a partir de qual commit estava fucionando normalmente e em qual começou a dar erro, então vai marcando um por um se está bad ou good, consequentemente achando onde começou o bug.


# Tags

E por último, ensinaram sobre as tags, que serve basicamente para facilitar o versionamento entre os commits, por exemplo v.3.12.5.
