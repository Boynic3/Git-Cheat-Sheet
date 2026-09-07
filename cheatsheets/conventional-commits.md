# 🏷️ Guia de Conventional Commits

O padrão *Conventional Commits* ajuda a manter o histórico do repositório limpo, rastreável e fácil de ler. 

## 📌 Prefixos e Exemplos Rápidos

- **`feat:`** (Nova funcionalidade)
  > `git commit -m "feat: implement tracking product service"`
- **`fix:`** (Correção de bugs)
  > `git commit -m "fix: remove getPayment() wrong attribute"`
- **`refactor:`** (Refatoração de código que não altera comportamento)
  > `git commit -m "refactor: change return log pattern"`
- **`style:`** (Formatação, espaços em branco, ponto e vírgula, etc)
  > `git commit -m "style: change function param for objects"`
  > `git commit -m "style: remove all blank spaces"`
- **`chore:`** (Manutenção, configurações, dependências ou tarefas invisíveis ao usuário)
  > `git commit -m "chore: add no-undef rule in eslintrc.json"`
- **`docs:`** (Atualização ou adição de documentação)
  > `git commit -m "docs: add technologies list in readme"`
- **`test:`** (Adição ou correção de testes automatizados)
  > `git commit -m "test: add test for create product automation"`
- **`perf:`** (Melhorias de performance)
  > `git commit -m "perf: change looping for parallel execution"`
- **`build:`** (Alterações no sistema de build ou bibliotecas externas)
  > `git commit -m "build: remove moment.js dependency"`
- **`revert:`** (Reverte um commit anterior)
  > `git commit -m "revert: back to a215868 commit"`

---

## 📝 Commits com Corpo (Mensagens Detalhadas)

Quando a alteração for muito grande, o título curto não é suficiente. Nesses casos, adicionamos um "corpo" ao commit para detalhar o que foi feito em tópicos.

No terminal, você pode fazer isso utilizando a flag `-m` múltiplas vezes (o primeiro `-m` é o título, o segundo `-m` é o corpo):

```bash
git commit -m "feat: adiciona menu inicial e refatora arquitetura de páginas" -m "- Cria novo index.html com interface minimalista servindo como hub do Algoritmica.
- Renomeia o antigo index.html para dijkstra.html.
- Implementa passagem de parâmetros de dificuldade (fácil/difícil) via URL.
- Unifica e organiza estilos no style.css para suportar múltiplas páginas."
```

*(Dica: Se preferir, você também pode digitar apenas `git commit` e dar `Enter`. Isso abrirá o editor de texto do seu terminal para você digitar o título, pular uma linha e escrever o corpo com mais calma).*