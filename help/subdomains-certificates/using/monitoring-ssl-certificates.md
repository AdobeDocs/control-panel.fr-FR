---
title: Surveillance des certificats SSL des sous-domaines
description: Découvrez comment surveiller les certificats SSL de vos sous-domaines
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# Surveillance des certificats SSL des sous-domaines {#monitoring-ssl-certificates}

Adobe Campaign vous recommande de sécuriser les sous-domaines qui hébergent vos pages d’entrée, en particulier ceux qui collectent des informations sensibles de vos clients.

**Le chiffrement** SSL (Secure Socket Layer) garantit la sécurité des sous-domaines que vous avez délégués à Adobe. Lorsque votre client remplit un formulaire Web ou consulte une page d’entrée hébergée par Adobe Campaign, les informations sont envoyées par défaut via un protocole non sécurisé (HTTP). Pour garantir une sécurité supplémentaire, sécurisez les informations envoyées avec un protocole HTTPS. Par exemple, votre adresse de sous-domaine &quot;http://info.mywebsite.com/&quot; sera désormais &quot;https://info.mywebsite.com/&quot;.

**Les certificats SSL ne sont pas installés sur les sous-domaines délégués eux-mêmes**. Ils sont installés sur les sous-domaines associés, principalement ceux qui hébergent des pages d’entrée, des pages de ressources et d’autres.

**Les certificats SSL sont fournis pour une période** spécifique (1 an, 60 jours, etc.). Une fois qu’un certificat expire, vous pouvez rencontrer des problèmes lors de l’accès aux pages d’entrée ou de l’utilisation des ressources du sous-domaine. Pour éviter cela, le Panneau de configuration vous permet de surveiller les certificats SSL de vos sous-domaines, ainsi que d’initier leur processus de renouvellement.

Plus de détails sur la délégation de sous-domaines sont disponibles [ici](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

La carte **[!UICONTROL Sous-domaines et Certificats]**vous permet de déterminer ceux de vos sous-domaines et sous-domaines associés qui hébergent vos pages d’entrée et vos ressources avec des certificats SSL installés dessus.

Vous pouvez également identifier facilement les sous-domaines dont les certificats expirent et les renouveler, le cas échéant.

>[!NOTE]
>
>Adobe recommande de renouveler un certificat SSL des sous-domaines associés **lorsqu’il se rapproche de la date d’expiration**. Le renouvellement du certificat peut prendre quelques jours selon votre organisation. Nous vous recommandons d’allouer le temps approprié pour ce processus.
<!-- note to remove? immediate, no more delay? -->

La liste des sous-domaines de chaque instance est directement accessible lors de la sélection de la carte **[!UICONTROL Sous-domaines et certificats]**.

Les sous-domaines sont organisés selon la date d’expiration la plus proche du certificat SSL, avec des informations visuelles sur l’expiration, en jours :

* **Vert**: le sous-domaine n’a pas de certificat expirant dans les 60 jours suivants.
* **Orange**: un ou plusieurs sous-domaines possèdent un certificat qui expirera dans les 60 jours suivants.
* **Rouge**: un ou plusieurs sous-domaines disposent d’un certificat qui expirera dans les 30 prochains jours.

![](assets/visual_alert2.png)

Pour plus d’informations sur les certificats d’un sous-domaine, cliquez sur le bouton **[!UICONTROL Détails du certificat]**.

![](assets/certificate_details4.png)

La liste de tous les sous-domaines connexes s’affichera sur leurs certificats. Elle comprend généralement des sous-domaines de pages d&#39;entrée, de pages de ressources, etc.

![](assets/monitoring_subdomains_details2.png)
