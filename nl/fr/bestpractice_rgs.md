---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Meilleures pratiques pour l'organisation des ressources dans un groupe de ressources
{: #bp_resourcegroups}

Un groupe de ressources est une fonction permettant d'organiser vos [ressources](/docs/resources?topic=resources-resource) de compte à des fins de contrôle d'accès et de facturation. Si vous êtes habitué à utiliser les espaces Cloud Foundry, vous pouvez être tenté d'organiser les ressources dans des groupes de ressources de la même manière que vous les organisiez dans des espaces. Tout élément pouvant être créé, géré et inclus dans un groupe de ressources est appelé une ressource. Il n'est pas possible d'ajouter d'utilisateurs à des groupes de ressources. Seules des ressources peuvent être ajoutées. 

Actuellement, tous les services ne prennent pas en charge l'utilisation du {{site.data.keyword.Bluemix_notm}} contrôle d'accès IAM (Identity and Access Management) et l'affectation à un groupe de ressources. Les services activés par IAM vous invitent à affecter de nouvelles instances de service à un groupe de ressources lors de leur création à partir du catalogue. L'accès aux ressources d'un groupe de ressources et au groupe lui-même est géré par IAM. En utilisant des rôles IAM, vous pouvez permettre aux utilisateurs d'accéder aux ressources organisées dans les groupes de ressources. Les rôles IAM peuvent également vous permettre d'afficher, de modifier et d'ajouter des instances de service dans un groupe de ressources ou de gérer l'accès à ce dernier.

Vous pouvez également trouver la liste des services activés par IAM lorsque vous affectez l'accès aux ressources à partir de l'interface utilisateur Identity and Access en procédant comme suit :
1. Accédez à **Gérer** &gt; **Accès (IAM)** puis sélectionnez **Utilisateurs**. 
2. Sélectionnez un utilisateur puis cliquez sur **Règles d'accès**. 
3. Sélectionnez **Affecter un accès** > **Affecter l'accès aux ressources**.
4. Dans le menu **Services**, sélectionnez le service à affecter. Pour tous les services ne disposant de prise en charge via l'utilisation d'IAM, vous pouvez continuer à utiliser les rôles, les espaces et les organisations Cloud Foundry. 
5. Cliquez sur **Affecter**.

Les rôles, les espaces et les organisations Cloud Foundry sont séparés des groupes de ressources et des rôles IAM. Un rôle Cloud Foundry ne peut jamais accorder l'accès aux ressources d'un groupe de ressources. 
{: note}


## Configuration de vos groupes de ressources
{: #setuprgs}

Tous les utilisateurs disposent d'un groupe de ressources unique par défaut pouvant être renommé. Affectez le rôle Editeur ou Administrateur à tous les services de gestion des comptes pour créer des groupes de ressources. Si vous avez un compte facturable, vous pouvez créer plusieurs groupes afin d'organiser vos ressources. Ainsi, vous pouvez :

* Affecter l'accès à un ensemble de ressources en utilisant un nombre minimal de règles 
* Afficher par informations d'utilisation de groupe de ressources à des fins de facturation 

Pour créer un groupe de ressources, procédez comme suit :

1. Accédez à **Gérer** > **Compte**. 
2. Développez **Ressources de compte** et sélectionnez **Groupes de ressources**. 
3. Cliquez sur **Créer un groupe de ressources**.
4. Entrez un nom pour le groupe de ressources.
5. Cliquez sur **Ajouter**.

## Ajout de ressources à un groupe de ressources
{: #addingtorgs}

Les services activés à l'aide du contrôle d'accès IAM appartiennent à un groupe de ressources et non à un espace ou à une organisation Cloud Foundry. Lorsque vous créez une instance de service pour l'un de ces services à partir du catalogue, vous êtes invité à affecter l'instance à un groupe de ressources. 

Votre sélection de groupe de ressource au moment de la création de l'instance est définitive et ne peut pas être modifiée.
{: important}

Lorsque des services supplémentaires permettent l'affectation à des groupes de ressources ainsi que l'utilisation du contrôle d'accès IAM, vous recevez des notifications sur votre liste de ressources si vous disposez d'instances de service Cloud Foundry éligibles à la migration. En [migrant une instance de service vers un groupe de ressources](/docs/resources?topic=resources-migrate), vous créez une instance liée dans un groupe de ressources de votre choix et l'instance Cloud Foundry devient un alias. 


## Affectation de l'accès à des groupes de ressources et aux ressources s'y trouvant
{: #assigning_access_rgs}

En créant des règles, vous octroyez l'accès aux utilisateurs ou aux groupes d'utilisateurs organisés dans des groupes d'accès. Les règles d'accès définissent une cible, qui est généralement une instance de service ou toutes les instances d'un service d'un groupe de ressources, qui définit le type d'accès autorisé. Il existe deux types de règle d'accès que vous devez affecter en tant que propriétaire de compte afin de permettre aux utilisateur de votre compte d'accéder aux ressources des groupes de ressources :

* Accès aux ressources dans un groupe de ressources. L'accès peut être accordé à toutes les ressources d'un groupe ou uniquement aux services sélectionnés d'un groupe.
* Accès afin de permettre aux utilisateurs de gérer le groupe, ce qui signifie que les utilisateurs peuvent voir le groupe, modifier son nom, gérer l'accès permettant à d'autres utilisateurs de gérer le groupe et surtout de créer et d'ajouter de nouvelles instances de service à un groupe.

Consultez le tableau suivant pour plus d'informations sur les deux types d'accès et savoir ce que chaque rôle IAM de plateforme affecté peut permettre à un utilisateur de faire :

| Détails de la règle d'accès  | Actions liées à l'accès dans des groupes de ressources | Action concernant les ressources des groupes de ressources | 
|:-----------------|:--------------|:---------------|
| Affecter l'accès à | Groupe de ressources sélectionné | Service sélectionné dans un groupe de ressources |
| Rôle Afficheur  | Afficher le groupe et ses caractéristiques mais non les ressources du groupe | Afficher les ressources du groupe | 
| Rôle Opérateur | Non applicable | Non applicable | 
| Rôle Editeur | Afficher ou modifier le nom ou d'autres caractéristiques du groupe, mais non les ressources du groupe | Créer, supprimer, modifier, suspendre, reprendre, afficher, lier et gérer l'accès aux ressources du groupe de ressources |
| Rôle Administrateur |  Afficher, modifier ou gérer l'accès pour le groupe, mais non pour les ressources du groupe | Créer, supprimer, modifier, suspendre, reprendre, afficher, lier et gérer l'accès aux ressources du groupe de ressources | 
{: caption="Tableau 1. Accès pour les groupes de ressources" caption-side="top"}

Si vous souhaitez qu'un utilisateur puisse créer une instance de service et l'ajouter à un groupe de ressources, l'utilisateur doit avoir au moins le rôle Afficheur pour le groupe de ressources et au moins le rôle Editeur pour le service.
{: tip}


## Exemples de règle d'accès
{: #sample_policies}

Consultez les exemples de règle d'accès suivants pour déterminer plus facilement comment affecter l'accès à des ressources de votre compte faisant partie de groupes de ressources.

1. Règle qui octroie à l'utilisateur le rôle de plateforme “Administrateur” pour {{site.data.keyword.Bluemix_notm}} Container Service dans l'ensemble du compte. Une règle avec ces caractéristiques permet à l'utilisateur d'accéder à toutes les instances de ce service et lui permet également de créer des instances du service dans tout groupe de ressources pour lequel l'utilisateur dispose au moins du rôle Afficheur. Les utilisateurs ayant le rôle Administrateur sur les ressources peuvent également accorder à d'autres utilisateurs l'accès à ces dernières.
2. Règle qui octroie à l'utilisateur le rôle de plateforme “Afficheur” pour un groupe de ressources mais non pour ses ressources membre. Une règle avec ces caractéristiques permet à l'utilisateur de voir le groupe de ressources. Ainsi, il peut créer des instances d'un service de ce groupe de ressources.
3. Règle qui octroie à l'utilisateur le rôle de plateforme “Editeur” pour toutes les ressources du groupe de ressources. Un utilisateur ayant le rôle Editeur sur une ressource peut éditer ou supprimer cette ressource.
4. Règle qui octroie à l'utilisateur le rôle de plateforme “Administrateur” pour l'ensemble du compte (tous les services activés par IAM). Une règle avec ces caractéristiques permet à l'utilisateur d'effectuer des actions de plateforme sur les ressources de l'ensemble du compte et permet également d'effectuer des actions de gestion sur le compte, telles que la gestion des groupes de ressources dans le compte.

## Exemples de cas d'utilisation
{: #usecase_examples}

Pour chacun de ces cas d'utilisation, si vous souhaitez que les utilisateurs d'un groupe aient tous le même niveau d'accès, ajoutez-les à un [groupe d'accès](/docs/iam?topic=iam-groups). L'utilisation de groupes d'accès permet de réduire de manière significative le nombre de règles d'accès. En effet, tous les membres du groupe héritent de l'accès affecté au groupe.
{: tip}

<ol>
<li><p>J'ai un compte de petite taille incluant uniquement 10 utilisateurs qui collaborent ensemble sur un seul projet. Certains utilisateurs doivent pouvoir gérer le compte et affecter l'accès à d'autres utilisateurs. D'autres doivent pouvoir mettre à disposition des instances de service, ce qui génère des dépenses. Les autres utilisateurs sont des développeurs d'application qui ont uniquement besoin d'utiliser les instances de service de leurs composants d'application.</p>
<p>Tous ces utilisateurs doivent se voir accorder différents rôles pour le compte et le groupe de ressources par défaut. Il n'est pas nécessaire de créer de groupes de ressources supplémentaires ou de restreindre l'accès à certaines ressources pour certains utilisateurs. Les utilisateurs peuvent se voir accorder les rôles appropriés à leurs besoins pour le compte et le groupe de ressources par défaut : Administrateur (compte des utilisateurs ayant besoin de gérer le compte et d'accorder l'accès à d'autres utilisateurs), Editeur (groupe de ressources par défaut et ses membres pour les utilisateurs ayant besoin de mettre à disposition des instances de service) et Auteur ou Lecteur (membres du groupe de ressources pour les utilisateurs ayant besoin uniquement d'utiliser les instances de service).</p>
</li>
<li><p>J'ai un compte qui inclut trois différentes équipes travaillant sur trois projets. Quelques utilisateurs sont administrateurs et doivent pouvoir créer de nouveaux groupes de ressources et affecter un accès utilisateur à des groupes de ressources. Les autres utilisateurs ont uniquement besoin d'accéder au groupe de ressources associé à leur projet.</p>
<p>J'affecte aux administrateurs le rôle Administrateur pour tous les services activés par IAM. J'affecte aux autres utilisateurs différents rôles en fonction de leurs projets pour le groupe de ressources et les membres de ce dernier : Editeur (groupe de ressources pour les utilisateurs ayant besoin de créer des instances) et Auteur ou Lecteur (membre de groupe de ressources pour les utilisateurs ayant besoin d'utiliser des instances).</p>
</li>
<li><p>J'ai un compte avec plusieurs groupes de ressources. J'ai des utilisateurs qui sont administrateurs du service A dans le compte, qui ont besoin d'accéder à toutes les instances de ce service ainsi que de créer des instances mais ces utilisateurs n'ont pas besoin d'avoir accès à d'autres ressources du compte.</p>
<p>J'affecte à ces utilisateurs le rôle Administrateur sur le service A au niveau du compte, tout en leur affectant le rôle Afficheur pour tous les groupes de ressources du compte où ils ont besoin de créer des instances.</p>
</li>
<li><p>J'ai un utilisateur dans mon compte qui a uniquement besoin d'accéder à une ressource spécifique d'un service, par exemple il doit disposer de droits en écriture dans un compartiment A d'IBM Cloud Object Storage. Cet utilisateur ne doit pas pouvoir voir les groupes de ressources de mon compte ou accéder à d'autres services ou à d'autres compartiments de cette instance de Cloud Object Storage.</p> 
<p>J'accorde à cet utilisateur le rôle Auteur pour le compartiment A dans l'instance spécifique de Cloud Object Storage. Vous pouvez octroyer cette règle en utilisant des interfaces spécifiques au service (interface utilisateur Cloud Object Storage, dans cet exemple) ou l'interface utilisateur Assign Access principale. L'interface utilisateur spécifique au service est recommandée car elle vous permet d'effectuer une sélection parmi une liste de ressources, alors que l'interface utilisateur Assign Access n'affiche pas les ressources inférieures au niveau d'instance de service et vous devez entrer manuellement le nom de ressource de cloud pour affecter une règle à ces ressources.</p>
</li>
<li><p>J'utilise actuellement des organisations et des espaces Cloud Foundry mais je vais commencer à utiliser des groupes de ressources et des groupes d'accès pour mes services activés par IAM. Actuellement, mes utilisateurs et mes ressources sont répartis dans des organisations pour les secteurs d'activité et les espaces sont utilisés pour différents projets d'un secteur d'activité.</p>
<p>J'utilise des groupes pour organiser les ressources de la même façon que je le faisais pour les espaces en traitant chaque groupe de ressources comme un espace de projet. Je configure ensuite des groupes d'accès distincts afin d'accorder l'accès nécessaire à mes utilisateurs aux groupes de ressources de niveau de projet approprié. L'accès peut être accordé à toutes les ressources ou uniquement à un groupe donné d'un ensemble. Vous pouvez donc configurer chaque groupe d'accès avec des niveaux d'accès différents aux ressources d'un groupe, ce qui accorde à chaque groupe d'utilisateurs l'accès dont il a besoin pour utiliser les ressources ou le groupe de ressources lui-même.</p>
</li>
</ol>


