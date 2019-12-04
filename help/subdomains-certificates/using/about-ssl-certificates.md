---
title: A propos des certificats SSL
description: En savoir plus sur les certificats SSL
translation-type: tm+mt
source-git-commit: ce93b595f4fbc2b3d72aadd034f93392565cb0e2

---


# A propos des certificats SSL {#about-ssl-certificates}

Adobe Campaign vous recommande de sécuriser les sous-domaines qui hébergent vos pages d’entrée, en particulier ceux qui collectent des informations sensibles de vos clients.

Le **cryptage SSL (Secure Socket Layer)** garantit la sécurité des sous-domaines que vous avez délégués à Adobe. Lorsque votre client remplit un formulaire web ou visite une landing page hébergée par Adobe Campaign, les informations sont envoyées par défaut via un protocole non sécurisé (HTTP). Pour assurer une sécurité supplémentaire, sécurisez les informations envoyées avec un protocole HTTPS. Par exemple, votre adresse de sous-domaine "http://info.mywebsite.com/" sera désormais "https://info.mywebsite.com/".

**Les certificats SSL ne sont pas installés sur les sous-domaines délégués**. Ils sont installés sur les sous-domaines associés, principalement ceux qui hébergent des pages d’entrée, des pages de ressources et d’autres.

**Les certificats SSL sont fournis pour une période** spécifique (1 an, 60 jours, etc.). Lorsqu'un certificat arrive à expiration, vous pouvez rencontrer des problèmes lors de l'accès aux landing pages ou de l'utilisation de ressources du sous-domaine. Pour éviter cela, le panneau de contrôle permet de surveiller les certificats SSL de vos sous-domaines et de lancer une procédure de renouvellement.

More details on subdomain delegation is available [here](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
