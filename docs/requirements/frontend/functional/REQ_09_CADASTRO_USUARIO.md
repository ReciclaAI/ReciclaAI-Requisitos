# Requisito Funcional: Cadastro de Usuário 

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** cadastrar manualmente um novo usuário na plataforma administrativa  
**PARA** permitir que ele utilize o sistema, especialmente em casos de criação assistida de contas ou habilitação de usuários.

## 2. Pré-condições
- O administrador deve estar autenticado no sistema.
- O administrador deve ter permissão para gerenciar usuários.
- O e-mail do novo usuário não pode estar previamente cadastrado.

## 3. Fluxo Principal
1. O administrador acessa a seção “Usuários” > “Cadastrar Novo Usuário” no painel administrativo.
2. O sistema exibe um formulário com os seguintes campos:
   - Nome completo
   - E-mail
   - Senha inicial ou opção para envio de e-mail de criação de senha
   - (Opcional) Tipo de perfil: Usuário comum ou outro papel definido
3. O administrador preenche os dados e clica em “Cadastrar”.
4. O sistema realiza validações:
   - Verifica se o e-mail é único (**RN01**)
   - Verifica se a senha atende aos critérios de segurança (**RN02**)
5. O sistema envia uma requisição `POST` para o endpoint `/cadastro` com os dados informados.
6. Se bem-sucedido, o sistema exibe uma mensagem de sucesso: “Usuário cadastrado com sucesso.”
7. O novo usuário pode fazer login com suas credenciais ou redefinir a senha, se aplicável.

## 4. Fluxo Alternativo

### 4a. Se o e-mail já estiver em uso:
1. O sistema exibe uma mensagem de erro: “Este e-mail já está em uso.”
2. O administrador deve informar um e-mail diferente ou revisar os dados.

### 4b. Se a senha não atender aos critérios:
1. O sistema exibe uma mensagem de erro: “A senha deve conter ao menos 8 caracteres, incluindo letras e números.”
2. O formulário permanece ativo para correção.

## 5. Pós-condições
- O novo usuário foi registrado no sistema com as credenciais definidas.
- O usuário pode acessar a aplicação via login normalmente.

## 6. Regras de Negócio
- **RN01**: O e-mail do usuário deve ser único no sistema.
- **RN02**: A senha deve ter no mínimo 8 caracteres e conter letras e números.
- **RN03**: O administrador pode escolher se define uma senha ou aciona envio automático de link de cadastro.
