---
product: campaign
solution: Campaign
title: Surveillance des débits et de la latence
description: Découvrez comment surveiller les débits et la latence de vos instances Campaign dans le panneau de contrôle.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 78%

---

# Surveillance des débits et de la latence {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="À propos de la surveillance des débits et de la latence "
>abstract="Dans cet onglet, vous pouvez surveiller les fluctuations des débits de diffusion et de latence sur vos instances au cours dʼune période donnée."

La surveillance des fluctuations des débits de diffusion et de latence sur une période donnée est essentielle pour comprendre lʼutilisation de vos instances et vous assurer de leur bon fonctionnement.

Ces informations sont mises à disposition par Panneau de Contrôle pour chacune de vos instances Campaign dans le **[!UICONTROL Surveillance des performances]** carte, **[!UICONTROL Débit et latence]** (notez que le Panneau de Contrôle peut prendre jusqu’à 1 heure pour afficher les chiffres).

* La zone relative au **[!UICONTROL Débit]** fournit des informations concernant le nombre de messages envoyés par heure à partir de l’instance Campaign sélectionnée, pour tous les canaux de communication auxquels vous avez droit.

* La zone relative à la **[!UICONTROL Latence]** fournit des informations concernant la latence rencontrée sur l’instance sélectionnée lors de l’envoi de communications transactionnelles en temps réel. Les latences sont capturées et visualisées aux 95e et 99e centiles, ce qui signifie que 95 % et 99 % des requêtes doivent être plus rapides que la latence donnée.

![](assets/throughput-latencies-overview.png)

>[!NOTE]
>
>Tous les chiffres fournis dans cet onglet sont approximatifs et ne sont donnés quʼà titre indicatif.

Par défaut, les données sont affichées pour la journée en cours. Vous pouvez modifier la période affichée à l’aide des boutons **[!UICONTROL 6 mois]**, **[!UICONTROL 30 jours]** et **[!UICONTROL 7 jours]**.

Vous pouvez également visualiser les informations sous la forme d’un tableau avec des colonnes triables plutôt qu’un graphique. Pour ce faire, cliquez sur le bouton **[!UICONTROL Paramètres de visualisation]**, puis sélectionnez **[!UICONTROL Tableau]**.

![](assets/throughput-latencies-table.png)
