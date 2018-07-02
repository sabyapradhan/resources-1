---

copyright:

  years: 2017, 2018

lastupdated: "2018-06-20"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Migrando instâncias de serviço do Cloud Foundry para um grupo de recursos
{: #migrate}

Para tornar sua experiência com o uso do {{site.data.keyword.Bluemix}} mais simples e mais flexível, o {{site.data.keyword.Bluemix}} introduziu [grupos de recursos](/docs/resources/resourcegroups.html#rgs), que são conceitualmente semelhantes a espaços do Cloud Foundry. Entretanto, os grupos de recursos incluem vários benefícios extras, como o controle de acesso de baixa granularidade usando o IBM Cloud Identity e o Access Management (IAM), a capacidade de conectar instâncias de serviços aos apps e serviços entre diferentes regiões e uma forma fácil de visualizar o uso por grupo.
{:shortdesc}

O {{site.data.keyword.Bluemix_notm}} está começando a mover serviços do Cloud Foundry para se beneficiar de grupos de recursos. Quando você vir o ícone ![Migrar esta instância de serviço para um grupo de recursos](images/migrate.svg "Migrar esta instância de serviço para um grupo de recursos") próximo a um de seus serviços em seu painel, um plano de migração deverá ser iniciado para suas instâncias de serviço a fim de mover da organização e espaço atuais do Cloud Foundry para um grupo de recursos. Até que um serviço do {{site.data.keyword.Bluemix_notm}} mova do uso de organizações, espaços e funções do Cloud Foundry para o uso de IAM e grupos de recursos, não é possível migrar suas instâncias de serviço existentes do Cloud Foundry para um grupo de recursos.

Ao migrar instâncias de serviço do Cloud Foundry existentes para um grupo de recursos, o grupo de recursos que você escolher não poderá ser mudado após a migração ser concluída. Então, é essencial que você planeje como deseja organizar os recursos na conta antes de migrar. Portanto, poderá ser necessário criar um ou mais grupos de recursos, se você tiver uma conta faturável, antes da migração. 

É possível tentar organizar seus recursos em grupos de recursos da mesma forma que organizou os recursos em espaços do Cloud Foundry. Para obter mais informações sobre como usar grupos de recursos, veja [Melhores práticas para organizar recursos em grupos de recursos](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).
{: tip}


## Por que migrar instâncias de serviço?

Os serviços que suportam controle de acesso e organização do Cloud IAM em grupos de recursos têm vários benefícios:

* Usando o controle de acesso de baixa granularidade, é possível configurar o acesso a instâncias de serviço individuais ou um grupo de recursos, que são organizados em um grupo de recursos. 
* Usando grupos de acesso e grupos de recursos para organizar usuários e recursos, você configura somente o número mínimo de políticas de acesso. Por exemplo, se você tem um conjunto de desenvolvedores e deseja que todos tenham acesso a recursos para um ambiente de desenvolvimento, é possível organizar todos esses usuários em um grupo de acesso de desenvolvedores e, em seguida, incluir todos os recursos aos quais eles precisam de acesso em um único grupo de recursos. Em seguida, é possível configurar uma única política para o grupo de acesso para ter acesso a todos os recursos no grupo de recursos.
* É possível visualizar o uso por grupo de recursos de maneira semelhante a como podia visualizar o uso por organizações do Cloud Foundry.
* É possível conectar-se a apps e serviços em qualquer espaço do Cloud Foundry, que permite conexões para apps e serviços de diferentes regiões. Quando você migra, a conexão é feita automaticamente transformando sua instância de serviço do Cloud Foundry original em um alias e criando uma instância vinculada em um grupo de recursos de sua escolha. O gráfico a seguir descreve como a conexão usando um alias funciona.

![Migrar esta instância de serviço para um grupo de recursos](images/alias.svg "Ligando uma instância de serviço a um espaço do Cloud Foundry para criar um alias")

## Quem pode migrar instâncias de serviço?
{: #whocanmigrate}

Os usuários devem ter acesso específico para migrar instâncias de serviço do Cloud Foundry para um grupo de recursos:

* Um usuário deve ter a função de Desenvolvedor no espaço do Cloud Foundry ou a função de Gerenciador de organização do Cloud Foundry na organização à qual a instância pertence.
* Um usuário deve ter pelo menos a função de Visualizador do IAM para gerenciar o grupo de recursos para o qual a instância será migrada.
* Um usuário deve ter pelo menos a função de Editor do IAM no serviço.

Para obter mais informações sobre como designar o acesso correto, veja [Acesso ao Cloud Foundry](/docs/iam/cfaccess.html#cfaccess) e [Acesso ao IAM](/docs/iam/users_roles.html#platformrolestable).

Para verificar o acesso que você tem, clique em **Gerenciar** &gt; **Segurança** &gt; **Identidade e acesso** na barra de menus do console e, em seguida, clique em **Usuários**. Clique em seu nome e revise suas **Políticas de acesso** para as funções designadas do IAM e **Acesso do Cloud Foundry** para ver a quais organizações você tem acesso e suas funções designadas do Cloud Foundry.
{: tip}


## Como a migração funciona?

Quando você migra uma instância de serviço de uma organização e de um espaço do Cloud Foundry para um grupo de recursos, uma nova instância de serviço vinculada é criada no grupo de recursos. A instância original na
organização e no espaço do Cloud Foundry se torna um
[alias](/docs/resources/connecting_apps.html#what_is_alias). O alias conta para a cota de sua organização, mas você é faturado por seu uso da instância de serviço no grupo de recursos.

![Migração de uma instância de serviço do Cloud Foundry para um grupo de recursos](images/migration.gif){: gif}

As instâncias de serviço são migradas uma por vez quando você é notificado no painel pelo ícone ![Migrar esta instância de serviço para um grupo de recursos](images/migrate.svg "Migrar esta instância de serviço para um grupo de recursos") que está associado à sua instância de serviço do Cloud Foundry.

Antes de iniciar o processo de migração, revise a documentação do serviço para ver se quaisquer mudanças adicionais e específicas de serviço devam ser feitas. Por exemplo, poderá ser necessário migrar dados de instâncias antigas para novas instâncias ou atualizar as credenciais que são usadas para seu app se você excluir o alias do Cloud Foundry. Os aplicativos que fazem uma chamada direta para a API de um serviço que foi migrado precisam atualizar a chamada API para usar uma chave API ou token de acesso do IAM.
{: tip}

1. Abra o menu **Mais ações**.
2. Selecione **Migrar para um grupo de recursos** para iniciar.
3. Selecione um grupo de recursos.
4. Clique em **Migrar** e a instância é migrada para você.
5. Como é possível migrar somente uma instância por vez, é possível continuar migrando instâncias elegíveis depois que você migra a primeira.

Depois de migrar com êxito uma instância, você a verá refletida na seção Serviços de seu painel. O alias permanece na seção do Cloud Foundry do painel. É possível usar o ![Ícone Link](images/link.svg "Ícone Link que representa um alias") na seção Cloud Foundry do painel para identificar os aliases.

## Próximas Etapas
{: #nextsteps}

Depois de migrar suas instâncias de serviço do Cloud Foundry para um grupo de recursos, você precisa assegurar que os usuários em sua conta tenham o nível necessário de acesso aos recursos nos grupos de recursos da conta. Talvez você queira fornecer acesso para gerenciar o grupo de recursos de modo que os usuários possam criar novas instâncias de serviço nos grupos de recursos da conta.

Para obter mais informações sobre como designar o acesso a recursos em seus grupos de recursos, veja [Designando acesso a grupos de recursos e aos recursos dentro deles](/docs/resources/bestpractice_rgs.html#assigning-access-to-resource-groups-and-the-resources-within-them).

Além disso, assegure-se de revisar a documentação para seu serviço para ver se alguma atualização para seus apps existentes deve ser feita após a migração ser concluída. 


## Resolução de problemas

Se você encontrar qualquer problema com a migração de instâncias de serviço do Cloud Foundry, verifique [Resolução de problemas de migração de instâncias de serviço](/docs/resources/ts_migration.html).
