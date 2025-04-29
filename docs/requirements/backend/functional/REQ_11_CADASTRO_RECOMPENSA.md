# Requisito Funcional 11: Cadastrar Recompensas por Pontos

## 1. Descrição do Caso de Uso
COMO **Administrador**  
QUERO **Cadastrar novas recompensas no sistema associadas a um número de pontos específicos**  
PARA **Oferecer incentivos aos usuários e motivá-los a realizar mais coletas.**

## 2. Pré-condições
- O administrador deve estar autenticado no sistema.
- O administrador deve ter permissões adequadas para gerenciar recompensas no sistema.

## 3. Fluxo Principal
1. O administrador envia uma requisição GET para o endpoint `/recompensas` para visualizar a lista de recompensas cadastradas no sistema.
2. O sistema retorna a lista de recompensas disponíveis.
3. O administrador envia uma requisição POST para o endpoint `/recompensas` com os seguintes dados da nova recompensa:
    - Nome da recompensa.
    - Descrição da recompensa.
    - Número de pontos necessários para resgatar a recompensa.
    - Imagem ou ícone da recompensa (opcional).
    - Limite de resgates por usuário (opcional).
4. O sistema valida os dados recebidos:
    - Verificação de que o número de pontos é um valor válido e positivo (RN01).
    - Verificação de que a descrição não está vazia (RN02).
    - Verificação de que o nome da recompensa é único no sistema (RN03).
5. Se os dados forem válidos, o sistema registra a nova recompensa no banco de dados.
6. O sistema retorna uma resposta de sucesso confirmando o cadastro da nova recompensa.

## 4. Fluxo Alternativo

### 4a. Se o número de pontos inserido não for válido ou estiver em formato incorreto:
1. O sistema retorna uma resposta de erro informando que o número de pontos deve ser um valor válido e positivo.
2. O sistema não prossegue com o cadastro até que o valor seja corrigido.

### 4b. Se a descrição estiver vazia:
1. O sistema retorna uma resposta de erro informando que a descrição da recompensa não pode estar vazia.

## 5. Pós-condições
- A nova recompensa foi cadastrada no banco de dados e está disponível para resgate pelos usuários, caso atinjam o número de pontos necessários.

## 6. Regras de Negócio
- **RN01**: O número de pontos necessários para resgatar a recompensa deve ser um valor positivo e válido.
- **RN02**: O nome da recompensa deve ser único no sistema para evitar duplicação de recompensas.
- **RN03**: A recompensa só pode ser resgatada após o usuário atingir a quantidade mínima de pontos definida.