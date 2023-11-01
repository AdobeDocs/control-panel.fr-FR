---
product: campaign
solution: Campaign
title: Marque des sous-domaines
description: En savoir plus sur la marque des sous-domaines
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Intermediate
exl-id: a489d051-fb95-45cf-bb6d-33aef10b7795
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 100%

---

# Marque des sous-domaines {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="À propos des sous-domaines et des certificats SSL"
>abstract="Surveillez vos sous-domaines et les certificats SSL associés."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=fr" text="Surveillance des certificats SSL"

## Pourquoi configurer des sous-domaines ?  {#why-setting-up-subdomains}

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler vos marques ou divers types de trafic (messages transactionnels, informations marketing, etc.).

Prenons l&#39;exemple du domaine « mybrand.com », utilisé pour envoyer des communications transactionnelles et marketing. Dans ce cas, vous pouvez décider de configurer deux sous-domaines :

* le sous-domaine « info.mybrand.com » pour vos communications transactionnelles (confirmation des achats, réinitialisation de mots de passe, etc.),
* et le sous-domaine « marketing.mybrand.com » pour vos emails de prospection.

Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si les sous-domaines « marketing.mybrand.com » se retrouvaient ajoutés à la liste bloquée par les fournisseurs de services Internet en raison d’une mauvaise délivrabilité, cela empêcherait le domaine « mybrand.com » entier et le sous-domaine « info.mybrand.com » d’être ajoutés à la liste bloquée.

## Méthodes de configuration de sous-domaine {#subdomain-delegation-methods}

La configuration de sous-domaine vous permet de configurer une sous-section de votre domaine (techniquement, une « zone DNS ») à utiliser avec Adobe Campaign. Les méthodes de configuration disponibles sont les suivantes :

* **Délégation complète de sous-domaine à Adobe Campaign** (recommandée) : le sous-domaine est entièrement délégué à Adobe. Adobe est en mesure de fournir la campagne en tant que service géré en contrôlant et en gérant tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des campagnes par e-mail.

* **Utilisation de CNAME** : créez un sous-domaine et utilisez des CNAME pour pointer vers des enregistrements spécifiques à Adobe. Grâce à cette configuration, Adobe et le client partagent la responsabilité de la maintenance du DNS.

Le tableau ci-dessous résume le fonctionnement de ces méthodes, ainsi que le niveau d’effort impliqué :

| Méthode de configuration | Fonctionnement | Niveau d&#39;effort |
|---|---|---|
| **Délégation complète** | Créez l’enregistrement du sous-domaine et de l’espace de noms. Adobe configurera alors tous les enregistrements DNS nécessaires à Adobe Campaign.<br/><br/>Dans cette configuration, Adobe est entièrement responsable de la gestion du sous-domaine et de tous les enregistrements DNS. | Faible |
| **CNAME, méthode personnalisée** | Créez l’enregistrement du sous-domaine et de l’espace de noms. Adobe fournira alors les enregistrements à placer sur vos serveurs DNS et configurera les valeurs correspondantes sur les serveurs DNS Adobe Campaign.<br/><br/>Dans cette configuration, vous partagez avec Adobe la responsabilité de la maintenance du DNS. | Élevée |

Des informations supplémentaires sur la configuration de domaine sont disponibles dans [cette documentation](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=fr).

Si vous avez des questions concernant les méthodes de configuration de sous-domaine, contactez l’équipe chargée de la délivrabilité d’Adobe ou l’assistance clientèle pour obtenir des conseils sur la délivrabilité.

## Cas d’utilisation des sous-domaines (Campaign v7/v8){#subdomains-use-cases}

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_usecase_selection"
>title="Sélection du cas dʼutilisation de votre sous-domaine"
>abstract="La ventilation de vos sous-domaines selon les cas dʼutilisation est une bonne pratique en matière de délivrabilité. Elle permet dʼisoler et de protéger la réputation de chaque sous-domaine."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=fr" text="Configuration dʼun nouveau sous-domaine"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=fr" text="Marque des sous-domaines"

Lors de la configuration de sous-domaines pour les instances Campaign v7/v8, vous devez sélectionner le cas d’utilisation pour lequel le sous-domaine sera utilisé (consultez la section [Configurer un nouveau sous-domaine](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

Les cas d’utilisation possibles sont les suivants :

* **Communications marketing** : communications destinées à un usage commercial. Exemple : campagne par e-mail de vente.

* **Communications transactionnelles et opérationnelles** : les communications transactionnelles contiennent des informations visant à terminer un processus que le destinataire a commencé avec vous. Exemple : confirmation d’achat, email de réinitialisation de mot de passe. Les communications organisationnelles se rapportent à l’échange d’informations, d’idées et d’opinions au sein et à l’extérieur de l’organisation, sans but commercial.

**La ventilation de vos sous-domaines selon les cas d’utilisation est une bonne pratique en matière de délivrabilité**. Elle permet d’isoler et de protéger la réputation de chaque sous-domaine. Par exemple, si votre sous-domaine de communications marketing est ajouté à la liste bloquée par les fournisseurs de services Internet, votre sous-domaine de communications transactionnelles ne sera pas affecté et pourra encore envoyer des communications.

**Vous pouvez configurer un sous-domaine pour les cas d’utilisation Marketing et Transactionnel** :

* Pour les cas d’utilisation Marketing, les sous-domaines seront configurés sur les instances **MID** (Mid-sourcing).
* Pour les cas d’utilisation Transactionnel, les sous-domaines seront configurés sur TOUTES les instances **RT** (Message Center/Real-time messaging) pour garantir la connectivité. Les sous-domaines fonctionneront donc avec toutes vos instances RT.

>[!NOTE]
>
>Si vous utilisez Campaign v7/v8, le Panneau de contrôle vous permet de voir les instances RT/MID connectées à l’instance Marketing que vous utilisez. Pour plus dʼinformations, consultez la section [Détails de l’instance](../../instances-settings/using/instance-details.md).

**Rubriques connexes :**

* [Configuration d’un nouveau sous-domaine](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Surveillance de vos sous-domaines](../../subdomains-certificates/using/monitoring-subdomains.md)
