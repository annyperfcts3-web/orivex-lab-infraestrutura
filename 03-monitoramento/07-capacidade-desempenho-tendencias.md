
# 07 — Capacidade, desempenho e análise de tendências

## 1. Objetivo

O gerenciamento de capacidade consiste em acompanhar a utilização dos recursos da infraestrutura para garantir que os equipamentos e serviços suportem a demanda atual e futura.

No ambiente de redes e telecomunicações, essa análise ajuda a identificar gargalos, prevenir indisponibilidades e planejar expansões.

## 2. Indicadores de desempenho

Os principais indicadores acompanhados no monitoramento são:

| Indicador | O que representa |
|---|---|
| CPU | Capacidade de processamento utilizada |
| Memória RAM | Memória utilizada pelo equipamento |
| Disco | Espaço de armazenamento disponível |
| Latência | Tempo de resposta entre dois pontos |
| Perda de pacotes | Percentual de pacotes que não chegam ao destino |
| Throughput | Volume de dados transmitidos em determinado período |
| Banda/interface | Utilização da capacidade de uma interface |
| Temperatura | Condição térmica do equipamento |
| Disponibilidade | Percentual de tempo em que o serviço permanece operacional |

## 3. Capacidade de rede

A capacidade de rede representa o volume máximo de dados que uma interface ou enlace consegue transportar.

Exemplo:

Um enlace de 1 Gbps está transportando 800 Mbps.

Utilização:

**800 Mbps ÷ 1.000 Mbps × 100 = 80%**

Nesse cenário, o enlace está utilizando 80% da capacidade disponível.

Acompanhamento contínuo permite identificar quando um enlace está próximo da saturação.

## 4. Gargalos de infraestrutura

Um gargalo ocorre quando determinado recurso limita o desempenho de um serviço ou equipamento.

Exemplos:

- Interface de rede próxima de 100% de utilização.
- CPU constantemente elevada.
- Memória RAM insuficiente.
- Disco com pouco espaço disponível.
- Latência elevada.
- Perda de pacotes.
- Temperatura acima do limite recomendado.

A identificação antecipada de gargalos permite realizar ações preventivas.

## 5. Análise de tendências

A análise de tendências consiste em observar o comportamento dos indicadores ao longo do tempo.

Ela permite identificar:

- Crescimento gradual do tráfego.
- Aumento recorrente de utilização de CPU.
- Crescimento do consumo de memória.
- Redução do espaço em disco.
- Aumento da quantidade de ONUs conectadas.
- Interfaces com utilização elevada em horários de pico.

Exemplo:

Se um enlace apresenta utilização de 50% em janeiro, 65% em fevereiro e 80% em março, existe uma tendência de crescimento que deve ser investigada.

## 6. Baseline de desempenho

Baseline é uma referência do comportamento normal de um equipamento ou serviço.

É construída por meio da coleta histórica de indicadores.

Exemplo de baseline:

- CPU normalmente entre 20% e 40%.
- Memória normalmente entre 30% e 60%.
- Latência dentro do padrão esperado.
- Tráfego com comportamento previsível.
- Temperatura dentro dos limites operacionais.

Desvios significativos em relação à baseline podem indicar anomalias.

## 7. Limites e alertas

As ferramentas de monitoramento permitem configurar limites para gerar alertas quando um indicador ultrapassa determinado valor.

Exemplo ilustrativo:

| Indicador | Limite de atenção |
|---|---:|
| CPU | Acima de 80% |
| Memória | Acima de 85% |
| Disco | Acima de 90% |
| Interface | Acima de 85% |
| Perda de pacotes | Acima de 2% |

Os limites devem ser ajustados conforme o equipamento, o serviço e a política operacional.

## 8. Aplicação no ambiente NOC/FTTH

Em uma operação NOC, o acompanhamento da capacidade ajuda a prevenir problemas que afetam os clientes.

Exemplos:

**OLT:** acompanhar CPU, memória, temperatura e utilização das interfaces.

**PON:** acompanhar quantidade de ONUs, tráfego e comportamento da porta.

**Uplink:** acompanhar utilização da banda e possíveis sinais de saturação.

**ONU/ONT:** acompanhar estado de conexão e níveis ópticos, quando disponíveis.

**Enlaces:** acompanhar latência, perda de pacotes e utilização da capacidade.

## 9. Ferramentas de acompanhamento

**Zabbix**
- Coleta indicadores de equipamentos.
- Monitora disponibilidade.
- Configura triggers e alertas.
- Armazena histórico de métricas.

**Grafana**
- Apresenta indicadores em dashboards.
- Permite visualizar séries históricas.
- Facilita a identificação de tendências.
- Auxilia na análise de desempenho.

## 10. Importância para a operação

O gerenciamento de capacidade contribui para:

- Prevenir indisponibilidades.
- Identificar gargalos.
- Planejar expansão da infraestrutura.
- Melhorar o desempenho dos serviços.
- Reduzir incidentes recorrentes.
- Apoiar decisões técnicas com dados históricos.

## 11. Conclusão

O monitoramento de capacidade e desempenho permite acompanhar a saúde da infraestrutura e antecipar possíveis problemas.

Em ambientes NOC e FTTH, a análise de indicadores como CPU, memória, tráfego, latência, perda de pacotes e utilização de enlaces é fundamental para manter a estabilidade e a qualidade dos serviços.
