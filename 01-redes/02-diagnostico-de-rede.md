# Laboratório de Diagnóstico de Rede

## 1. Objetivo

Documentar e praticar comandos utilizados para verificar conectividade, identificar configurações de rede e diagnosticar possíveis falhas.

## 2. Comandos de diagnóstico

### 2.1 ipconfig

Exibe as configurações de rede do computador Windows.

```cmd
ipconfig
```

Para visualizar informações completas:

```cmd
ipconfig /all
```

**Informações analisadas:**
- Endereço IPv4.
- Máscara de sub-rede.
- Gateway padrão.
- Servidores DNS.

### 2.2 ping

Testa a conectividade entre dispositivos.

```cmd
ping 8.8.8.8
```

**Objetivo:** verificar se existe comunicação com o endereço de destino e analisar o tempo de resposta.

### 2.3 tracert

Identifica os saltos percorridos pelos pacotes até o destino.

```cmd
tracert 8.8.8.8
```

**Objetivo:** auxiliar na identificação de possíveis pontos de falha no caminho da comunicação.

### 2.4 nslookup

Consulta informações de resolução DNS.

```cmd
nslookup google.com
```

**Objetivo:** verificar se um nome de domínio está sendo resolvido para um endereço IP.

### 2.5 netstat

Exibe conexões de rede e portas utilizadas pelo sistema.

```cmd
netstat -ano
```

**Objetivo:** analisar conexões ativas, portas e identificadores de processos.

## 3. Atividade prática

Executar os comandos no Prompt de Comando do Windows e registrar os resultados.

| Comando | Finalidade |
|---|---|
| ipconfig | Consultar configuração IP |
| ping | Testar conectividade |
| tracert | Analisar rota |
| nslookup | Consultar DNS |
| netstat | Analisar conexões e portas |

## 4. Registro dos testes

Os resultados devem ser documentados com data, comando executado, destino, resultado observado e conclusão.

## 5. Aplicação profissional

Esses comandos são utilizados em atividades de suporte técnico, administração de redes, infraestrutura de TI e monitoramento NOC.

## 6. Observação

Laboratório didático executado em ambiente Windows. Os resultados devem ser preenchidos após a realização dos testes.

## 7. Execução prática — Teste de conectividade com o gateway

**Comando executado:**

```cmd
ping 192.168.1.1
```

**Resultados obtidos:**

| Indicador | Resultado |
|---|---:|
| Pacotes enviados | 4 |
| Pacotes recebidos | 4 |
| Pacotes perdidos | 0 |
| Perda de pacotes | 0% |
| Tempo médio | 5 ms |
| TTL | 64 |

**Análise técnica:**

O teste apresentou 100% de respostas do gateway, sem perda de pacotes. O tempo médio de resposta foi de 5 ms.

**Conclusão:**

A comunicação entre o computador e o gateway local apresentou funcionamento normal durante o teste.

**Status:** Teste executado com sucesso.

## 8. Execução prática — Teste de conectividade externa

**Comando executado:**

```cmd
ping 8.8.8.8
```

**Resultados obtidos:**

| Indicador | Resultado |
|---|---:|
| Pacotes enviados | 4 |
| Pacotes recebidos | 4 |
| Pacotes perdidos | 0 |
| Perda de pacotes | 0% |
| Latência mínima | 19 ms |
| Latência máxima | 26 ms |
| Latência média | 22 ms |

**Análise técnica:**

O destino externo respondeu às quatro solicitações ICMP. Não houve perda de pacotes durante o teste. A latência média observada foi de 22 ms.

**Conclusão:**

Foi confirmada a comunicação IP entre o computador e o destino externo durante a execução do teste.

**Status:** Teste executado com sucesso.

## 9. Execução prática — Consulta DNS

**Comando executado:**

```cmd
nslookup google.com
```

**Resultados obtidos:**

| Indicador | Resultado |
|---|---|
| Domínio | google.com |
| Servidor DNS | dns.google |
| Endereço do servidor | 2001:4860:4860::8888 |
| IPv4 retornado | 172.217.29.206 |
| IPv6 retornado | 2800:3f0:4001:81a::200e |

**Análise técnica:**

O servidor DNS respondeu à consulta e retornou registros de endereço IPv4 e IPv6. A indicação de resposta não autoritativa não representa, por si só, um erro.

**Conclusão:**

A resolução de nomes do domínio consultado apresentou funcionamento normal durante o teste.

**Status:** Teste executado com sucesso.
## 10. Execução prática — Rastreamento de rota

**Comando executado:**

```cmd
tracert 8.8.8.8
```

**Resultados obtidos:**

- Destino: dns.google (8.8.8.8)
- Total de saltos: 14
- Primeiro salto: 192.168.1.1
- Destino alcançado no salto 14
- Tempo de resposta no destino: 19 a 23 ms

**Análise técnica:**

O rastreamento identificou o gateway local no primeiro salto, seguido por equipamentos intermediários com endereços privados e públicos. O destino final foi alcançado no décimo quarto salto.

Foram observadas variações de latência em alguns saltos intermediários, sem evidência suficiente para concluir que exista congestionamento ou falha.

**Conclusão:**

A rota até o endereço 8.8.8.8 foi concluída com sucesso.

**Status:** Teste executado com sucesso.


## 11. Execução prática — Análise de conexões com NETSTAT

**Comando executado:**

```cmd
netstat -ano
```

**Objetivo:**

Identificar conexões TCP e UDP, portas em estado de escuta, conexões estabelecidas e identificadores de processos (PID).

**Resultados observados:**

- Foram identificadas portas TCP em estado LISTENING.
- Foram identificadas conexões TCP em estado ESTABLISHED.
- Foram observadas conexões em TIME_WAIT.
- Foram identificadas comunicações locais utilizando o endereço 127.0.0.1.
- Foram observadas conexões externas utilizando a porta TCP 443.
- Foram identificadas entradas UDP, incluindo as portas 5353 e 5355.

**Análise técnica:**

O resultado demonstra que o computador mantém serviços aguardando conexões e estabelece comunicações com outros dispositivos e servidores externos.

O estado LISTENING indica que uma aplicação está aguardando conexões em determinada porta. ESTABLISHED representa uma conexão TCP estabelecida. TIME_WAIT indica uma conexão encerrada que permanece temporariamente nesse estado.

O parâmetro -o permite visualizar o PID associado às conexões, possibilitando investigar qual processo está utilizando determinada porta.

**Conclusão:**

O comando NETSTAT permitiu identificar o comportamento das conexões de rede do computador, contribuindo para atividades de diagnóstico, administração e análise básica de segurança.

**Status:** Teste executado com sucesso.


## 12. Identificação de processo por PID

**Comando executado:**

```cmd
tasklist /FI "PID eq 1448"
```

**Resultado:**

- Processo identificado: chrome.exe
- PID: 1448

**Análise técnica:**

Após identificar conexões externas pelo comando NETSTAT, foi utilizado o TASKLIST para relacionar o PID 1448 ao processo chrome.exe (Google Chrome).

Essa prática permite identificar qual aplicação está utilizando determinado recurso de rede e auxilia na investigação de conexões e possíveis incidentes.

**Conclusão:**

Foi possível relacionar um processo em execução às conexões identificadas anteriormente, demonstrando a integração entre os comandos NETSTAT e TASKLIST.

**Status:** Teste executado com sucesso.


## 13. Execução prática — Identificação de processos e portas com NETSTAT

**Comando executado:**

```cmd
netstat -abno
```

**Objetivo:**

Identificar portas TCP e UDP, estados das conexões e executáveis associados aos processos que utilizam recursos de rede.

**Resultados observados:**

- Identificação do serviço RPC do Windows associado à porta 135.
- Identificação da porta 445, relacionada ao serviço SMB.
- Identificação do FortiSSLVPNdaemon.exe na porta local 8053.
- Identificação de processos do FortiClient, incluindo FortiESNAC.exe.
- Identificação do Visual Studio Code (Code.exe) com conexão externa.
- Identificação de conexões dos processos chrome.exe, msedge.exe e OneDrive.exe.
- Identificação de serviços do Windows, incluindo Dnscache e SSDPSRV.

**Análise técnica:**

A execução do NETSTAT com os parâmetros -abno permitiu visualizar os executáveis associados às conexões e portas utilizadas pelo sistema operacional.

Foi possível relacionar processos específicos aos estados das conexões, facilitando a investigação de aplicações que utilizam recursos de rede.

Também foram observadas portas em estado LISTENING, conexões ESTABLISHED e entradas UDP utilizadas por serviços de rede.

**Observação de segurança:**

A presença de uma porta em estado LISTENING não representa necessariamente uma vulnerabilidade. É necessário avaliar o serviço associado, as regras de firewall e a exposição da porta.

**Conclusão:**

O teste permitiu aprofundar a análise das conexões de rede e identificar aplicações e serviços responsáveis pela utilização de portas no Windows.

**Status:** Teste executado com sucesso.


## 14. Investigação da porta 445 — Identificação do processo

**Comando executado:**

```cmd
tasklist /FI "PID eq 4"
```

**Resultado:**

- Processo: System
- PID: 4
- Sessão: Services

**Análise técnica:**

A consulta identificou que o PID 4 pertence ao processo System, componente central do Windows.

Na análise anterior com NETSTAT, a porta TCP 445 apareceu em estado LISTENING, associada ao PID 4.

A porta 445 está relacionada ao protocolo SMB (Server Message Block), utilizado para compartilhamento de arquivos e recursos em rede.

**Conclusão:**

Foi possível relacionar a porta 445 ao processo System, demonstrando como investigar serviços e processos associados às portas do sistema operacional.

**Status:** Teste executado com sucesso.


## 15. Verificação do Firewall do Windows

**Comando executado:**

```cmd
netsh advfirewall show allprofiles
```

**Resultados observados:**

- Perfil Domínio: Ligado.
- Perfil Particular: Ligado.
- Perfil Público: Ligado.
- Política de entrada: BlockInbound.
- Política de saída: AllowOutbound.
- Gerenciamento remoto: Desabilitado.
- Registro de conexões permitidas e bloqueadas: Desabilitado.

**Análise técnica:**

A consulta confirmou que o Firewall do Windows está habilitado nos três perfis de rede.

A política padrão bloqueia conexões de entrada e permite conexões de saída, respeitando as regras de firewall configuradas.

Também foi observada uma indicação de gerenciamento de regras por política de grupo (GPO).

**Conclusão:**

A verificação permitiu analisar o estado do firewall e identificar as políticas básicas de proteção de tráfego de entrada e saída.

**Status:** Teste executado com sucesso.


## 16. Análise das regras do Firewall do Windows

**Comando executado:**

```cmd
netsh advfirewall firewall show rule name=all
```

**Objetivo:**

Consultar as regras de entrada e saída configuradas no Firewall do Windows.

**Resultados observados:**

- Foram identificadas regras habilitadas e desabilitadas.
- Foram encontradas regras relacionadas a DHCP, mDNS e Wi-Fi Direct.
- Foram identificadas regras de descoberta de rede.
- Foram observadas regras relacionadas a SNMP e LLMNR desabilitadas.
- Foram identificadas regras de gerenciamento remoto desabilitadas.

**Análise técnica:**

A consulta permitiu visualizar as políticas de comunicação do Firewall do Windows, incluindo direção do tráfego, protocolos, perfis de rede e ações permitidas.

**Conclusão:**

A análise das regras contribuiu para compreender como o firewall controla as comunicações de entrada e saída e como diferentes serviços de rede possuem regras específicas.

**Status:** Consulta executada com sucesso.
## 17. Análise detalhada das regras do Visual Studio Code

Foi realizada a consulta detalhada das regras de firewall associadas ao Visual Studio Code.

Comando utilizado:

netsh advfirewall firewall show rule name="Visual Studio Code" verbose

Resultados identificados:

- Existem duas regras habilitadas.
- Uma regra permite conexões de entrada TCP.
- Outra regra permite conexões de entrada UDP.
- Ambas estão associadas ao executável Code.exe.
- As duas regras estão configuradas para o perfil Público.
- Endereços IP e portas estão definidos como Qualquer.
- A ação configurada é Permitir.

Análise técnica:

As regras autorizam tráfego de entrada destinado ao Visual Studio Code no perfil de rede pública. Essa configuração merece revisão, principalmente em redes públicas, mas não comprova, isoladamente, uma exposição ou invasão.

Próxima etapa:
Verificar a necessidade dessas permissões conforme os recursos utilizados no Visual Studio Code, antes de realizar qualquer alteração.