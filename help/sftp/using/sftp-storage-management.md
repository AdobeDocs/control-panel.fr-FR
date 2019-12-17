---
title: Gestion de l’espace de stockage SFTP
description: Découvrez comment surveiller et gérer l’espace de stockage de votre serveur SFTP
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Gestion de l’espace de stockage SFTP {#sftp-storage-management}

En fonction des modalités de votre contrat, les capacités de stockage de votre serveur SFTP peuvent varier.

Il est essentiel que vous surveilliez régulièrement l’espace disponible pour chacun de vos serveurs SFTP. Sinon, vous risquez de ne plus pouvoir enregistrer de fichiers supplémentaires sur le serveur ou d’exécuter avec succès les workflows qui dépendent des mises à jour de ce serveur.

**Rubriques connexes :**

* [Tutoriel vidéo sur Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/monitoring-server-capacity-whitelisting-adding-ssh-key.html)
* [Tutoriel vidéo sur Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Accès aux informations relatives à la capacité de stockage {#accessing-storage-capacity-information}

La section **[!UICONTROL Capacité du disque SFTP la plus utilisée]**dans l’en-tête inclut les trois serveurs les plus utilisés attachés aux instances auxquelles vous avez accès en tant qu’administrateur. Ces informations sont disponibles dans chaque onglet de la carte SFTP.

![](assets/control_panel_topspace.png)

Les informations sur l’espace utilisé par toutes les instances auxquelles vous avez accès sont disponibles dans l’onglet **[!UICONTROL Stockage]**de la carte SFTP. Elles sont mises à jour à chaque actualisation de la page.

![](assets/control_panel_space.png)

Pour chaque instance, une alerte visuelle vous indique quand le stockage dépasse la capacité :

* **Orange** : l’instance dépasse 80 % de sa capacité.
* **Rouge** : l’instance dépasse 90 % de sa capacité.

D’autres conseils permettent de savoir comment procéder si votre serveur arrive à saturation.

## Bonnes pratiques lorsque la capacité de stockage est épuisée {#best-practices-when-capacity-runs-out}

1. **Nettoyez le serveur SFTP en supprimant des fichiers anciens ou inutiles**. Pour plus d’informations sur l’accès à votre dossier de serveur SFTP, reportez-vous à [cette section](../../sftp/using/logging-into-sftp-server.md).
1. Vérifiez que les **workflows** qui nettoient vos serveurs SFTP s’exécutent correctement. Pour plus d’informations sur les workflows techniques dans Adobe Campaign, reportez-vous aux documentations dédiées [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) et [Campaign Standard](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html).
1. Contactez l’équipe de votre compte pour **demander plus d’espace de stockage** (des frais supplémentaires peuvent s’appliquer).
1. Contactez l’**Assistance clientèle** si vous pensez qu’il y a un problème.
