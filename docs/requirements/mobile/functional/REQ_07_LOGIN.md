### Requisito Funcional 07: Login do Usuário

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Fazer login no sistema  
**PARA** Acessar minhas informações pessoais, histórico de coletas, recompensas e pontos acumulados.

**2. Pré-condições**  
- O usuário deve ter uma conta cadastrada no sistema.  
- O usuário deve ter acesso à internet.  
- O sistema deve ter um mecanismo de autenticação configurado.

**3. Fluxo Principal**  
1. O usuário abre o aplicativo ou painel web e acessa a tela de login.  
2. O sistema solicita que o usuário insira seu e-mail e senha.  
3. O usuário preenche o e-mail e senha corretamente.  
4. O sistema valida as credenciais:
   - Verifica se o e-mail existe no banco de dados.
   - Compara a senha fornecida com a armazenada (devidamente criptografada) no banco de dados.
5. Se as credenciais forem válidas, o sistema autentica o usuário e gera um token de sessão (JWT).
6. O sistema redireciona o usuário para a tela principal do aplicativo ou painel, de acordo com seu perfil (usuário comum ou administrador).
7. O sistema exibe uma mensagem de boas-vindas, confirmando o login bem-sucedido.

**4. Fluxo Alternativo**  
4a. Se o e-mail não estiver registrado no sistema:
   1. O sistema exibe uma mensagem informando que o e-mail não foi encontrado e solicita que o usuário verifique o e-mail ou faça o cadastro.  
   2. O sistema não prossegue com o login até que o usuário insira um e-mail válido.

4b. Se a senha estiver incorreta:
   1. O sistema exibe uma mensagem de erro informando que a senha está incorreta e solicita que o usuário tente novamente.

4c. Se o usuário esquecer a senha:
   1. O sistema oferece uma opção de "Esqueci minha senha" que redireciona o usuário para uma tela de recuperação de senha.
   2. O sistema solicita o e-mail para enviar as instruções de recuperação.

**5. Pós-condições**  
- O usuário está autenticado e tem acesso ao sistema, podendo realizar ações de acordo com seu perfil.  
- O sistema gera um token de sessão (JWT) que é armazenado no dispositivo do usuário para autenticação subsequente sem necessidade de inserir as credenciais novamente.

**6. Regras de Negócio**  
- **RN01** - O e-mail deve ser único no sistema.  
- **RN02** - A senha deve ser verificada utilizando criptografia segura (ex.: bcrypt).  
- **RN03** - O sistema deve gerar um token JWT para autenticação, que deve expirar após um tempo determinado (ex.: 30 minutos).
- **RN04** - O usuário não deve ser capaz de visualizar a senha ao fazer o login. A senha deve ser tratada de forma segura e nunca ser armazenada em texto claro.

**7. Requisitos Não Funcionais**  
- O tempo de resposta para validar o login não deve exceder 2 segundos.  
- O sistema deve ser capaz de autenticar até 10.000 usuários simultaneamente sem degradação perceptível no desempenho.  
- O processo de login deve ser seguro, protegendo os dados do usuário, em conformidade com a LGPD e outras regulamentações de segurança de dados.

