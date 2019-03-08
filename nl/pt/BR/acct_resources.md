---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: service instances, resource group, resource

subcollection: resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# O que é um recurso?
{: #resource}

Um recurso é qualquer coisa que possa ser criada, gerenciada e contida em um [grupo de recursos](/docs/resources?topic=resources-rgs). Alguns exemplos incluem apps, instâncias de serviço, clusters de contêineres, volumes de armazenamento e servidores virtuais. Todas as instâncias de serviço que podem ser incluídas em um grupo de recursos quando elas são criadas por meio do catálogo são chamadas de recursos e são gerenciadas usando o controle de acesso do IAM. Os serviços que suportam o uso do [funções do IAM para acesso](/docs/iam?topic=iam-userroles#iamusermanrol) e organização em um grupo de recursos são serviços ativados por IAM.

Nem todos os serviços suportam o uso de grupos de recursos e do IAM atualmente. Todas as instâncias de serviço que são incluídas nas organizações e espaços do Cloud Foundry quando elas são criadas por meio do catálogo são distintamente diferentes dos serviços ativados pelo IAM. Os serviços do Cloud Foundry não têm conexão com grupos de recursos e usam [funções do Cloud Foundry para gerenciamento de acesso](/docs/iam?topic=iam-cfaccess#cfroles). Esses serviços são chamados de serviços do Cloud Foundry. Conforme os serviços ativam o suporte para IAM e grupos de recursos, você é notificado sobre a capacidade de [migrar instâncias existentes do Cloud Foundry para um grupo de recursos](/docs/resources?topic=resources-migrate).
