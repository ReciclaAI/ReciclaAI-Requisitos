# Requisito Funcional: Consultar Pontos de Coleta no Mapa

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** visualizar os pontos de coleta cadastrados em um mapa na interface administrativa  
**PARA** monitorar a localização e distribuição geográfica dos pontos de coleta.

## 2. Pré-condições
- O administrador deve estar autenticado na plataforma web.
- O sistema deve ter pontos de coleta cadastrados com coordenadas geográficas válidas.
- O painel administrativo deve estar integrado com uma API de mapas (ex: Google Maps, Leaflet, Mapbox).

## 3. Fluxo Principal
1. O administrador acessa a seção “Mapa de Pontos de Coleta” no painel administrativo.
2. O sistema carrega os dados dos pontos de coleta via requisição `GET` ao endpoint `/pontos-de-coleta`.
3. O sistema exibe os pontos de coleta em um mapa interativo, utilizando marcadores com base em latitude e longitude.
4. O administrador pode interagir com os marcadores e visualizar detalhes como:
   - Endereço
   - Tipo(s) de resíduos aceitos
   - Capacidade de armazenamento
   - Horário de funcionamento
   - Status operacional (ativo/inativo)
5. O administrador pode aplicar filtros no mapa (ex: por tipo de resíduo, status, capacidade).

## 4. Fluxo Alternativo

### 4a. Se não houver pontos de coleta cadastrados:
1. O sistema exibe uma mensagem: “Nenhum ponto de coleta encontrado no sistema.”

### 4b. Se houver falha ao carregar o mapa:
1. O sistema exibe uma mensagem de erro: “Erro ao carregar o mapa. Tente novamente mais tarde.”

## 5. Pós-condições
- O administrador visualizou os pontos de coleta no mapa da plataforma.
- O administrador pode utilizar essas informações para tomada de decisão e gerenciamento de infraestrutura.

## 6. Regras de Negócio
- **RN01**: O sistema deve exibir os pontos de coleta com base em suas coordenadas geográficas.
- **RN02**: Os marcadores no mapa devem permitir visualização rápida de informações relevantes ao gerenciamento.
- **RN03**: O mapa deve oferecer suporte a filtros e pesquisa para facilitar a análise administrativa.
