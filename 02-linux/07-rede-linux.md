
# Redes Linux

## 1. Objetivo

Documentar os principais comandos utilizados para consultar e diagnosticar configurações de rede em sistemas Linux.

## 2. Interfaces de rede

O comando ip addr permite consultar endereços IP e informações das interfaces de rede.

Exemplo:

ip addr

O comando ip link permite consultar o estado das interfaces.

## 3. Endereçamento e roteamento

| Comando | Finalidade |
|---|---|
| ip addr | Consultar endereços IP |
| ip link | Consultar interfaces |
| ip route | Consultar tabela de rotas |
| hostname -I | Consultar endereços IP locais |

## 4. Diagnóstico de conectividade

| Comando | Finalidade |
|---|---|
| ping | Testar conectividade |
| traceroute | Identificar o caminho dos pacotes |
| ss -tulnp | Consultar portas e serviços |
| ip neigh | Consultar tabela de vizinhos |

## 5. Resolução DNS

O DNS realiza a tradução de nomes de domínio em endereços IP.

Comandos:

resolvectl status
nslookup google.com

A disponibilidade desses comandos depende da distribuição e das ferramentas instaladas.

## 6. Aplicação em infraestrutura

Os comandos de rede Linux permitem investigar problemas de conectividade, interfaces indisponíveis, rotas incorretas, portas utilizadas por serviços e falhas de resolução DNS.

## 7. Conclusão

O conhecimento das ferramentas de rede Linux é essencial para administração de servidores, diagnóstico de conectividade, troubleshooting e operação de infraestrutura NOC.
