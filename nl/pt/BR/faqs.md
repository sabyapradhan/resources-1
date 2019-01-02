---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-15"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# FAQ
{: #resources-faq}

## O que é um grupo de recursos?
{: #resource-group}
{: faq}

Um grupo de recursos é uma maneira para organizar os recursos da conta em agrupamentos customizáveis. Qualquer recurso de conta que é gerenciado usando o controle de acesso do {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) pertence a um grupo de recursos em sua conta. Designe os recursos a um grupo de recursos ao criá-los do catálogo. Em seguida, será possível visualizar o uso por grupo de recursos
na conta e designar facilmente aos usuários o acesso a todos os recursos ou apenas a um em um grupo de recursos.

Para obter mais informações sobre como criar e trabalhar com os grupos de recursos, consulte
[Gerenciando os grupos de recursos](/docs/resources/resourcegroups.html#rgs).  

## Por que devo migrar as instâncias de serviço do Cloud Foundry para um grupo de recursos?
{: #instance-migrated}
{: faq}

A migração dos serviços do Cloud Foundry para um grupo de recursos significa que os serviços que estão sendo usados agora
estão disponíveis para uso com o controle de acesso do IAM e os grupos de recursos. É possível obter vantagem do controle de acesso
de baixa granularidade usando as funções do IAM. Também é possível visualizar o uso por grupo de recursos na conta. 

Quando você tiver serviços do Cloud Foundry que possam ser migrados para um grupo de recursos, você receberá uma notificação em sua lista de recursos. Para obter mais informações sobre o processo de migração, consulte
[Migrando as instâncias de serviço e os apps do Cloud Foundry para um
grupo de recursos](/docs/resources/instance_migration.html#migrate).

## Por que não consigo criar um recurso e incluí-lo em um grupo de recursos?
{: #create-add-resource}
{: faq}

Muito provavelmente você está lidando com um problema de acesso. Deve-se ter pelo menos a função de visualizador no
próprio grupo de recursos e, pelo menos, a função do editor no serviço da conta. É possível entrar em contato com o administrador da
conta para verificar o acesso designado na conta. 

## Quem pode criar grupos de recursos?
{: #create-resource}
{: faq}

É possível criar grupos de recursos apenas se você tiver designada a função de Administrador em todos os serviços {{site.data.keyword.Bluemix_notm}} Identity and Access ativados para a conta.

## Posso excluir um grupo de recursos?
{: #delete-resource-group}
{: faq}

Não é possível excluir um grupo de recursos após ele ter sido criado.

## Posso mover as instâncias de serviço entre os grupos de recursos?
{: #instances-between-rgs}
{: faq}

Não é possível mover as instâncias de serviço entre os grupos de recursos. Se você designar uma instância de serviço incorretamente, deverá excluir e recriar a instância para designá-la ao grupo de recursos correto.  

## Posso visualizar o uso por grupo de recursos?
{: #view-usage}
{: faq}

Sim, você pode. Para abrir a página Painel de uso, clique em **Gerenciar** &gt; **Faturamento e uso**. Selecione **Uso** para visualizar um resumo do uso por grupo de recursos para a conta. 
