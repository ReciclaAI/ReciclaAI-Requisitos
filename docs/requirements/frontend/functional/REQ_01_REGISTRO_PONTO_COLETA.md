# Requisito Funcional: Registro de ponto de coleta

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** Preencher um formulário na interface administrativa para cadastrar um novo ponto de coleta  
**PARA** Gerenciar e monitorar os pontos de coleta de resíduos recicláveis.

## 2. Pré-condições
- O administrador deve estar autenticado e autorizado a acessar a área de gerenciamento de pontos de coleta.
- A interface deve estar carregada com os dados e validações necessárias.

## 3. Fluxo Principal
1. O administrador acessa a seção “Pontos de Coleta” no painel administrativo.
2. O administrador clica no botão “Cadastrar novo ponto”.
3. O sistema exibe um formulário com os seguintes campos obrigatórios:
   - Nome do ponto de coleta
   - Endereço completo
   - Tipo(s) de resíduos aceitos (lista de seleção)
   - Capacidade máxima de armazenamento (número)
   - Horário de funcionamento
   - Método de verificação (ex: QR Code, sensor)
4. O administrador preenche o formulário e clica em “Salvar”.
5. O sistema realiza validações no frontend:
   - Nome preenchido e único (validação pode ser feita via requisição de verificação ao backend)
   - Endereço com formato válido
   - Capacidade como número positivo
6. Se as validações forem atendidas, o sistema envia uma requisição `POST` para o endpoint `/pontos-de-coleta` com os dados preenchidos.
7. Ao receber a confirmação do backend, o sistema exibe uma mensagem de sucesso e redireciona para a lista de pontos de coleta.

## 4. Fluxo Alternativo

### 4a. Se o formulário for enviado com erros de preenchimento:
1. O sistema exibe mensagens de erro ao lado dos campos inválidos ou obrigatórios não preenchidos.
2. O botão “Salvar” permanece desabilitado ou o formulário não é enviado até que todos os campos estejam corretos.

### 4b. Se o backend retornar um erro (ex: nome já existente):
1. O sistema exibe uma mensagem de erro ao usuário informando o motivo (ex: “Nome já cadastrado”).
2. O administrador pode corrigir o campo e reenviar o formulário.

## 5. Pós-condições
- O novo ponto de coleta está registrado no sistema e aparece na lista do painel administrativo.
- As informações são refletidas na interface e sincronizadas com o backend.

## 6. Regras de Negócio (validadas no frontend e/ou backend)
- **RN01**: O nome do ponto de coleta deve ser único no sistema.
- **RN02**: O endereço deve ser válido e bem formatado.
- **RN03**: A capacidade de armazenamento deve ser um valor numérico positivo.
