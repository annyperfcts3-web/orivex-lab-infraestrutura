
# 09 — Monitoramento e Disponibilidade na Nuvem

## 1. Introdução

O monitoramento em nuvem permite acompanhar o funcionamento, desempenho, capacidade e disponibilidade dos recursos computacionais.

É fundamental para identificar falhas, prevenir interrupções e garantir a continuidade dos serviços de TI.

## 2. Principais indicadores de monitoramento

### CPU

Representa a utilização do processamento da máquina virtual.

Uma utilização muito elevada pode indicar sobrecarga.

### Memória RAM

Permite acompanhar o consumo de memória dos sistemas e aplicações.

A falta de memória pode provocar lentidão e falhas.

### Armazenamento

Monitora a capacidade e a utilização dos discos e volumes.

Indicadores:
- Espaço utilizado.
- Espaço disponível.
- IOPS.
- Latência de leitura e escrita.

### Rede

Permite acompanhar o tráfego e a conectividade dos recursos.

Indicadores:
- Latência.
- Perda de pacotes.
- Throughput.
- Tráfego de entrada e saída.
- Disponibilidade de interfaces.

## 3. Ferramentas de monitoramento em nuvem

### Amazon CloudWatch

Serviço da AWS utilizado para monitorar recursos e aplicações.

Principais funcionalidades:
- Coleta de métricas.
- Monitoramento de logs.
- Configuração de alarmes.
- Acompanhamento de desempenho.
- Identificação de anomalias.

### Azure Monitor

Serviço da Microsoft Azure utilizado para acompanhar recursos e aplicações.

Principais funcionalidades:
- Coleta de métricas.
- Análise de logs.
- Configuração de alertas.
- Monitoramento de máquinas virtuais.
- Análise de desempenho.

## 4. Logs, métricas e eventos

### Logs

Registros de atividades realizadas por sistemas, aplicações e serviços.

Exemplo: registro de falha na inicialização de um servidor.

### Métricas

Valores numéricos utilizados para acompanhar o comportamento de um recurso.

Exemplo: utilização de CPU em 85%.

### Eventos

Registros de ocorrências ou mudanças de estado em um ambiente.

Exemplo: inicialização, desligamento ou falha de uma máquina virtual.

## 5. Alertas e notificações

Os alertas permitem identificar situações que exigem atenção ou intervenção.

Exemplos:
- CPU acima de 90%.
- Disco com menos de 10% de espaço livre.
- Máquina virtual indisponível.
- Aumento da latência.
- Perda de conectividade.

Os limites devem ser definidos de acordo com os requisitos de cada ambiente.

## 6. Alta disponibilidade

Alta disponibilidade é a capacidade de manter sistemas e serviços operacionais com o mínimo de interrupção.

Estratégias:
- Redundância de recursos.
- Distribuição entre zonas de disponibilidade.
- Balanceamento de carga.
- Replicação.
- Monitoramento contínuo.
- Planos de recuperação.

## 7. SLA, SLI e SLO

### SLA — Service Level Agreement

Acordo de nível de serviço estabelecido entre fornecedor e cliente.

Define compromissos, responsabilidades e níveis de serviço.

### SLI — Service Level Indicator

Indicador utilizado para medir determinado aspecto do serviço.

Exemplo: percentual de requisições atendidas com sucesso.

### SLO — Service Level Objective

Objetivo de nível de serviço que estabelece uma meta para um indicador.

Exemplo: disponibilidade mensal de 99,9%.

## 8. Cálculo de disponibilidade

A disponibilidade pode ser calculada pela fórmula:

Disponibilidade (%) = (Tempo total - Tempo de indisponibilidade) / Tempo total × 100

Exemplo:

Um serviço deveria funcionar durante 720 horas em um mês, mas ficou indisponível por 7,2 horas.

Disponibilidade = (720 - 7,2) / 720 × 100

Disponibilidade = 99%

## 9. MTBF e MTTR

### MTBF — Mean Time Between Failures

Tempo médio entre falhas.

É utilizado para avaliar a confiabilidade de um equipamento ou sistema reparável.

### MTTR — Mean Time To Repair

Tempo médio para reparo ou restauração.

É utilizado para avaliar o tempo necessário para recuperar um equipamento ou serviço.

Fórmulas:

MTBF = Tempo total de operação / Número de falhas

MTTR = Tempo total de reparo / Número de reparos

## 10. Capacidade e desempenho

O gerenciamento de capacidade busca garantir que os recursos disponíveis atendam à demanda atual e futura.

Devem ser acompanhados:
- CPU.
- Memória.
- Armazenamento.
- Tráfego de rede.
- Latência.
- Crescimento da demanda.
- Tendências de utilização.

## 11. Aplicação em infraestrutura e operação

O profissional de infraestrutura deve:

- Monitorar servidores e máquinas virtuais.
- Acompanhar métricas e logs.
- Configurar alertas.
- Identificar falhas.
- Investigar causas de incidentes.
- Acompanhar SLA.
- Avaliar disponibilidade.
- Planejar capacidade.
- Documentar ocorrências e ações corretivas.

## 12. Resumo para revisão

| Conceito | Significado |
|---|---|
| CloudWatch | Monitoramento AWS |
| Azure Monitor | Monitoramento Azure |
| Logs | Registros de atividades |
| Métricas | Indicadores numéricos |
| Eventos | Ocorrências no ambiente |
| SLA | Acordo de nível de serviço |
| SLI | Indicador de nível de serviço |
| SLO | Objetivo de nível de serviço |
| MTBF | Tempo médio entre falhas |
| MTTR | Tempo médio de reparo |
| HA | Alta disponibilidade |

---
**ORIVEX LAB — Infraestrutura e Redes**  
Trilha: Computação em Nuvem
