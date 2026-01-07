# Passando do Repositório Local para o Remoto

Após configurar seu repositório Git localmente e realizar seus primeiros commits, o próximo passo é conectá-lo a um repositório remoto (como o GitHub, GitLab ou Bitbucket) para backup, colaboração e compartilhamento.

## Criando um Repositório Remoto

1.  **Crie um novo repositório no GitHub/GitLab**: Acesse a plataforma de sua escolha e crie um novo repositório. **Não inicialize o repositório com um README, .gitignore ou licença** se você já tem um repositório local com conteúdo.
2.  **Copie a URL do Repositório**: Após a criação, a plataforma fornecerá uma URL para o seu novo repositório (geralmente HTTPS ou SSH). Copie esta URL.

## Conectando o Repositório Local ao Remoto

No seu terminal, dentro da pasta do seu projeto local, execute os seguintes comandos:

1.  **Adicionar o Repositório Remoto**: Este comando informa ao Git onde está o seu repositório remoto. `origin` é um nome padrão para o repositório remoto principal.
    ```bash
    git remote add origin <URL_DO_REPOSITORIO_REMOTO>
    ```
    Substitua `<URL_DO_REPOSITORIO_REMOTO>` pela URL que você copiou do GitHub/GitLab.

2.  **Enviar os Commits Locais para o Remoto**: Este comando "empurra" (push) seus commits do branch `master` (ou `main`) local para o branch `master` (ou `main`) do repositório remoto.
    ```bash
    git push -u origin master
    ```
    O flag `-u` (ou `--set-upstream`) configura o branch local para rastrear o branch remoto, facilitando futuros `git push` e `git pull`.

## Clonando um Repositório Remoto Existente

Se você deseja começar a trabalhar em um projeto que já existe em um repositório remoto, você pode cloná-lo diretamente:

```bash
git clone <URL_DO_REPOSITORIO_REMOTO>
```

Este comando baixará uma cópia completa do repositório para o seu computador, incluindo todo o histórico de commits, e configurará automaticamente a conexão com o repositório remoto.
