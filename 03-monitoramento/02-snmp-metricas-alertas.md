
# SNMP, Métricas e Alertas de Monitoramento

## 1. Objetivo

Documentar o protocolo SNMP, seus componentes, operações, métricas e níveis de severidade utilizados no monitoramento de infraestrutura.

## 2. Conceito de SNMP

SNMP (Simple Network Management Protocol) é um protocolo utilizado para monitorar e gerenciar equipamentos de rede.

## 3. Componentes

| Componente | Função |
|---|---|
| SNMP Manager | Sistema de gerenciamento |
| SNMP Agent | Agente instalado no equipamento |
| MIB | Base de informações de gerenciamento |
| OID | Identificador de objeto monitorado |

## 4. Portas utilizadas

| Porta | Protocolo | Função |
|---|---|---|
| UDP 161 | SNMP | Consultas |
| UDP 162 | SNMP Trap | Notificações |

## 5. Operações SNMP

- GET: consulta informações.
- GETNEXT: consulta o próximo objeto.
- GETBULK: consulta vários objetos.
- SET: modifica objetos autorizados.
- TRAP: envia notificações.
- INFORM: envia notificações com confirmação.

## 6. Versões

- SNMPv1: versão inicial.
- SNMPv2c: utiliza community strings.
- SNMPv3: oferece autenticação e privacidade.

## 7. Métricas monitoradas

- CPU.
- Memória RAM.
- Tráfego de entrada e saída.
- Erros de interface.
- Pacotes descartados.
- Uptime.
- Latência.
- Perda de pacotes.

## 8. Níveis de severidade

- Informational: informação.
- Warning: atenção.
- Average: problema moderado.
- High: problema grave.
- Disaster: situação crítica.

Os limites de severidade dependem das políticas da plataforma de monitoramento.

## 9. Aplicação em NOC

O SNMP permite acompanhar equipamentos de rede, identificar alterações de desempenho, coletar métricas e receber notificações de eventos.

## 10. Conclusão

O conhecimento de SNMP, métricas e alertas é essencial para monitoramento, diagnóstico de falhas e operação de infraestrutura de redes.
