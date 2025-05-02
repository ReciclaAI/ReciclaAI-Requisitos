# Requisito Funcional 14: Esqueci a Senha

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Recuperar minha senha caso a tenha esquecido**  
PARA **Recuperar o acesso à minha conta e continuar utilizando o sistema.**

## 2. Pré-condições
- O usuário deve ter uma conta registrada no sistema.
- O usuário deve fornecer o e-mail associado à sua conta.

## 3. Fluxo Principal
1. O usuário envia uma requisição POST para o endpoint `/recuperar-senha` com o e-mail cadastrado.
2. O sistema valida se o e-mail está registrado no sistema.
3. O sistema envia um e-mail com um link para redefinir a senha.
4. O usuário clica no link recebido e é redirecionado para uma página para inserir uma nova senha.
5. O usuário envia a nova senha e o sistema a valida:
   - Verificação de que a senha atende aos requisitos de segurança.
6. O sistema atualiza a senha no banco de dados e confirma a alteração.

## 4. Fluxo Alternativo

### 4a. Se o e-mail não estiver registrado:
1. O sistema retorna uma mensagem informando que o e-mail não está cadastrado.

### 4b. Se a senha não atender aos requisitos de segurança:
1. O sistema retorna uma mensagem de erro informando que a senha não atende aos requisitos.
2. O usuário é solicitado a criar uma senha mais forte.

## 5. Pós-condições
- A senha do usuário foi alterada com sucesso e ele pode fazer login com a nova senha.

## 6. Regras de Negócio
- **RN01**: O sistema deve garantir que a nova senha atenda aos requisitos de segurança.
- **RN02**: O link de recuperação de senha deve expirar após 24 horas para evitar uso indevido.