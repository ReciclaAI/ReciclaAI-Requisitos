### Requisito Funcional 2: Registro do Peso do Lixo Descartado

**1. Descrição do Caso de Uso**  
**COMO** Sistema Embarcado (Ponto de Coleta)  
**QUERO** Registrar o peso do lixo descartado  
**PARA** Calcular a pontuação do usuário com base na quantidade de lixo descartado.

**2. Pré-condições**  
- O sistema embarcado deve estar equipado com sensores de peso (por exemplo, sensores de carga ou balanças).
- O usuário deve ter completado a coleta no ponto de coleta.

**3. Fluxo Principal**  
1. O usuário deposita o lixo no ponto de coleta.
2. O sistema embarcado detecta o peso do lixo descartado através dos sensores.
3. O sistema registra o peso e o associa à coleta realizada.
4. O sistema envia os dados de peso para o backend para cálculo da pontuação do usuário.

**4. Fluxo Alternativo**  
4a. Se o sensor de peso não detectar o lixo:
   1. O sistema exibe uma mensagem de erro informando que o peso não foi detectado corretamente e solicita que o usuário tente novamente.

**5. Pós-condições**  
- O peso do lixo foi registrado corretamente e associado à coleta.
- O sistema enviou os dados de peso para o backend para o cálculo de pontos.

**6. Regras de Negócio**  
- **RN01** - O peso registrado deve ser preciso e de acordo com a capacidade do sensor.
- **RN02** - O sistema deve ser capaz de registrar e transmitir dados em tempo real para garantir que o cálculo da pontuação seja imediato.
