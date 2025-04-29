# Requisito Funcional 2: Validar Coleta no Ponto de Coleta

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Validar minha coleta no ponto de coleta por meio da leitura do QR code**  
PARA **Associar o meu descarte de resíduos ao meu perfil e acumular pontos.**

## 2. Pré-condições
- O usuário deve estar autenticado no sistema.
- O ponto de coleta deve estar configurado para gerar um QR code válido.

## 3. Fluxo Principal
1. O usuário envia uma requisição POST para o endpoint `/validar-coleta` com os dados do QR code escaneado.
2. O sistema valida o QR code recebido:
    - Verificação de que o QR code é válido e está associado a um ponto de coleta existente (RN01).
3. Se o QR code for válido, o sistema associa a coleta ao ponto de coleta correto e ao perfil do usuário.
4. O sistema registra a coleta no banco de dados e adiciona pontos à conta do usuário.
5. O sistema retorna uma resposta de sucesso com a pontuação acumulada e confirmação de coleta.

## 4. Fluxo Alternativo

### 4a. Se o QR code não for válido ou não for reconhecido:
1. O sistema retorna uma resposta de erro informando que o QR code não é válido.
2. O sistema solicita que o usuário tente escanear o QR code novamente.

## 5. Pós-condições
- O usuário recebeu pontos pela coleta registrada.
- A coleta foi associada ao ponto de coleta correto no banco de dados.

## 6. Regras de Negócio
- **RN01**: O QR code deve ser válido e exclusivo para cada ponto de coleta.
- **RN02**: O sistema deve garantir que o ponto de coleta e a coleta realizada sejam corretamente associados ao usuário.