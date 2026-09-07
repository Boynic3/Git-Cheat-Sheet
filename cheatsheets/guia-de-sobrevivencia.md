# 🛠️ Comandos Básicos do Git

Um resumo rápido para o dia a dia.

### O Básico do Básico
- `git status`: Vê o que foi alterado.
- `git add .`: Adiciona todas as modificações para o próximo commit.
- `git commit -m "tipo: mensagem"`: Salva as alterações (lembre do nosso padrão!).
- `git push origin branch`: Envia para o GitHub.
- `git pull origin branch`: Puxa as atualizações do GitHub.

### Desfazendo besteiras
- `git restore <arquivo>`: Descarta as alterações locais de um arquivo que ainda não tomou `add`.
- `git reset HEAD~1`: Desfaz o último commit, mas mantém os arquivos alterados na sua máquina.

### 🔙 Desfazendo Besteiras (Avançado)
- `git reset --soft HEAD~1`: Reverte o último commit, mas **mantém** os arquivos alterados e prontos para um novo commit (no stage). Excelente para arrumar um erro de digitação na mensagem do commit.
- `git reset --hard HEAD`: 🚨 **PERIGO!** Descarta **tudo** o que não foi salvo e volta exatamente para como o código estava no último commit.
- `git restore .`: Descarta tudo o que não foi salvo, mas **mantém** o que já foi adicionado com `git add` (no stage).

# 💻 Comandos Gerais de Terminal
- `mkdir nomeDaPasta`: Cria uma nova pasta no diretório atual (ex: `mkdir projeto-novo`).