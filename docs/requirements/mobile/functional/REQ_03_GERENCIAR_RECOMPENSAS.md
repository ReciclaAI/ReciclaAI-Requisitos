### Requisito Funcional 3: Consultar Recompensas do Usuário

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Consultar as recompensas acumuladas com as coletas  
**PARA** Saber quantos pontos eu tenho e onde posso resgatar as recompensas disponíveis.

**2. Pré-condições**  
- O usuário deve estar autenticado no sistema.  
- O sistema deve ter um banco de dados com as recompensas disponíveis.

**3. Fluxo Principal**  
1. O usuário abre o aplicativo e acessa a seção de recompensas.  
2. O sistema exibe a quantidade de pontos acumulados pelo usuário.  
3. O sistema exibe uma lista de recompensas disponíveis, com informações sobre os pontos necessários para resgatar cada uma.
4. O usuário pode visualizar as recompensas, incluindo detalhes como descrição e quantos pontos são necessários para o resgate.
5. O sistema exibe uma indicação de onde o usuário pode resgatar cada recompensa (por exemplo, um local de resgate, loja online, etc.).

**4. Fluxo Alternativo**  
4a. Se o usuário não tiver pontos suficientes:
   1. O sistema exibe uma mensagem informando que o usuário não tem pontos suficientes para resgatar as recompensas.

**5. Pós-condições**  
- O usuário visualizou as recompensas que pode resgatar e os pontos necessários para cada uma.  
- O sistema atualiza a quantidade de pontos do usuário sempre que ele visualiza sua pontuação.

**6. Regras de Negócio**  
- **RN01** - O usuário deve visualizar a quantidade exata de pontos acumulados e as recompensas correspondentes.
- **RN02** - A lista de recompensas deve ser atualizada em tempo real, refletindo as mudanças nos pontos acumulados e nas recompensas disponíveis.

**7. Requisitos Não Funcionais**  
- O sistema deve carregar a seção de recompensas em até 3 segundos para garantir uma boa experiência de usuário.  
- O conteúdo da seção de recompensas deve ser responsivo, garantindo a visualização adequada em diferentes dispositivos (smartphones, tablets, etc.).

