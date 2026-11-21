
# 01 — Fundamentos de Automação com Python

## 1. Objetivo

A automação de infraestrutura consiste em utilizar ferramentas e scripts para executar tarefas repetitivas de forma padronizada, reduzindo o trabalho manual e aumentando a eficiência operacional.

Em ambientes NOC, a automação pode auxiliar no monitoramento, diagnóstico de redes, coleta de informações e geração de relatórios.

## 2. O que é Python?

Python é uma linguagem de programação de alto nível, conhecida pela sintaxe simples e pela ampla utilização em automação, análise de dados, desenvolvimento e administração de sistemas.

Principais características:

- Sintaxe simples e legível.
- Linguagem interpretada.
- Multiplataforma.
- Grande quantidade de bibliotecas.
- Utilizada em automação de redes e infraestrutura.

## 3. Aplicações em infraestrutura e redes

Python pode ser utilizado para:

- Automatizar testes de conectividade.
- Verificar disponibilidade de equipamentos.
- Consultar endereços IP.
- Coletar informações de dispositivos.
- Analisar arquivos de log.
- Gerar relatórios operacionais.
- Automatizar tarefas administrativas.
- Identificar falhas recorrentes.

## 4. Estruturas fundamentais

### Variáveis

Armazenam informações utilizadas pelo programa.

Exemplo:

```python
equipamento = "OLT"
ip = "192.168.1.10"
disponibilidade = True
```

### Condicionais

Permitem executar ações diferentes conforme uma condição.

Exemplo:

```python
if disponibilidade:
    print("Equipamento disponível")
else:
    print("Equipamento indisponível")
```

### Laços de repetição

Permitem executar uma tarefa várias vezes.

Exemplo:

```python
equipamentos = ["OLT", "SWITCH", "ROTEADOR"]

for equipamento in equipamentos:
    print(equipamento)
```

### Funções

Permitem organizar e reutilizar blocos de código.

Exemplo:

```python
def verificar_equipamento(nome):
    print(f"Verificando: {nome}")

verificar_equipamento("OLT")
```

## 5. Bibliotecas utilizadas em automação

| Biblioteca | Aplicação |
|---|---|
| os | Interação com recursos do sistema operacional |
| subprocess | Execução de comandos externos |
| socket | Comunicação de rede |
| requests | Requisições HTTP |
| pandas | Análise e manipulação de dados |
| paramiko | Conexões SSH |
| netmiko | Automação de equipamentos de rede |

## 6. Automação de monitoramento

Um script pode verificar se determinado equipamento responde a uma solicitação de rede.

Exemplo conceitual:

```python
import subprocess

ip = "8.8.8.8"

resultado = subprocess.run(
    ["ping", "-n", "1", ip],
    capture_output=True,
    text=True
)

if resultado.returncode == 0:
    print("Equipamento ou destino respondeu")
else:
    print("Destino sem resposta")
```

Observação: o parâmetro `-n` é utilizado no Windows. Em sistemas Linux, normalmente utiliza-se `-c`.

## 7. Automação em ambientes NOC/FTTH

Exemplos de aplicações:

**Monitoramento de equipamentos**
- Verificar disponibilidade de OLTs, switches e roteadores.
- Identificar equipamentos sem resposta.

**Diagnóstico**
- Automatizar testes de ping.
- Verificar conectividade entre equipamentos.
- Coletar informações de interfaces.

**Análise de incidentes**
- Processar arquivos de log.
- Identificar mensagens de erro.
- Agrupar ocorrências por equipamento.

**Relatórios**
- Gerar relatórios de disponibilidade.
- Organizar informações de incidentes.
- Consolidar indicadores operacionais.

## 8. Benefícios da automação

- Redução de tarefas manuais.
- Economia de tempo.
- Padronização de procedimentos.
- Redução de erros operacionais.
- Maior produtividade.
- Facilidade na análise de grandes volumes de informações.
- Agilidade na identificação de falhas.

## 9. Cuidados na automação

A automação deve ser desenvolvida com controle e segurança.

Boas práticas:

- Não armazenar senhas diretamente no código.
- Utilizar controle de acesso.
- Registrar as ações executadas.
- Tratar erros e exceções.
- Validar os resultados antes de executar mudanças.
- Evitar alterações automáticas sem autorização.
- Documentar os scripts desenvolvidos.

## 10. Conclusão

A automação com Python é uma competência importante para profissionais de infraestrutura e redes.

Em operações NOC, permite automatizar verificações, coletar informações, analisar logs e gerar relatórios, contribuindo para uma operação mais eficiente, padronizada e confiável.
```
