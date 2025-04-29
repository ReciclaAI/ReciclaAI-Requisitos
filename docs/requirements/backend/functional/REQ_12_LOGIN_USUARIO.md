# Requisito Funcional 12: Login de Usuário

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Fazer login no sistema**  
PARA **Acessar minha conta e realizar ações relacionadas ao meu perfil e coletas realizadas.**

## 2. Pré-condições
- O usuário deve ter uma conta cadastrada no sistema.
- O usuário deve fornecer credenciais válidas (usuário e senha).

## 3. Fluxo Principal
1. O usuário envia uma requisição POST para o endpoint `/login` com seu nome de usuário e senha.
2. O sistema valida as credenciais fornecidas:
   - Verificação se o nome de usuário existe.
   - Verificação se a senha está correta.
3. Se as credenciais forem válidas, o sistema gera um token de autenticação (JWT) e o retorna ao usuário.
4. O sistema permite que o usuário acesse as funcionalidades do sistema, como consultar pontos de coleta, registrar coletas, visualizar recompensas, etc.

## 4. Fluxo Alternativo

### 4a. Se as credenciais forem inválidas:
1. O sistema retorna uma mensagem de erro informando que o nome de usuário ou senha estão incorretos.
2. O usuário é solicitado a tentar novamente.

## 5. Pós-condições
- O usuário foi autenticado com sucesso e tem acesso ao sistema.

## 6. Regras de Negócio
- **RN01**: O sistema deve garantir que as credenciais fornecidas sejam validadas corretamente.
- **RN02**: O token de autenticação deve ser gerado de forma segura e ter um tempo de expiração definido.