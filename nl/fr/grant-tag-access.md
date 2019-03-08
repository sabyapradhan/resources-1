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


# Octroi aux utilisateurs de l'accès leur permettant d'étiqueter des ressources
{: #access}

En tant que propriétaire de compte, vous pouvez souhaiter déléguer certaines des responsabilités de l'étiquetage de ressources. Pour cela, vous pouvez octroyer l'accès à d'autres utilisateurs du compte leur permettant d'ajouter et de retirer des étiquettes dans des ressources. Pour que les utilisateurs du compte puissent ajouter des étiquettes à une ressource, ils doivent disposer de l'accès approprié. L'accès aux services qui appartiennent à un groupe de ressources est géré par les règles d'accès {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) et l'accès aux services qui appartiennent à un espace et une organisation Cloud Foundry est géré par les rôles d'espace et d'organisation Cloud Foundry.
{: shortdesc}

## Droits d'étiquetage
{: #tagging-permissions}

Les étiquettes sont visibles de tout utilisateur d'un compte. Une fois qu'une ressource est étiquetée, l'étiquette est visible par tous les utilisateurs ayant un accès en lecture à la ressource. Pour ajouter ou retirer une étiquette à une ressource, certains droits ou rôles d'accès sont requis en fonction du type de ressource. Consultez le tableau suivant pour savoir quel rôle est requis pour chaque type de ressource.


| Type de ressource | Rôle |
|--------|---------------|
| Activé par IAM | Editeur ou Administrateur pour la ressource |
| Cloud Foundry | Rôle Développeur pour l'espace auquel appartient la ressource  |
| Infrastructure classique*| Droits d'affichage des détails de matériel ou droits d'affichage des détails de serveur virtuel |
| Cloud Object Storage S3 sur l'infrastructure classique | Droits de gestion de stockage |
{: caption="Tableau 1. Rôles requis pour l'ajout ou le retrait d'étiquettes" caption-side="top"}

*Les ressources pouvant être étiquetées dans l'infrastructure classique sont les suivantes : Invité virtuel, Hôte virtuel dédié, Contrôleur de livraison d'applications réseau, Membre de passerelle, Sous-réseau et Pare-feu de sous-réseau (dédié).


## Octroi de l'accès pour l'étiquetage des ressources activées par IAM
{: #iam-managed}

Les ressources qui appartiennent à un groupe de ressources sont gérées par les règles d'accès {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM). Procédez comme suit pour affecter le rôle Editeur afin qu'un utilisateur puisse étiqueter les ressources activées par IAM :

  1. Dans la console {{site.data.keyword.Bluemix_notm}}, cliquez sur **Gérer > Accès (IAM)** puis sélectionnez **Utilisateurs**.
  2. Cliquez sur le nom de l'utilisateur auquel vous octroyez l'accès.
  3. Cliquez sur **Règles d'accès** > **Affecter un accès**.
  4. Sélectionnez l'option **Affecter l'accès aux ressources**.
  5. Dans la liste des services, sélectionnez un service spécifique ou **Tous les services avec l'offre Identity and Access activée**.
  6. Dans la liste des rôle d'accès de la plateforme, sélectionnez **Editeur**.
  7. Cliquez sur **Affecter**.

## Octroi de l'accès pour l'étiquetage des ressources Cloud Foundry
{: #cf_tag_access}

Les ressources appartenant à un espace et à une organisation Cloud Foundry sont gérées par les rôles d'espace et d'organisation Cloud Foundry. Procédez comme suit pour affecter le rôle d'espace Développeur afin qu'un utilisateur puisse étiqueter les ressources Cloud Foundry :

 1. Cliquez sur **Gérer > Accès (IAM)** puis sélectionnez **Utilisateurs**.
2. Sélectionnez le nom de l'utilisateur auquel vous souhaitez fournir l'accès.
3. Cliquez sur **Accès Cloud Foundry**.
4. Cliquez sur **Affecter une organisation**.
5. Développez et sélectionnez l'`organisation` avec l'instance de service à laquelle vous souhaitez que l'utilisateur ait accès.
6. Sélectionnez la région.
7. Sélectionnez le rôle d'espace **Développeur**.
8. Cliquez sur **Sauvegarder un rôle**.

## Octroi de l'accès pour l'étiquetage des ressources de l'infrastructure classique
{: #classic-infra}

Procédez comme suit pour affecter le rôle d'accès Responsable pour qu'un utilisateur puisse étiqueter les services de l'infrastructure classique :

  1. Cliquez sur **Gérer > Accès (IAM)** puis sélectionnez **Utilisateurs**.
  2. Cliquez sur le nom de l'utilisateur auquel vous octroyez l'accès.
  3. Cliquez sur **Infrastructure classique**.
  4. Dans l'onglet **Droits**, développez la catégorie **Périphériques**.
  5. Sélectionnez **Afficher les informations détaillées sur le matériel** et **Afficher les détails du serveur virtuel**. Si vous avez besoin d'affecter l'accès à Cloud Object Storage S3, affectez le droit **Gestion de stockage**.
  6. Cliquez sur **Sauvegarder**.
  7. Cliquez sur l'onglet **Périphériques**.
  8. Sélectionnez **Tous les serveurs bare metal** ou **Tous les serveurs virtuels** en fonction de la ressource à étiqueter.
