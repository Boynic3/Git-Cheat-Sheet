# 🤝 Guia de Contribuição

Obrigado por contribuir com o **Git Cheat Sheet & Dev Diary**! Este documento reúne tudo o que você precisa saber para propor mudanças de forma organizada e consistente com o restante do projeto.

## 📑 Índice

1. [Antes de começar](#antes-de-começar)
2. [Fluxo de contribuição](#fluxo-de-contribuição)
3. [Padrão de nomenclatura de branches](#padrão-de-nomenclatura-de-branches)
4. [Padrão de commits](#padrão-de-commits)
5. [Abrindo um Pull Request](#abrindo-um-pull-request)
6. [Registrando um problema (Troubleshooting)](#registrando-um-problema-troubleshooting)
7. [Estrutura do repositório](#estrutura-do-repositório)

---

## Antes de começar

- Não faça commits diretos na branch `main`. Toda alteração deve passar por uma branch própria e um Pull Request.
- Verifique se o conteúdo que você quer adicionar já não existe em `/cheatsheets` ou `/troubleshooting` antes de criar um arquivo novo.
- Mantenha um tom claro e direto — o objetivo do repositório é economizar tempo de quem for ler depois.

---

## Fluxo de contribuição

1. **Atualize seu repositório local:**
   ```bash
   git pull origin main
   ```
2. **Crie uma branch** seguindo o [padrão de nomenclatura](#padrão-de-nomenclatura-de-branches):
   ```bash
   git checkout -b feat/minha-nova-dica
   ```
3. **Adicione seu conteúdo** seguindo os templates do repositório (cheatsheet novo, entrada de troubleshooting, etc.).
4. **Faça o commit** usando o [Padrão de Commits](#padrão-de-commits).
5. **Envie para o GitHub:**
   ```bash
   git push origin feat/minha-nova-dica
   ```
6. **Abra um Pull Request** usando o template disponível e peça a revisão de outro membro da equipe.

---

## Padrão de nomenclatura de branches

Toda branch deve seguir o formato:

```
<tipo>/<descricao-curta-em-kebab-case>
```

- **tipo**: o mesmo prefixo usado nos [commits](#padrão-de-commits), indicando a natureza da mudança.
- **descrição**: resumo curto, em minúsculas, sem acentos, com palavras separadas por hífen (`-`).
- Se a branch estiver associada a uma issue, o número pode ser incluído no final: `fix/23-corrige-link-quebrado`.

### Tipos de branch permitidos

| Prefixo      | Quando usar                                                        | Exemplo                              |
|--------------|---------------------------------------------------------------------|---------------------------------------|
| `feat/`      | Nova dica, tutorial, cheatsheet ou funcionalidade                   | `feat/adiciona-guia-docker`           |
| `fix/`       | Correção de comando errado, erro de digitação ou link quebrado      | `fix/corrige-flag-git-commit`         |
| `docs/`      | Alterações no README, CONTRIBUTING ou documentação em geral         | `docs/atualiza-regras-contribuicao`   |
| `chore/`     | Manutenção, organização de pastas ou arquivos de configuração       | `chore/organiza-pasta-troubleshooting`|
| `style/`     | Formatação e identidade visual (sem mudança de conteúdo/lógica)     | `style/ajusta-cores-tema`             |
| `refactor/`  | Reorganização de conteúdo existente sem mudar o significado         | `refactor/reestrutura-cheatsheet-git` |
| `test/`      | Adição ou ajuste de exemplos testáveis / scripts de validação       | `test/valida-links-readme`            |
| `perf/`      | Melhorias de performance em scripts ou automações do repositório    | `perf/otimiza-script-build`           |
| `build/`     | Mudanças em ferramentas de build, CI ou dependências                | `build/atualiza-workflow-actions`     |
| `revert/`    | Reversão de uma mudança anterior                                   | `revert/reverte-a215868`              |
| `hotfix/`    | Correção urgente aplicada diretamente sobre `main`                  | `hotfix/corrige-link-quebrado-prod`   |

> ⚠️ Evite branches genéricas como `nova-branch`, `teste` ou `wip`. O prefixo ajuda qualquer pessoa a entender o propósito só de olhar a lista de branches.

---

## Padrão de commits

Utilizamos **Conventional Commits** para manter o histórico legível:

```
<tipo>: <descrição curta em minúsculas e no imperativo>
```

Os tipos seguem a mesma tabela usada nas branches (`feat`, `fix`, `docs`, `chore`, `style`, `refactor`, `test`, `perf`, `build`, `revert`). O guia completo, com exemplos de commits simples e com corpo detalhado, está em [`cheatsheets/conventional-commits.md`](./cheatsheets/conventional-commits.md).

---

## Abrindo um Pull Request

- Use o template automático (`.github/PULL_REQUEST_TEMPLATE.md`) — ele é carregado sozinho ao abrir o PR.
- Descreva **o que mudou** e **por quê**, mesmo que seja uma alteração pequena.
- Relacione a branch/commit ao tipo de mudança correspondente.
- Peça revisão de pelo menos uma pessoa antes do merge.
- Prefira **squash merge** para manter o histórico da `main` limpo.
- Só marque o PR como pronto para revisão depois de conferir o checklist do template.

---

## Registrando um problema (Troubleshooting)

Esta é uma das seções mais importantes do repositório. Se você travou em um erro, resolveu e quer deixar registrado, crie um arquivo Markdown (`.md`) na pasta `/troubleshooting` ou adicione a um arquivo existente usando **exatamente** o formato abaixo.

### Template de Registro

```markdown
# Título curto do problema

**Eu acabei de ter um problema assim:**

> Descreva o problema de forma clara. Inclua a mensagem de erro do terminal, se houver.
> _Exemplo: Fui fazer um push, mas o repositório remoto tinha alterações que eu não tinha localmente. O terminal retornou `error: failed to push some refs`._

**E a solução foi esse comando:**

​```bash
# Cole o comando exato aqui
git pull origin main --rebase
​```

**Ele serve para tal coisa:**

> Explique de forma simples o que o comando faz nos bastidores.
> _Exemplo: Esse comando baixa as alterações do repositório remoto e aplica os meus commits locais "por cima" deles, criando uma linha do tempo limpa sem commits extras de merge._
```

Veja um exemplo real em [`troubleshooting/00-exemplo.md`](./troubleshooting/00-exemplo.md).

---

## Estrutura do repositório

```text
├── .github/
│   └── PULL_REQUEST_TEMPLATE.md   # Template usado automaticamente nos PRs
├── cheatsheets/                   # Guias rápidos de comandos (ex: guia-de-sobrevivencia.md)
├── troubleshooting/               # Registros de problemas e soluções (siga o template acima)
├── CONTRIBUTING.md                # Este arquivo
└── README.md                      # Apresentação geral do projeto
```

---

_Feito com ☕ e muito `git reset` pelos membros da equipe._
