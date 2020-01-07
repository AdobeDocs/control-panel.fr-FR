---
title: Marque des sous-domaines
description: En savoir plus sur la marque des sous-domaines
translation-type: tm+mt
source-git-commit: c44f6800a0f7905fe9e5619388c7007f0af8f973

---


# Marque des sous-domaines {#subdomains-branding}

>[!IMPORTANT]
>
>La délégation de sous-domaines du Panneau de configuration sera disponible en version bêta d&#39;ici la fin janvier et sujette à de fréquentes mises à jour et modifications sans préavis.

## Pourquoi configurer des sous-domaines ? {#why-setting-up-subdomains}

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler vos marques ou divers types de trafic (messages transactionnels, informations marketing, etc.).

Prenons l&#39;exemple du domaine « mybrand.com », utilisé pour envoyer des communications transactionnelles et marketing. Dans ce cas, vous pouvez décider de configurer deux sous-domaines :

* le sous-domaine « info.mybrand.com » pour vos communications transactionnelles (confirmation des achats, réinitialisation de mots de passe, etc.),
* Et le sous-domaine « marketing.mybrand.com » pour vos e-mails de prospection.

Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si le sous-domaine « marketing.mybrand.com » se retrouvait classé sur liste noire par les fournisseurs de services Internet en raison d’une mauvaise délivrabilité, cela empêcherait le domaine « mybrand.com » entier et le sous-domaine « info.mybrand.com » d’être placés sur liste noire.

## Méthodes de délégation de sous-domaine {#subdomain-delegation-methods}

La délégation de sous-domaine vous permet de déléguer une sous-section de votre domaine (techniquement, une « zone DNS ») à utiliser avec Adobe Campaign. Les méthodes de configuration disponibles sont les suivantes :

* **Délégation complète de sous-domaine à Adobe Campaign** (recommandée) : le sous-domaine est entièrement délégué à Adobe. Adobe est en mesure de fournir la campagne en tant que service géré en contrôlant et en gérant tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des campagnes par e-mail.

* **Utilisation de CNAME** (non recommandée et non prise en charge via le Panneau de contrôle) : créez un sous-domaine et utilisez des CNAME pour pointer vers des enregistrements spécifiques à Adobe. Grâce à cette configuration, Adobe et le client partagent la responsabilité de la maintenance du DNS.

Le tableau ci-dessous résume le fonctionnement de ces méthodes, ainsi que le niveau d’effort impliqué :

| Méthode de délégation | Fonctionnement | Niveau d&#39;effort |
|---|---|---|
| **Délégation complète** | Créez l’enregistrement du sous-domaine et de l’espace de nommage. Adobe configurera alors tous les enregistrements DNS nécessaires à Adobe Campaign.<br/><br/>Dans cette configuration, Adobe est entièrement responsable de la gestion du sous-domaine et de tous les enregistrements DNS. | Faible |
| **CNAME, méthode personnalisée** | Créez l’enregistrement du sous-domaine et de l’espace de nommage. Adobe fournira alors les enregistrements à placer sur vos serveurs DNS et configurera les valeurs correspondantes sur les serveurs DNS Adobe Campaign.<br/><br/>Dans cette configuration, vous partagez avec Adobe la responsabilité de la maintenance du DNS. | Élevée |

Des informations supplémentaires sur la délégation de domaine sont disponibles [dans cette documentation](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

Si vous avez des questions sur les méthodes de délégation de sous-domaines, contactez l’équipe de délivrabilité d’Adobe ou contactez le service à la clientèle pour demander des conseils sur la délivrabilité.
