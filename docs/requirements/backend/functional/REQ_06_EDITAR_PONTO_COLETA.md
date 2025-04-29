# Requisito Funcional 6: Editar Ponto de Coleta

## 1. Descrição do Caso de Uso
COMO **Administrador**  
QUERO **Editar as informações de um ponto de coleta existente**  
PARA **Manter os dados dos pontos de coleta atualizados e precisos.**

## 2. Pré-condições
- O administrador deve estar autenticado no sistema.
- O ponto de coleta a ser editado deve estar registrado no banco de dados.

## 3. Fluxo Principal
1. O administrador envia uma requisição GET para o endpoint `/pontos-de-coleta/{id}` para obter as informações atuais do ponto de coleta.
2. O sistema retorna os dados atuais do ponto de coleta, incluindo:
    - Nome do ponto de coleta.
    - Endereço.
    - Tipo de resíduos aceitos.
    - Capacidade.
    - Horário de funcionamento.
3. O administrador envia uma requisição PUT para o endpoint `/pontos-de-coleta/{id}` com os dados alterados (ex: nome, endereço, tipo de resíduos aceitos, capacidade, horário de funcionamento).
4. O sistema valida os dados recebidos:
    - Verificação de que o nome e o endereço são únicos no sistema (RN01).
    - Verificação de que a capacidade e o horário de funcionamento estão no formato correto (RN02).
5. Se os dados forem válidos, o sistema atualiza o ponto de coleta no banco de dados.
6. O sistema retorna uma resposta de sucesso, confirmando que as informações foram atualizadas.

## 4. Fluxo Alternativo

### 4a. Se os dados estiverem incorretos ou incompletos:
1. O sistema retorna uma resposta de erro informando os campos que precisam ser corrigidos.
2. O sistema não prossegue com a atualização até que todos os campos obrigatórios sejam preenchidos corretamente.

## 5. Pós-condições
- O ponto de coleta foi atualizado no banco de dados com as novas informações fornecidas.

## 6. Regras de Negócio
- **RN01**: O nome e o endereço do ponto de coleta devem ser únicos no sistema.
- **RN02**: As alterações nos dados de capacidade e horário de funcionamento devem ser validadas corretamente.