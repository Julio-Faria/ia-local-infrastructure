# Arquitetura da solução

## Visão geral

A solução será executada em uma máquina virtual Ubuntu Server hospedada no VirtualBox. Os serviços de IA serão organizados em contêineres Docker, com armazenamento persistente para modelos, configurações e documentos.

## Fluxo de interação planejado

1. O usuário acessa a interface Open WebUI por um navegador na rede local.
2. O Open WebUI encaminha a solicitação ao serviço Ollama.
3. O Ollama executa o modelo de linguagem selecionado na CPU do servidor.
4. A resposta é devolvida à interface web.
5. Quando a base RAG estiver configurada, documentos técnicos poderão fornecer contexto adicional às respostas.

## Componentes

### Ubuntu Server

Sistema operacional da máquina virtual e base para os serviços.

### Docker Engine e Docker Compose

Camada de execução e gerenciamento dos contêineres. A configuração será documentada após a instalação e validação.

### Ollama

Runtime responsável por disponibilizar e executar modelos de linguagem localmente. O desempenho dependerá do modelo, da quantização e dos recursos de CPU e memória disponíveis.

### Open WebUI

Interface web que permitirá conversar com os modelos disponibilizados pelo Ollama.

### Base de conhecimento (RAG)

Mecanismo planejado para recuperar trechos relevantes de documentos técnicos e incluí-los como contexto nas consultas. RAG não é o mesmo que treinar ou realizar fine-tuning do modelo.

### Prometheus e Grafana

Já existem serviços de monitoramento no ambiente hospedeiro. A consulta pela IA será tratada como uma integração futura, com acesso somente ao necessário e sem expor diretamente serviços de monitoramento à rede pública.

## Rede e segurança

- A VM utilizará conectividade pela rede local.
- Os serviços web deverão exigir autenticação.
- A API do Ollama não deverá ser exposta indiscriminadamente.
- O firewall deverá permitir somente as portas e origens necessárias.
- A operação offline será validada somente depois que imagens de contêineres, modelos e dependências estiverem disponíveis localmente.

## Estado atual

A arquitetura é uma proposta de implantação. Os componentes e integrações serão marcados como concluídos somente após instalação e testes documentados.
