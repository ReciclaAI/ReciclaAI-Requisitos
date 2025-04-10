### Requisito Funcional 6: Editar Ponto de Coleta  

**1. Descrição do Caso de Uso**  
**COMO** Administrador  
**QUERO** Editar as informações de um ponto de coleta existente  
**PARA** Manter os dados dos pontos de coleta atualizados e precisos.

**2. Pré-condições**  
- O administrador deve estar autenticado no sistema.  
- O ponto de coleta a ser editado deve estar registrado no sistema.

**3. Fluxo Principal**  
1. O administrador acessa a lista de pontos de coleta no painel de administração.  
2. O administrador seleciona o ponto de coleta a ser editado.  
3. O sistema exibe as informações atuais do ponto de coleta.  
4. O administrador altera os campos necessários (ex: nome, endereço, tipo de resíduos aceitos, capacidade, horário de funcionamento).  
5. O administrador submete as alterações.  
6. O sistema valida os dados e confirma as modificações, atualizando o ponto de coleta no banco de dados.

**4. Fluxo Alternativo**  
4a. Se os dados estiverem incorretos ou incompletos:
   1. O sistema exibe mensagens de erro indicando quais campos precisam ser corrigidos.
   2. O sistema não prossegue com a edição até que todos os campos obrigatórios sejam preenchidos corretamente.

**5. Pós-condições**  
- O ponto de coleta foi atualizado no sistema com as novas informações.  

**6. Regras de Negócio**  
- **RN01** - O nome e o endereço do ponto de coleta devem ser únicos no sistema.  
- **RN02** - As alterações nos dados de capacidade e horário de funcionamento devem ser validadas corretamente.