# IA Local para Infraestrutura de TI

Projeto de construção e documentação de uma plataforma de Inteligência Artificial executada localmente, com foco em apoio a atividades de infraestrutura de Tecnologia da Informação.

A proposta é manter os modelos e os dados sob controle da infraestrutura local, permitindo consultas pela rede interna e, após a preparação e validação dos componentes, operação sem dependência de conexão com a internet.

> **Status:** em implantação. O ambiente Ubuntu Server está sendo preparado. Os componentes listados como planejados ainda não devem ser considerados instalados ou validados.

## Objetivos

- Executar modelos de linguagem localmente.
- Disponibilizar uma interface web para interação com a IA.
- Criar uma base de conhecimento com documentação técnica.
- Documentar instalação, configuração, operação, segurança e manutenção.
- Em uma etapa futura, integrar consultas controladas às métricas do Prometheus e do Grafana.

## Arquitetura planejada

| Componente | Responsabilidade | Situação |
|---|---|---|
| Ubuntu Server 24.04 LTS | Sistema operacional da máquina virtual | Em implantação |
| Docker Engine e Docker Compose | Execução e gerenciamento dos serviços | Planejado |
| Ollama | Execução local dos modelos de IA | Planejado |
| Open WebUI | Interface web para interação com os modelos | Planejado |
| Base de conhecimento (RAG) | Recuperação de conteúdo de documentos técnicos | Planejado |
| Prometheus e Grafana | Monitoramento e visualização de métricas existentes | Integração futura |

## Ambiente de laboratório

A implantação está sendo realizada em uma máquina virtual no Oracle VirtualBox, hospedada em um computador físico.

Configuração inicial planejada para a VM:

- Sistema: Ubuntu Server 24.04 LTS
- Memória RAM: 8 GB
- Processadores virtuais: 2 vCPUs
- Disco virtual: aproximadamente 100 GB
- Rede: adaptador em modo Bridge

Os endereços IP, nomes de dispositivos, credenciais, tokens e demais dados privados do ambiente não são publicados neste repositório.

## Estrutura da documentação

- [Arquitetura](docs/architecture.md)
- [Progresso da implantação](docs/progress.md)

## Segurança

- Não armazene senhas, tokens, chaves privadas ou arquivos de configuração com segredos neste repositório.
- Não publique logs que contenham dados pessoais, endereços internos ou informações operacionais sensíveis.
- Restrinja o acesso aos serviços à rede necessária.
- Faça backup dos volumes persistentes e dos documentos utilizados pela base de conhecimento.
- Revise os arquivos antes de cada publicação.

## Princípio de documentação

Este repositório diferencia claramente o que está **implantado**, **em andamento** e **planejado**. Uma etapa só será marcada como concluída depois de testada no ambiente.

## Licença

Ainda não definida.
