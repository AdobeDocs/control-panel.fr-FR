---
title: Surveillance des certificats SSL des sous-domaines
description: Découvrez comment surveiller les certificats SSL de vos sous-domaines
translation-type: tm+mt
source-git-commit: c51a43fb310bbb8bd7570bc4ea668d708159535c

---


# Surveillance de vos sous-domaines {#monitoring-subdomains}

Il est essentiel de surveiller vos sous-domaines pour vous assurer qu’ils sont tous correctement configurés pouren vue de fonctionner avec Adobe Campaign.

La liste des sous-domaines de chacune de vos instances de production est directement accessible en sélectionnant la carte **[!UICONTROL Sous-domaines et certificats]**.

The **[!UICONTROL Last verification]**column indicates when a subdomain was verified for the last time. Vous pouvez lancer une vérification à tout moment en cliquant sur le bouton**...**/**[!UICONTROL  Vérifier le sous-domaine]**.

![](assets/subdomain_verification.png)

>[!CAUTION]
>
>Adobe déconseille d’utiliser des sous-domaines sans date de certificat, car cela peut entraîner des problèmes de délivrabilité pour ces sous-domaines.

Lors du lancement d’une vérification, plusieurs opérations sont effectuées pour vérifier que le sous-domaine est correctement configuré (contrôle du client d’instance, test d’envoi de courrier électronique, etc.)

Si la vérification du sous-domaine échoue, contactez le service à la clientèle Adobe pour plus d’informations.
