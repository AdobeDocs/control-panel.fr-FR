---
product: campaign
solution: Campaign
title: Surveillance des certificats SSL des sous-domaines
description: Découvrez comment surveiller les certificats SSL de vos sous-domaines
feature: Control Panel
role: Admin
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 100%

---

# Surveillance des certificats SSL des sous-domaines {#monitoring-ssl-certificates}

## À propos des certificats SSL {#about-ssl-certificates}

Adobe Campaign vous recommande de sécuriser les sous-domaines hébergeant vos landing pages, en particulier ceux qui recueillent des informations sensibles sur vos clients.

Le **chiffrement SSL (Secure Socket Layer)** garantit la sécurité des sous-domaines que vous avez configurés en vue de leur fonctionnement avec Adobe. Lorsque votre client remplit un formulaire web ou visite une landing page hébergée par Adobe Campaign, les informations sont envoyées par défaut via un protocole non sécurisé (HTTP). Pour assurer une sécurité supplémentaire, sécurisez les informations envoyées avec un protocole HTTPS. Par exemple, l’adresse du sous-domaine « http://info.monsiteweb.com/ » deviendra « https://info.monsiteweb.com/ ».

**Les certificats SSL ne sont pas installés sur les sous-domaines configurés**. Ils sont installés sur les sous-domaines associés, principalement ceux qui hébergent des landing pages, des pages de ressources, etc.

**Les certificats SSL sont fournis pour une période spécifique** (1 an, 60 jours, etc.). Lorsqu’un certificat arrive à expiration, vous pouvez rencontrer des problèmes lors de l’accès aux landing pages ou de l’utilisation de ressources du sous-domaine. Pour éviter cela, le Panneau de contrôle permet de surveiller les certificats SSL de vos sous-domaines et de lancer une procédure de renouvellement.

![](assets/no_certificate.png)

## Gestion des certificats SSL {#management}

La surveillance des certificats SSL est essentielle pour garantir la sécurité de vos sous-domaines. Depuis le panneau de contrôle, vous pouvez installer et renouveler vous-même les certificats SSL de vos sous-domaines, ou bien les déléguer à Adobe afin que ce processus soit exécuté automatiquement sans intervention de votre part.

Il est vivement recommandé de déléguer la gestion des certificats SSL de vos sous-domaines à Adobe, car Adobe crée automatiquement le certificat et le renouvelle tous les ans avant l’expiration. Vous réduisez ainsi le risque d’erreurs pouvant se produire lors de la gestion manuelle des certificats. [Découvrez comment déléguer les certificats SSL des sous-domaines à Adobe](delegate-ssl.md)

Vous trouverez ci-dessous une liste complète des conséquences liées à la gestion manuelle des certificats, par opposition à la délégation de cette opération à Adobe :

|       | Certificat géré par le client ou la cliente | Certificat géré par Adobe |
|  ---  |  ---  |  ---  |
| Fournisseur de certificats | Autorités de certification tierces | Adobe via les gestionnaires de certificats AWS |
| Étapes manuelles | Génération, achat et installation de CSR | Aucun |
| Processus de renouvellement | Responsabilité du client ou de la cliente | Géré automatiquement par Adobe |
| Sécurité des sous-domaines | Le domaine peut comporter des sous-domaines non sécurisés (tracking, miroir et ressources), sauf si vous installez/renouvelez des certificats. | Chaque nouveau domaine (s’il est sélectionné pour la gestion par Adobe) comporte tous les sous-domaines sécurisés par défaut. |
| Coût du certificat | Le client ou la cliente supporte le coût des certificats | Gratuit |

## Surveillance des certificats SSL {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Détails du sous-domaine"
>abstract="Récupérez des informations sur les certificats SSL de vos sous-domaines."

L’état des certificats SSL de vos sous-domaines est disponible directement dans la liste des sous-domaines en sélectionnant la carte **[!UICONTROL Sous-domaines et certificats]**.

Les sous-domaines sont classés en fonction de la date d’expiration la plus proche du certificat SSL. De plus, des informations visuelles sur l’expiration (délai en jours) sont proposées :

* **Vert** : le sous-domaine n’a pas de certificat arrivant à expiration dans les 60 prochains jours.
* **Orange** : un ou plusieurs sous-domaines ont un certificat qui arrivera à expiration dans les 60 prochains jours.
* **Rouge** : un ou plusieurs sous-domaines ont un certificat qui arrivera à expiration dans les 30 prochains jours.
* **Gris** : aucun certificat n’a été installé pour le sous-domaine.

![](assets/subdomains_list.png)

Pour obtenir plus de détails sur un sous-domaine, cliquez sur le bouton **[!UICONTROL Détails du sous-domaine]**.
La liste de tous les sous-domaines associés s&#39;affiche. En règle générale, elle contient les sous-domaines des landing pages, des pages de ressources, etc.

L’onglet **[!UICONTROL Infos sur l’expéditeur]** fournit des informations sur les boîtes de réception configurées (Expéditeur, Réponse, Email d’erreur).

![](assets/subdomain_details.png)

Si l’un des certificats SSL de votre sous-domaine est sur le point d’arriver à expiration, vous pouvez le renouveler directement depuis le Panneau de contrôle. Pour plus d’informations à ce sujet, consultez la section : [Renouvellement du certificat SSL d’un sous-domaine](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

**Rubriques connexes :**

* [Renouvellement du certificat SSL d’un sous-domaine](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marque des sous-domaines](../../subdomains-certificates/using/subdomains-branding.md)
