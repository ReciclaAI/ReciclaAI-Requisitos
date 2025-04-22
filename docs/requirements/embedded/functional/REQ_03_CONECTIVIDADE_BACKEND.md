### Requisito Funcional 3: Conectividade com Backend

**1. Descrição do Caso de Uso**  
**COMO** Sistema Embarcado (Ponto de Coleta)  
**QUERO** Enviar dados de coleta para o backend  
**PARA** Registrar e processar a coleta realizada pelo usuário.

**2. Pré-condições**  
- O sistema embarcado deve ter conectividade com a internet (via Wi-Fi).
- O ponto de coleta deve estar registrado no sistema e preparado para enviar os dados.

**3. Fluxo Principal**  
1. O sistema embarcado valida o QR code escaneado e o peso do lixo.
2. O sistema prepara os dados (QR code, peso, ID do ponto de coleta, etc.) para envio.
3. O sistema envia os dados para o backend através de um message broker.
4. O backend processa os dados e atualiza o status da coleta e a pontuação do usuário.

**4. Fluxo Alternativo**  
4a. Se a conexão com o backend falhar:
   1. O sistema exibe uma mensagem de erro informando que a conexão com o servidor não foi possível.
   2. O sistema deve tentar enviar os dados novamente até que a conexão seja restabelecida.

**5. Pós-condições**  
- Os dados da coleta foram enviados com sucesso para o backend.
- O backend processou os dados e atualizou o status da coleta e a pontuação do usuário.

**6. Regras de Negócio**  
- **RN01** - O sistema embarcado deve garantir que os dados sejam enviados para o backend de forma segura e eficiente.
- **RN02** - Se a comunicação falhar, o sistema deve tentar novamente até que os dados sejam registrados corretamente.
