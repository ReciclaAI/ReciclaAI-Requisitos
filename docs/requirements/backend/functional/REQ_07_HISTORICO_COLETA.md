# Requisito Funcional 7: Histórico de Coletas do Usuário

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Visualizar o histórico das minhas coletas realizadas**  
PARA **Acompanhar as coletas que fiz e verificar meus pontos acumulados.**

## 2. Pré-condições
- O usuário deve estar autenticado no sistema.
- O usuário deve ter realizado coletas previamente.

## 3. Fluxo Principal
1. O usuário envia uma requisição GET para o endpoint `/historico-coletas` com seu identificador de usuário.
2. O sistema consulta o banco de dados para buscar o histórico de coletas do usuário, retornando uma lista com as seguintes informações:
    - Data da coleta.
    - Ponto de coleta.
    - Tipo de resíduos descartados.
    - Pontos acumulados.
3. O sistema retorna uma resposta com o histórico das coletas realizadas.
4. O usuário pode clicar em um item da lista para visualizar detalhes adicionais da coleta, como:
    - Quantidade de resíduos descartados.
    - Recompensas associadas, se houver.

## 4. Fluxo Alternativo

### 4a. Se o usuário não tiver realizado coletas:
1. O sistema retorna uma resposta informando que o histórico de coletas está vazio.

## 5. Pós-condições
- O usuário visualizou seu histórico de coletas realizadas, com detalhes sobre as coletas e pontos acumulados.

## 6. Regras de Negócio
- **RN01**: O histórico de coletas deve ser carregado de forma eficiente e em tempo real, garantindo que o usuário veja as coletas mais recentes.
- **RN02**: O sistema deve garantir que o histórico seja atualizado automaticamente com as coletas mais recentes à medida que forem realizadas.