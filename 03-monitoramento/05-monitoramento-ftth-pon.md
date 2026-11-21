
# Monitoramento de Redes FTTH e PON

## 1. Objetivo

Documentar os principais elementos, indicadores e alarmes utilizados no monitoramento de redes FTTH e PON.

## 2. Arquitetura FTTH

FTTH significa Fiber To The Home, tecnologia que utiliza fibra óptica para levar conectividade até o cliente.

Principais elementos:

| Elemento | Função |
|---|---|
| OLT | Equipamento central da rede PON |
| ODF | Distribuição de fibras ópticas |
| Splitter | Divisão do sinal óptico |
| CTO | Caixa de terminação óptica |
| ONU/ONT | Equipamento instalado no cliente |
| Fibra óptica | Meio de transmissão |

## 3. Indicadores monitorados

- Disponibilidade da OLT.
- Estado das interfaces PON.
- ONUs online e offline.
- Potência óptica Tx e Rx.
- Tráfego de entrada e saída.
- Temperatura dos equipamentos.
- Erros e descartes de interfaces.

## 4. Principais alarmes

| Alarme | Significado |
|---|---|
| LOS | Perda de sinal |
| LOF | Perda de enquadramento |
| Dying Gasp | Sinalização de perda de alimentação elétrica da ONU |
| ONU Offline | ONU sem comunicação com a OLT |
| High Temperature | Temperatura elevada |
| Link Down | Interface ou enlace indisponível |
| Optical Low | Potência óptica abaixo do limite configurado |

## 5. Potência óptica

A potência óptica é medida em dBm.

O monitoramento considera:

- Potência de transmissão (Tx).
- Potência de recepção (Rx).
- Atenuação do enlace.
- Limites operacionais do fabricante e da classe óptica.

## 6. Tratamento de incidentes

Em eventos de indisponibilidade, o profissional deve:

1. Identificar o equipamento e a interface afetada.
2. Avaliar a quantidade de clientes impactados.
3. Consultar alarmes e histórico.
4. Correlacionar eventos.
5. Registrar o incidente.
6. Acompanhar a normalização.

## 7. Aplicação em NOC

O monitoramento FTTH permite identificar falhas em equipamentos, interfaces PON e enlaces ópticos, contribuindo para a continuidade dos serviços de telecomunicações.

## 8. Conclusão

O conhecimento de arquitetura FTTH, indicadores ópticos e alarmes PON é fundamental para monitoramento e diagnóstico de redes de acesso.
