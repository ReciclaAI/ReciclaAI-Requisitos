# Requisito Funcional: Login do Administrador 

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** fazer login na plataforma administrativa  
**PARA** acessar os módulos de gerenciamento do sistema, como pontos de coleta, recompensas, limites de coletas e feedbacks.

## 2. Pré-condições
- O administrador deve ter uma conta válida no sistema.
- O administrador deve informar suas credenciais (usuário e senha) corretamente no formulário de login.

## 3. Fluxo Principal
1. O administrador acessa a tela de login da plataforma administrativa.
2. O administrador preenche os campos de **usuário** e **senha**.
3. O sistema realiza uma requisição `POST` para o endpoint `/login` com as credenciais informadas.
4. O backend valida as credenciais:
   - Verifica se o nome de usuário existe e está habilitado.
   - Verifica se a senha informada está correta.
5. Se as credenciais forem válidas:
   - O sistema retorna um token JWT (ou similar) com permissões administrativas.
   - O sistema armazena o token de forma segura no frontend (ex: via cookie seguro ou localStorage com medidas de segurança).
   - O administrador é redirecionado para o painel principal (ex: dashboard).
6. A partir deste ponto, o administrador pode navegar entre os módulos disponíveis, com autenticação válida nas requisições.

## 4. Fluxo Alternativo

### 4a. Se as credenciais forem inválidas:
1. O sistema exibe uma mensagem de erro: “Usuário ou senha incorretos.”
2. O formulário permanece ativo para nova tentativa.

### 4b. Se o servidor estiver indisponível:
1. O sistema exibe uma notificação de falha: “Erro de conexão. Tente novamente mais tarde.”

## 5. Pós-condições
- O administrador foi autenticado com sucesso e tem acesso ao painel administrativo da plataforma.

## 6. Regras de Negócio
- **RN01**: As credenciais devem ser validadas com segurança e as senhas comparadas via hash.
- **RN02**: O token de autenticação deve ser gerado com escopo de acesso administrativo e tempo de expiração adequado.
- **RN03**: A sessão do administrador deve ser encerrada após inatividade ou logout explícito.
