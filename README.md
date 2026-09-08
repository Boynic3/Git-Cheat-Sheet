# 🛠️ Git Cheat Sheet & Dev Diary

Bem-vindos ao nosso diário de bordo comunitário!

Este repositório é a nossa base de conhecimento compartilhada. O objetivo aqui é documentar comandos úteis de Git, padronizações de projeto e, principalmente, registrar aqueles problemas chatos que resolvemos na força do ódio para nunca mais precisarmos pesquisar a solução do zero.

---

## 📑 Índice

1. [Como Contribuir](#como-contribuir)
2. [Padrão de Commits (Conventional Commits)](#padrao-de-commits)
3. [Como Registrar um Problema (Troubleshooting)](#registrar-problema)
4. [Estrutura do Repositório](#estrutura)

---

## <a id="como-contribuir"></a>🤝 Como Contribuir

Não faça commits diretos na branch `main` — toda mudança passa por uma branch própria e um Pull Request.

O fluxo completo, o **padrão de nomenclatura de branches** (`feat/`, `fix/`, `docs/`, etc.) e as regras para abrir um PR estão detalhados no **[CONTRIBUTING.md](./CONTRIBUTING.md)**. Ao abrir um Pull Request, o [template padrão](./.github/PULL_REQUEST_TEMPLATE.md) é carregado automaticamente.

---

## <a id="padrao-de-commits"></a>🏷️ Padrão de Commits

Nós utilizamos o **Conventional Commits** para manter o histórico legível. Todo commit deve seguir este formato:

`<tipo>: <descrição curta em minúsculas e no imperativo>`

### Tipos permitidos:

- **`feat:`** Adiciona uma nova dica, tutorial ou registro de problema. _(Ex: feat: adiciona solucao para conflito de merge rebase)_
- **`fix:`** Corrige um comando errado ou erro de digitação em algum documento. _(Ex: fix: corrige flag do comando git commit)_
- **`docs:`** Alterações no README ou na estrutura de documentação. _(Ex: docs: atualiza regras de contribuicao)_
- **`chore:`** Manutenção, organização de pastas ou arquivos ignorados. _(Ex: chore: organiza arquivos da pasta troubleshooting)_
- **`style:`** Define a aparência visual e a identidade estética da interface, controlando propriedades como cores, tipografia, espaçamentos, bordas e efeitos visuais. _(Ex: style: altera a cor de fundo primária do tema)_

---

## <a id="registrar-problema"></a>🚨 Como Registrar um Problema

Esta é a seção mais importante do repositório! Se você travou em um erro, resolveu e quer deixar registrado, crie um arquivo Markdown (`.md`) na pasta `/troubleshooting` ou adicione a um arquivo existente usando **exatamente** o formato abaixo:

### Template de Registro

**Eu acabei de ter um problema assim:**

> Descreva o problema de forma clara. Inclua a mensagem de erro do terminal, se houver.
> _Exemplo: Fui fazer um push, mas o repositório remoto tinha alterações que eu não tinha localmente. O terminal retornou `error: failed to push some refs`._

**E a solução foi esse comando:**

```bash
# Cole o comando exato aqui
git pull origin main --rebase
```

**Ele serve para tal coisa:**

> Explique de forma simples o que o comando faz nos bastidores.
> _Exemplo: Esse comando baixa as alterações do repositório remoto e aplica os meus commits locais "por cima" deles, criando uma linha do tempo limpa sem commits extras de merge._

---

## <a id="estrutura"></a>📂 Estrutura do Repositório

Organize seus arquivos da seguinte forma para facilitar a busca:

```text
├── .github/
│   └── PULL_REQUEST_TEMPLATE.md   # Template usado automaticamente nos PRs
├── /cheatsheets          # Guias rápidos de comandos (ex: git-basico.md, docker-basico.md)
├── /troubleshooting      # Registros de problemas e soluções (siga o template acima)
├── CONTRIBUTING.md       # Fluxo de contribuição, padrão de branches e commits
└── README.md             # Este arquivo
```

---

_Feito com ☕ e muito Git Reset pelos membros da equipe._
