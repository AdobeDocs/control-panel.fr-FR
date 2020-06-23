---
title: Configuration d’un nouveau sous-domaine
description: Découvrez comment configurer un nouveau sous-domaine pour vos instances de campagne
translation-type: tm+mt
source-git-commit: 5b7e8126789690662e72e72c885700b971362004
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 81%

---


# Configuration d’un nouveau sous-domaine {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Configurer de nouveaux sous-domaines et gérer les certificats"
>abstract="Vous devez configurer un nouveau sous-domaine et gérer les certificats SSL de vos sous-domaines pour envoyer des emails ou publier des landing pages avec Adobe Campaign."
>additional-url="https://docs.adobe.com/content/help/fr-FR/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Comment surveiller les certificats SSL de vos sous-domaines"

>[!IMPORTANT]
>
>La délégation de sous-domaine depuis le panneau de contrôle est disponible en version bêta et sujette à de fréquentes mises à jour et modifications sans préavis.

## Délégation complète de sous-domaine {#full-subdomain-delegation}

Le Panneau de contrôle vous permet de déléguer entièrement un sous-domaine à Adobe Campaign. Pour ce faire, procédez comme suit :

1. Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez l’instance de production souhaitée, puis cliquez sur **[!UICONTROL Configurer un nouveau sous-domaine]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >La délégation de sous-domaine n’est disponible que pour les instances de **production**.
   >
   >Si l’instance sélectionnée ne comporte aucun sous-domaine configuré, le premier sous-domaine délégué à Adobe deviendra le **sous-domaine principal** de cette instance. Vous ne pourrez plus le modifier à l’avenir. Des enregistrements DNS inversés seront créés pour d’autres sous-domaines utilisant le sous-domaine principal. Les adresses de réponse et bounce pour les autres sous-domaines seront générées à partir du sous-domaine principal.

1. Cliquez sur **[!UICONTROL Suivant]** pour confirmer votre choix de la méthode de délégation complète.

   Note that [CNAME](#use-cnames) and custom methods are currently not supported by the Control Panel.

   ![](assets/subdomain3.png)

1. Créez le sous-domaine et les serveurs de noms souhaités dans la solution d’hébergement utilisée par votre entreprise. Pour ce faire, copiez et collez les informations du serveur de noms Adobe affichées dans l’assistant. Pour plus d’informations sur la création d’un sous-domaine dans une solution d’hébergement, reportez-vous à ce [tutoriel vidéo](https://video.tv.adobe.com/v/30175?captions=fre_fr).

   >[!IMPORTANT]
   >
   >Lors de la configuration des serveurs de noms, veillez à **ne jamais déléguer votre sous-domaine racine à Adobe**. Sinon, le domaine ne pourra fonctionner qu’avec Adobe. Toute autre utilisation sera impossible, comme par exemple envoyer des emails internes aux employés de votre entreprise.
   >
   >De plus, **ne créez pas de fichier de zone distinct** pour ce nouveau sous-domaine.

   ![](assets/subdomain4.png)

1. Une fois le sous-domaine créé avec les informations du serveur de noms Adobe correspondantes, cliquez sur **[!UICONTROL Suivant]**.

1. Sélectionnez le cas d’utilisation souhaité pour le sous-domaine :

   * **Communications marketing** : communications destinées à un usage commercial. Exemple : campagne par email de vente.
   * **Communications transactionnelles et opérationnelles** : les communications transactionnelles contiennent des informations visant à terminer un processus que le destinataire a commencé avec vous. Exemple : confirmation d’achat, email de réinitialisation de mot de passe. Les communications organisationnelles se rapportent à l’échange d’informations, d’idées et d’opinions au sein et à l’extérieur de l’organisation, sans but commercial.
   ![](assets/subdomain5.png)

   **La ventilation de vos sous-domaines selon les cas d’utilisation est une bonne pratique en matière de délivrabilité**. Elle permet d’isoler et de protéger la réputation de chaque sous-domaine. Par exemple, si votre sous-domaine pour les communications marketing finit par être ajouté à la liste bloquée par des Prestataires Internet, votre sous-domaine de communications transactionnelles ne sera pas affecté et pourra toujours envoyer des communications.

   **Vous pouvez déléguer un sous-domaine pour les cas d’utilisation Marketing et Transactionnel** :

   * Pour les cas d’utilisation Marketing, les sous-domaines seront configurés sur les instances **MID** (Mid-sourcing).
   * Pour les cas d’utilisation Transactionnel, les sous-domaines seront configurés sur TOUTES les instances **RT** (Message Center/Real-time messaging) pour garantir la connectivité. Les sous-domaines fonctionneront donc avec toutes vos instances RT.
   >[!NOTE]
   >
   >Si vous utilisez Campaign Classic, le Panneau de contrôle vous permet de voir quelles instances RT/MID sont connectées à l’instance Marketing que vous utilisez. For more on this, refer to the [Instance Details](../../instances-settings/using/instance-details.md) section.

1. Entrez le sous-domaine que vous avez créé dans votre solution d’hébergement, puis cliquez sur **[!UICONTROL Soumettre]**.

   Veillez à indiquer le **nom complet** du sous-domaine à déléguer. Par exemple, pour déléguer le sous-domaine « usoffers.email.weretail.com », saisissez « usoffers.email.weretail.com ».

   ![](assets/subdomain6.png)

1. Une fois le sous-domaine envoyé, le panneau de contrôle vérifie qu’il pointe correctement vers les enregistrements NS Adobe et que l’enregistrement Start of Authority (SOA) n’existe pas pour ce sous-domaine.

   >[!NOTE]
   >
   >Pendant l’exécution de la délégation de sous-domaine, d’autres requêtes effectuées via le panneau de contrôle seront mises en file d’attente et exécutées uniquement une fois la délégation de sous-domaine terminée. Cela permet d’éviter tout problème de performances.

1. Si les vérifications réussissent, le panneau de contrôle commence à configurer le sous-domaine avec des enregistrements DNS, des URL supplémentaires, des boîtes de réception, etc.

   ![](assets/subdomain7.png)

   Eventually, the **Deliverability team** will be notified about the new subdomain, in order to audit it. Le processus de vérification peut prendre jusqu’à 10 jours ouvrés après la délégation du sous-domaine. Les contrôles effectués comprennent les tests de feedback loops et de boucles de plaintes relatives au spam. Nous vous déconseillons donc d’utiliser le sous-domaine avant la fin de la vérification, car cela pourrait entraîner une mauvaise réputation du sous-domaine.

   Pour afficher plus de détails sur la progression de la configuration, cliquez sur le bouton **[!UICONTROL Détails du processus]**.

   ![](assets/subdomain_audit.png)

   **Résolution des problèmes:**

   * Dans certains cas, la délégation est effectuée, mais pas la vérification du sous-domaine. The subdomain will stay into the **[!UICONTROL Configured]** list with a job log providing information on the error. Contactez l’Assistance clientèle si vous avez des difficultés à résoudre le problème.
   * Si le sous-domaine est affiché comme &quot;Non vérifié&quot; après avoir été configuré, lancez une nouvelle vérification du sous-domaine (**...** / **[!UICONTROL Vérifier le sous-domaine]**). S&#39;il affiche toujours le même statut, la raison pourrait être qu&#39;il existe une certaine personnalisation sur le schéma destinataire, qui ne peut pas être vérifiée à l&#39;aide de processus standard. Essayez d&#39;envoyer une campagne avec ce sous-domaine.
   * Si la configuration du sous-domaine prend trop de temps (plus de 10 jours ouvrés) à l’étape de l’audit de délivrabilité, contactez le service à la clientèle.

À la fin du processus, les sous-domaines sont configurés pour fonctionner avec votre instance Adobe Campaign et les éléments suivants sont créés :

* **Le sous-domaine avec les enregistrements DNS** suivants : SOA, MX, CNAME, DKIM, SPF et TXT
* **Des sous-domaines supplémentaires** pour héberger les pages miroir, de ressources et de tracking, ainsi que la clé de domaine
* **Des boîtes de réception** : Expéditeur, Erreur, Réponse

   Par défaut, la boîte de réception « Réponse » du panneau de contrôle est configurée pour effacer les emails et ne peut pas être examinée. Si vous souhaitez surveiller votre boîte de réception « Réponse » pour vos campagnes marketing, n’utilisez pas cette adresse.

Pour obtenir plus de détails sur un sous-domaine, cliquez sur le bouton **[!UICONTROL Détails du sous-domaine]** et **[!UICONTROL Infos sur l’expéditeur]**.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Utilisation des CNAME {#use-cnames}

L’utilisation des CNAME pour la délégation de sous-domaine n’est pas prise en charge par le panneau de contrôle. Pour utiliser cette méthode, contactez l’Assistance clientèle Adobe.

**Rubriques connexes :**

* [Délégation de sous-domaines (tutoriel vidéo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Marque des sous-domaines](../../subdomains-certificates/using/subdomains-branding.md)
* [Surveillance de vos sous-domaines](../../subdomains-certificates/using/monitoring-subdomains.md)