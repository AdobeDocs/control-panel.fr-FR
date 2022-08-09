---
product: campaign
solution: Campaign
title: Surveiller les contacts principaux et les événements
description: Découvrez comment identifier les événements se produisant sur vos instances et les contacts principaux chez Adobe.
feature: Control Panel
role: Architect
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: 8d1eda31cbe6ab915760d4894a03a4a0055a3130
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 100%

---

# Surveiller les contacts principaux et les événements {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Calendrier de service"
>abstract="La section des contacts principaux dresse une liste des personnes de contact chez Adobe, que vous pouvez appeler pour toute demande ou problème se produisant sur vos instances. Dans la section Calendrier des événements du service , vous pouvez identifier les versions et les révisions de service pour l’instance sélectionnée et configurer des rappels pour les événements à venir."

>[!IMPORTANT]
>
>Le calendrier de service est disponible en version Beta et est sujet à de fréquentes mises à jour et modifications sans préavis.

Pour assurer la surveillance de vos instances Campaign, l’identification des événements planifiés sur celles-ci revêt un caractère essentiel.

Grâce au panneau de contrôle, vous pouvez surveiller les versions et les révisions de service se produisant sur vos instances, ainsi qu’accéder à une liste de contacts principaux chez Adobe pour toute demande ou problème.

Ces informations sont accessibles depuis la vignette **[!UICONTROL Calendrier de service]** sur la page d’accueil du panneau de contrôle.

## Contacts principaux {#key-contacts}

La section **[!UICONTROL Contacts principaux]** dresse une liste des personnes de contact chez Adobe, que vous pouvez appeler pour toute demande ou problème se produisant sur vos instances.

>[!NOTE]
>
>Cette section affiche des informations uniquement pour les comptes de services gérés.

![](assets/service-events-contacts.png)

Les contacts principaux exercent les rôles suivants :

* **[!UICONTROL TAM]** : gestionnaire de compte technique,
* **[!UICONTROL CSM]** : responsable du succès client,
* **[!UICONTROL Délivrabilité]** : point de contact pour les opérations de délivrabilité,
* **[!UICONTROL Gestionnaire de transition]** : gestionnaire de transition Managed Services (compte Managed Services uniquement),
* **[!UICONTROL Spécialiste de l’intégration]** : spécialiste affecté au compte pour vous aider lors de l’intégration à Campaign Classic (compte Managed Services uniquement).

## Événements {#events}

### Surveiller les événements {#monitor-events}

La section **[!UICONTROL Calendrier des événements de service]** affiche toutes les versions antérieures et à venir ainsi que les révisions de service pour l’instance sélectionnée.

![](assets/service-events-calendar.png)

La colonne **[!UICONTROL Remarque]** fournit des informations sur le statut de chaque version :

* **[!UICONTROL Disponibilité générale]** : dernier build stable disponible.
* **[!UICONTROL Disponibilité limitée]** : déploiement à la demande uniquement.
* **[!UICONTROL Release Candidate]** : validée par les ingénieurs Adobe. En attente de contrôle en production.
* **[!UICONTROL Version préliminaire]** : disponibilité anticipée pour les besoins spécifiques des clients.
* **[!UICONTROL Plus disponible]** : cette version ne contient aucun problème majeur, mais un build plus récent est disponible avec des correctifs supplémentaires. Une mise à niveau est requise.
* **[!UICONTROL Obsolète]** : le build contient des régressions connues.
Le build n’est plus pris en charge. La mise à niveau est obligatoire.

Vous pouvez attribuer un indicateur à un ou plusieurs événements à venir et ainsi en effectuer le suivi. Pour ce faire, cliquez sur le bouton Ellipse en regard du nom de l’événement.

![](assets/service-events-flag.png)

### Définir des rappels {#reminders}

Avec le calendrier de service, vous pouvez définir des rappels afin d’être averti par e-mail avant qu’un événement ne se produise.

>[!NOTE]
>
>Pour être averti des événements à venir, vous devez être abonné aux alertes par e-mail dans le panneau de contrôle. [En savoir plus](../performance-monitoring/using/email-alerting.md)

Pour définir une alerte pour un événement, procédez comme suit :

1. Cliquez sur le bouton représentant les points de suspension en regard de l’événement qui doit vous être rappelé, puis sélectionnez **[!UICONTROL Définir un rappel]**.

1. Donnez un titre au rappel, puis sélectionnez la date à laquelle vous souhaitez être averti avant l’événement.

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >Si vous ne vous êtes pas abonné aux alertes du panneau de contrôle, un message s’affiche ; vous pouvez alors vous inscrire pour recevoir des notifications par e-mail.

1. Le rappel est maintenant défini pour l’événement sélectionné. Vous pouvez le survoler à tout moment avec la souris pour voir le titre correspondant.

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >Vous pouvez configurer jusqu’à 2 rappels pour le même événement.

1. À la date spécifiée dans le rappel, un e-mail vous sera envoyé pour vous informer de l’événement à venir. Le rappel sera automatiquement supprimé des **[!UICONTROL Rappels]** dans le menu Calendrier de service.
