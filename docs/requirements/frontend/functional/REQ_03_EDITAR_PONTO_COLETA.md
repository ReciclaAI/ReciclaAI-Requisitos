# Requisito Funcional: Editar Ponto de Coleta

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** editar as informações de um ponto de coleta existente através da interface administrativa  
**PARA** manter os dados dos pontos de coleta atualizados e precisos.

## 2. Pré-condições
- O administrador deve estar autenticado no painel web.
- O ponto de coleta a ser editado deve estar previamente cadastrado e disponível na base de dados.
- A tela de edição deve estar acessível a partir da listagem de pontos de coleta.

## 3. Fluxo Principal
1. O administrador acessa a seção “Pontos de Coleta” no painel administrativo.
2. O administrador localiza o ponto de coleta desejado na listagem e clica em “Editar”.
3. O sistema carrega os dados atuais do ponto de coleta no formulário de edição:
   - Nome
   - Endereço
   - Tipo(s) de resíduos aceitos
   - Capacidade
   - Horário de funcionamento
4. O administrador altera os campos desejados.
5. O sistema realiza validações no frontend:
   - Nome e endereço preenchidos e com formato válido
   - Capacidade numérica positiva
   - Horário de funcionamento com formato válido
6. O administrador clica em “Salvar Alterações”.
7. O sistema envia uma requisição `PUT` para o endpoint `/pontos-de-coleta/{id}` com os dados atualizados.
8. Se a atualização for bem-sucedida, o sistema exibe uma mensagem de confirmação e retorna à listagem.

## 4. Fluxo Alternativo

### 4a. Se o formulário estiver incompleto ou com erros:
1. O sistema exibe mensagens de erro ao lado dos campos inválidos.
2. O botão “Salvar Alterações” permanece desabilitado ou o formulário não é enviado.

### 4b. Se o backend retornar erro (ex: nome ou endereço já cadastrados):
1. O sistema exibe uma mensagem de erro: “Nome/Endereço já cadastrado”.
2. O administrador pode corrigir e reenviar o formulário.

## 5. Pós-condições
- As informações do ponto de coleta foram atualizadas no sistema e refletem os novos dados informados pelo administrador.
- O administrador visualiza as alterações na listagem ou no mapa.

## 6. Regras de Negócio
- **RN01**: O nome e o endereço do ponto de coleta devem ser únicos no sistema.
- **RN02**: Os campos de capacidade e horário de funcionamento devem ser preenchidos em formato válido e coerente.
