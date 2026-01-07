# Configuração de Chave SSH para GitHub/GitLab

A autenticação via SSH oferece uma forma segura e conveniente de interagir com repositórios Git remotos, eliminando a necessidade de digitar sua senha repetidamente.

## O que é uma Chave SSH?

Uma **Chave SSH** é um par de chaves criptográficas (pública e privada) utilizado para autenticação segura. A chave pública é adicionada ao seu perfil no GitHub/GitLab, enquanto a chave privada permanece em seu computador, protegida por uma senha.

## Passos para Configurar uma Chave SSH

1.  **Gerar a Chave SSH**:
    Abra o terminal (Git Bash no Windows, terminal no Linux/macOS) e execute o comando:
    ```bash
    ssh-keygen -t ed25519 -C "seu@email.com"
    ```
    Substitua `seu@email.com` pelo seu endereço de e-mail. Siga as instruções, pressionando Enter para usar o local padrão e, opcionalmente, defina uma senha para sua chave privada.

2.  **Copiar a Chave Pública**:
    Após a geração, sua chave pública estará no arquivo `~/.ssh/id_ed25519.pub`. Copie seu conteúdo para a área de transferência:
    ```bash
    cat ~/.ssh/id_ed25519.pub
    ```

3.  **Adicionar a Chave Pública ao GitHub/GitLab**:
    - Acesse as configurações da sua conta no GitHub ou GitLab.
    - Navegue até a seção "SSH and GPG keys" (GitHub) ou "SSH Keys" (GitLab).
    - Clique em "New SSH Key" ou "Add SSH Key".
    - Cole o conteúdo da sua chave pública no campo fornecido e dê um título descritivo à chave.

4.  **Testar a Conexão SSH**:
    Para verificar se a conexão SSH está funcionando corretamente, execute:
    ```bash
    ssh -T git@github.com
    ```
    Você deverá ver uma mensagem de sucesso, indicando que a autenticação foi bem-sucedida.

## Agente SSH

Para evitar digitar a senha da sua chave privada a cada uso, você pode iniciar o agente SSH e adicionar sua chave a ele:

```bash
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_ed25519
```

Isso manterá sua chave privada carregada na memória durante a sessão, permitindo autenticação automática.

## Usando SSH com Git

Com a chave SSH configurada, você pode clonar repositórios usando o protocolo SSH:

```bash
git clone git@github.com:usuario/repositorio.git
```

**Referência**: Para mais detalhes, consulte a documentação oficial do GitHub: [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
