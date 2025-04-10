### Requisito Funcional 8: Notificação de Nova Recompensa Disponível  

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Receber uma notificação quando uma nova recompensa estiver disponível para resgatar  
**PARA** Ser notificado sobre as novas oportunidades de recompensas com base nos meus pontos acumulados.

**2. Pré-condições**  
- O usuário deve estar autenticado no sistema.  
- O usuário deve ter acumulado pontos suficientes para resgatar recompensas.

**3. Fluxo Principal**  
1. O sistema monitora a quantidade de pontos do usuário.  
2. Quando o usuário atinge um número de pontos que corresponde a uma recompensa disponível, o sistema envia uma notificação ao dispositivo móvel do usuário.  
3. A notificação inclui detalhes sobre a recompensa disponível e os pontos necessários para resgatar.

**4. Fluxo Alternativo**  
4a. Se o usuário não tiver pontos suficientes para a recompensa:
   1. O sistema não envia a notificação de recompensa, pois o usuário não tem pontos suficientes.

**5. Pós-condições**  
- O usuário é notificado sobre a recompensa disponível quando atingir o número necessário de pontos.

**6. Regras de Negócio**  
- **RN01** - A notificação de recompensa deve ser enviada apenas quando o usuário atingir a quantidade mínima de pontos para resgatar a recompensa.
- **RN02** - A notificação deve incluir informações claras sobre os requisitos para resgatar a recompensa.
