### Requisito Funcional 09: Esqueci a Senha

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Recuperar minha senha  
**PARA** Poder acessar minha conta caso tenha esquecido minha senha.

**2. Pré-condições**  
- O usuário deve ter uma conta registrada no sistema.  
- O usuário deve ter acesso ao e-mail associado à conta.

**3. Fluxo Principal**  
1. O usuário acessa a tela de login e clica na opção "Esqueci minha senha".  
2. O sistema solicita que o usuário insira o e-mail associado à conta.  
3. O usuário insere o e-mail e envia a solicitação.  
4. O sistema verifica se o e-mail está registrado no banco de dados.
5. Se o e-mail for válido, o sistema envia um e-mail de recuperação de senha, contendo um link para redefinir a senha.
6. O usuário clica no link de recuperação e é redirecionado para uma página onde pode inserir uma nova senha.  
7. O usuário insere e confirma a nova senha.  
8. O sistema valida a senha inserida:
   - Verifica se a senha atende aos requisitos de segurança definidos (mínimo de 8 caracteres, letras maiúsculas e minúsculas, números e caracteres especiais).
9. Se a senha for válida, o sistema atualiza a senha do usuário no banco de dados e exibe uma mensagem de sucesso.  
10. O usuário é redirecionado para a tela de login para acessar sua conta com a nova senha.

**4. Fluxo Alternativo**  
4a. Se o e-mail não estiver registrado no sistema:
   1. O sistema exibe uma mensagem informando que o e-mail não foi encontrado no banco de dados.

4b. Se a senha inserida não atender aos requisitos de segurança:
   1. O sistema exibe uma mensagem informando que a senha não atende aos requisitos e solicita que o usuário insira uma senha válida.

**5. Pós-condições**  
- A senha do usuário foi atualizada no sistema.  
- O usuário pode fazer login com a nova senha.

**6. Regras de Negócio**  
- **RN01** - O e-mail fornecido deve estar registrado no sistema.  
- **RN02** - A nova senha deve atender às políticas de segurança definidas pelo sistema.

**7. Requisitos Não Funcionais**  
- O tempo de resposta para enviar o e-mail de recuperação não deve exceder 5 segundos.  
- O sistema deve garantir a segurança da recuperação de senha, protegendo as informações sensíveis dos usuários.

