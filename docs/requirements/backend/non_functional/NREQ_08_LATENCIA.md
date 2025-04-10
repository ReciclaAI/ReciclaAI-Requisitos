## 1. Identificação  
**Código:** RNF08  
**Nome:** Latência da Comunicação com Ponto de Coleta  

## 2. Descrição  
A comunicação entre o aplicativo e os pontos de coleta deve ser realizada com uma latência inferior a **5 segundo**, para garantir a rapidez na validação das coletas.  

## 3. Justificativa  
Esse requisito é essencial para garantir que o sistema de validação de coleta seja rápido, sem atrasos, proporcionando uma experiência fluida para o usuário durante o processo de descarte dos resíduos.  

## 4. Critérios de Aceitação  
- **CA01**: A comunicação entre o aplicativo e o ponto de coleta deve ser realizada em menos de 5 segundo.  
- **CA02**: Caso a latência ultrapasse 5 segundo, o sistema deve registrar um erro e tentar uma nova comunicação automaticamente.  
- **CA03**: O tempo de resposta da comunicação deve ser monitorado em tempo real.

## 5. Observações Técnicas  
- O uso de tecnologias como MQTT ou WebSocket pode ser considerado para melhorar a latência da comunicação.  
- A infraestrutura dos pontos de coleta deve ser otimizada para garantir alta disponibilidade e baixa latência.