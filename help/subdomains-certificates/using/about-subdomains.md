---
title: A propos des sous-domaines
description: En savoir plus sur les sous-domaines
translation-type: tm+mt
source-git-commit: c2ef995d49118943bdd77e6d3c14ef7ec643e672

---


# A propos du sous-domaine {#about-subdomains}

## Pourquoi configurer des sous-domaines ? {#why-setting-up-subdomains}

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler divers types de trafic (entreprise, informations marketing, etc.).

Prenons l&#39;exemple du domaine &quot;mybrand.com&quot;, utilisé pour envoyer des communications à la fois informatives et marketing :

* info.mybrand.com pour vos communications internes
* marketing.mybrand.com pour vos courriers électroniques de prospection.

Dans ce cas, vous pouvez décider de déléguer le sous-domaine &quot;marketing.mybrand.com&quot; à Adobe Campaign. Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si les sous-domaines &quot;marketing.mybrand.com&quot; étaient placés sur liste noire par les fournisseurs de services Internet en raison d’une mauvaise délivrabilité, cela empêcherait le blocage de l’ensemble des domaines &quot;mybrand.com&quot; et &quot;info.mybrand.com&quot;.

## Méthodes de délégation de sous-domaine {#subdomain-delegation-methods}

La délégation de sous-domaine vous permet de déléguer une sous-section de votre domaine (techniquement une &quot;zone DNS&quot;) pour une utilisation avec Adobe Campaign. Les méthodes de configuration disponibles sont les suivantes :

* **Délégation de sous-domaine complète vers Adobe Campaign** (recommandé)

   Le sous-domaine est entièrement délégué à Adobe. Adobe est en mesure de fournir la campagne en tant que service géré en contrôlant et en gérant tous les aspects du DNS requis pour la diffusion, le rendu et le suivi des campagnes par courrier électronique.

* **Utilisation de CNAME** (non recommandé et non pris en charge par le Panneau de configuration) :

   Créez un sous-domaine et utilisez des CNAME pour pointer vers des enregistrements spécifiques à Adobe. Grâce à cette configuration, Adobe et le client partagent la responsabilité de la maintenance du DNS.

Pour plus d&#39;informations sur chacune de ces méthodes (responsabilité implicite, exigences, etc.), consultez [cette documentation](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
