# 🌱 Git Básico: O que é, Instalação e Configuração

> _"Git, é o início de tudo."_
> — inspirado em "Última Vez", do Alee.
>
> Antes do primeiro commit, antes do primeiro repositório, antes de qualquer linha de código versionada, existe só isso: o começo.

Um resumo rápido pra quem tá começando ou vai configurar uma máquina nova.

---

## 🤔 O que é o Git?

Git é um **sistema de controle de versão distribuído**. Na prática, ele:

- Guarda um "histórico de fotografias" (commits) do seu projeto ao longo do tempo, então dá pra voltar em qualquer ponto sem perder nada.
- É **distribuído**: cada pessoa tem uma cópia completa do histórico na própria máquina, não só no servidor (diferente de sistemas antigos tipo SVN).
- Roda **local**, sem precisar de internet pra maioria dos comandos (`add`, `commit`, `log`, `diff`...). Só precisa de rede pra sincronizar com um remoto (`push`, `pull`, `fetch`).
- Não é a mesma coisa que **GitHub** — o Git é a ferramenta, o GitHub é só um serviço na nuvem que hospeda repositórios Git (existem outros, como GitLab e Bitbucket).

---

## 📥 Instalação

### Windows

1. Baixe o instalador em [git-scm.com/download/win](https://git-scm.com/download/win).
2. Rode o instalador e siga o padrão (dá pra manter as opções default na maioria das telas).
3. Isso instala também o **Git Bash**, um terminal com os comandos Unix mais usados.

Se preferir via gerenciador de pacotes:
```bash
winget install --id Git.Git -e --source winget
```

### macOS

Opção mais simples, via [Homebrew](https://brew.sh/):
```bash
brew install git
```

Ou instalando as Ferramentas de Linha de Comando da Apple (já vem com o Git):
```bash
xcode-select --install
```

### Linux

**Debian/Ubuntu:**
```bash
sudo apt update
sudo apt install git
```

**Fedora/RHEL:**
```bash
sudo dnf install git
```

**Arch:**
```bash
sudo pacman -S git
```

### ✅ Conferindo se instalou

```bash
git --version
```

Deve retornar algo como `git version 2.4x.x`.

---

## ⚙️ Configurações essenciais

Antes do primeiro commit, configure **quem você é** — essa informação vai junto em todo commit que você fizer.

```bash
git config --global user.name "FarmadorDeAura"
git config --global user.email "farmadordeaura@email.com"
```

> 💡 `--global` aplica a config pra todos os repositórios da sua máquina. Se quiser um nome/e-mail diferente só num projeto específico, rode o mesmo comando **sem** `--global` dentro da pasta do projeto.

### Outras configs úteis

- **Branch padrão como `main`** (evita cair em `master` por padrão):
  ```bash
  git config --global init.defaultBranch main
  ```

- **Editor de texto padrão** (usado em mensagens de commit sem `-m`, rebases interativos, etc.):
  ```bash
  git config --global core.editor "code --wait"   # VS Code
  # ou
  git config --global core.editor "vim"            # Vim
  ```

- **Guardar credenciais** (evita digitar usuário/senha ou token toda hora):
  ```bash
  git config --global credential.helper cache   # guarda por um tempo em memória
  # ou
  git config --global credential.helper store   # guarda em disco (menos seguro)
  ```

- **Cores no terminal** (facilita ler `status`, `diff`, `log`):
  ```bash
  git config --global color.ui auto
  ```

### Conferindo suas configurações

```bash
git config --list          # mostra tudo que foi configurado
git config user.name        # mostra só um valor específico
```

Isso também abre e edita o arquivo de config diretamente:
```bash
git config --global --edit
```

---

## 🚀 Próximo passo

Depois de instalado e configurado, o dia a dia de comandos (status, add, commit, push, pull, reset...) está no [`guia-de-sobrevivencia.md`](./guia-de-sobrevivencia.md).
