# Requisito Funcional 10: Feedback de Coleta

## 1. Descrição do Caso de Uso
COMO **Usuário**  
QUERO **Enviar um feedback sobre a experiência de coleta**  
PARA **Melhorar o serviço e fornecer informações sobre minha experiência.**

## 2. Pré-condições
- O usuário deve estar autenticado no sistema.
- O usuário deve ter realizado uma coleta.

## 3. Fluxo Principal
1. O usuário envia uma requisição POST para o endpoint `/feedback` com os dados do feedback, incluindo:
    - Avaliação da coleta (de 1 a 5 estrelas).
    - Comentários sobre a experiência.
2. O sistema valida os dados recebidos:
    - Verificação de que os campos obrigatórios estão preenchidos (avaliação e/ou comentários).
3. O sistema armazena o feedback no banco de dados, registrando as informações associadas ao usuário e à coleta.
4. O sistema retorna uma resposta de sucesso confirmando que o feedback foi registrado.

## 4. Fluxo Alternativo

### 4a. Se o formulário de feedback estiver incompleto:
1. O sistema retorna uma resposta de erro informando que os campos obrigatórios não foram preenchidos corretamente.
2. O sistema solicita que o usuário complete os campos obrigatórios antes de enviar o feedback.

## 5. Pós-condições
- O feedback do usuário foi registrado no sistema.
- O administrador pode acessar os feedbacks recebidos por meio de uma interface administrativa para analisar as experiências dos usuários.

## 6. Regras de Negócio
- **RN01**: O feedback deve ser armazenado de forma anônima, se solicitado pelo usuário.
- **RN02**: O sistema deve garantir que o feedback seja registrado e acessível para análise por administradores, possibilitando a avaliação da experiência dos usuários.