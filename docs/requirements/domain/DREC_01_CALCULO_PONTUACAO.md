### Requisito de Domínio: Cálculo de Pontuação por kg de Lixo

**1. Descrição**  
**COMO** Sistema de Coleta  
**QUERO** Calcular a pontuação do usuário com base na quantidade de lixo descartado (em kg)  
**PARA** Oferecer recompensas proporcionais à quantidade de resíduos recicláveis coletados e incentivar a participação ativa na reciclagem.

**2. Regras de Negócio**  
- **RN01** - A pontuação será atribuída com base na quantidade de lixo descartado, considerando 1 ponto para cada 200 gramas de lixo descartado.  
- **RN02** - O cálculo da pontuação será feito da seguinte forma:
  - **Pontuação = Peso do lixo (kg) / 0,2 (200 gramas)**  
  - Exemplo: Para 1 kg de lixo, a pontuação será **1 kg / 0,2 = 5 pontos**.
  
- **RN03** - O sistema deve realizar o cálculo automaticamente, sem distinção do tipo de resíduo, considerando apenas o peso total do lixo descartado.
  
- **RN04** - O sistema deve registrar o peso do lixo descartado, em gramas ou quilos, e calcular a pontuação correspondente de forma precisa.

**3. Exemplo de Cálculo**  
- Se o usuário descartar 1 kg de lixo (1000 gramas), a pontuação será:
  **Pontuação = 1000 gramas / 200 gramas = 5 pontos.**

- Se o usuário descartar 500 gramas de lixo, a pontuação será:
  **Pontuação = 500 gramas / 200 gramas = 2,5 pontos.** (Neste caso, o sistema deve arredondar para o ponto mais próximo, se necessário, ou fazer o arredondamento para baixo.)

**4. Considerações Técnicas**  
- O sistema deve garantir que o peso do lixo seja registrado corretamente para que o cálculo da pontuação seja feito de forma precisa.
- O sistema deve calcular a pontuação automaticamente com base no peso do lixo registrado na coleta, sem a necessidade de intervenção manual.

**5. Requisitos Não Funcionais**  
- O cálculo da pontuação deve ser realizado em tempo real, sem impactar o desempenho do sistema.
- O sistema deve garantir que o cálculo da pontuação seja consistente em todos os dispositivos e plataformas do sistema, refletindo qualquer coleta nova ou ajustes no cálculo.

