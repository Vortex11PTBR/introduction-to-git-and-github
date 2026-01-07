# Resolvendo Conflitos no Git

Conflitos de merge ocorrem quando duas ou mais pessoas modificam a mesma parte de um arquivo, ou quando um desenvolvedor exclui um arquivo que outro modificou. O Git não consegue decidir automaticamente qual alteração manter, exigindo intervenção manual.

## Cenário de Conflito

Imagine que você e um colega estão trabalhando no mesmo arquivo `receitas.md`. Você adiciona uma receita de bolo, e seu colega adiciona uma receita de pavê, ambos na mesma linha ou seção do arquivo.

1.  **Seu Colega Faz um Commit e Push**: Seu colega adiciona a receita de pavê, commita e envia para o repositório remoto (`git push origin master`).

2.  **Você Tenta Fazer Push**: Você termina sua receita de bolo, commita (`git commit -m "Adiciona receita de bolo"`) e tenta enviar (`git push origin master`). O Git rejeitará seu push, informando que o repositório remoto tem alterações que você não tem.

## Passos para Resolver um Conflito

1.  **Puxar as Alterações Remotas**: O primeiro passo é trazer as alterações do repositório remoto para o seu local:
    ```bash
    git pull origin master
    ```
    Neste momento, o Git identificará o conflito e marcará os arquivos afetados.

2.  **Identificar os Conflitos**: O Git modificará o arquivo `receitas.md` (no nosso exemplo) para mostrar as seções conflitantes. Ele usará marcadores especiais para indicar as suas alterações (`<<<<<<< HEAD`) e as alterações do seu colega (`>>>>>>> <hash_do_commit_do_colega>`):

    ```markdown
    <<<<<<< HEAD
    - Receita de Bolo
    =========
    - Receita de Pavê
    >>>>>>> hash_do_commit_do_colega
    ```

3.  **Resolver Manualmente**: Abra o arquivo conflitante em seu editor de código (VS Code, por exemplo). Você precisará editar o arquivo, removendo os marcadores de conflito (`<<<<<<<`, `=======`, `>>>>>>>`) e decidindo qual versão do código manter, ou combinando as duas versões de forma lógica.

    Por exemplo, para manter ambas as receitas:

    ```markdown
    - Receita de Bolo
    - Receita de Pavê
    ```

4.  **Marcar o Conflito como Resolvido**: Após editar o arquivo e remover todos os marcadores de conflito, você precisa informar ao Git que o conflito foi resolvido:
    ```bash
    git add receitas.md
    ```
    Você pode usar `git status` para verificar se o arquivo foi adicionado à *staging area*.

5.  **Committer a Resolução**: Finalmente, faça um novo commit para registrar a resolução do conflito:
    ```bash
    git commit -m "Resolve conflito em receitas.md: adiciona bolo e pave"
    ```

6.  **Enviar as Alterações Resolvidas**: Agora você pode enviar suas alterações, incluindo a resolução do conflito, para o repositório remoto:
    ```bash
    git push origin master
    ```

Resolver conflitos é uma parte comum do trabalho colaborativo com Git. A prática leva à perfeição!
