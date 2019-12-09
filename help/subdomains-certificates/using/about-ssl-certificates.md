---
title: A propos des certificats SSL
description: En savoir plus sur les certificats SSL
translation-type: tm+mt
source-git-commit: 6bc165f995d34d21b5bce379db3095317db10906

---


# A propos des certificats SSL {#about-ssl-certificates}

Adobe Campaign vous recommande de sécuriser les sous-domaines qui hébergent vos pages d’entrée, en particulier ceux qui collectent des informations sensibles de vos clients.

**Le chiffrement** SSL (Secure Socket Layer) garantit la sécurité des sous-domaines que vous avez délégués à Adobe. Lorsque votre client remplit un formulaire Web ou consulte une page d’entrée hébergée par Adobe Campaign, les informations sont envoyées par défaut via un protocole non sécurisé (HTTP). Pour garantir une sécurité supplémentaire, sécurisez les informations envoyées avec un protocole HTTPS. Par exemple, votre adresse de sous-domaine &quot;http://info.mywebsite.com/&quot; sera désormais &quot;https://info.mywebsite.com/&quot;.

**Les certificats SSL ne sont pas installés sur les sous-domaines délégués eux-mêmes**. Ils sont installés sur les sous-domaines associés, principalement ceux qui hébergent des pages d’entrée, des pages de ressources et d’autres.

**Les certificats SSL sont fournis pour une période** spécifique (1 an, 60 jours, etc.). Une fois qu’un certificat expire, vous pouvez rencontrer des problèmes lors de l’accès aux pages d’entrée ou de l’utilisation des ressources du sous-domaine. Pour éviter cela, le Panneau de configuration vous permet de surveiller les certificats SSL de vos sous-domaines, ainsi que d’initier leur processus de renouvellement.

Plus de détails sur la délégation de sous-domaines sont disponibles [ici](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
