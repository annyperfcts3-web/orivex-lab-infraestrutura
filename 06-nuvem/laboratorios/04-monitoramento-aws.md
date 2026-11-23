# Laboratório 04 — Monitoramento AWS com CloudWatch

## 1. Objetivo
Conhecer o Amazon CloudWatch e identificar métricas de monitoramento de uma instância EC2.

## 2. Ambiente
- Serviço: Amazon CloudWatch
- Região: Ohio (`us-east-2`)
- Instância: ORIVEX-EC2-LINUX
- ID: `i-016875f33b297f266`
- Tipo: `t3.micro`
- Sistema operacional: Amazon Linux 2023

## 3. Métricas identificadas

| Métrica | Finalidade |
|---|---|
| CPUUtilization | Uso da CPU |
| DiskReadBytes | Volume de dados lidos do disco |
| DiskReadOps | Quantidade de operações de leitura |

## 4. Resultado observado

O CloudWatch apresentou a mensagem "Não há dados disponíveis" para as métricas consultadas.

A instância estava no estado `stopped`, com monitoramento detalhado desativado. Portanto, não foram observadas novas medições durante a consulta.

## 5. Conclusão

O laboratório permitiu conhecer a interface do Amazon CloudWatch, localizar métricas associadas ao EC2 e compreender sua aplicação no monitoramento de infraestrutura em nuvem.

**Projeto:** ORIVEX LAB — Infraestrutura e Redes