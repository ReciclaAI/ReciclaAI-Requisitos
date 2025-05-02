# Caso de Uso: Cadastro de Ponto de Coleta

## 1. Descrição do Caso de Uso
COMO **Administrador**  
QUERO **Cadastrar um novo ponto de coleta no sistema**  
PARA **Gerenciar e monitorar os pontos de coleta de resíduos recicláveis.**

## 2. Pré-condições
- O administrador deve estar autenticado no sistema.
- O administrador deve ter permissões para gerenciar pontos de coleta.

## 3. Fluxo Principal
1. O administrador envia uma requisição POST para o endpoint `/pontos-de-coleta` com os dados do novo ponto de coleta.
2. O sistema valida os dados recebidos:
    - Verificação de que o nome do ponto de coleta é único (RN01).
    - Verificação de que o endereço está no formato correto (RN02).
    - Verificação de que a capacidade de armazenamento é um valor numérico positivo (RN03).
3. Se os dados forem válidos, o sistema registra o novo ponto de coleta no banco de dados.
4. O sistema retorna uma resposta de sucesso com os detalhes do ponto de coleta cadastrado, incluindo:
    - Nome do ponto de coleta.
    - Endereço completo.
    - Tipo de resíduos aceitos.
    - Capacidade máxima de armazenamento.
    - Horário de funcionamento.
    - Método de verificação.
5. O administrador pode consultar a lista de pontos de coleta cadastrados via requisição GET no endpoint `/pontos-de-coleta`.

## 4. Fluxo Alternativo

### 4a. Se os dados estiverem incorretos ou incompletos:
1. O sistema retorna uma resposta de erro indicando quais campos precisam ser corrigidos.
2. O sistema não prossegue com o cadastro até que todos os campos obrigatórios sejam corrigidos e preenchidos corretamente.

## 5. Pós-condições
- O novo ponto de coleta está registrado no banco de dados do sistema.
- As informações do ponto de coleta são armazenadas e podem ser consultadas via API.

## 6. Regras de Negócio
- **RN01**: O nome do ponto de coleta deve ser único no sistema.
- **RN02**: O endereço deve ser válido e bem formatado.
- **RN03**: A capacidade de armazenamento deve ser um valor numérico positivo.