### Requisito Funcional 6: Feedback de Coleta  

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Enviar um feedback sobre a experiência de coleta  
**PARA** Melhorar o serviço e fornecer informações sobre minha experiência.

**2. Pré-condições**  
- O usuário deve estar autenticado no sistema.  
- O usuário deve ter realizado uma coleta.

**3. Fluxo Principal**  
1. O usuário acessa a opção de feedback no aplicativo após realizar a coleta.  
2. O sistema exibe um formulário de feedback com campos como:
   - Avaliação da coleta (de 1 a 5 estrelas)
   - Comentários sobre a experiência
3. O usuário preenche o formulário e envia o feedback.  
4. O sistema registra o feedback e armazena as informações no banco de dados.

**4. Fluxo Alternativo**  
4a. Se o formulário de feedback estiver incompleto:
   1. O sistema exibe uma mensagem solicitando que o usuário preencha os campos obrigatórios.

**5. Pós-condições**  
- O feedback do usuário foi registrado no sistema.  
- O administrador pode acessar os feedbacks recebidos para avaliar a experiência dos usuários.

**6. Regras de Negócio**  
- **RN01** - O feedback deve ser armazenado de forma anônima, se solicitado pelo usuário.
- **RN02** - O sistema deve garantir que o feedback seja registrado e acessível para análise por administradores.
