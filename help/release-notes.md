---
product: campaign
solution: Campaign
title: Versions du panneau de contrôle
description: Dernières notes de mise à jour du panneau de contrôle.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 8b0f652559e0296a22b3eac92057e6f4487215e1
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 84%

---

# Versions du panneau de contrôle {#control-panel-releases}

Vous trouverez ici des informations sur les dernières versions du panneau de contrôle.

>[!NOTE]
>
>Le panneau de contrôle est accessible à tous les utilisateurs administrateurs. Les étapes permettant d’accorder un accès administrateur à un utilisateur sont présentées dans [cette section](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html#discover-control-panel).
>
>Pour Campaign Classic v7, veuillez noter que votre instance doit être hébergée sur AWS et mise à niveau avec la dernière version de [Gold Standard](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/gs-release/gs-overview.html?lang=fr#release-notes) ou la dernière version de [GA (21.1)](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/latest-release.html?lang=fr#release-notes). Découvrez comment vérifier votre version dans [cette section](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=fr#getting-your-campaign-version). Pour vérifier si votre instance est hébergée sur AWS, suivez les étapes présentées sur [cette page](faq.md).

## Octobre 2021 {#october-2021}

**Plage IP et période de validité des clés publiques**

Il est désormais possible de définir une durée pour la disponibilité des plages d’adresses IP et des clés publiques. En savoir plus dans la section [Listes autorisées des plages d’adresses IP](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) et [Gestion des clés](sftp/using/key-management.md#installing-ssh-key) sections.

**Plage IP et édition de clé publique**

Vous pouvez désormais modifier la variable [Plages IP](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) et [clés publiques](sftp/using/key-management.md#editing-public-keys) que vous créez. Notez que cette fonctionnalité n’est pas disponible pour les éléments créés avant la version actuelle du Panneau de Contrôle.

**Alertes sur la plage IP SFTP et expiration de la clé publique**

La fonctionnalité d’alerte par email inclut désormais des alertes sur l’expiration des listes autorisées d’adresses IP SFTP et l’expiration de la clé publique SFTP. [En savoir plus](performance-monitoring/using/email-alerting.md)

<!--**Full support with Campaign v8**

The **Subdomain** and **Certificate** management capabilities are now supported by Control Panel on Adobe Campaign v8.-->

## Août 2021 {#august-2021}

**Prise en charge de Campaign v8**

Le panneau de contrôle est désormais disponible pour Adobe Campaign v8, à l’exception des fonctionnalités de gestion de **Sous-domaine** et de **Certificat**, qui ne sont pas encore prises en charge. En savoir plus dans la [documentation de Campaign v8](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html){target=&quot;_blank&quot;}

## Octobre 2020 {#october-2020}

**Configuration de sous-domaines à l’aide de CNAME**

Le panneau de contrôle permet maintenant de configurer un sous-domaine pour qu’il fonctionne avec Adobe à l’aide de CNAME, directement depuis l’interface. [En savoir plus](subdomains-certificates/using/setting-up-new-subdomain.md)

**Améliorations de la surveillance des bases de données**

La surveillance des bases de données a été améliorée avec des mesures supplémentaires. Vous pouvez ainsi obtenir des informations détaillées sur les ressources qui consomment de l’espace dans votre base de données. [En savoir plus](performance-monitoring/using/database-monitoring.md)

## Juin 2020 {#june-2020}

**Audit de délivrabilité des sous-domaines**

Après avoir délégué un nouveau sous-domaine, le panneau de contrôle vous permet désormais de suivre l’audit effectué par l’équipe chargée de la délivrabilité. [En savoir plus](subdomains-certificates/using/setting-up-new-subdomain.md)

**Gestion des clés GPG**

Le panneau de contrôle vous permet maintenant de générer une paire de clés GPG pour vous puissiez facilement décrypter les données qui entrent dans Campaign et qui proviennent de l’extérieur. En outre, nous avons ajouté une fonctionnalité permettant d’installer une clé GPG publique pour crypter les données qui sortent de Campaign. [En savoir plus](instances-settings/using/gpg-keys-management.md)

**Surveillance des profils actifs**

Le panneau de contrôle vous permet maintenant de surveiller le nombre de profils actifs utilisés par vos instances et comptabilisés à des fins de facturation. [En savoir plus](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>La surveillance des profils actifs depuis le panneau de contrôle est disponible en version bêta et sujette à de fréquentes mises à jour et modifications sans préavis.

## Mai 2020 {#may-2020}

**Gestion des certificats pour les sous-domaines CNAME**

Le panneau de contrôle permet maintenant de renouveler les certificats SSL de vos sous-domaines qui ont été configurés avec la méthode CNAME. [En savoir plus](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Avril 2020 {#april-2020}

**Gestion des enregistrements TXT Google**

Grâce au panneau de contrôle de Campaign, vous pouvez ajouter des enregistrements de vérification de site TXT Google aux sous-domaines utilisés pour envoyer des emails aux adresses Gmail. [En savoir plus](subdomains-certificates/using/managing-txt-records.md)

**Surveillance de l’espace des bases de données**

Le panneau de contrôle de Campaign dispose de fonctionnalités de surveillance des bases de données, ce qui vous permet d’afficher l’utilisation de l’espace des bases de données à la demande et au fil du temps. [En savoir plus](performance-monitoring/using/database-monitoring.md)

**Alertes par email**

Le panneau de contrôle de Campaign dispose de fonctionnalités d’alerte par email en temps réel. Une fois connecté au panneau de contrôle, vous pouvez vous abonner pour recevoir des alertes lorsque les performances de votre système risquent de se détériorer, ou si une action est nécessaire pour garantir des performances élevées. [En savoir plus](performance-monitoring/using/email-alerting.md)

## Janvier 2020 {#january-2020}

*22 janvier 2020*

De nouvelles fonctionnalités ont été ajoutées pour permettre aux utilisateurs administrateurs de configurer des sous-domaines et de renouveler des certificats SSL à partir du panneau de contrôle.

Pour plus d’informations, reportez-vous aux pages suivantes :
* [Configuration d’un nouveau sous-domaine](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renouvellement du certificat SSL d’un sous-domaine](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Ces fonctionnalités seront disponibles en version bêta. Elle seront sujettes à de fréquentes mises à jour et modifications sans préavis.

## Septembre 2019 {#september-2019}

*16 septembre 2019*

Nous avons ajouté de nouvelles fonctionnalités permettant aux administrateurs d’ajouter des adresses IP à la liste autorisée afin de se connecter aux instances Campaign Classic.
En outre, les utilisateurs administrateurs peuvent maintenant afficher la liste des instances Campaign Classic et l’éligibilité pour les upgrades de build.

Pour plus d’informations, consultez la [documentation dédiée](instances-settings/using/ip-allow-listing-instance-access.md).

## Août 2019 {#august-2019}

De nouvelles fonctionnalités ont été ajoutées pour les utilisateurs administrateurs qui peuvent maintenant recevoir des notifications avant l’expiration des certificats SSL de leurs domaines. Pour plus d’informations, consultez la [documentation détaillée](subdomains-certificates/using/monitoring-ssl-certificates.md).

De plus, ces utilisateurs peuvent maintenant supprimer les clés SSH qui ont été ajoutées pour accéder aux serveurs SFTP.

## Juillet 2019 {#july-2019}

De nouvelles fonctionnalités ont été ajoutées pour permettre aux utilisateurs administrateurs de mieux contrôler les paramètres des instances Campaign Classic. Les nouvelles fonctionnalités du panneau de contrôle comprennent la possibilité d’ajouter des URL auxquelles Adobe Campaign se connecte pour les transferts de données/fichiers.

Pour plus d’informations, consultez la [documentation détaillée](instances-settings/using/url-permissions.md).
