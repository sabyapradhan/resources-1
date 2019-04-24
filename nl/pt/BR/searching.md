---

copyright:

  years: 2015, 2019
lastupdated: "2019-02-18"

keywords: search, find,

subcollection: resources, find resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}


# Procurando Recursos
{: #searching-for-resources}

É possível procurar recursos provisionados que você espera localizar na lista de recursos e ofertas no catálogo em qualquer lugar no console do {{site.data.keyword.cloud}}. Insira o recurso ou a tag no campo de procura na barra de menus do console. Também é possível usar a interface da linha de comandos (CLI) do {{site.data.keyword.Bluemix_notm}} para procurar em seus recursos. A CLI procura por aplicativos distribuídos e instâncias de serviço em locais e data centers.
{:shortdesc}

## Refinando seus resultados da procura
{: #results}

<dl>
<dt>Visualizar todos os resultados de recursos</dt>
<dd>Use essa opção para visualizar uma lista de recursos filtrados que preenche automaticamente o campo de nome dentro da lista de recursos, fornecendo a você os resultados mais relevantes. A procura retornada exibe os primeiros 10 resultados de recursos. Se você souber que há mais resultados, será possível ver todos eles na lista de recursos. Essa opção aparecerá se ela corresponder a um resultado de recurso ou procura de tag. Se ele não corresponder a um nome de resultado de recurso ou tag, ele não aparecerá.</dd>
<dt>Visualizar todos os resultados de catálogos</dt>
<dd>Use essa opção para visualizar uma procura de catálogo filtrada. Os primeiros cinco resultados são exibidos pelo nome. Se você desejar obter um critério de procura mais detalhado para entradas no catálogo, como procurar a descrição, será possível clicar nesse link e obter uma visualização de resultados do catálogo filtrados. Essa opção ajuda a localizar as ofertas que você deseja criar mais rapidamente. Isso aparecerá se houver correspondência com um resultado do catálogo. Esse campo não aparecerá se a consulta de procura iniciar com `tag:`.</dd>
<dt>Procurar casos de suporte</dt>
<dd>Use essa opção para filtrar por casos de suporte abertos na plataforma, incluindo recursos de infraestrutura. Isso é mostrado no final da procura se você procurar qualquer coisa, inclusive se você procurar por `tag:`.</dd>
<dt>Procurar no Docs</dt>
<dd>Use essa opção para obter uma filtragem da documentação. Isso é mostrado no final da procura se você procurar qualquer coisa, inclusive se você procurar por `tag:`.</dd>
</dl>

Pressione a tecla de barra (/) para navegar o cursor para o campo de procura.
{: tip}


## Procurando com a CLI
{: #searching-cl}

Também é possível procurar em todos os seus recursos usando a sintaxe de consulta Lucene, com um comando único usando a CLI do {{site.data.keyword.Bluemix_notm}}, a partir da versão 0.6.7.

  A CLI atualmente não procura recursos que estão em execução em instâncias de infraestrutura clássica.
  {: note}

É possível procurar os atributos a seguir:

<dl>
<dt>`Nome `</dt>
<dd> O nome definido pelo usuário do recurso.</dd>
<dt>` região  `</dt>
<dd>A localização geográfica na qual o recurso é provisionado. Os valores permitidos são `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de` e `jp-tok`.</dd>
<dt>`service_name`</dt>
<dd>O nome do serviço como aparece na coluna Nome da saída de 'ibmcloud catalog service-marketplace'.</dd>
<dt>`family`</dt>
<dd>O componente de nuvem ao qual seu recurso pertence. Os valores permitidos são `cloud_foundry`, `containers` ou `resource_controller`.</dd>
<dt>`organization_id`</dt>
<dd>O GUID da organização do Cloud Foundry.</dd>
<dt>`doc.space_id`</dt>
<dd>O GUID do espaço do Cloud Foundry.</dd>
<dt>`doc.resource_group_id`</dt>
<dd>O ID do grupo de recursos.</dd>
<dt>`type                    `</dt>
<dd>O tipo de recurso. Os valores válidos são `k8-cluster`, `cf-service-instance`, `cf-user-provided-service-instance`, `cf-organization`, `cf-service-binding`, `cf-space`, `cf-application`, `resource-instance`, `resource-alias`, `resource-binding` e `resource-group`.</dd>
<dt>`creation_date`</dt>
<dd>A data na qual o recurso é criado.</dd>
<dt>`modification_date`</dt>
<dd> A data da última modificação do recurso.</dd>
</dl>

### Exemplos de procura
{: #resource-name}

Os exemplos a seguir podem ajudar a procurar recursos de conta.

* Para procurar por todos os seus recursos denominados `ABC`, insira o comando a seguir.

    `ibmcloud resource search ‘name:ABC’`

* Para procurar por todos os aplicativos do Cloud Foundry chamados `MyResource`, insira o comando a seguir.

    `ibmcloud resource search 'name:my* AND type:cf-application'
`

* Para procurar todas as instâncias de serviço do Message Hub, insira o comando a seguir.

    `ibmcloud resource search 'service_name:messagehub'`

* Para procurar todos os recursos na organização do Cloud Foundry `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` ou o grupo de recursos `c900d9671b235c00461c5e311a8aeced` na região `us-south`, insira o comando a seguir.

    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`

* Para procurar por todos os recursos que foram criados entre 16 de maio de 2018 e 20 de maio de 2018, insira o comando a seguir.

    `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`

* Para procurar por todos os recursos cujo nome comece com "my", ordenado por tipo, insira o comando a seguir.

    `ibmcloud resource search 'name:my*' -s type`
