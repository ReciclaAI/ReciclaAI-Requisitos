### Requisito Funcional 08: Cadastrar Conta de Usuário

**1. Descrição do Caso de Uso**  
**COMO** Novo Usuário  
**QUERO** Criar uma conta no sistema  
**PARA** Poder acessar as funcionalidades do aplicativo, como coletar resíduos, acumular pontos e resgatar recompensas.

**2. Pré-condições**  
- O usuário deve ter um endereço de e-mail válido.  
- O usuário não deve ter uma conta já registrada com o mesmo e-mail.  
- O sistema deve fornecer um formulário de cadastro acessível.

**3. Fluxo Principal**  
1. O usuário acessa a tela de cadastro do aplicativo ou painel.  
2. O sistema solicita que o usuário preencha o seguinte formulário de cadastro:
   - Nome completo
   - E-mail
   - Telefone (opcional)
   - Senha
   - Confirmar senha
3. O usuário preenche todos os campos obrigatórios.  
4. O sistema valida os dados inseridos:
   - Verifica se o e-mail não está registrado no sistema.
   - Compara se as senhas inseridas no campo "Senha" e "Confirmar senha" são iguais.
   - Verifica se o e-mail está no formato correto.
   - Verifica se a senha atende aos requisitos de segurança (mínimo de 8 caracteres, letras maiúsculas e minúsculas, números e caracteres especiais).
5. Se a validação for bem-sucedida, o sistema registra os dados no banco de dados e cria a conta de usuário.  
6. O sistema envia um e-mail de confirmação de cadastro ao usuário, contendo um link para ativação da conta.
7. O usuário clica no link de ativação para confirmar a conta. Após isso, o usuário é redirecionado para a tela de login.

**4. Fluxo Alternativo**  
4a. Se o e-mail já estiver registrado no sistema:
   1. O sistema exibe uma mensagem informando que o e-mail já está em uso e solicita que o usuário insira um e-mail diferente.

4b. Se as senhas não corresponderem:
   1. O sistema exibe uma mensagem de erro informando que as senhas não são iguais e solicita que o usuário corrija.

**5. Pós-condições**  
- O usuário está cadastrado no sistema e pode realizar login.  
- O sistema envia uma notificação de sucesso para o usuário confirmando o cadastro.

**6. Regras de Negócio**  
- **RN01** - O e-mail deve ser único no sistema.  
- **RN02** - A senha deve atender às políticas de segurança definidas pelo sistema, incluindo a combinação de letras, números e caracteres especiais, com um mínimo de 8 caracteres.  
- **RN03** - A confirmação da senha deve ser idêntica à senha inserida no campo anterior.

**7. Requisitos Não Funcionais**  
- O tempo de resposta para validar e confirmar o cadastro não deve exceder 3 segundos.  
- O sistema deve ser responsivo e acessível em diferentes dispositivos, incluindo smartphones e tablets.  
- O sistema deve garantir a segurança e confidencialidade dos dados pessoais dos usuários, em conformidade com a LGPD.
