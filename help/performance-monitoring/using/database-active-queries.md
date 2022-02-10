---
product: campaign
solution: Campaign
title: Surveillance des requêtes actives
description: Découvrez comment surveiller les requêtes actives sur vos instances Campaign dans le panneau de contrôle.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: ht
source-wordcount: '123'
ht-degree: 100%

---

# Surveillance des requêtes actives {#long-running-queries}

La zone relative aux **[!UICONTROL Requêtes actives]**, sous l’onglet **[!UICONTROL Bases de données]**, répertorie les cinq requêtes qui ont été exécutées le plus longtemps sur l’instance sélectionnée.

![](assets/active-queries.png)

Les colonnes **[!UICONTROL Durée]** indiquent la durée d’exécution d’une requête sur l’instance. La durée s’affiche au format suivant : `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Si l’une des requêtes est active depuis plus de 24 heures, vous serez averti par e-mail si vous vous êtes abonné aux [alertes par e-mail](email-alerting.md).
>
>Dans ce cas, contactez lʼassistance clientèle afin quʼelle identifie le problème et y apporte une solution. Vous devrez lui communiquer la valeur de la colonne **[!UICONTROL PID]**, qui est un identifiant unique pour la requête.
