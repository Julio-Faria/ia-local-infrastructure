# Progresso da implantação

Este documento acompanha as etapas do laboratório. O estado deve ser atualizado com base em verificações realizadas no servidor.

## Preparação da máquina virtual
- [x] Criar VM no Oracle VirtualBox.
- [x] Definir Ubuntu Server 26.04.1 LTS como sistema operacional.
- [x] Configurar 8 GB de RAM, 2 vCPUs e disco virtual de aproximadamente 100 GB.
- [x] Configurar adaptador de rede em modo Bridge.
- [x] Concluir a instalação do Ubuntu Server 26.04.1 LTS.
- [x] Atualizar a lista de pacotes e aplicar as atualizações disponíveis.
- [x] Validar acesso SSH e conectividade de rede via DHCP.
- [ ] Validar armazenamento e demais parâmetros operacionais.

## Plataforma de contêineres
- [x] Configurar o repositório oficial do Docker para Ubuntu.
- [x] Instalar Docker Engine (29.9.3).
- [x] Instalar Docker Compose plugin (5.7.0).
- [x] Verificar containerd (2.4.2).
- [x] Confirmar que o serviço Docker está ativo e habilitado na inicialização.
- [ ] Executar contêiner de teste e validar persistência dos contêineres.

## Inteligência artificial local
- [ ] Instalar Ollama.
- [ ] Baixar e avaliar um modelo compatível com os recursos disponíveis.
- [ ] Instalar Open WebUI.
- [ ] Validar comunicação entre Open WebUI e Ollama.
- [ ] Configurar autenticação e armazenamento persistente.

## Base de conhecimento
- [ ] Configurar recuperação aumentada por geração (RAG).
- [ ] Adicionar documentos técnicos não confidenciais.
- [ ] Testar recuperação, relevância e referências às fontes.

## Monitoramento e operação
- [ ] Planejar integração controlada com Prometheus.
- [ ] Validar consultas de métricas sem conceder permissões desnecessárias.
- [ ] Definir backups e procedimento de restauração.
- [ ] Testar funcionamento sem acesso à internet.

## Registro de alterações
### 2026-11-10
- Ubuntu Server 26.04.1 LTS instalado e atualizado.
- Acesso SSH validado.
- Rede mantida em modo Bridge com DHCP durante a implantação; a tentativa de IP estático foi revertida para preservar a conectividade.
- Repositório oficial do Docker configurado.
- Docker Engine 29.9.3, Docker Compose plugin 5.7.0 e containerd 2.4.2 instalados.
- Serviço Docker verificado como ativo e habilitado na inicialização.
- Cliente e servidor Docker verificados com docker version.

As etapas concluídas devem ser acompanhadas de evidências de teste, sem incluir credenciais, dados pessoais ou informações privadas da rede.