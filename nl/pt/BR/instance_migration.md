---

copyright:

  years: 2017, 2019

lastupdated: "2019-02-19"

keywords: migrate, migrating to a resource group, migrate Cloud Foundry

subcollection: resources

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Migrando instâncias de serviço e apps do Cloud Foundry para um grupo de recursos
{: #migrate}

Para tornar sua experiência com o uso de {{site.data.keyword.Bluemix}} mais simples e mais flexível, introduzimos [grupos de recursos](/docs/resources?topic=resources-rgs), que são conceitualmente semelhantes aos espaços do Cloud Foundry. No entanto, os grupos de recursos incluem vários benefícios extras, como controle de acesso de granularidade mais refinada usando o IBM Cloud Identity and Access Management (IAM), a capacidade de conectar instâncias de serviço a apps e serviços em diferentes regiões e uma maneira fácil de visualizar o uso por grupo.
{:shortdesc}

Estamos começando a mover os serviços do Cloud Foundry para nos beneficiar de grupos de recursos, o que significa que quando você vê o ícone ![Migrar esta instância de serviço para um grupo de recursos](images/migrate.svg "Migrar esta instância de serviço para um grupo de recursos") ao lado de um de seus serviços em sua lista de recursos, deve ser iniciado um plano de migração para as instâncias de serviço ou apps que são criados por meio do [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.dev_console}}](https://cloud.ibm.com/developer/appservice/dashboard) para mover de sua organização e espaço do Cloud Foundry atual para um grupo de recursos. Até que um serviço do {{site.data.keyword.Bluemix_notm}} mova do uso de organizações, espaços e funções do Cloud Foundry para o uso de IAM e grupos de recursos, não é possível migrar suas instâncias de serviço existentes do Cloud Foundry para um grupo de recursos.

Ao migrar instâncias de serviço do Cloud Foundry ou apps do {{site.data.keyword.dev_console}} existentes para um grupo de recursos, o grupo que você escolher não poderá ser mudado após a conclusão da migração. Portanto, é essencial planejar como você deseja organizar os recursos na conta antes de migrar. Isso pode significar que você precisará criar um ou mais grupos de recursos, se tiver uma conta faturável, antes da migração.

É possível tentar organizar seus recursos em grupos de recursos da mesma forma que organizou os recursos em espaços do Cloud Foundry. Para obter mais informações sobre como usar grupos de recursos, veja [Melhores práticas para organizar recursos em grupos de recursos](/docs/resources?topic=resources-bp_resourcegroups).
{: tip}


## Por que migrar?
{: #why_migrate}

### Instâncias de serviço do Cloud Foundry
{: #cf_instances}

Os serviços que suportam controle de acesso e organização do Cloud IAM em grupos de recursos têm vários benefícios:

* Ao usar o controle de acesso de baixa granularidade, é possível configurar o acesso a instâncias de serviço individuais ou a um grupo de recursos que são organizados em um grupo de recursos.
* Usando grupos de acesso e grupos de recursos para organizar usuários e recursos, você configura somente o número mínimo de políticas de acesso. Por exemplo, se você tem um conjunto de desenvolvedores e deseja que todos tenham acesso a recursos para um ambiente de desenvolvimento, é possível organizar todos esses usuários em um grupo de acesso de desenvolvedores e, em seguida, incluir todos os recursos aos quais eles precisam de acesso em um único grupo de recursos. Em seguida, é possível configurar uma única política para o grupo de acesso para ter acesso a todos os recursos no grupo de recursos.
* É possível visualizar o uso por grupo de recursos semelhante à maneira que você pode visualizar o uso por organizações do Cloud Foundry.
* É possível conectar-se a apps e serviços em qualquer espaço do Cloud Foundry, que permite conexões para apps e serviços de diferentes regiões. Ao migrar, a conexão é feita automaticamente quando você transforma sua instância de serviço original do Cloud Foundry em um alias e quando cria uma instância vinculada em um grupo de recursos de sua escolha. O gráfico a seguir mostra como funciona a conexão usando um alias.

![Migrar esta instância de serviço para um grupo de recursos](images/alias.svg "Ligando uma instância de serviço a um espaço do Cloud Foundry para criar um alias")

### {{site.data.keyword.dev_console}}  apps
{: #app_services}

Anteriormente, os apps do {{site.data.keyword.dev_console}} podiam ser associados apenas a instâncias de serviço do Cloud Foundry. Agora, se você migrar seus apps para um grupo de recursos, poderá associar seus apps a instâncias de serviço que pertençam a um grupo de recursos e suportem o controle de acesso do Cloud IAM.

## Quem pode migrar?
{: #whocanmigrate}

### Acesso necessário para instâncias de serviço
{: #required_access_instances}

Os usuários devem ter acesso específico para migrar instâncias de serviço do Cloud Foundry para um grupo de recursos:

* Um usuário deve ter a função de Desenvolvedor no espaço do Cloud Foundry ou a função de Gerenciador de organização do Cloud Foundry na organização à qual a instância pertence.
* Um usuário deve ter pelo menos a função de Visualizador do IAM para gerenciar o grupo de recursos para o qual a instância será migrada.
* Um usuário deve ter pelo menos a função de Editor do IAM no serviço.

Para obter mais informações sobre como designar o acesso correto, veja [Acesso ao Cloud Foundry](/docs/iam?topic=iam-cfaccess) e [Acesso ao IAM](/docs/iam?topic=iam-userroles#platformrolestable1).

Para conferir o acesso que você tem, clique em **Gerenciar** &gt; **Acessar (IAM)** na barra de menus do console e, em seguida, clique em **Usuários**. Clique em seu nome e revise suas **Políticas de acesso** para as funções designadas do IAM e **Acesso do Cloud Foundry** para ver a quais organizações você tem acesso e suas funções designadas do Cloud Foundry.
{: tip}

### Acesso necessário para apps  {{site.data.keyword.dev_console}}
{: #required_access_apps}

Qualquer usuário que possa acessar um aplicativo do {{site.data.keyword.dev_console}} pode migrá-lo. No entanto, a migração de um app não migra serviços que estão associados ao app. As instâncias de serviço devem ser migradas separadamente.

## Como a migração funciona?
{: #how}

### Migrando instâncias de serviço
{: #migrate_instances}

Quando você migra uma instância de serviço de uma organização e de um espaço do Cloud Foundry para um grupo de recursos, uma nova instância de serviço vinculada é criada no grupo de recursos. A instância original na
organização e no espaço do Cloud Foundry se torna um
[alias](/docs/resources?topic=resources-connect_app#what_is_alias). O alias conta em direção à cota para sua organização, mas você é faturado por seu uso da instância de serviço no grupo de recursos.

![Migração de uma instância de serviço do Cloud Foundry para um grupo de recursos](images/migration.gif){: gif}

As instâncias de serviço são migradas uma de cada vez quando você é notificado sobre a lista de recursos pelo ícone ![Migrar esta instância de serviço para um grupo de recursos](images/migrate.svg "Migrar esta instância de serviço para um grupo de recursos") que está associado a sua instância de serviço do Cloud Foundry.

Antes de iniciar o processo de migração, revise a documentação de seu serviço para ver se quaisquer mudanças adicionais específicas do serviço que você pode ter que fazer ao migrar sua instância de serviço para um grupo de recursos. Por exemplo, talvez seja necessário migrar dados de instâncias antigas para novas instâncias ou atualizar as credenciais que são usadas para seu app se você excluir o alias do Cloud Foundry. Os aplicativos que fazem uma chamada direta para a API de um serviço que é migrado precisam atualizar a chamada API para usar uma chave de API do IAM ou um token de acesso.
{: tip}

1. Abra o menu **Mais ações**.
2. Selecione **Migrar para um grupo de recursos** para iniciar.
3. Selecione um grupo de recursos.
4. Clique em **Migrar** e a instância é migrada para você.
5. Como é possível migrar somente uma instância por vez, é possível continuar migrando instâncias elegíveis depois que você migra a primeira.

Depois de migrar com êxito uma instância, você a verá na seção Serviços de sua lista de recursos. O alias permanece na seção Cloud Foundry da lista de recursos. É possível usar o ![Ícone de link](images/link.svg "Ícone de link que representa um alias") na seção do Cloud Foundry da lista de recursos para identificar os aliases.

### Migrando apps  {{site.data.keyword.dev_console}}
{: #migrate_apps}

Os apps são migrados um de cada vez, clicando no ícone ![Migrar esta instância de serviço para um grupo de recursos](images/migrate.svg "Migrar esta instância de serviço para um grupo de recursos") associado a cada entrada na visualização Lista de Aplicativos.

1. Selecione o ícone **Menu** ![Ícone Menu](../icons/icon_hamburger.svg) e selecione o portal do desenvolvedor de interesse, como Watson, Mobile ou Apps da Web, por exemplo.
2. Selecione **Apps**, que exibe as listas **Apps (Ação necessária)** e **Apps (migrados)**.
3. Para cada entrada na lista **Apps (ação necessária)**, clique no ícone **Migrar** ![Migrar esta instância de serviço para um grupo de recursos](images/migrate.svg "Migrar esta instância de serviço para um grupo de recursos").
4. Selecione ou crie um novo grupo de recursos.
5. Clique em **Migrar** e o app será migrado para você.
6. Confirme se o app agora é mostrado na lista **Apps (migrados)**.
7. Como é possível migrar apenas um app de cada vez, é possível continuar migrando apps elegíveis após a migração do primeiro.


## Próximas Etapas
{: #migrate_next_steps}

Depois de migrar suas instâncias de serviço do Cloud Foundry para um grupo de recursos, você precisa assegurar que os usuários em sua conta tenham o nível necessário de acesso aos recursos nos grupos de recursos da conta. Talvez você também queira fornecer acesso para gerenciar o grupo de recursos para que os usuários possam criar novas instâncias de serviço nos grupos de recursos da conta.

Para obter mais informações sobre como designar o acesso a recursos em seus grupos de recursos, veja [Designando acesso a grupos de recursos e aos recursos dentro deles](/docs/resources?topic=resources-bp_resourcegroups#assigning_access_rgs).

Além disso, certifique-se de revisar a documentação de seu serviço para ver se deverá ser realizada alguma atualização dos apps existentes após a conclusão da migração.


## Resolução de problemas
{: #ts_migration}

Se você se deparar com qualquer problema com a migração de instâncias de serviço do Cloud Foundry, confira [Resolvendo problemas de serviços e recursos](/docs/resources?topic=resources-services).
