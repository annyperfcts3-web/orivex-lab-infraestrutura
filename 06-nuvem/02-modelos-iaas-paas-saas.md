
# 02 — Modelos de Serviço em Nuvem: IaaS, PaaS e SaaS

## 1. Introdução

A computação em nuvem oferece diferentes modelos de serviços. Os três principais são:

- IaaS — Infrastructure as a Service (Infraestrutura como Serviço).
- PaaS — Platform as a Service (Plataforma como Serviço).
- SaaS — Software as a Service (Software como Serviço).

A principal diferença entre eles está no nível de gerenciamento e responsabilidade do provedor e do cliente.

## 2. IaaS — Infraestrutura como Serviço

O IaaS fornece recursos básicos de infraestrutura computacional pela internet.

O cliente pode contratar e configurar:

- Máquinas virtuais.
- Processamento (CPU).
- Memória RAM.
- Armazenamento.
- Redes virtuais.
- Sistemas operacionais.

**Responsabilidade do cliente:** administrar o sistema operacional, aplicações, dados, configurações e controles de acesso, conforme o serviço contratado.

**Exemplo:** criar uma máquina virtual Linux na AWS EC2 ou uma VM no Azure Virtual Machines.

Aplicação em infraestrutura:
- Instalação e administração de servidores.
- Configuração de endereçamento IP.
- Gerenciamento de discos.
- Configuração de firewall.
- Monitoramento de recursos.

## 3. PaaS — Plataforma como Serviço

O PaaS fornece uma plataforma gerenciada para desenvolver, executar e disponibilizar aplicações.

O provedor administra a infraestrutura e boa parte do ambiente operacional.

O cliente concentra-se principalmente em:

- Desenvolvimento de aplicações.
- Configuração do ambiente.
- Gerenciamento dos dados.
- Implantação e manutenção do código.

**Exemplo:** Azure App Service e Google App Engine.

Aplicação em infraestrutura:
- Hospedagem de aplicações.
- Publicação de sistemas.
- Gerenciamento de ambientes de desenvolvimento.
- Redução da administração direta de servidores.

## 4. SaaS — Software como Serviço

O SaaS disponibiliza aplicações prontas para utilização pela internet.

O provedor administra a infraestrutura, a plataforma e o próprio software.

O usuário utiliza o serviço e gerencia configurações e dados sob sua responsabilidade.

**Exemplos:**
- Microsoft 365.
- Google Workspace.
- Salesforce.

Aplicação:
- Correio eletrônico corporativo.
- Ferramentas de colaboração.
- Sistemas de gestão empresarial.
- Aplicações acessadas pelo navegador.

## 5. Comparação entre os modelos

| Característica | IaaS | PaaS | SaaS |
|---|---|---|---|
| Infraestrutura física | Provedor | Provedor | Provedor |
| Sistema operacional | Cliente | Provedor | Provedor |
| Plataforma de execução | Cliente | Provedor | Provedor |
| Aplicação | Cliente | Cliente | Provedor |
| Uso principal | Infraestrutura | Desenvolvimento | Utilização de software |

*Observação: a divisão exata de responsabilidades pode variar conforme o serviço contratado.*

## 6. Diferença prática

Imagine uma empresa que precisa disponibilizar um sistema:

- **IaaS:** contrata uma máquina virtual e administra o servidor e a aplicação.
- **PaaS:** publica a aplicação em uma plataforma gerenciada.
- **SaaS:** utiliza um software pronto, sem administrar sua infraestrutura.

## 7. Modelo de responsabilidade compartilhada

Na nuvem, segurança e administração são responsabilidades divididas entre o provedor e o cliente.

O provedor protege os componentes sob sua gestão. O cliente continua responsável por aspectos como dados, identidades, permissões e configurações que estejam sob seu controle.

O nível de responsabilidade do cliente geralmente é maior no IaaS e menor no SaaS.

## 8. Relação com infraestrutura e operação

O profissional de infraestrutura precisa compreender esses modelos para:

- Escolher soluções adequadas às necessidades da organização.
- Administrar máquinas virtuais e sistemas.
- Entender os limites de responsabilidade do provedor.
- Planejar segurança e disponibilidade.
- Controlar recursos e custos.

## 9. Resumo para revisão

- IaaS: infraestrutura computacional como serviço.
- PaaS: plataforma gerenciada para desenvolvimento e execução.
- SaaS: software pronto disponibilizado como serviço.
- IaaS oferece maior controle ao cliente.
- SaaS exige menor administração direta de infraestrutura pelo cliente.
- O modelo de responsabilidade compartilhada deve ser considerado em todos os modelos.

---
**ORIVEX LAB — Infraestrutura e Redes**  
Trilha: Computação em Nuvem
