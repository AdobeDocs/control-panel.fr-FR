---
product: campaign
solution: Campaign
title: Top 10 des ressources temporaires
description: Découvrez comment surveiller, dans le panneau de contrôle, les 10 ressources temporaires les plus importantes générées par les workflows et les diffusions de votre base de données Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: b17abddf6bad7e58cb7bd825cd97322427a0b21f
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 79%

---

# Top 10 des ressources temporaires {#top-10}

Le **[!UICONTROL Top 10 des ressources temporaires]** répertorie les 10 plus importantes ressources temporaires générées par les workflows et les diffusions.

La surveillance des workflows et des diffusions qui créent des ressources temporaires importantes est essentielle pour surveiller votre base de données. Si une ressource temporaire consomme trop d’espace de base de données, vérifiez que ce workflow ou cette diffusion est nécessaire et, éventuellement, accédez à votre instance pour l’arrêter.

>[!IMPORTANT]
>
>À titre de recommandation générale, il est préférable d’éviter de placer **plus de 40 colonnes** dans des ressources à configurer. Si un workflow présente un grand nombre de tables ou des tailles volumineuses de base de données, nous recommandons de le vérifier afin de déterminer pourquoi il génère autant de données.
>
>Les instructions Campaign Standard et Classic sont également disponibles dans [cette page](database-preventing-overload.md) pour vous aider à éviter la surcharge de la base de données.

![](assets/database-top10.png)

Le **[!UICONTROL Afficher tout]** vous permet d’accéder à la **[!UICONTROL Présentation du stockage]** détails pour obtenir des informations détaillées sur ces ressources temporaires. Pour plus dʼinformations, consultez [cette page](database-storage-overview.md).
