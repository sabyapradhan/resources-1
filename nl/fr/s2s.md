---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-06"

keywords: service authorization, service instance's access, connect service to app

subcollection: resources

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Connexion de services à une application Cloud Foundry
{: #s2s_binding}

Pour utiliser un service dans une application Cloud Foundry, vous devez créer une connexion ou lier ce service à l'application.
{: shortdesc}

Pour connecter un service à votre application à partir de la page des détails  d'un service spécifique, procédez comme suit :

Vous pouvez également créer des connexions depuis votre application vers le service. Sélectionnez votre application dans la liste de ressources, accédez au menu **Connexions**, puis sélectionnez le service.
{: note}

1. Dans la liste des ressources, cliquez sur **Services** et sélectionnez le service auquel vous souhaitez accéder. La page des détails du service s'affiche.
2. Cliquez sur **Connexions** dans le panneau de navigation.
3. Cliquez sur **Créer une connexion**.
4. Cliquez sur **Connecter** pour la ligne de l'application pour laquelle vous voulez créer une connexion.
5. Sélectionnez un rôle d'accès à affecter à la connexion. Ce rôle définit les actions autorisées que peut effectuer l'application qui accède au service.
6. Facultatif : sélectionnez, créez ou générez automatiquement un ID de service qu'utilisera l'application pour accéder au service. Le rôle d'accès sélectionné à l'étape précédente est affecté à cet ID de service. Si vous ne sélectionnez pas d'option, un élément est généré. 
7. Facultatif : ajoutez des paramètres de configuration au format JSON.
8. Cliquez sur **Connecter & et reconstituer l'application**.


Si vous souhaitez restreindre l'accès d'une application à l'instance de service, cliquez sur **Connexions** dans le panneau de navigation puis sur **Annuler la liaison** dans le menu pour l'application connectée afin de supprimer la liaison de service.
{: tip}
