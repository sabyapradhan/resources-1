---

copyright:

  years: 2015, 2019
lastupdated: "2019-04-08"

keywords: service key, api key, bind, credential

subcollection: resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:note: .note}


# Incluindo e visualizando credenciais
{: #service_credentials}

É possível gerar um novo conjunto de credenciais para casos em que você deseja conectar manualmente um consumidor externo a um serviço {{site.data.keyword.Bluemix}}. Por exemplo, se você estiver tentando ligar um app AWS a um serviço do Watson, será necessário gerar uma nova credencial que possa ser usada para ligá-los.

## Incluindo uma credencial ao ligar um serviço ativado pelo IAM
{: #IAM}

Os serviços que são gerenciados pelo {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) podem gerar uma chave de recursos, também conhecida como uma credencial. Credenciais são específicas do serviço e variam com base em como cada serviço
define as credenciais que eles precisam gerar. Uma credencial pode conter um nome do usuário, senha, nome do host, porta e uma URL.

No entanto, embora os conteúdos de cada credencial sejam exclusivos para o serviço que os gera, todos os serviços gerenciados pelo IAM requerem que novas credenciais incluam uma função de acesso ao serviço IAM. Alguns serviços podem gerar mais dados que requerem que parâmetros sejam passados. Por exemplo, um serviço pode requerer que você insira um parâmetro de linguagem para configurar a linguagem padrão que é retornada na chave de recursos gerada.

Conclua as etapas a seguir para incluir uma credencial em um serviço que é gerenciado pelo IAM:

1. Na lista de recursos, selecione o nome do serviço para abrir a página de detalhes do serviço. Em seguida, selecione a guia Credenciais e clique em **Nova credencial +**.
2. No diálogo Incluir nova credencial, forneça um **Nome**.
3. Especifique a função. Este valor configura a função de acesso do serviço IAM. Para obter mais informações, veja: [Acesso ao IAM](/docs/iam?topic=iam-userroles)
4. Opcionalmente, é possível fornecer um ID de serviço permitindo que o IAM gere um valor exclusivo para você ou fornecendo um ID de serviço existente. Para obter mais informações, consulte: [Criando e trabalhando com IDs de serviço](/docs/iam?topic=iam-serviceids)
5. Opcionalmente, é possível fornecer mais parâmetros como um objeto JSON válido que contém parâmetros de configuração específicos do serviço, fornecidos sequencialmente ou em um arquivo.

  A maioria dos serviços não requer parâmetros extras e, para serviços que fazem isso, cada serviço define sua própria lista exclusiva de parâmetros. Para obter uma lista de parâmetros de configuração suportados, veja a documentação para a oferta de serviços específica.
  {: note}
6. Clique em **Incluir** para gerar a nova credencial de serviço.

## Incluindo uma credencial ao ligar um serviço Cloud Foundry
{: #cf_credential}

Os serviços do Cloud Foundry podem gerar uma chave de serviço, também conhecida como credencial. Credenciais são específicas do serviço e variam com base em como cada serviço
define as credenciais que eles precisam gerar. Uma credencial de serviço pode conter um nome do usuário, senha, nome do host, porta e uma URL.

No entanto, os conteúdos de cada credencial são exclusivos para o serviço que os gera. Alguns serviços podem gerar dados extras que requerem que parâmetros sejam passados. Por exemplo, um serviço pode requerer que você insira um parâmetro de linguagem para configurar a linguagem padrão que é retornada na chave de serviço gerada.

Conclua as etapas a seguir para incluir uma credencial do Cloud Foundry:

1. Na página de detalhes do serviço, selecione a guia Credenciais e clique em **Nova credencial + **.
2. No diálogo Incluir nova credencial, forneça um **Nome**.
3. Opcionalmente, é possível fornecer mais parâmetros como um objeto JSON válido que contém parâmetros de configuração específicos do serviço, fornecidos sequencialmente ou em um arquivo.

  A maioria dos serviços não requer parâmetros extras e, para serviços que fazem isso, cada serviço define sua própria lista exclusiva de parâmetros. Para obter uma lista de parâmetros de configuração suportados, veja a documentação para a oferta de serviços específica.
  {: note}
4. Clique em **Incluir** para gerar a nova credencial de serviço.

## Visualizando uma credencial
{: #viewing-credentials}

Depois que uma credencial é criada para um serviço, ela pode ser visualizada a qualquer momento para usuários que precisam do valor da chave de API. No entanto, todos os usuários devem ter o nível correto de acesso para ver os detalhes de uma credencial, incluindo o valor da chave de API. O acesso do usuário deve ser igual ou maior que o da credencial de serviço. Por exemplo, se a credencial tiver a função de serviço do IAM `Writer`, o usuário que estiver tentando visualizar a credencial deverá ter a função de serviço do IAM `Writer` ou `Manager` para esse serviço específico designado. Quando um usuário não tiver o acesso correto, os detalhes, como o valor da chave de API, serão editados.

Para visualizar uma credencial de serviço existente para um serviço, conclua as etapas a seguir:

1. Na lista de Recursos, selecione o nome do serviço para abrir a página de detalhes do serviço. 
2. Clique em **Credenciais de serviço**
3. Expanda **Visualizar credenciais** na linha para uma credencial existente.

