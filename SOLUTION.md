## 1. Sistema Embarcado para Coleta de Resíduos

### Descrição
O sistema embarcado consiste em um dispositivo físico que opera como ponto de coleta de resíduos recicláveis. Ele será equipado com sensores, mecanismos de validação e uma interface de usuário simples (como uma tela ou LEDs). O principal objetivo é permitir que o usuário registre e valide a coleta de resíduos através da leitura de QR codes, associando a coleta ao usuário que está realizando o descarte.

### Componentes
- **Dispositivo de Coleta**: Uma lixeira inteligente com sensores de presença (para detectar quando o lixo é depositado) e conectividade com a rede.
- **Leitor de QR Code**: O sistema deve ser capaz de exibir um QR code único no ponto de coleta, que o usuário pode escanear com o celular para validar a coleta e acumular pontos.
- **Sensores de Peso/Volume**: Para garantir que o lixo descartado seja de fato reciclável e adequado à categoria do ponto.
- **Conectividade**: A comunicação entre o sistema embarcado e o backend será realizada via MQTT ou WebSocket para garantir comunicação em tempo real e baixa latência.

### Tecnologias
- **Hardware**: Microcontroladores (ex.: Raspberry Pi ou Arduino) para controle e monitoramento.
- **Comunicação**: MQTT ou WebSocket para comunicação em tempo real com o backend.
- **Leitor de QR Code**: Biblioteca para ler QR codes (ex.: ZXing ou ZXing.Net).
- **Sensores**: Sensores de peso (ex.: Load Cell), sensores de proximidade ou câmera para monitoramento do processo de coleta.

---

## 2. Web Admin Frontend

### Descrição
O painel de administração será um site acessível para os administradores do sistema, onde poderão gerenciar os pontos de coleta, visualizar dados analíticos (dashboard), monitorar o status dos pontos, e configurar novos pontos de coleta.

### Componentes
- **Dashboard**: Exibição de gráficos de desempenho, pontos de coleta mais ativos, informações sobre os usuários e status de cada ponto de coleta.
- **Gerenciamento de Pontos de Coleta**: Interface para registrar novos pontos, definir parâmetros de coleta e visualizar o status dos pontos já registrados.
- **Consulta de Pontos**: Funcionalidade de pesquisa para localizar pontos próximos ou disponíveis para coleta.

### Tecnologias
- **Frontend**: React para construir uma interface interativa e responsiva.
- **Bibliotecas de UI**: Material-UI ou Ant Design para componentes de interface modernos e responsivos.
- **State Management**: Redux ou Context API para gerenciar o estado da aplicação.
- **Mapas**: API do Google Maps ou Mapbox para exibir a localização dos pontos de coleta.
- **Autenticação e Autorização**: JWT (JSON Web Tokens) para controle de acesso de administradores.

---

## 3. Backend de Microserviços

### Descrição
O backend será uma arquitetura de microserviços, com serviços desacoplados para gerenciar diferentes aspectos do sistema, como usuários, pontos de coleta, recompensas, entre outros. Cada serviço será independente, podendo ser escalado separadamente.

### Componentes
- **Microserviço de Usuários**: Gerencia o cadastro, autenticação e pontuação dos usuários.
- **Microserviço de Pontos de Coleta**: Gerencia os pontos de coleta, validações e status.
- **Microserviço de Coleta**: Processa os dados de coleta (incluindo a leitura do QR code, monitoramento de resíduos e recompensa ao usuário).
- **Microserviço de Recompensas**: Calcula e gerencia as recompensas, pontos e trocas.

### Tecnologias
- **Linguagem**: Java com Spring Boot para a criação dos microserviços, aproveitando a robustez e a escalabilidade dessa linguagem no backend.
- **Banco de Dados**: PostgreSQL para armazenamento relacional de dados, com tabelas para usuários, pontos de coleta, transações de coleta e recompensas.
- **API Gateway**: Spring Cloud Gateway para orquestrar o tráfego entre os microserviços.
- **Autenticação**: Spring Security com JWT para autenticação e autorização de requisições.
- **Mensageria**: Kafka ou RabbitMQ para comunicação assíncrona entre microserviços (ex.: para enviar notificações ou atualizações em tempo real).

---

## 4. App Mobile

### Descrição
O aplicativo móvel será utilizado pelos usuários para localizar pontos de coleta no mapa, escanear QR codes para registrar as coletas e visualizar informações educativas sobre reciclagem e sustentabilidade.

### Componentes
- **Mapas de Pontos de Coleta**: Exibição interativa de um mapa com pontos de coleta próximos ao usuário.
- **Leitura de QR Code**: Funcionalidade para escanear QR codes nos pontos de coleta para associar a coleta ao usuário.
- **Área Educacional**: Seção do app com conteúdos educativos sobre reciclagem, tipos de resíduos, e como realizar um descarte adequado.
- **Sistema de Recompensas**: Acompanhamento da pontuação e recompensas obtidas pelo usuário ao realizar coletas.

### Tecnologias
- **Framework**: Flutter para construir o aplicativo móvel, permitindo a criação de uma base de código compartilhada entre plataformas iOS e Android.
- **Mapas**: Plugin do Google Maps ou Mapbox para exibir a localização dos pontos de coleta.
- **Leitura de QR Code**: Biblioteca Flutter para escanear QR codes, como `flutter_barcode_scanner` ou `qr_code_scanner`.
- **Área Educacional**: Tela de conteúdo interativo com vídeos, infográficos e textos sobre reciclagem. A biblioteca `flutter_navigation` será usada para navegação entre as telas.
- **Backend**: Conexão com os microserviços através de chamadas RESTful ou GraphQL para manipulação de dados.

---

## 5. Arquitetura Geral

### Descrição
O sistema será estruturado de forma a garantir alta disponibilidade, escalabilidade e resiliência. A comunicação entre as partes será eficiente, utilizando tecnologias de mensageria para garantir que os dados sejam atualizados em tempo real entre os pontos de coleta, o app móvel e o painel de administração.

### Arquitetura
1. **Sistema Embarcado**: O ponto de coleta (lixeira inteligente) se comunica com o backend via MQTT ou WebSocket para enviar dados sobre o descarte de resíduos e atualizar a pontuação do usuário.
2. **Backend de Microserviços**: Todos os microserviços (usuários, pontos de coleta, recompensas) serão comunicados de maneira eficiente através de REST APIs ou GraphQL.
3. **Frontend Web Admin**: O painel de administração será hospedado em um servidor web e se comunicará com os microserviços via APIs.
4. **Aplicativo Móvel**: O app se conecta ao backend para acessar dados sobre pontos de coleta e atualizar o status das coletas. Ele também faz uso de funcionalidades offline, armazenando dados localmente quando não há conectividade, e sincronizando assim que a conexão for restaurada.

### Tecnologias de Infraestrutura
- **Containerização**: Docker para contêinerizar os microserviços, garantindo que cada componente seja facilmente escalável e isolado.
- **Orquestração de Containers**: Kubernetes para gerenciamento de contêineres em larga escala, permitindo autoescalabilidade, balanceamento de carga e monitoramento.
- **CI/CD**: Jenkins ou GitLab CI para automação de testes, builds e deploys.
- **Cloud**: AWS ou Google Cloud para infraestrutura escalável, com serviços de balanceamento de carga, bases de dados gerenciadas e armazenamento em nuvem.

---

## 6. Fluxo de Interação

1. **Usuário** abre o app e visualiza um mapa com os pontos de coleta próximos.
2. **Usuário** escaneia o QR code exibido no ponto de coleta.
3. **Sistema Embarcado** valida a coleta e envia a informação ao backend via MQTT.
4. **Backend** registra a coleta e atualiza a pontuação do usuário, que é refletida no app.
5. **Administrador** acessa o painel web para monitorar as coletas, consultar dados analíticos e gerenciar os pontos de coleta.

---

Este sistema integra tecnologias modernas para garantir que a coleta de resíduos seja realizada de forma eficiente, interativa e sustentável. Com o uso de IoT no ponto de coleta, microserviços para o backend, Flutter para o app móvel e uma interface amigável no frontend, o sistema oferece uma experiência completa tanto para os usuários quanto para os administradores.


















