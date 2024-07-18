---
title: Dernière version
description: Cette page répertorie toutes les nouvelles fonctionnalités et améliorations apportées au Panneau de contrôle.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 100%

---

# Dernière version {#control-panel-releases}

Cette page répertorie les nouvelles fonctionnalités et améliorations apportées au Panneau de contrôle.

## Octobre 2023 {#october-2023}

**Interface utilisateur**

* Le panneau de contrôle est désormais disponible dans d’autres langues. [En savoir plus](../discover/using/discovering-the-interface.md#supported-languages-languages)

**Surveillance des profils actifs**

* Vous pouvez désormais surveiller le nombre de profils actifs auxquels vous avez droit et le nombre total de profils utilisés dans votre organisation dans toutes les instances, si vous utilisez plusieurs instances. [En savoir plus](../performance-monitoring/using/active-profiles-monitoring.md)

**Enregistrements DMARC**

* Plusieurs adresses e-mail peuvent désormais recevoir des e-mails de rapport agrégé et de rapport d’échec. [En savoir plus](../subdomains-certificates/using/dmarc.md)
* Des modifications ont été apportées si des enregistrements DMARC et BIMI existent pour un sous-domaine :

   * Les enregistrements DMARC ne peuvent pas être supprimés. Si vous souhaitez en supprimer un, vous devez d’abord supprimer l’enregistrement BIMI.
   * Les enregistrements DMARC peuvent être modifiés, mais la rétrogradation de la règle vers « Aucun » n’est pas autorisée et sa valeur en pourcentage doit être de 100.

