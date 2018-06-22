---

copyright:

  years: 2018
lastupdated: "2018-06-08"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}


# Melhores práticas para organizar recursos em um grupo de recursos
{: #bp_resourcegroups}

Os grupos de recursos são um recurso para organizar seus [recursos](/docs/resources/acct_resources.html#resource) de conta para propósitos de controle de acesso e faturamento. Se você está familiarizado com o uso espaços do Cloud Foundry, pode pensar em organizar os recursos em grupos de recursos de forma semelhante à maneira como organizou os recursos em espaços. Um recurso é qualquer coisa que possa ser criada, gerenciada e contida em um grupo de recursos. Os usuários não são incluídos em grupos de recursos. Somente recursos podem ser incluídos. 

Atualmente, nem todos os serviços suportam o uso de controle de acesso do {{site.data.keyword.Bluemix_notm}} Identidade e Acesso Management (IAM) e a designação a um grupo de recursos. Os serviços gerenciados pelo IAM solicitam que você designe novas instâncias de serviço a um grupo de recursos ao criá-las no catálogo. O acesso aos recursos em um grupo de recursos e o grupo de recursos em si são gerenciados pelo IAM. Usando funções do IAM, é possível fornecer aos usuários acesso aos recursos que são organizados nos grupos de recursos. As funções do IAM também podem fornecer a capacidade de visualizar, editar, incluir novas instâncias de serviço ou gerenciar o acesso a um grupo de recursos.

Também é possível localizar a lista de serviços gerenciados pelo IAM quando você designa acesso aos recursos da UI do Identity and Access. Acesse **Gerenciar** &gt; **Segurança** &gt; **Identidade e acesso**, em seguida, selecione qualquer ID do usuário ou serviço e selecione **Designar acesso** no menu **Ações**. Em seguida, selecione **Designar acesso a recursos** e, no menu suspenso **Serviços**, é possível visualizar os serviços que suportam o uso do IAM. Para todos os serviços que ainda não suportam o uso do IAM, é possível continuar a usar as organizações, os espaços e as funções do Cloud Foundry. 

As organizações, os espaços e as funções do Cloud Foundry são claramente separados dos grupos de recursos e funções do IAM. Portanto, uma função do Cloud Foundry nunca pode conceder acesso a recursos dentro de um grupo de recursos.
{: tip}


## Configurando seu grupos de recursos

Todos os usuários obtêm um único grupo de recursos por padrão que pode ser renomeado. Se você tem uma conta faturável, é possível criar mais de um grupo de recursos para organizar seus recursos. Ao organizar recursos em grupos de recursos diferentes, é possível:

* Tornar a designação de acesso a um conjunto de recursos mais fácil usando um número mínimo de políticas 
* Visualizar informações de uso do grupo de recursos para propósitos de faturamento 

Para criar um novo grupo de recursos, conclua as etapas a seguir:

1. Acesse **Gerenciar** &gt; **Conta** &gt; **Grupos de recursos**.
2. Clique em **Criar um grupo de recursos**.
3. Insira um nome para seu grupo de recursos.
4. Clique em ** Adicionar**.


## Incluindo recursos em um grupo de recursos

Os serviços que são gerenciados usando o controle de acesso do IAM pertencem a um grupo de recursos, em vez de uma organização ou um espaço do Cloud Foundry. Ao criar uma instância de serviço para um desses serviços do catálogo,
é solicitado que você designe a instância a um grupo de recursos. 

**Importante**: sua seleção de grupo de recursos no momento da criação da instância é final e não pode ser mudada.

Conforme mais serviços ativam a designação para grupos de recursos e o uso de controle de acesso do IAM, você é notificado em seu painel se tem instâncias de serviço existentes do Cloud Foundry que são elegíveis para migração. Ao [migrar uma instância de serviço para um grupo de recursos](/docs/resources/instance_migration.html), você está criando uma nova instância vinculada em um grupo de recursos de sua escolha e a instância do Cloud Foundry se torna um alias. 


## Designando acesso a grupos de recursos e aos recursos dentro deles

Você fornece acesso para usuários ou grupos de usuários que são organizados em grupos de acesso criando políticas de acesso. As políticas de acesso configuram um destino, que é geralmente uma instância de serviço ou todas as instâncias de um serviço em um grupo de recursos e uma função que define qual tipo de acesso é permitido. Há dois tipos de políticas de acesso que você precisa designar como um proprietário da conta para permitir aos usuários em sua conta o acesso para trabalhar com recursos em grupos de recursos:

* Acesso a recursos em um grupo de recursos. O acesso pode ser concedido a todos os recursos em um grupo ou somente serviços selecionados em um grupo.
* Acesso para permitir que os usuários gerenciem o grupo, significando que os usuários podem visualizar o grupo, edite o nome do grupo, gerenciar o acesso para outros gerenciarem o grupo e o mais importante poder criar e incluir novas instâncias de serviço em um grupo.

Revise a tabela a seguir para obter mais informações sobre os dois tipos de acesso e o que cada função do IAM da plataforma designada fornece a um usuário a capacidade de fazer:

| Detalhes da política de acesso  | Ações para acesso em grupos de recursos | Ação em recursos em grupos de recursos | 
|:-----------------|:--------------|:---------------|
| Designar acesso a | Grupo de recursos selecionados | Serviço selecionado em um grupo de recursos |
| Função de visualizador  | Visualizar o grupo e suas características, mas não os recursos no grupo | Visualizar recursos no grupo | 
| Função de operador | Não aplicável | Não aplicável | 
| Função do editor | Visualizar ou editar o nome ou outras características do grupo, mas não os recursos no grupo | Criar, excluir, editar, suspender, continuar, visualizar, ligar e gerenciar o acesso de recursos no grupo de recursos |
| Função de administrador | Visualizar, editar ou gerenciar o acesso para o grupo, mas não os recursos no grupo | Criar, excluir, editar, suspender, continuar, visualizar, ligar e gerenciar o acesso de recursos no grupo de recursos | 
{: caption="Tabela 1. Acesso para grupos de recursos" caption-side="top"}

Se você deseja que um usuário possa criar uma nova instância de serviço e incluí-la em um grupo de recursos, o usuário deve ser designado como um Visualizador ou acima no grupo de recursos e Editor ou acima no serviço.
{: tip}


## As políticas de acesso de amostra

Revise as políticas de acesso de amostra a seguir para ajudá-lo a determinar como você pode desejar designar acesso aos recursos em sua conta que pertencem a grupos de recursos.

1. Uma política que concede ao usuário a Função de plataforma “Administrador” no {{site.data.keyword.Bluemix_notm}} Container Service na conta inteira. Uma política com esses detalhes permite ao usuário acesso a todas as instâncias desse serviço e permite que o usuário crie instâncias do serviço em qualquer grupo de recursos no qual o usuário tenha pelo menos a função de Visualizador. Os usuários com a função de Administrador em qualquer recurso também podem conceder a outros usuários acesso a esse recurso.
2. Uma política que concede ao usuário a Função de plataforma “Visualizador” em um grupo de recursos, mas não seus recursos de membros. Uma política com esses detalhes permite ao usuário visibilidade para o grupo de recursos, que é necessária para criar instâncias de qualquer serviço nesse grupo de recursos.
3. Uma política que concede ao usuário a Função de plataforma “Editor” em todos os recursos no grupo de recursos. Um usuário com a função de Editor em um recurso pode editar ou excluir esse recurso.
4. Uma política que concede ao usuário a Função de plataforma “Administrador” na conta inteira (todos os serviços ativados por IAM). Uma política com esses detalhes permite que o usuário execute quaisquer ações da plataforma em qualquer recurso na conta inteira e também inclui a capacidade de executar ações de gerenciamento na conta, como gerenciar os grupos de recursos na conta.

## Exemplos de Caso de Uso

Para cada um desses casos de uso, se tiver um grupo de usuários que você deseja que todos tenham o mesmo nível de acesso, inclua-os em um [grupo de acesso](/docs/iam/groups.html#groups). Usando grupos de acesso, é possível usar um número mínimo de políticas de acesso porque todos os membros do grupo de acesso herdam o acesso designado ao grupo.
{: tip}

1. Eu tenho uma conta pequena com somente 10 usuários, que trabalham todos juntos em um único projeto. Alguns desses usuários precisam ser capazes de gerenciar a conta e designar acesso a outros usuários. Alguns dos usuários precisam ser capazes de provisionar instâncias de serviço que incorrerão em despesas. Outros usuários são desenvolvedores de aplicativos que precisam somente ser capazes de usar as instâncias de serviço de seus componentes de aplicativo. Todos esses usuários devem ter várias funções concedidas na conta e no grupo de recursos padrão, não há necessidade de criar grupos de recursos adicionais para separar recursos ou restringir alguns usuários de acessar alguns dos recursos. Os usuários podem ter as funções adequadas às suas necessidades concedidas na conta e no grupo de recursos padrão – Administrador na conta para usuários que precisam ser capazes de gerenciar a conta e fornecer acesso aos outros, Editor no grupo de recursos padrão e em seus membros para usuários que precisam ser capazes de provisionar instâncias de serviço e Gravador ou Leitor nos membros do grupo de recursos para usuários que precisam somente usar as instâncias de serviço.
2. Eu tenho uma conta que inclui três equipes diferentes que trabalham em três projetos. Alguns usuários são administradores e precisam da capacidade de incluir novos usuários na conta, criar novos grupos de recursos e designar aos usuários acesso a grupos de recursos. Os usuários restantes precisam somente de acesso ao grupo de recursos associado ao seu projeto. Eu designaria aos administradores a função de Administrador de conta. Eu designaria aos usuários restantes várias funções no grupo de recursos e membros do grupo de recursos associados a seus projetos - Editor do grupo de recursos para aqueles que precisam criar instâncias, mais Leitor ou Gravador do membro do grupo de recursos para aqueles que precisam ser capazes de usar instâncias.
3. Eu tenho uma conta com múltiplos grupos de recursos. Eu tenho alguns usuários que são os administradores para o Serviço A em toda a minha conta e precisam de acesso para todas as instâncias desse serviço, bem como a capacidade de criar instâncias, mas esses usuários não precisam de acesso para quaisquer outros recursos na conta. Eu designaria a esses usuários a função de Administrador no Serviço A no nível de conta, bem como designaria a função de Visualizador para todos os grupos de recursos na conta na qual eles precisam ser capazes de criar instâncias.
4. Eu tenho um usuário em minha conta que precisa somente de acesso a um recurso específico em um serviço, por exemplo a capacidade de gravar em um Depósito A no IBM Cloud Object Storage. Esse usuário não deve ser capaz de ver os grupos de recursos em minha conta ou acessar quaisquer outros serviços ou quaisquer outros depósitos nessa instância do Cloud Object Storage. Eu daria a esse usuário a função de Gravador no Depósito A na instância específica de Cloud Object Storage. É possível conceder essa política usando interfaces específicas do serviço (a UI do Cloud Object Storage, neste exemplo) ou a UI principal Designar Acesso. A UI específica do serviço é recomendada porque ela permitirá que você escolha entre uma lista de recursos, enquanto a UI Designar Acesso não exibe recursos abaixo do nível da instância de serviço e você precisaria inserir manualmente o CRN para designar políticas a esses recursos.
