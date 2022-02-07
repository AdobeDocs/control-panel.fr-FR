---
product: campaign
solution: Campaign
title: Surveillance des requêtes actives
description: Découvrez comment surveiller les requêtes actives sur vos instances Campaign dans le panneau de contrôle.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 52%

---

# Surveillance des requêtes actives {#long-running-queries}

La zone relative aux **[!UICONTROL Requêtes actives]**, sous l’onglet **[!UICONTROL Bases de données]**, répertorie les cinq requêtes qui ont été exécutées le plus longtemps sur l’instance sélectionnée.

![](assets/active-queries.png)

Les colonnes **[!UICONTROL Durée]** indiquent la durée d’exécution d’une requête sur l’instance. La durée s’affiche au format suivant : `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Si l’une des requêtes est principale depuis plus de 24 heures, vous en serez averti par email si vous vous êtes abonné à [alertes par email](email-alerting.md).
>
>Dans ce cas, contactez l’assistance clientèle afin qu’elle identifie et résolve le problème. Vous devrez leur fournir la variable **[!UICONTROL PID]** valeur de colonne, qui est un identifiant unique de la requête.
