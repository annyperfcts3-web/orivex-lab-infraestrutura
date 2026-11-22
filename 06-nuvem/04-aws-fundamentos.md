
# 04 — Fundamentos da Amazon Web Services (AWS)

## 1. Introdução

A Amazon Web Services (AWS) é uma plataforma de computação em nuvem que oferece serviços de infraestrutura, armazenamento, redes, bancos de dados, segurança e monitoramento.

A plataforma permite provisionar recursos computacionais sob demanda, conforme as necessidades de cada organização.

## 2. Principais serviços AWS

### Amazon EC2 — Elastic Compute Cloud

Serviço utilizado para criar e executar máquinas virtuais na nuvem.

Aplicações:
- Hospedagem de servidores Linux e Windows.
- Execução de aplicações.
- Administração de ambientes computacionais.
- Dimensionamento de recursos de processamento e memória.

### Amazon S3 — Simple Storage Service

Serviço de armazenamento de objetos.

Aplicações:
- Armazenamento de arquivos.
- Backup.
- Armazenamento de logs.
- Distribuição de conteúdo.

### Amazon VPC — Virtual Private Cloud

Permite criar uma rede virtual isolada dentro da AWS.

Componentes:
- VPC.
- Sub-redes.
- Tabelas de rotas.
- Internet Gateway.
- Security Groups.
- Network ACLs.

### AWS IAM — Identity and Access Management

Serviço de gerenciamento de identidades e permissões.

Permite:
- Criar usuários e grupos.
- Definir políticas de acesso.
- Criar funções (roles).
- Aplicar o princípio do menor privilégio.
- Controlar o acesso aos serviços AWS.

### Amazon CloudWatch

Serviço de monitoramento de recursos e aplicações.

Permite:
- Coletar métricas.
- Consultar logs.
- Configurar alarmes.
- Acompanhar desempenho e disponibilidade.

## 3. Regiões e zonas de disponibilidade

### Região (Region)

Área geográfica onde a AWS mantém sua infraestrutura de nuvem.

### Zona de disponibilidade (Availability Zone)

Localização isolada dentro de uma região, composta por uma ou mais instalações de infraestrutura.

A utilização de múltiplas zonas pode aumentar a disponibilidade e a tolerância a falhas de aplicações.

## 4. Infraestrutura como serviço na AWS

Com serviços como Amazon EC2, o profissional pode:

- Provisionar máquinas virtuais.
- Escolher sistemas operacionais.
- Configurar CPU e memória.
- Associar volumes de armazenamento.
- Configurar conectividade de rede.
- Controlar regras de acesso.
- Monitorar o funcionamento dos recursos.

## 5. Segurança na AWS

A segurança deve considerar:

- Gerenciamento de identidade e acesso (IAM).
- Autenticação multifator (MFA).
- Políticas de permissões.
- Criptografia de dados.
- Segurança de rede.
- Monitoramento de atividades.
- Backup e recuperação.

## 6. Modelo de responsabilidade compartilhada

A AWS é responsável pela segurança da infraestrutura física e dos componentes que administra.

O cliente é responsável pela segurança dos recursos e configurações sob seu controle, como permissões, dados e configurações de sistemas, de acordo com o serviço utilizado.

## 7. Aplicação em infraestrutura e operação

O profissional de infraestrutura pode utilizar a AWS para:

- Criar servidores virtuais.
- Configurar redes e sub-redes.
- Administrar armazenamento.
- Gerenciar usuários e permissões.
- Monitorar métricas e alarmes.
- Planejar disponibilidade.
- Automatizar tarefas operacionais.

## 8. Resumo para revisão

| Serviço | Função |
|---|---|
| EC2 | Máquinas virtuais |
| S3 | Armazenamento de objetos |
| VPC | Rede virtual |
| IAM | Identidade e permissões |
| CloudWatch | Monitoramento |
| Region | Região geográfica |
| Availability Zone | Zona de disponibilidade |

---
**ORIVEX LAB — Infraestrutura e Redes**  
Trilha: Computação em Nuvem
