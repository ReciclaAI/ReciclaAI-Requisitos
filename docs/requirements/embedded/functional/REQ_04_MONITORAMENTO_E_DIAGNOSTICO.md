### Requisito Funcional 4: Monitoramento e Diagnóstico do Sistema Embarcado

**1. Descrição do Caso de Uso**  
**COMO** Administrador  
**QUERO** Monitorar o status do sistema embarcado em tempo real  
**PARA** Detectar falhas e garantir o funcionamento adequado do ponto de coleta.

**2. Pré-condições**  
- O sistema embarcado deve estar instalado e funcionando corretamente.
- O administrador deve ter acesso ao painel de monitoramento do sistema.

**3. Fluxo Principal**  
1. O administrador acessa o painel de monitoramento do sistema embarcado.
2. O sistema exibe o status de todos os pontos de coleta em tempo real, incluindo:
   - Estado da conexão com o backend.
   - Status dos sensores de peso.
   - Status de exibição do QR code.
   - Erros ou falhas detectadas no sistema.
3. O administrador pode visualizar dados de diagnóstico e histórico de eventos.
4. Se um erro for detectado, o administrador pode tomar medidas corretivas, como reiniciar o sistema ou substituir componentes defeituosos.

**4. Fluxo Alternativo**  
4a. Se o sistema detectar uma falha no hardware (como falha no sensor de peso):
   1. O sistema exibe uma mensagem de erro informando o tipo da falha e sugere ações corretivas.
   2. O administrador pode realizar manutenção no sistema ou substituir componentes defeituosos.

**5. Pós-condições**  
- O status do sistema embarcado foi monitorado e qualquer falha foi detectada e registrada para ação corretiva.
- O sistema embarcado foi ajustado ou corrigido conforme necessário.

**6. Regras de Negócio**  
- **RN01** - O sistema embarcado deve ser capaz de reportar falhas de hardware ou software em tempo real.
- **RN02** - O painel de monitoramento deve ser atualizado em tempo real para refletir o status atual dos pontos de coleta.
