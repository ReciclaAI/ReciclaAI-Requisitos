## Contexto

A crescente preocupação com a sustentabilidade e o impacto ambiental tem levado cada vez mais pessoas a adotar práticas de reciclagem e descarte consciente de resíduos. No entanto, muitas vezes a falta de incentivo e o acesso limitado a pontos de coleta dificultam o engajamento das pessoas nesse processo. Com isso, surge a necessidade de um sistema inovador que estimule a participação dos cidadãos na reciclagem de resíduos. O aplicativo proposto visa conectar usuários com pontos de coleta, permitindo que cada coleta seja verificada e recompensada, incentivando a adoção de hábitos mais sustentáveis.

## Problema

Embora a reciclagem seja um passo importante para reduzir o impacto ambiental, muitas pessoas ainda não participam ativamente desse processo. Isso se deve, em parte, à falta de motivação, infraestrutura inadequada e desconhecimento sobre como e onde realizar o descarte adequado de resíduos recicláveis. O principal problema a ser resolvido é a criação de um sistema acessível e eficiente que possibilite aos usuários coletar, transportar e descartar corretamente os resíduos recicláveis, com o devido reconhecimento por suas ações sustentáveis.

## Estrutura de Pastas

- **docs/requirements**: Documentação do projeto.
  - **diagrams/**: Diagramas de requisitos.
    - **BPMN/**: Diagrama BPMN.
    - **Estado/**: Diagramas de estado.
    - **NFR/**: Diagramas NFR.
    - **UC/**: Diagramas de casos de uso.
  - **functional/**: Requisitos funcionais.
  - **non_functional/**: Requisitos não funcionais.
  - **domain/**: Requisitos de domínio (regras de negócio).

## Glossário

### Glossário do Sistema de Coleta e Reciclagem de Resíduos

- **Usuário Comum**: Pessoa que utiliza o aplicativo para realizar a coleta e o descarte de resíduos recicláveis, acumulando pontos ou recompensas ao cumprir as tarefas.

- **Administrador**: Pessoa que tem permissões para gerenciar o sistema, incluindo o cadastro de pontos de coleta, a criação e gestão de recompensas, e a visualização de dados analíticos.

- **Ponto de Coleta**: Local designado para o descarte de resíduos recicláveis. O ponto de coleta está equipado com um sistema de verificação, como QR codes, para garantir que a coleta seja validada corretamente pelo aplicativo.

- **Sistema Embarcado**: Dispositivo físico, como uma lixeira inteligente, que realiza a validação do descarte de resíduos através de tecnologia como QR codes, sensores de presença ou outros mecanismos tecnológicos.

- **Coleta**: Processo no qual o usuário descarta resíduos recicláveis em um ponto de coleta e valida a ação para acumular pontos.

- **QR Code**: Código de barras 2D que contém informações, como o identificador único do ponto de coleta. O usuário escaneia o QR code com o aplicativo para registrar sua coleta.

- **Recompensa**: Benefício oferecido aos usuários que realizam o descarte correto de resíduos nos pontos de coleta. As recompensas podem ser resgatadas com pontos acumulados.

- **Pontos**: Unidade de medida para o reconhecimento das ações do usuário. A cada coleta feita corretamente, o usuário acumula pontos, que podem ser trocados por recompensas.

- **Histórico de Coletas**: Registro de todas as coletas realizadas pelo usuário, incluindo informações sobre pontos de coleta, tipos de resíduos e pontos acumulados.

- **Feedback**: Avaliação fornecida pelo usuário sobre sua experiência de coleta. Pode incluir uma avaliação por estrelas e comentários adicionais.

- **Notificação**: Comunicação enviada ao usuário informando sobre eventos importantes, como o sucesso de uma coleta, novas recompensas disponíveis ou falhas no processo de validação.

- **Recompensas por Pontos**: Benefícios oferecidos aos usuários com base na quantidade de pontos acumulados por coletas. As recompensas podem incluir produtos, cupons, descontos, entre outros.

- **Limite de Coletas Diárias**: Quantidade máxima de coletas que um usuário pode realizar em um único dia. Este limite pode ser configurado pelo administrador do sistema.

- **Administração do Sistema**: Processo de gerenciamento do sistema por parte dos administradores, incluindo o cadastro de pontos de coleta, a criação de recompensas, a edição de dados e a análise de dados analíticos.

- **Dashboard**: Interface gráfica utilizada pelos administradores para monitorar o desempenho do sistema, visualizar estatísticas sobre pontos de coleta, coletas realizadas, usuários e recompensas.

- **Autenticação**: Processo de verificação da identidade do usuário, utilizado para garantir que somente usuários autorizados possam acessar o sistema e suas funcionalidades.

- **Autorização**: Definição de permissões de acesso para usuários e administradores, garantindo que apenas pessoas com permissões específicas possam realizar determinadas ações, como gerenciar pontos de coleta ou cadastrar recompensas.

- **Microserviços**: Arquitetura do backend, onde diferentes serviços são responsáveis por tarefas específicas, como o gerenciamento de usuários, pontos de coleta e recompensas. Cada serviço pode ser escalado independentemente para atender à demanda.

- **Backend**: Parte do sistema responsável pela lógica de negócios, armazenamento de dados e comunicação com o frontend. O backend é composto por microserviços, banco de dados e APIs.

- **Frontend**: Interface de usuário com a qual o usuário interage. No caso do sistema, o frontend inclui o aplicativo móvel (Flutter), o painel de administração (React) e as interfaces para consulta e interação com o sistema.

- **API**: Interface de Programação de Aplicações, utilizada para permitir a comunicação entre os microserviços do backend e o frontend.

- **MVP (Minimum Viable Product)**: Versão inicial do sistema, com funcionalidades mínimas para atender às necessidades principais, como o cadastro de pontos de coleta e a validação de coletas via QR code.

- **Armazenamento de Dados**: Processo de armazenamento das informações dos usuários, coletas realizadas, pontos acumulados e recompensas resgatadas em um banco de dados seguro.

- **Segurança da Informação**: Conjunto de medidas adotadas para proteger os dados pessoais e de coleta, garantindo que informações sensíveis sejam criptografadas e acessadas apenas por usuários autorizados.

- **LGPD (Lei Geral de Proteção de Dados)**: Lei brasileira que estabelece regras para a coleta, armazenamento e tratamento de dados pessoais, garantindo a privacidade dos usuários e a proteção de seus dados.

- **Resgatar Recompensa**: Processo no qual o usuário troca seus pontos acumulados por uma recompensa disponível no sistema. O resgate é feito diretamente pelo aplicativo.

- **Sensores de Coleta**: Equipamentos no ponto de coleta que detectam a presença e quantidade de resíduos depositados. Eles ajudam a validar a coleta e podem acionar notificações automáticas.

- **Notificação em Tempo Real**: Mensagens enviadas ao usuário de forma instantânea, informando sobre o sucesso ou falha de uma coleta, bem como outras informações relevantes, como novas recompensas ou limites atingidos.

- **Escalabilidade**: Capacidade do sistema de aumentar a capacidade de processamento ou armazenamento para lidar com um número maior de usuários ou pontos de coleta sem prejudicar a performance.

- **Monitoramento**: Processo de acompanhar o status e o desempenho do sistema em tempo real, permitindo identificar problemas e corrigir falhas rapidamente.

- **Backup**: Processo de criação de cópias de segurança dos dados do sistema, garantindo que informações importantes possam ser restauradas em caso de falhas ou perda de dados.

- **API Gateway**: Componente de infraestrutura que gerencia as requisições entre o frontend e os microserviços do backend, garantindo que as solicitações sejam direcionadas ao serviço correto e otimizando a comunicação.

- **Kubernetes**: Sistema de orquestração de contêineres utilizado para gerenciar e escalar os microserviços do backend, garantindo alta disponibilidade e resiliência do sistema.

## Time de desenvolvimento

### Product Owner
#### - Pablo Deyvid de Paiva

### Scrum Master
#### - Gabriele Rêgo

### Mobile Developer
#### - Luis Eduardo (Tech lead)
#### - Vinicius Melo

### Frontend Developer
#### - Tobias Santos (Tech lead)
#### - André Medeiros

### Backend Developer
#### - Gabriele Duarte (Tech lead)
#### - Pedro Medeiros

### Embedded Developer
#### - André Liberato (Tech lead)
#### - Beatriz Camilo