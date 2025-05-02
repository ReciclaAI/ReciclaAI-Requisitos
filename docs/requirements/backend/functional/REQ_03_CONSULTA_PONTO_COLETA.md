# Requisito Funcional 3: Consultar Pontos de Coleta no Mapa

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Consultar os pontos de coleta disponíveis em um mapa**  
PARA **Localizar os pontos de coleta mais próximos a mim.**

## 2. Pré-condições
- O usuário deve ter o aplicativo instalado e estar autenticado.
- O sistema deve ter dados de pontos de coleta cadastrados no banco de dados, com informações de localização.

## 3. Fluxo Principal
1. O usuário envia uma requisição GET para o endpoint `/pontos-de-coleta/proximos` com sua localização (latitude e longitude).
2. O sistema recebe a localização do usuário e consulta os pontos de coleta cadastrados no banco de dados.
3. O sistema calcula a proximidade dos pontos de coleta em relação ao usuário com base na localização geográfica.
4. O sistema retorna uma lista dos pontos de coleta próximos ao usuário, incluindo as seguintes informações:
    - Endereço.
    - Tipo de resíduos aceitos.
    - Horário de funcionamento.
5. O sistema exibe as localizações dos pontos de coleta em um mapa no frontend, com possibilidade de interação para visualizar mais detalhes.

## 4. Fluxo Alternativo

### 4a. Se o usuário não tiver conexão com a internet:
1. O sistema retorna uma resposta de erro informando que não é possível carregar os dados sem conexão.
2. O sistema oferece a opção de visualizar pontos de coleta offline, caso esses dados estejam armazenados localmente.

## 5. Pós-condições
- O usuário localizou pontos de coleta próximos a ele, com base na sua localização atual.
- O sistema exibiu as informações detalhadas sobre os pontos de coleta no mapa.

## 6. Regras de Negócio
- **RN01**: O mapa deve ser atualizado em tempo real para refletir a localização correta dos pontos de coleta, com base na localização do usuário.
- **RN02**: Os pontos de coleta devem ser exibidos de acordo com a proximidade ao usuário, ordenados de mais próximos para mais distantes.