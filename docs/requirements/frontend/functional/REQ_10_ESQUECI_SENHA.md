# Requisito Funcional: Recuperação de Senha para Administrador 

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** recuperar minha senha caso a tenha esquecido  
**PARA** restabelecer o acesso ao painel administrativo e continuar gerenciando o sistema.

## 2. Pré-condições
- O administrador deve possuir uma conta registrada no sistema.
- O administrador deve informar o e-mail vinculado à sua conta para iniciar o processo de recuperação.

## 3. Fluxo Principal
1. O administrador acessa a tela de login do painel e clica em “Esqueci minha senha”.
2. O sistema exibe um campo para preenchimento do e-mail.
3. O administrador insere o e-mail associado à conta e clica em “Recuperar Senha”.
4. O sistema realiza uma requisição `POST` para o endpoint `/recuperar-senha` com o e-mail fornecido.
5. O backend valida se o e-mail está registrado no sistema.
6. O sistema envia um e-mail contendo um link seguro para redefinição de senha.
7. O administrador acessa o link recebido e é redirecionado para a página de redefinição.
8. O administrador informa a nova senha.
9. O sistema valida:
   - Se a senha atende aos critérios mínimos de segurança (**RN01**).
   - Se o link está válido e não expirado (**RN02**).
10. O sistema atualiza a senha no banco de dados e exibe uma confirmação de sucesso.
11. O administrador é redirecionado para a tela de login para autenticar-se com a nova senha.

## 4. Fluxo Alternativo

### 4a. Se o e-mail informado não estiver cadastrado:
1. O sistema exibe a mensagem: “E-mail não encontrado. Verifique e tente novamente.”

### 4b. Se o link de redefinição estiver expirado:
1. O sistema exibe a mensagem: “Este link expirou. Solicite uma nova recuperação de senha.”

### 4c. Se a nova senha não for segura:
1. O sistema exibe a mensagem: “A senha deve conter ao menos 8 caracteres, incluindo letras e números.”

## 5. Pós-condições
- A senha foi redefinida com sucesso.
- O administrador pode acessar normalmente o sistema com a nova senha.

## 6. Regras de Negócio
- **RN01**: A nova senha deve conter no mínimo 8 caracteres, com letras e números.
- **RN02**: O link de redefinição de senha deve expirar em no máximo 24 horas.
- **RN03**: O processo de recuperação não deve expor se um e-mail está cadastrado, por segurança (opcional).
