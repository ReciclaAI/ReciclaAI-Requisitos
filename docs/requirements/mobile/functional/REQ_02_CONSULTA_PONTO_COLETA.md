### Requisito Funcional 2: Consultar Pontos de Coleta no Mapa  

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Consultar os pontos de coleta disponíveis em um mapa  
**PARA** Localizar os pontos de coleta mais próximos a mim.

**2. Pré-condições**  
- O usuário deve ter o aplicativo instalado e estar autenticado.  
- O sistema deve ter dados de pontos de coleta cadastrados.

**3. Fluxo Principal**  
1. O usuário abre o aplicativo e acessa a tela de consulta de pontos de coleta.  
2. O sistema exibe um mapa com a localização do usuário.  
3. O sistema exibe no mapa os pontos de coleta próximos ao usuário.  
4. O usuário pode interagir com o mapa, visualizando mais informações sobre os pontos de coleta, como endereço, tipo de resíduos aceitos e horário de funcionamento.

**4. Fluxo Alternativo**  
4a. Se o usuário não tiver conexão com a internet:
   1. O sistema exibe uma mensagem informando que não é possível carregar o mapa sem conexão.
   2. O sistema oferece a opção de visualizar pontos de coleta offline, se disponível.

**5. Pós-condições**  
- O usuário localizou pontos de coleta próximos a ele.  
- O usuário pode interagir com o mapa para obter mais detalhes.

**6. Regras de Negócio**  
- **RN01** - O mapa deve ser atualizado em tempo real para refletir a localização correta dos pontos de coleta.
- **RN02** - Os pontos de coleta devem ser exibidos de acordo com a proximidade ao usuário.
