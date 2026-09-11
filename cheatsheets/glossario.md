# Glossário: Git, GitHub e Boas Práticas em Engenharia de Software

**Versão:** 1.0

## Introdução

Este documento consiste em um cheatsheet e glossário técnico focado nos conceitos, comandos, fluxos de trabalho e boas práticas essenciais para desenvolvimento de software, com ênfase no uso do Git, ecossistema GitHub e arquitetura/engenharia de software.

Seu propósito é servir como guia de referência rápida e padronizada para equipes e desenvolvedores, estruturado com abreviações, nomenclaturas formais, explicações conceituais, cenários práticos de aplicação e sistema de links internos para fácil navegação e integração em bases de conhecimento (Wikis, repositórios de documentação e portais de engenharia).

---

## 1. Git & Controle de Versão (Comandos e Conceitos)

| Termo / Abreviação | Nome Real | Descrição / Significado | Aplicação | Links |
| :--- | :--- | :--- | :--- | :--- |
| **commit** | Commit / Snapshot | Registro estático do estado dos arquivos rastreados em um determinado instante no histórico de alterações. | Salvar alterações locais estruturadas com uma mensagem explicativa e atômica. | <!-- [`[Git Core]`](./docs/git-core.md) \| [`[Mensagens de Commit]`](./docs/conventional-commits.md) --> |
| **branch** | Branch / Ramificação | Linha de desenvolvimento independente e ponteiro móvel para commits no repositório. | Criar novas funcionalidades, correções de bugs ou experimentos sem afetar a linha principal. | <!-- [`[Git Branching]`](./docs/git-branching.md) \| [`[Git Flow]`](./docs/git-workflows.md) --> |
| **merge** | Merge / Fusão | Combinação de histórico e estados de duas ou mais branches distintas em um único commit de fusão. | Integrar o código finalizado de uma branch de feature/fix na branch principal (`main`/`develop`). | <!-- [`[Merge vs Rebase]`](./docs/merge-vs-rebase.md) --> |
| **rebase** | Rebase / Re-baseamento | Reaplicação da sequência de commits de uma branch sobre a ponta de outra branch base, mantendo histórico linear. | Atualizar a branch de trabalho com as últimas alterações da branch principal limpando commits redundantes. | <!-- [`[Merge vs Rebase]`](./docs/merge-vs-rebase.md) --> |
| **stash** | Git Stash / Armazenamento Temporário | Área de armazenamento temporário para salvar modificações do diretório de trabalho sem necessidade de commit. | Salvar progresso não finalizado para alternar rapidamente de branch ou resolver uma urgência. | <!-- [`[Git Utilities]`](./docs/git-utilities.md) --> |
| **HEAD** | HEAD Pointer | Ponteiro de referência simbólica que indica a branch e o commit atualmente em uso no workspace. | Utilizado em operações de inspeção, navegação, checkout, reset e verificação de estados. | <!-- [`[Git Core]`](./docs/git-core.md) --> |

<!--
| **cherry-pick** | Cherry-Pick | Seleção e aplicação de commits específicos provenientes de uma branch em outra branch ativa. | Importar uma correção crítica de bug aplicada em outra branch sem realizar o merge completo. | <!-- [`[Git Utilities]`](./docs/git-utilities.md) |
-->

---

## 2. GitHub & Fluxos de Colaboração

| Termo / Abreviação | Nome Real | Descrição / Significado | Aplicação | Links |
| :--- | :--- | :--- | :--- | :--- |
| **PR** | Pull Request | Solicitação formal para integrar alterações propostas de uma branch remota para a base de código principal. | Iniciar revisão de código (*code review*), discussões, validação de regras de proteção e testes de CI. | <!-- [`[Pull Requests]`](./docs/pull-requests.md) \| [`[Code Review]`](./docs/code-review-guidelines.md) --> |
| **CR** | Code Review / Revisão de Código | Processo sistemático de análise técnica e qualitativa de código escrito por pares de desenvolvimento. | Garantir qualidade, detectar falhas precocemente, padronizar estilos e compartilhar conhecimento. | <!-- [`[Boas Práticas]`](./docs/best-practices.md) \| [`[Code Review]`](./docs/code-review-guidelines.md) --> |
| **issue** | Issue / Registro de Demanda | Item de rastreamento para registrar bugs, melhorias, tarefas técnicas ou discussões de projeto. | Gestão de tarefas, planejamento de sprints, rastreamento de defeitos e documentação de decisões. | <!-- [`[Gestão de Projetos]`](./docs/project-management.md) --> |
| **fork** | Fork / Cópia de Repositório | Cópia independente de um repositório remoto sob a propriedade de outra conta/organização. | Contribuições para projetos Open Source ou criação de derivações sem acesso direto de escrita. | <!-- [`[GitHub Workflow]`](./docs/github-workflow.md) --> |

<!--
| **LFS** | Git Large File Storage | Extensão que substitui arquivos grandes por ponteiros de texto dentro do repositório Git. | Gestão de ativos pesados (mídia, bancos de dados embutidos, artefatos de ML) sem sobrecarregar o histórico. | <!-- [`[Git Advanced]`](./docs/git-advanced.md) --> 


---

## 3. Boas Práticas, Padrões e Arquitetura

| Termo / Abreviação | Nome Real | Descrição / Significado | Aplicação | Links |
| :--- | :--- | :--- | :--- | :--- |
| **Conventional Commits** | Convenção de Mensagens de Commit | Especificação padronizada de mensagens de commit para legibilidade humana e automação por máquinas. | Estruturação de histórico (ex.: `feat: add oauth2 login`, `fix: resolve memory leak`), automação de changelogs. | <!-- [`[Mensagens de Commit]`](./docs/conventional-commits.md) \| [`[SemVer]`](./docs/semver-guide.md) --> |
| **CI/CD** | Continuous Integration / Continuous Deployment | Prática e conjunto de pipelines para automatizar build, testes e implantação contínua de aplicações. | Execução de suítes de testes automatizados e deploy em ambientes de staging/produção via GitHub Actions. | <!-- [`[DevOps]`](./docs/devops-ci-cd.md) \| [`[GitHub Actions]`](./docs/github-actions.md) --> |
| **API**| Application Programming Interface | Permite a comunicação entre sistemas, que um aplicativo solicite dados ou serviços de outro sistema. | Envio de código de verificação(SMS ou WhatsApp por exemplo), Botão de login como "Entrar com o Google" e "Entrar com o Facebook" | |
| **Endpoint** | Ponto de acesso / URL de Serviço | Um endereço de URL específico onde uma API recebe as requisições de um sistema para enviar ou buscar dados. | A URL ://site.com que o aplicativo celular acessa para puxar a lista de itens que aparecem na tela do usuário. | |
| **Deploy** | Distribuição / Implantação | Publicar o sistema em produção, basicamente "colocar no ar" a aplicação desenvolvida. | Disponibilizar uma versão preliminar para testes internos ou para o acesso real dos usuários| |
| **Escalability** | Escalabilidade | Capacidade de um sistema suportar um aumento crescente de carga de trabalho (usuários ou dados) sem perder desempenho. | Adaptar o site de uma loja para não cair durante os acessos massivos da Black Friday, ou aumentar servidores automaticamente quando um app viraliza. | |
| **Refactoring** | Refatoração | Melhorar a estrutura interna de um código para torná-lo mais limpo e eficiente, sem alterar o seu comportamento visual ou funcional. | Organizar um código confuso e repetitivo feito às pressas para que outros programadores consigam entendê-lo e modificá-lo mais facilmente no futuro. | |
| **Framework** | Estrutura / Modelo de trabalho | Conjunto de ferramentas, códigos e estruturas pré-moldadas que servem de base para guiar e acelerar o desenvolvimento de um software. | Usar o React ou Bootstrap para criar o visual de um site rapidamente, em vez de programar cada botão e animação do zero absoluto. | |
| **Stack** | Conjunto de tecnologias | O conjunto de tecnologias, linguagens de programação, bancos de dados e ferramentas utilizadas para construir e rodar um software. | Uma empresa que usa Python, Django e PostgreSQL para criar seu sistema web define essa combinação como a sua stack de desenvolvimento. | |


<!--
| **SemVer** | Semantic Versioning / Versionamento Semântico | Sistema de versionamento baseado no formato `MAJOR.MINOR.PATCH` segundo regras de compatibilidade. | Definição de lançamentos de software, APIs e controle de dependências em gerenciadores de pacotes. | <!-- [`[SemVer]`](./docs/semver-guide.md) |
| **DRY** | Don't Repeat Yourself | Princípio de design que busca reduzir a duplicação de conceitos e lógicas de código. | Modularização, abstração de funções genéricas e reutilização de componentes. | <!-- [`[Design Principles]`](./docs/design-principles.md) |
| **KISS** | Keep It Simple, Stupid | Princípio focado na simplicidade do design de sistemas, evitando complexidade desnecessária. | Prevenção de sobre-engenharia (*overengineering*), facilidade de manutenção e leitura de código. | <!-- [`[Design Principles]`](./docs/design-principles.md) |
| **SOLID** | Princípios SOLID | Cinco princípios de design de software orientado a objetos para criar código sustentável e testável. | Arquitetura de software, desacoplamento de componentes e extensibilidade de sistemas. | <!-- [`[Arquitetura de Software]`](./docs/software-architecture.md) |
-->
---


## Histórico de Versão

| Versão | Data | Autor / Contribuidor | Descrição das Alterações |
| :--- | :--- | :--- | :--- |
| **1.0** | 08/09/2026 | Pedrinho | Criação inicial do cheatsheet e glossário com seções de Git, GitHub, Boas Práticas e padrão de hyperlinks. |
| **1.01**| 11/09/2026| Moretti | Adiciona mais termos no Tópico 3 Boas Práticas, Padrões e Arquitetura
