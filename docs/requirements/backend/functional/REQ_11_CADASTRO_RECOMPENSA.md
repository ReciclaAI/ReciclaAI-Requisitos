### Requisito Funcional 11: Cadastrar Recompensas por Pontos  

**1. Descrição do Caso de Uso**  
**COMO** Administrador  
**QUERO** Cadastrar novas recompensas no sistema associadas a um número de pontos específicos  
**PARA** Oferecer incentivos aos usuários e motivá-los a realizar mais coletas.

**2. Pré-condições**  
- O administrador deve estar autenticado no sistema.  
- O administrador deve ter permissões adequadas para gerenciar recompensas no sistema.

**3. Fluxo Principal**  
1. O administrador acessa a página de gerenciamento de recompensas no painel de administração.  
2. O sistema exibe a lista de recompensas cadastradas e a opção para adicionar uma nova recompensa.  
3. O administrador clica na opção de adicionar nova recompensa.  
4. O sistema solicita que o administrador insira os seguintes dados:
   - Nome da recompensa
   - Descrição da recompensa
   - Número de pontos necessários para resgatar
   - Imagem ou ícone da recompensa (opcional)
   - Limite de resgates por usuário (opcional)
5. O administrador preenche os campos e submete o formulário.  
6. O sistema valida os dados inseridos, incluindo:
   - Verificação de que o número de pontos é um valor válido e positivo.
   - Verificação de que a descrição não está vazia.
7. O sistema registra a nova recompensa e exibe uma mensagem de sucesso.  
8. A nova recompensa é adicionada à lista de recompensas disponíveis para resgate pelos usuários.

**4. Fluxo Alternativo**  
4a. Se o número de pontos inserido não for válido ou estiver em formato incorreto:
   1. O sistema exibe uma mensagem de erro informando que o número de pontos deve ser um valor válido.
   2. O sistema não prossegue com o cadastro até que o valor seja corrigido.

4b. Se a descrição estiver vazia:
   1. O sistema exibe uma mensagem de erro informando que a descrição da recompensa não pode estar vazia.

**5. Pós-condições**  
- A nova recompensa foi cadastrada no sistema e está disponível para os usuários resgatarem, caso atinjam o número de pontos necessários.  
- A recompensa foi registrada no banco de dados.

**6. Regras de Negócio**  
- **RN01** - O número de pontos necessários para resgatar a recompensa deve ser um valor positivo e válido.  
- **RN02** - O nome da recompensa deve ser único no sistema para evitar duplicação de recompensas.  
- **RN03** - A recompensa só pode ser resgatada após o usuário atingir a quantidade mínima de pontos definida.
