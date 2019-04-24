---



copyright:

  years: 2017, 2019
lastupdated: "2019-02-07"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:note: .note}

# Gerenciando grupos de recursos
{: #rgs}

Um grupo de recursos é uma maneira de organizar seus recursos de conta em agrupamentos customizáveis para que seja possível designar rapidamente acesso aos usuários para mais de um recurso por vez. Qualquer recurso de conta que é gerenciado usando o controle de acesso do {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) pertence a um grupo de recursos em sua conta. Os serviços do Cloud Foundry são designados a organizações e espaços e não podem ser incluídos em um grupo de recursos.

Para iniciar o gerenciamento de seus grupos de recursos, acesse **Gerenciar ** &gt; **Conta**. Expanda **Recursos da conta** e, em seguida, selecione **Grupos de recursos**. Lá, é possível visualizar os grupos de recursos, incluir recursos, renomeá-los, gerenciar acesso e criar novos grupos de recursos. Para obter mais informações sobre como trabalhar com grupos de recursos, veja [Melhores práticas para organizar recursos em grupos de recursos](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).


## Criando um grupo de recursos

Se você tiver uma conta pré-paga ou de assinatura, será possível criar múltiplos grupos de recursos para gerenciar a cota e visualizar o uso de faturamento facilmente para um conjunto de recursos. Também será possível agrupar recursos para tornar mais fácil a designação de acesso de usuários para mais de uma instância por vez. É importante observar que é possível renomear um grupo de recursos, mas não é possível excluir um grupo de recursos após ele ter sido criado.

Se você tem uma conta Lite ou uma avaliação de 30 dias, não é possível criar grupos de recursos adicionais, mas é possível renomear o grupo de recursos padrão.

As conexões entre um grupo de recursos e uma organização ou espaço do Cloud Foundry são restringidas por sua cota. Para obter mais informações, veja [O que é um alias?](/docs/resources/connecting_apps.html#what_is_alias).
{: note}

1. Acesse **Gerenciar** &gt; **Conta**. Expanda **Recursos da conta** e, em seguida, selecione **Grupos de recursos**. 
2. Clique em **Criar um grupo de recursos**.
3. Insira um nome para seu grupo de recursos.
4. Clique em **Incluir**.

## Incluindo recursos em um grupo de recursos

Os serviços que são gerenciados com o IAM pertencem a um grupo de recursos em vez de organização ou espaço do Cloud Foundry. Ao criar uma instância de serviço para um desses serviços por meio do catálogo, será solicitado que designe a instância a um grupo de recursos. A seleção de grupo de recursos no momento da
criação da instância é definitiva e não pode ser mudada.

Para que os usuários em sua conta sejam capazes de criar recursos do catálogo e designá-los a um grupo de recursos, eles deverão ter duas políticas de acesso designadas:

* Uma política com função de visualizador ou superior no próprio grupo de recursos
* Uma política com função de editor ou superior no serviço na conta

## Visualizando recursos em grupos de recursos

Para visualizar facilmente os recursos que estão contidos em um grupo de recursos, filtre por grupo de recursos na sua lista de recursos.

## Renomeando um grupo de recursos

O primeiro grupo de recursos é criado e nomeado `Padrão` para você. É possível escolher atualizar o nome desse grupo ou quaisquer outros grupos criados.

1. Acesse **Gerenciar** &gt; **Conta**. Expanda **Recursos da conta** e, em seguida, selecione **Grupos de recursos**. 
2. Selecione **Renomear** no menu **Ações** ![Ícone Lista de ações](../icons/action-menu-icon.svg).
3. Insira um nome exclusivo e clique em **Salvar**.

## Gerenciando recursos e grupos de recursos usando o {{site.data.keyword.Bluemix_notm}} CLI

A CLI do {{site.data.keyword.Bluemix_notm}} tem múltiplos comandos que suportam o gerenciamento de recurso. Para obter mais informações, consulte [Trabalhando com recursos e grupos de recursos](/docs/cli/reference/ibmcloud/cli_resource_group.html#ibmcloud_commands_resource).

## Gerenciando o acesso a seus grupos de recursos

O Cloud IAM oferece a flexibilidade para fornecer acesso de usuário de baixa granularidade aos recursos em sua conta. É possível usar o Cloud IAM para designar políticas a usuários, que fornecem acesso de usuário a todos os recursos em um grupo de recursos, um único tipo de serviço em um grupo de recursos ou uma instância de serviço individual na conta. Fornecer aos usuários acesso aos recursos dentro de um grupo de recursos não lhes dá acesso para gerenciar o próprio grupo de recursos. É possível configurar o acesso para a capacidade de visualizar, editar e gerenciar o grupo de recursos reais separadamente.

Para obter mais informações, consulte [Gerenciando o acesso a recursos](/docs/iam/mngiam.html#iammanidaccser).
