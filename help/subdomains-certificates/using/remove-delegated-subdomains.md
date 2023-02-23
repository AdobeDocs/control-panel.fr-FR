---
product: campaign
solution: Campaign
title: Suppression de la délégation de sous-domaines
description: Découvrez comment supprimer la délégation de sous-domaines à Adobe.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 5a8c4c4d1c5c527135901cd41f2b0936af8737b4
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 2%

---

# Suppression de la délégation de sous-domaines à Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Suppression de la délégation de sous-domaine"
>abstract="Cet écran vous permet de supprimer la délégation d’un sous-domaine à Adobe. Gardez à l’esprit que ce processus ne peut pas être annulé ou arrêté une fois envoyé.<br><br>Si vous essayez de supprimer la délégation d’un domaine Principal pour l’instance sélectionnée, vous serez invité à choisir le domaine qui le remplacera."

Panneau de Contrôle vous permet de supprimer la délégation d’un sous-domaine qui a été délégué à l’Adobe, y compris la configuration CNAME.

## Remarques importantes {#important}

Avant de poursuivre, examinez attentivement les impacts qui se produisent une fois le processus de suppression déclenché :

* La suppression de la délégation de sous-domaine ne peut pas être annulée et sera irréversible une fois démarrée jusqu’à ce que l’exécution du processus soit en cours.
* Aucune autre délégation de sous-domaine ne peut être supprimée lorsqu’un processus similaire sur un autre sous-domaine est en cours.
* Une délégation supprimée sur un sous-domaine ne peut pas être déléguée à nouveau avant 3 jours de sa suppression.

## Suppression d’une délégation de sous-domaine {#steps}

Pour supprimer la délégation d’un sous-domaine à Adobe, procédez comme suit :

1. Cliquez sur le bouton représentant des points de suspension en regard de la délégation de domaine à supprimer, puis sélectionnez **[!UICONTROL Supprimer le sous-domaine délégué]**.

   ![](assets/undelegate-subdomain.png)

1. Examinez la clause de non-responsabilité et reconnaissez la suppression de la délégation de domaine à Adobe.

1. Consultez les informations concernant l’instance à laquelle le sous-domaine est associé, y compris les affinités IP associées et les configurations de marque.

   Si vous supprimez la délégation du domaine Principal pour l’instance sélectionnée, vous devez choisir le domaine qui le remplacera à l’aide de la propriété **[!UICONTROL Domaine de remplacement]** liste.

   Cliquez sur **[!UICONTROL Suivant]** pour procéder à la suppression.

   ![](assets/undelegate-subdomain-details.png)

1. Examinez le résumé qui s’affiche. Pour confirmer la suppression, saisissez l’URL du domaine pour lequel vous souhaitez supprimer la délégation, puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](assets/undelegate-submit.png)

Une fois la suppression de la délégation commencée, la tâche en attente s’affiche dans les journaux de la tâche jusqu’à ce qu’elle soit terminée.

![](assets/undelegate-job.png)

## Codes d’erreur {#FAQ}

Cette section répertorie les messages d’erreur que vous pouvez rencontrer lors de la tentative de suppression de la délégation d’un sous-domaine :

| Code erreur | Message | Description |
|  ---  |  ---  |  ---  |
| 8002 | La suppression du domaine délégué demandé ne peut pas être traitée, car une demande similaire se chevauche en cours. Veuillez réessayer après 3 jours | Une tâche de suppression de délégation de sous-domaine est déjà en cours de traitement pour l’instance sélectionnée. Patientez jusqu’à 3 jours pour lancer une nouvelle tâche de suppression. |
| 8003 | La suppression du domaine délégué demandé n’est pas prise en charge pour cette instance. | La suppression de la délégation n’est pas prise en charge pour le sous-domaine sélectionné en raison d’un problème technique. Contactez l’assistance clientèle. |
| 8004 | La suppression du domaine délégué demandé n’est pas autorisée, car il n’y a qu’un seul domaine dans cette instance. | Un seul sous-domaine a été délégué pour l’instance sélectionnée. La suppression de la délégation n’est pas autorisée. |
| 8005 | La suppression du domaine délégué demandé n’est pas prise en charge pour cette configuration. | La suppression de la délégation n’est pas prise en charge pour le sous-domaine sélectionné en raison d’un problème technique. Contactez l’assistance clientèle. |
| 8006 | La suppression du domaine délégué demandé n’est pas autorisée pour des raisons inconnues. Veuillez contacter l’assistance clientèle. | La suppression de la délégation n’est pas prise en charge pour l’instance sélectionnée en raison de problèmes inconnus, contactez l’assistance clientèle. |
