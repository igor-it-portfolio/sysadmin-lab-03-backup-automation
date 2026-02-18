# 🛡️ # 🛡️ SysAdmin Lab: Backup Automation & Retention Policy

Este repositório contém a solução prática do **Laboratório**, focada em automação de infraestrutura Linux.

## 📋 Descrição do Projeto
Este projeto faz parte do meu laboratório de administração de sistemas (Lab 03) e consiste em uma solução automatizada para backup e gestão de armazenamento. O script utiliza Bash para realizar sincronização incremental e compactação, garantindo a integridade dos dados e o uso eficiente do disco através de uma política de retenção automatizada.

## 🛠️ Tecnologias Utilizadas
* **Rsync**: Sincronização incremental inteligente.
* **Tar (Gzip)**: Compactação de dados para redução de custos de armazenamento.
* **Cron**: Automação de tarefas agendadas (Scheduled Tasks).
* **Bash Script**: Lógica de automação e tratamento de logs.
* **Find**: Implementação da regra de expurgo (Retenção de 7 dias).

## ⚙️ Como o Sistema Funciona
1. **Sincronização**: O script espelha os arquivos da origem para uma área de staging.
2. **Compactação**: Gera um arquivo `.tar.gz` nomeado com o timestamp da execução.
3. **Logs**: Cada etapa é registrada em um arquivo `.log` para auditoria.
4. **Limpeza Automática**: Arquivos de backup com mais de 7 dias são deletados automaticamente para preservar o espaço em disco.

## 🚀 Como Configurar
1. Clone este repositório.
2. Ajuste as variáveis de caminho no script `backup_automatico.sh`.
3. Adicione ao Crontab (`crontab -e`):
   `15 03 * * * /bin/bash /caminho/do/script.sh`

## 📸 Demonstração Visual

As evidências de execução, logs e validação do sistema de retenção podem ser encontradas na pasta de documentação do projeto:

📂 [Acessar evidências e prints (Pasta /docs)](./docs/)
