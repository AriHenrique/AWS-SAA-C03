# Amazon EC2 (Elastic Compute Cloud)

O Amazon EC2 é um serviço fundamental na plataforma de computação em nuvem da Amazon Web Services (AWS). Ele permite que os usuários provisionem e gerenciem máquinas virtuais (instâncias) escaláveis em um ambiente de nuvem altamente flexível. Aqui estão alguns pontos-chave a serem considerados:

### Instâncias Personalizáveis: 
O EC2 oferece uma ampla gama de tipos de instância com diferentes capacidades de CPU, memória e armazenamento, permitindo que você escolha a configuração ideal para suas cargas de trabalho.

### Flexibilidade Geográfica: 
Você pode implantar instâncias EC2 em várias regiões e zonas de disponibilidade ao redor do mundo, permitindo alta disponibilidade e baixa latência para seus aplicativos.

### Modelo de Pagamento Sob Demanda: 
O EC2 é baseado em um modelo de pagamento sob demanda, o que significa que você paga apenas pelo tempo em que suas instâncias estão em execução, sem compromissos de longo prazo.

### Elasticidade e Escalabilidade:
Você pode dimensionar verticalmente (aumentar ou diminuir recursos de instâncias) e horizontalmente (adicionar ou remover instâncias) de acordo com as necessidades de sua aplicação.

### Amplas Opções de SO:
O EC2 suporta uma variedade de sistemas operacionais, incluindo Linux, Windows e outros, permitindo que você escolha o SO mais adequado para suas cargas de trabalho.

### Segurança e Redes:
Você pode configurar grupos de segurança para controlar o tráfego de rede para suas instâncias e integrar suas instâncias EC2 com redes virtuais privadas (VPCs) para maior segurança.

### Armazenamento Flexível:
Além do armazenamento temporário incluído com as instâncias, você pode anexar volumes de armazenamento EBS (Elastic Block Store) para armazenamento persistente.

### Amazon Machine Images (AMIs):
As AMIs são imagens virtuais que servem como modelos para suas instâncias EC2. Você pode escolher entre AMIs pré-configuradas ou criar suas próprias.

## Componentes de uma Instância EC2

Uma instância EC2 (Amazon Elastic Compute Cloud) é composta por vários componentes essenciais para sua configuração e operação. Aqui estão os principais componentes:

## 1. Endereço Elastic IP (EIP)
- Um **Elastic IP** é um endereço IP estático que pode ser associado a uma instância EC2. Isso permite que a instância tenha um endereço IP persistente, facilitando a recuperação após paradas ou reinicializações.

## 2. Keypair (Par de Chaves)
- Um **keypair** é usado para autenticar e acessar remotamente uma instância EC2. Você cria um par de chaves (pública e privada) e associa a chave pública à instância. A chave privada é usada para se conectar à instância com segurança.

## 3. VPC (Virtual Private Cloud) e Subnet
- Uma **VPC** é uma rede virtual isolada na AWS que permite que você crie sua própria rede personalizada. As instâncias EC2 são lançadas em subnets dentro da VPC. Isso ajuda a segmentar e organizar sua infraestrutura de rede.

## 4. IAM (Identity and Access Management)
- **IAM** é o serviço de gerenciamento de identidade da AWS. Você pode usar o IAM para criar políticas e conceder permissões específicas às instâncias EC2. Isso controla quem pode fazer o quê nas instâncias.

## 5. Grupo de Segurança (Security Group)
- Um **grupo de segurança** é uma camada de segurança que age como um firewall virtual em torno das instâncias EC2. Você define regras de entrada e saída no grupo de segurança para controlar o tráfego de rede para e de suas instâncias.

## Definições de Valores para o EC2

O Amazon Elastic Compute Cloud (EC2) oferece várias opções de pagamento e modelos de instâncias para atender às necessidades de diferentes cargas de trabalho. Abaixo estão as definições dos principais valores associados ao EC2:

## 1. On-Demand
- **On-Demand** é um modelo de pagamento para instâncias EC2 em que você paga apenas pelo tempo em que as instâncias estão em execução, sem compromissos de longo prazo. É ideal para cargas de trabalho variáveis e imprevisíveis.<br><br>
- **Exemplo de Uso:** Um site de comércio eletrônico que experimenta picos de tráfego sazonal. Durante os períodos de alta demanda, a empresa pode provisionar instâncias EC2 sob demanda para lidar com o aumento de tráfego. Quando a demanda diminui, eles podem desligar as instâncias para economizar custos.

## 2. Reserved (Reservadas)
- As instâncias **Reserved** são adquiridas com compromissos de longo prazo, geralmente 1 ou 3 anos, em troca de preços significativamente mais baixos em comparação com instâncias sob demanda. Elas são ideais para cargas de trabalho previsíveis e contínuas.<br><br>
- **Exemplo de Uso:** Uma empresa que executa um banco de dados em execução 24/7 pode reservar instâncias EC2 para o banco de dados por um período de 3 anos. Isso garante um preço mais baixo e previsível em comparação com instâncias sob demanda.

## 3. Spot Instance (Instância Spot)
- As **Spot Instances** são instâncias EC2 que permitem que você aproveite capacidade não utilizada da AWS a preços muito mais baixos. No entanto, elas podem ser interrompidas a qualquer momento se a capacidade for necessária para instâncias sob demanda ou reservadas.<br><br>
- **Exemplo de Uso:** Um projeto de processamento em lote de análise de dados que não tem prazos estritos pode usar instâncias Spot para aproveitar os recursos não utilizados da AWS a preços mais baixos. O processamento pode ser interrompido se as instâncias Spot forem interrompidas devido à demanda.

## 4. Dedicated Instance (Instância Dedicada)
- Uma **Dedicated Instance** é uma instância EC2 em que você tem garantias de que será a única instância em um servidor físico. Isso pode ser necessário para atender a requisitos específicos de conformidade ou isolamento.<br><br>
- **Exemplo de Uso:** Uma empresa que precisa cumprir regulamentações específicas de privacidade de dados pode usar instâncias dedicadas para garantir que suas cargas de trabalho compartilhem servidores físicos apenas com recursos autorizados e sem compartilhamento de hardware com outras instâncias.

## 5. Dedicated Hosts (Hosts Dedicados)
- **Dedicated Hosts** são servidores físicos dedicados a você na AWS. Eles oferecem controle total sobre a infraestrutura do host e são ideais para cargas de trabalho que exigem isolamento total.<br><br>
- **Exemplo de Uso:** Uma organização governamental que precisa de controle total sobre a infraestrutura pode usar hosts dedicados para hospedar suas instâncias EC2. Isso permite um alto nível de isolamento e conformidade com regulamentações de segurança.

## 6. Saving Plans (Planos de Economia)
- **Saving Plans** são planos de economia flexíveis que oferecem descontos automáticos em relação às instâncias sob demanda em troca de um compromisso de uso. Eles são adequados para cargas de trabalho que têm requisitos de uso variável.<br><br>
- **Exemplo de Uso:** Uma startup em crescimento que espera um aumento gradual na demanda por recursos de computação pode optar por planos de economia. Isso proporciona economias à medida que a empresa expande sua infraestrutura, mantendo flexibilidade para acomodar as mudanças no uso.

## Período de Cobrança do EC2 por Sistema Operacional

## 1. Windows, Red Hat e SUSE
- **Período de Cobrança:** O Windows, Red Hat e SUSE em instâncias EC2 são cobrados por hora, com um período mínimo de cobrança de 1 hora. Isso significa que, mesmo que você inicie a instância e a utilize por apenas 10 minutos, você será cobrado pelo uso de 1 hora inteira. Da mesma forma, se deixar a instância ligada por 1 hora e 10 minutos, será cobrado por 2 horas.

## 2. Linux
- **Período de Cobrança:** Instâncias EC2 com sistemas operacionais Linux são cobradas por segundo após o primeiro minuto. No primeiro minuto de uso, você é cobrado pelo uso mínimo de 1 minuto, mesmo que utilize a instância por apenas alguns segundos. Após o primeiro minuto, a cobrança é feita exatamente pelos segundos utilizados. Por exemplo, se você usar a instância por 2 minutos e 20 segundos, será cobrado por 2 minutos e 20 segundos, mas se ligar a instância e usar por 30 segundos, será cobrado por 1 minuto.

## Categorias de Instâncias Reservadas na AWS EC2

As instâncias reservadas na Amazon Web Services (AWS) EC2 são divididas em duas categorias principais: "Standard" (Padrão) e "Convertible" (Convertível). Cada categoria oferece diferentes níveis de flexibilidade e opções de modificação. Aqui está uma explicação de ambas:

### 1. Instâncias Reservadas Standard (Padrão)

- As **Instâncias Reservadas Standard** são ideais para cargas de trabalho previsíveis e contínuas, nas quais você sabe exatamente o tipo de instância e a capacidade que precisará por um período prolongado, geralmente de 1 ano ou 3 anos.

- Elas oferecem o maior desconto em comparação com instâncias sob demanda e são a escolha mais econômica quando você tem alta confiança em seus requisitos de computação a longo prazo.

- As Instâncias Reservadas Standard não podem ser modificadas durante o período de compromisso, ou seja, você deve manter o mesmo tipo de instância reservada durante toda a duração do compromisso.

### 2. Instâncias Reservadas Convertible (Convertível)

- As **Instâncias Reservadas Convertible** oferecem um nível superior de flexibilidade. Você pode modificar o tipo de instância reservada, como mudar a família de instâncias, o tamanho e a capacidade, durante o período de compromisso.

- Isso é vantajoso quando você não tem certeza sobre os requisitos de sua carga de trabalho a longo prazo e deseja a capacidade de fazer alterações ao longo do tempo.

- As **Instâncias Reservadas Convertible** geralmente têm um desconto ligeiramente menor em comparação com as Standard, devido à flexibilidade adicional que oferecem.

### Instâncias Reservadas na AWS EC2: Standard vs. Convertible

As instâncias reservadas na Amazon Web Services (AWS) EC2 oferecem opções de flexibilidade para atender às necessidades das cargas de trabalho a longo prazo. Vamos explorar as possibilidades de modificação em ambas as categorias:

#### 1. Instâncias Reservadas Standard (Padrão)

- **Modificações Permitidas:**
    - Zona de Disponibilidade (AZ): Você pode modificar a zona de disponibilidade dentro da mesma região.
    - Tamanho da Instância: É possível modificar o tamanho da instância para uma instância reservada Standard de tamanho igual ou superior.
    - Tipo de Rede (Networking Type): Você pode alterar o tipo de rede da instância reservada.

- **Restrições:**
    - Não é possível modificar a família da instância ou o sistema operacional durante o período de compromisso.

#### 2. Instâncias Reservadas Convertible (Convertível)

- **Modificações Permitidas:**
    - Zona de Disponibilidade (AZ): Você pode modificar a zona de disponibilidade dentro da mesma região.
    - Tamanho da Instância: É possível modificar o tamanho da instância para uma instância reservada Convertible de tamanho igual ou superior.
    - Tipo de Rede (Networking Type): Você pode alterar o tipo de rede da instância reservada.
    - Família da Instância: As instâncias reservadas Convertible oferecem a flexibilidade de modificar a família da instância, permitindo uma mudança mais ampla no tipo de instância.
    - Sistema Operacional (OS): Você pode mudar o sistema operacional da instância reservada.

- **Restrições:**
    - As modificações não podem resultar em uma diminuição do compromisso financeiro inicial. Por exemplo, você não pode mudar para uma instância menor com um compromisso financeiro menor.

## Tipos de Saving Plans (Planos de Economia) na AWS

A AWS oferece diferentes tipos de Saving Plans (Planos de Economia) para atender às diversas necessidades dos clientes. Vamos explorar os dois tipos mencionados:

### 1. Compute Saving Plan (Plano de Economia de Computação)

- **Duração do Compromisso:** Pode variar de 1 a 3 anos.

- **Cobertura de Serviços:** Este tipo de plano é adequado para serviços de computação, incluindo Fargate, Lambda e EC2.

- **Flexibilidade:** Você pode aplicar o Compute Saving Plan a serviços em qualquer região, família de instâncias, tamanho e qualquer sistema operacional (OS).

- **Uso Ideal:** É uma escolha flexível para empresas que desejam economizar em uma variedade de serviços de computação em diferentes configurações de família de instâncias e regiões.

### 2. EC2 Saving Plan (Plano de Economia para EC2)

- **Duração do Compromisso:** Pode variar de 1 a 3 anos.

- **Cobertura de Serviços:** Este plano é específico para instâncias EC2.

- **Restrições:** Para EC2 Saving Plans, você deve escolher uma região específica e uma família de instâncias específica. No entanto, você pode aplicar o plano a qualquer tamanho de instância e a qualquer sistema operacional (OS) dentro dessa família de instâncias.

- **Uso Ideal:** É uma escolha direcionada para organizações que usam instâncias EC2 em uma região e família de instâncias específicas e desejam economizar de forma personalizada, escolhendo entre diferentes tamanhos de instância e sistemas operacionais dentro dessa família.

## Ciclo de Vida de uma Instância EC2 na AWS

O ciclo de vida de uma instância EC2 na Amazon Web Services (AWS) envolve vários estados, cada um com um significado específico. Vamos explorar o processo de inicialização de uma instância EC2 na AWS e como o Identity and Access Management (IAM) desempenha um papel fundamental nesse processo.

### 1. Solicitação de Inicialização

O ciclo de vida começa quando um usuário ou processo solicita a inicialização (ligamento) de uma instância EC2 por meio da API da AWS, da interface de linha de comando ou do Console de Gerenciamento da AWS.

### 2. Verificação de Permissões do IAM

Antes de iniciar a instância, a AWS verifica as permissões do IAM do solicitante para garantir que ele tenha a autorização adequada para executar a ação de inicialização. O IAM é usado para controlar o acesso a recursos na AWS e garantir a segurança.

### 3. Início da Instância

Após a verificação bem-sucedida das permissões do IAM, a instância EC2 é iniciada e entra no estado "Pending" (Em Inicialização). Durante essa fase, a AWS aloca recursos, inicializa o sistema operacional e configura a rede.

### 4. Estado "Running" (Em Execução)

Quando o processo de inicialização é concluído com sucesso, a instância entra no estado "Running" (Em Execução). Neste estado, a instância está ativa e pronta para aceitar solicitações. As permissões do IAM são aplicadas para controlar o acesso aos recursos e serviços da AWS enquanto a instância está em execução.

### 5. Estado "Stopped" (Parada)

Se um usuário decide parar a instância, ela entra no estado "Stopped" (Parada). Neste estado, a instância está desligada, mas sua configuração e dados são mantidos. Ela não está em execução e não incorre em cobranças. Você pode iniciar a instância novamente quando precisar. As permissões do IAM não são verificadas neste estado, pois a instância está desligada.

### 6. Estado "Terminated" (Desligada)

Se uma instância é terminada, ela entra no estado "Terminated" (Desligada). Isso significa que a instância foi encerrada e os recursos associados a ela foram liberados. Uma vez terminada, a instância não pode ser reiniciada e não existe mais. As permissões do IAM não são aplicadas neste estado, pois a instância não está mais ativa.

### 7. Estado "Hibernate" (Hibernação)

Alguns tipos de instâncias EC2 suportam o estado de hibernação. Quando uma instância é colocada em hibernação, o estado da memória da instância é salvo em disco e a instância pode ser retomada exatamente do ponto em que parou após um desligamento. Durante a hibernação e retomada, as permissões do IAM podem ser aplicadas para controlar o acesso aos recursos e serviços da AWS, dependendo do estado em que a instância se encontra.

##  Grupo de Posicionamento EC2 na AWS (Estratégias de Posicionamento)

Os Grupos de Posicionamento EC2 (Auto Scaling Groups - ASG) na Amazon Web Services (AWS) permitem que você gerencie a escalabilidade automática das suas instâncias EC2. Uma parte importante do controle de como as instâncias são distribuídas dentro do grupo é a escolha da estratégia de posicionamento. Existem três estratégias comuns:

### 1. "Cluster" (Agrupamento)

- **Objetivo:** A estratégia "Cluster" visa agrupar instâncias em um mesmo grupo para maximizar a densidade de instâncias em hosts físicos.
- **Utilização:** É útil quando você deseja garantir que várias instâncias do seu grupo sejam colocadas fisicamente próximas umas das outras.
- **Benefícios:** Pode ser importante para aplicativos que exigem baixa latência ou que se beneficiam da proximidade física das instâncias.

### 2. "Spread" (Distribuição Uniforme)

- **Objetivo:** A estratégia "Spread" visa distribuir instâncias uniformemente em várias zonas de disponibilidade (AZs) para melhorar a resiliência contra falhas de uma única AZ.
- **Utilização:** É útil quando você deseja alta disponibilidade e redundância, garantindo que as instâncias não estejam todas na mesma AZ.
- **Funcionamento:** Cada instância é colocada em uma AZ diferente, proporcionando maior isolamento.

### 3. "Partition" (Partição)

- **Objetivo:** A estratégia "Partition" permite que você defina partições de instâncias com base em critérios específicos, como tags.
- **Utilização:** É útil quando você deseja criar grupos de instâncias com base em características comuns, como aplicativos, clientes ou ambientes.
- **Benefícios:** Isso permite um controle granular sobre como as instâncias são distribuídas, tornando a gestão mais eficiente.

Ao escolher a estratégia de posicionamento para o seu Grupo de Posicionamento EC2, leve em consideração os requisitos específicos do seu aplicativo, como latência, alta disponibilidade e necessidades de isolamento. Cada estratégia pode ser apropriada para diferentes casos de uso, e a escolha certa pode melhorar o desempenho e a confiabilidade do seu ambiente na AWS.
