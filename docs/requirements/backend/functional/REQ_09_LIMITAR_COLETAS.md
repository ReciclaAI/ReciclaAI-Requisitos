### Requisito Funcional 9: Limitar Coletas por Usuário  

**1. Descrição do Caso de Uso**  
**COMO** Administrador  
**QUERO** Definir um limite de coletas que um usuário pode realizar por dia  
**PARA** Controlar o número de coletas realizadas e evitar abusos.

**2. Pré-condições**  
- O administrador deve estar autenticado no sistema.  
- O sistema deve ter uma configuração para limitar o número de coletas diárias por usuário.

**3. Fluxo Principal**  
1. O administrador acessa a configuração do sistema para limitar as coletas diárias dos usuários.  
2. O sistema permite que o administrador defina o número máximo de coletas diárias permitidas para cada usuário.  
3. O administrador submete a configuração.  
4. O sistema valida a configuração e aplica o limite de coletas diárias.

**4. Fluxo Alternativo**  
4a. Se o administrador tentar definir um valor inválido:
   1. O sistema exibe uma mensagem de erro informando que o valor é inválido e solicita que o administrador insira um número válido.

**5. Pós-condições**  
- O limite de coletas diárias foi atualizado e está em vigor para todos os usuários.

**6. Regras de Negócio**  
- **RN01** - O limite de coletas diárias deve ser configurável pelo administrador do sistema.
- **RN02** - O limite de coletas deve ser verificado cada vez que um usuário tenta realizar uma coleta.
