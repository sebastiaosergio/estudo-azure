# Bancos de dados #

Azure fornece uma gama de possibilidades para armazenamento e uso dos dados. Entre eles estão:
`Azure CosmoDB`, `SQL do Azure (SQLServer)`, `Intancia gerenciada SQL`, `Azure para MySQL`, `Azure para Postgree` (com `Citrus` - escalabilidade horizontal - tecnologia disponível para o Postgree).

Para cada necessidade existe uma solução em bancos de dados. Destaca-se o `CosmoDB` que é um banco noSQL que permite a ***conexão via api*** por diversas ferramentas, como Mongo, Cassandra etc.

# Big Data #

Microsoft Azure fornece diversas possiblidades para a análise e armazenamento de grandes massas de dados não padronizados e de diversas fontes e origens.

Entre elas: `Azure Synapse Analytics`, `Azure HDInsight`, `Azure Databricks` e `Azure Data Lake Analytics`.

# Serviços de Computação ##

## Máquinas Virtuais do Azure ##

São virtualizações de uma máquina para uso exclusivo e com total controle de gerenciamento dos recursos e capacidades da máquina.

**Quando usar?**
- Controle total sobre o SO (sistema operacional).
- Capacidade para executar um software personalizado.
- Usar configurações personalizadas de hospedagem.

As VMs são pre-configuradas em imagens. Sendo necessário selecionar qual imagem deseja na configuração inicial da sua VM. 

Em casos de uma migração da rede local para a nuvem, pode-se utilizar um rede privada e VMs integradas. Fornecendo assim a mesma experiência de uma rede local corporativa.

Em casos de aplicações como o SharePoint pode-se fazer a migração para a cloud, utilizando VMs pré-configuradas.

Caso queira migrar um servidor local para a nuvem pode-se utilizar o procesos de lift-and-shift. Nesse caso cria-se uma imagem do seu servidor local e executa essa imagem em uma VM, fornecendo assim a mesma estrutura lógica na VM criada. Migração rápida e mais simplificada.

Pode-se criar também um conjunto de dimensionamento de VM. Nesse caso serão um grupo de VMs já preconfiguradas e que serão "dimensionados" conforme a necessidade, replicando entre as VM as configurações definidas.

Também possui a opção de Lotes. No caso dos Lotes serão levantadas uma série de VMS e configuradas todas com a estrutura definidas, após a carga de trabalho for sendo concluídas as máquinas serão descartadas e eliminadas.

---
## Instâncias de Contêiner do Azure ##

Caso não necessite de uma gestão do SO, pode-se utilizar os containers. Que são unidades virtualizadas, sem a camanda de SO exposta, por tanto com um menor custo de consumo, podendo estar ou não no mesmo host físico.

Um dos contêiners mais famosos é o Docker.

As VMs virtualizam o hardware da máquina e os Contêiners virtualizam o SO.

É possível gerenciar seus containers (ou orquestrar). No caso pode-se parar, pausar, redimensionar um container ou vários deles. 

Existem dois serviços de orquestração de containers: **Instâncias de Contêiner do Azure** e **AKS (Serviço de Kubernetes do Azure)**.

### Kubernetes ###

É um orquestrador de containers, que além de gerenciamento dos containers fornece uma API rica para melhor proveito do uso de dados. Além disso é possível criar regras de redimensionamento, atualização com pouca inatividade, replicação de containers, pods (nós ou máquinas preestabelecidas etc).

Containers e Kubernets são muito utilizados em uma arquitetura de microserviços, pois gera independência na evolução e manutenção dos serviços.

---
## Serviço de aplicativo do Azure ##

*trecho retirado do Microsoft Learn*
> permite que você crie e hospede aplicativos Web, trabalhos em segundo plano, back-ends de dispositivos móveis e APIs RESTful na linguagem de programação de sua escolha sem gerenciar a infraestrutura. Ele oferece dimensionamento automático e alta disponibilidade. O Serviço de Aplicativo é compatível com Windows e Linux e permite implantações automatizadas do GitHub, Azure DevOps ou qualquer repositório Git para dar suporte a um modelo de implantação contínua.

Existem dois serviços principais que removem essa abstração de infraestrutura e fornecem um trecho de ação utilizado baseado em certos gatilhos e desligados após esse procedimento:

*Azure Functions* e *Aplicativos Lógicos do Azure*

Azure functions - Executa um determinado bloco de código baseado em algum gatilho. Caso necessite de estado o processo é chamado de Durable functions, pois dependeram do estado para serem executadas. Porém na maioria dos casos as funções são sem estado, permitindo a rápida execução e a rápida saída. 

Aplicativos Lógicos do Azure - São fluxos de trabalho executados baseados em determinados gatilhos. São utilizados em casos onde um gatilho o ativa e ele realiza diversas cargas de trabalho baseado em integrações com diversos aplicativos e serviços web. 

Os fluxos de trabalho do Aplicativos Lógicos do Azure são gerados no formato JSON. São fornecidos cerca de 200 conectores e blocos de processamento para a utilizaçao no Aplicativos lógicos (e-mail, slack, zendesk etc).



---
## Azure Functions ##
(ou Servless - computação "sem" servidor) ##

