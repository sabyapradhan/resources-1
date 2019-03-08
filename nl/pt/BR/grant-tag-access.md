---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: tagging, enabling others to tag, tagging permissions

subcollection: resources

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Concedendo aos usuários acesso aos recursos de tag
{: #access}

Como proprietário da conta, talvez você queira delegar algumas das responsabilidades de recursos de identificação. Para fazer isso, é possível conceder acesso a outros usuários na conta para incluir e remover tags de recursos. Para que os usuários na conta incluam tags em um recurso, eles devem ter o acesso apropriado designado. O acesso a serviços que pertencem a um grupo de recursos é gerenciado pelas políticas de acesso do {{site.data.keyword.Bluemix}} Identity and Access Management (IAM), e o acesso aos serviços que pertencem a uma organização e um espaço do Cloud Foundry é gerenciado pelas funções de espaço e organização do Cloud Foundry.
{: shortdesc}

## Identificando permissões
{: #tagging-permissions}

As tags ficam visíveis para qualquer usuário em uma conta. Quando um recurso é identificado, a tag fica visível para todos os usuários que têm acesso de leitura para o recurso. Para incluir ou remover uma tag de um recurso, determinadas funções ou permissões de acesso são necessárias dependendo do tipo de recurso. Confira a tabela a seguir para entender qual função é necessária para cada tipo de recurso.


| Tipo de recurso | Função |
|--------|---------------|
| Ativado para IAM | Editor ou Administrador no recurso |
| Cloud Foundry | Função de desenvolvedor no espaço ao qual o recurso pertence  |
| Infraestrutura clássica*| Visualizar a permissão de detalhes de hardware ou visualizar a permissão de detalhes do servidor virtual |
| Cloud Object Storage S3 na infraestrutura clássica | Permissão de gerenciamento de armazenamento |
{: caption="Tabela 1. Funções necessárias para incluir e remover tags" caption-side="top"}

*Os recursos identificáveis na infraestrutura clássica são Convidados virtuais, Host dedicado virtual, Controlador de entrega de aplicativo de rede, Membro do gateway, Sub-rede, VLAN e Firewall de VLAN (Dedicado).


## Concedendo acesso para identificação de recursos ativados pelo IAM
{: #iam-managed}

Os recursos que pertencem a um grupo de recursos são gerenciados pelas políticas de acesso do {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM). Conclua as etapas a seguir para designar a função de Editor a um usuário para identificar recursos ativados pelo IAM:

  1. No console do {{site.data.keyword.Bluemix_notm}}, clique em **Gerenciar > Acesso (IAM) ** e selecione **Usuários**.
  2. Clique no nome do usuário ao usuário ao qual você está concedendo acesso.
  3. Clique em **Políticas de acesso** > **Designar acesso**.
  4. Selecione a opção **Designar acesso aos recursos**.
  5. Na lista de serviços, selecione um serviço específico ou **Todos os serviços ativados de identidade e acesso**.
  6. Na lista de funções de acesso da plataforma, selecione **Editor**.
  7. Clique em **Designar**.

## Concedendo acesso para identificar recursos do Cloud Foundry
{: #cf_tag_access}

Os recursos pertencentes a uma organização e um espaço do Cloud Foundry são gerenciados pelas funções de organização e espaço do Cloud Foundry. Conclua as etapas a seguir para designar a função de espaço do Desenvolvedor a um usuário para identificar os recursos do Cloud Foundry:

 1. Clique em **Gerenciar > Acesso (IAM)** e selecione **Usuários**.
2. Selecione o nome para o usuário ao qual você deseja fornecer acesso.
3. Clique em **Acesso do Cloud Foundry**.
4. Clique em **Designar organização**.
5. Expanda e selecione a `Organização` com a instância de serviço à qual você deseja fornecer o acesso de usuário.
6. Selecione a região.
7. Selecione a função de espaço **Desenvolvedor**.
8. Clique em **Salvar função**.

## Concedendo acesso para identificação de recursos de infraestrutura clássica
{: #classic-infra}

Conclua as etapas a seguir para designar a função de acesso de serviço do Gerenciador a um usuário para identificar os serviços de infraestrutura clássica:

  1. Clique em **Gerenciar > Acesso (IAM)** e selecione **Usuários**.
  2. Clique no nome do usuário ao usuário ao qual você está concedendo acesso.
  3. Clique em **Infraestrutura clássica**
  4. Na guia **Permissões**, expanda a categoria **Dispositivos**.
  5. Selecione **Visualizar detalhes do hardware** e **Visualizar detalhes do Virtual Server**. Se for necessário designar acesso ao Cloud Object Storage S3, designe a permissão **Gerenciar armazenamento**.
  6. Clique em **Salvar**.
  7. Clique na guia **Dispositivos**.
  8. Selecione **Todos os servidores bare metal** ou **Todos os servidores virtuais**, dependendo do recurso que você gostaria de identificar.
