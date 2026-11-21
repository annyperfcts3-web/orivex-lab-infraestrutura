# Laboratório de Endereçamento IPv4

## 1. Objetivo

Praticar o planejamento e a análise de endereçamento IPv4, incluindo cálculo de sub-redes, identificação de hosts válidos e endereço de broadcast.

## 2. Cenário prático

Uma empresa precisa configurar uma rede local para atender até 50 dispositivos.

**Requisitos:**
- Rede IPv4 privada.
- Pelo menos 50 hosts utilizáveis.
- Máscara de sub-rede adequada.
- Identificação do gateway e da faixa de endereços disponíveis.

## 3. Planejamento da rede

| Parâmetro | Valor |
|---|---|
| Endereço de rede | 192.168.10.0 |
| Prefixo CIDR | /26 |
| Máscara | 255.255.255.192 |
| Broadcast | 192.168.10.63 |
| Primeiro host | 192.168.10.1 |
| Último host | 192.168.10.62 |
| Gateway sugerido | 192.168.10.1 |
| Hosts utilizáveis | 62 |

## 4. Cálculo da sub-rede

A máscara /26 reserva 26 bits para a identificação da rede e 6 bits para hosts.

Fórmula:

2⁶ - 2 = 62 hosts utilizáveis.

O intervalo da sub-rede é de 192.168.10.0 até 192.168.10.63.

## 5. Resultado

A rede /26 atende ao requisito de 50 dispositivos, disponibilizando 62 endereços utilizáveis.

## 6. Conceitos praticados

- Endereçamento IPv4.
- Máscara de sub-rede.
- Notação CIDR.
- Cálculo de hosts.
- Endereço de rede.
- Broadcast.
- Gateway padrão.

## 7. Observação

Este laboratório representa um cenário didático de planejamento de rede. Os endereços apresentados não representam uma configuração de produção.