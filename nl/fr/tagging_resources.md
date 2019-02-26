---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-29"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Utilisation d'étiquettes
{: #tag}

Une étiquette est un libellé affecté à une ressource pour un filtrage simple des ressources de votre liste de ressources. Les étiquettes permettent d'organiser vos ressources et de les trouver facilement ultérieurement.  
{: shortdesc}

Pour voir une liste complète des étiquettes de votre compte, accédez à **Gérer > Comptes** puis sélectionnez **Etiquettes**.

## Limitations et règles d'étiquetage
{: #limits}

La taille maximale d'une étiquette est de 128 caractères. Les caractères autorisés sont les suivants : A-Z, 0-9, espace, trait de soulignement, tiret, point et virgule. De plus, il n'est pas nécessaire de respecter l'utilisation des minuscules/majuscules pour les étiquettes. L'utilisation du signe deux points permet de créer à partir de l'étiquette une chaîne dans laquelle vous pouvez isoler deux parties logiques, comme `clé:valeur`. Vous ne pouvez pas utiliser le signe deux points dans une étiquette sans créer de paire. Une virgule sépare les étiquettes et ne peut pas être utilisée dans le nom de l'étiquette lui-même.

## Ajout et retrait d'étiquettes sur une ressource
{: #add-remove}

1. Dans la console {{site.data.keyword.Bluemix_notm}}, cliquez sur l'icône Menu ![Icône Menu](../icons/icon_hamburger.svg) > **Liste de ressources** pour afficher votre liste de ressources. 
2. Cliquez sur le bouton de développement du type de ressource correspondant à la ressource à étiqueter. Par exemple, si vous souhaitez étiqueter une instance d'{{site.data.keyword.cos_full_notm}}, sélectionnez **Stockage**.  
3. Cliquez sur l'icône Actions ![Icône Actions](../icons/action-menu-icon.svg) pour ajouter ou mettre à jour une étiquette pour la ressource. 

    * Pour ajouter une étiquette, cliquez sur le menu Actions ![Icône Actions](../icons/action-menu-icon.svg), sélectionnez **Ajouter des étiquettes** et entrez un nom pour votre étiquette. 
    * Pour ajouter des étiquettes supplémentaires, cliquez sur l'icône Editer ![Icône Editer](../icons/edit-tagging.svg) se trouvant en regard de l'étiquette affichée et entrez un nom pour votre étiquette. Appuyez sur Entrée pour continuer à ajouter des étiquettes.
4. Pour retirer une étiquette, cliquez sur l'icône Editer ![Icône Editer](../icons/edit-tagging.svg). Cliquez ensuite sur l'icône Retirer ![Icône Retirer](../icons/close-tagging.svg) se trouvant en regard de l'étiquette. 

## Recherche d'étiquettes
{: #search-tags}

Vous pouvez rechercher des étiquettes en utilisant une des méthodes suivantes :

  * Utilisez la barre de recherche se trouvant dans la barre de menus de la console {{site.data.keyword.Bluemix_notm}}.
  * Vous pouvez filtrer votre liste de ressources en fonction de l'étiquette recherchée.
  * A partir de la page des détails de l'application, vous pouvez rechercher les étiquettes associées à cette ressource.

La même étiquette peut être associée à plusieurs ressources par différents utilisateurs du même compte de facturation. De plus, tous les utilisateurs ne voient pas toutes les ressources du compte.
{: note}


## Etiquetage pour les revendeurs
{: #resell}

Tous les membres d'un compte peuvent voir les étiquettes.
Si votre compte est associé à différentes organisations (si vous êtes revendeur, par exemple), vous pouvez recommander à vos clients de ne pas stocker d'informations sur des étiquettes, d'autres utilisateurs du même compte risqueraient alors d'accéder à des informations confidentielles.

Pour contrôler la visibilité des étiquettes, suivez les instructions d'étiquetage et faites savoir aux utilisateurs que les étiquettes sont visibles dans l'ensemble du compte. 

Utilisez des codes et nom des noms pour les clients et les comptes et évitez de placer des informations confidentielles sur des étiquettes.
{: tip}

