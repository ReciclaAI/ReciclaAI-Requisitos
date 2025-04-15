### Requisito Funcional 1: Exibição de QR Code para Validação de Coleta

**1. Descrição do Caso de Uso**  
**COMO** Sistema Embarcado (Ponto de Coleta)  
**QUERO** Exibir um QR code para validação da coleta de resíduos  
**PARA** Permitir que o usuário valide sua coleta e acumule pontos.

**2. Pré-condições**  
- O sistema embarcado deve estar funcionando corretamente e conectado à rede.
- O usuário deve ter o aplicativo aberto e pronto para escanear o QR code.

**3. Fluxo Principal**  
1. O sistema embarcado exibe um QR code único, que está associado ao ponto de coleta.
2. O usuário escaneia o QR code usando o aplicativo.
3. O sistema embarcado valida que o QR code foi escaneado corretamente.
4. O sistema envia os dados da coleta para o backend para registro e atualização dos pontos do usuário.

**4. Fluxo Alternativo**  
4a. Se o QR code não for reconhecido ou se houver erro na leitura:
   1. O sistema exibe uma mensagem de erro informando que o QR code não foi reconhecido e solicita que o usuário tente novamente.

**5. Pós-condições**  
- O QR code foi validado com sucesso e a coleta foi registrada.
- Os pontos do usuário foram atualizados no sistema.

**6. Regras de Negócio**  
- **RN01** - O QR code deve ser único para cada ponto de coleta.
- **RN02** - O QR code deve ser validado em tempo real para garantir que o usuário seja imediatamente notificado sobre o status da coleta.
