
# Gerenciamento de Usuários e Grupos Linux

## 1. Objetivo

Documentar os conceitos e comandos utilizados para administrar usuários e grupos em sistemas Linux.

## 2. Conceitos fundamentais

- Usuários: contas que permitem acesso ao sistema.
- Grupos: agrupamentos de usuários para gerenciamento de permissões.
- Root: conta administrativa com privilégios elevados.
- UID: identificador numérico do usuário.
- GID: identificador numérico do grupo.
- Sudo: mecanismo de execução de comandos com privilégios administrativos autorizados.

## 3. Principais comandos

| Comando | Finalidade |
|---|---|
| useradd | Criar usuário |
| usermod | Modificar usuário |
| userdel | Excluir usuário |
| passwd | Alterar senha |
| groupadd | Criar grupo |
| groupdel | Excluir grupo |
| groups | Consultar grupos |
| whoami | Identificar usuário atual |
| id | Consultar UID e GID |

## 4. Arquivos importantes

| Arquivo | Finalidade |
|---|---|
| /etc/passwd | Informações das contas |
| /etc/shadow | Informações protegidas de autenticação |
| /etc/group | Informações dos grupos |

## 5. Aplicação em infraestrutura

O gerenciamento de usuários e grupos permite controlar acessos, organizar permissões e aplicar princípios de segurança em servidores Linux.

## 6. Conclusão

O controle de usuários e grupos é fundamental para a administração segura de sistemas Linux, especialmente em ambientes corporativos e de infraestrutura de TI.
