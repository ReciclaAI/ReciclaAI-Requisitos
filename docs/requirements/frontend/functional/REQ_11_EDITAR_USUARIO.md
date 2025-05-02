# Requisito Funcional: Editar Dados de Usuário 

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** editar as informações de um usuário cadastrado no sistema  
**PARA** manter os dados atualizados e corrigir inconsistências cadastrais quando necessário.

## 2. Pré-condições
- O administrador deve estar autenticado e ter permissão para gerenciar usuários.
- O usuário a ser editado deve estar previamente cadastrado no sistema.

## 3. Fluxo Principal
1. O administrador acessa a seção “Usuários” no painel administrativo.
2. O sistema exibe uma lista de usuários com opção de busca e filtros.
3. O administrador localiza e seleciona o usuário que deseja editar.
4. O sistema exibe um formulário com os dados atuais do usuário:
   - Nome
   - E-mail
   - (Opcional) Nova senha
5. O administrador atualiza os campos desejados e clica em “Salvar Alterações”.
6. O sistema realiza validações:
   - Verifica se o novo e-mail (caso alterado) é único no sistema (**RN01**)
   - Verifica se a nova senha (caso fornecida) atende aos critérios de segurança (**RN02**)
7. O sistema envia uma requisição `PUT` para o endpoint `/editar-usuario` com os dados modificados.
8. Se a operação for bem-sucedida, o sistema exibe uma mensagem de confirmação.

## 4. Fluxo Alternativo

### 4a. Se o e-mail informado já estiver em uso:
1. O sistema exibe uma mensagem: “Este e-mail já está cadastrado no sistema.”
2. O administrador deve inserir um e-mail diferente ou cancelar a alteração.

### 4b. Se a nova senha não atender aos critérios:
1. O sistema exibe a mensagem: “A senha deve conter no mínimo 8 caracteres, incluindo letras e números.”

## 5. Pós-condições
- As informações do usuário foram atualizadas corretamente no sistema.
- O administrador pode verificar as mudanças no perfil do usuário.

## 6. Regras de Negócio
- **RN01**: O e-mail fornecido deve ser único e não pode estar associado a outro usuário.
- **RN02**: A nova senha, se informada, deve ter no mínimo 8 caracteres e conter letras e números.
- **RN03**: Apenas administradores com permissão podem realizar edições cadastrais em contas de usuários.
