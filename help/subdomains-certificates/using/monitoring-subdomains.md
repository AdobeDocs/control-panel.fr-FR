---
title: Surveillance des certificats SSL des sous-domaines
description: Découvrez comment surveiller les certificats SSL de vos sous-domaines
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Surveillance des sous-domaines {#monitoring-subdomains}

Il est essentiel de surveiller vos sous-domaines pour vous assurer qu’ils sont tous correctement configurés pour fonctionner avec Adobe Campaign.

The list of subdomains for each of your production instances is accessible directly when selecting the **[!UICONTROL Subdomains &amp; Certificates]**card.

![](assets/subdomains_list.png)

To get more details on a subdomain, click the **[!UICONTROL Subdomain Details]**button.
La liste de tous les sous-domaines connexes s’affiche. En règle générale, elle contient les sous-domaines des landing pages, des pages de ressources, etc.

L’onglet Informations **[!UICONTROL sur l’]**expéditeur fournit des informations sur les boîtes de réception configurées (expéditeur, réponse, courrier électronique d’erreur).

![](assets/subdomain_details.png)


Dans la liste des sous-domaines, la colonne **[!UICONTROL Dernière vérification]**indique quand un sous-domaine a été vérifié pour la dernière fois.** Vous pouvez lancer une vérification à tout moment en cliquant sur le **... /**[!UICONTROL  Vérifier le bouton de sous-domaine]** .

>[!CAUTION]
>
>Adobe déconseille d’utiliser des sous-domaines sans date de vérification, car cela peut entraîner des problèmes de délivrabilité pour ces sous-domaines.

![](assets/subdomain_verification.png)

Lors du lancement d’une vérification, plusieurs opérations sont effectuées pour vérifier que le sous-domaine est correctement configuré :

1. Le Panneau de configuration vérifie que le sous-domaine appartient au client d’instance.
1. Un courrier électronique est envoyé de l’instance utilisant ce sous-domaine à un ensemble de destinataires de test de &quot;250ok&quot; (une plateforme tierce d’analyse et de délivrabilité des courriers électroniques).
1. Après réception du courrier électronique, 250ok lit les en-têtes de courrier électronique et vérifie si le SPF et le DKIM sont configurés et valides.
1. Le Panneau de configuration sonde en permanence l’état de livraison à partir de 250ok pendant environ 20 minutes. Si le SPF et le DKIM sont transmis, cela signifie que le sous-domaine demandé est vérifié et entièrement configuré et prêt à être utilisé pour l’envoi de courriers électroniques.
