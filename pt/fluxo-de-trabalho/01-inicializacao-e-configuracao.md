# Inicialização e Configuração Básica do Git

Antes de começar a trabalhar com um repositório Git, é fundamental inicializá-lo e configurar suas informações de usuário.

## Inicializando um Repositório (`git init`)

Para transformar um diretório comum em um repositório Git, utilize o comando `git init`:

```bash
git init
```

Este comando cria uma subpasta oculta chamada `.git` dentro do seu diretório de trabalho. Esta pasta contém todos os metadados e o histórico do seu repositório. Para visualizar arquivos e pastas ocultas, você pode usar `ls -a` no Linux/macOS ou configurar seu explorador de arquivos no Windows.

## Configurando o Autor (`git config`)

É crucial configurar seu nome de usuário e e-mail para que seus commits sejam devidamente atribuídos. Essas informações são gravadas em cada commit que você faz.

### Configuração Global

Para configurar seu nome e e-mail globalmente (para todos os seus repositórios no sistema):

```bash
git config --global user.email "seu@email.com"
git config --global user.name "Seu Nome"
```

Substitua `"seu@email.com"` e `"Seu Nome"` pelas suas informações.

### Verificando as Configurações

Para listar todas as configurações do Git (globais e locais):

```bash
git config --list
```

### Alterando ou Removendo Configurações

Para alterar um e-mail já cadastrado:

```bash
git config --global user.email "novo@email.com"
```

Para remover uma configuração global (por exemplo, o e-mail):

```bash
git config --global --unset user.email
```

O mesmo princípio se aplica para `user.name` ou outras configurações. Lembre-se de usar o nome exato da configuração como aparece em `git config --list`.
