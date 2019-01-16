---

copyright:

  years: 2018
lastupdated: "2018-01-09"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Melhores práticas para organizar recursos em um grupo de recursos
{: #bp_resourcegroups}

Um grupo de recursos é um recurso que você usa para organizar os [recursos](/docs/resources/acct_resources.html#resource) da conta para propósitos de controle de acesso e faturamento. Se você estiver familiarizado com o uso de espaços do Cloud Foundry, pense em organizar recursos em grupos de recursos de forma semelhante à maneira como organizou os recursos em espaços. Um recurso é qualquer coisa que possa ser criada, gerenciada e contida em um grupo de recursos. Os usuários não são incluídos em grupos de recursos. Somente recursos podem ser incluídos. 

Atualmente, nem todos os serviços suportam o uso de controle de acesso do {{site.data.keyword.Bluemix_notm}} Identidade e Acesso Management (IAM) e a designação a um grupo de recursos. Os serviços ativados pelo IAM solicitam que você designe novas instâncias de serviço a um grupo de recursos ao criá-las por meio do catálogo. O acesso aos recursos em um grupo de recursos e o grupo de recursos em si são gerenciados pelo IAM. Usando funções do IAM, é possível fornecer aos usuários acesso aos recursos que são organizados nos grupos de recursos. As funções do IAM também podem fornecer a capacidade de visualizar, editar, incluir novas instâncias de serviço ou gerenciar o acesso a um grupo de recursos.

Também é possível localizar a lista de serviços ativados pelo IAM ao designar acesso aos recursos por meio da IU do Identity and Access, concluindo as etapas a seguir:
1. Acesse **Gerenciar** &gt; **Acesso (IAM)** e selecione **Usuários**. 
2. Selecione qualquer usuário e clique em **Políticas de acesso**. 
3. Selecione **Designar acesso** > **Designar acesso aos recursos**.
4. Usando o menu **Serviços**, selecione o serviço que você deseja designar. Para todos os serviços que ainda não suportam o uso do IAM, é possível continuar usando as organizações, os espaços e as funções do Cloud Foundry. 
5. Clique em **Designar**.

As organizações, os espaços e as funções do Cloud Foundry são claramente separados dos grupos de recursos e funções do IAM. Uma função do Cloud Foundry nunca pode conceder acesso a recursos dentro de um grupo de recursos. 
{: note}


## Configurando seu grupos de recursos

Todos os usuários obtêm um único grupo de recursos por padrão que pode ser renomeado. Designe a função de editor ou de administrador a todos os serviços de gerenciamento de conta para criar grupos de recursos. Se você tem uma conta faturável, é possível criar mais de um grupo de recursos para organizar seus recursos. Ao organizar recursos em grupos de recursos diferentes, é possível:

* Tornar a designação de acesso a um conjunto de recursos mais fácil usando um número mínimo de políticas 
* Visualizar informações de uso do grupo de recursos para propósitos de faturamento 

Para criar um novo grupo de recursos, conclua as etapas a seguir:

1. Acesse **Gerenciar** > **Conta**. 
2. Expanda **Recursos da conta** e selecione **Grupos de recursos**. 
3. Clique em **Criar um grupo de recursos**.
4. Insira um nome para seu grupo de recursos.
5. Clique em **Incluir**.


## Incluindo recursos em um grupo de recursos

Os serviços que são ativados usando o controle de acesso do IAM pertencem a um grupo de recursos, em vez de organização ou espaço do Cloud Foundry. Ao criar uma instância de serviço para um desses serviços por meio do catálogo, será solicitado que designe a instância a um grupo de recursos. 

**Importante**: sua seleção de grupo de recursos no momento da criação da instância é final e não pode ser mudada.

À medida que mais serviços ativarem a designação para grupos de recursos e o uso do controle de acesso do IAM, você será notificado em sua lista de recursos se você tiver instâncias de serviço existentes do Cloud Foundry que sejam elegíveis para migração. Ao [migrar uma instância de serviço para um grupo de recursos](/docs/resources/instance_migration.html), você está criando uma nova instância vinculada em um grupo de recursos de sua escolha e a instância do Cloud Foundry se torna um alias. 


## Designando acesso a grupos de recursos e aos recursos dentro deles

Você fornece acesso para usuários ou grupos de usuários que são organizados em grupos de acesso, criando políticas de acesso. As políticas de acesso configuram um destino, que é geralmente uma instância de serviço ou todas as instâncias de um serviço em um grupo de recursos e uma função que define qual tipo de acesso é permitido. Há dois tipos de políticas de acesso que você precisa designar como um proprietário da conta para permitir aos usuários em sua conta o acesso para trabalhar com recursos em grupos de recursos:

* Acesso a recursos em um grupo de recursos. O acesso pode ser concedido a todos os recursos em um grupo ou somente serviços selecionados em um grupo.
* Acesso para permitir que os usuários gerenciem o grupo, o que significa que os usuários podem visualizar o grupo, editar o nome do grupo, gerenciar o acesso a outros para gerenciar o grupo e o mais importante para criar e incluir novas instâncias de serviço em um grupo.

Revise a tabela a seguir para obter mais informações sobre os dois tipos de acesso e o que cada função do IAM da plataforma designada fornece a um usuário a capacidade de fazer:

| Detalhes da política de acesso  | Ações para acesso em grupos de recursos | Ação em recursos em grupos de recursos | 
|:-----------------|:--------------|:---------------|
| Designar acesso a | Grupo de recursos selecionados | Serviço selecionado em um grupo de recursos |
| Função de visualizador  | Visualizar o grupo e suas características, mas não os recursos no grupo | Visualizar recursos no grupo | 
| Função de operador | Não aplicável | Não aplicável | 
| Função do editor | Visualizar ou editar o nome ou outras características do grupo, mas não os recursos no grupo | Criar, excluir, editar, suspender, continuar, visualizar, ligar e gerenciar o acesso de recursos no grupo de recursos |
| Função de administrador |  Visualizar, editar ou gerenciar o acesso para o grupo, mas não os recursos no grupo | Criar, excluir, editar, suspender, continuar, visualizar, ligar e gerenciar o acesso de recursos no grupo de recursos | 
{: caption="Tabela 1. Acesso para grupos de recursos" caption-side="top"}

Se você deseja que um usuário crie uma nova instância de serviço e inclua-a em um grupo de recursos, o usuário deve ser designado como um Visualizador ou superior no grupo de recursos e Editor ou acima no serviço.
{: tip}


## As políticas de acesso de amostra

Revise as políticas de acesso de amostra a seguir para ajudá-lo a determinar como você pode desejar designar acesso aos recursos em sua conta que pertencem a grupos de recursos.

1. Uma política que concede ao usuário a Função de plataforma “Administrador” no {{site.data.keyword.Bluemix_notm}} Container Service na conta inteira. Uma política com esses detalhes permite ao usuário acesso a todas as instâncias desse serviço e permite que o usuário crie instâncias do serviço em qualquer grupo de recursos no qual o usuário tenha pelo menos a função de Visualizador. Os usuários com a função de Administrador em qualquer recurso também podem conceder a outros usuários acesso a esse recurso.
2. Uma política que concede ao usuário a Função de plataforma “Visualizador” em um grupo de recursos, mas não seus recursos de membros. Uma política com esses detalhes permite ao usuário visibilidade para o grupo de recursos, que é necessária para criar instâncias de qualquer serviço nesse grupo de recursos.
3. Uma política que concede ao usuário a Função de plataforma “Editor” em todos os recursos no grupo de recursos. Um usuário com a função de Editor em um recurso pode editar ou excluir esse recurso.
4. Uma política que concede ao usuário a Função de plataforma “Administrador” na conta inteira (todos os serviços ativados por IAM). Uma política com esses detalhes permite que o usuário execute quaisquer ações da plataforma em qualquer recurso na conta inteira e também inclui a capacidade de executar ações de gerenciamento na conta, como gerenciar os grupos de recursos na conta.

## Exemplos de Caso de Uso

Para cada um desses casos de uso, se tiver um grupo de usuários que você deseja que todos tenham o mesmo nível de acesso, inclua-os em um [grupo de acesso](/docs/iam/groups.html#groups). Usando grupos de acesso, é possível usar um número mínimo de políticas de acesso, já que todos os membros do grupo de acesso herdam qualquer acesso que esteja designado ao grupo.
{: tip}

<ol>
<li><p>Eu tenho uma conta pequena com somente 10 usuários, que trabalham todos juntos em um único projeto. Alguns desses usuários precisam gerenciar a conta e designar acesso a outros usuários. Alguns dos usuários precisam provisionar instâncias de serviço, que incorrerão em despesas. Outros usuários são desenvolvedores de aplicativos que precisam somente usar as instâncias de serviço de seus componentes de aplicativos.</p>
<p>Todos esses usuários devem ter várias funções concedidas na conta e no grupo de recursos padrão, não há necessidade de criar grupos de recursos adicionais para separar recursos ou restringir alguns usuários de acessar alguns dos recursos. É possível conceder aos usuários as funções apropriadas às suas necessidades na conta e no grupo de recursos padrão – Administrador na conta para usuários que precisam gerenciar a conta e fornecer acesso aos outros, Editor no grupo de recursos padrão e em seus membros para usuários que precisam provisionar instâncias de serviço e Gravador ou Leitor nos membros do grupo de recursos para usuários que precisam apenas usar as instâncias de serviço.</p>
</li>
<li><p>Eu tenho uma conta que inclui três equipes diferentes que trabalham em três projetos. Poucos usuários são administradores e precisam da capacidade para criar novos grupos de recursos e designar acesso de usuários a grupos de recursos. Os usuários restantes precisam somente de acesso ao grupo de recursos associado ao seu projeto.</p>
<p>Eu designaria aos administradores a função de Administrador em todos os serviços ativados pelo IAM. Eu designaria aos usuários restantes várias funções nos membros do grupo de recursos e do grupo de recursos que estão associados ao seu projeto - Editor do grupo de recursos para aqueles que precisam criar instâncias, mais Leitor ou Gravador do membro do grupo de recursos para aqueles que precisam usar as instâncias.</p>
</li>
<li><p>Eu tenho uma conta com múltiplos grupos de recursos. Eu tenho alguns usuários que são os administradores para o Serviço A em toda a minha conta e precisam de acesso para todas as instâncias desse serviço, bem como a capacidade de criar instâncias, mas esses usuários não precisam de acesso para quaisquer outros recursos na conta.</p>
<p>Eu designaria a esses usuários a função de Administrador no Serviço A no nível da conta, bem como designando a eles a função de Visualizador a todos os grupos de recursos na conta em que eles precisam criar instâncias.</p>
</li>
<li><p>Eu tenho um usuário em minha conta que precisa somente de acesso a um recurso específico em um serviço, por exemplo a capacidade de gravar em um Depósito A no IBM Cloud Object Storage. Esse usuário não deve ver os grupos de recursos em minha conta ou acessar quaisquer outros serviços ou quaisquer outros depósitos nessa instância do Cloud Object Storage.</p> 
<p>Eu daria a esse usuário a função de Gravador no Depósito A na instância específica de Cloud Object Storage. É possível conceder essa política usando interfaces específicas de serviço (a IU do Cloud Object Storage, neste exemplo) ou a IU principal de Designar acesso. A IU específica do serviço é recomendada porque permite escolher em uma lista de recursos, enquanto a IU de Designar acesso não exibe recursos abaixo do nível da instância de serviço e você precisaria inserir manualmente o CRN para designar a política a esses recursos.</p>
</li>
<li><p>Eu estou usando organizações e espaços do Cloud Foundry hoje, mas eu vou começar usando grupos de recursos e grupos de acesso para os meus serviços ativados pelo IAM. Atualmente, meus usuários e recursos são organizados em organizações para linhas de negócios e os espaços são usados para diferentes projetos dentro de uma linha de negócios.</p>
<p>Eu usaria grupos de recursos para organizar recursos da mesma maneira que fiz com espaços, considerando cada grupo de recursos como um espaço do projeto. Em seguida, eu configuraria grupos de acesso separados para fornecer o acesso necessário aos meus usuários para os grupos de recursos de nível de projeto certos. O acesso pode ser fornecido a todos os recursos em um grupo de recursos ou mesmo a apenas um grupo seleto de recursos em um grupo de recursos. Portanto, é possível configurar cada grupo de acesso com diferentes níveis de acesso aos recursos dentro de um grupo de recursos, o que fornece a cada grupo de usuários o acesso que eles requerem para trabalhar com os recursos ou o próprio grupo de recursos.</p>
</li>
</ol>


