
### Requisito Funcional 7: Histórico de Coletas do Usuário  

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Visualizar o histórico das minhas coletas realizadas  
**PARA** Acompanhar as coletas que fiz e verificar meus pontos acumulados.

**2. Pré-condições**  
- O usuário deve estar autenticado no sistema.  
- O usuário deve ter realizado coletas previamente.

**3. Fluxo Principal**  
1. O usuário acessa a seção de histórico de coletas no aplicativo.  
2. O sistema exibe uma lista das coletas realizadas, incluindo as seguintes informações:
   - Data da coleta
   - Ponto de coleta
   - Tipo de resíduos descartados
   - Pontos acumulados
3. O usuário pode visualizar detalhes de cada coleta, como a quantidade de resíduos descartados e qualquer recompensa associada.

**4. Fluxo Alternativo**  
4a. Se o usuário não tiver realizado coletas:
   1. O sistema exibe uma mensagem informando que o histórico de coletas está vazio.

**5. Pós-condições**  
- O usuário visualizou seu histórico de coletas realizadas.

**6. Regras de Negócio**  
- **RN01** - O histórico de coletas deve ser carregado de forma eficiente e em tempo real.
- **RN02** - O sistema deve garantir que o histórico seja sempre atualizado com as coletas mais recentes.
