---
title: Notes de mise à jour 2023
description: Cette page répertorie toutes les versions 2023 du panneau de contrôle.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 100%

---

# Notes de mise à jour 2023 {#rn-2023}

## Septembre 2023 {#september-2023}

<table>
<thead>
<tr>
<th><strong>Gestion des enregistrements DMARC et BIMI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>Vous pouvez maintenant ajouter des enregistrements DMARC et BIMI directement depuis le panneau de contrôle :

<ul><li>Les <strong>enregistrements DMARC</strong> offrent un moyen d’authentifier le domaine de la personne expéditrice et d’empêcher l’utilisation non autorisée du domaine à des fins malveillantes. <a href="../subdomains-certificates/using/dmarc.md">Découvrez comment ajouter des enregistrements DMARC.</a></li>
<li>Les <strong>enregistrements BIMI</strong> vous permettent d’afficher un logo approuvé en regard de vos e-mails dans les boîtes de réception des fournisseurs de messagerie afin d’améliorer la reconnaissance de la marque et la confiance en elle. <a href="../subdomains-certificates/using/bimi.md">Découvrez comment ajouter des enregistrements BIMI.</a></li></ul>
</td>
</tr>
</tbody>
</table>

## Juin 2023 {#june-2023}

* Vous pouvez désormais déléguer les certificats SSL des sous-domaines déjà délégués à Adobe directement à partir de la liste des sous-domaines. [En savoir plus](../subdomains-certificates/using/delegate-ssl.md).

* L’expéditeur des e-mails d’alerte a été remplacé par `"alert@notifications.campaign.adobe.com"`.

## Améliorations de mai 2023 {#may-2023}

**Délégation des certificats SSL des sous-domaines à Adobe**

Vous pouvez désormais laisser Adobe gérer les certificats SSL de vos sous-domaines. Si vous utilisez des CNAME pour configurer votre sous-domaine, les enregistrements de certificats seront automatiquement générés et fournis afin de générer un certificat dans votre solution d’hébergement de domaine.

Notez que cette fonctionnalité n’est disponible que lors de la configuration d’un nouveau sous-domaine. Vous ne pouvez pas déléguer de certificats pour les sous-domaines délégués existants. [En savoir plus](../subdomains-certificates/using/setting-up-new-subdomain.md)

>[!NOTE]
>
>Le protocole SSL géré par Adobe est une fonctionnalité gratuite.

## Mars 2023 {#march-2023}

**Suppression de la délégation de sous-domaines pour les CNAME**

Vous pouvez désormais supprimer la délégation des sous-domaines configurés à l’aide de CNAME. [En savoir plus](../subdomains-certificates/using/remove-delegated-subdomains.md)

## Février 2023 {#february-2023}

**Suppression de la délégation pour les sous-domaines délégués à Adobe**

Vous pouvez maintenant supprimer la délégation d’un sous-domaine entièrement délégué à Adobe. [En savoir plus](../subdomains-certificates/using/remove-delegated-subdomains.md)

>[!NOTE]
>
>La suppression de la délégation n’est actuellement pas disponible pour les sous-domaines qui ont été configurés à l’aide de CNAME.

**Calendrier de service**

Le calendrier de service fournit maintenant une vue Calendrier pour suivre les événements importants qui se produisent sur vos instances. Des informations ont également été ajoutées dans les notifications envoyées aux utilisateurs et utilisatrices abonnés aux alertes du panneau de contrôle. [En savoir plus](../service-events/service-events.md)

![](assets/do-not-localize/gif-calendar.gif)

## Janvier 2023 {#january-2023}

**Nouvelle fonctionnalité de modèle d’hébergement hybride**

Les clientes et clients disposant d’un modèle d’hébergement hybride peuvent désormais ajouter des adresses IP à la liste autorisée pour accéder aux instances MID. [En savoir plus](../instances-settings/using/ip-allow-listing-instance-access.md)

**Amélioration de la demande de signature de certificat (CSR)**

Le champ Ville/Localité est désormais facultatif pendant la génération de la demande de signature de certificat.
