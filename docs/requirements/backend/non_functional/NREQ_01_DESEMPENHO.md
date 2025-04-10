## 1. Identificação  
**Código:** RNF01  
**Nome:** Desempenho na Validação de Coleta  

## 2. Descrição  
O sistema deve validar a coleta de resíduos em até **5 segundos** após o usuário realizar o processo de descarte no ponto de coleta, garantindo a rapidez e eficiência do processo.  

## 3. Justificativa  
Esse requisito visa assegurar que os usuários tenham uma experiência ágil ao validar suas coletas e não enfrentem atrasos no processo de recompensa, mantendo o engajamento no aplicativo.  

## 4. Critérios de Aceitação  
- **CA01**: O tempo entre o descarte do usuário e a validação do sistema deve ser inferior a 5 segundos.  
- **CA02**: Caso o tempo de validação ultrapasse 5 segundos, o sistema deve registrar o erro e tentar a validação novamente.  
- **CA03**: A validação deve ser realizada sem erros em 99% dos casos.

## 5. Observações Técnicas  
- O sistema deve ser otimizado para garantir o processamento rápido de dados, utilizando tecnologias de mensageria e verificação em tempo real.  
- A arquitetura do ponto de coleta deve garantir que o sistema embarcado consiga se comunicar com o servidor do aplicativo sem latência significativa.