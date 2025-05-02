# Requisito Funcional 15: Editar Usuário

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Editar minhas informações pessoais no sistema**  
PARA **Manter meus dados atualizados, como nome, e-mail e senha.**

## 2. Pré-condições
- O usuário deve estar autenticado no sistema.
- O usuário deve fornecer dados válidos para atualização (nome, e-mail, senha).

## 3. Fluxo Principal
1. O usuário envia uma requisição PUT para o endpoint `/editar-usuario` com as informações que deseja atualizar:
   - Nome (opcional).
   - E-mail (opcional).
   - Senha (opcional).
2. O sistema valida os dados fornecidos:
   - Verificação de que o e-mail fornecido (se alterado) é único no sistema.
   - Verificação de que a senha atende aos requisitos de segurança (se alterada).
3. O sistema atualiza as informações do usuário no banco de dados.
4. O sistema retorna uma mensagem de sucesso confirmando que as informações foram atualizadas.

## 4. Fluxo Alternativo

### 4a. Se o e-mail fornecido já estiver em uso:
1. O sistema retorna uma mensagem de erro informando que o e-mail já está registrado.
2. O usuário é solicitado a fornecer outro e-mail.

### 4b. Se a senha fornecida não atender aos requisitos de segurança:
1. O sistema retorna uma mensagem de erro informando que a senha não atende aos requisitos.
2. O usuário é solicitado a criar uma senha mais forte.

## 5. Pós-condições
- As informações do usuário foram atualizadas no sistema.

## 6. Regras de Negócio
- **RN01**: O e-mail fornecido deve ser único no sistema.
- **RN02**: A senha deve ser segura, com um mínimo de 8 caracteres, contendo letras e números.