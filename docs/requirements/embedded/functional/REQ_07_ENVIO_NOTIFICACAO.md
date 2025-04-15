### Requisito Funcional 7: Envio de Notificação para Administradores em Caso de Falha

**1. Descrição do Caso de Uso**  
**COMO** Sistema Embarcado (Ponto de Coleta)  
**QUERO** Enviar uma notificação para os administradores em caso de falha no ponto de coleta  
**PARA** Garantir que os administradores sejam informados rapidamente sobre problemas no sistema.

**2. Pré-condições**  
- O sistema embarcado deve ter uma conexão de rede ativa.
- O administrador deve estar configurado para receber notificações de falha.

**3. Fluxo Principal**  
1. O sistema embarcado monitora o status dos sensores e da conexão com o backend.
2. Se for detectada uma falha no ponto de coleta (ex: falha no sensor de peso, falha na exibição do QR code, falha na comunicação com o backend), o sistema envia uma notificação para os administradores.
3. A notificação inclui detalhes sobre o tipo de falha e o ponto de coleta afetado.

**4. Fluxo Alternativo**  
4a. Se a falha for resolvida automaticamente:
   1. O sistema notifica os administradores que a falha foi corrigida.

**5. Pós-condições**  
- O administrador foi notificado sobre a falha no ponto de coleta.
- A falha foi registrada para análise posterior.

**6. Regras de Negócio**  
- **RN01** - O sistema deve ser capaz de detectar falhas de hardware ou software e notificá-los em tempo real aos administradores.
- **RN02** - A notificação deve ser clara e incluir detalhes suficientes para o administrador tomar ações corretivas.
