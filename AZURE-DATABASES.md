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

---
## Instâncias de Contêiner do Azure ##

---
## Serviço de aplicativo do Azure ##

---
## Azure Functions ##
(ou Servless - computação "sem" servidor) ##

