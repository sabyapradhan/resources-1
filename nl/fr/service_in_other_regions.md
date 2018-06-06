---

copyright:
  years: 2015, 2018
lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}

# Utilisation des services dans une autre région
{: #cross_region_service}

Si une instance de service est créée et liée à des applications dans une région, vous pouvez l'utiliser dans une autre région de l'une des façons suivantes :
{: shortdesc}

  * Utilisez les données d'identification du service pour configurer votre instance d'application directement. Voir [Utilisation des services {{site.data.keyword.Bluemix_notm}} avec des applications externes](/docs/apps/reqnsi.html#accser_external){: new_window}
pour des détails.
  * Créez un service fourni par l'utilisateur comme pont.

	Pour utiliser une instance de service qui existe dans une autre région, procédez comme suit :

      1. Passez dans la région dans laquelle l'instance de service existe. Dans la barre de menus {{site.data.keyword.Bluemix_notm}}, développez le menu **Région**, puis sélectionnez la région où est présente l'instance de service.

      2. Récupérez les données d'identification et les paramètres de connexion depuis la variable d'environnement VCAP_SERVICES de l'instance de service dans la région dans laquelle le service existe. Procédez comme suit :

	       1. Dans le tableau de bord {{site.data.keyword.Bluemix_notm}}, cliquez sur la vignette de votre application. La page Présentation s'affiche.
	       2. Dans le panneau de navigation, cliquez sur **Données d'identification**. Les détails de la variable d'environnement *VCAP_SERVICES* sont affichés. Enregistrez le contenu JSON pour l'instance de service.

      3. Passez dans la région dans laquelle vous voulez utiliser l'instance de service. Dans la barre de menus {{site.data.keyword.Bluemix_notm}}, développez le menu **Région**, puis sélectionnez la région où vous désirez utiliser l'instance de service.

      4. Créez une instance de service fournie par l'utilisateur en utilisant les données d'identification et les paramètres de connexion que vous avez enregistrés depuis la variable d'environnement *VCAP_SERVICES*. Pour plus d'informations sur la création d'une instance de service fournie par l'utilisateur, voir [Création d'une instance de service fournie par l'utilisateur](/docs/apps/reqnsi.html#user_provide_services).

      5. Liez l'instance de service fournie par l'utilisateur à votre application avec la commande suivante :

	     ```
	     bluemix service bind myapp user-provided_service_instance
	     ```
