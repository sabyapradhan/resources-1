---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-26"

keywords: service availability, service location, using services across regions

subcollection: resources

---

{:shortdesc: .shortdesc}

# Utilisation des services dans une autre région
{: #cross_region_service}

Si une instance de service est créée et liée à des applications dans une région, vous pouvez l'utiliser dans une autre région de l'une des façons suivantes :
{: shortdesc}

  * Utilisez les données d'identification du service pour configurer votre instance d'application directement. Pour plus de détails, voir [Connexion de services à des applications externes](/docs/resources?topic=resources-externalapp#externalapp).
  * Créez un service fourni par l'utilisateur comme pont.

	Pour utiliser une instance de service qui existe dans une autre région, procédez comme suit :

      1. Pour accéder à la région dans laquelle se trouve l'instance de service, cliquez sur l'icône **Menu  ![Icône Menu](../icons/icon_hamburger.svg)** > **Liste de ressources**. Développez ensuite le menu **EMPLACEMENT** et sélectionnez la région.

      2. Récupérez les données d'identification et les paramètres de connexion depuis la variable d'environnement VCAP_SERVICES de l'instance de service dans la région dans laquelle le service existe. Procédez comme suit :

	       1. Dans le tableau de bord {{site.data.keyword.Bluemix_notm}}, cliquez sur **Tout afficher** sur la vignette des applications. La page Présentation s'affiche.
	       2. Dans le panneau de navigation, cliquez sur **Données d'identification**. Les détails de la variable d'environnement *VCAP_SERVICES* sont affichés. Enregistrez le contenu JSON pour l'instance de service.

      3. Accédez à la région dans laquelle vous voulez utiliser l'instance de service. Cliquez sur l'icône **Menu ![Icône Menu](../icons/icon_hamburger.svg)** > **Liste de ressources**. Développez ensuite le menu **EMPLACEMENT** et sélectionnez la région dans laquelle utiliser l'instance de service.

      4. Créez une instance de service fournie par l'utilisateur en utilisant les données d'identification et les paramètres de connexion que vous avez enregistrés depuis la variable d'environnement *VCAP_SERVICES*. Pour plus d'informations, voir [Création d'une instance de service fournie par l'utilisateur](/docs/apps/tutorials?topic=creating-apps-add-resource#user_provide_services).

      5. Liez l'instance de service fournie par l'utilisateur à votre application avec la commande suivante :

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```
