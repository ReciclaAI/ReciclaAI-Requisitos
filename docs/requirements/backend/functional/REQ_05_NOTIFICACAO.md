# Requisito Funcional 5: Exibir Notificação de Coleta Realizada

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Receber uma notificação após validar minha coleta no ponto de coleta**  
PARA **Saber que minha coleta foi registrada corretamente e que ganhei pontos.**

## 2. Pré-condições
- O usuário deve estar autenticado no sistema.
- O usuário deve ter completado a coleta e validado o QR code.

## 3. Fluxo Principal
1. O sistema recebe uma requisição POST para o endpoint `/validar-coleta` e confirma que o usuário completou a coleta e validou o QR code.
2. O sistema valida os dados da coleta e, se o QR code for válido, registra a coleta e os pontos ganhos no banco de dados.
3. O sistema envia uma notificação para o dispositivo móvel do usuário usando o serviço de notificações (por exemplo, Firebase Cloud Messaging ou Push Notifications), informando o sucesso da coleta.
4. A notificação inclui:
    - A quantidade de pontos ganhos.
    - A confirmação de que a coleta foi registrada corretamente.
5. O sistema retorna uma resposta de sucesso para o backend confirmando a notificação enviada.

## 4. Fluxo Alternativo

### 4a. Se houver um erro na validação:
1. O sistema retorna uma resposta de erro e envia uma notificação ao usuário informando que houve um erro na validação da coleta.
2. A notificação orienta o usuário a tentar novamente a validação da coleta.

## 5. Pós-condições
- O usuário recebeu a notificação de coleta realizada com sucesso.
- A coleta foi registrada no banco de dados e os pontos do usuário foram atualizados.

## 6. Regras de Negócio
- **RN01**: A notificação deve ser enviada em tempo real após a validação da coleta e atualização dos pontos.
- **RN02**: A notificação deve incluir detalhes relevantes, como a quantidade de pontos ganhos e a confirmação da coleta registrada.