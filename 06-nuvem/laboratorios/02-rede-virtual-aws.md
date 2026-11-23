
# Laboratório 02 — Rede Virtual na AWS (VPC)

## 1. Objetivo

Analisar a arquitetura de rede virtual criada na AWS, identificando a VPC, sub-redes, tabela de rotas, Internet Gateway, Security Group e conectividade da instância EC2.

O laboratório demonstra conceitos práticos de redes em nuvem, segmentação de rede, roteamento e controle de tráfego.

## 2. Ambiente utilizado

| Componente | Configuração |
|---|---|
| Provedor | Amazon Web Services (AWS) |
| Região | us-east-2 (Ohio) |
| Serviço | Amazon VPC |
| Instância | ORIVEX-EC2-LINUX |
| Sistema operacional | Amazon Linux 2023 |
| Tipo da instância | t3.micro |
| Estado ao final da análise | Interrompida |

## 3. Configuração da VPC

**ID:** `vpc-0cf05e6e8a540066f`

| Propriedade | Resultado |
|---|---|
| CIDR IPv4 | 172.31.0.0/16 |
| CIDR IPv6 | Não configurado |
| Estado | Available |
| VPC padrão | Sim |
| Resolução DNS | Habilitada |
| Nomes de host DNS | Habilitados |

A VPC é a rede virtual isolada logicamente na AWS, na qual são organizados os recursos de infraestrutura.

## 4. Sub-redes identificadas

Foram identificadas três sub-redes distribuídas em diferentes zonas de disponibilidade.

| Sub-rede | CIDR IPv4 | Zona |
|---|---|---|
| subnet-0d3e5c786c747a325 | 172.31.0.0/20 | us-east-2a |
| subnet-0fc83ff0ece87ae86 | 172.31.16.0/20 | us-east-2b |
| subnet-073f416a0a8d6b480 | 172.31.32.0/20 | us-east-2c |

As sub-redes permitem segmentar a rede virtual e distribuir recursos entre zonas de disponibilidade.

## 5. Tabela de rotas

**ID:** `rtb-0f7849194583c0576`

Foram identificadas duas rotas:

| Destino | Alvo | Status |
|---|---|---|
| 172.31.0.0/16 | local | Ativo |
| 0.0.0.0/0 | Internet Gateway | Ativo |

### Interpretação

- `172.31.0.0/16`: permite comunicação interna entre os recursos da VPC.
- `0.0.0.0/0`: encaminha o tráfego destinado a redes externas para o Internet Gateway.

## 6. Associação das sub-redes

A análise identificou:

- Associações explícitas: 0.
- Sub-redes sem associação explícita: 3.
- As três sub-redes utilizam a tabela de rotas principal da VPC.

Na AWS, quando uma sub-rede não está explicitamente associada a outra tabela, ela utiliza a tabela principal da VPC.

## 7. Internet Gateway

**ID:** `igw-0485a12dd54e81d1c`

| Propriedade | Resultado |
|---|---|
| Estado | Attached |
| VPC associada | vpc-0cf05e6e8a540066f |

O Internet Gateway permite a comunicação entre a VPC e a internet, desde que existam rotas, endereços IP e regras de segurança compatíveis.

## 8. Network ACL

**ID:** `acl-02a551a03c15d107b`

A Network ACL analisada é a ACL padrão da VPC.

Foram observadas regras de entrada e saída com:
- Regra 100: permitir tráfego.
- Regra *: negar tráfego não correspondido pelas regras anteriores.

A Network ACL atua como uma camada de controle de tráfego no nível da sub-rede.

## 9. Security Group

**Nome:** `launch-wizard-1`

**ID:** `sg-0d0de6f26ada22518`

### Regras de entrada identificadas

| Serviço | Protocolo | Porta | Origem |
|---|---|---|---|
| HTTP | TCP | 80 | 201.87.251.133/32 |
| SSH | TCP | 22 | 201.87.251.133/32 |
| SSH | TCP | 22 | Lista de prefixos pl-03915406641cb1f53 |

### Regra de saída identificada

| Tipo | Protocolo | Portas | Destino |
|---|---|---|---|
| Todo o tráfego | Todos | Todas | 0.0.0.0/0 |

A regra de saída permite conexões iniciadas pela instância para qualquer destino IPv4.

O Security Group funciona como firewall virtual associado à instância ou à interface de rede.

## 10. Identificação da instância na rede

**Nome:** ORIVEX-EC2-LINUX

**ID:** `i-016875f33b297f266`

| Propriedade | Resultado |
|---|---|
| Tipo | t3.micro |
| IP privado | 172.31.45.51 |
| IP público após interrupção | Não atribuído |
| VPC | vpc-0cf05e6e8a540066f |
| Sub-rede | subnet-073f416a0a8d6b480 |
| Zona de disponibilidade | us-east-2c |
| Estado final | Interrompida |

O endereço privado `172.31.45.51` pertence ao bloco `172.31.32.0/20`.

Portanto, a instância está localizada na sub-rede da zona us-east-2c.

## 11. Teste prático de conectividade

Durante o laboratório, a instância foi iniciada para instalação e validação do servidor web Nginx.

### Instalação

```bash
sudo dnf install nginx -y
```

### Inicialização

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

### Verificação do serviço

```bash
sudo systemctl status nginx --no-pager
```

Resultado observado:

- Serviço: nginx.service
- Estado: active (running)
- Inicialização automática: enabled

### Teste HTTP local

```bash
curl -I http://localhost
```

Resultado observado:

```text
HTTP/1.1 200 OK
Server: nginx/1.30.7
Content-Type: text/html
```

O código HTTP 200 confirmou que o servidor web respondeu corretamente.

### Verificação da porta 80

```bash
sudo ss -lntp | grep ':80'
```

Resultado observado:

- Porta TCP 80 em LISTEN.
- Escuta em `0.0.0.0:80`.
- Escuta em `[::]:80`.

Isso confirmou que o Nginx estava escutando conexões HTTP nas interfaces IPv4 e IPv6 da instância.

## 12. Publicação da página ORIVEX LAB

O arquivo padrão do Nginx foi personalizado:

```bash
sudo nano /usr/share/nginx/html/index.html
```

Foi criada uma página HTML com a identificação:

- ORIVEX LAB
- Infraestrutura de Redes e Computação em Nuvem
- Servidor AWS Online
- Sistema operacional Amazon Linux 2023
- Servidor Web Nginx
- Ambiente Amazon EC2

A página foi acessada pelo navegador utilizando o endereço IPv4 público que estava atribuído à instância durante o teste.

## 13. Análise técnica da arquitetura

A infraestrutura analisada possui:

- Uma VPC com bloco IPv4 /16.
- Três sub-redes em zonas de disponibilidade distintas.
- Uma tabela de rotas principal.
- Um Internet Gateway associado à VPC.
- Uma Network ACL padrão.
- Um Security Group com regras de entrada e saída.
- Uma instância Linux executando Nginx.

As três sub-redes utilizam a tabela principal, que possui rota padrão para o Internet Gateway.

**Observação importante:** embora as três sub-redes tenham caminho de rota para o Internet Gateway, a classificação e o acesso efetivo à internet dependem também da configuração de endereços públicos, regras de segurança e demais componentes de rede.

Não foi identificada uma arquitetura de sub-redes privadas com NAT Gateway neste laboratório.

## 14. Encerramento e controle de custos

Após os testes, a instância EC2 foi interrompida.

O estado final foi confirmado como:

```text
Instance state: Stopped
```

A interrupção encerra a cobrança pelo uso computacional da instância enquanto ela permanece parada, mas o armazenamento EBS e outros recursos associados podem continuar gerando custos.

## 15. Competências praticadas

- Administração de VPC.
- Endereçamento IPv4 e CIDR.
- Segmentação de redes com sub-redes.
- Roteamento IPv4.
- Internet Gateway.
- Network ACL.
- Security Groups.
- Identificação de IP privado e público.
- Administração básica de Linux na AWS.
- Instalação e gerenciamento do Nginx.
- Diagnóstico de conectividade HTTP.
- Controle de custos de recursos em nuvem.

## 16. Conclusão

O laboratório permitiu analisar na prática os principais componentes de uma rede virtual na AWS.

Foi possível identificar a estrutura da VPC, compreender a associação das sub-redes à tabela de rotas principal, verificar o caminho para o Internet Gateway e analisar os controles de segurança.

Também foi realizada a implantação de um servidor web Nginx em uma instância Amazon EC2, com validação do serviço por meio de testes HTTP e verificação da porta TCP 80.

O ambiente foi interrompido após a conclusão dos testes.

**Projeto:** ORIVEX LAB — Infraestrutura e Redes  
**Laboratório:** 02 — Rede Virtual na AWS (VPC)
