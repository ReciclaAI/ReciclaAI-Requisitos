# Requisito Funcional 8: Notificação de Nova Recompensa Disponível

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Receber uma notificação quando uma nova recompensa estiver disponível para resgatar**  
PARA **Ser notificado sobre as novas oportunidades de recompensas com base nos meus pontos acumulados.**

## 2. Pré-condições
- O usuário deve estar autenticado no sistema.
- O usuário deve ter acumulado pontos suficientes para resgatar recompensas.

## 3. Fluxo Principal
1. O sistema monitora os pontos acumulados pelo usuário no banco de dados.
2. Quando o usuário atinge a quantidade mínima de pontos necessária para resgatar uma recompensa disponível, o sistema verifica se há uma recompensa correspondente.
3. O sistema envia uma notificação para o dispositivo móvel do usuário, utilizando um serviço de notificações (por exemplo, Firebase Cloud Messaging ou Push Notifications).
4. A notificação inclui os seguintes detalhes:
    - A recompensa disponível.
    - A quantidade de pontos necessários para resgatar a recompensa.
    - Instruções para o resgate da recompensa.
5. O sistema retorna uma confirmação do envio da notificação.

## 4. Fluxo Alternativo

### 4a. Se o usuário não tiver pontos suficientes para a recompensa:
1. O sistema não envia a notificação de recompensa, pois o usuário não tem pontos suficientes para resgatar a recompensa.

## 5. Pós-condições
- O usuário é notificado sobre a recompensa disponível quando atingir o número necessário de pontos.

## 6. Regras de Negócio
- **RN01**: A notificação de recompensa deve ser enviada apenas quando o usuário atingir a quantidade mínima de pontos para resgatar a recompensa.
- **RN02**: A notificação deve incluir informações claras sobre os requisitos para resgatar a recompensa, como o nome da recompensa e a quantidade de pontos necessários.