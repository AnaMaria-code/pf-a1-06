# Guia de Comandos Git

Este documento apresenta **20 comandos do Git**, agrupados por categoria, contendo **explicação** e **2 exemplos de uso** para cada comando.

---

## 1. Configuração Inicial

### 1. `git config`
Configura informações do Git, como nome e e-mail do usuário.

**Exemplo 1:**
```bash
git config --global user.name "Ana Carolina"
```

**Exemplo 2:**
```bash
git config --global user.email "ana@email.com"
```

---

### 2. `git init`
Inicializa um novo repositório Git em uma pasta.

**Exemplo 1:**
```bash
git init
```

**Exemplo 2:**
```bash
git init meu-projeto
```

---

### 3. `git clone`
Cria uma cópia local de um repositório remoto.

**Exemplo 1:**
```bash
git clone https://github.com/user/repositorio.git
```

**Exemplo 2:**
```bash
git clone https://github.com/user/repositorio.git projeto-local
```

---

## 2. Verificação de Estado

### 4. `git status`
Mostra o estado atual dos arquivos.

**Exemplo 1:**
```bash
git status
```

**Exemplo 2:**
```bash
git status -s
```

---

### 5. `git log`
Exibe o histórico de commits.

**Exemplo 1:**
```bash
git log
```

**Exemplo 2:**
```bash
git log --oneline
```

---

### 6. `git diff`
Mostra diferenças entre versões dos arquivos.

**Exemplo 1:**
```bash
git diff
```

**Exemplo 2:**
```bash
git diff main develop
```

---

## 3. Manipulação de Arquivos

### 7. `git add`
Adiciona arquivos para a área de stage.

**Exemplo 1:**
```bash
git add arquivo.txt
```

**Exemplo 2:**
```bash
git add .
```

---

### 8. `git rm`
Remove arquivos do repositório.

**Exemplo 1:**
```bash
git rm arquivo.txt
```

**Exemplo 2:**
```bash
git rm --cached arquivo.txt
```

---

### 9. `git mv`
Move ou renomeia arquivos.

**Exemplo 1:**
```bash
git mv antigo.txt novo.txt
```

**Exemplo 2:**
```bash
git mv pasta1/arquivo.txt pasta2/
```

---

## 4. Commits

### 10. `git commit`
Salva alterações no histórico do projeto.

**Exemplo 1:**
```bash
git commit -m "Adiciona tela inicial"
```

**Exemplo 2:**
```bash
git commit -am "Corrige bug no login"
```

---

### 11. `git commit --amend`
Permite alterar o último commit realizado.

**Exemplo 1:**
```bash
git commit --amend
```

**Exemplo 2:**
```bash
git commit --amend -m "Mensagem corrigida"
```

---

## 5. Branches

### 12. `git branch`
Gerencia branches no repositório.

**Exemplo 1:**
```bash
git branch
```

**Exemplo 2:**
```bash
git branch nova-feature
```

---

### 13. `git checkout`
Troca de branch ou restaura arquivos.

**Exemplo 1:**
```bash
git checkout develop
```

**Exemplo 2:**
```bash
git checkout -b feature-login
```

---

### 14. `git switch`
Alternativa moderna para trocar branches.

**Exemplo 1:**
```bash
git switch main
```

**Exemplo 2:**
```bash
git switch -c hotfix
```

---

## 6. Merge e Rebase

### 15. `git merge`
Une branches diferentes.

**Exemplo 1:**
```bash
git merge develop
```

**Exemplo 2:**
```bash
git merge feature-login
```

---

### 16. `git rebase`
Reorganiza o histórico de commits.

**Exemplo 1:**
```bash
git rebase main
```

**Exemplo 2:**
```bash
git rebase -i HEAD~3
```

---

## 7. Repositório Remoto

### 17. `git remote`
Gerencia conexões com repositórios remotos.

**Exemplo 1:**
```bash
git remote -v
```

**Exemplo 2:**
```bash
git remote add origin https://github.com/user/projeto.git
```

---

### 18. `git push`
Envia commits para o repositório remoto.

**Exemplo 1:**
```bash
git push origin main
```

**Exemplo 2:**
```bash
git push -u origin develop
```

---

### 19. `git pull`
Baixa e integra alterações do repositório remoto.

**Exemplo 1:**
```bash
git pull
```

**Exemplo 2:**
```bash
git pull origin main
```

---

### 20. `git fetch`
Baixa atualizações do repositório remoto sem aplicar merge.

**Exemplo 1:**
```bash
git fetch
```

**Exemplo 2:**
```bash
git fetch origin
```

---

# 📌 Resumo por Categoria

| Categoria | Comandos |
|-----------|----------|
| Configuração | `git config`, `git init`, `git clone` |
| Verificação | `git status`, `git log`, `git diff` |
| Arquivos | `git add`, `git rm`, `git mv` |
| Commits | `git commit`, `git commit --amend` |
| Branches | `git branch`, `git checkout`, `git switch` |
| Integração | `git merge`, `git rebase` |
| Remoto | `git remote`, `git push`, `git pull`, `git fetch` |

---
