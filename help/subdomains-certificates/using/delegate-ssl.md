---
product: campaign
solution: Campaign
title: Déléguer des certificats SSL de sous-domaines à Adobe
description: Découvrez comment déléguer les certificats SSL de vos sous-domaines à Adobe.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a2b3d409-704b-4e81-ae40-b734f755b598
source-git-commit: 31d181770474428a7b42e96f2e603cc820db48d4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 61%

---

# Déléguer des certificats SSL de sous-domaines à Adobe {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="Déléguer des certificats SSL de sous-domaines à Adobe"
>abstract="Le panneau de contrôle vous permet de laisser Adobe gérer les certificats SSL de vos sous-domaines. Si vous utilisez des CNAME pour configurer votre sous-domaine, les enregistrements de certificats seront automatiquement générés et fournis afin de générer un certificat dans votre solution d’hébergement de domaine."

Il est vivement recommandé de déléguer la gestion des certificats SSL de vos sous-domaines à Adobe, car Adobe crée automatiquement le certificat et le renouvelle tous les ans avant l’expiration de ce dernier.

Si vous utilisez des CNAME pour configurer une délégation de sous-domaine, Adobe fournira des enregistrements de certificat à utiliser dans votre solution d’hébergement de domaine pour générer votre certificat.

La délégation des certificats SSL à Adobe peut être effectuée lors de la configuration d’un nouveau sous-domaine ou pour des sous-domaines déjà délégués.

>[!NOTE]
>
>Le protocole SSL géré par Adobe est une fonctionnalité gratuite. La délégation du certificat d’un sous-domaine à Adobe est transparente et n’a aucun impact sur vos campagnes et sur la délivrabilité. [En savoir plus sur la gestion des certificats SSL](monitoring-ssl-certificates.md#management)


## Déléguer les certificats SSL des nouveaux sous-domaines {#new}

Pour déléguer des certificats SSL lors de la configuration d’un nouveau sous-domaine, activez l’option **[!UICONTROL Choisir le protocole SSL géré par Adobe pour les sous-domaines]** de l’assistant de configuration de sous-domaine. Le processus de génération de certificat diffère en fonction de la méthode de délégation de sous-domaine :

* **Délégation complète de sous-domaine** : le certificat SSL est automatiquement demandé et installé par Adobe sans aucune action de votre part. Une fois que vous avez envoyé la configuration de sous-domaine, la demande d’installation du certificat est traitée immédiatement dans le cadre du workflow de configuration de sous-domaine. [En savoir plus sur la délégation complète de sous-domaine](setting-up-new-subdomain.md#full-subdomain-delegation)

* **Délégation CNAME** : les enregistrements de certificat à copier dans votre solution d’hébergement seront fournis ultérieurement dans l’assistant de configuration. Vous devez générer ces enregistrements de certificat dans votre solution d’hébergement de domaine avant d’envoyer la configuration de sous-domaine. [En savoir plus sur la délégation CNAME](setting-up-new-subdomain.md#use-cnames)

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## Déléguer des certificats SSL pour les sous-domaines déjà délégués {#delegated}

Pour déléguer des certificats SSL pour un sous-domaine déjà délégué, cliquez sur le bouton représentant des points de suspension en regard du sous-domaine souhaité, puis cliquez sur **[!UICONTROL Basculer vers le protocole SSL géré]**.

![](assets/delegate-ssl-list.png){width="70%" align="left"}

Le processus de génération du certificat dépend de la configuration initiale du sous-domaine :

### Sous-domaines entièrement délégués

Pour les sous-domaines configurés à l’aide de la délégation complète de sous-domaines (avec les serveurs de noms Adobe), le certificat SSL est automatiquement demandé et installé par Adobe. Une fois que vous avez cliqué sur **[!UICONTROL Basculer vers le SSL géré]** et confirmé, la demande d’installation du certificat est envoyée immédiatement, sans nécessiter aucune action supplémentaire de votre part.

### Sous-domaines délégués CNAME

Pour les sous-domaines configurés à l’aide de la délégation CNAME, une boîte de dialogue s’affiche avec les enregistrements de certificat qui ont été automatiquement générés par Adobe. Copiez ces enregistrements un par un ou en téléchargeant un fichier CSV, puis accédez à votre solution d’hébergement de domaine pour générer le certificat correspondant.

Assurez-vous que tous les enregistrements des certificats ont été générés dans votre solution d’hébergement de domaine. Si tout est correctement configuré, confirmez la création des enregistrements puis cliquez sur **[!UICONTROL Envoyer]**.

![](assets/delegate-ssl.png){width="70%" align="left"}
