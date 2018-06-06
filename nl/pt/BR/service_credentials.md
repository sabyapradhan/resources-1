---

copyright:

  years: 2015, 2018
lastupdated: "2018-02-13"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}


# Incluindo uma nova credencial
{: #service_credentials}

É possível gerar um novo conjunto de credenciais para casos em que você deseja conectar manualmente um consumidor externo a um serviço {{site.data.keyword.Bluemix}}. Por exemplo, se você estiver tentando ligar um app AWS a um serviço do Watson, será necessário gerar uma nova credencial que possa ser usada para ligá-los juntos.

## Incluindo uma credencial ao ligar um serviço ativado pelo IAM
{: #IAM}

Os serviços que são gerenciados pelo {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) podem gerar uma chave de recursos, também conhecida como uma credencial. Credenciais são específicas do serviço e variam com base em como cada serviço
define as credenciais que eles precisam gerar. Uma credencial pode conter um nome de usuário, senha, nome do host, porta e uma URL. 

No entanto, embora os conteúdos de cada credencial sejam exclusivos para o serviço que os gera, todos os serviços gerenciados pelo IAM requerem que novas credenciais incluam uma função de acesso ao serviço IAM. Alguns serviços podem gerar dados adicionais que requerem que parâmetros sejam passados. Por exemplo, um serviço pode requerer que você insira um parâmetro de linguagem para configurar a linguagem padrão retornada na chave de recursos que é gerada. 

Conclua as etapas a seguir para incluir uma nova credencial em um serviço que é gerenciado pelo IAM:

1. No painel, selecione o nome do serviço para abrir a página de detalhes do serviço. Em seguida, selecione a guia Credenciais e clique em **Nova credencial +**.
2. No diálogo Incluir nova credencial, forneça um **Nome**.
3. Especifique a função. Este valor configura a função de acesso do serviço IAM. Para obter mais informações, veja: [Acesso ao IAM](/docs/iam/users_roles.html#userroles)
4. Opcionalmente, é possível fornecer um ID de serviço permitindo que o IAM gere um valor exclusivo para você ou fornecendo um ID de serviço existente. Para obter mais informações, veja: [Criando e gerenciando IDs de serviço](https://console.stage1.bluemix.net/docs/iam/serviceid.html#serviceids)
3. Opcionalmente, é possível fornecer parâmetros adicionais como um objeto JSON válido contendo parâmetros de configuração específicos do serviço, fornecidos sequencialmente ou em um arquivo.

  **Nota**. A maioria dos serviços não requer parâmetros adicionais e para serviços que o requerem, cada serviço define sua própria lista exclusiva de parâmetros. Para obter uma lista de parâmetros de configuração suportados, veja a documentação para a oferta de serviços específica.
4. Clique em **Incluir** para gerar a nova credencial de serviço.

## Incluindo uma credencial ao ligar um serviço Cloud Foundry
{: #cf}

Os serviços do Cloud Foundry podem gerar uma chave de serviço, também conhecida como credencial. Credenciais são específicas do serviço e variam com base em como cada serviço
define as credenciais que eles precisam gerar. Uma credencial de serviço pode conter um nome de usuário, uma senha, um nome de host, uma porta e uma URL. 

No entanto, os conteúdos de cada credencial são exclusivos para o serviço que os gera. Alguns serviços podem gerar dados adicionais que requerem que parâmetros sejam passados. Por exemplo, um serviço pode requerer que você insira um parâmetro de idioma para configurar o idioma padrão retornado na chave de serviço que é gerada. 

Conclua as etapas a seguir para incluir uma nova credencial do Cloud Foundry:

1. Na página de detalhes do serviço, selecione a guia Credenciais e clique em **Nova credencial + **.
2. No diálogo Incluir nova credencial, forneça um **Nome**.
3. Opcionalmente, é possível fornecer parâmetros adicionais como um objeto JSON válido contendo parâmetros de configuração específicos do serviço, fornecidos sequencialmente ou em um arquivo.

  **Nota**. A maioria dos serviços não requer parâmetros adicionais e para serviços que o requerem, cada serviço define sua própria lista exclusiva de parâmetros. Para obter uma lista de parâmetros de configuração suportados, veja a documentação para a oferta de serviços específica.
4. Clique em **Incluir** para gerar a nova credencial de serviço.

