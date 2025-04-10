### Requisito Funcional 5: Exibir Notificação de Coleta Realizada  

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Receber uma notificação após validar minha coleta no ponto de coleta  
**PARA** Saber que minha coleta foi registrada corretamente e que ganhei pontos.

**2. Pré-condições**  
- O usuário deve estar autenticado no sistema.  
- O usuário deve ter completado a coleta e validado o QR code.

**3. Fluxo Principal**  
1. O sistema confirma que o usuário completou a coleta e validou o QR code.  
2. O sistema envia uma notificação ao dispositivo móvel do usuário informando o sucesso da coleta.  
3. A notificação inclui a quantidade de pontos ganhos e a confirmação de que a coleta foi registrada corretamente.

**4. Fluxo Alternativo**  
4a. Se houver um erro na validação:
   1. O sistema envia uma notificação informando que houve um erro na validação da coleta e pede que o usuário tente novamente.

**5. Pós-condições**  
- O usuário recebeu a notificação de coleta realizada.  
- A coleta foi registrada e os pontos foram atualizados no sistema.

**6. Regras de Negócio**  
- **RN01** - A notificação deve ser enviada em tempo real após a validação da coleta.
- **RN02** - A notificação deve incluir detalhes relevantes, como a quantidade de pontos ganhos.
