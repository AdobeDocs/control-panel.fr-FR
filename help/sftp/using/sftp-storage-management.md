---
title: Gestion de l’espace de stockage SFTP
description: Découvrez comment surveiller et gérer l’espace de stockage de votre serveur SFTP
translation-type: ht
source-git-commit: 834adb7c937a9927901f91e257a8df44e72ca45b

---


# Gestion de l’espace de stockage SFTP {#sftp-storage-management}

>[!CONTEXTUALHELP]
>id="cp_storage"
>title="À propos de la capacité de stockage"
>abstract="Dans cet onglet, vous pouvez afficher les informations sur la capacité de stockage et l’utilisation des serveurs SFTP. Seuls les serveurs SFTP auxquels vous avez accès sont visibles ici. Contactez l’administrateur pour demander un accès aux autres serveurs SFTP."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4" text="Regarder une vidéo de démonstration"

En fonction des modalités de votre contrat, les capacités de stockage de votre serveur SFTP peuvent varier.

Il est essentiel que vous surveilliez régulièrement l’espace disponible pour chacun de vos serveurs SFTP. Sinon, vous risquez de ne plus pouvoir enregistrer de fichiers supplémentaires sur le serveur ou d’exécuter avec succès les workflows qui dépendent des mises à jour de ce serveur.

**Rubriques connexes :**

* [Tutoriel vidéo sur Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/monitoring-server-capacity-whitelisting-adding-ssh-key.html)
* [Tutoriel vidéo sur Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Accès aux informations relatives à la capacité de stockage {#accessing-storage-capacity-information}

Les informations sur l’espace utilisé par toutes les instances auxquelles vous avez accès sont disponibles dans l’onglet **[!UICONTROL Stockage]** de la carte SFTP. Elles sont mises à jour à chaque actualisation de la page.

![](assets/control_panel_space.png)

Pour chaque instance, une alerte visuelle vous indique quand le stockage dépasse la capacité :

* **Orange** : l’instance dépasse 80 % de sa capacité.
* **Rouge** : l’instance dépasse 90 % de sa capacité.

D’autres conseils permettent de savoir comment procéder si votre serveur arrive à saturation.

## Bonnes pratiques lorsque la capacité de stockage est épuisée {#best-practices-when-capacity-runs-out}

1. **Nettoyez le serveur SFTP en supprimant des fichiers anciens ou inutiles**. Pour plus d’informations sur l’accès à votre dossier de serveur SFTP, reportez-vous à [cette section](../../sftp/using/logging-into-sftp-server.md).
1. Vérifiez que les **workflows** qui nettoient vos serveurs SFTP s’exécutent correctement. Pour plus d’informations sur les workflows techniques dans Adobe Campaign, reportez-vous aux documentations dédiées [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) et [Campaign Standard](https://helpx.adobe.com/fr/campaign/standard/administration/using/technical-workflows.html).
1. Contactez l’équipe de votre compte pour **demander plus d’espace de stockage** (des frais supplémentaires peuvent s’appliquer).
1. Contactez l’**Assistance clientèle** si vous pensez qu’il y a un problème.
