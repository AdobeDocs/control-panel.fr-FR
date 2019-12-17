---
title: Marque des sous-domaines
description: En savoir plus sur la marque des sous-domaines
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Marque des sous-domaines {#subdomains-branding}

## Pourquoi configurer des sous-domaines ? {#why-setting-up-subdomains}

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler vos marques, ou divers types de trafic (messages transactionnels, informations marketing, etc.).

Prenons l&#39;exemple du domaine &quot;mybrand.com&quot;, qui est utilisé pour envoyer des communications transactionnelles et marketing. Dans ce cas, vous pouvez décider de configurer deux sous-domaines :

* sous-domaine &quot;info.mybrand.com&quot; pour vos communications transactionnelles (confirmation des achats, réinitialisation du mot de passe, etc.),
* Sous-domaine &quot;marketing.mybrand.com&quot; pour vos courriers électroniques de prospection.

Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si les sous-domaines &quot;marketing.mybrand.com&quot; étaient placés sur liste noire par les fournisseurs de services Internet en raison d’une mauvaise délivrabilité, cela empêcherait la liste noire de l’ensemble du domaine &quot;mybrand.com&quot; et du sous-domaine &quot;info.mybrand.com&quot;.

## Méthodes de délégation de sous-domaine {#subdomain-delegation-methods}

La délégation de sous-domaine vous permet de déléguer une sous-section de votre domaine (techniquement une &quot;zone DNS&quot;) pour une utilisation avec Adobe Campaign. Les méthodes de configuration disponibles sont les suivantes :

* **Délégation complète de sous-domaine à Adobe Campaign** (recommandé) : Le sous-domaine est entièrement délégué à Adobe. Adobe est en mesure de fournir la campagne en tant que service géré en contrôlant et en gérant tous les aspects du DNS requis pour la diffusion, le rendu et le suivi des campagnes par courrier électronique.

* **Utilisation de CNAME** (non recommandé et non pris en charge par le Panneau de configuration) : Créez un sous-domaine et utilisez des CNAME pour pointer vers des enregistrements spécifiques à Adobe. Grâce à cette configuration, Adobe et le client partagent la responsabilité de la maintenance du DNS.

Le tableau ci-dessous résume le fonctionnement de ces méthodes, ainsi que le niveau d’effort implicite :

| Méthode de délégation | Fonctionnement | Niveau d&#39;effort |
|---|---|---|
| **Délégation complète** | Créez l’enregistrement du sous-domaine et de l’espace de noms. Adobe configurera alors tous les enregistrements DNS requis pour Adobe Campaign.<br/><br/>Dans cette configuration, Adobe est entièrement responsable de la gestion du sous-domaine et de tous les enregistrements DNS. | Faible |
| **CNAME, méthode personnalisée** | Créez l’enregistrement du sous-domaine et de l’espace de noms. Adobe fournira alors les enregistrements à placer dans vos serveurs DNS et configurera les valeurs correspondantes dans les serveurs DNS Adobe Campaign.<br/><br/>Dans cette configuration, vous et Adobe partagez la responsabilité de la maintenance du DNS. | Elevée |

Des informations supplémentaires sur la délégation de domaines sont disponibles[dans cette documentation](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
