# ☁️ A Jornada do Zero à Nuvem: Construindo, Quebrando e Evoluindo!

## 🎯 Visão Geral
Muitos profissionais hoje em dia querem começar a construir a casa pelo telhado, utilizando ferramentas "da moda" sem entender como a fundação realmente funciona. Para construir a minha base como **Engenheiro de Nuvem** e **SRE (Site Reliability Engineering)**, eu decidi fazer o caminho inverso: comecei sujando as mãos nas raízes da infraestrutura para entender exatamente como o motor funciona antes de tentar automatizá-lo.

Nos últimos meses, desenvolvi este laboratório prático dividido em 3 grandes fases evolutivas. Meu objetivo não era apenas "fazer funcionar", mas ver a infraestrutura reagir sob pressão, escalar e falhar.

---

## 🏗️ As 3 Fases Evolutivas da Arquitetura

### [Fase 1: A "Raiz" (Infraestrutura Manual)](./docs/lab-raiz)
Eu não queria usar automação mágica logo de cara. Construí um sistema clássico peça por peça, hospedando o front-end de forma Serverless no Amazon S3 e rodando o back-end em servidores virtuais Amazon EC2. 
*   **O objetivo:** Sofrer com as dores do dia a dia da operação manual. Configurei redes na mão, encarei bloqueios rígidos de segurança (Zero Trust) e lidei com erros de comunicação. Monitorei a saúde da aplicação usando o Amazon CloudWatch para entender o valor de traduzir um erro de sistema em um alerta real para a equipe.

### [Fase 2: O Ganho de Escala (Automação)](./docs/lab-avancado)
Uma vez que entendi a dor do trabalho manual, era hora de evoluir. Abandonei a configuração de servidores um a um e empacotei minha aplicação usando Containers (Docker). 
*   **O objetivo:** Garantir a alta disponibilidade. Implementei um Application Load Balancer para distribuir os acessos e criei regras de Auto Scaling, fazendo com que o sistema se multiplicasse sozinho sempre que o tráfego de usuários aumentasse, incluindo arquitetura orientada a eventos (AWS Lambda).

### [Fase 3: O Padrão Enterprise (IaC e Orquestração)](./docs/lab-datadog-kubernets)
O ápice da jornada foi atingir o nível das grandes corporações. Parei de clicar em botões no painel (ClickOps) e passei a escrever a minha infraestrutura inteira em linhas de código (Terraform). 
*   **O objetivo:** Governança e Observabilidade. Criei um orquestrador poderoso (Kubernetes/Amazon EKS) para gerenciar tudo e implementei o Datadog para telemetria profunda, deixando de operar "às cegas".

---

## 💰 O Mundo Real: Limitações e Responsabilidade Financeira (FinOps)
O maior aprendizado, no entanto, veio da realidade física. Como criei esse laboratório em uma conta gratuita da AWS, enfrentei graves gargalos de limite de memória dos servidores. Tentar rodar ferramentas corporativas pesadas (como o agente do Datadog) em máquinas minúsculas me forçou a tomar decisões difíceis. 

Por conta dessas limitações de hardware, optei estrategicamente por não implementar recursos avançados, pois isso exigiria instâncias pagas e estouraria o orçamento. **Saber a hora de parar e respeitar a saúde financeira do projeto é uma das maiores responsabilidades de um Engenheiro SRE.**

---

## 🤖 O "Elefante na Sala": Engenharia e IA
Toda essa arquitetura e documentação não foi feita apenas "fazendo perguntas" a um chat. Eu construí e calibrei um Agente Customizado no Google Gemini para atuar como meu Mentor Sênior (SRE). Alimentei esse agente com diretrizes rígidas, documentações oficiais e a didática das maiores referências da engenharia de software (como Uncle Bob, Martin Fowler e Kelsey Hightower).

Programei a minha IA para debater arquitetura comigo e questionar minhas decisões. A IA foi a minha alavanca de produtividade: deleguei o trabalho braçal e repetitivo para a máquina, para que eu pudesse focar 100% do meu raciocínio no que realmente importa: **pensar em arquitetura, segurança, viabilidade financeira e resolução de incidentes complexos.**

---

## 📂 Acesse a Documentação Completa
Não acredite apenas nas minhas palavras: Eu documentei toda essa jornada. Abaixo você encontra os links detalhando a arquitetura, prints das telas, todos os erros reais que enfrentei pelo caminho e como o meu raciocínio lógico resolveu cada um deles (Runbooks).

*   👉 **[Acessar a Fase 1: Lab Raiz](./docs/lab-raiz)**
*   👉 **[Acessar a Fase 2: Lab Avançado](./docs/lab-avancado)**
*   👉 **[Acessar a Fase 3: Lab Datadog + Kubernetes](./docs/lab-datadog-kubernets)**

<br>