---
title: Surveillance des certificats SSL des sous-domaines
description: Découvrez comment surveiller les certificats SSL de vos sous-domaines
translation-type: tm+mt
source-git-commit: 52f155bbbecec9edabc66cbc28756f9579b81f04

---


# Surveillance des sous-domaines {#monitoring-subdomains}

Il est essentiel de surveiller vos sous-domaines pour vous assurer qu’ils sont tous correctement configurés pour fonctionner avec Adobe Campaign.

The list of subdomains for each of your production instances is accessible directly when selecting the **[!UICONTROL Subdomains &amp; Certificates]**card.

![](assets/subdomains_list.png)

Dans la liste des sous-domaines, la colonne **[!UICONTROL Dernière vérification]**indique quand un sous-domaine a été vérifié pour la dernière fois.** Vous pouvez lancer une vérification à tout moment en cliquant sur le **... /**[!UICONTROL  Vérifier le bouton de sous-domaine]** .

![](assets/subdomain_verification.png)

>[!CAUTION]
>
>Adobe déconseille d’utiliser des sous-domaines sans date de vérification, car cela peut entraîner des problèmes de délivrabilité pour ces sous-domaines.

Lors du lancement d’une vérification, plusieurs opérations sont effectuées pour vérifier que le sous-domaine est correctement configuré (contrôle du client d’instance, test d’envoi de courrier électronique, etc.)

Si la vérification du sous-domaine échoue, contactez le service à la clientèle Adobe pour plus d’informations.
