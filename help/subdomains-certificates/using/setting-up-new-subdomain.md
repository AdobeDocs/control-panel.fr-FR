---
title: Configuration d’un nouveau sous-domaine
description: Découvrez comment configurer un nouveau sous-domaine pour vos instances de campagne
translation-type: tm+mt
source-git-commit: 52f155bbbecec9edabc66cbc28756f9579b81f04

---


# Configuration d’un nouveau sous-domaine {#setting-up-subdomain}

>[!NOTE]
>
>La délégation de sous-domaines du Panneau de configuration est actuellement en version bêta et sujette à de fréquentes mises à jour et modifications sans notification.

## Délégation de sous-domaine complète {#full-subdomain-delegation}

Le Panneau de configuration vous permet de déléguer entièrement un sous-domaine à Adobe Campaign. Pour ce faire, procédez comme suit :

1. Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez l’instance de production souhaitée, puis cliquez sur**[!UICONTROL  Configurer un nouveau sous-domaine]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >La délégation de sous-domaine est disponible uniquement pour les instances **de production** .

1. Cliquez sur **[!UICONTROL Suivant]**pour confirmer la méthode de délégation complète.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[Les méthodes CNAME](#use-cnames) et personnalisées ne sont actuellement pas prises en charge par le Panneau de configuration.

1. Créez le sous-domaine et les serveurs de noms souhaités dans la solution d’hébergement utilisée par votre entreprise. Pour ce faire, copiez-collez les informations du serveur de noms Adobe affichées dans l’assistant. Pour plus d’informations sur la création d’un sous-domaine dans une solution d’hébergement, reportez-vous à la vidéo [du](https://video.tv.adobe.com/v/30175?captions=fre_fr)didacticiel.

   >[!CAUTION]
   >
   >Lors de la configuration des serveurs de noms, veillez à **ne jamais déléguer votre sous-domaine racine à Adobe**. Sinon, le domaine ne pourra fonctionner qu’avec Adobe. Toute autre utilisation sera impossible, comme par exemple envoyer des courriers électroniques internes aux employés de votre entreprise.

   ![](assets/subdomain4.png)

   Notez que si aucun sous-domaine n’est configuré, le sous-domaine que vous configurez est considéré comme le sous-domaine **** principal. Les boîtes de réception (expéditeur, erreur, adresses de réponse) resteront identiques pour tous les sous-domaines configurés ultérieurement sur ce sous-domaine.

   Une fois le sous-domaine créé avec les informations correspondantes du serveur de noms Adobe, cliquez sur **[!UICONTROL Suivant]**.

1. Sélectionnez le cas d’utilisation souhaité pour le sous-domaine :

   * **Communications** marketing : communications destinées à un usage commercial. Exemple : campagne par courrier électronique de vente.
   * **Communications** transactionnelles et opérationnelles : les communications transactionnelles contiennent des informations visant à terminer un processus que le destinataire a commencé avec vous. Exemple : confirmation d’achat, courrier électronique de réinitialisation du mot de passe. Les communications organisationnelles se rapportent à l&#39;échange d&#39;informations, d&#39;idées et de vues au sein et à l&#39;extérieur de l&#39;organisation, sans but commercial.
   >[!NOTE]
   >
   >La ventilation de vos sous-domaines selon les cas d’utilisation est une bonne pratique pour la délivrabilité. Ce faisant, la réputation de chaque sous-domaine est isolée et protégée.
   >
   >Par exemple, si votre sous-domaine pour les communications marketing est mis sur liste noire par les fournisseurs de services Internet, votre sous-domaine de communications transactionnelles ne sera pas affecté et continuera à être en mesure d’envoyer des communications.

   ![](assets/subdomain5.png)

1. Entrez le sous-domaine que vous avez créé dans votre solution d’hébergement, puis cliquez sur **[!UICONTROL Envoyer]**.

   >[!NOTE]
   >
   > Veillez à renseigner le nom **** complet du sous-domaine à déléguer. Par exemple, pour déléguer le sous-domaine &quot;usoffres.email.weretail.com&quot;, saisissez &quot;usoffres.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

1. Une fois le sous-domaine envoyé, le Panneau de configuration vérifie qu’il pointe correctement vers les enregistrements Adobe NS et que l’enregistrement de début d’autorité (SOA) n’existe pas pour ce sous-domaine.

1. Si les vérifications sont réussies, le Panneau de configuration commencera à configurer le sous-domaine avec des enregistrements DNS, des URL supplémentaires, des boîtes de réception, etc. Vous pouvez obtenir plus de détails sur la progression de la configuration en cliquant sur le bouton Détails **[!UICONTROL du]**processus.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >Dans certains cas, la délégation s’effectue mais le sous-domaine peut ne pas être vérifié. Le sous-domaine va directement dans la liste des sous-domaines ****vérifiés avec l’état**[!UICONTROL  Non vérifié]** et un journal des tâches fournissant des informations sur l’erreur. Contactez le service à la clientèle si vous rencontrez des problèmes pour résoudre le problème.
   >
   >Notez que, pendant l’exécution de la délégation de sous-domaine, d’autres requêtes par l’intermédiaire du Panneau de configuration seront entrées dans une file d’attente et exécutées uniquement une fois la délégation de sous-domaine terminée, afin d’éviter tout problème de performances.

A la fin du processus, les sous-domaines seront configurés pour fonctionner avec votre instance Adobe Campaign et les éléments ci-dessous seront créés :

* **Sous-domaine** avec les enregistrements **** DNS suivants : SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Sous-domaines** supplémentaires pour héberger le miroir, la ressource, les pages de suivi et la clé de domaine,
* **Inbox**: Expéditeur, erreur, réponse.

Pour plus d’informations sur le sous-domaine, cliquez sur le bouton Détails **[!UICONTROL du]**sous-domaine.

![](assets/subdomain_details_general.png)

![](assets/subdomains_details_senderinfo.png)

>[!NOTE]
>
>En plus de l’étape de traitement, Adobe informera l’équipe de délivrabilité du nouveau sous-domaine afin de contrôler le sous-domaine qui a été créé. Le processus de vérification peut prendre jusqu’à 3 jours après la délégation du sous-domaine.
>
>Les contrôles effectués comprennent les boucles de commentaires et les tests de boucles de plaintes de spam. Nous vous déconseillons donc d&#39;utiliser le sous-domaine avant la fin de la vérification, car cela pourrait entraîner une mauvaise réputation du sous-domaine.

## Utilisation de CNAME {#use-cnames}

L’utilisation de CNAME pour la délégation de sous-domaines n’est pas recommandée par Adobe et n’est pas prise en charge par le Panneau de configuration. Pour utiliser cette méthode, contactez le service à la clientèle Adobe.
