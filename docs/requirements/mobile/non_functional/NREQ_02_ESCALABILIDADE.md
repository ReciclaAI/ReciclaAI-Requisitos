## 1. Identificação  
**Código:** RNF02  
**Nome:** Escalabilidade do Sistema  

## 2. Descrição  
O sistema deve ser capaz de suportar até **1 milhão de usuários simultâneos** realizando coletas e interações no aplicativo sem degradação perceptível no desempenho.  

## 3. Justificativa  
Este requisito é essencial para garantir que o sistema possa crescer conforme o número de usuários aumente, sem comprometer a experiência do usuário, especialmente em grandes cidades ou durante campanhas de reciclagem.  

## 4. Critérios de Aceitação  
- **CA01**: O sistema deve ser capaz de processar até 1 milhão de interações simultâneas sem apresentar lentidão significativa.  
- **CA02**: O tempo de resposta do sistema deve ser inferior a 3 segundos em cenários de alta carga.  

## 5. Observações Técnicas  
- A arquitetura deve ser baseada em microserviços, com escalabilidade horizontal.  
- O sistema deve utilizar balanceamento de carga eficiente e ter servidores distribuídos para garantir desempenho consistente. 