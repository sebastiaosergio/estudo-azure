# Serviços de armazenamento

## Armazenamento em disco

Funciona como um disco na cloud, podendo ser HD ou SSD. Esse discos serão acessados por VMs do Azure

---
## Blobs

Solução de armazenamento de objetos. Dados não estruturados, podendo ser arquivos de imagem, aúdio, vídeo, logs... Não são limitads a tipos de  arquivos, podendo até mesmo conter tipos personalizados. 

Os objetos armazenados não dependerão de um controle e gerenciamento de disco. Ficando a cargo do Azure o armazenamento e retorno do path do objeto.

Pode-se utilizar para diversos fins, entre eles: log, streaming de vídeo e aúdio, backup etc.

---
## Arquivos do Azure

Funciona como um diretório na nuvem, utilizando inclusive protocolos de arquivos semelhante ao SO. 

Pode-se inclusive, mapear como unidade de rede.

Além disso os arquivos podem ser acessados via uma URL com tempo de expiração.

---
## Entendo o Blob

Além do armazenamento tradicional é importante compreender o fluxo de uso e necessidade do conteúdo armazenado. Isso afetará diretamente o custo do Armazenamento no Azure.

Para isso existe as **Camandas de Acesso**. Com elas é possível analisar o fluxo de uso e configurar ele para a camanda de acesso correta, reduzindo custos.

### Tipos de camanda de acesso

| Tipo | Descricao |
|------|-----------|
| **HOT** Camada de acesso quente | Otimizada para dados com acessos frequentes (imagems de um site, arquivos estáticos de acesso público) |
| **COLD** Camada de acesso frio | Otimizada para acesso menos frequente e armazenamento de pelo menos 30 dias (faturas de clientes, relatorios mensais) |
| Camada de acesso aos arquivos | Acesso raro e armazenamento por pelo menos 180 dias (6 meses) (backups de longo prazo) |

> Importante entender que o armazenamento é menor quando menos a utilização dos dados. Porém quando se utiliza ou necessita atualizar o valor para esse procedimento é maior que o **hot**. Ou seja, manter o arquivo é mais barato, mas acessá-lo é mais caro. 
> Por isso é importantíssimo fazer uma análise muito detalhada desse uso.

