
# 05 — Fundamentos Microsoft Azure

## 1. Introdução

O Microsoft Azure é uma plataforma de computação em nuvem da Microsoft. Oferece serviços de processamento, armazenamento, redes, bancos de dados, segurança e monitoramento.

É utilizado por organizações para hospedar aplicações, administrar servidores e integrar ambientes locais com recursos em nuvem.

## 2. Principais serviços do Azure

### Azure Virtual Machines

Serviço de criação e execução de máquinas virtuais.

Aplicações:
- Hospedagem de servidores Windows e Linux.
- Execução de aplicações.
- Administração de sistemas operacionais.
- Dimensionamento de CPU e memória.

### Azure Virtual Network (VNet)

Permite criar redes virtuais isoladas no Azure.

Componentes:
- Redes virtuais.
- Sub-redes.
- Tabelas de rotas.
- Peering de redes.
- Network Security Groups (NSG).

### Azure Blob Storage

Serviço de armazenamento de objetos.

Aplicações:
- Armazenamento de arquivos.
- Backup.
- Logs.
- Dados não estruturados.

### Microsoft Entra ID

Serviço de gerenciamento de identidades e acesso.

Permite:
- Gerenciar usuários e grupos.
- Controlar autenticação.
- Aplicar políticas de acesso.
- Configurar autenticação multifator (MFA).
- Integrar identidades corporativas.

### Azure Monitor

Serviço de monitoramento de recursos e aplicações.

Permite:
- Coletar métricas.
- Consultar logs.
- Configurar alertas.
- Analisar desempenho.
- Acompanhar disponibilidade.

## 3. Organização da infraestrutura Azure

### Região (Region)

Área geográfica onde os recursos do Azure são disponibilizados.

### Zona de disponibilidade (Availability Zone)

Localização fisicamente separada dentro de uma região, projetada para aumentar a resiliência dos serviços.

### Grupo de recursos (Resource Group)

Contêiner lógico utilizado para organizar e administrar recursos do Azure.

## 4. Redes no Azure

A infraestrutura de redes permite:

- Criar redes virtuais.
- Dividir redes em sub-redes.
- Configurar regras de segurança.
- Estabelecer comunicação entre redes.
- Conectar ambientes locais à nuvem.

### Network Security Group (NSG)

Controla o tráfego de entrada e saída de recursos associados, utilizando regras de segurança.

## 5. Segurança e identidade

O gerenciamento de segurança envolve:

- Microsoft Entra ID.
- Controle de acesso baseado em funções (RBAC).
- Autenticação multifator (MFA).
- Políticas de acesso.
- Proteção de dados.
- Monitoramento de atividades.

## 6. Aplicação em infraestrutura e operação

O profissional de infraestrutura pode utilizar o Azure para:

- Administrar máquinas virtuais.
- Configurar redes virtuais.
- Gerenciar armazenamento.
- Controlar identidades e permissões.
- Monitorar recursos.
- Integrar infraestrutura local e nuvem.

## 7. Comparação AWS e Azure

| Função | AWS | Azure |
|---|---|---|
| Máquina virtual | EC2 | Virtual Machines |
| Rede virtual | VPC | Virtual Network |
| Armazenamento de objetos | S3 | Blob Storage |
| Identidade e acesso | IAM | Microsoft Entra ID |
| Monitoramento | CloudWatch | Azure Monitor |

## 8. Resumo para revisão

- Azure Virtual Machines: máquinas virtuais.
- Virtual Network: redes virtuais.
- Blob Storage: armazenamento de objetos.
- Microsoft Entra ID: gerenciamento de identidades.
- Azure Monitor: monitoramento.
- Resource Group: organização lógica dos recursos.
- NSG: controle de tráfego de rede.
- RBAC: controle de acesso baseado em funções.

---
**ORIVEX LAB — Infraestrutura e Redes**  
Trilha: Computação em Nuvem
