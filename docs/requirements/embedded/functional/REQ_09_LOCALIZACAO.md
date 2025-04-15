### Requisito Funcional 9: Localização GPS do Ponto de Coleta

**1. Descrição do Caso de Uso**  
**COMO** Sistema Embarcado (Ponto de Coleta)  
**QUERO** Registrar e enviar a localização GPS do ponto de coleta  
**PARA** Permitir que o usuário localize pontos de coleta próximos e garantir que o sistema saiba a localização exata dos pontos para monitoramento e gerenciamento.

**2. Pré-condições**  
- O sistema embarcado deve ter um módulo de GPS funcional.
- O ponto de coleta deve estar configurado para registrar e enviar a localização do ponto.
- O sistema deve estar conectado à internet para enviar a localização ao backend.

**3. Fluxo Principal**  
1. O sistema embarcado coleta os dados de localização GPS do ponto de coleta (latitude e longitude).
2. O sistema valida se a localização foi capturada corretamente.
3. O sistema registra a localização GPS no banco de dados local do ponto de coleta.
4. O sistema envia a localização GPS ao backend para registro centralizado e para que o ponto de coleta possa ser exibido no mapa para os usuários do aplicativo.
5. O sistema embarcado atualiza periodicamente a localização para garantir que os dados estejam sempre precisos, especialmente se o ponto de coleta for móvel.

**4. Fluxo Alternativo**  
4a. Se o GPS não conseguir capturar a localização corretamente:
   1. O sistema exibe uma mensagem de erro informando que a localização não pôde ser detectada e solicita ao administrador que verifique o dispositivo GPS.
   2. O sistema tenta obter a localização novamente até que a captura seja bem-sucedida.

4b. Se a conexão com a internet falhar durante o envio da localização:
   1. O sistema armazena a localização GPS localmente até que a conexão seja restabelecida.
   2. Assim que a conexão for restaurada, os dados de localização são enviados para o backend.

**5. Pós-condições**  
- A localização GPS do ponto de coleta foi registrada corretamente no sistema.  
- A localização foi enviada ao backend para que os usuários possam visualizar o ponto de coleta em um mapa.

**6. Regras de Negócio**  
- **RN01** - A localização GPS deve ser capturada com precisão e enviada ao backend de forma eficiente.
- **RN02** - O sistema deve garantir que a localização GPS seja registrada corretamente sempre que o ponto de coleta estiver ativo.
- **RN03** - Se o ponto de coleta for móvel, a localização deve ser atualizada periodicamente para refletir sua posição atual.