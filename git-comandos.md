1. Configuração Inicial
1. git config

Configura informações do Git, como nome e e-mail do usuário.

Exemplo 1:

git config --global user.name "Ana Carolina"

Exemplo 2:

git config --global user.email "ana@email.com"
2. git init

Inicializa um novo repositório Git em uma pasta.

Exemplo 1:

git init

Exemplo 2:

git init meu-projeto
3. git clone

Cria uma cópia local de um repositório remoto.

Exemplo 1:

git clone https://github.com/user/repositorio.git

Exemplo 2:

git clone https://github.com/user/repositorio.git projeto-local
2. Verificação de Estado
4. git status

Mostra o estado atual dos arquivos.

Exemplo 1:

git status

Exemplo 2:

git status -s
5. git log

Exibe histórico de commits.

Exemplo 1:

git log

Exemplo 2:

git log --oneline
6. git diff

Mostra diferenças entre versões dos arquivos.

Exemplo 1:

git diff

Exemplo 2:

git diff main develop
3. Manipulação de Arquivos
7. git add

Adiciona arquivos para a área de stage.

Exemplo 1:

git add arquivo.txt

Exemplo 2:

git add .
8. git rm

Remove arquivos do repositório.

Exemplo 1:

git rm arquivo.txt

Exemplo 2:

git rm --cached arquivo.txt
9. git mv

Move ou renomeia arquivos.

Exemplo 1:

git mv antigo.txt novo.txt

Exemplo 2:

git mv pasta1/arquivo.txt pasta2/
4. Commits
10. git commit

Salva alterações no histórico.

Exemplo 1:

git commit -m "Adiciona tela inicial"

Exemplo 2:

git commit -am "Corrige bug no login"
11. git amend

Altera o último commit.

Exemplo 1:

git commit --amend

Exemplo 2:

git commit --amend -m "Mensagem corrigida"
5. Branches
12. git branch

Gerencia branches.

Exemplo 1:

git branch

Exemplo 2:

git branch nova-feature
13. git checkout

Troca de branch ou restaura arquivos.

Exemplo 1:

git checkout develop

Exemplo 2:

git checkout -b feature-login
14. git switch

Alternativa moderna ao checkout para branches.

Exemplo 1:

git switch main

Exemplo 2:

git switch -c hotfix
6. Merge e Rebase
15. git merge

Une branches.

Exemplo 1:

git merge develop

Exemplo 2:

git merge feature-login
16. git rebase

Reorganiza histórico de commits.

Exemplo 1:

git rebase main

Exemplo 2:

git rebase -i HEAD~3
7. Repositório Remoto
17. git remote

Gerencia conexões remotas.

Exemplo 1:

git remote -v

Exemplo 2:

git remote add origin https://github.com/user/projeto.git
18. git push

Envia commits para o repositório remoto.

Exemplo 1:

git push origin main

Exemplo 2:

git push -u origin develop
19. git pull

Baixa e integra alterações remotas.

Exemplo 1:

git pull

Exemplo 2:

git pull origin main
20. git fetch

Baixa atualizações remotas sem mesclar.

Exemplo 1:

git fetch

Exemplo 2:

git fetch origin
