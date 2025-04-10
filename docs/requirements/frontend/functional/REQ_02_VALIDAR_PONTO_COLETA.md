### Requisito Funcional 2: Validar Coleta no Ponto de Coleta  

**1. Descrição do Caso de Uso**  
**COMO** Usuário  
**QUERO** Validar minha coleta no ponto de coleta por meio da leitura do QR code  
**PARA** Associar o meu descarte de resíduos ao meu perfil e acumular pontos.  

**2. Pré-condições**  
- O usuário deve estar autenticado no aplicativo.  
- O ponto de coleta deve estar configurado para exibir um QR code válido.

**3. Fluxo Principal**  
1. O usuário chega ao ponto de coleta e abre o aplicativo.  
2. O sistema solicita que o usuário escaneie o QR code exibido no ponto de coleta.  
3. O usuário escaneia o QR code com a câmera do celular.  
4. O sistema valida o QR code, associando-o ao ponto de coleta correto.
5. O sistema registra a coleta e adiciona pontos à conta do usuário.  
6. O sistema exibe uma mensagem de sucesso, confirmando a coleta e a pontuação obtida.

**4. Fluxo Alternativo**  
4a. Se o QR code não for válido ou não for reconhecido:
   1. O sistema exibe uma mensagem de erro informando que o QR code não é válido.
   2. O sistema solicita que o usuário tente escanear o QR code novamente.

**5. Pós-condições**  
- O usuário recebeu pontos pela coleta registrada.  
- A coleta foi associada ao ponto de coleta correto.

**6. Regras de Negócio**  
- **RN01** - O QR code deve ser válido e exclusivo para cada ponto de coleta.  
- **RN02** - O sistema deve garantir que o ponto de coleta e a coleta realizada sejam corretamente associados ao usuário.
