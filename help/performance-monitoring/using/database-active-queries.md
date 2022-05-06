---
product: campaign
solution: Campaign
title: Surveillance des requêtes actives
description: Découvrez comment surveiller les requêtes actives sur vos instances Campaign dans le panneau de contrôle.
feature: Control Panel
role: Architect
level: Experienced
exl-id: a1ea14f9-ec1d-4e10-89ef-846065512e8c
source-git-commit: 7078ff03bf2e4d156a71de4d900cbfcbd2ded312
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 100%

---

# Surveillance des requêtes actives {#long-running-queries}

La zone relative aux **[!UICONTROL Requêtes actives]**, sous l’onglet **[!UICONTROL Bases de données]**, répertorie les cinq requêtes qui ont été exécutées le plus longtemps sur l’instance sélectionnée.

![](assets/active-queries.png)

Les colonnes **[!UICONTROL Durée]** indiquent la durée d’exécution d’une requête sur l’instance. La durée s’affiche au format suivant : `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Si l’une des requêtes est active depuis plus de 24 heures, contactez l’assistance clientèle afin qu’elle identifie et résolve le problème. Vous devrez alors indiquer la valeur de la colonne **[!UICONTROL PID]**, qui est un identifiant unique pour la requête.
