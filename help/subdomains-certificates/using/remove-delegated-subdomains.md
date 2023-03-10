---
product: campaign
solution: Campaign
title: Supprimer la délégation des sous-domaines
description: Découvrez comment supprimer la délégation des sous-domaines à Adobe.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 349eb8778a19263b83b70b8c920c401aff7fa24a
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 100%

---

# Supprimer la délégation de sous-domaines à Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Supprimer la délégation de sous-domaine"
>abstract="Cet écran vous permet de supprimer la délégation d’un sous-domaine à Adobe. Notez que ce processus ne peut pas être annulé et qu’il est irréversible tant que son exécution n’est pas terminée.<br><br>Si vous essayez de supprimer la délégation d’un domaine principal de l’instance sélectionnée, il vous sera demandé de choisir le domaine qui le remplacera."

Le panneau de contrôle vous permet de supprimer la délégation d’un sous-domaine qui a été délégué à Adobe.

>[!NOTE]
>
>La suppression de la délégation n’est actuellement pas disponible pour les sous-domaines qui ont été configurés à l’aide de CNAME.

## Remarques importantes {#important}

Avant de poursuivre, examinez attentivement les impacts qui se produisent une fois le processus de suppression déclenché :

* Une fois le processus déclenché, la suppression de la délégation de sous-domaine ne peut plus être annulée et est irréversible tant que l’exécution du processus n’est pas terminée.
* Aucune autre délégation de sous-domaine ne peut être supprimée lorsqu’un processus similaire sur un autre sous-domaine est en cours.
* Une délégation supprimée sur un sous-domaine ne peut pas être déléguée à nouveau dans les 3 jours suivant sa suppression.

## Supprimer la délégation d’un sous-domaine {#steps}

Pour supprimer la délégation d’un sous-domaine à Adobe, procédez comme suit :

1. Cliquez sur le bouton représentant des points de suspension en regard de la délégation de domaine à supprimer, puis sélectionnez **[!UICONTROL Supprimer le sous-domaine délégué]**.

   ![](assets/undelegate-subdomain.png)

1. Consultez la clause d’exclusion de responsabilité et reconnaissez la suppression de la délégation de domaine à Adobe.

1. Consultez les informations concernant l’instance à laquelle le sous-domaine est associé, y compris les affinités IP associées et les configurations de marque.

   Si vous supprimez la délégation du domaine principal pour l’instance sélectionnée, vous devez choisir le domaine qui le remplacera à l’aide de la liste **[!UICONTROL Domaine de remplacement]**.

   Cliquez sur **[!UICONTROL Suivant]** pour procéder à la suppression.

   ![](assets/undelegate-subdomain-details.png)

1. Examinez le résumé qui s’affiche. Pour confirmer la suppression, saisissez l’URL du domaine pour lequel vous souhaitez supprimer la délégation, puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](assets/undelegate-submit.png)

Une fois la suppression de la délégation initiée, le traitement en attente s’affiche dans les logs de traitements jusqu’à ce qu’il soit terminé.

![](assets/undelegate-job.png)

## Codes d’erreur {#FAQ}

Cette section répertorie les messages d’erreur que vous pouvez rencontrer lors de la tentative de suppression de la délégation d’un sous-domaine :

| Code d’erreur | Message | Description |
|  ---  |  ---  |  ---  |
| 8002 | Impossible de supprimer le domaine délégué demandé en raison d’une demande similaire en cours. Réessayez dans 3 jours | Un traitement de suppression de délégation de sous-domaine est déjà en cours pour l’instance sélectionnée. Patientez 3 jours pour lancer un nouveau traitement de suppression. |
| 8003 | La suppression du domaine délégué demandé n’est pas prise en charge pour cette instance. | La suppression de la délégation n’est pas prise en charge pour le sous-domaine sélectionné en raison d’un problème technique. Contactez l’assistance clientèle. |
| 8004 | La suppression du domaine délégué demandé n’est pas autorisée, car il n’y a qu’un seul domaine dans cette instance. | Un seul sous-domaine a été délégué pour l’instance sélectionnée. La suppression de la délégation n’est pas autorisée. |
| 8005 | La suppression du domaine délégué demandé n’est pas prise en charge pour cette configuration. | La suppression de la délégation n’est pas prise en charge pour le sous-domaine sélectionné en raison d’un problème technique. Contactez l’assistance clientèle. |
| 8006 | La suppression du domaine délégué demandé n’est pas autorisée pour des raisons inconnues. Veuillez contacter l’assistance clientèle. | La suppression de la délégation n’est pas prise en charge pour l’instance sélectionnée en raison de problèmes inconnus, contactez l’assistance clientèle. |
