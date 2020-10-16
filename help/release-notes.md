---
title: Versions du Panneau de contrôle
translation-type: tm+mt
source-git-commit: 1c7e5a830ff9a6b6a726cfbe30ca2ad264f1d8c6
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 80%

---


# Versions du Panneau de contrôle {#control-panel-releases}

Vous trouverez ici des informations sur les dernières versions de Panneau de Contrôle.

>[!NOTE]
>
>Veuillez noter que le Panneau de contrôle est disponible pour les clients hébergés sur AWS uniquement, à l’exception des environnements hybrides, qui ne sont pas encore pris en charge. Aucune mise à niveau n’est requise pour accéder au panneau de contrôle. Vérifiez que vous êtes un utilisateur administrateur pour y accéder.

## Octobre 2020 {#october-2020}

**Configuration de sous-domaines à l’aide de CNAME**

Le Panneau de Contrôle vous permet désormais de configurer un sous-domaine pour qu’il fonctionne avec l’Adobe à l’aide de CNAME directement depuis l’interface. [En savoir plus](subdomains-certificates/using/setting-up-new-subdomain.md)

**Améliorations de la surveillance des bases de données**

L&#39;onglet Surveillance **[!UICONTROL de la]** base de données a été amélioré avec des mesures supplémentaires, ce qui vous permet d&#39;obtenir des informations détaillées sur les ressources qui consomment de l&#39;espace sur votre base de données. [En savoir plus](performance-monitoring/using/database-monitoring.md)

## Juin 2020 {#june-2020}

**Audit de délivrabilité des sous-domaines**

Après avoir délégué un nouveau sous-domaine, le panneau de contrôle vous permet désormais de suivre l’audit effectué par l’équipe chargée de la délivrabilité. [En savoir plus](subdomains-certificates/using/setting-up-new-subdomain.md)

**Gestion des clés GPG**

Le Panneau de contrôle vous permet maintenant de générer une paire de clés GPG pour vous puissiez facilement décrypter les données qui entrent dans dans Campaign et qui proviennent de l’extérieur. En outre, nous avons ajouté une fonctionnalité permettant d’installer une clé GPG publique pour crypter les données qui sortent de Campaign. [En savoir plus](instances-settings/using/gpg-keys-management.md)
* [Tutoriels vidéo sur Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/gpg-key-management/gpg-key-management-overview.html)
* [Tutoriels vidéo sur Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/gpg-key-management/gpg-key-management-overview.html)

**Surveillance des profils actifs**

Le panneau de contrôle vous permet maintenant de surveiller le nombre de profils actifs utilisés par vos instances et comptabilisés à des fins de facturation. [En savoir plus](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>La surveillance des profils actifs depuis le panneau de contrôle est disponible en version bêta et sujette à de fréquentes mises à jour et modifications sans préavis.
>
>Cette fonctionnalité est disponible pour les clients hébergés sur AWS depuis le build Campaign Standard 10368 et le build Campaign Classic 8931. Si vous utilisez un build antérieur, vous devez effectuer la mise à niveau pour utiliser cette fonctionnalité.

## Mai 2020 {#may-2020}

**Gestion des certificats pour les sous-domaines CNAME**

Le Panneau de Contrôle vous permet désormais de renouveler les certificats SSL de vos sous-domaines qui ont été configurés avec la méthode CNAME. [En savoir plus](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Avril 2020 {#april-2020}

**Gestion des enregistrements TXT Google**

Grâce au Panneau de contrôle de Campaign, vous pouvez ajouter des enregistrements de vérification de site TXT Google aux sous-domaines utilisés pour envoyer des emails aux adresses Gmail. [En savoir plus](subdomains-certificates/using/managing-txt-records.md)

**Surveillance de l’espace des bases de données**

Le Panneau de contrôle de Campaign dispose de fonctionnalités de surveillance des bases de données, ce qui vous permet d’afficher l’utilisation de l’espace des bases de données à la demande et au fil du temps. [En savoir plus](performance-monitoring/using/database-monitoring.md)

**Alertes par email**

Le Panneau de contrôle de Campaign dispose de fonctionnalités d’alerte par email en temps réel. Une fois connecté au Panneau de contrôle, vous pouvez vous abonner pour recevoir des alertes lorsque les performances de votre système risquent de se détériorer, ou si une action est nécessaire pour garantir des performances élevées. [En savoir plus](performance-monitoring/using/email-alerting.md)

## Janvier 2020 {#january-2020}

*22 janvier 2020*

Nous avons ajouté de nouvelles fonctionnalités permettant aux administrateurs de configurer des sous-domaines et de renouveler les certificats SSL à partir du Panneau de Contrôle.

Pour plus d’informations, reportez-vous aux pages suivantes :
* [Configuration d’un nouveau sous-domaine](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renouvellement du certificat SSL d’un sous-domaine](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Ces fonctionnalités seront disponibles en version bêta. Elle seront sujettes à de fréquentes mises à jour et modifications sans préavis.

## Septembre 2019 {#september-2019}

*16 septembre 2019*

Nous avons ajouté de nouvelles fonctionnalités permettant aux administrateurs d’ajouter des adresses IP à la liste autorisée afin de se connecter aux instances Campaign Classic.
En outre, les utilisateurs administrateurs peuvent maintenant afficher la liste des instances Campaign Classic et l’éligibilité pour les upgrades de build.

Pour plus d’informations, consultez la [documentation dédiée](instances-settings/using/ip-allow-listing-instance-access.md).

## Août 2019 {#august-2019}

De nouvelles fonctionnalités ont été ajoutées pour les utilisateurs administrateurs qui peuvent maintenant recevoir des notifications avant l’expiration des certificats SSL de leurs domaines. Pour plus d’informations, consultez la [documentation détaillée](subdomains-certificates/using/monitoring-ssl-certificates.md).

De plus, les utilisateurs Admin peuvent maintenant supprimer les clés SSH qui ont été ajoutées pour accéder aux serveurs SFTP.

## Juillet 2019 {#july-2019}

De nouvelles fonctionnalités ont été ajoutées pour permettre aux utilisateurs administrateurs de mieux contrôler les paramètres des instances Campaign Classic. Les nouvelles fonctionnalités du Panneau de contrôle comprennent la possibilité d’ajouter des URL auxquelles Adobe Campaign se connecte pour les transferts de données/fichiers.

Pour plus d’informations, consultez la [documentation détaillée](instances-settings/using/url-permissions.md).
