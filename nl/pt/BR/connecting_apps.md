---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}

# Gerenciando conexões
{: #connect_app}

É possível conectar um serviço a um aplicativo {{site.data.keyword.Bluemix}} existente ou novo na guia **Conexões** do painel de serviço. Conectar um serviço a um aplicativo cria uma ligação entre eles. É possível desvincular, incluir mais conexões ou excluir conexões da guia **Conexões**.

No entanto, quando você conecta uma instância de serviço gerenciada pelo Identity and Access Management (IAM) do {{site.data.keyword.Bluemix_notm}} a um aplicativo, um alias do serviço gerenciado pelo IAM é criado automaticamente no espaço correspondente com as informações de ligação especificadas. Esse alias é representado como uma instância de serviço do serviço gerenciado pelo IAM.
{:shortdesc}

## O que é um alias?
{: #what_is_alias}

Um alias é uma conexão entre o serviço gerenciado pelo IAM em um grupo de recursos e um aplicativo dentro de uma organização ou um espaço. No console do {{site.data.keyword.Bluemix_notm}}, a conexão (alias) é representada como uma instância de serviço. É possível gerenciar seus alias modificando a instância de serviço que representa sua conexão.

Os aliases são como links simbólicos que contêm referências a recursos remotos e permitem a interoperabilidade e a reutilização de uma instância na plataforma. Por exemplo, é possível criar uma instância de um serviço em um grupo de recursos e, em seguida, reutilizá-la em qualquer região disponível criando um alias em uma organização ou um espaço nessas regiões.

As regras a seguir se aplicam a aliases:

* Não há encargos extras para um alias, mas cada alias é contado com relação à sua cota em sua organização.
* É possível criar apenas um alias por espaço no console do {{site.data.keyword.Bluemix_notm}}. No entanto, mais de um alias por espaço pode ser criado usando a CLI do {{site.data.keyword.Bluemix_notm}}. Para obter mais informações, consulte [Trabalhando com recursos e grupos de recursos](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource).
* Será possível criar múltiplas conexões entre seu serviço gerenciado pelo IAM e qualquer aplicativo em qualquer espaço, organização e região na mesma conta se você tiver permissão.
* Múltiplas conexões feitas no mesmo espaço para diferentes apps por meio de uma instância de serviço gerenciada pelo IAM usam o mesmo alias.
* A desvinculação de uma instância de serviço gerenciada pelo IAM *não* exclui a instância de serviço que representa o alias.
* Excluir o aplicativo ao qual sua instância de serviço gerenciada pelo IAM está conectada *não* exclui a instância que representa o alias.
* Excluir uma instância de serviço gerenciada pelo IAM *exclui* a instância de serviço que representa o alias.

## Criando uma conexão (alias) entre um serviço gerenciado pelo IAM e um app
{: #creating_alias}

Para conectar sua instância de serviço gerenciada pelo IAM a um aplicativo:

1. Acesse seu painel.

2. Clique no nome do seu app para abrir a visualização de detalhes do app.

3. Clique em **Conectar existente** e escolha em seu app existente. Ou clique em **Criar conexão** para criar um app ao qual se conectar.

4. Especifique a **Função de acesso para conexão**. Este valor configura a função de acesso do serviço IAM. Para obter mais informações, veja [Acesso ao IAM](/docs/iam?topic=iam-userroles).

5. Opcionalmente, é possível fornecer um **ID de serviço para conexão**, permitindo que o IAM gere um valor exclusivo para você ou fornecendo um ID de serviço existente. Para obter mais informações, consulte [Criando e trabalhando com IDs de serviço](/docs/iam?topic=iam-serviceids).

6. Clique em **Criar**.

## Visualizando um alias
{: #view_alias}

Depois que você cria uma conexão entre um serviço gerenciado pelo IAM e um app, o alias é exibido na guia **Conexões** do app conectado. Além disso, o alias é exibido como uma instância de serviço em execução em sua lista de recursos e contém uma guia **Conexões** apenas quando você o abre.

1. Acesse sua lista de recursos.
2. Na tabela **Application Services**, clique no nome da instância de serviço para abrir a visualização de detalhes do serviço. Se ela tiver somente uma guia **Conexões**, ela será um alias.

## Excluindo um alias
{: #delete_alias}

A maneira mais fácil de excluir o alias é excluir a instância de serviço gerenciada pelo IAM. No entanto, é possível manter sua instância de serviço gerenciado pelo IAM e excluir o alias diretamente.

1. Acesse sua lista de recursos.
2. Na tabela **Application Services**, clique no nome da instância de serviço para abrir a visualização de detalhes do serviço. Se ela tiver somente uma guia **Conexões**, ela será um alias.
3. Exclua a instância.

## Criando uma conexão entre vários serviços
{: #multiple_services}

Para obter mais informações, veja [Usando serviços em outro serviço](/docs/resources?topic=resources-s2s_binding).
