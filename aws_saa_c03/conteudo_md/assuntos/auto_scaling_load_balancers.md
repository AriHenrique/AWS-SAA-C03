## Introdução ao Elastic Load Balancer (ELB)

O Elastic Load Balancer (ELB) é um serviço da Amazon Web Services (AWS) projetado para distribuir o tráfego de rede de maneira uniforme entre várias instâncias de Amazon Elastic Compute Cloud (EC2) ou recursos de backend, melhorando a escalabilidade e a disponibilidade das aplicações.

**Exemplo:** Se você possui várias instâncias EC2 executando uma aplicação web, o ELB pode distribuir o tráfego entre elas, ajudando a evitar sobrecargas em uma única instância.

## Diferença entre Scaling UP x Scaling Out

- **Scaling UP:** Refere-se ao aumento da capacidade de uma única instância ou recurso. Isso é feito aumentando os recursos, como CPU e RAM, de uma única máquina.

- **Scaling Out:** Envolve adicionar mais instâncias ou recursos semelhantes. É uma abordagem horizontal, onde novas instâncias são adicionadas para lidar com um maior volume de tráfego.

**Exemplo:** Se sua aplicação web estiver enfrentando um aumento de tráfego, você pode escalar horizontalmente (Scaling Out) adicionando mais instâncias EC2 ao ELB.

## Conhecendo o EC2 Auto Scaling

O Amazon EC2 Auto Scaling é um serviço que ajuda a manter a escalabilidade automática das instâncias EC2, ajustando o número de instâncias com base nas métricas configuradas.

**Exemplo:** Você pode configurar o Auto Scaling para adicionar mais instâncias EC2 ao seu grupo quando a CPU média das instâncias existentes atingir um limite predefinido.

## Introdução ao Load Balancer

Um Load Balancer é um dispositivo ou serviço que distribui o tráfego de rede entre múltiplos destinos, garantindo que as solicitações dos clientes sejam encaminhadas de maneira eficaz para os recursos de backend.

**Exemplo:** Quando um usuário acessa um site, o Load Balancer decide para qual servidor a solicitação deve ser direcionada com base em métricas de saúde e algoritmos de balanceamento.

## Tipos de Load Balancers

Existem vários tipos de Load Balancers na AWS:

- **Classic Load Balancer:** Um balanceador de carga tradicional que distribui o tráfego entre instâncias EC2.

- **Application Load Balancer (ALB):** Um balanceador de carga de camada de aplicação que opera no nível de aplicação e é altamente flexível.

- **Network Load Balancer (NLB):** Um balanceador de carga de camada de transporte que é adequado para aplicativos que lidam com tráfego TCP/UDP.

**Exemplo:** Se você está executando uma aplicação web com várias camadas, pode optar por um Application Load Balancer (ALB) para rotear o tráfego com base em regras de camada de aplicação.

## Auto Scaling com Application Load Balancer (ALB)

O Application Load Balancer (ALB) pode ser usado em conjunto com o Amazon EC2 Auto Scaling para dimensionar automaticamente os recursos conforme necessário. O ALB distribuirá o tráfego entre as instâncias escaladas automaticamente.

**Exemplo:** Se a carga aumentar em seu aplicativo, o Auto Scaling pode adicionar novas instâncias EC2 e o ALB irá distribuir o tráfego entre elas.

Esses tópicos abrangem os fundamentos dos Load Balancers e como eles são usados em conjunto com o Auto Scaling na AWS. Se você tiver dúvidas adicionais ou precisar de exemplos mais específicos, sinta-se à vontade para perguntar.
