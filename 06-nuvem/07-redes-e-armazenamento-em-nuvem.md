
# 07 — Redes e Armazenamento em Nuvem

## 1. Introdução

A infraestrutura em nuvem depende de serviços de rede e armazenamento para permitir a comunicação entre recursos computacionais e guardar dados e aplicações.

O planejamento desses componentes é essencial para garantir desempenho, segurança, disponibilidade e escalabilidade.

## 2. Redes virtuais

As redes virtuais permitem organizar e controlar a comunicação entre máquinas virtuais, aplicações e outros recursos em nuvem.

Principais componentes:

- **VPC (AWS):** rede virtual isolada.
- **VNet (Azure):** rede virtual no ambiente Azure.
- **Subnet:** divisão lógica de uma rede.
- **IP privado:** endereço utilizado na comunicação interna.
- **IP público:** endereço utilizado para comunicação com redes externas.
- **Route Table:** define os caminhos que o tráfego de rede deve seguir.
- **Gateway:** permite comunicação entre redes diferentes.

## 3. Conectividade em nuvem

A comunicação entre ambientes locais e nuvem pode ocorrer por diferentes tecnologias.

### VPN

Cria um túnel criptografado através de uma rede pública, permitindo comunicação segura entre ambientes.

Exemplo: conectar a rede corporativa de uma empresa a uma VPC na AWS.

### Conexão dedicada

Permite estabelecer conectividade privada entre a infraestrutura local e o provedor de nuvem.

Exemplos:
- AWS Direct Connect.
- Azure ExpressRoute.

## 4. Segurança de rede

A proteção da infraestrutura em nuvem envolve:

- Firewalls.
- Security Groups.
- Network ACLs.
- Network Security Groups (NSG).
- Controle de portas e protocolos.
- Segmentação de redes.
- Monitoramento do tráfego.

O acesso deve seguir o princípio do menor privilégio.

## 5. Tipos de armazenamento

### Armazenamento em bloco

Os dados são organizados em blocos e apresentados como volumes para servidores e máquinas virtuais.

Exemplos:
- AWS EBS.
- Azure Managed Disks.

Aplicações:
- Discos de máquinas virtuais.
- Bancos de dados.
- Sistemas operacionais.

### Armazenamento de arquivos

Organiza dados em arquivos e diretórios, permitindo compartilhamento entre sistemas.

Exemplos:
- Amazon EFS.
- Azure Files.

Aplicações:
- Compartilhamento de arquivos.
- Diretórios corporativos.
- Dados compartilhados entre servidores.

### Armazenamento de objetos

Armazena dados como objetos, normalmente com metadados e identificadores próprios.

Exemplos:
- Amazon S3.
- Azure Blob Storage.

Aplicações:
- Backups.
- Imagens.
- Vídeos.
- Logs.
- Arquivos não estruturados.

## 6. Comparação dos tipos de armazenamento

| Tipo | Organização | Aplicação |
|---|---|---|
| Bloco | Blocos e volumes | Discos de servidores |
| Arquivo | Arquivos e diretórios | Compartilhamento |
| Objeto | Objetos e metadados | Backup e arquivos |

## 7. Backup, snapshots e replicação

### Backup

Cópia de segurança utilizada para recuperar dados após perda, falha ou incidente.

### Snapshot

Captura do estado de um volume ou recurso em determinado momento, conforme as características do serviço.

### Replicação

Processo de manter cópias de dados em outro local ou ambiente para aumentar a disponibilidade e apoiar a recuperação.

## 8. RAID e armazenamento

RAID é uma tecnologia que combina discos para obter diferentes níveis de desempenho, capacidade ou redundância.

Exemplos:

- RAID 0: distribuição de dados (striping), sem redundância.
- RAID 1: espelhamento (mirroring).
- RAID 5: distribuição com paridade.
- RAID 6: distribuição com dupla paridade.
- RAID 10: combinação de espelhamento e distribuição.

RAID não substitui backup.

## 9. Disponibilidade e desempenho

O planejamento do armazenamento deve considerar:

- Capacidade.
- Latência.
- IOPS.
- Throughput.
- Redundância.
- Replicação.
- Política de retenção.
- Recuperação de dados.

## 10. Aplicação em infraestrutura e operação

O profissional de infraestrutura deve saber:

- Planejar redes virtuais.
- Configurar sub-redes e rotas.
- Administrar conectividade VPN.
- Controlar tráfego de rede.
- Escolher o tipo de armazenamento adequado.
- Configurar backup e recuperação.
- Monitorar capacidade e desempenho.

## 11. Resumo para revisão

- VPC/VNet: rede virtual.
- Subnet: divisão lógica da rede.
- VPN: túnel criptografado.
- Direct Connect/ExpressRoute: conectividade dedicada.
- Bloco: volumes para servidores.
- Arquivo: compartilhamento em diretórios.
- Objeto: armazenamento de dados como objetos.
- Backup: cópia de segurança.
- Snapshot: captura de estado.
- Replicação: manutenção de cópias em outro local.
- RAID: organização de discos para desempenho ou redundância.

---
**ORIVEX LAB — Infraestrutura e Redes**  
Trilha: Computação em Nuvem
