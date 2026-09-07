# 🛠️ Git Cheat Sheet & Dev Diary

Bem-vindos ao nosso diário de bordo comunitário! 

Este repositório é a nossa base de conhecimento compartilhada. O objetivo aqui é documentar comandos úteis de Git, padronizações de projeto e, principalmente, registrar aqueles problemas chatos que resolvemos na força do ódio para nunca mais precisarmos pesquisar a solução do zero.

---

## 📑 Índice
1. [Como Contribuir](#-como-contribuir)
2. [Padrão de Commits (Conventional Commits)](#-padrão-de-commits)
3. [Como Registrar um Problema (Troubleshooting)](#-como-registrar-um-problema)
4. [Estrutura do Repositório](#-estrutura-do-repositório)

---

## 🤝 Como Contribuir

Para manter a organização, não faça commits diretos na branch `main`. Siga este fluxo:

1. **Atualize seu repositório local:**
   ```bash
   git pull origin main
   ```
2. **Crie uma nova branch para a sua dica/solução:**
   ```bash
   git checkout -b feat/minha-nova-dica
   ```
3. **Adicione seu conteúdo** seguindo os templates abaixo.
4. **Faça o commit** usando o [Padrão de Commits](#-padrão-de-commits).
5. **Envie para o GitHub:**
   ```bash
   git push origin feat/minha-nova-dica
   ```
6. **Abra um Pull Request (PR)** e peça para alguém dar um "Approve" rápido.

---

## 🏷️ Padrão de Commits

Nós utilizamos o **Conventional Commits** para manter o histórico legível. Todo commit deve seguir este formato:

`<tipo>: <descrição curta em minúsculas e no imperativo>`

### Tipos permitidos:
* **`feat:`** Adiciona uma nova dica, tutorial ou registro de problema. *(Ex: feat: adiciona solucao para conflito de merge rebase)*
* **`fix:`** Corrige um comando errado ou erro de digitação em algum documento. *(Ex: fix: corrige flag do comando git commit)*
* **`docs:`** Alterações no README ou na estrutura de documentação. *(Ex: docs: atualiza regras de contribuicao)*
* **`chore:`** Manutenção, organização de pastas ou arquivos ignorados. *(Ex: chore: organiza arquivos da pasta troubleshooting)*

---

## 🚨 Como Registrar um Problema

Esta é a seção mais importante do repositório! Se você travou em um erro, resolveu e quer deixar registrado, crie um arquivo Markdown (`.md`) na pasta `/troubleshooting` ou adicione a um arquivo existente usando **exatamente** o formato abaixo:

### Template de Registro

**Eu acabei de ter um problema assim:**  
> Descreva o problema de forma clara. Inclua a mensagem de erro do terminal, se houver.
> *Exemplo: Fui fazer um push, mas o repositório remoto tinha alterações que eu não tinha localmente. O terminal retornou `error: failed to push some refs`.*

**E a solução foi esse comando:**  
```bash
# Cole o comando exato aqui
git pull origin main --rebase
```

**Ele serve para tal coisa:**  
> Explique de forma simples o que o comando faz nos bastidores. 
> *Exemplo: Esse comando baixa as alterações do repositório remoto e aplica os meus commits locais "por cima" deles, criando uma linha do tempo limpa sem commits extras de merge.*

---

## 📂 Estrutura do Repositório

Organize seus arquivos da seguinte forma para facilitar a busca:

```text
├── /cheatsheets          # Guias rápidos de comandos (ex: git-basico.md, docker-basico.md)
├── /troubleshooting      # Registros de problemas e soluções (siga o template acima)
└── README.md             # Este arquivo
```

---
*Feito com ☕ e muito Git Reset pelos membros da equipe.*
