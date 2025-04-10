### Requisito Funcional 4: Gerenciar Recompensas do Usuário  

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Consultar as recompensas acumuladas com as coletas  
**PARA** Saber quantos pontos eu tenho e quais recompensas posso resgatar.

**2. Pré-condições**  
- O usuário deve estar autenticado no sistema.  
- O sistema deve ter um banco de dados com as recompensas disponíveis.

**3. Fluxo Principal**  
1. O usuário abre o aplicativo e acessa a seção de recompensas.  
2. O sistema exibe a quantidade de pontos acumulados pelo usuário.  
3. O sistema exibe uma lista de recompensas disponíveis, com a opção de resgatar utilizando os pontos acumulados.  
4. O usuário escolhe uma recompensa e confirma o resgate.  
5. O sistema valida se o usuário tem pontos suficientes para o resgate.
6. O sistema deduz os pontos necessários e confirma o resgate.

**4. Fluxo Alternativo**  
4a. Se o usuário não tiver pontos suficientes:
   1. O sistema exibe uma mensagem informando que o usuário não tem pontos suficientes para resgatar a recompensa.

**5. Pós-condições**  
- O usuário resgatou uma recompensa e seus pontos foram atualizados.  
- A recompensa foi registrada no banco de dados.

**6. Regras de Negócio**  
- **RN01** - O usuário só pode resgatar recompensas se tiver pontos suficientes.  
- **RN02** - A quantidade de pontos necessária para resgatar cada recompensa deve ser definida no sistema.