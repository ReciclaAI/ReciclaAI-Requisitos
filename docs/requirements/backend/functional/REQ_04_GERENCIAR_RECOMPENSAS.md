# Requisito Funcional 4: Gerenciar Recompensas do Usuário

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Consultar as recompensas acumuladas com as coletas**  
PARA **Saber quantos pontos eu tenho e quais recompensas posso resgatar.**

## 2. Pré-condições
- O usuário deve estar autenticado no sistema.
- O sistema deve ter um banco de dados com as recompensas disponíveis e os pontos acumulados pelo usuário.

## 3. Fluxo Principal
1. O usuário envia uma requisição GET para o endpoint `/recompensas` para consultar suas recompensas acumuladas.
2. O sistema verifica a quantidade de pontos acumulados pelo usuário no banco de dados.
3. O sistema retorna a quantidade de pontos acumulados e a lista de recompensas disponíveis, incluindo:
    - Nome da recompensa.
    - Quantidade de pontos necessários para resgatar.
    - Descrição da recompensa.
4. O usuário escolhe uma recompensa e envia uma requisição POST para o endpoint `/resgatar-recompensa` com o ID da recompensa selecionada.
5. O sistema valida se o usuário tem pontos suficientes para o resgate:
    - Se o usuário tem pontos suficientes, o sistema deduz os pontos necessários e confirma o resgate.
    - O sistema registra o resgate da recompensa no banco de dados e retorna uma resposta de sucesso com os novos pontos do usuário.
6. O sistema atualiza os dados do usuário no banco de dados, incluindo os pontos restantes.

## 4. Fluxo Alternativo

### 4a. Se o usuário não tiver pontos suficientes:
1. O sistema retorna uma resposta de erro informando que o usuário não tem pontos suficientes para resgatar a recompensa.

## 5. Pós-condições
- O usuário resgatou uma recompensa e seus pontos foram atualizados no banco de dados.
- O resgate da recompensa foi registrado no sistema.

## 6. Regras de Negócio
- **RN01**: O usuário só pode resgatar recompensas se tiver pontos suficientes para o resgate.
- **RN02**: A quantidade de pontos necessária para resgatar cada recompensa deve ser definida no sistema e estar disponível na consulta.