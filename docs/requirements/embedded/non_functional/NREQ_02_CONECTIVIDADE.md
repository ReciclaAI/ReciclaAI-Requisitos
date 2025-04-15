## 1. Identificação  
**Código:** RNF02  
**Nome:** Conectividade e Comunicação com o Backend

## 2. Descrição  
O sistema embarcado deve ser capaz de se comunicar com o backend para enviar dados de coletas e receber comandos sem interrupções, garantindo a integração contínua com a plataforma.

## 3. Justificativa  
Este requisito é essencial para garantir que os dados sejam registrados corretamente no backend em tempo real, evitando falhas ou dados inconsistentes e permitindo que o processo de validação seja realizado adequadamente.

## 4. Critérios de Aceitação  
- **CA01**: O sistema deve enviar os dados de coleta ao backend em tempo real, com um tempo de latência inferior a **3 segundos**.  
- **CA02**: O sistema deve garantir uma comunicação estável e sem falhas, com uma taxa de reconexão automática de **95%** quando a conexão com a internet for perdida.

## 5. Observações Técnicas  
- O sistema embarcado deve utilizar protocolos de comunicação em tempo real, como **MQTT** ou **WebSockets**, para garantir baixa latência e alta disponibilidade.
- A infraestrutura de rede do sistema deve ser robusta e redundante para evitar falhas de comunicação.
