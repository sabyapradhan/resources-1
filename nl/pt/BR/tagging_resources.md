---

copyright:

  years: 2018
lastupdated: "2018-11-27"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Trabalhando com tags
{: #tag}

Uma tag é um rótulo que você designa a um recurso para filtragem fácil de recursos em sua lista de recursos. É possível usar tags para organizar seus recursos e localizá-los com facilidade posteriormente.  
{: shortdesc}

Para ver uma lista completa de tags em sua conta, acesse **Gerenciar > Conta** e selecione **Tags**.

## Regras e limitações de tag
{: #limits}

O tamanho máximo de uma tag é 128 caracteres. Os caracteres permitidos são A-Z, 0-9, espaço em branco, sublinhado, hífen, ponto e dois pontos, e as tags não fazem distinção entre maiúsculas e minúsculas. Os dois pontos transformam a tag em um par `key:value`. Não é possível usar dois pontos em uma tag sem criar um par `key:value`. Uma vírgula separa as tags, portanto, as vírgulas não podem ser usadas dentro do próprio nome da tag.


## Incluindo e removendo tags em um recurso
{: #add-remove}

1. No console do {{site.data.keyword.Bluemix_notm}}, clique no ícone Menu ![Ícone Menu](../icons/icon_hamburger.svg) > **Lista de recursos** para visualizar sua lista de recursos. 
2. Expanda a seta de tipo de recurso que contém o recurso que você deseja identificar. Por exemplo, se você deseja identificar uma instância do {{site.data.keyword.cos_full_notm}}, expanda **Armazenamento**.  
3. Clique no ícone Ações ![Ícone Ações](../icons/action-menu-icon.svg) para incluir ou atualizar uma tag para o recurso. 

    * Para incluir uma tag, clique no menu Ações ![Ícone Ações](../icons/action-menu-icon.svg), selecione **Incluir tags** e digite um nome para sua tag. 
    * Para incluir tags adicionais, clique no ícone Editar ![Ícone Editar](../icons/edit-tagging.svg) próximo à tag exibida e digite um nome para a sua tag. Pressione Enter para continuar a incluir tags.
4. Para remover uma tag, clique no ícone Editar ![Ícone Editar](../icons/edit-tagging.svg). Em seguida, clique no ícone Remover ![Ícone Remover](../icons/close-tagging.svg) próximo à tag. 

## Procurando tags
{: #search-tags}

É possível procurar tags usando qualquer um dos métodos a seguir:

  * Tente a barra de procura que está localizada na barra de menus do console do {{site.data.keyword.Bluemix_notm}}.
  * É possível filtrar sua lista de recursos pela tag que você está procurando.
  * Na da página de detalhes do aplicativo, é possível localizar as tags que estão associadas a esse recurso.

A mesma tag pode ser anexada a vários recursos por diferentes usuários na mesma conta de cobrança e nem todos os usuários têm visibilidade em todos os recursos na conta.
{: note}


## Identificação para revendedores
{: #resell}

As tags são visíveis para todos os membros de uma conta. Se sua conta estiver associada a diferentes organizações, se você for um revendedor, por exemplo, talvez você queira recomendar a seus clientes para não armazenarem informações em tags que possam divulgar informações confidenciais aos outros na mesma conta.

Para controlar a visibilidade da tag, distribua as diretrizes de identificação e informe aos usuários que as tags são visíveis em toda a conta. 

Use códigos em vez de nomes para clientes e contas e evite colocar informações confidenciais nas tags.
{: tip}

