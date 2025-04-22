### Requisito Funcional 8: Configuração de Sensores no Ponto de Coleta

**1. Descrição do Caso de Uso**  
**COMO** Administrador  
**QUERO** Configurar os sensores no ponto de coleta  
**PARA** Ajustar as configurações do ponto de coleta de acordo com as necessidades específicas de operação.

**2. Pré-condições**  
- O administrador deve estar autenticado no sistema.
- O sistema embarcado deve estar conectado e disponível para configuração.

**3. Fluxo Principal**  
1. O administrador acessa a interface de configuração do ponto de coleta.
2. O administrador configura os parâmetros dos sensores, como:
   - Sensores de peso (ajustes de capacidade máxima)
   - Sensores de proximidade
   - Sensores de temperatura (se aplicável)
3. O administrador salva as configurações e o sistema embarcado aplica as alterações.

**4. Fluxo Alternativo**  
4a. Se as configurações forem inválidas:
   1. O sistema exibe uma mensagem de erro indicando que a configuração é inválida ou não pode ser aplicada.

**5. Pós-condições**  
- O ponto de coleta está configurado com os novos parâmetros de sensores.
- As alterações foram aplicadas e o ponto de coleta está pronto para operar com as novas configurações.

**6. Regras de Negócio**  
- **RN01** - O administrador deve ter permissões adequadas para configurar os sensores no ponto de coleta.
- **RN02** - O sistema deve validar as configurações antes de aplicá-las.