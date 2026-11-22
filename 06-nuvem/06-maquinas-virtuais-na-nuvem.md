
# 06 — Máquinas Virtuais na Nuvem

## 1. Introdução

Uma máquina virtual (VM — Virtual Machine) é um ambiente computacional virtualizado que funciona como um computador independente, utilizando recursos físicos de um servidor.

Na computação em nuvem, máquinas virtuais são disponibilizadas sob demanda por provedores como AWS e Microsoft Azure.

## 2. Componentes de uma máquina virtual

Uma máquina virtual pode possuir:

- CPU virtual (vCPU).
- Memória RAM.
- Disco virtual.
- Interface de rede virtual.
- Sistema operacional.
- Configurações de segurança.

Esses recursos são definidos conforme a necessidade da aplicação.

## 3. Hipervisor

O hipervisor é a camada de software responsável por criar e executar máquinas virtuais, distribuindo os recursos físicos do servidor entre elas.

### Tipos de hipervisores

**Tipo 1 — Bare Metal**

Executado diretamente sobre o hardware físico.

Exemplos:
- VMware ESXi.
- Microsoft Hyper-V.
- Xen.

**Tipo 2 — Hosted**

Executado sobre um sistema operacional convencional.

Exemplos:
- Oracle VirtualBox.
- VMware Workstation.

## 4. Máquinas virtuais na AWS e Azure

### AWS EC2

Serviço que permite provisionar instâncias de máquinas virtuais.

É possível configurar:
- Tipo de instância.
- Processamento e memória.
- Sistema operacional.
- Armazenamento.
- Rede.
- Regras de segurança.

### Azure Virtual Machines

Serviço que permite criar máquinas virtuais Windows e Linux na plataforma Azure.

É possível configurar:
- Tamanho da máquina.
- CPU e memória.
- Sistema operacional.
- Discos.
- Rede virtual.
- Regras de acesso.

## 5. Escalabilidade

A capacidade de uma máquina virtual pode ser ajustada conforme a necessidade.

### Escalabilidade vertical

Aumenta ou reduz os recursos de uma máquina existente, como CPU e memória.

### Escalabilidade horizontal

Adiciona ou remove máquinas virtuais para distribuir a carga de trabalho.

## 6. Armazenamento das máquinas virtuais

As máquinas virtuais utilizam discos virtuais para armazenar sistemas operacionais, aplicações e dados.

Exemplos:
- AWS EBS.
- Azure Managed Disks.

É importante planejar capacidade, desempenho, backup e recuperação.

## 7. Rede e segurança

Uma máquina virtual precisa de conectividade e controles de acesso adequados.

Elementos importantes:
- Endereço IP privado e público.
- Interface de rede virtual.
- Sub-rede.
- Tabela de rotas.
- Firewall.
- Security Groups ou NSGs.
- Controle de acesso remoto.

O acesso administrativo deve ser restrito aos endereços e usuários autorizados.

## 8. Disponibilidade e recuperação

Para aumentar a disponibilidade de máquinas virtuais, podem ser utilizadas estratégias como:

- Distribuição de instâncias entre zonas de disponibilidade.
- Redundância.
- Backups periódicos.
- Snapshots de discos.
- Monitoramento de recursos.
- Planos de recuperação de desastres.

## 9. Aplicação em infraestrutura e operação

O profissional de infraestrutura pode utilizar máquinas virtuais para:

- Hospedar servidores.
- Executar sistemas corporativos.
- Administrar serviços Linux e Windows.
- Configurar redes.
- Monitorar CPU, memória e armazenamento.
- Planejar capacidade e disponibilidade.
- Executar rotinas de backup e recuperação.

## 10. Resumo para revisão

| Conceito | Significado |
|---|---|
| VM | Máquina virtual |
| Hipervisor | Gerencia máquinas virtuais |
| vCPU | Processador virtual |
| RAM | Memória da máquina |
| Tipo 1 | Hipervisor executado diretamente no hardware |
| Tipo 2 | Hipervisor executado sobre um sistema operacional |
| Escala vertical | Aumentar recursos da VM |
| Escala horizontal | Adicionar máquinas |
| Snapshot | Captura do estado de um disco ou volume |

---
**ORIVEX LAB — Infraestrutura e Redes**  
Trilha: Computação em Nuvem
