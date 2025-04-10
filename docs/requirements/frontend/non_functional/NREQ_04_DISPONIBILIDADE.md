## 1. Identificação  
**Código:** RNF04  
**Nome:** Disponibilidade do Sistema  

## 2. Descrição  
O sistema deve garantir uma **disponibilidade mínima de 99,9%** durante o horário de operação, exceto em casos de manutenção programada ou emergencial.  

## 3. Justificativa  
Esse requisito é essencial para garantir que os usuários possam utilizar o sistema sem interrupções frequentes, especialmente durante campanhas de reciclagem, onde a disponibilidade é crítica para o engajamento contínuo dos usuários.  

## 4. Critérios de Aceitação  
- **CA01**: O sistema deve ter uma disponibilidade de pelo menos 99,9%, com tempo de inatividade inferior a 8,76 horas anuais.  
- **CA02**: As falhas não planejadas devem ser resolvidas em no máximo 1 hora após a identificação do problema.  

## 5. Observações Técnicas  
- O sistema deve ser monitorado constantemente para detectar falhas rapidamente.  
- A arquitetura deve ser redundante, com servidores em diferentes regiões para evitar falhas de disponibilidade.