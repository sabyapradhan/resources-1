---

copyright:
  years: 2015, 2018
lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}

# Usando serviços em uma outra região
{: #cross_region_service}

Se você tiver uma instância de serviço criada e ligada a apps em uma região, será possível usar essa instância de serviço em uma outra região com um dos métodos a seguir:
{: shortdesc}

  * Use as credenciais de serviço para configurar sua instância do app diretamente. Consulte [Ativando aplicativos externos para usar o serviço do {{site.data.keyword.Bluemix_notm}}](/docs/apps/reqnsi.html#accser_external){: new_window} para obter detalhes.
  * Crie um serviço fornecido pelo usuário como uma ponte.

	Para usar uma instância de serviço existente
em uma outra região, conclua as etapas a seguir:

      1. Alterne para a região em que a instância de serviço existe. Na barra de menus do {{site.data.keyword.Bluemix_notm}}, expanda o menu **Região** e, em seguida, selecione a região na qual a instância de serviço existe.

      2. Recupere as credenciais e os parâmetros de conexão da variável de ambiente VCAP_SERVICES da instância de serviço na região na qual o serviço existe. Conclua
as etapas a seguir:

	       1. No Painel do {{site.data.keyword.Bluemix_notm}}, clique no tile do aplicativo. A página Visão geral é exibida.
	       2. Na área de janela de navegação, clique em **Credenciais**. Os detalhes da variável de ambiente *VCAP_SERVICES* são exibidos. Registre o conteúdo JSON para a
instância de serviço.

      3. Alterne para a região em que você deseja usar a instância de
serviço. Na barra de menus do {{site.data.keyword.Bluemix_notm}}, expanda o menu **Região** e, em seguida, selecione a região na qual você deseja usar a instância de serviço.

      4. Crie uma instância de serviço fornecida pelo usuário usando as credenciais
e os parâmetros de conexão que você registrou a partir da variável de ambiente
*VCAP_SERVICES*. Para obter informações sobre como criar uma instância de serviço fornecida pelo usuário, consulte [Criando uma instância de serviço fornecida pelo usuário](/docs/apps/reqnsi.html#user_provide_services).

      5. Ligue a instância de serviço fornecida pelo usuário ao seu app
usando o comando a seguir:

	     ```
	     bluemix service bind myapp user-provided_service_instance
	     ```
