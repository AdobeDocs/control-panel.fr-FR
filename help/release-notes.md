---
product: campaign
solution: Campaign
title: Versions du Panneau de contrôle
description: Dernières notes de mise à jour du Panneau de contrôle.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: c52094b8145bdd84aa9e71430a811b8a7b32354d
workflow-type: ht
source-wordcount: '882'
ht-degree: 100%

---

# Versions du Panneau de contrôle {#control-panel-releases}

Vous trouverez ici des informations sur les dernières versions du panneau de contrôle.

>[!NOTE]
>
>Le panneau de contrôle est accessible uniquement aux utilisateurs administrateurs. Pour en savoir plus sur les autorisations, consultez [cette section](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=fr#discover-control-panel).
>
>Pour Campaign Classic v7, votre instance doit être hébergée sur Amazon Web Services (AWS) et mise à niveau vers le dernier [build stable de Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=fr#rn-statuses) (ou vers le build 9032 ou supérieur). Découvrez comment vérifier votre version dans [cette section](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=fr#getting-your-campaign-version). Pour vérifier si votre instance est hébergée sur AWS, suivez les étapes présentées sur [cette page](faq.md#hosted-aws).

## Février 2022 {#february-2022}

**Surveillance des paramètres de workflow**

Vous pouvez désormais surveiller les paramètres de workflow qui peuvent nécessiter une attention particulière pour éviter tout problème sur vos instances. [En savoir plus](performance-monitoring/using/workflow-monitoring.md).

## Janvier 2022 {#january-2022}

**Surveillance des requêtes actives**

Le panneau de contrôle vous permet désormais de surveiller les requêtes qui ont été exécutées le plus longtemps sur vos instances. [En savoir plus](performance-monitoring/using/database-active-queries.md)

**Surveillance des débits et de la latence**

Vous pouvez désormais surveiller les fluctuations des débits de diffusion et de latence sur vos instances au cours d’une période donnée. [En savoir plus](performance-monitoring/using/thoughputs-latencies.md)

**Opérations liées aux certificats SSL sur de nouveaux sous-domaines**

Les opérations liées aux certificats SSL peuvent désormais être effectuées sur un sous-domaine nouvellement créé, même si l’audit de délivrabilité est toujours en cours. [En savoir plus](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Octobre 2021 {#october-2021}

**Période de validité des plages d’adresses IP et des clés publiques**

Il est désormais possible de définir une durée pour la disponibilité des plages d’adresses IP et des clés publiques. Pour en savoir plus, consultez les sections [Liste autorisée des plages d’adresses IP](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) et [Gestion des clés](sftp/using/key-management.md#installing-ssh-key).

**Modification des plages d’adresses IP et des clés publiques**

Vous pouvez désormais modifier les [plages d’adresses IP](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) et les [clés publiques](sftp/using/key-management.md#editing-public-keys) que vous créez. Notez que les éléments créés avant la version actuelle du Panneau de contrôle ne prennent pas en charge cette fonctionnalité.

**Envoi d’alertes lors de l’expiration des plages d’adresses IP et des clés publiques SFTP**

La fonctionnalité de réception d’alertes par email vous avertit désormais lorsque la liste autorisée des adresses IP SFTP et les clés publiques SFTP arrivent à expiration. [En savoir plus](performance-monitoring/using/email-alerting.md)

**Prise en charge complète de Campaign v8**

Les fonctionnalités de gestion des **Sous-domaines** et des **Certificats** sont désormais prises en charge par le Panneau de contrôle dans Adobe Campaign v8.

## Août 2021 {#august-2021}

**Prise en charge de Campaign v8**

Le Panneau de contrôle est désormais disponible pour Adobe Campaign v8, à l’exception des fonctionnalités de gestion de **Sous-domaine** et de **Certificat**, qui ne sont pas encore prises en charge. En savoir plus dans la [documentation de Campaign v8](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html?lang=fr){target=&quot;_blank&quot;}

## Octobre 2020 {#october-2020}

**Configuration de sous-domaines à l’aide de CNAME**

Le Panneau de contrôle permet maintenant de configurer un sous-domaine pour qu’il fonctionne avec Adobe à l’aide de CNAME, directement depuis l’interface. [En savoir plus](subdomains-certificates/using/setting-up-new-subdomain.md)

**Améliorations de la surveillance des bases de données**

La surveillance des bases de données a été améliorée avec des mesures supplémentaires. Vous pouvez ainsi obtenir des informations détaillées sur les ressources qui consomment de l’espace dans votre base de données. [En savoir plus](performance-monitoring/using/database-monitoring.md)

## Juin 2020 {#june-2020}

**Audit de délivrabilité des sous-domaines**

Après avoir délégué un nouveau sous-domaine, le Panneau de contrôle vous permet désormais de suivre l’audit effectué par l’équipe chargée de la délivrabilité. [En savoir plus](subdomains-certificates/using/setting-up-new-subdomain.md)

**Gestion des clés GPG**

Le Panneau de contrôle vous permet maintenant de générer une paire de clés GPG pour vous puissiez facilement déchiffrer les données qui entrent dans dans Campaign et qui proviennent de l’extérieur. En outre, nous avons ajouté une fonctionnalité permettant d’installer une clé GPG publique pour chiffrer les données qui sortent de Campaign. [En savoir plus](instances-settings/using/gpg-keys-management.md)

**Surveillance des profils actifs**

Le Panneau de contrôle vous permet maintenant de surveiller le nombre de profils actifs utilisés par vos instances et comptabilisés à des fins de facturation. [En savoir plus](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>La surveillance des profils actifs depuis le Panneau de contrôle est disponible en version bêta et sujette à de fréquentes mises à jour et modifications sans préavis.

## Mai 2020 {#may-2020}

**Gestion des certificats pour les sous-domaines CNAME**

Le Panneau de contrôle permet maintenant de renouveler les certificats SSL de vos sous-domaines qui ont été configurés avec la méthode CNAME. [En savoir plus](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Avril 2020 {#april-2020}

**Gestion des enregistrements TXT Google**

Grâce au Panneau de contrôle de Campaign, vous pouvez ajouter des enregistrements de vérification de site TXT Google aux sous-domaines utilisés pour envoyer des emails aux adresses Gmail. [En savoir plus](subdomains-certificates/using/managing-txt-records.md)

**Surveillance de l’espace des bases de données**

Le Panneau de contrôle de Campaign dispose de fonctionnalités de surveillance des bases de données, ce qui vous permet d’afficher l’utilisation de l’espace des bases de données à la demande et au fil du temps. [En savoir plus](performance-monitoring/using/database-monitoring.md)

**Alertes par email**

Le Panneau de contrôle de Campaign dispose de fonctionnalités d’alerte par email en temps réel. Une fois connecté au Panneau de contrôle, vous pouvez vous abonner pour recevoir des alertes lorsque les performances de votre système risquent de se détériorer, ou si une action est nécessaire pour garantir des performances élevées. [En savoir plus](performance-monitoring/using/email-alerting.md)

## Janvier 2020 {#january-2020}

*22 janvier 2020*

De nouvelles fonctionnalités ont été ajoutées pour permettre aux utilisateurs administrateurs de configurer des sous-domaines et de renouveler des certificats SSL à partir du Panneau de contrôle.

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

De nouvelles fonctionnalités ont été ajoutées pour permettre aux utilisateurs administrateurs de mieux contrôler les paramètres des instances Campaign Classic. Les nouvelles fonctionnalités du Panneau de contrôle comprennent la possibilité d’ajouter des URL auxquelles Adobe Campaign se connecte pour les transferts de données/fichiers.

Pour plus d’informations, consultez la [documentation détaillée](instances-settings/using/url-permissions.md).
