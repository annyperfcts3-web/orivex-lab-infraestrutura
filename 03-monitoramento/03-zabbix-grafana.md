
# Zabbix e Grafana — Monitoramento de Infraestrutura

## 1. Objetivo

Documentar as funcionalidades e os componentes das plataformas Zabbix e Grafana, utilizadas no monitoramento e na visualização de métricas de infraestrutura.

## 2. Zabbix

O Zabbix é uma plataforma de monitoramento que permite acompanhar servidores, equipamentos de rede, aplicações e serviços.

Principais funcionalidades:

- Monitoramento de disponibilidade.
- Coleta de métricas.
- Monitoramento via SNMP.
- Geração de alertas.
- Histórico de dados.
- Configuração de triggers.

## 3. Componentes do Zabbix

| Componente | Função |
|---|---|
| Zabbix Server | Processamento do monitoramento |
| Zabbix Agent | Coleta de informações |
| Zabbix Proxy | Coleta e encaminhamento de dados |
| Database | Armazenamento de informações |
| Frontend | Interface de administração |

## 4. Conceitos do Zabbix

- Host: equipamento monitorado.
- Item: métrica coletada.
- Trigger: condição de identificação de problema.
- Event: evento gerado pelo sistema.
- Template: conjunto de configurações reutilizáveis.
- Discovery: descoberta automática de dispositivos e recursos.

## 5. Grafana

O Grafana é uma plataforma de visualização e análise de métricas.

Principais funcionalidades:

- Criação de dashboards.
- Visualização de gráficos.
- Análise histórica.
- Integração com fontes de dados.
- Configuração de alertas.

## 6. Integração Zabbix e Grafana

As ferramentas podem trabalhar integradas.

O Zabbix realiza o monitoramento e a coleta de informações, enquanto o Grafana permite visualizar os dados em dashboards.

## 7. Aplicação em NOC

As ferramentas permitem acompanhar indicadores de disponibilidade, CPU, memória, temperatura, tráfego de interfaces e falhas em equipamentos de rede.

## 8. Conclusão

O conhecimento de Zabbix e Grafana é importante para monitoramento de infraestrutura, análise de desempenho, identificação de falhas e operação de ambientes NOC.
