---
product: campaign
solution: Campaign
title: Surveillance des débits et de la latence
description: Découvrez comment surveiller les débits et la latence de vos instances Campaign dans le panneau de contrôle.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: cbc068c921d0d16b49c881693e44e1ba2a90d015
workflow-type: ht
source-wordcount: '230'
ht-degree: 100%

---

# Surveillance des débits et de la latence {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="À propos de la surveillance des débits et de la latence "
>abstract="Dans cet onglet, vous pouvez surveiller les fluctuations des débits de diffusion et de latence sur vos instances au cours dʼune période donnée."

La surveillance des fluctuations des débits de diffusion et de latence sur une période donnée est essentielle pour comprendre lʼutilisation de vos instances et vous assurer de leur bon fonctionnement.

Ces informations sont disponibles dans le panneau de contrôle pour chacune de vos instances Campaign, dans la vignette **[!UICONTROL Surveillance des performances]** et sous lʼonglet **[!UICONTROL Débits et latences]**.

>[!NOTE]
>
>Tous les chiffres fournis dans cet onglet sont approximatifs et ne sont donnés quʼà titre indicatif.

![](assets/throughput-latencies-overview.png)

Par défaut, les données sont affichées pour la journée en cours. Vous pouvez modifier la période affichée à l’aide des boutons **[!UICONTROL 6 mois]**, **[!UICONTROL 30 jours]** et **[!UICONTROL 7 jours]**.

La zone relative au **[!UICONTROL Débit]** fournit des informations concernant le nombre de messages envoyés par heure à partir de l’instance Campaign sélectionnée, pour tous les canaux de communication auxquels vous avez droit.

Vous pouvez également visualiser ces informations dans un format de tableau avec des colonnes triables plutôt que dans un graphique. Pour ce faire, cliquez sur le bouton **[!UICONTROL Paramètres de visualisation]**, puis sélectionnez **[!UICONTROL Tableau]**.

![](assets/throughput-latencies-table.png)

La zone relative à la **[!UICONTROL Latence]** fournit des informations concernant la latence rencontrée sur l’instance sélectionnée lors de l’envoi de communications transactionnelles en temps réel. Les latences sont capturées et visualisées aux 95e et 99e centiles, ce qui signifie que 95 % et 99 % des requêtes doivent être plus rapides que la latence donnée.

![](assets/throughput-latencies-latency.png)
