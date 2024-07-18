---
title: Notes de mise à jour 2022
description: Cette page répertorie toutes les versions 2022 du panneau de contrôle.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9fb18bb6-c4e4-48aa-849c-d9129add5266
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 100%

---

# Notes de mise à jour 2022 {#rn-2022}

## Octobre 2022 {#october-2022}

Les alertes par e-mail vous avertissent désormais lorsque l’un de vos certificats SSL arrive à expiration dans 30 jours ou moins. [En savoir plus](../performance-monitoring/using/email-alerting.md)

## Septembre 2022 {#september-2022}

Les clientes et clients disposant d’un modèle d’hébergement hybride peuvent désormais configurer de nouveaux sous-domaines. [En savoir plus](../subdomains-certificates/using/setting-up-new-subdomain.md)

## Août 2022 {#august-2022}

* Les clientes et clients disposant d’un modèle d’hébergement hybride peuvent désormais vérifier leurs sous-domaines. [En savoir plus](../subdomains-certificates/using/monitoring-subdomains.md)
* Le champ Unité d’organisation (UO) est désormais facultatif dans la demande de génération de certificat (CSR). [En savoir plus](../subdomains-certificates/using/renewing-subdomain-certificate.md)

## Juillet 2022 {#july-2022}

<table>
<thead>
<tr>
<th><strong>Installation des certificats des sous-domaines pour le modèle d’hébergement hybride</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>Les clientes et clients disposant d’un modèle d’hébergement hybride peuvent désormais renouveler les certificats SSL de leurs sous-domaines à partir du panneau de contrôle.</p><p>Pour plus d’informations, consultez la <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

## Juin 2022 {#june-2022}

### Nouveautés

<table>
<thead>
<tr>
<th><strong>Les 10 premiers fichiers consommant de l’espace sur les serveurs SFTP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant identifier les 10 fichiers qui consomment le plus d’espace sur un serveur SFTP. <a href="../sftp/using/sftp-storage-management.md">En savoir plus</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rappels du calendrier de service</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le calendrier de service vous permet désormais de définir des rappels afin d’être averti par e-mail avant qu’un événement ne se produise sur vos instances. <a href="../service-events/service-events.md">En savoir plus</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Améliorations de la génération de la CSR des sous-domaines</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Plusieurs améliorations ont été apportées au processus de génération de la demande de signature de certificat (CSR). <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">En savoir plus</a></p><ul><li>Lors de la génération d’une demande de signature de certificat, vous pouvez désormais sélectionner l’un des sous-domaines inclus comme nom commun.</li><li>Vous pouvez désormais copier le résumé de la demande de signature de certificat avant de la générer.</li><li>Une fois qu’une demande de signature de certificat a été générée, vous pouvez la télécharger à nouveau à partir des logs de traitement. Cette fonctionnalité ne s’applique pas aux certificats générés avant cette version.</li></ul><p>

</td>
</tr>
</tbody>
</table>

### Améliorations

**Paramètres des instances**

* Le nombre maximum de clés GPG du panneau de contrôle a été porté à 60. [En savoir plus](../instances-settings/using/gpg-keys-management.md)

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
<p>Le panneau de contrôle est désormais disponible pour les clientes et clients ayant un modèle d’hébergement hybride. Ces personnes peuvent tirer parti des fonctionnalités du panneau de contrôle en fournissant l’URL de leur instance MID/RT configurée dans leur instance marketing dans le panneau de contrôle.</p><p>Pour plus d’informations, consultez la <a href="../instances-settings/using/external-accounts.md">documentation détaillée</a>.</p>
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
<p>Les fonctionnalités de surveillance des débits et des latences ont été améliorées :<ul><li>Vous pouvez maintenant déterminer les identifiants des 5 diffusions les plus importantes qui contribuent au débit de votre instance.</li><li>Si vous utilisez Campaign Classic v7/v8, vous pouvez désormais visualiser la latence d’un canal spécifique.</p></li><p>Pour plus d’informations, consultez la <a href="../performance-monitoring/using/throughputs-latencies.md">documentation détaillée</a>.</p>
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
<p>Vous pouvez désormais surveiller les versions antérieures et à venir ainsi que les révisions de service se produisant sur vos instances. Vous pouvez également accéder à une liste de contacts principaux chez Adobe pour toute demande ou problème.</p><p>Pour plus d’informations, consultez la <a href="../service-events/service-events.md">documentation détaillée</a>.</p>
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
<p>La surveillance des débits et de la latence est désormais disponible pour les clientes et clients Campaign Standard et v8, ainsi que pour les clientes et clients Campaign v7 qui ont les numéros de build 9032, 9330, 9346 ou 9349 et des déploiements Stand-alone (sans instance MID).</p><p>Pour plus d’informations, consultez la <a href="../performance-monitoring/using/throughputs-latencies.md">documentation détaillée</a>.</p>
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
<p>Vous pouvez désormais surveiller les paramètres de workflow qui peuvent nécessiter une attention particulière pour éviter tout problème sur vos instances. </p><p>Pour plus d’informations, consultez la <a href="../performance-monitoring/using/workflow-monitoring.md">documentation détaillée</a>.</p>
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
<p>Le Panneau de contrôle vous permet désormais de surveiller les requêtes qui ont été exécutées le plus longtemps sur vos instances.</p><p>Pour plus d’informations, consultez la <a href="../performance-monitoring/using/database-active-queries.md">documentation détaillée</a>.</p>
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
<p>Vous pouvez désormais surveiller les fluctuations des débits de diffusion et de latence sur vos instances au cours d’une période donnée.</p><p>Pour plus d’informations, consultez la <a href="../performance-monitoring/using/throughputs-latencies.md">documentation détaillée</a>.</p>
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
<p>Les opérations liées aux certificats SSL peuvent désormais être effectuées sur un sous-domaine nouvellement créé, même si l’audit de délivrabilité est toujours en cours.</p><p>Pour plus d’informations, consultez la <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>
