# Comandos Essenciais do Git

Esta seção apresenta os comandos Git mais utilizados, com seus equivalentes para sistemas operacionais Windows e Linux, facilitando a transição e o uso em diferentes ambientes.

## Comandos de Navegação e Manipulação de Arquivos

| Descrição             | Windows (W)             | Linux (L)                   |
| :-------------------- | :---------------------- | :-------------------------- |
| Listar diretórios     | `dir`                   | `ls`                        |
| Mudar diretório       | `cd`                    | `cd`                        |
| Limpar tela           | `cls`                   | `clear` ou `Ctrl + L`       |
| Criar diretório       | `mkdir`                 | `mkdir`                     |
| Criar arquivo com texto | `echo hello > hello.txt`| `echo hello > hello.txt`    |
| Deletar arquivos      | `del <arquivo>`         | `rm <arquivo>`              |
| Remover diretório     | `rmdir <diretorio> /S /Q`| `rm -rf <diretorio>`        |

## Comandos Git

| Comando Git                     | Descrição                                                                 |
| :------------------------------ | :------------------------------------------------------------------------ |
| `git init`                      | Inicializa um novo repositório Git na pasta atual. Cria a pasta `.git` oculta. |
| `git config --global user.email "seu@email.com"` | Configura o e-mail do autor para todos os repositórios locais.          |
| `git config --global user.name "Seu Nome"`     | Configura o nome do autor para todos os repositórios locais.            |
| `git add .` ou `git add <arquivo>` | Adiciona arquivos ao *staging area* (área de preparação) para o próximo commit. |
| `git commit -m "Mensagem do commit"` | Registra as alterações do *staging area* no histórico do repositório com uma mensagem descritiva. |
| `git status`                    | Mostra o status do repositório: arquivos modificados, adicionados, etc.   |
| `git remote add origin <URL>`   | Adiciona um repositório remoto (geralmente no GitHub) ao seu repositório local. |
| `git push origin master`        | Envia os commits do seu repositório local para o branch `master` do repositório remoto. |
| `git pull origin master`        | Baixa as alterações do branch `master` do repositório remoto para o seu repositório local. |
| `git config --list`             | Lista todas as configurações do Git.                                      |
| `git config --global --unset user.email` | Remove o e-mail do autor configurado globalmente.                         |

**Observação**: Para comandos administrativos no Linux, pode ser necessário usar `sudo su` para obter privilégios de superusuário.
