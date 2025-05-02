# Requisito Funcional: Cadastro de Limite de Coletas Diárias por Usuário 

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** cadastrar e atualizar o limite de coletas diárias permitidas por usuário através da interface administrativa  
**PARA** controlar o número de coletas realizadas e evitar abusos no uso do sistema.

## 2. Pré-condições
- O administrador deve estar autenticado na plataforma administrativa.
- A interface deve conter uma seção de configurações do sistema acessível ao administrador.
- O sistema deve estar apto a armazenar e aplicar limites de coletas por usuário.

## 3. Fluxo Principal
1. O administrador acessa a seção “Configurações” > “Limites de Coleta” no painel administrativo.
2. O sistema realiza uma requisição `GET` para o endpoint `/configuracao/coletas-diarias` e exibe o valor atual do limite.
3. O administrador edita o campo de "Limite de Coletas por Dia" e insere um novo valor.
4. O sistema realiza validações no frontend:
   - O valor deve ser um número inteiro, positivo e maior que zero.
5. Ao clicar em “Salvar”, o sistema envia uma requisição `PUT` para o endpoint `/configuracao/coletas-diarias` com o novo valor.
6. O sistema exibe uma mensagem de sucesso confirmando a atualização do limite.
7. O novo limite entra imediatamente em vigor e será aplicado às coletas realizadas a partir daquele momento.

## 4. Fluxo Alternativo

### 4a. Se o valor inserido for inválido:
1. O sistema exibe mensagens de erro indicando o problema (ex: “Insira um número válido maior que zero”).
2. O botão “Salvar” permanece desativado até que o valor seja corrigido.

### 4b. Se o backend retornar erro na atualização:
1. O sistema exibe uma mensagem de erro: “Não foi possível atualizar o limite. Tente novamente.”

## 5. Pós-condições
- O limite de coletas diárias por usuário foi cadastrado ou atualizado com sucesso.
- O sistema aplicará o novo limite automaticamente nas próximas coletas realizadas pelos usuários.

## 6. Regras de Negócio
- **RN01**: O limite de coletas diárias deve ser configurável apenas por administradores autenticados.
- **RN02**: O valor do limite deve ser um número inteiro positivo.
- **RN03**: O sistema deve verificar o limite a cada nova coleta e impedir o registro de novas coletas caso o limite diário tenha sido atingido.
