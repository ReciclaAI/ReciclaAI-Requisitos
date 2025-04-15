### Requisito Funcional 6: Detecção de Lixo no Ponto de Coleta

**1. Descrição do Caso de Uso**  
**COMO** Sistema Embarcado (Ponto de Coleta)  
**QUERO** Detectar a presença de lixo no ponto de coleta  
**PARA** Validar que o usuário está realizando o descarte corretamente.

**2. Pré-condições**  
- O sistema embarcado deve ter sensores de proximidade ou sensores de presença instalados no ponto de coleta.
- O usuário deve realizar o descarte de resíduos.

**3. Fluxo Principal**  
1. O sistema embarcado monitora a presença de lixo no ponto de coleta.
2. Quando o lixo é detectado, o sistema ativa o processo de validação da coleta, solicitando ao usuário que escaneie o QR code.
3. O sistema registra a coleta e envia os dados ao backend, incluindo a detecção de lixo.

**4. Fluxo Alternativo**  
4a. Se o lixo não for detectado:
   1. O sistema exibe uma mensagem informando que não foi detectado lixo e solicita que o usuário insira o lixo corretamente.

**5. Pós-condições**  
- O sistema confirmou a presença de lixo e iniciou o processo de validação da coleta.

**6. Regras de Negócio**  
- **RN01** - O sistema deve ser capaz de detectar a presença de lixo com precisão, utilizando sensores adequados.
- **RN02** - O sistema não deve permitir o processo de validação de coleta sem a detecção de lixo.
