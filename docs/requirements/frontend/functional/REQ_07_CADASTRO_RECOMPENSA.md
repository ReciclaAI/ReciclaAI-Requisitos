# Requisito Funcional: Cadastrar Recompensas por Pontos 

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** cadastrar novas recompensas na interface administrativa, associadas a um número específico de pontos  
**PARA** oferecer incentivos aos usuários e motivá-los a realizar mais coletas.

## 2. Pré-condições
- O administrador deve estar autenticado e autorizado a gerenciar recompensas.
- A interface deve ter acesso à listagem atual de recompensas e à funcionalidade de cadastro.

## 3. Fluxo Principal
1. O administrador acessa a seção “Recompensas” no painel administrativo.
2. O sistema carrega a lista atual de recompensas via requisição `GET` ao endpoint `/recompensas`.
3. O administrador clica em “Cadastrar Nova Recompensa”.
4. O sistema exibe um formulário com os seguintes campos:
   - Nome da recompensa (texto)
   - Descrição da recompensa (texto)
   - Pontos necessários para resgate (número positivo)
   - Imagem ou ícone (upload, opcional)
   - Limite de resgates por usuário (opcional)
5. O administrador preenche os dados e clica em “Salvar”.
6. O sistema valida os campos:
   - Pontos devem ser positivos (**RN01**)
   - Descrição não pode estar vazia (**RN02**)
   - Nome da recompensa deve ser único (**RN03**, pode ser verificado via backend)
7. O sistema envia uma requisição `POST` para o endpoint `/recompensas` com os dados informados.
8. Se bem-sucedido, o sistema exibe uma mensagem de confirmação e a nova recompensa aparece na lista.

## 4. Fluxo Alternativo

### 4a. Se o número de pontos for inválido:
1. O sistema exibe erro: “Informe um número positivo de pontos.”
2. O campo é destacado e o botão “Salvar” fica desabilitado até a correção.

### 4b. Se a descrição estiver vazia:
1. O sistema exibe erro: “A descrição da recompensa é obrigatória.”

### 4c. Se o nome da recompensa já estiver cadastrado:
1. O sistema exibe erro: “Nome já utilizado. Escolha outro nome para a recompensa.”

## 5. Pós-condições
- A nova recompensa está cadastrada e disponível no sistema.
- Usuários podem visualizar e resgatar a recompensa assim que atingirem os pontos necessários.

## 6. Regras de Negócio
- **RN01**: O número de pontos necessários deve ser um valor positivo e válido.
- **RN02**: A descrição da recompensa é obrigatória.
- **RN03**: O nome da recompensa deve ser único no sistema.
- **RN04**: O sistema deve controlar o limite de resgates por usuário, quando definido.
