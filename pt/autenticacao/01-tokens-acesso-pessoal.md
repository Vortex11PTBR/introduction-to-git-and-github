# Tokens de Acesso Pessoal (Personal Access Tokens - PATs)

Os Personal Access Tokens (PATs) são uma alternativa segura para autenticação no GitHub/GitLab, especialmente quando a autenticação via SSH não é viável ou preferível. Eles funcionam como senhas, mas com escopo e validade definidos, oferecendo maior controle sobre as permissões.

## Quando usar PATs?

- Quando você precisa de acesso programático aos seus repositórios.
- Em ambientes onde a configuração SSH é complexa ou restrita.
- Para integrar ferramentas de terceiros que precisam interagir com seus repositórios.

## Como criar um PAT (GitHub)

1.  **Acesse as Configurações do Desenvolvedor**: No GitHub, vá para `Settings` > `Developer settings` > `Personal access tokens` > `Tokens (classic)`.
2.  **Gere um Novo Token**: Clique em `Generate new token`.
3.  **Defina o Escopo e Validade**: Escolha as permissões (escopos) que o token terá (ex: `repo` para acesso total a repositórios) e defina uma data de expiração.
4.  **Guarde o Token**: Após a criação, o token será exibido **apenas uma vez**. Copie-o e guarde-o em um local **seguro**, como um gerenciador de senhas. **Nunca compartilhe seu PAT publicamente.**

## Como usar um PAT

Ao realizar operações Git que exigem autenticação (como `git push` ou `git clone` via HTTPS), você será solicitado a fornecer seu nome de usuário e senha. Em vez da sua senha da conta, você usará o PAT.

```bash
Username for 'https://github.com': seu_usuario
Password for 'https://seu_usuario@github.com': seu_personal_access_token
```

**Importante**: Sempre defina um prazo de validade para seus PATs e revogue-os quando não forem mais necessários para minimizar riscos de segurança.
