
# Processos e Serviços Linux

## 1. Objetivo

Documentar os principais comandos utilizados para monitorar processos, administrar serviços e consultar registros de eventos em sistemas Linux.

## 2. Conceito de processo

Um processo representa um programa em execução no sistema operacional.

Cada processo possui um identificador único chamado PID (Process ID).

## 3. Principais comandos de processos

| Comando | Finalidade |
|---|---|
| ps | Consultar processos |
| ps aux | Listar processos em execução |
| top | Monitorar processos e recursos |
| htop | Monitoramento interativo |
| kill | Enviar sinais a processos |
| pgrep | Localizar processos pelo nome |

## 4. Gerenciamento de serviços

O systemctl é utilizado para administrar serviços em sistemas que utilizam systemd.

| Comando | Finalidade |
|---|---|
| systemctl status | Consultar estado |
| systemctl start | Iniciar serviço |
| systemctl stop | Parar serviço |
| systemctl restart | Reiniciar serviço |
| systemctl enable | Habilitar inicialização automática |
| systemctl disable | Desabilitar inicialização automática |

## 5. Consulta de logs

O journalctl permite consultar registros de eventos do sistema e de serviços gerenciados pelo systemd.

Exemplos:

journalctl
journalctl -u nginx
journalctl -u nginx -f
journalctl -p err

## 6. Aplicação em infraestrutura

Esses comandos são utilizados para investigar indisponibilidade de serviços, consumo elevado de CPU e memória, falhas de processos e erros registrados pelo sistema.

## 7. Conclusão

O gerenciamento de processos, serviços e logs é fundamental para a administração de servidores Linux, monitoramento de infraestrutura e troubleshooting em ambientes NOC.
