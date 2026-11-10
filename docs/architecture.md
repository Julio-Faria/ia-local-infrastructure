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
### Ubuntu Server 26.04.1 LTS
Sistema operacional instalado na máquina virtual. O acesso administrativo remoto por SSH está disponível. A rede está atualmente configurada em modo Bridge com obtenção de endereço via DHCP; a configuração de IP estático foi deixada de lado durante a implantação.

### Docker Engine e Docker Compose
Instalados a partir do repositório oficial do Docker para Ubuntu.
- Docker Engine: 29.9.3.
- Docker Compose plugin: 5.7.0.
- containerd: 2.4.2.

O serviço Docker está ativo e habilitado para iniciar automaticamente. A validação de execução de contêineres e persistência ainda será realizada.

### Ollama
Runtime responsável por disponibilizar e executar modelos de linguagem localmente. O desempenho dependerá do modelo, da quantização e dos recursos de CPU e memória disponíveis. Instalação pendente.

### Open WebUI
Interface web que permitirá conversar com os modelos disponibilizados pelo Ollama. Instalação pendente.

### Base de conhecimento (RAG)
Mecanismo planejado para recuperar trechos relevantes de documentos técnicos e incluí-los como contexto nas consultas. RAG não é o mesmo que treinar ou realizar fine-tuning do modelo.

### Prometheus e Grafana
Já existem serviços de monitoramento no ambiente hospedeiro. A consulta pela IA será tratada como uma integração futura, com acesso somente ao necessário e sem expor diretamente serviços de monitoramento à rede pública.

## Rede e segurança
- A VM utiliza conectividade pela rede local, por adaptador Bridge e DHCP neste estágio.
- Os serviços web deverão exigir autenticação.
- A API do Ollama não deverá ser exposta indiscriminadamente.
- O firewall deverá permitir somente as portas e origens necessárias.
- A operação offline será validada somente depois que imagens de contêineres, modelos e dependências estiverem disponíveis localmente.

## Estado atual
Ubuntu Server 26.04.1 LTS e plataforma Docker estão instalados. O serviço Docker foi verificado como ativo; as versões do Engine, cliente e Compose foram conferidas. A instalação dos componentes de IA e as validações de contêineres, armazenamento persistente, segurança e operação offline permanecem pendentes.