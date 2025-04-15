### Requisito Funcional 5: Atualização de Software do Sistema Embarcado

**1. Descrição do Caso de Uso**  
**COMO** Administrador  
**QUERO** Atualizar o software do sistema embarcado  
**PARA** Garantir que o sistema esteja sempre funcionando com as versões mais recentes e seguras.

**2. Pré-condições**  
- O sistema embarcado deve ter conectividade com a internet.
- O administrador deve ter permissões para realizar a atualização de software.

**3. Fluxo Principal**  
1. O administrador acessa o painel de gerenciamento do sistema embarcado.
2. O sistema verifica se há atualizações de software disponíveis.
3. Se houver uma atualização disponível, o administrador aprova a instalação.
4. O sistema embarcado faz o download e instala a atualização automaticamente.
5. O administrador é notificado quando a atualização for concluída com sucesso.

**4. Fluxo Alternativo**  
4a. Se a conexão com a internet falhar durante a atualização:
   1. O sistema exibe uma mensagem informando que a atualização não pôde ser concluída.
   2. O sistema tenta novamente a atualização até que a conexão seja restabelecida.

**5. Pós-condições**  
- O sistema embarcado foi atualizado para a versão mais recente do software.
- O administrador foi notificado sobre o sucesso da atualização.

**6. Regras de Negócio**  
- **RN01** - O sistema embarcado deve ser capaz de verificar atualizações periodicamente e permitir a atualização remota sem intervenção manual.
- **RN02** - A atualização de software deve ser segura e não causar interrupções no funcionamento do sistema.
