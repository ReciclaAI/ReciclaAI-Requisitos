### Requisito Funcional 1: Cadastrar Ponto de Coleta  

**1. Descrição do Caso de Uso**  
**COMO** Administrador  
**QUERO** Cadastrar um novo ponto de coleta no sistema  
**PARA** Gerenciar e monitorar os pontos de coleta de resíduos recicláveis.  

**2. Pré-condições**  
- O administrador deve estar autenticado no sistema.  
- O administrador deve ter permissões para gerenciar pontos de coleta.  

**3. Fluxo Principal**  
1. O administrador acessa a página de cadastro de ponto de coleta.  
2. O sistema solicita que o administrador insira as informações do ponto de coleta, como:
   - Nome do ponto de coleta
   - Endereço completo
   - Tipo de resíduos aceitos
   - Capacidade máxima de armazenamento
   - Horário de funcionamento
   - Método de verificação (QR Code, Sensor, etc.)
3. O administrador preenche os campos obrigatórios e submete o formulário.  
4. O sistema valida os dados inseridos:
   - Verificação de formato válido para endereço.
   - Verificação de que o horário de funcionamento está no formato correto.
5. O sistema registra o novo ponto de coleta e exibe uma mensagem de sucesso.  
6. O administrador pode visualizar o ponto de coleta cadastrado na lista de pontos disponíveis.

**4. Fluxo Alternativo**  
4a. Se os dados estiverem incorretos ou incompletos:
   1. O sistema exibe mensagens de erro indicando quais campos precisam ser corrigidos.
   2. O sistema não prossegue com o cadastro até que todos os campos obrigatórios sejam preenchidos corretamente.

**5. Pós-condições**  
- O novo ponto de coleta está registrado no sistema.  
- As informações do ponto de coleta são armazenadas no banco de dados do sistema.

**6. Regras de Negócio**  
- **RN01** - O nome do ponto de coleta deve ser único no sistema.  
- **RN02** - O endereço deve ser válido e bem formatado.
- **RN03** - A capacidade de armazenamento deve ser um valor numérico positivo.