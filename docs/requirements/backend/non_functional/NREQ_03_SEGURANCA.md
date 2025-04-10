## 1. Identificação  
**Código:** RNF03  
**Nome:** Segurança de Dados Pessoais  

## 2. Descrição  
Todos os dados pessoais dos usuários, como nome, endereço e informações sobre as coletas, devem ser criptografados tanto em repouso quanto em trânsito, utilizando criptografia de **padrão AES-256** ou superior.  

## 3. Justificativa  
Esse requisito visa proteger a privacidade dos usuários e garantir que informações sensíveis não sejam acessadas por partes não autorizadas, em conformidade com as regulamentações de privacidade de dados, como a LGPD.  

## 4. Critérios de Aceitação  
- **CA01**: Todos os dados pessoais devem ser criptografados utilizando AES-256 em repouso.  
- **CA02**: A comunicação entre o aplicativo e o servidor deve ser realizada via protocolo HTTPS com criptografia TLS.  
- **CA03**: O sistema deve realizar auditorias regulares de segurança para verificar possíveis vulnerabilidades.

## 5. Observações Técnicas  
- A implementação de criptografia deve ser feita utilizando bibliotecas de segurança amplamente reconhecidas.  
- O acesso aos dados sensíveis deve ser restrito apenas a usuários e serviços autorizados.