# Requisito Funcional 13: Cadastro de Usuário

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Cadastrar uma nova conta no sistema**  
PARA **Utilizar as funcionalidades do sistema e começar a registrar minhas coletas.**

## 2. Pré-condições
- O usuário deve fornecer as informações necessárias para o cadastro (nome, e-mail, senha).
- O e-mail fornecido deve ser único no sistema.

## 3. Fluxo Principal
1. O usuário envia uma requisição POST para o endpoint `/cadastro` com as informações necessárias:
   - Nome.
   - E-mail.
   - Senha.
2. O sistema valida os dados fornecidos:
   - Verificação de que o e-mail não está em uso.
   - Verificação de que a senha atende aos requisitos de segurança.
3. O sistema cria uma nova conta de usuário e armazena as informações no banco de dados.
4. O sistema retorna uma mensagem de sucesso e permite que o usuário faça login com a conta recém-criada.

## 4. Fluxo Alternativo

### 4a. Se o e-mail já estiver em uso:
1. O sistema retorna uma mensagem de erro informando que o e-mail já foi cadastrado.
2. O usuário é solicitado a fornecer outro e-mail.

### 4b. Se a senha não atender aos requisitos de segurança:
1. O sistema retorna uma mensagem de erro informando que a senha não atende aos requisitos.
2. O usuário é solicitado a criar uma senha mais forte.

## 5. Pós-condições
- O usuário foi registrado no sistema e pode fazer login para acessar as funcionalidades.

## 6. Regras de Negócio
- **RN01**: O e-mail fornecido deve ser único no sistema.
- **RN02**: A senha deve ser segura, com um mínimo de 8 caracteres, contendo letras e números.