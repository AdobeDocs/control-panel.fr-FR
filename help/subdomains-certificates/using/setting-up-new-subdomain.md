---
title: Configuration d’un nouveau sous-domaine
description: Découvrez comment configurer un nouveau sous-domaine pour vos instances de campagne
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Configuration d’un nouveau sous-domaine {#setting-up-subdomain}

## Délégation de sous-domaine complète {#full-subdomain-delegation}

Le Panneau de configuration vous permet de déléguer entièrement un sous-domaine à Adobe Campaign. Pour ce faire, procédez comme suit :

1. Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez l’instance de production souhaitée, puis cliquez sur**[!UICONTROL  Configurer un nouveau sous-domaine]**.

   >[!NOTE]
   >
   >La délégation de sous-domaine est disponible uniquement pour les instances **de production** .

   ![](assets/subdomain1.png)

1. Cliquez sur **[!UICONTROL Suivant]**pour confirmer la méthode de délégation complète.

   >[!NOTE]
   >
   >[Les méthodes CNAME](#use-cnames) et personnalisées ne sont actuellement pas prises en charge par le Panneau de configuration.

   ![](assets/subdomain3.png)

1. Créez le sous-domaine et les serveurs de noms souhaités dans la solution d’hébergement utilisée par votre entreprise. Pour ce faire, copiez-collez les informations du serveur de noms Adobe affichées dans l’assistant.

   Pour plus d’informations sur la création d’un sous-domaine dans une solution d’hébergement, reportez-vous à ce didacticiel vidéo.

   ![](assets/subdomain4.png)

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

A la fin du processus, les sous-domaines seront configurés pour fonctionner avec votre instance Adobe Campaign et les éléments ci-dessous seront créés :

* **Sous-domaine** avec les enregistrements **** DNS suivants : SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Sous-domaines** supplémentaires pour héberger le miroir, la ressource, les pages de suivi et la clé de domaine,
* **Inbox**: Expéditeur, erreur, réponse.

## Utilisation de CNAME {#use-cnames}

L’utilisation de CNAME pour la délégation de sous-domaines n’est pas recommandée par Adobe et n’est pas prise en charge par le Panneau de configuration.

Pour utiliser cette méthode, contactez votre service à la clientèle Adobe.
