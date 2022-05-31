---
product: campaign
solution: Campaign
title: Versions du Panneau de contrôle
description: Cette page répertorie toutes les nouvelles fonctionnalités et améliorations apportées au Panneau de contrôle.
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 87b28195ede08756d5084aad36bf1c95f621b5f5
workflow-type: ht
source-wordcount: '1174'
ht-degree: 100%

---

# Versions du Panneau de contrôle {#control-panel-releases}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations apportées au Panneau de contrôle.

>[!NOTE]
>
>Le panneau de contrôle est accessible uniquement aux utilisateurs administrateurs. Pour en savoir plus sur les autorisations, consultez [cette section](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=fr#discover-control-panel).
>
>Pour Campaign v7, votre instance doit être hébergée sur Amazon Web Services (AWS) et mise à niveau vers le dernier [build stable de Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=fr#rn-statuses) (ou vers le build 9032 ou supérieur). Découvrez comment vérifier votre version dans [cette section](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=fr#getting-your-campaign-version). Pour vérifier si votre instance est hébergée sur AWS, suivez les étapes présentées sur [cette page](faq.md#hosted-aws).

## Mai 2022 {#may-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilité du panneau de contrôle pour le modèle d’hébergement hybride</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le panneau de contrôle est désormais disponible pour les clients ayant un modèle d’hébergement hybride. Ces clients peuvent tirer parti des fonctionnalités du panneau de contrôle en fournissant l’URL de leur instance MID/RT configurée dans leur instance marketing dans le panneau de contrôle.</p><p>Pour plus d’informations, consultez la <a href="instances-settings/using/external-accounts.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mises à jour de la surveillance des débits et des latences</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les fonctionnalités de surveillance des débits et des latences ont été améliorées :<ul><li>Vous pouvez maintenant déterminer les identifiants des 5 diffusions les plus importantes qui contribuent au débit de votre instance.</li><li>Les clients Campaign Classic v7/v8 peuvent désormais visualiser la latence d’un canal spécifique.</p></li><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/thoughputs-latencies.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


## Avril 2022 {#april-2022}

<table>
<thead>
<tr>
<th><strong>Surveiller les contacts principaux et les événements sur vos instances</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais surveiller les versions antérieures et à venir ainsi que les révisions de service se produisant sur vos instances. Vous pouvez également accéder à une liste de contacts principaux chez Adobe pour toute demande ou problème.</p><p>Pour plus d’informations, consultez la <a href="service-events/service-events.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

## Mars 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilité de la surveillance des débits et de la latence</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La surveillance des débits et de la latence est désormais disponible pour tous les clients Campaign Standard et v8, ainsi que pour les clients Campaign v7 qui ont les numéros de build 9032, 9330, 9346 ou 9349 et des déploiements Stand-alone (sans instance MID).</p><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/thoughputs-latencies.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

## Février 2022 {#february-2022}

<table>
<thead>
<tr>
<th><strong>Surveillance des paramètres de workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais surveiller les paramètres de workflow qui peuvent nécessiter une attention particulière pour éviter tout problème sur vos instances. </p><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/workflow-monitoring.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

## Janvier 2022 {#january-2022}

<table>
<thead>
<tr>
<th><strong>Surveillance des requêtes actives</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Panneau de contrôle vous permet désormais de surveiller les requêtes qui ont été exécutées le plus longtemps sur vos instances.</p><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/database-active-queries.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Surveillance des débits et de la latence</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais surveiller les fluctuations des débits de diffusion et de latence sur vos instances au cours d’une période donnée.</p><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/thoughputs-latencies.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Opérations liées aux certificats SSL sur de nouveaux sous-domaines</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les opérations liées aux certificats SSL peuvent désormais être effectuées sur un sous-domaine nouvellement créé, même si l’audit de délivrabilité est toujours en cours.</p><p>Pour plus d’informations, consultez la <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

## Octobre 2021 {#october-2021}

<table>
<thead>
<tr>
<th><strong>Période de validité des plages d’adresses IP et des clés publiques</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il est désormais possible de définir une durée pour la disponibilité des plages d’adresses IP et des clés publiques. </p><p>Pour plus d’informations, consultez les sections <a href="sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list">Listes autorisées des plages d’adresses IP</a> et <a href="sftp/using/key-management.md#installing-ssh-key">Gestion des clés</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modification des plages d’adresses IP et des clés publiques</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais modifier les <a href="sftp/using/ip-range-allow-listing.md#editing-ip-ranges">plages d’adresses IP</a> et les <a href="sftp/using/key-management.md#editing-public-keys">clés publiques</a> que vous créez. Notez que les éléments créés avant la version actuelle du Panneau de contrôle ne prennent pas en charge cette fonctionnalité.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envoi d’alertes lors de l’expiration des plages d’adresses IP et des clés publiques SFTP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La fonctionnalité de réception d’alertes par e-mail vous avertit désormais lorsque la liste autorisée des adresses IP SFTP et les clés publiques SFTP arrivent à expiration.</p><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/email-alerting.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge complète de Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les fonctionnalités de gestion des <strong>Sous-domaines</strong> et des <strong>Certificats</strong> sont désormais prises en charge par le Panneau de contrôle dans Adobe Campaign v8</a>.</p>
</td>
</tr>
</tbody>
</table>

## Août 2021 {#august-2021}

<table>
<thead>
<tr>
<th><strong>Prise en charge de Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Panneau de contrôle est désormais disponible pour Adobe Campaign v8, à l’exception des fonctionnalités de gestion de <strong>Sous-domaines</strong> et de <strong>Certificats</strong>, qui ne sont pas encore prises en charge.</p><p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html?lang=fr" target="blank">documentation de Campaign v8</a>.</p>
</td>
</tr>
</tbody>
</table>

## Octobre 2020 {#october-2020}

<table>
<thead>
<tr>
<th><strong>Configuration de sous-domaines à l’aide de CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Panneau de contrôle permet désormais de configurer un sous-domaine pour qu’il fonctionne avec Adobe à l’aide de CNAME, directement depuis l’interface.</p><p>Pour plus d’informations, consultez la <a href="subdomains-certificates/using/setting-up-new-subdomain.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Améliorations apportées à la surveillance des bases de données</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La surveillance des bases de données a été améliorée à l’aide de mesures supplémentaires. Vous pouvez ainsi obtenir des informations détaillées sur les ressources qui consomment de l’espace dans votre base de données.</p><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/database-monitoring.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

## Juin 2020 {#june-2020}

<table>
<thead>
<tr>
<th><strong>Audit de délivrabilité des sous-domaines</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Après avoir délégué un nouveau sous-domaine, le Panneau de contrôle vous permet de suivre l’audit effectué par l’équipe chargée de la délivrabilité.</p><p>Pour plus d’informations, consultez la <a href="subdomains-certificates/using/setting-up-new-subdomain.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestion des clés GPG</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Panneau de contrôle vous permet désormais de générer une paire de clés GPG afin que vous puissiez facilement déchiffrer les données qui entrent dans Campaign de l’extérieur. De plus, nous avons ajouté une fonctionnalité permettant d’installer une clé GPG publique afin de chiffrer les données qui sortent de Campaign.</p><p>Pour plus d’informations, consultez la <a href="instances-settings/using/gpg-keys-management.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Surveillance des profils actifs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Panneau de contrôle vous permet désormais de surveiller le nombre de profils actifs utilisés par vos instances et comptabilisés à des fins de facturation.</p><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/active-profiles-monitoring.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>La surveillance des profils actifs depuis le Panneau de contrôle est disponible en version Beta et est sujette à de fréquentes mises à jour et modifications sans préavis.

## Mai 2020 {#may-2020}

<table>
<thead>
<tr>
<th><strong>Gestion des certificats pour les sous-domaines CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Panneau de contrôle permet désormais de renouveler les certificats SSL de vos sous-domaines qui ont été configurés par la méthode CNAME.</p><p>Pour plus d’informations, consultez la <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

## Avril 2020 {#april-2020}

<table>
<thead>
<tr>
<th><strong>Gestion des enregistrements TXT Google</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au Panneau de contrôle de Campaign, vous pouvez ajouter des enregistrements de vérification de site TXT Google aux sous-domaines utilisés pour envoyer des e-mails aux adresses Gmail.</p><p>Pour plus d’informations, consultez la <a href="subdomains-certificates/using/managing-txt-records.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Surveillance de l’espace des bases de données</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Panneau de contrôle de Campaign dispose de fonctionnalités de surveillance des bases de données, ce qui vous permet d’afficher l’utilisation de l’espace des bases de données à la demande et dans le temps.</p><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/database-monitoring.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alertes par e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Panneau de contrôle de Campaign dispose de fonctionnalités d’alerte par e-mail en temps réel. Une fois connecté au Panneau de contrôle, vous pouvez vous abonner pour recevoir des alertes lorsque les performances de votre système risquent de se détériorer ou si une action est nécessaire pour garantir des performances élevées.</p><p>Pour plus d’informations, consultez la <a href="performance-monitoring/using/email-alerting.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

## Janvier 2020 {#january-2020}

De nouvelles fonctionnalités ont été ajoutées pour permettre aux utilisateurs administrateurs de configurer des sous-domaines et de renouveler des certificats SSL à partir du Panneau de contrôle.

Pour plus d’informations, reportez-vous aux pages suivantes :
* [Configuration d’un nouveau sous-domaine](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renouvellement du certificat SSL d’un sous-domaine](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Ces fonctionnalités seront disponibles en version bêta. Elle seront sujettes à de fréquentes mises à jour et modifications sans préavis.

## Septembre 2019 {#september-2019}

Nous avons ajouté de nouvelles fonctionnalités permettant aux administrateurs d’ajouter des adresses IP à la liste autorisée afin de se connecter aux instances Campaign v7/v8.
De plus, les utilisateurs administrateurs peuvent maintenant afficher la liste des instances Campaign v7/v8 et l’éligibilité pour les upgrades de build.

Pour plus d’informations, consultez la [documentation dédiée](instances-settings/using/ip-allow-listing-instance-access.md).

## Août 2019 {#august-2019}

De nouvelles fonctionnalités ont été ajoutées pour les utilisateurs administrateurs qui peuvent maintenant recevoir des notifications avant l’expiration des certificats SSL de leurs domaines. Pour plus d’informations, consultez la [documentation détaillée](subdomains-certificates/using/monitoring-ssl-certificates.md).

De plus, ces utilisateurs peuvent maintenant supprimer les clés SSH qui ont été ajoutées pour accéder aux serveurs SFTP.

## Juillet 2019 {#july-2019}

De nouvelles fonctionnalités ont été ajoutées pour permettre aux utilisateurs administrateurs de mieux contrôler les paramètres des instances Campaign v7/v8. Les nouvelles fonctionnalités du Panneau de contrôle comprennent la possibilité d’ajouter des URL auxquelles Adobe Campaign se connecte pour les transferts de données/fichiers.

Pour plus d’informations, consultez la [documentation détaillée](instances-settings/using/url-permissions.md).
