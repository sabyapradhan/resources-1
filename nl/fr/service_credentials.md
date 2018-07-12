---

copyright:

  years: 2015, 2018
lastupdated: "2018-06-20"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# Ajout de données d'identification
{: #service_credentials}

Vous pouvez générer un nouveau jeu de données d'identification pour le cas où vous voudriez connecter manuellement un consommateur extérieur à un service {{site.data.keyword.Bluemix}}. Par exemple, si vous tentez de lier une application AWS à un service Watson, vous devrez générer de nouvelles données d'identification pouvant être utilisées pour lier entre-eux ces deux éléments.

## Ajout de données d'identification lors de la liaison d'un service avec l'offre IAM activée
{: #IAM}

Les services gérés par {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) peuvent générer une clé de ressource, également dénommée donnée d'identification. Les données d'identification sont propres au service concerné et varient en fonction de la manière dont chaque service définit les données d'identification devant être générées. Ces données d'identification peuvent contenir un nom d'utilisateur, un mot de passe, un nom d'hôte, un port et une URL.

Toutefois, alors que le contenu de chaque donnée d'identification est unique au service qui le génère, tous les services gérés par IAM nécessitent que de nouvelles données d'identification incluent un rôle d'accès du service IAM. Certains services peuvent générer des données supplémentaires nécessitant de renseigner des paramètres. Par exemple, un service peut vous demander d'entrer un paramètre langue pour définir la langue par défaut renvoyée dans la clé de ressource générée.

Pour ajouter des données d'identification à un service géré par IAM, procédez comme suit :

1. Dans le tableau de bord, sélectionnez la nom du service pour ouvrir la page des détails du service. Sélectionnez ensuite l'onglet Données d'identification et cliquez sur **Nouvelles données d'identification + **.
2. Dans la boîte de dialogue Ajouter de nouvelles données d'identification, entrez un **Nom**.
3. Spécifiez le rôle. Cette valeur définit le rôle d'accès du service IAM. Pour plus d'informations, voir [Accès IAM](/docs/iam/users_roles.html#userroles).
4. Facultatif : vous pouvez renseigner la zone ID de service soit en autorisant IAM à générer automatiquement une valeur unique, soit en fournissant l'ID d'un service existant. Pour plus d'informations, voir [Création et gestion des ID de service](/docs/iam/serviceid.html#serviceids).
5. Vous pouvez également fournir d'autres paramètres par le biais d'un objet JSON valide contenant des paramètres de configuration spécifiques au service et qui seront soumis soit en ligne, soit dans un fichier.

  **Remarque **. La plupart des services ne requièrent pas de paramètres supplémentaires et pour ceux qui en ont besoin, chaque service définit sa propre liste unique de paramètres. Pour la liste des paramètres de configuration pris en charge, reportez-vous à la documentation de l'offre de service concernée.
6. Cliquez sur **Ajouter** pour générer les nouvelles données d'identification du service.

## Ajout de données d'identification lors de la liaison d'un service Cloud Foundry
{: #cf}

Les services Cloud Foundry peuvent générer une clé de service, également dénommée donnée d'identification. Les données d'identification sont propres au service concerné et varient en fonction de la manière dont chaque service définit les données d'identification devant être générées. Les données d'identification de service peuvent contenir un nom d'utilisateur, un mot de passe, un nom d'hôte, un port et une URL.

Toutefois, le contenu de chaque donnée d'identification est propre au service qui le génère. Certains services peuvent générer des données supplémentaires nécessitant de renseigner des paramètres. Par exemple, un service peut vous demander d'entrer un paramètre langue pour définir la langue par défaut renvoyée dans la clé de service générée.

Pour ajouter des données d'identification Cloud Foundry, procédez comme suit :

1. Dans la page des détails du service, sélectionnez l'onglet Données d'identification, puis cliquez sur **Nouvelles données d'identification + **.
2. Dans la boîte de dialogue Ajouter de nouvelles données d'identification, entrez un **Nom**.
3. Vous pouvez également fournir d'autres paramètres par le biais d'un objet JSON valide contenant des paramètres de configuration spécifiques au service et qui seront soumis soit en ligne, soit dans un fichier.

  **Remarque **. La plupart des services ne requièrent pas de paramètres supplémentaires et pour ceux qui en ont besoin, chaque service définit sa propre liste unique de paramètres. Pour la liste des paramètres de configuration pris en charge, reportez-vous à la documentation de l'offre de service concernée.
4. Cliquez sur **Ajouter** pour générer les nouvelles données d'identification du service.

