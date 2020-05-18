---
title: Versions du Panneau de contrôle
translation-type: tm+mt
source-git-commit: 49d84c42446ed1fc996b9d57005565b15ca24e77
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 61%

---


# Versions du Panneau de contrôle {#control-panel-releases}

Vous trouverez ici des informations sur les dernières versions du Panneau de contrôle.

>[!NOTE]
>
>Veuillez noter que le Panneau de configuration est disponible pour les clients hébergés sur AWS uniquement, à l’exception des environnements hybrides qui ne sont pas encore pris en charge. Aucune mise à niveau n’est requise pour accéder au panneau de contrôle. Vérifiez que vous êtes un utilisateur administrateur pour y accéder.

## Mai 2020 (#mai-2020)

**Gestion des clés GPG**

Le Panneau de configuration vous permet désormais de générer une paire de clés GPG, afin que vous puissiez facilement déchiffrer les données arrivant à Campaign de l&#39;extérieur. En outre, nous avons ajouté une fonctionnalité permettant d&#39;installer une clé GPG publique pour chiffrer les données en quittant Campaign. [En savoir plus](instances-settings/using/gpg-keys-management.md)

**Gestion des certificats pour les sous-domaines CNAME**

Le Panneau de configuration vous permet désormais de renouveler les certificats SSL de vos sous-domaines qui ont été délégués avec la méthode CNAME. [En savoir plus](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Avril 2020 {#april-2020}

**Gestion des enregistrements TXT Google**

Grâce au Panneau de contrôle de Campaign, vous pouvez ajouter des enregistrements de vérification de site TXT Google aux sous-domaines utilisés pour envoyer des emails aux adresses Gmail. [En savoir plus](subdomains-certificates/using/managing-txt-records.md)

**Surveillance de l’espace des bases de données**

Le Panneau de configuration Campaign est doté de fonctionnalités de surveillance de base de données, ce qui vous permet de vue à la demande et au fil du temps l’utilisation de l’espace de base de données. [En savoir plus](performance-monitoring/using/database-monitoring.md)

**Alertes par email**

Le Panneau de configuration Campaign est doté de fonctions d&#39;alerte par courriel en temps réel, ce qui vous permet de vous connecter au Panneau de configuration et de vous inscrire pour recevoir des alertes lorsque votre système risque de se détériorer, ou une action est nécessaire pour garantir des performances élevées pour l&#39;avenir. [En savoir plus](performance-monitoring/using/email-alerting.md)

## Janvier 2020 {#january-2020}

*22 janvier 2020*

De nouvelles fonctionnalités ont été ajoutées pour permettre aux utilisateurs administrateurs de déléguer des sous-domaines et de renouveler des certificats SSL à partir du panneau de contrôle.

Pour plus d’informations, reportez-vous aux pages suivantes :
* [Configuration d’un nouveau sous-domaine](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renouvellement du certificat SSL d’un sous-domaine](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Ces fonctionnalités seront disponibles en version bêta. Elle seront sujettes à de fréquentes mises à jour et modifications sans préavis.

## Septembre 2019 {#september-2019}

*16 septembre 2019*

De nouvelles fonctionnalités ont été ajoutées pour que les utilisateurs administrateurs puissent whitelister des adresses IP afin de se connecter aux instances Campaign Classic.
En outre, les utilisateurs administrateurs peuvent maintenant afficher la liste des instances Campaign Classic et l’éligibilité pour les upgrades de build.

Pour plus d’informations, consultez la [documentation dédiée](instances-settings/using/ip-whitelisting-instance-access.md).

## Août 2019 {#august-2019}

De nouvelles fonctionnalités ont été ajoutées pour les utilisateurs administrateurs qui peuvent maintenant recevoir des notifications avant l’expiration des certificats SSL de leurs domaines. Pour plus d&#39;informations, consultez la [documentation détaillée](subdomains-certificates/using/monitoring-ssl-certificates.md).

De plus, les utilisateurs Admin peuvent maintenant supprimer les clés SSH qui ont été ajoutées pour accéder aux serveurs SFTP.

## Juillet 2019 {#july-2019}

De nouvelles fonctionnalités ont été ajoutées pour permettre aux utilisateurs administrateurs de mieux contrôler les paramètres des instances Campaign Classic. Les nouvelles fonctionnalités du Panneau de contrôle comprennent la possibilité d’ajouter des URL auxquelles Adobe Campaign se connecte pour les transferts de données/fichiers.

Pour plus d&#39;informations, consultez la [documentation détaillée](instances-settings/using/url-permissions.md).
