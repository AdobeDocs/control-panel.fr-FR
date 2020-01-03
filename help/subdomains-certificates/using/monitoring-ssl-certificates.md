---
title: Surveillance des certificats SSL des sous-domaines
description: Découvrez comment surveiller les certificats SSL de vos sous-domaines
translation-type: tm+mt
source-git-commit: 52f155bbbecec9edabc66cbc28756f9579b81f04

---


# Monitoring subdomains&#39; SSL certificates {#monitoring-ssl-certificates}

## À propos des certificats SSL {#about-ssl-certificates}

Adobe Campaign vous recommande de sécuriser les sous-domaines hébergeant vos landing pages, en particulier ceux qui recueillent des informations sensibles sur vos clients.

Le **cryptage SSL (Secure Socket Layer)** garantit la sécurité des sous-domaines que vous avez délégués à Adobe. Lorsque votre client remplit un formulaire web ou visite une landing page hébergée par Adobe Campaign, les informations sont envoyées par défaut via un protocole non sécurisé (HTTP). Pour assurer une sécurité supplémentaire, sécurisez les informations envoyées avec un protocole HTTPS. Par exemple, l’adresse du sous-domaine « http://info.monsiteweb.com/ » deviendra « https://info.monsiteweb.com/ ».

**Les certificats SSL ne sont pas installés sur les sous-domaines délégués**. Ils sont installés sur les sous-domaines associés, principalement ceux qui hébergent des landing pages, des pages de ressources, etc.

**Les certificats SSL sont fournis pour une période spécifique** (1 an, 60 jours, etc.). Lorsqu’un certificat arrive à expiration, vous pouvez rencontrer des problèmes lors de l’accès aux landing pages ou de l’utilisation de ressources du sous-domaine. Pour éviter cela, le panneau de contrôle permet de surveiller les certificats SSL de vos sous-domaines et de lancer une procédure de renouvellement.

![](assets/no_certificate.png)

## Surveillance des certificats SSL {#monitoring-certificates}

L’état des certificats SSL de vos sous-domaines est disponible directement dans la liste des sous-domaines lors de la sélection de la carte **[!UICONTROL Sous-domaines et certificats]**.

Les sous-domaines sont classés en fonction de la date d’expiration la plus proche du certificat SSL. De plus, des informations visuelles sur l’expiration (délai en jours) sont proposées :

* **Vert** : le sous-domaine n’a pas de certificat arrivant à expiration dans les 60 prochains jours.
* **Orange** : un ou plusieurs sous-domaines ont un certificat qui arrivera à expiration dans les 60 prochains jours.
* **Rouge** : un ou plusieurs sous-domaines ont un certificat qui arrivera à expiration dans les 30 prochains jours.
* **Gris**: aucun certificat n’a été installé pour le sous-domaine.

![](assets/subdomains_list.png)

To get more details on a subdomain, click the **[!UICONTROL Subdomain Details]**button.
La liste de tous les sous-domaines connexes s’affiche. En règle générale, elle contient les sous-domaines des landing pages, des pages de ressources, etc.

L’onglet Informations **[!UICONTROL sur l’]**expéditeur fournit des informations sur les boîtes de réception configurées (expéditeur, réponse, courrier électronique d’erreur).

![](assets/subdomain_details.png)

Si l’un des certificats SSL de votre sous-domaine est sur le point d’expirer, vous pouvez le renouveler directement à partir du Panneau de configuration. Pour plus d&#39;informations à ce sujet, reportez-vous à cette section : [Renouvellement du certificat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)SSL d’un sous-domaine.

>[!NOTE]
>
>Le renouvellement du certificat du Panneau de configuration sera bientôt disponible en version bêta. En attendant, reportez-vous à [cette page](https://helpx.adobe.com/campaign/kb/control-panel-subdomains-certificates.html) pour en savoir plus sur la manière de surveiller les certificats dans le Panneau de configuration.
