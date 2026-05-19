# Diretrizes e Relatório de Execução do GitFlow - PrettyFlights

Este documento registra as diretrizes oficiais de ramificação e o histórico real da simulação do ciclo de vida da versão 1.0.0 do Módulo do Totem de Check-in do PrettyFlights.

## 1. Estrutura de Branches Adotada

* **`main`**: Centraliza o código estável em produção. Cada atualização gera uma tag de versão incremental (`v1.0.0`, `v1.0.1`).
* **`develop`**: Linha base para integração de novas funcionalidades.
* **`feature/*`**: Ramificações temporárias para o desenvolvimento de novas features (ex: `feature/localizador-checkin`).
* **`release/*`**: Fase de congelamento de código para testes e ajustes finais antes do deploy.
* **`hotfix/*`**: Ramificação emergencial para correção de bugs críticos encontrados diretamente em produção.

---

## 2. Relatório de Atividades da Execução Real (Passo a Passo)

Abaixo está o registro cronológico das atividades executadas no repositório, documentando as ações tomadas e as correções de percurso efetuadas:

### A) Inicialização do Repositório
* **Atividade:** Criação da estrutura inicial e vinculação com o GitHub.
* **Comandos executados:** `git init -b main`, criação do guia de comandos e push inicial para o repositório remoto.

### B) Criação da Estrutura Permanente
* **Atividade:** Criação da branch de integração contínua.
* **Comandos executados:** `git checkout -b develop` seguido de `git push -u origin develop`.

### C) Desenvolvimento da Feature
* **Atividade:** Criação da funcionalidade de busca por localizador alfanumérico no totem.
* **Comandos executados:** Criação da branch `feature/localizador-checkin` e desenvolvimento do arquivo de código `checkin.py`.

### D) Integração da Feature na Develop
* **Atividade:** Incorporação da feature concluída na linha de desenvolvimento utilizando merge não-fast-forward para preservar o histórico.
* **Comandos executados:** `git checkout develop`, `git merge --no-ff feature/localizador-checkin` e deleção da branch temporária com `git branch -d`.

### E) Criação da Release 1.0.0 e Resolução de Conflito
* **Atividade:** Preparação da versão estável, publicação em produção (`main`) e atualização da `develop`.
* **Nota de Execução (Correção de Percurso):** Durante a tentativa de merge na `main`, foi identificado que o arquivo inicial possuía um erro de grafia (`chechin.py`). O arquivo foi corrigido localmente para `checkin.py` com o comando `mv` do terminal e adicionado via `git add checkin.py`.
* **Resolução de Conflito:** Ao executar o merge da release com a main atualizada, ocorreu um conflito no arquivo de código. O conflito foi solucionado aplicando a estratégia `git checkout --theirs checkin.py`, assumindo as alterações homologadas na release.
* **Finalização:** O merge foi concluído e a tag oficial `v1.0.0` foi gerada na `main`.

### F & G) Correção de Bug Emergencial (Hotfix 1.0.1)
* **Atividade:** Tratamento de uma falha crítica de estouro de memória que travava a tela do totem nos aeroportos em tempo real.
* **Nota de Execução:** Criada a branch `hotfix/tela-travada` a partir da `main`. O código foi corrigido inserindo a função `corrigir_timeout()`.
* **Sincronização:** O hotfix foi mesclado com sucesso na `main` (gerando a tag de patch `v1.0.1`) e reincorporado na `develop` para garantir que a correção persista nas próximas versões do sistema.
