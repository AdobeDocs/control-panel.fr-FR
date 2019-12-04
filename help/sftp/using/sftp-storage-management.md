---
title: Gestion de l'espace de stockage SFTP
description: Découvrez comment surveiller et gérer le stockage de votre serveur SFTP
translation-type: tm+mt
source-git-commit: 111c8fd461f6f1c567288acd7a83aee5ef7fce97

---


# Gestion de l'espace de stockage SFTP {#sftp-storage-management}

En fonction des modalités de votre contrat, les capacités de stockage de votre serveur SFTP peuvent varier.

Il est essentiel que vous surveilliez régulièrement l'espace disponible pour chacun de vos serveurs SFTP. Sinon, vous risquez de ne plus pouvoir enregistrer de fichiers supplémentaires sur le serveur ou d'exécuter avec succès les workflows qui dépendent des mises à jour de ce serveur.

**Rubriques connexes :**

* [Tutoriel vidéo sur Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/managing-sftp-servers.html)
* [Tutoriel vidéo sur Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Accès aux informations relatives à la capacité de stockage {#accessing-storage-capacity-information}

La section **[!UICONTROL Serveurs SFTP les plus utilisés]dans l'en-tête inclut les trois serveurs les plus utilisés attachés aux instances auxquelles vous avez accès en tant qu'administrateur.** Ces informations sont disponibles dans chaque onglet de la vignette SFTP.

![](assets/control_panel_topspaceNEW.png)

Information about the space used by all instances you have access to is available in the **[!UICONTROL Storage]** tab of the SFTP card. Elles sont mises à jour à chaque actualisation de la page.

![](assets/control_panel_spaceNEW.png)

Pour chaque cas, une alerte visuelle vous permet de savoir quand son stockage dépasse sa capacité :

* **Orange**: l'instance a dépassé 80 % de sa capacité,
* **Rouge**: l’instance dépasse 90 % de sa capacité.

D'autres conseils permettent de savoir comment procéder si votre serveur arrive à saturation.

## Bonnes pratiques lorsque la capacité de stockage est épuisée {#best-practices-when-capacity-runs-out}

1. **Nettoyez le serveur SFTP en supprimant des fichiers anciens ou inutiles**. Pour plus d'informations sur l'accès à votre dossier de serveur SFTP, reportez-vous à [cette section](../../sftp/using/logging-into-sftp-server.md).
1. Vérifiez que les **workflows** qui nettoient vos serveurs SFTP s'exécutent correctement. For more on technical workflows in Adobe Campaign, refer to the dedicated [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) and [Campaign Standard](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html) documentations.
1. Contactez votre équipe de compte pour **demander plus d'espace de stockage** (des frais supplémentaires peuvent s'appliquer).
1. Contactez le **service à la clientèle** si vous pensez qu’il y a un problème.
