## 1. Identificação  
**Código:** RNF01  
**Nome:** Desempenho e Tempo de Resposta do Sistema Embarcado

## 2. Descrição  
O sistema embarcado deve garantir que todas as operações, como a validação de coletas e a exibição do QR code, sejam realizadas rapidamente, sem impactar a experiência do usuário.

## 3. Justificativa  
Este requisito visa assegurar que o sistema embarcado funcione de maneira eficiente e sem atrasos, garantindo a fluidez no processo de coleta e validação, o que contribui para a satisfação do usuário.

## 4. Critérios de Aceitação  
- **CA01**: O tempo de resposta para a validação de uma coleta e o cálculo da pontuação não deve exceder **2 segundos**.  
- **CA02**: O tempo de resposta para exibição de QR code não deve exceder **1 segundo** após a detecção da presença de lixo no ponto de coleta.  
- **CA03**: O sistema deve ser capaz de detectar a presença de lixo e validar o QR code com uma taxa de sucesso de **99%**.

## 5. Observações Técnicas  
- O sistema embarcado deve ser otimizado para minimizar o uso de recursos de hardware e maximizar a velocidade de resposta.
- O sistema deve ser capaz de operar em tempo real, utilizando algoritmos eficientes e baixa latência.
