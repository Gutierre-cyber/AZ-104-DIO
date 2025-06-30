Este repositório documenta a implementação de soluções de monitoramento na plataforma Microsoft Azure, utilizando ferramentas como Azure Monitor, Log Analytics e Application Insights. O objetivo é demonstrar como coletar, analisar e visualizar métricas, logs e telemetria de aplicações para garantir a saúde, performance e disponibilidade dos recursos na nuvem.

Visão Geral do Projeto
Neste projeto, você aprenderá a configurar e utilizar os serviços de monitoramento do Azure para obter insights profundos sobre o desempenho e a operação de seus recursos. Serão abordados tópicos essenciais como:

Azure Monitor: Serviço central para coletar, analisar e agir sobre dados de telemetria de seus ambientes Azure e on-premises.

Log Analytics Workspaces: Espaços de trabalho para coletar e correlacionar logs de diversas fontes, permitindo consultas avançadas com KQL (Kusto Query Language).

Application Insights: Monitoramento de performance de aplicações (APM) para identificar gargalos, erros e problemas de performance no código.

Alertas e Dashboards: Como configurar notificações para eventos críticos e criar painéis personalizados para visualização rápida do status dos seus recursos.

Tecnologias Utilizadas
Microsoft Azure

Azure Monitor

Log Analytics

Application Insights

Kusto Query Language (KQL)

Máquinas Virtuais (VMs) no Azure (como recurso a ser monitorado, opcional)

Web Apps no Azure (como recurso a ser monitorado, opcional)

Pré-requisitos
Antes de iniciar, certifique-se de ter:

Uma conta ativa no Azure com uma assinatura válida. Você pode obter uma conta gratuita com créditos para começar.

Conhecimento básico sobre o Portal do Azure.

(Opcional) Algum recurso já implantado no Azure (ex: uma Máquina Virtual, um App Service) para ser monitorado. Se não tiver, o guia incluirá passos para criar recursos básicos para fins de demonstração.

Passo a Passo da Implementação do Monitoramento
Siga este guia para configurar o monitoramento em seu ambiente Azure.

1. Configuração Básica do Azure Monitor
O Azure Monitor é o serviço guarda-chuva para todas as suas necessidades de monitoramento.

Acessar o Azure Monitor: No Portal do Azure, procure por "Monitor" na barra de pesquisa superior e clique no serviço.

Visão Geral: Explore a seção "Visão Geral" para ter uma ideia das métricas e logs já coletados automaticamente para sua assinatura.

2. Criação e Configuração de um Log Analytics Workspace
Um Log Analytics Workspace é onde seus dados de log serão armazenados e analisados.

No Portal do Azure, procure por "Log Analytics workspaces" e clique em "+ Criar".

Básico:

Assinatura: Escolha sua assinatura.

Grupo de recursos: Crie um novo (ex: rg-monitoramento) ou selecione um existente.

Nome: Dê um nome único (ex: la-workspace-meuprojeto).

Região: Escolha a região geográfica mais próxima.

Revisar + Criar: Clique em "Revisar + criar" e depois em "Criar".

Configurar Fontes de Dados: Após a criação, vá para o seu Workspace. Em "Configurações", você pode conectar diferentes fontes de dados (ex: VMs, contêineres, soluções de monitoramento).

3. Monitorando Máquinas Virtuais (Exemplo)
Vamos conectar uma VM existente (ou uma nova) ao seu Log Analytics Workspace.

Navegue até a sua Máquina Virtual no Portal do Azure.

No menu da VM, em "Monitoramento", clique em "Configurações de diagnóstico" ou "Logs".

Configurar Agente Log Analytics: Se o agente ainda não estiver instalado, o Azure irá guiá-lo para instalá-lo e conectá-lo ao seu Log Analytics Workspace. Isso permitirá que a VM envie logs de desempenho, eventos e customizados.

Métricas: Na seção "Métricas" da VM, você pode explorar métricas de CPU, disco, rede, etc., e criar seus próprios gráficos.

4. Utilizando o Application Insights (Exemplo para Aplicações Web)
Para monitorar o desempenho de aplicações, o Application Insights é ideal.

No Portal do Azure, procure por "Application Insights" e clique em "+ Criar".

Básico:

Tipo de recurso: "Recurso" (para aplicações .NET, Java, Node.js, etc.).

Assinatura: Escolha sua assinatura.

Grupo de recursos: Use o mesmo grupo de recursos do seu Log Analytics Workspace.

Nome: Dê um nome (ex: appinsights-minhaaplicacao).

Região: Escolha a região.

Revisar + Criar: Clique em "Revisar + criar" e depois em "Criar".

Integrar com sua Aplicação:

No painel do Application Insights, siga as instruções para "Configurar o monitoramento". Isso geralmente envolve adicionar um SDK à sua aplicação (ex: NuGet para .NET, NPM para Node.js) e configurar a Connection String ou Instrumentation Key.

Para Azure App Services, a integração pode ser feita diretamente pelo portal.

5. Explorando Logs com Kusto Query Language (KQL)
O KQL é a linguagem de consulta usada no Log Analytics para extrair insights dos seus logs.

No seu Log Analytics Workspace ou no Azure Monitor, navegue até "Logs".

Você verá uma interface de consulta. Tente algumas consultas básicas:

Logs de desempenho da VM: Perf | where ObjectName == "Processor" and CounterName == "% Processor Time" | summarize avg(CounterValue) by InstanceName, bin(TimeGenerated, 1h)

Eventos de segurança da VM: SecurityEvent | where EventID == 4624 (Login bem-sucedido)

Requisições do Application Insights: requests | summarize count() by resultCode

Experimente e explore as tabelas de logs disponíveis.

6. Configuração de Alertas
Os alertas notificam você sobre condições críticas.

No Azure Monitor, clique em "Alertas" e depois em "+ Criar" -> "Regra de alerta".

Escopo: Selecione o recurso que você deseja monitorar (VM, App Insights, etc.).

Condição: Defina a métrica ou consulta de log que disparará o alerta (ex: "CPU > 90% por 5 minutos", "Contagem de erros HTTP 500 > 10 em 5 minutos").

Ações: Configure um grupo de ações (email, SMS, webhook, automação).

Detalhes: Dê um nome e descrição ao alerta.

Revisar + Criar: Finalize a criação.

7. Criação de Dashboards Personalizados
Dashboards fornecem uma visão consolidada dos seus principais indicadores.

No Portal do Azure, clique em "Dashboard" (ou crie um novo).

Adicionar Bloco: Clique em "Adicionar um bloco".

Selecione Gráficos: Você pode adicionar gráficos de métricas, resultados de consultas de logs, status de alertas, e muito mais. Arraste e solte os elementos desejados para montar seu painel.

Estrutura do Repositório (Sugestão)
.
├── README.md
├── images/
│   ├── portal_azure_monitor.png
│   ├── log_analytics_workspace_creation.png
│   ├── vm_diagnostic_settings.png
│   ├── application_insights_overview.png
│   ├── kql_query_example.png
│   ├── alert_rule_creation.png
│   └── custom_dashboard_example.png
├── scripts/
│   └── deploy_vm.sh  (Opcional: script para implantar uma VM de teste)
├── docs/
│   └── troubleshooting_monitoramento.md (Opcional: dicas de troubleshooting)
└── .gitignore
Como Entregar Seu Projeto
Crie seu repositório público no GitHub.

Popule-o com este README.md (adaptado e completado com sua experiência).

Se tiver, adicione as capturas de tela relevantes na pasta images/.

Inclua quaisquer arquivos adicionais que documentem sua jornada ou scripts que você usou.

Copie o link do seu repositório.

Clique no botão “Entregar Projeto” (mencionado nas instruções originais) e cole o link, adicionando uma breve descrição sobre o que você implementou e suas principais aprendizagens.
