
# Laboratório 01 — Provisionamento de Máquina Virtual na AWS

## 1. Objetivo

Provisionar uma máquina virtual na AWS utilizando Amazon EC2, instalar e configurar um servidor web Nginx e validar o funcionamento do serviço por meio de testes de conectividade HTTP e TCP.

## 2. Ambiente utilizado

| Componente | Configuração |
|---|---|
| Provedor Cloud | Amazon Web Services (AWS) |
| Serviço | Amazon EC2 |
| Instância | ORIVEX-EC2-LINUX |
| Sistema operacional | Amazon Linux 2023 |
| Tipo de instância | t3.micro |
| Região | us-east-2 |
| Acesso administrativo | AWS Systems Manager Session Manager |
| Servidor web | Nginx |
| Porta HTTP | TCP 80 |

## 3. Configuração de acesso e gerenciamento

Foi associada uma função IAM à instância EC2 para permitir o gerenciamento por meio do AWS Systems Manager.

O perfil padrão de gerenciamento de hosts (DHMC) foi habilitado na conta e região, permitindo o gerenciamento da instância pelo Systems Manager.

O agente SSM foi verificado e reiniciado:

```bash
sudo systemctl restart amazon-ssm-agent
sudo systemctl status amazon-ssm-agent --no-pager
```

Resultado: serviço ativo e em execução.

A conexão pelo Session Manager foi estabelecida com sucesso.

## 4. Instalação do Nginx

Atualização dos metadados e instalação do servidor web:

```bash
sudo dnf install nginx -y
```

Inicialização do serviço:

```bash
sudo systemctl start nginx
```

Configuração para inicialização automática:

```bash
sudo systemctl enable nginx
```

Verificação do serviço:

```bash
sudo systemctl status nginx --no-pager
```

Resultado: `active (running)`.

## 5. Publicação da página ORIVEX LAB

Foi editado o arquivo padrão do servidor web:

```bash
sudo nano /usr/share/nginx/html/index.html
```

Foi criada uma página personalizada apresentando o ambiente ORIVEX LAB, com informações sobre o sistema operacional, servidor web e infraestrutura em nuvem.

## 6. Configuração de rede

No Security Group da instância EC2, foi adicionada uma regra de entrada para permitir acesso HTTP:

| Protocolo | Porta | Origem |
|---|---|---|
| TCP | 80 | Meu IP |

O acesso externo foi validado pelo endereço IPv4 público da instância.

## 7. Testes e validações

### 7.1 Teste HTTP local

Comando:

```bash
curl -I http://localhost
```

Resultado:

```text
HTTP/1.1 200 OK
Server: nginx/1.30.7
Content-Type: text/html
```

Conclusão: o servidor web respondeu corretamente à requisição HTTP.

### 7.2 Verificação da porta TCP 80

Comando:

```bash
sudo ss -lntp | grep ':80'
```

Resultado observado:

- Estado: LISTEN
- IPv4: 0.0.0.0:80
- IPv6: [::]:80
- Processo: nginx

Conclusão: o Nginx está escutando na porta TCP 80 nas interfaces IPv4 e IPv6.

### 7.3 Teste externo

A página personalizada do ORIVEX LAB foi acessada pelo navegador utilizando o IPv4 público da instância.

Resultado: página carregada com sucesso.

## 8. Resultado final

A atividade demonstrou o provisionamento e a configuração de uma máquina virtual em ambiente de computação em nuvem.

Foram realizados procedimentos de:

- Provisionamento de infraestrutura com Amazon EC2.
- Gerenciamento de acesso utilizando IAM e Systems Manager.
- Administração de sistema operacional Linux.
- Instalação e gerenciamento de serviços.
- Configuração de regras de entrada no Security Group.
- Publicação de conteúdo por meio do Nginx.
- Diagnóstico de conectividade HTTP e TCP.

**Status do laboratório:** Concluído com sucesso.

## 9. Observação

Este laboratório foi desenvolvido em ambiente de estudo, com recursos da AWS. Os resultados representam testes realizados na instância durante a execução da atividade.

