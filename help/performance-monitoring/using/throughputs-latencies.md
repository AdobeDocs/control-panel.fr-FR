---
product: campaign
solution: Campaign
title: Surveillance des débits et de la latence
description: Découvrez comment surveiller les débits et la latence de vos instances Campaign dans le panneau de contrôle.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: ea738ea3764e4651e0eb7b4bcc68a9f7b3c8d1e5
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 100%

---

# Surveillance des débits et de la latence {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="À propos de la surveillance des débits et de la latence "
>abstract="Dans cet onglet, vous pouvez surveiller les fluctuations des débits de diffusion et de latence sur vos instances au cours dʼune période donnée. Pour obtenir des informations sur les diffusions qui contribuent au débit, passez en vue tabulaire."

Le Panneau de contrôle vous permet de surveiller les débits de diffusion et la latence pour chacune de vos instances.

>[!IMPORTANT]
>
>Cette fonctionnalité est disponible pour tous les clients Campaign Standard et v8, ainsi que pour les clients Campaign v7 qui ont les numéros de build 9032 et ultérieurs, y compris les [déploiements autonomes](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html?lang=fr) (sans instance MID).

La surveillance des fluctuations des débits de diffusion et de latence sur une période donnée est essentielle pour comprendre lʼutilisation de vos instances et vous assurer de leur bon fonctionnement.

Ces informations sont disponibles dans le panneau de contrôle pour chacune de vos instances Campaign, dans la vignette **[!UICONTROL Surveillance des performances]** et sous lʼonglet **[!UICONTROL Débits et latence]** (notez que le panneau de contrôle peut prendre jusqu’à 1 heure pour afficher les chiffres).

>[!NOTE]
>
>Tous les chiffres fournis dans cet onglet sont approximatifs et ne sont donnés quʼà titre indicatif.

![](assets/throughput-latencies-overview.png)

Par défaut, les données sont affichées pour la journée en cours. Vous pouvez modifier la période affichée à l’aide des boutons **[!UICONTROL 6 mois]**, **[!UICONTROL 30 jours]** et **[!UICONTROL 7 jours.]** Les données sont présentées des façons suivantes :
* Chaque heure pour les vues de 1 jour et 7 jours,
* Toutes les 6 heures pour la vue sur 30 jours,
* Chaque jour pour la vue sur 6 mois.

Vous pouvez également visualiser les informations dans un format de tableau avec des colonnes triables plutôt que dans un graphique. Pour ce faire, cliquez sur le bouton **[!UICONTROL Paramètres de visualisation]**, puis sélectionnez **[!UICONTROL Tableau]**.

![](assets/throughput-latencies-table.png)

## Débit du moniteur {#throughput}

La zone relative au **[!UICONTROL Débit]** fournit des informations concernant le nombre de messages envoyés par heure à partir de l’instance Campaign sélectionnée, pour tous les canaux de communication auxquels vous avez droit.

>[!NOTE]
>
>Pour Campaign v7/v8, le nombre affiché pour le débit correspond au débit obtenu à partir des instances MID (mid-sourcing). Pour les déploiements Stand-alone de marketing (MKT) (sans instance MID), le débit de l’instance MKT s’affiche à la place.

En outre, le panneau de contrôle vous permet de repérer les identifiants des 5 diffusions les plus importantes qui contribuent au débit pendant la période sélectionnée. Ces informations sont disponibles en vue tabulaire uniquement :

![](assets/throughput-latencies-top5.png)

## Surveiller la latence {#latency}

La zone relative à la **[!UICONTROL Latence]** fournit des informations concernant la latence rencontrée sur l’instance sélectionnée lors de l’envoi de communications transactionnelles en temps réel.

>[!NOTE]
>
>Notez que les informations relatives à **Latence de profil** sont également disponibles pour les instances [!DNL Campaign Standard] uniquement.

Les latences sont capturées et visualisées aux 95e et 99e centiles, ce qui signifie que 95 % et 99 % des requêtes doivent être plus rapides que la latence donnée.

![](assets/throughput-latencies-latency.png)

Par défaut, la latence s’affiche pour tous les canaux. Vous pouvez visualiser la latence pour un canal spécifique à l’aide de la liste déroulante.

![](assets/throughput-latencies-filter.png)

>[!NOTE]
>
>Le filtrage de canal est disponible uniquement pour les instances Campaign Classic v7/v8.
