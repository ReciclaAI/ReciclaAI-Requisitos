# Requisito Funcional 9: Limitar Coletas por Usuário

## 1. Descrição do Caso de Uso
COMO **Administrador**  
QUERO **Definir um limite de coletas que um usuário pode realizar por dia**  
PARA **Controlar o número de coletas realizadas e evitar abusos.**

## 2. Pré-condições
- O administrador deve estar autenticado no sistema.
- O sistema deve ter uma configuração que permita definir o limite de coletas diárias por usuário.

## 3. Fluxo Principal
1. O administrador envia uma requisição GET para o endpoint `/configuracao/coletas-diarias` para visualizar a configuração atual do limite de coletas diárias.
2. O sistema retorna o valor atual do limite de coletas diárias configurado no banco de dados.
3. O administrador envia uma requisição PUT para o endpoint `/configuracao/coletas-diarias` com o novo valor do limite de coletas diárias.
4. O sistema valida o valor enviado:
    - Verificação de que o valor é um número válido e positivo.
5. O sistema aplica a nova configuração, atualizando o limite de coletas diárias no banco de dados.
6. O sistema retorna uma resposta de sucesso confirmando que o limite foi atualizado.

## 4. Fluxo Alternativo

### 4a. Se o administrador tentar definir um valor inválido:
1. O sistema retorna uma resposta de erro informando que o valor é inválido.
2. O administrador é solicitado a inserir um número válido para o limite de coletas diárias.

## 5. Pós-condições
- O limite de coletas diárias foi atualizado e está em vigor para todos os usuários.

## 6. Regras de Negócio
- **RN01**: O limite de coletas diárias deve ser configurável pelo administrador do sistema.
- **RN02**: O limite de coletas deve ser verificado cada vez que um usuário tenta realizar uma coleta, e o sistema deve impedir coletas adicionais caso o limite diário seja atingido.