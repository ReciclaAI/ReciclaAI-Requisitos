# Requisito Funcional: Visualizar Feedback de Coletas 

## 1. Descrição do Caso de Uso
**COMO** Administrador  
**QUERO** visualizar os feedbacks enviados pelos usuários sobre suas experiências de coleta  
**PARA** analisar a qualidade do serviço e identificar melhorias no processo de descarte e atendimento.

## 2. Pré-condições
- O administrador deve estar autenticado na plataforma administrativa.
- Os usuários devem ter enviado feedbacks após realizar coletas.

## 3. Fluxo Principal
1. O administrador acessa a seção “Feedbacks de Coleta” no painel administrativo.
2. O sistema envia uma requisição `GET` para o endpoint `/feedback` para buscar os registros de feedbacks armazenados.
3. O sistema exibe uma lista dos feedbacks recebidos, contendo:
   - Avaliação (1 a 5 estrelas)
   - Comentários do usuário (se houver)
   - Data do feedback
   - Identificação do ponto de coleta e/ou coleta associada
   - Identificação do usuário (se não for anônimo)
4. O administrador pode:
   - Filtrar feedbacks por avaliação (ex: apenas notas 1 e 2)
   - Filtrar por ponto de coleta ou período
   - Exportar feedbacks para análise externa (opcional)
5. O administrador analisa os feedbacks para tomar decisões gerenciais e operacionais.

## 4. Fluxo Alternativo

### 4a. Se não houver feedbacks registrados:
1. O sistema exibe a mensagem: “Nenhum feedback encontrado.”

### 4b. Se algum feedback for anônimo:
1. O sistema exibe o campo "Usuário" como “Anônimo”.

## 5. Pós-condições
- O administrador acessou e visualizou os feedbacks enviados por usuários.
- Os dados foram utilizados para avaliação da qualidade do serviço.

## 6. Regras de Negócio
- **RN01**: Feedbacks anônimos devem ocultar qualquer dado de identificação do usuário.
- **RN02**: O sistema deve armazenar e exibir todos os feedbacks com integridade e precisão.
- **RN03**: O administrador deve ter opções de filtro por ponto de coleta, avaliação e data para facilitar a análise.
