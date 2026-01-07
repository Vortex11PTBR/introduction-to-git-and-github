# Adicionando e Commitando Alterações no Git

Após fazer modificações em seus arquivos, o Git oferece um processo de duas etapas para registrar essas alterações no histórico do repositório: **adicionar** (staging) e **commitar**.

## `git add` (Adicionando ao Staging Area)

O comando `git add` é usado para adicionar arquivos modificados ou novos ao *staging area* (também conhecida como índice). A *staging area* é uma área intermediária onde você prepara as alterações que deseja incluir no próximo commit.

- **Adicionar todos os arquivos modificados e novos no diretório atual:**
  ```bash
  git add .
  ```
  ou
  ```bash
  git add *
  ```

- **Adicionar um arquivo específico:**
  ```bash
  git add <nome_do_arquivo>
  ```

## `git commit` (Registrando as Alterações)

Depois que os arquivos são adicionados ao *staging area*, o comando `git commit` é usado para registrar essas alterações permanentemente no histórico do repositório. Cada commit representa um "instantâneo" do seu projeto em um determinado momento e deve vir acompanhado de uma mensagem descritiva.

- **Realizar um commit com uma mensagem:**
  ```bash
  git commit -m "Mensagem descritiva do commit"
  ```
  A mensagem do commit deve ser clara e concisa, explicando o que foi alterado e por quê.

## `git status` (Verificando o Status do Repositório)

O comando `git status` é essencial para acompanhar o estado do seu repositório. Ele mostra quais arquivos foram modificados, quais estão na *staging area* e quais ainda não foram rastreados pelo Git.

```bash
git status
```

Este comando é muito útil para verificar suas alterações antes de commitar e para garantir que você está adicionando os arquivos corretos.
