
# 01 — Fundamentos de Segurança da Informação e Redes

## 1. Objetivo

A segurança da informação busca proteger dados, sistemas, equipamentos e serviços contra acessos não autorizados, alterações indevidas, vazamentos e indisponibilidades.

Em ambientes de infraestrutura e telecomunicações, a segurança é essencial para manter a continuidade dos serviços e proteger a rede.

## 2. Tríade da Segurança da Informação (CIA)

A segurança da informação é baseada em três princípios:

| Princípio | Significado |
|---|---|
| Confidencialidade | Garantir que somente pessoas autorizadas acessem as informações |
| Integridade | Garantir que os dados não sejam alterados indevidamente |
| Disponibilidade | Garantir que sistemas e serviços estejam acessíveis quando necessários |

**Exemplo:**
- Confidencialidade: proteger credenciais de acesso.
- Integridade: impedir alterações não autorizadas nas configurações.
- Disponibilidade: manter servidores e enlaces funcionando.

## 3. Autenticação e autorização

**Autenticação:** processo de confirmar a identidade de um usuário ou dispositivo.

Exemplos:
- Senha.
- Certificado digital.
- Biometria.
- Autenticação multifator (MFA).

**Autorização:** define quais recursos e operações o usuário pode acessar após ser autenticado.

Exemplo: um técnico pode consultar informações de um equipamento, mas não necessariamente alterar sua configuração.

## 4. Princípio do menor privilégio

Cada usuário deve possuir somente as permissões necessárias para executar suas atividades.

Esse princípio reduz riscos de:
- Alterações indevidas.
- Acessos não autorizados.
- Vazamento de informações.
- Comprometimento de sistemas.

## 5. Firewall

Firewall é um mecanismo de segurança que controla o tráfego de rede conforme regras predefinidas.

Pode permitir ou bloquear conexões com base em critérios como:
- Endereço IP de origem e destino.
- Porta de comunicação.
- Protocolo.
- Direção do tráfego.

Exemplos de protocolos e portas:
- HTTP: TCP 80.
- HTTPS: TCP 443.
- SSH: TCP 22.
- DNS: UDP/TCP 53.
- SNMP: UDP 161 e 162.

## 6. VPN

VPN (Virtual Private Network) cria um túnel protegido para comunicação através de uma rede pública ou não confiável.

É utilizada para:
- Acesso remoto seguro.
- Comunicação entre unidades.
- Acesso de técnicos à infraestrutura corporativa.
- Proteção do tráfego durante a transmissão.

## 7. Principais ameaças

| Ameaça | Descrição |
|---|---|
| Malware | Software malicioso |
| Ransomware | Malware que bloqueia ou criptografa dados e exige resgate |
| Phishing | Tentativa de enganar usuários para obter informações |
| Brute force | Tentativas repetidas de descobrir credenciais |
| DDoS | Sobrecarga de um serviço por grande volume de tráfego |
| Spoofing | Falsificação de identidade ou endereço |
| Sniffing | Captura e análise do tráfego de rede |

## 8. Criptografia

A criptografia transforma informações legíveis em dados protegidos por meio de algoritmos e chaves.

Principais conceitos:

- Criptografia simétrica: utiliza a mesma chave para criptografar e descriptografar.
- Criptografia assimétrica: utiliza um par de chaves, pública e privada.
- Hash: gera um resumo de tamanho definido a partir de uma informação, sendo utilizado para verificação de integridade e armazenamento seguro de senhas, conforme o algoritmo empregado.

Exemplos:
- AES: algoritmo de criptografia simétrica.
- RSA: algoritmo de criptografia assimétrica.
- SHA-256: função hash.

## 9. Segurança em ambientes NOC e FTTH

Em uma operação NOC, a segurança deve proteger equipamentos, sistemas de monitoramento e acessos administrativos.

Boas práticas:

- Utilizar credenciais individuais.
- Não compartilhar senhas.
- Utilizar VPN para acessos remotos autorizados.
- Aplicar o princípio do menor privilégio.
- Manter sistemas e equipamentos atualizados.
- Registrar alterações na infraestrutura.
- Monitorar tentativas de acesso suspeitas.
- Proteger interfaces administrativas de OLTs, roteadores e switches.

## 10. Backup e recuperação

Backup é a cópia de segurança de dados, configurações ou sistemas.

É importante para:
- Recuperação após falhas.
- Proteção contra ransomware.
- Restauração de configurações.
- Continuidade operacional.

Uma estratégia de backup deve prever periodicidade, retenção, proteção das cópias e testes de restauração.

## 11. Conclusão

A segurança da informação é fundamental para proteger a infraestrutura de redes e garantir a continuidade dos serviços.

Em ambientes NOC, medidas como firewall, VPN, autenticação, controle de acesso, criptografia e backup ajudam a reduzir riscos e preservar a disponibilidade, a integridade e a confidencialidade dos dados.
