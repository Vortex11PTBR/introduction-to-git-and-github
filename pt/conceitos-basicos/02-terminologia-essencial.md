# Terminologia Essencial do Git

Para entender o funcionamento do Git, é fundamental conhecer alguns termos chave:

## SHA-1 (Secure Hash Algorithm 1)

O SHA-1 é um **algoritmo de criptografia** que gera um *hash* de 40 dígitos. No Git, ele é usado para identificar de forma única cada objeto (arquivos, diretórios, commits). Qualquer alteração, por menor que seja, no conteúdo de um arquivo resultará em um SHA-1 completamente diferente, garantindo a integridade e rastreabilidade dos dados.

## Blob (Binary Large Object)

Um **Blob** representa o conteúdo de um arquivo individual armazenado no Git. Ele guarda o conteúdo bruto do arquivo, sem metadados como nome ou permissões. Cada vez que um arquivo é modificado e salvo, um novo blob é criado.

## Tree (Árvore)

Um **Tree** é um objeto que funciona como um diretório. Ele lista blobs (arquivos) e outros trees (subdiretórios), formando a estrutura hierárquica do repositório. Um tree aponta para os blobs e trees que ele contém, juntamente com seus nomes e permissões.

## Commit

Um **Commit** é um "instantâneo" (snapshot) do repositório em um determinado momento. Ele aponta para um objeto tree raiz que representa o estado completo do projeto naquele commit. Além disso, um commit contém metadados importantes como:

- **Mensagem**: Uma descrição do que foi alterado.
- **Autor**: Quem fez a alteração.
- **Data**: Quando a alteração foi feita.
- **Pai (Parent)**: Referência ao commit anterior, formando o histórico do projeto.

Esses elementos são a base para o controle de versão no Git, permitindo que o histórico do projeto seja mantido de forma eficiente e segura.
