---
title: Versions du Panneau de contrôle
translation-type: tm+mt
source-git-commit: 98f2fa0b3e943026bda28b615f0f11db54c404a6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 100%

---


# Versions du Panneau de contrôle {#control-panel-releases}

Vous trouverez ici des informations sur les dernières versions du Panneau de contrôle.

>[!NOTE]
>
>Veuillez noter que le Panneau de contrôle est disponible pour les clients hébergés sur AWS uniquement, à l’exception des environnements hybrides, qui ne sont pas encore pris en charge. Aucune mise à niveau n’est requise pour accéder au panneau de contrôle. Vérifiez que vous êtes un utilisateur administrateur pour y accéder.

## Mai 2020 (#mai-2020)

**Gestion des certificats pour les sous-domaines CNAME**

Le Panneau de contrôle permet maintenant de renouveler les certificats SSL de vos sous-domaines qui ont été délégués avec la méthode CNAME. [En savoir plus](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Avril 2020 {#april-2020}

**Gestion des enregistrements TXT Google**

Grâce au Panneau de contrôle de Campaign, vous pouvez ajouter des enregistrements de vérification de site TXT Google aux sous-domaines utilisés pour envoyer des emails aux adresses Gmail. [En savoir plus](subdomains-certificates/using/managing-txt-records.md)

**Surveillance de l’espace des bases de données**

Le Panneau de contrôle de Campaign dispose de fonctionnalités de surveillance des bases de données, ce qui vous permet d’afficher l’utilisation de l’espace des bases de données à la demande et au fil du temps. [En savoir plus](performance-monitoring/using/database-monitoring.md)

**Alertes par email**

Le Panneau de contrôle de Campaign dispose de fonctionnalités d’alerte par email en temps réel. Une fois connecté au Panneau de contrôle, vous pouvez vous abonner pour recevoir des alertes lorsque les performances de votre système risquent de se détériorer, ou si une action est nécessaire pour garantir des performances élevées. [En savoir plus](performance-monitoring/using/email-alerting.md)

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
