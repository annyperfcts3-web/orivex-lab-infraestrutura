
# Permissões de Arquivos e Diretórios Linux

## 1. Objetivo

Documentar os mecanismos de controle de acesso a arquivos e diretórios no Linux.

## 2. Categorias de usuários

- u (User): proprietário.
- g (Group): grupo.
- o (Others): demais usuários.

## 3. Tipos de permissões

| Permissão | Significado | Valor |
|---|---|---:|
| r | Leitura | 4 |
| w | Escrita | 2 |
| x | Execução | 1 |

## 4. Comando chmod

Utilizado para modificar permissões.

Exemplo:

chmod 755 arquivo.sh

Interpretação:

- Proprietário: leitura, escrita e execução.
- Grupo: leitura e execução.
- Outros: leitura e execução.

Outros exemplos:

- chmod 777: acesso total para todos.
- chmod 644: proprietário lê e escreve; demais apenas leem.
- chmod 700: acesso total somente para o proprietário.
- chmod 755: proprietário tem acesso total; demais leem e executam.

## 5. Comando chown

Utilizado para alterar o proprietário e o grupo de arquivos e diretórios.

Exemplo:

chown anny:infraestrutura arquivo.txt

## 6. Comando ls -l

Utilizado para visualizar permissões, proprietário, grupo, tamanho e data de modificação.

## 7. Aplicação em infraestrutura

O gerenciamento de permissões é fundamental para proteger arquivos, restringir acessos indevidos e manter a segurança de servidores Linux.

## 8. Conclusão

O conhecimento de chmod, chown e das permissões rwx é essencial para a administração e segurança de sistemas Linux.
