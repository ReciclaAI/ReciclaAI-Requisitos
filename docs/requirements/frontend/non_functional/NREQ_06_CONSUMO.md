## 1. Identificação  
**Código:** RNF06  
**Nome:** Consumo de Recursos  

## 2. Descrição  
O sistema deve ser otimizado para consumir recursos de hardware de forma eficiente, garantindo que o uso de CPU e memória seja mantido abaixo de **70%** durante o uso normal, sem afetar a performance do aplicativo.  

## 3. Justificativa  
Esse requisito visa garantir que o aplicativo seja eficiente e não sobrecarregue os dispositivos dos usuários, especialmente em dispositivos móveis com capacidade limitada, melhorando a experiência do usuário e evitando falhas.  

## 4. Critérios de Aceitação  
- **CA01**: O uso de CPU do sistema deve ser inferior a 70% em condições normais de operação.  
- **CA02**: O uso de memória RAM não deve ultrapassar 70% durante o uso contínuo do aplicativo.  
- **CA03**: O sistema deve ser testado em diferentes dispositivos para garantir a otimização do consumo de recursos.  

## 5. Observações Técnicas  
- A implementação de algoritmos eficientes e o uso de bibliotecas otimizadas para o dispositivo são essenciais.  
- Deve-se considerar o gerenciamento eficiente de tarefas em segundo plano para evitar sobrecarga de recursos.