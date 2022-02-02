---
product: campaign
solution: Campaign
title: Surveillance des requêtes actives
description: Découvrez comment surveiller les requêtes actives sur vos instances Campaign dans le panneau de contrôle.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: 6922e132321f67e1e8122e33ead3c5e54c639763
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 100%

---

# Surveillance des requêtes actives {#long-running-queries}

La zone relative aux **[!UICONTROL Requêtes actives]**, sous l’onglet **[!UICONTROL Bases de données]**, répertorie les cinq requêtes qui ont été exécutées le plus longtemps sur l’instance sélectionnée.

![](assets/active-queries.png)

Les colonnes **[!UICONTROL Durée]** indiquent la durée d’exécution d’une requête sur l’instance. La durée s’affiche au format suivant : `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Si l’une des requêtes est active depuis plus de 24 heures, contactez l’assistance clientèle afin qu’elle identifie et résolve le problème. Dans ce cas, vous devrez communiquer la valeur de la colonne **[!UICONTROL PID]**, qui est un identifiant unique pour la requête.